<!-- copy74e11e41a8cf4f10946b7bb35b258ed3 -->

# Getting Support

Find out how you can get support from SAP for the UI theme designer.



<a name="copy74e11e41a8cf4f10946b7bb35b258ed3__section_cym_5rl_ndb"/>

## SAP Support

If you encounter an issue with the UI theme designer that cannot be resolved using the recommended troubleshooting steps, you can report an incident through the [SAP Support Portal](https://support.sap.com/en/index.html).

When reporting an incident, selecting the appropriate component ensures your request reaches the correct support team. Refer to the table below to determine which component best matches the nature of your problem:


<table>
<tr>
<th valign="top">

Component Name

</th>
<th valign="top">

Description

</th>
<th valign="top">

When to Use

</th>
</tr>
<tr>
<td valign="top">

`CA-UI2-THD-CF`

</td>
<td valign="top">

UI theme designer on SAP BTP, Cloud Foundry

</td>
<td valign="top">

-   Issues within the UI theme designer web application
-   Unable to open UI theme designer
-   Custom themes not applied anymore at all
-   Problems when transporting themes
-   Issues in developer scenarios, such as binding the theming service



</td>
</tr>
<tr>
<td valign="top">

`CA-UI2-THD-S4HC`

</td>
<td valign="top">

UI theme designer on SAP S/4HANA Cloud Public Edition

</td>
<td valign="top">

-   Problems with communication arrangement for integrating UI theme designer from SAP BTP into SAP S/4HANA Cloud Public Edition



</td>
</tr>
<tr>
<td valign="top">

`EP-WZ-PER`

</td>
<td valign="top">

Personalization, theme manager

</td>
<td valign="top">

-   Issues with managing themes in the SAP Build Work Zone theme manager
-   Problems assigning themes in the appearance dialog



</td>
</tr>
<tr>
<td valign="top">

`CA-FLP-FE-COR`

</td>
<td valign="top">

SAP Fiori launchpad frontend core and services

</td>
<td valign="top">

-   Components in SAP Build Work Zone sites do not display correctly with a custom theme applied
-   Problems with SAP themes



</td>
</tr>
<tr>
<td valign="top">

`CA-UI5-CTR`

</td>
<td valign="top">

SAPUI5 controls

</td>
<td valign="top">

-   Visual issues with SAPUI5 controls when using a custom theme
-   Problems with SAPUI5 applications using SAP standard themes



</td>
</tr>
<tr>
<td valign="top">

`CA-UI5-COR`

</td>
<td valign="top">

SAPUI5 core

</td>
<td valign="top">

-   Errors in SAPUI5 theming API
-   Custom theme not applied to some parts of a SAPUI5 application



</td>
</tr>
<tr>
<td valign="top">

`BC-WD-UR`

</td>
<td valign="top">

Unified Rendering

</td>
<td valign="top">

-   Web Dynpro ABAP or SAP GUI for HTML applications show issues with custom themes \(for example, components not displaying as expected\)
-   Problems with Web Dynpro ABAP or SAP GUI for HTML applications using SAP standard themes



</td>
</tr>
</table>



## Information to Include in Your Support Ticket

Once you have identified the correct component, gathering the following information will help the support team to understand and resolve your issue efficiently:

-   **Description of the problem:** Clearly explain what is happening, what you expected to happen, and the exact error messages if any.
-   **Steps to reproduce the issue:** Provide a list of actions needed to trigger the problem.
-   **Screenshots and logs:**
    -   Attach relevant screenshots showing errors, selected options, and console logs.

    -   To help us understand the issue better, refer to these screenshots and logs in your problem description.


-   **URLs of affected sites:** Provide direct links to the impacted pages.
-   **UI theme designer version information:** Specify the version\(s\) you are using. You can find the version information by opening the *Help* menu and selecting *About* within the UI theme designer web application.

-   **Custom theme files:** Attach a copy of your custom theme. To do this, export your theme from the UI theme designer using the *Source files only* option, as described in the [Exporting Themes](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/26e5140268f94045b3b031c4027fff4d.html "Administrators use the export function to download themes as zip files from the UI theme designer to a local hard disk.") :arrow_upper_right: section.

-   **HTTP traces:** Capture HTTP traces using Google Chrome or Microsoft Edge \(Chromium\) as described in SAP Note [1990706](https://me.sap.com/notes/1990706). Tips for recording:
    -   Start recording before entering the site URL.
    -   Open a blank browser page first to avoid capturing unrelated activity.
    -   Enter and access the site.
    -   Reproduce the issue.
    -   Stop recording.

-   **Support user credentials:** Provide a support username and password with the necessary permissions to reproduce the issue. For guidance, see SAP Note [3543065](https://me.sap.com/notes/3543065)

