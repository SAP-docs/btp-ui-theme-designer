<!-- loioab10b7d57dcc47f7a189a97e715c0d30 -->

# Supporting the `sap-theme` URL Parameter

The `sap-theme` URL parameter is the standard way of communicating the desired Theme ID and Theme Root to an application. UI technologies like UI5 Web Components or SAPUI5 use it to apply the desired theme. You only have to support it if you do not use a UI technology that already supports it.

On a high level, you parse `sap-theme=${themeId}@${themeRoot}` and load `${themeRoot}/Base/baseLib/${themeId}/css_variables.css`. For security, you only load themes from theme roots you trust. For resilience, you load a default theme from a default theme root first, and update the default theme to match the actual theme, once this is successfully loaded.

> ### Note:  
> The approach below work for themes and theme sets equally. Internally, theme sets use media queries to conditionally apply the included appearances based on the user agent settings of the end user. See [MDN: prefers-color-scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-color-scheme) and [MDN: prefers-contrast](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-contrast) for details.



## Procedure

1.  Define your default theme and default theme root:
    -   The default theme root is ideally the content folder of the [@sap-theming/theming-base-content](https://www.npmjs.com/package/@sap-theming/theming-base-content) npm package that you developed your application against, served by a CDN or hosted by yourself.
    -   You can pick the default theme as you like, usually the low-contrast light appearance of the latest theme provided by SAP \(such as `sap_horizon`\).

2.  Load the `css_variables.css` of the default theme from the default theme root, which is located in the `baseLib` library of the Base framework. That way, your application will remain usable even if the UI Theme Designer service is unavailable.
3.  Load your own CSS from wherever you’d like. It should make use of the CSS custom properties provided in the `css_variables.css` to adapt to different themes.
4.  Parse the sap-theme URL parameter.
    -   The part before the `@` is the `themeId`.
    -   The part after the `@` is the `themeRoot`. `@` and `themeRoot` are optional; use your default theme root if they are not available.

5.  If there is a `themeRoot` and it’s different to your default theme root, verify that it’s from a source you trust. You could introduce the meta tag to define whom you trust \(you still have to check against that list manually, unless you use a UI technology that does that for you, like UI5 Web Components or SAPUI5 that call this meta tag `<meta name="sap-allowed-theme-origins" content="comma-separated-list-of-trusted-protocol-host-and-port-tuples">`\).
6.  If `themeId` or `themeRoot` differ from your defaults, load the `css_variables.css` of the desired theme from the desired theme root in addition to the `css_variables.css` you already loaded from your defaults.
7.  Once the desired `css_variables.css` file is applied, evaluate the CSS custom property `--sapSapThemeId`. If your theme differs from the default one, update the `href` of the `<link>` that loads the default `css_variables.css`. Point it to the `--sapSapThemeId` theme in your default theme root.

    > ### Note:  
    > Do not add a new `<link>` after the custom theme's `css_variables.css`. Adding a new default theme link would override the custom theme.

    This ensures that you have default values for all theming parameters you rely on, even if the custom theme was built with an older Theming Base Content than what you developed with.

8.  If your own CSS is theme-dependent, update the `href` of that `<link>` as well.



## Example

This example shows the complete bootstrap process described above. Use this approach if you do not have access to a UI technology that manages these steps for you. The example assumes the following conditions:

-   You reference `@sap-theming/theming-base-content` as an npm module from the jsDelivr CDN.
-   Your custom styles are in `/assets/my-own-styles.css`.
-   You use sap\_horizon as the default theme.
-   You want to allow themes from your application router at https://example.com as well.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Example of a themable application</title>
    <link id="default-theme" rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@sap-theming/theming-base-content/content/Base/baseLib/sap_horizon/css_variables.css">
    <link id="my-own-styles" rel="stylesheet" href="/assets/my-own-styles.css">
    <meta name="sap-allowed-theme-origins" content="https://example.com">
    <link id="custom-theme" rel="stylesheet">
  </head>
  <body>
    <h1 style="font-family: var(--sapFontHeaderFamily); font-size: var(--sapFontHeader1Size); color: var(--sapTextColor)">It works!</h1>
    <script>
    const DEFAULT_THEME = 'sap_horizon';
    const DEFAULT_THEME_ROOT = 'https://cdn.jsdelivr.net/npm/@sap-theming/theming-base-content/content';

    const [themeId, themeRoot = DEFAULT_THEME_ROOT] = decodeURIComponent(new URLSearchParams(location.search).get('sap-theme') || DEFAULT_THEME).split('@');
    const allowedThemeOrigins = [DEFAULT_THEME_ROOT, ...document.querySelector('meta[name="sap-allowed-theme-origins"][content]')?.content.split(',')].map(url => new URL(url).origin);

    if (allowedThemeOrigins.includes(new URL(themeRoot).origin) && (themeId !== DEFAULT_THEME || themeRoot !== DEFAULT_THEME_ROOT)) {
      const customTheme = document.getElementById('custom-theme');
      customTheme.addEventListener('load', () => requestAnimationFrame(() => {
        const sapSapThemeId = getComputedStyle(document.body).getPropertyValue('--sapSapThemeId');
        if (sapSapThemeId !== DEFAULT_THEME) {
          document.getElementById('default-theme').href = `${DEFAULT_THEME_ROOT}/Base/baseLib/${sapSapThemeId}/css_variables.css`;
        }
      }));
      customTheme.href = `${themeRoot.replace(/\/$/, '')}/Base/baseLib/${themeId}/css_variables.css`;
    }
    </script>
  </body>
</html>
```



## Results

With the steps described above, you get an application that supports the sap-theme URL parameter to be themeable, while being secure and resilient.



## Next Steps

Go ahead and use your themeable application in an existing application launcher like SAP Build Work Zone, or validate theme IDs and determine their theme roots yourselves as described in [Determining Theme ID and Theme Root](determining-theme-id-and-theme-root-c612d38.md).

