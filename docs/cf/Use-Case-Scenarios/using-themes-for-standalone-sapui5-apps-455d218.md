<!-- loio455d21820d6946a4b58c8e55e0e6c194 -->

# Using Themes for Standalone SAPUI5 Apps

Administrators can assign themes to standalone SAPUI5 applications \(without SAP Fiori launchpad\).

Use themes for any standalone SAPUI5 app that you've deployed to your SAP BTP subaccount. A standalone app is any SAPUI5 application that you’ve deployed to your SAP BTP account without using SAP Fiori launchpad from the Portal service.

To use your themes for standalone SAPUI5 applications, you need to configure the individual applications.



<a name="loio455d21820d6946a4b58c8e55e0e6c194__section_gyv_y1v_c2b"/>

## The overall process is as follows:

1.  Launch the *UI Theme Designer* from the SAP BTP cockpit.

2.  Switch to the required SAPUI5 version.

    > ### Note:  
    > When you open the UI theme designer directly from SAP BTP, the UI theme designer starts using the latest available SAPUI5.
    > 
    > If your application is using a different version, you should switch the version to your application’s version.

3.  Create a theme in the UI theme designer.

    For more information, see [Creating a New Theme](../creating-a-new-theme-72c730b.md).

4.  Deploy your custom theme to you SAP BTP subaccount.

5.  Apply your custom theme to any SAPUI5 application in your subaccount by using a URL parameter or by hardcoding the initial theme in the SAPUI5 application.

    For more information, see [Applying Custom Themes to SAPUI5 Apps](applying-custom-themes-to-sapui5-apps-eeb654b.md).


