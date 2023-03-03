<!-- loio80642ec6cc3c4b7cb840e17dfec8fd8d -->

# Running a Custom Theme via a SAPUI5 Bootstrap Configuration

Administrators can run a custom theme via a SAPUI5 bootstrap configuration.



<a name="loio80642ec6cc3c4b7cb840e17dfec8fd8d__prereq_hh1_4ty_y3b"/>

## Prerequisites

-   You have published your theme to SAP BTP.

-   You have added a route to the theming service.

    For more information, see .


You can hardcode your custom theme as an initial theme in the HTML script tag of an SAPUI5 application as follows:



<a name="loio80642ec6cc3c4b7cb840e17dfec8fd8d__steps_ih1_4ty_y3b"/>

## Procedure

1.  Open the code for the target SAPUI5 application to which you want to assign your theme.

2.  Insert the following parameters in the SAPUI5 bootstrap script tag:

    -   `data-sap-ui-versionedLibCss="true"`
    -   `data-sap-ui-theme`: this is the theme ID you provided when you created the theme.
    -   `data-sap-ui-theme-roots`: enter the following:

        `{"<theme_id>" : "/<path>/themeroot/v1/UI5"}` or

        `{"<theme_id>" : "/comsapuitheming.runtime/themeroot/v1/UI5"}` if optional setting in `xs-app.json` isn't used

        Where:

        -   `<theme_id>` is the ID you provided when creating the theme.

        -   `<path>` is the theming service path you used for your mapping in the application router file of the theming service. For more information, see .


    -   `data-sap-ui-resourceroots` enter the following

        `data-sap-ui-resourceroots='{"<appName>": "/"}`

        where `<appName>` is your business application used for binding a UI theme designer instance to the app router module.


    > ### Sample Code:  
    > ```
    > <script id="sap-ui-bootstrap"                                              
    >           src="/resources/sap-ui-core.js"                                              
    >           data-sap-ui-versionedLibCss="true"                                              
    >           data-sap-ui-theme="custom1belize"                                                                                                                                          
    >           data-sap-ui-theme-roots='{"custom1belize" : "/themes/themeroot/v1/UI5/"}'
    >           data-sap-ui-resourceroots='{"<appName>": "/"}'>
    >          </script> 
    > ```


