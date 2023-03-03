<!-- loio74e5b688cf404c63a376814bf1c6a583 -->

# Running a Custom Theme via a SAPUI5 Bootstrap Configuration

Administrators can run a custom theme via a SAPUI5 bootstrap configuration.



<a name="loio74e5b688cf404c63a376814bf1c6a583__section_ujq_qnm_l2b"/>

## Prerequisite

You have saved and built your custom theme.



<a name="loio74e5b688cf404c63a376814bf1c6a583__section_dym_tnm_l2b"/>

## Procedure

You can hardcode your custom theme as an initial theme in the HTML script tag of an SAPUI5 application as follows:

1.  Open the code for the target SAPUI5 application to which you want to assign your theme.

2.  Insert the following parameters in the SAPUI5 bootstrap script tag:

    -   `data-sap-ui-theme`:

        The theme ID you used to create the theme.

    -   `data-sap-ui-theme-roots`:

        Enter the following: `{"<themeID>" : "/sap/public/bc/themes/~client-<client>” }`

        Where:

        -   `<themeID>` is the technical ID of a published theme in the same SAP BTP subaccount. The ID is visible on the start screen of the UI theme designer.

        -   `<client>` is the SAP client where the theme is saved.




For more information, see SAP Note [2043817](https://launchpad.support.sap.com/#/notes/2043817)

> ### Sample Code:  
> ```
> <script id="sap-ui-bootstrap"                                              
>           src="resources/sap-ui-core.js"                                              
>           …
> 
>           data-sap-ui-versionedLibCss="true"   
>           data-sap-ui-theme="custom_belize"                                
>           data-sap-ui-theme-roots='{"custom_belize" : "/sap/public/bc/themes/~client-020'> 
>          </script> 
> 
> ```

