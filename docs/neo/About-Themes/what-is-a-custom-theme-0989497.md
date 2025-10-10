<!-- copy0989497d60fe4d5db2b3b22be38e9473 -->

# What is a Custom Theme?

A custom theme is a theme you create with the UI theme designer to apply your corporate branding to SAP applications.

Custom themes are always based on an existing SAP theme and include your specific adaptations—such as a company logo, changes to main theming colors, or control-specific color adjustments.



## What Can You Customize in a Theme?

Most theming parameters are related to colors, but you can also customize certain images, font properties, and a limited set of dimension parameters.

-   **You can customize:**
    -   Main colors and colors for various UI elements
    -   Images, such as the company logo or background images for the shell and applications
    -   Border radius \(for example, for buttons and tiles\)
    -   Fonts, either by selecting a common font family or using a web font

-   **You can also adjust some dimension parameters, with limitations:**
    -   Border width
    -   Border radius
    -   Shadows


> ### Remember:  
> Changes to dimension parameters should be made with caution, as altering dimensions can potentially disrupt application layouts.



## Structure of a Custom Theme

The structure of a custom theme mirrors that of SAP themes. For more details, see [Overview of SAP Theming Content](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/91ebfe2a14204244bd052a03018d6781.html "SAP Theming Content is the set of parameters and assets that define branding and visual styles across SAP applications.") :arrow_upper_right:. Custom themes contain only the delta information—meaning only the changes you made compared to the base SAP theme are saved. When a custom theme is compiled, both your customizations and the base SAP theme are combined to generate the final theme.

In this documentation, we use the term "theme" generically when the context is clear. When it is necessary to distinguish, we explicitly refer to "SAP themes" or "custom themes."

Because a custom theme only stores the differences from the base SAP theme, its structure will vary depending on the specific changes you have made. Typically, it includes the same framework and library organization as SAP themes, along with metadata files \(such as `.theming` files\).

**Example:**

An exported ZIP file of a custom theme including an uploaded logo, a shell background image, and changes to main colors.

```
.
├── Base
│    └── baseLib
│         ├── .theming
│         ├── base.less
│         ├── css_variables.less
│         ├── custom.less
│         ├── img
│         │    └── misc
│         │          ├── sapCompamyLogo.png
│         │          └── sapShell_BackgroundImage.png
│         └──  ...
├── UI5
│    └── ...
├── UR
│    └── ...
├── exportThemesInfo.json
└── neo-app.json
```

When a custom theme is compiled, it also generates a corresponding CSS file for each LESS file, as well as a theme avatar to visually represent the theme.

**Related Information**  


[SAP Design System: SAP Fiori for Web](https://www.sap.com/design-system/fiori-design-web/?external)

[SAP Design System: Design Tokens](https://www.sap.com/design-system/fiori-design-web/foundations/visual/design-tokens?external)

[SAP Design System: Theming](https://www.sap.com/design-system/fiori-design-web/foundations/visual/theming?external)

