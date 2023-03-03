<!-- loio936ce5da329f4036a4945ddd13977a9b -->

# Running a Custom Theme via a URL Parameter

Administrators can run SAPUI5 applications with a custom theme using a URL parameter.



## Prerequisites

You have saved and built your custom theme.



## Context

To run SAPUI5, Web Dynpro ABAP, or SAP GUI for HTML applications with a custom theme, you can use the URL parameter `sap-theme` to set or override the initial theme.



<a name="loio936ce5da329f4036a4945ddd13977a9b__steps_fdx_xvk_1l"/>

## Procedure

1.  Launch your application.

2.  In the address field of your browser, add the following parameters to the application URL:

    `sap-theme=<themeID>@/sap/public/bc/themes/~client-<client>`

    Where:

    -   `<themeID>` is the technical ID of a published theme in the same SAP BTP subaccount. The ID is visible on the start screen of the UI theme designer.

    -   `<client>` is the SAP client where the theme is saved.


    For more information, see SAP Note [2043817](https://launchpad.support.sap.com/#/notes/2043817) 

    > ### Note:  
    > To consume a theme from a different host, use`theme=<themeID>@<protocol>://<hostname>:<port>/sap/public/bc/themes/~client-<client>`
    > 
    > Where: `<protocol>`, `<hostname>`, and `<port>` are http/https, the full qualified host name and the protocol differs from the standard port.
    > 
    > > ### Remember:  
    > > Make sure that the theme’s UI technology version is compatible with the used UI technology version. We recommend that you use the same UI technology versions on the system that contains the theme and the system that hosts the app using the theme.


