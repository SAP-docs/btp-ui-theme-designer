<!-- loio6111b74766804a2c8d314951e1b04ff9 -->

# Configuring the Launchpad to Use the Custom Theme

To consume the custom theme in the launchpad module, modify the CommonDataModel.json file of your launchpad module.

1.  In [SAP Business Application Studio](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US), open the CommonDataModel.json file, located under the launchpad module of your application.

2.  In the sites section of the CommonDataModel.json, add your custom theme as follows:

    ```
    // this property defines the default theme for the site
    "theme.id":"sap_belize",
    
    // this property defines the list of available themes for the site
    "theme.active":["sap_belize","sap_belize_plus","sap_belize_hcb","sap_belize_hcw"],
    ```


**Related Information**  


[Creating Custom Themes on SAP BTP Portal](https://help.sap.com/viewer/ad4b9f0b14b0458cad9bd27bf435637d/Cloud/en-US/3e0b9016fc6e45d2be259d3244c4af10.html)

