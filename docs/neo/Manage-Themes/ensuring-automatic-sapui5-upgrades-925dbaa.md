<!-- copy925dbaad992441499a5a477aa0b5f57b -->

# Ensuring Automatic SAPUI5 Upgrades

To ensure compatibility, themes must be upgraded when the technology version changes.

The CSS files of a custom theme only work for the SAPUI5 version for which the theme was built when it was exported from the UI theme designer. In SAP BTP, SAPUI5 is automatically upgraded once a new version is available, and this might result in unexpected display of your theme. Therefore, if the version of a UI technology has changed, you will need to rebuild your custom themes to ensure that they work properly.

See SAP Notes [2140280](https://me.sap.com/notes/2140280) and [2119552](https://me.sap.com/notes/2119552).



<a name="copy925dbaad992441499a5a477aa0b5f57b__section_f4d_zym_22b"/>

## Automatic SAPUI5 upgrades

If you run the UI theme designer in SAP Fiori launchpad on SAP BTP or on SAP Fiori, cloud edition, you can use the **theming service** to rebuild the theme automatically whenever the SAPUI5 version changes.

To enable the theming service to upgrade a theme automatically, configure this option in the Theme Manager as follows:

1.  In the SAP Fiori launchpad configuration cockpit, or in the *Admin Space*, under *Services and Tools*, click the *Theme Manager* tile.

2.  Set the *Theme Upgrade* option to ON.

    > ### Note:  
    > When you publish a theme, the Theme Manager sets this option automatically to ON.


