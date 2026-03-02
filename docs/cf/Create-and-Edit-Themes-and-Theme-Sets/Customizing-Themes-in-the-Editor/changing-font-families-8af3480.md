<!-- loio8af3480eac4944be9262309871af03ac -->

<link rel="stylesheet" type="text/css" href="../../css/sap-icons.css"/>

# Changing Font Families

You can change font families. Use this option with caution. Changing the font family can affect text width and impact the layout of SAP Build Work Zone sites and applications.



## Prerequisites

You use [Expert Theming](expert-theming-7b01607.md).



## Procedure

1.  Search for the term *Family*.

2.  Enter a prioritized list of font family names or generic family names for the theming parameter you want to change.

    -   You can enter multiple font family names for each parameter. Use single or double quotes if the names contain spaces, and separate each name with a comma. For each character, the browser uses the first available font in your list that contains that character. For more information about font families on the web, see the "Font families" section of [MDN: Text and font fundamentals](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Text_styling/Fundamentals#font_families).
    -   You are responsible for ensuring that the fonts you use are available to end users of your theme. Use web-safe or default fonts, or provide `@font-face` definitions for your own fonts in custom CSS. For a list of web-safe fonts, see [cssfontstack.com](https://www.cssfontstack.com/). To use your own fonts, refer to the **To use your own font:** example in [Adding Custom CSS](adding-custom-css-895a4b0.md) for instructions on including `@font-face` definitions.
    -   There are separate font family parameters for different font weights. Each font displays at the intended weight when you set it to `font-weight 400`. For example: a font you use for `sapFontBoldFamily` appears bold at `font-weight 400`.
    -   The font you use for `sapContent_IconFontFamily` must have icons at the same unicode glyphs as the SAP-icons font. Explore the glyphs at [Theming base content: SAP-icons](https://sap.github.io/theming-base-content/docs/#/icons/SAP-icons). For example, if you replace the whole SAP-icons font, your font needs to include a glyph that represents *Refresh* <span class="SAP-icons-V5"></span> at unicode `0xe010`. See the **To replace an icon:** example of [Adding Custom CSS](adding-custom-css-895a4b0.md) for an alternative: Use your own version of SAP-icons with `unicode-range` to change only the icons you need. This approach avoids changing `sapContent_IconFontFamily` and duplicating all the icons.

    > ### Note:  
    > -   You can also change the most impactful font families in the **Text Attributes** section of the [Detailed Theming](detailed-theming-db09bb9.md) menu.
    > -   The recommended preview page for adapting font families is Text \(SAPUI5 Controls\). For more information about working with preview pages, see **Best Practices for Selecting Preview Pages** in [Selecting and Adding Preview Pages](selecting-and-adding-preview-pages-8988483.md).




## Results

The preview updates automatically.



## Next Steps

Save your theme as described in [Saving Themes](saving-themes-c99d9df.md).

