<!-- copyfee3c509e8e942d7bd0adee1b574e18b -->

# Running a Custom Theme via a URL Parameter

Administrators can run SAPUI5 applications with a custom theme using a URL parameter.



## Prerequisites

-   You have published your theme to SAP BTP.

-   You have added a route to the theming service. For more information, see [Applying Custom Themes to SAPUI5 Apps](applying-custom-themes-to-sapui5-apps-93d5eb0.md)


To run SAPUI5 applications with a custom theme, you can use the URL parameter `sap-theme` to set or override the initial theme.



## Procedure

1.  Launch your SAPUI5 application.

2.  In the address field of your browser, add the following to the application URL:

    `sap-theme=<themeID>@<path>&sap-ui-versionedLibCss=true`

    Where:

    -   `<themeID>` is the ID you provided when you created the theme.
    -   `<path>` is the application path you used for your mapping.

        For more information, see [Applying Custom Themes to SAPUI5 Apps](applying-custom-themes-to-sapui5-apps-93d5eb0.md).



