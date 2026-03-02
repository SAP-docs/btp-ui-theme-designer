<!-- loio8f49dceb09d44ec780c811219f8e0caa -->

# Launching the Theme Designer Web App

To launch the theme designer web app you can either press *Launch Theme Designer* in the *Theme Manager* section of the *User Actions* menu of your SAP Build Work Zone site, or you can add `/comsapuitheming.themedesigner/` to your Application Router \(`AppRouter`\) URL.



## Prerequisites

-   Your administrator has set up UI theme designer as described in [Initial Setup of UI Theme Designer](../Initial-Setup-of-UI-Theme-Designer/initial-setup-of-ui-theme-designer-d9eb188.md).
-   You have at least the `Viewer (sap-theming)` role as described in [Permissions](../Advanced-Information/permissions-c3fdb69.md).



## Procedure

**To launch the Theme Designer web app from a SAP Build Work Zone site**

1.  Under your avatar in the User Actions menu, select *Theme Manager*.

    > ### Note:  
    > To access the *Theme Manager*, you need to have the `Theme_Admin` role.

2.  Select the *Launch Theme Designer* button located at the bottom-left of the *Theme Manager*.

    For more information on the Theme Manager, see [SAP Build Work Zone, advanced edition: Overview of Theming and Branding](https://help.sap.com/docs/build-work-zone-advanced-edition/sap-build-work-zone-advanced-edition/overview-of-theming-and-branding) and [SAP Build Work Zone, standard edition: Overview of Theming and Branding](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/overview-of-theming-and-branding?version=Cloud).


**To launch the Theme Designer web app from a known `AppRouter` URL**

1.  Append `/comsapuitheming.themedesigner`/ to the URL.

There are several options to find the `AppRouter` URL of your own applications:

-   In the SAP BTP cockpit on subaccount level, select your space and navigate to *Applications*. The URL of your `AppRouter` is mentioned under *Application Routes*.
-   In SAP Business Application Studio, the `AppRouter` URL is logged to the job console at the end of the deployment process. The log entry is

    ```
    Application YOUR_APP-approuter has been created. Application URL is: YOUR_APPROUTER_URL.
    ```


To find the `AppRouter` URL of your SAP Build Work Zone

1.  Open your SAP BTP cockpit on subaccount level.
2.  Navigate to *Services* \> *Instances and Subscriptions*.
3.  The `AppRouter` URL of your SAP Build Work Zone is mentioned under *Subscriptions*.



## Result

The Theme Designer web app opens to the Welcome Page.



## Next Steps

Create new themes and theme sets or work with your existing ones as described in [Managing Themes and Theme Sets on the Welcome Page](managing-themes-and-theme-sets-on-the-welcome-page-e358508.md).

