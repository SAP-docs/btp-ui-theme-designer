<!-- loio25896d06a71a4bc190833c5947f6fdcd -->

# Running a Custom Theme via a URL Parameter

Administrators can run SAPUI5 applications with a custom theme using a URL parameter.



<a name="loio25896d06a71a4bc190833c5947f6fdcd__prereq_evl_cty_y3b"/>

## Prerequisites

-   You have published your theme to SAP BTP.

-   You have added a route to the theming service. For more information, see [Applying Custom Themes to SAPUI5 Apps](applying-custom-themes-to-sapui5-apps-eeb654b.md).


To run SAPUI5 applications with a custom theme, you can use the URL parameter `sap-theme` to set or override the initial theme.



<a name="loio25896d06a71a4bc190833c5947f6fdcd__steps_fvl_cty_y3b"/>

## Procedure

1.  Launch your SAPUI5 application.

2.  In the address field of your browser, add the following to the application URL:

    `sap-theme=<themeID>@<path>&sap-ui-versionedLibCss=true`

    Where:

    -   `<themeID>` is the ID you provided when you created the theme.
    -   `<path>` is the theming service path you used for your mapping.

        For more information, see [Applying Custom Themes to SAPUI5 Apps](applying-custom-themes-to-sapui5-apps-eeb654b.md).



