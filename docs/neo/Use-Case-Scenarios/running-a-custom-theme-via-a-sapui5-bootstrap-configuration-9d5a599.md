<!-- copy9d5a5995ab2b47cea39f2e08012a48d3 -->

# Running a Custom Theme via a SAPUI5 Bootstrap Configuration

Administrators can run a custom theme via a SAPUI5 bootstrap configuration.



## Prerequisites

-   You have published your theme to SAP BTP.

-   You have added a route to the theming service.

    For more information, see [Applying Custom Themes to SAPUI5 Apps](applying-custom-themes-to-sapui5-apps-93d5eb0.md).


You can hardcode your custom theme as an initial theme in the HTML script tag of an SAPUI5 application as follows:



## Procedure

1.  Open the code for the target SAPUI5 application to which you want to assign your theme.

2.  Insert the following parameters in the SAPUI5 bootstrap script tag:

    -   `data-sap-ui-versionedLibCss="true"`
    -   `data-sap-ui-theme`: this is the theme ID you provided when you created the theme.
    -   `data-sap-ui-theme-roots`: enter the following:

        `{"<themeId>" : "/<path>/UI5"}`

        Where:

        -   `<themeID>` is the ID you provided when creating the theme.

        -   `<path>` is the application path you used for your mapping in the application descriptor file of the theming service. For more information, see [Applying Custom Themes to SAPUI5 Apps](applying-custom-themes-to-sapui5-apps-93d5eb0.md)



    > ### Sample Code:  
    > ```
    > <script id="sap-ui-bootstrap"                                              
    >           src="resources/sap-ui-core.js"                                              
    >           data-sap-ui-versionedLibCss="true"                                              
    >           data-sap-ui-theme="custom1belize"                                                                                                                                          
    >           data-sap-ui-theme-roots='{"custom1belize" : "/themes/UI5/"}'> 
    >          </script> 
    > ```


