<!-- copy3b7df83134e1426fb4def49abe0a0e34 -->

# Overview of SAP Theming Content

SAP Theming Content is the set of parameters and assets that define branding and visual styles across SAP applications.



<a name="copy3b7df83134e1426fb4def49abe0a0e34__section_sfw_tp4_12b"/>

## What is the SAP Theming Content?

The theming content is the implementation of the [SAP Fiori for Web Design System](https://www.sap.com/design-system/fiori-design-web/?external). It delivers the foundational styles and resources for multiple SAP themes, such as Horizon and Quartz. [Design Tokens](https://www.sap.com/design-system/fiori-design-web/foundations/visual/design-tokens?external) from the SAP Design System are mapped directly to theming parameters within the theming content. While [LESS](https://lesscss.org/) is currently the main technology used, the theming content is evolving towards greater use of [CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_cascading_variables/Using_CSS_custom_properties) for more flexibility and modern web standards.

The theming content includes:

-   Theming parameters defined in LESS files
-   Fonts for typography and icons
-   Images and graphical assets
-   Metadata describing each theme



<a name="copy3b7df83134e1426fb4def49abe0a0e34__section_o2s_3q4_12b"/>

## Structure of the Theming Content

The theming content is organized into frameworks and libraries. The Base framework serves as the foundation for all supported SAP UI technologies. If a specific UI technology requires its own theming resources, it is represented by its own framework within the theming content.

```
├── Base
│    └── baseLib
├── UI5
│    ├── sap/ui/core
│    ├── sap/m
│    ├── sap/ui/ushell
│    └── ...
├── UR
│    ├── baseLib
│    ├── ls
│    ├── c2
│    └── ...
└── ...
```

Each library provides theming information for multiple SAP themes. The base theme is the foundation of all SAP themes; other SAP themes have the prefix “sap\_”. In general, the SAP themes inherit all theming information from the base theme. See, for example, the Base framework:

```
├── Base
│    └── baseLib
│         ├── baseTheme
│         ├── sap_horizon
│         ├── sap_horizon_dark
│         ├── sap_horizon_hcb
│         ├── sap_horizon_hcw
│         └── ...
└── ...
```



<a name="copy3b7df83134e1426fb4def49abe0a0e34__section_ppd_vp4_12b"/>

## Metadata

Metadata is available in `.themin`g files for

-   Frameworks, for example [/Base/.theming](https://github.com/SAP/theming-base-content/blob/master/content/Base/.theming)
-   Libraries, for example [/Base/baseLib/.theming](https://github.com/SAP/theming-base-content/blob/master/content/Base/baseLib/.theming)
-   Themes, for example [/Base/baseLib/sap\_horizon/.theming](https://github.com/SAP/theming-base-content/blob/master/content/Base/baseLib/sap_horizon/.theming).

The metadata include information such as the entity type, ID, description and further information required for the compilation of a theme or theme set.



## Supported SAP Themes and Theme Sets

The following SAP themes are currently supported for creating custom themes:

-   SAP Horizon \(Set\) \(`sap_horizon_set`\)
    -   SAP Morning Horizon \(`sap_horizon`\)
    -   SAP Evening Horizon \(`sap_horizon_dark`\)
    -   SAP High-Contrast White \(Horizon\) \(`sap_horizon_hcw`\)
    -   SAP High-Contrast Black \(Horizon\) \(`sap_horizon_hcb`\)

-   SAP Quartz \(Set\) \(`sap_fiori_3_set`\)
    -   SAP Quartz Light \(`sap_fiori_3`\)
    -   SAP Quartz Dark \(`sap_fiori_3_dark`\)
    -   SAP High-Contrast White \(Quartz\) \(`sap_fiori_3_hcw`\)
    -   SAP High-Contrast Black \(Quartz\) \(`sap_fiori_3_hcb`\)




For the most modern look and optimal accessibility, it is recommended to use the latest SAP Horizon themes when creating custom themes. To learn more about the reference palette and the design principles \(DNA\) of SAP themes, see [SAP Design System: Color Overview](https://www.sap.com/design-system/fiori-design-web/v1-142/foundations/visual/colors-overview).

The reference palette and parameter dependencies may vary between themes. For details, review [Theme Parameter Dependencies](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/18d80b4f0aec482a98bbd9a8bc289749.html "") :arrow_upper_right:.



The list of supported themes may vary depending on the UI framework and its version:

-   For SAPUI5, see [Supported Combinations of Libraries and Themes](https://ui5.sap.com/#/topic/38ff8c27b022475a92b591bcf6262551)
-   For SAP GUI for HTML, see SAP Note [254097](https://me.sap.com/notes/254097) - Supported Themes for SAPGUI for HTML
-   For Web Dynpro ABAP, see [Web Dynpro ABAP - Theming support matrix](https://help.sap.com/docs/SUPPORT_CONTENT/wdabap/3362186816.html#Stylesheetsandthemes-matrix)



## Accessibility

SAP themes are designed with accessibility standards in mind, including features such as color contrast and text resizing, to ensure inclusivity and usability for all users. For details on the WCAG target version supported by a specific SAP theme, refer to [SAP Design System: Accessibility](https://www.sap.com/design-system/fiori-design-web/foundations/visual/theming?external#accessibility).

**Related Information**  


[SAP Design System: SAP Fiori for Web](https://www.sap.com/design-system/fiori-design-web/?external)

[SAP Design System: Design Tokens](https://www.sap.com/design-system/fiori-design-web/foundations/visual/design-tokens?external)

[SAP Design System: Theming](https://www.sap.com/design-system/fiori-design-web/foundations/visual/theming?external)

[MDN: Using CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_cascading_variables/Using_CSS_custom_properties)

[LESS](https://lesscss.org/)

[GitHub Theming Base Content](https://github.com/SAP/theming-base-content)

