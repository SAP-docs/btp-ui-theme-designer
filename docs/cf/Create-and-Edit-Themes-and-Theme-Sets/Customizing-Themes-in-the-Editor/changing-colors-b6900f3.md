<!-- loiob6900f3e9cf649d095e3b057924c4c0f -->

# Changing Colors

You can change the colors of your theme, either by using the color picker or by entering the value directly.

The value can simply be a color, such as a hex value, a reference to a parameter, or any LESS 1.6.3 color expression.



## Prerequisites

You are working in the editor as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).



## Procedure

Find the color parameter you want to change. Color parameters have a color swatch next to their value input.

**To change a color with the color picker:**

1.  Open the color picker by selecting the color swatch, or by selecting [F4\].
2.  Select a color using the color picker. You can choose from hue-saturation-lightness \(HSL\), red-green-blue \(RGB\), both with an alpha channel, or from palette parameters you create as described in [Reusing Color Parameters](reusing-color-parameters-16ed37f.md). The preview and color swatch update with every change.
3.  Select *OK* to confirm the new color or revert to the old one with *Cancel.*

**To enter a value directly:**

You can manually enter the value you want for the parameter you want to change. The value can be any LESS expression that evaluates to a color, especially:

-   An RGB hex value with three or six digits, such as `#333` or `#0070f2`.
-   A reference to an existing color parameter, such as `@sapBrandColor` or `@myPaletteParameter`. See [Reusing Color Parameters](reusing-color-parameters-16ed37f.md) for details on how to define your own parameters for reuse.
-   A color function such as `lighten(...)` or `fade(...)`. See [LESS: Functions](https://lesscss.org/functions/) for details on available LESS functions. For example, you can create a complementary color of the Brand Color with a defined lightness of 70% by using a value like `spin(hsl(hue(@sapBrandColor), saturation(@sapBrandColor), 70%), 180)`.

> ### Note:  
> Themes use LESS 1.6.3 and support only the language features available in that version. You can't use modern color spaces such as `oklab(...)`. If you need to use these color spaces, escape the value -`~"oklab(0.572 -0.044 -0.209)"`. But then make sure that no other parameter uses a color function on the value you changed because LESS no longer treats the value as a color, and using color functions on it causes a build error.



## Result

The preview updates automatically.



## Next Steps

Save your theme as described in [Saving Themes](saving-themes-c99d9df.md).

