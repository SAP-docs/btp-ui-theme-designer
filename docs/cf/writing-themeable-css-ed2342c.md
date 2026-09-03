<!-- loioed2342c0312f42029f9da6a7649e9783 -->

# Writing Themeable CSS

SAP Theming Content provides a variety of CSS custom properties that you can use to make your application themeable.

The SAP Design System is structured so that you can build applications using only the available CSS custom properties. For more information, see [Overview of SAP Theming Content](About-Themes/overview-of-sap-theming-content-91ebfe2.md).

Advanced theming needs, such as base-theme-dependent delta CSS or additional parameters derived from SAP Theming Content's CSS custom properties, can be achieved with modern CSS features like relative colors, nested selectors, or container style queries.



## Context

The main building blocks and techniques you can use to write themeable CSS are:

-   Giving CSS custom properties a value with, for example:

    ```
    --my-color: #123456;
    ```

-   Actually defining a CSS custom property with type \(syntax\) and behavior with, for example:

    ```
    @property --my-color {  
      syntax: '<color>';  
      inherits: true; 
      initial-value: #000;}
    
    ```

-   Using a CSS custom property with, for example:

    ```
    @property --my-color {  
      syntax: '<color>';  
      inherits: true; 
      initial-value: #000;}
    
    ```

-   Calculating with CSS values with, for example:

    ```
    calc(var(--my-dimension) / 2)
    ```

-   Clamping CSS values between a minimum and a maximum with, for example:

    ```
    clamp(0, var(--my-dimension), 1)
    ```

-   Relative colors, for example:

    ```
    hsl(from #123456 h s l / a)
    ```

-   Container style queries against custom properties, for example:

    ```
    @container style(--my-color: #123456) {  
      body {    
        --my-contrast-color: #fff;  
      }
    }
    ```

-   Nested rules, for example:

    ```
    html[dir=rtl] {  
      body {    
        --my-icon-content: '\e1ed';   
      }
    }
    ```

-   Logical properties, for example:

    ```
    padding-inline-start: 0.25rem;
    ```


There are many more exciting modern CSS features. This is the subset that we think is sufficient to implement themeable applications with the SAP Theming Content.

Use MDN: [CSS: Cascading Style Sheets](https://developer.mozilla.org/en-US/docs/Web/CSS) as an entry point to explore the capabilities in more detail.



## Prerequisites

Your application loads `${themeId}/Base/baseLib/${themeRoot}/css_variables.css` as described in [Supporting the sap-theme URL Parameter](supporting-the-sap-theme-url-parameter-ab10b7d.md).



## Procedure



### To use existing CSS custom properties

Reference the CSS custom property you intend to use with `var()`. For example:

```
my-button {
  background-color: var(--sapButton_Background);
}
```



### To derive colors from existing CSS custom properties

Use CSS relative colors and `calc()` to derive from existing CSS custom properties. See MDN: [Using relative colors](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Colors/Using_relative_colors) for details. For example \(with the `oklch()` color space, you could use other color spaces like `xyz()` or `hsl()` as well\):

```
my-button {
  --lighten-by-10-percent: oklch(from var(--sapButton_Background) calc(l + 0.1) c h);
  --saturate-by-20-percent: oklch(from var(--sapButton_Background) l calc(c + 0.2) h);
  --hue-rotate-by-30-percent: oklch(from var(--sapButton_Background) l c calc(h + 0.3));
}
```



### To pick a color based on contrast against CSS custom property

There are plans for a `color-contrast()` CSS primitive that, in the simplest iteration, would resolve to either black or white, depending on which has the higher contrast against the input color. Until it is available in the baseline, you can use modern color spaces and calculations with `clamp()` to mimic this primitive:

```
:root {
  --my-contrast-color: oklch(from var(--my-color) clamp(0, (l / 0.623 - 1) * -infinity, 1) 0 0);
}
```

This has a shortcoming: `--my-contrast-color` will either be black or white. To hand-pick colors depending on contrast, you need to store this black or white in an intermediate custom property, use a container style query to inspect its value, and act depending on that. To inspect the value, you must define it as a color – not just any property with a value:

```
@property --my-black-or-white {syntax: '<color>'; inherits: true; initial-value: #000;}

:root {
  /* same oklch() as above */
  --my-black-or-white: oklch(from var(--my-color) clamp(0, (l / 0.623 - 1) * -infinity, 1) 0 0);
}

@container style(--my-black-or-white: oklch(0 0 0)) {
  --my-contrast-color: var(--sapTextColor); /* --my-contrast-color is black-ish */
}

@container style(--my-black-or-white: oklch(1 0 0)) {
  --my-contrast-color: var(--sapContent_ContrastTextColor); /* --my-contrast-color is white-ish */
}
```



### To add delta CSS based on the applied SAP theme

The CSS custom property `--sapSapThemeId` contains the theme ID of the theme \(if it’s an SAP theme\) or the SAP theme it is based on \(if it’s a custom theme\). With that, you can target the SAP theme with a container style query:

```
@container style(--sapSapThemeId: sap_horizon) {
  /* styles for sap_horizon */
  body {
    --my-color: #123456;
  }
}

@container style(--sapSapThemeId: sap_horizon_dark)
  or style(--sapSapThemeId: sap_horizon_hcb)
  or style(--sapSapThemeId: sap_fiori_3_dark)
  or style(--sapSapThemeId: sap_fiori_3_hcb) {
  /* styles for all dark and high-contrast black themes */
  body {
    --my-color: #abcdef;
  }
}
```



### To work with right-to-left reading modes

Use logical properties:

```

my-button {
  /* custom properties just to illustrate the replacement */
  padding-block-start: var(--deprecated-padding-top);
  padding-block-end: var(--deprecated-padding-bottom);
  padding-inline-start: var(--deprecated-padding-left);
  padding-inline-end: var(--deprectated-padding-right);
  /* same for margin-block-start, margin-block-end, ... */
}
```

