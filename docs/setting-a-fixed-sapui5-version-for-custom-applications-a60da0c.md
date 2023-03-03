<!-- copya60da0cd42124e54accfe2d77b168e5e -->

# Setting a Fixed SAPUI5 Version for Custom Applications

To prevent applications from breaking by the automated SAPUI5 upgrade within SAP BTP, you configure a specific SAPUI5 version in the application descriptor file of your SAPUI5 application and then upgrade whenever you want.



## Context

The CSS \(Cascading Style Sheet\) files of a given custom theme only work for the SAPUI5 version for which the theme was built when it was exported from the UI theme designer.

In SAP BTP, SAPUI5 is automatically upgraded once a new version is available. This could result in unexpected changes to your theme, which you can fix by rebuilding the theme.



<a name="copya60da0cd42124e54accfe2d77b168e5e__steps_mcy_sph_ws"/>

## Procedure

1.  Once you have exported your theme, choose *Help* \> *Info*.

2.  In the dialog box, copy the version number from the *SAPUI5 Dist.Layer* field \(for example, 1.28.10\).

3.  Open the app to which you want to apply your custom theme in a development environment such as SAP Web IDE.

4.  Open the `neo-app.json` file.

5.  Add the SAPUI5 Distribution version number you copied in step 2 as the value of the `version` parameter.

    > ### Example:  
    > This configuration example shows how to reference the SAPUI5 version 1.28.10 using the neo-app.json file.
    > 
    > ```
    > 
    > ... 
    > "routes": [
    >          {
    >             "path": "/resources",
    >             "target": {
    >                 "type": "service",
    >                 "name": "sapui5",
    >                 "version": "1.28.10", 
    >                 "entryPath": "/resources"                    
    >              },
    >             "description": "SAPUI5"            
    >           }
    > ] 
    > ... 
    > 
    > ```


