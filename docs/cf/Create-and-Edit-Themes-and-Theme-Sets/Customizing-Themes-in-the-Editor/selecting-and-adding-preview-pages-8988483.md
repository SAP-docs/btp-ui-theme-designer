<!-- loio898848329cd344dd8afff5dbc13c2b85 -->

<link rel="stylesheet" type="text/css" href="../../css/sap-icons.css"/>

# Selecting and Adding Preview Pages

When you open the editor for the first time, it shows a default selection of preview pages. You can add more preview pages from a set of predefined options or add your own applications.

To preview your theme changes effectively, select the preview pages that best match your theming scenario. Your selection of the preview pages is stored in your local browser storage, so they are available the next time you open the UI theme designer. To delete your preferences from local storage, open the user menu and choose *Clear Preferences*.



<a name="loio898848329cd344dd8afff5dbc13c2b85__section_pbx_m1d_1qb"/>

## Prerequisite

You are working in the editor as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).



<a name="loio898848329cd344dd8afff5dbc13c2b85__section_spd_2cd_1qb"/>

## Procedure

**To add or remove preview pages from the predefined set:**

1.  Select *Add Preview Pages* <span class="SAP-icons-V5"></span>.
2.  Choose a test suite.
3.  Select the preview pages you want to add or deselect the pages you want to remove.

> ### Note:  
> You can also select the test suite title in the *Preview Pages* pane to open the configuration screen of that test suite.

**To add your own applications:**

1.  Select *Add Preview Pages* <span class="SAP-icons-V5"></span>.
2.  Enter the URL of the application in the *Link to Application* field under the *Add Application* section.
3.  **Optional** Name the application. This name appears in the preview pages list. If you don't provide a name, the UI theme designer tries to generate one based on the page.
4.  Choose *Add*.

> ### Note:  
> -   If your application runs on a different host than the UI theme designer, the application must support the theme post-message sent by the UI theme designer. For instructions on enabling cross-origin preview, follow the tutorial [Add a Cross Origin Preview for the UI Theme Designer](https://help.sap.com/docs/link-disclaimer?site=https%3A%2F%2Fdevelopers.sap.com%2Ftutorials%2Fadd-cross-origin-preview-page.html?locale=en-US&state=DRAFT&version=Cloud%20(dev)).
> -   You can add only links to your own applications and not upload a complete preview page.

**To edit or remove your own applications:**

1.  Hover over the application in the list of preview pages.
2.  Select *Edit* :pencil2: or *Remove* <span class="SAP-icons-V5"></span>.



## Best Practices for Selecting Preview Pages

Preview pages are grouped by UI technologies. SAPUI5 is the reference UI technology for theming, so SAPUI5 preview pages appear by default when you start the UI theme designer for the first time.

Preview pages are designed to cover a variety of theming scenarios. Choose preview pages that best represent your theming needs for the most accurate results:

****


<table>
<tr>
<th valign="top">

**Theming Scenario**

</th>
<th valign="top">

**Recommended Preview Pages**

</th>
</tr>
<tr>
<td valign="top">

Quick theming using main parameters

</td>
<td valign="top">

Quick Theming \(SAPUI5 Applications\), Launchpad \(SAPUI5 Applications\)

</td>
</tr>
<tr>
<td valign="top">

Theming the launchpad

</td>
<td valign="top">

Launchpad \(SAPUI5 Applications\), Shell \(SAPUI5 Controls\)

</td>
</tr>
<tr>
<td valign="top">

Adjusting main theming parameters and continue with some specific control fine-tuning in Detailed Theming

</td>
<td valign="top">

Quick Theming \(SAPUI5 Applications\), Launchpad \(SAPUI5 Applications\), selective control pages in SAPUI5 controls

</td>
</tr>
<tr>
<td valign="top">

Theming specific UI controls, including different states

</td>
<td valign="top">

All control pages in SAPUI5 controls

</td>
</tr>
</table>

> ### Note:  
> You can find relevant parameters for a control preview page in [Expert Theming](expert-theming-7b01607.md) by selecting the tag corresponding to the control name.

