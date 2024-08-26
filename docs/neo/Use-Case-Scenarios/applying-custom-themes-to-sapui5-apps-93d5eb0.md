<!-- copy93d5eb0b468947bb91e23504a95a6307 -->

# Applying Custom Themes to SAPUI5 Apps

Administrators can apply custom themes to SAPUI5 standalone applications.

You can apply a custom theme to any SAPUI5 application using a URL parameter or by hardcoding the initial theme in the SAPUI5 application. To do this, you must have deployed your custom theme to your SAP BTP subaccount.

For more information, see [Deploying Your Custom Themes to SAP BTP](deploying-your-custom-themes-to-sap-btp-e07be57.md).

Once this is in place, use the application descriptor file `neo-app.json` to configure the behavior of your SAPUI5 application by mapping a path to the theming service to access your themes.

Let's get started.



<a name="copy93d5eb0b468947bb91e23504a95a6307__section_w2l_frx_wdb"/>

## First map a path to the theming service storing your theme data

1.  Open the application to which your custom theme should be applied in an IDE \(for example, SAP Web IDE\).

2.  Open the `neo-app.json.` file.

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
    >            "path": "/themes", 
    >            "target": {
    >                "type": "service",
    >                "name": "theming"
    >                "entryPath":"/themes"
    >                      },
    >            "description": "Theming Service"
    >              }
    >           ]
    > ...
    > 
    > ```




<a name="copy93d5eb0b468947bb91e23504a95a6307__section_tdb_2tx_wdb"/>

## Then run your SAPUI5 application in one of the following ways:

