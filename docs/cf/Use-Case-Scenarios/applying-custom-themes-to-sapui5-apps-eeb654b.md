<!-- loioeeb654b57d074e828fd7ab91f543e472 -->

# Applying Custom Themes to SAPUI5 Apps

Administrators can apply custom themes to SAPUI5 standalone applications.

You can apply a custom theme to any SAPUI5 application using a URL parameter or by hardcoding the initial theme in the SAPUI5 application. To do this, you must have deployed your custom theme to your SAP BTP subaccount.

For more information, see [Initial Setup of UI Theme Designer](../Initial-Setup-of-UI-Theme-Designer/initial-setup-of-ui-theme-designer-d9eb188.md).

Optionally, you can use the application router config file `xs-app.json` to configure the behavior of your SAPUI5 application by mapping a path to the theming service to access your themes.

Let's get started.



<a name="loioeeb654b57d074e828fd7ab91f543e472__section_w2l_frx_wdb"/>

## First map a path to the theming service storing your theme data

1.  Open the application to which your custom theme should be applied in an IDE \(for example, SAP Web IDE\).

2.  Open the `xs-app.json` file.

3.  Enter the following parameters:


    <table>
    <tr>
    <td valign="top">
    
    `path` parameter
    
    </td>
    <td valign="top">
    
    Enter an application path to be mapped.

    This path can then be referenced in a URL parameter or in the SAPUI5 bootstrap configuration. See below.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `name` parameter
    
    </td>
    <td valign="top">
    
    Enter the name of the application storing your theme data.
    
    </td>
    </tr>
    </table>
    
    > ### Example:  
    > This configuration example maps all paths starting with `/themes` to the the theming service that provides access to your custom themes.
    > 
    > ```
    > 
    > ...
    > "routes": [
    >              {
    >                "source": "^/themes/(.*)$", 
    >                "target": "$1",
    >                "service": "com.sap.ui.theming",
    >                "endpoint": "runtime"
    >              }
    >           ]
    > ...
    > 
    > ```




<a name="loioeeb654b57d074e828fd7ab91f543e472__section_tdb_2tx_wdb"/>

## Then run your SAPUI5 application in one of the following ways:

-   Via a URL Parameter

    For more information, see [Running a Custom Theme via a URL Parameter](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/25896d06a71a4bc190833c5947f6fdcd.html?q=Running%20a%20Custom%20Theme%20via%20a%20URL%20Parameter).

-   Via the SAPUI5 Bootstrap Configuration

-   For more information, see [Running a Custom Theme via a SAPUI5 Bootstrap Configuration](running-a-custom-theme-via-a-sapui5-bootstrap-configuration-80642ec.md).


