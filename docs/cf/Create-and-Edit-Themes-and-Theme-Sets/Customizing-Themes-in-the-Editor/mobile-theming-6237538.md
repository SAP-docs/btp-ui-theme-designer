<!-- loio6237538bfaaa41a8b60f8c24b81083c8 -->

# Mobile Theming

Mobile theming displays the theming parameters supported by SAP Mobile Start.



## Prerequisites

You are working in the editor as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).



## Context

You can apply your theme to both web applications and the native mobile application SAP Mobile Start. SAP Mobile Start uses a different design system than SAP Fiori for Web. The mobile design system depends on the mobile operating system. Only a limited set of theming parameters affects the mobile design. For detailed information about parameter support, see [SAP Mobile Start: Themes for Custom Corporate Branding](https://help.sap.com/docs/mobile-start/mobile-start-administration-guide/themes-for-custom-corporate-branding-overview?version=2.5).



## Procedure

1.  In the *Editor* pane, select *Mobile*.

2.  **Optional:** Select one of the preview pages from the SAP Mobile Start Applications test suite as described in [Selecting and Adding Preview Pages](selecting-and-adding-preview-pages-8988483.md). These preview pages are specifically designed to show the effects of the subset of parameters used by SAP Mobile Start.

3.  Change the parameter values according to your needs as described in [Changing Parameters](changing-parameters-0d328f8.md).




## Results

The preview updates automatically.

> ### Note:  
> You can generally use the same theme for both web and native mobile applications. However, since the mobile design relies on the operating system’s design system, some adjustments may be necessary for mobile. You may also want to create a separate theme specifically for mobile. In this case, you can use the [Duplicating Themes and Theme Sets](../duplicating-themes-and-theme-sets-ec77044.md) feature to copy your theme, including your changes, and make further adjustments as needed.



## Next Steps

Export your theme as described in [Exporting Themes and Theme Sets](../exporting-themes-and-theme-sets-26e5140.md). Select *Source Files + CSS Resources* and deselect *UR* and *SAPUI5*, as described in [SAP Mobile Start: Themes for Custom Branding \(iOS\)](https://help.sap.com/docs/mobile-start/mobile-start-administration-guide/themes-for-custom-corporate-branding-ios) or [SAP Mobile Start: Themes for Custom Corporate Branding \(Android\)](https://help.sap.com/docs/mobile-start/mobile-start-administration-guide/themes-for-custom-corporate-branding-android). After exporting, import your theme into SAP Mobile Start by following the instructions in the respective documentation for iOS or Android.

