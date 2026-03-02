<!-- loiof69af60df4fc470e8801dab9db6948e8 -->

# Integrating in SAP S/4HANA Cloud Public Edition and SAP BTP, ABAP Environment

To apply a theme to SAP Fiori launchpad running in SAP S/4HANA Cloud Public Edition or SAP BTP ABAP environment, you must integrate the UI theme designer service from SAP BTP, Cloud Foundry environment with communication arrangement `SAP_COM_0623`.



## Prerequisites

You have published a theme or theme set as described in [Publishing Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/publishing-themes-and-theme-sets-f4889a4.md).



### Procedure for Administrators

1.  Create a communication arrangement in SAP S/4HANA Cloud Public Edition to establish a connection to the SAP BTP, Cloud Foundry environment for fetching themes which can then be used in SAP S/4HANA Cloud Public Edition as described in [SAP BTP, Cloud Foundry Environment \(SAP\_COM\_0623\)](https://help.sap.com/docs/SAP_S4HANA_CLOUD/0f69f8fb28ac4bf48d2b57b9637e81fa/78444165263648c39d1584c82af5eddc.html?version=2602.500).
2.  Specify a default theme with parameter `THEMING_DEFAULT_THEME` or allow users to select themes with parameter `USERSETTINGS_SET_THEME` as described in [SAP Fiori Launchpad for SAP S/4HANA Public Cloud Edition: Manage Launchpad Settings](https://help.sap.com/docs/SAP_S4HANA_CLOUD/4fc8d03390c342da8a60f8ee387bca1a/22d573aead754b80abca18ec71872fb7.html?version=2602.500).



### Procedure for Users

1.  In the user menu, select *Settings*.
2.  Select *Appearance*.
3.  Choose a theme or *Automatic*. When you select *Automatic*, the theme adjusts automatically to your system settings as specified in the theme set.

For more information, see [SAP Fiori Launchpad for SAP S/4HANA Public Cloud Edition: Managing your Settings](https://help.sap.com/docs/SAP_S4HANA_CLOUD/4fc8d03390c342da8a60f8ee387bca1a/5bc5a24e86a14feea5f2d223d4abf1a4.html?version=2602.500)

