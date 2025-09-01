<!-- loio8b0bf5c76c8b4f53b0240b85ecf76353 -->

# Guided Answers



## UI Theme Designer

When working with [UI Theme Designer](https://help.sap.com/viewer/8ec2dae34eb44cbbb560be3f9f1592fe/7.40.19/en-US/a118094264684230bb6510045b5b5b7c.html) you are running into problems in design time or in run time.



**Run Time** - The issue is seen in the application when it runs with the theme applied

**Design time** - The issue happens when trying use UI theme designer, i.e. creating,building, saving themes or transporting themes

-   Runtime
-   Design time



## RunTime Issues with Custom Theme on SAP BTP

-   For UI Theme Designer on SAP BTP, it is important that the SAPUI5 version that the site uses and the SAPUI5 version in which the theme was created, is the same.

    Therefore, to customize a theme, the UI Theme Designer must always be opened from Fiori Configuration Cockpit \(FCC\) as follows:

    -   Go to SAP BTP Cockpit \> "Services" \> select service "Portal" \> click on "Go to Service" \(if service is not enabled, [see guide](https://gad5158842f.us2.hana.ondemand.com/dtp/viewer/#/tree/2065/actions/27097?version=current)\)
    -   In the new tab that opens, click on "Site Directory" \> Click on the "Edit" link for the site to be themed to open FCC \(at least one Site has to be available in order to edit it\)
    -   In FCC, go to "Services and Tools" \> "UI Theme Designer"


-   In SAP BTP, SAPUI5 is upgraded automatically. UI5 versions for apps are backward compatible so you need to ensure that the runtime environment which is the site and theme UI5 versions are compatible. See SAP Help [Maintaining Compatibility Between the Site Theme and the SAPUI5 Version](https://help.hana.ondemand.com/cloud_portal/frameset.htm?8b4b801695564ad4b9601a2878162636.html) and also KBA [2333779](https://launchpad.support.sap.com/#/notes/2333779) - 'Theme rendering issue SAP Cloud Portal service'.

-   Note that once a theme is assigned to a site, it is compiled by the theme service so that it is available at runtime. The compilation starts only when the first access to the site happens. Therefore, the user with the first access to the site, after a new theme is assigned, will see the changes to the theme after a delay.

-   Custom themes are deployed to the cloud platform account as HTML5 applications. Therefore, every custom theme must be available as a Helium app in the Cockpit -\> Applications -\> HTML5 Applications.

-   If the above does not help then raise an incident in CA-UI2-THD component with the following information:
    -   Description of issue, if possible with screenshots.
    -   [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs




## Design Time

-   Startup or Loading of UI Theme Designer
-   Create / Build / Rebuild / Save theme
-   Other



## Issues with Previews, Editor Tools, Transport

-   ABAP
-   Enterprise Portal
-   Issues common to all 3 platforms



## UI Theme Designer Issues on ABAP

Check if the following KBAs are applicable:

-   [2561929](https://launchpad.support.sap.com/#/notes/2561929) - UI Theming Tool for ABAP: Display info of custom theme only one time
-   [2512380](https://launchpad.support.sap.com/#/notes/2512380) - How to Transport Custom Themes in UI Theme Designer on ABAP
-   [2519986](https://launchpad.support.sap.com/#/notes/2519986) - Quick Theming parameters blank in UI theme Designer

-   If the KBAs do not help then raise an incident in CA-UI2-THD component with the following information:

    1. Description of issue, if possible with screenshots.

    2. [HTTPwatch](https://launchpad.support.sap.com/#/notes/0001558903) / Fiddler traces / Screenshots of Google Chrome console logs

    3. UI Theme designer [version information](https://launchpad.support.sap.com/#/notes/0002405598)




## UI Theme Designer on Enterprise Portal Issues

Check if the following KBAs are applicable:

-   [2526513](https://launchpad.support.sap.com/#/notes/2526513) - SAP Standard themes are missing under the UI Theme Designer
-   [2542921](https://launchpad.support.sap.com/#/notes/2542921) - Certain SAP themes are missing under the UI Theme Designer
-   [2519986](https://launchpad.support.sap.com/#/notes/2519986) - Quick Theming parameters blank in UI theme Designer
-   [2418927](https://launchpad.support.sap.com/#/notes/2418927) - 'Custom CSS is not supported for selected technology' error in UI Theme Designer
-   [2393092](https://launchpad.support.sap.com/#/notes/2393092) - How to import LESS mode custom theme\(.epa\) to another LESS mode portal
-   [2393091](https://launchpad.support.sap.com/#/notes/2393091) - How to export a custom theme in LESS mode \[VIDEO\]

-   If the KBAs do not help then raise an incident in CA-UI2-THD component with the following information:

    1. Description of issue, if possible with screenshots

    2. [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs

    3. Portal [version information](https://launchpad.support.sap.com/#/notes/0001757810)




## Common issues in UI Theme Designer on ABAP, Enterprise Portal and SAP BTP

-   [2495619](https://launchpad.support.sap.com/#/notes/2495619) - Preview error on UI Theme Designer when creating new theme

-   [2522531](https://launchpad.support.sap.com/#/notes/2522531) - How to find theme parameters for an element in UI Theme Designer

-   [2410359](https://launchpad.support.sap.com/#/notes/2410359) - Error when importing theme into UI Theme Designer

-   [2466020](https://launchpad.support.sap.com/#/notes/2466020) - Domain warning in UI theme designer

-   [2409539](https://launchpad.support.sap.com/#/notes/2409539) - How to identify source platform for a UI Theme Designer theme zip file

-   [2593846](https://launchpad.support.sap.com/#/notes/2593846) - SAP Belize Deep theme not available in UI Theme Designer

-   If the KBAs do not help then raise an incident in CA-UI2-THD component with the following information:

    1.  Description of issue, if possible with screenshots.
    2.  2. What platform is the UI theme designer being run on ?

        -   Portal
        -   NW ABAP
        -   SAP BTP

    3.  Version information \(on premise\)

        [ABAP](https://launchpad.support.sap.com/#/notes/2405598) / [Portal](https://launchpad.support.sap.com/#/notes/1757810)

    4.  4. HTTPwatch trace as per KBA [1558903](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs





## Build, Rebuild, Save and Publish Problems

-   ABAP
-   Enterprise Portal
-   SAP BTP



## Theme compiling issues in UI Theme Designer on ABAP

-   Check if the following KBAs are applicable

    [2421307](https://launchpad.support.sap.com/#/notes/2421307) - Uncaught Loading Theme "CRMWebUI.baseLib.baseTheme" failed

    [2534432](https://launchpad.support.sap.com/#/notes/2534432) - UI theme designer: Uncaught Loading Theme "sap\_corbu" failed. No configuration found.


-   It is always recommended to use UI Theme Designer with the latest patch and latest version of theming content. So, if the issue still persists after rebuilding the theme then check if the "Unified Rendering" and "Base" theming content has been updated to the latest available versions.

    Follow note [1852401](https://launchpad.support.sap.com/#/notes/1852401) to apply latest patch for UI Theme Designer.

    Refer to note [2408180](https://launchpad.support.sap.com/#/notes/2408180) to update "Unified Rendering" and "Base" theming content


-   If the above does not help then raise an incident in CA-UI2-THD component with the following information:

1.  Steps followed to recreate the issue
2.  [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) or Fiddler trace recorded while recreating the issue
3.  UI Theme designer [version information](https://launchpad.support.sap.com/#/notes/0002405598)



## Theme Compilation Issues on Enterprise Portal

-   Check KBA [2395401](https://launchpad.support.sap.com/#/notes/2395401) - Uncaught Calling repository method Notify error when Rebuilding theme using the UI Theme Designer \[Central Note\]

-   It is recommended to have the latest version of theming engine version and theming content. So, if the issue still persists after rebuilding the theme then check if the theming engine and theming content have been updated to the latest available versions.

    Unified Rendering content is delivered in **Portal Basis** \(**EP-BASIS**\) component.

    From 7.50 SP02 Unified Rendering content is delivered in **Fiori launchpad** \(**EP-FLP**\) component.

    Theming Engine is delivered in software component **Portal Basis** \(**EP-BASIS**\) for following versions

    -   7.30 SP10 - SP12
    -   7.31 SP09 - SP14
    -   7.40 SP04 - SP09
    -   For higher versions, Theming Engine is delivered in **SAPUI5 Client RT AS JAVA**\(**UISAPUI5\_JAVA**\).

    In addition to above patch, also apply patches for all the dependent software components following SAP Note [1974464](https://launchpad.support.sap.com/#/notes/1974464).


-   If the above steps do not help then create an incident in the CA-UI2-THD component with the following information:

    1. Description of issue, if possible with screenshots.

    2. [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs

    3. Portal [version information](https://launchpad.support.sap.com/#/notes/0001757810)




## Theme compiling issues in UI Theme Designer on SAP BTP

-   Check if the following KBA is applicable

    [2631112](https://launchpad.support.sap.com/#/notes/2631112) - E-mail address needs to be supplied by the Identity Provider \(custom IdP\)


-   If the above does not help then raise an incident in CA-UI2-THD component with the following information:

1.  Steps followed to recreate the issue
2.  [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) or Fiddler trace recorded while recreating the issue
3.  UI Theme designer version



## Startup or Loading issues

-   ABAP
-   Enterprise Portal
-   SAP BTP



## Startup / Loading Issues on SAP BTP

Currently the following cases are known:

-   [2466055](https://launchpad.support.sap.com/#/notes/2466055) - 503 No application is available to handle this request for UI Theme Designer in SAp BTP
-   [2502305](https://launchpad.support.sap.com/#/notes/2502305) - 403 Service Forbidden for UI Theme Designer on SAP BTP

If the KBAs does not help then raise an incident in CA-UI2-THD component with the following information:

1.  Description of issue, if possible with screenshots.
2.  [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs





## Startup / Loading issues on Enterprise Portal

Currently the following cases are known:

-   [2463881](https://launchpad.support.sap.com/#/notes/2463881) - UI Theme Designer Blank due to Clickjacking protection disabled
-   [2457630](https://launchpad.support.sap.com/#/notes/2457630) - Theme repository could not be read error in UI Theme Designer on portal

-   If the KBAs do not help then raise an incident in CA-UI2-THD component with the following information:

    1. Description of issue, if possible with screenshots.

    2. [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs

    3. Portal [version information](https://launchpad.support.sap.com/#/notes/0001757810)




## Startup / Loading Issues on ABAP

-   Check if this KBA is applicable: [2564602](https://launchpad.support.sap.com/#/notes/2564602) - UI Theme Designer url opens blank page



-   If the KBA does not help then raise an incident in CA-UI2-THD component with the following information:

1.  Description of issue, if possible with screenshots
2.  [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) or Fiddler trace recorded while recreating the issue
3.  UI Theme designer [version information](https://launchpad.support.sap.com/#/notes/0002405598)



## Custom Theme Check

Themes that have name starting with sap\_ are SAP provided standard themes. For e.g. sap\_belize.

Other themes are custom themes.

Outcomes:

-   Yes
-   No, it happens when using a default SAP provided theme



## Standard Theme Used by Application

Check on SCN WIKI [Platform and Theme Support Overview](https://wiki.scn.sap.com/wiki/x/ZQptH) if the theme is supported for the UI technology \(SAPUI5, Web Dynpro ABAP, Portal etc. \).



If the SAP provided theme is supported for the UI technology then there is an issue with the application or the UI technology and not with the UI Theme Designer.



## Building Custom Theme

Custom themes can be rebuilt using the **Save**and **Build** or **Rebuild** option in the UI Theme Designer.

Outcomes:

-   Yes, but issue persists
-   No



## Design Time Issue

Rebuild the theme by following the steps in KBA:

[2505163](https://launchpad.support.sap.com/#/notes/2505163) - How to Rebuild custom themes in UI Theme Designer

-   Yes
-   No



## Theme Has Been Succcessfully Rebuilt

-   ABAP
-   Enterprise Portal
-   SAP BTP



## Update Theming Content for UI Theme Designer on ABAP

-   Check if the following KBAs are applicable:

    [2513085](https://launchpad.support.sap.com/#/notes/2513085) - Fiori Launchpad fails to load with custom theme specified as URL-parameter

    [2501766](https://launchpad.support.sap.com/#/notes/2501766) - External theme from a different domain does not work with UI5 app

    [2517461](https://launchpad.support.sap.com/#/notes/2517461) - SAP logo displays instead of custom Company Logo in Fiori Launchpad




-   It is always recommended to use UI Theme Designer with the latest patch and latest version of theming content. So, if the issue still persists after rebuilding the theme and the above KBAs are not applicable then ensure that the "Unified Rendering" and "Base" theming content has been updated to the latest available versions.

    Follow note [1852401](https://launchpad.support.sap.com/#/notes/1852401) to apply latest patch for UI Theme Designer

    Refer to note [2408180](https://launchpad.support.sap.com/#/notes/2408180) to update "Unified Rendering" and "Base" theming content


-   If the above steps do not solve the issue then raise an incident in CA-UI2-THD component with the following information:

    1. Description of issue, if possible with screenshots

    2. [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs

    3. UI Theme designer [version information](https://launchpad.support.sap.com/#/notes/2405598)




## Update Theming Content on Enterprise Portal

-   Check if the following KBAs are applicable:

    [2476897](https://launchpad.support.sap.com/#/notes/2476897) - Custom Portal theme is not set after system restart

    [2493344](https://launchpad.support.sap.com/#/notes/2493344) - Portal Fallback theme is not working as expected with WebDynpro or WebGUI applications

    [2499476](https://launchpad.support.sap.com/#/notes/2499476) - FLP@EP Portal Runtime Error Child not found: at portal\_content/themes

    [2368405](https://launchpad.support.sap.com/#/notes/2368405) - Custom theme masthead displaying incorrectly after activating LESS mode

    [2521292](https://launchpad.support.sap.com/#/notes/2521292) - Custom theme displays without css for RTL language

    [2430019](https://launchpad.support.sap.com/#/notes/2430019) - Incomplete dropdown contents or incorrect position of dropdown in IE11


-   It is recommended to have the latest version of theming engine version and theming content.

    If the issue still persists after rebuilding the theme then check if the theming engine and theming content have been updated to the latest available versions.

    Unified Rendering content is delivered in software component **Portal Basis** \(**EP-BASIS**\)

    From 7.50 SP02 Unified Rendering content is delivered in software component **Fiori launchpad** \(**EP-FLP**\).

    Theming Engine is delivered in software component **Portal Basis** \(**EP-BASIS**\) for following versions

    -   7.30 SP10 - SP12
    -   7.31 SP09 - SP14
    -   7.40 SP04 - SP09
    -   For higher versions, Theming Engine is delivered in **SAPUI5 Client RT AS JAVA**\(**UISAPUI5\_JAVA**\).


In addition to above patch, also apply patches for all the dependent software components following SAP Note [1974464](https://launchpad.support.sap.com/#/notes/1974464).



-   If the above points do not help then raise an incident in CA-UI2-THD component with the following information:

    1. Description of issue, if possible with screenshots.

    2. [HTTPwatch](https://launchpad.support.sap.com/#/notes/1558903) / Fiddler traces / Screenshots of Google Chrome console logs

    3. Portal [version information](https://launchpad.support.sap.com/#/notes/0001757810)


