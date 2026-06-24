<!-- copyad000cde148843e4a83262c446a350b3 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Adding Custom CSS

You can add custom CSS for different UI technologies to your theme.



<a name="copyad000cde148843e4a83262c446a350b3__prereq_N1001D_N1001A_N10001"/>

## Prerequisites

-   You have the `CustomCssEditor (sap-theming)` role as described in [Permissions](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/c3fdb69e274f4d9bb33139763faa7a1f.html "UI theme designer defines different permissions, that administrators can set up access for editing themes.") :arrow_upper_right:.
-   You are working in the editor as described in [Customizing Themes in the Editor](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/aa4b233eb1da4f30ae6d888424a92de5.html "In the editor you can make changes to themes and preview them.") :arrow_upper_right:.



<a name="copyad000cde148843e4a83262c446a350b3__context_N10014_N10011_N10001"/>

## Context

Adding custom CSS lets you make advanced changes of your theme that aren't possible by changing theme parameters alone. Use this option with caution.

> ### Note:  
> -   SAP does not take responsibility for changes you make with custom CSS. If you create an incident as described in [Getting Support](https://help.sap.com/docs/ui-theme-designer/ui-theme-designer/getting-support?state=DRAFT), and the problem does not occur without custom CSS, SAP does not investigate the issue.
> -   Custom CSS runs the risk of breaking when the CSS or HTML structure of the targeted UI technology changes. Your custom CSS will eventually stop functioning when the version of the targeted UI technology is updated. You'll need to make manual adjustments as needed.
> -   Check whether you can achieve your target design using [Expert Theming](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/7b01607cb9564f6d94087a6db995c350.html "If you need to make changes beyond what or offer, use expert theming. This option lets you browse all available parameters and make fine-tuned adjustments to your theme.") :arrow_upper_right:. Use this approach whenever possible.
> -   Technically, what you author is not CSS but LESS \(and specifically LESS 1.6.3\). Some modern CSS features, like container queries, typed properties or modern color spaces, are not available and using them leads to build errors. Other features might be interpreted as LESS, and you have to escape them to keep them as CSS; for example, LESS would evaluate `calc(100% - 2px)` to `calc(98%)`, and you have to escape it as `~"calc(100% - 2px)"` to keep it.



## Procedure

1.  In the *Editor* pane, select *CSS*. If the *CSS* tab is missing, check that you have the `CustomCssEditor (sap-theming)` role.

2.  Select the *UI Technology* you want to add custom CSS for, for example *SAPUI5, UR* \(Unified Rendering\) or *Base* \(all other UI technologies\).

    > ### Note:  
    > -   You can add custom CSS only for UI technologies included in the selected preview. Make sure you select a preview of the UI technology where you want to add custom CSS. *Base* is always present.
    > -   Custom CSS is applied only to the UI technology you added it to. For example, adding custom CSS to SAPUI5 does not affect UR-based applications.
    > -   Custom CSS of the *Base* UI technology is generated as a copy of the custom CSS of SAPUI5 and UR whenever the theme is opened in the editor. Changes you make manually are overwritten. To stop the auto-generation and make your changes to *Base* permanent, remove the following line from the Base custom CSS: `DELETE_THIS_LINE_TO_MAKE_CHANGES_PERMANENT`.

3.  Enter your CSS code in the editor.

4.  Choose *Apply* or select [Ctrl\] + [Shift\] + [A\]  \(on macOS [Cmd\] + [Shift\] + [A\]  \).




<a name="copyad000cde148843e4a83262c446a350b3__result_N10037_N10012_N10001"/>

## Results

Your custom CSS is added to the CSS of the UI technology you selected. The preview updates automatically.



## Example

**To make your palette parameters available as CSS custom properties:**

Suppose you have created the palette parameters `myBlue` and `myGreen` as described in [Reusing Color Parameters](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/16ed37f3d20a48b49c71108017caf0a8.html "You can create your own Palette of color parameters and reference them throughout your theme.") :arrow_upper_right:, and you want to use them in the otherwise theme-independent CSS of your own custom SAPUI5 control `com.example.MyButton`.

So you select a SAPUI5 preview in the *Preview Pages* pane and open the *CSS* tab in the *Editor* pane.

Remember that the custom CSS is actually LESS, and you can reference your palette parameters as LESS variables. You can add the following custom CSS:

```
:root {
  --myBlue: @myBlue;
  --myGreen: @myGreen;
}
```

You can now use them in the styles of your `com.example.MyButton` SAPUI5 control. You don't have to include them in your theme's CSS. You can keep the control CSS with the implementation of the control. For example, you can use a `style.css` file and reference it from the control manifest, as described in UI5 Demo Kit: [Step 14: Custom CSS and Theme Colors](https://ui5.sap.com/#/topic/723f4b2334e344c08269159797f6f796)\):

```
.myButton--blue {
  background-color: var(--myBlue, blue);
}
.myButton--green {
  background-color: var(--myGreen, green);
}
```

**To use your own font:**

Suppose you want to use your own font instead of 72. You are aware that you need to provide different fonts for different weights, with very specific characteristics. For example, `SemiboldDuplex` at font-weight 400 must appear as `semibold` but occupy the same space as the standard font's regular weight.

SAP Note [3534039](https://me.sap.com/notes/3534039) - *Using a custom font in a theme* describes the process in detail. In summary, you need to provide @font-face definitions for all your fonts in your custom CSS. These definitions point to URLs where your fonts are hosted or include the fonts directly as `base64-encoded` data URLs. After you define the fonts, change the font-family parameters, such as `sapFontFamily`.

With your font `MyFont` hosted at `example.com/fonts`, you can use the following custom CSS for all UI technologies, to define both a regular and a bold version:

```
@font-face {   font-family: ‘MyFont’;
  src: url(‘https://example.com/fonts/MyFont.woff2’) format(‘woff2’);
  font-weight: normal;
  font-style: normal; }
@font-face {
  font-family: ‘MyFont’;
  src: url(‘https://example.com/fonts/MyFont-Bold.woff2’) format(‘woff2’);
  font-weight: bold;
  font-style: normal;
}
@font-face {
  font-family: ‘MyFont-Bold’;
  src: url(‘https://example.com/fonts/MyFont-Bold.woff2’) format(‘woff2’);
  font-weight: normal;
  font-style: normal;
}

```

This allows you to change `sapFontFamily` to `MyFont` and, for example, `sapFontHeaderFamily` to `MyFont-Bold`.

Keep in mind that this is only a small subset of the fonts you need to overwrite. For a complete list, refer to the `@font-face` definitions in the [`css_variables.css` of Morning Horizon](https://github.com/SAP/theming-base-content/blob/master/content/Base/baseLib/sap_horizon/css_variables.css). You can choose to use the "full" versions and omit the `unicode-ranges`. These ranges serve only as a performance optimization.

**To replace an icon:**

Suppose you need to replace an icon of the SAP-icons. You have identified the Unicode glyph of the icon you need to replace with [Theming base content: SAP-icons](https://sap.github.io/theming-base-content/docs/#/icons/SAP-icons). You have created your own font that contains just your new icon exactly at the glyph you’ve identified.

As in the “use your own font” example above, you have to either host this icon font somewhere, or inline it as the `base64` data URL of the `@font-face` definitions in your custom CSS. Then the idea is to restrict your font to only the glyphs you need to replace using a `unicode-range`, and keep using the original SAP-icons everywhere else.

If you have a font that contains the glyphs 0xe026 <span class="SAP-icons-V5"></span> and 0xe0b6 <span class="SAP-icons-V5"></span> at `example.com/fonts/MySAP-icons.woff2`, your custom CSS for all UI technologies would be:

```
@font-face {
  font-family: ‘SAP-icons’;
  src: url(‘https://example.com/fonts/MySAP-icons.woff2’) format(‘woff2’);
  font-weight: normal;
  font-style: normal;
  unicode-range: U+E026, U+E0b6;
}
```



## Next Steps

Save your changes as described in [Saving Themes](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/c99d9df29d3c4a45a883e15ce2753178.html "You can save changes you made in your theme at any time during its creation and design.") :arrow_upper_right:.

