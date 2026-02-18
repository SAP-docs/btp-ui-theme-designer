<!-- loio377f9056a6084be18493a98bffa9edf0 -->

# What's New for UI Theme Designer





**2026**


<table>
<tr>
<th valign="top">

Technical Component

</th>
<th valign="top">

Environment

</th>
<th valign="top">

Title

</th>
<th valign="top">

Description

</th>
<th valign="top">

Action

</th>
<th valign="top">

Lifecycle

</th>
<th valign="top">

Type

</th>
<th valign="top">

Line of Business

</th>
<th valign="top">

Modular Business Process

</th>
<th valign="top">

Product

</th>
<th valign="top">

Latest Revision

</th>
<th valign="top">

Available as of

</th>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

**Prohibit Palette Parameters Starting with Underscores** 

</td>
<td valign="top">

Palette parameters that begin with an underscore can conflict with SAP internal UI technology parameters. As a result, the UI theme designer now prevents the creation of new palette parameters starting with an underscore. Existing parameters are unaffected, but it is recommended to replace any palette parameters that start with an underscore.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-17

</td>
<td valign="top">

2026-02-17

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry
-   Neo



</td>
<td valign="top">

**Theming Base Content Version** 

</td>
<td valign="top">

The base theming content is updated to version 11.34.0. Review the changes at [https://github.com/SAP/theming-base-content/releases](https://github.com/SAP/theming-base-content/releases).

-   **SAP-icons font replaced by SVGs**

    The SAP-icons font has been supplemented with SVG icons. All icons previously available in the SAP-icons font are now also provided as [SVGs](https://github.com/SAP/theming-base-content/tree/master/content/Base/icons). While the SAP-icons font remains available, new icons will be added only as SVGs. Developers using the SAP-icons font are encouraged to switch to SVG icons going forward.




</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-17

</td>
<td valign="top">

2026-02-17

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry
-   Neo



</td>
<td valign="top">

**New SAP Icons for Business Suite** 

</td>
<td valign="top">

The SAP-icons library for Business Suite has been updated to versions v2.091/v1.091, introducing a new icon \(`e13d` – "Zoom to Fit"\).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry
-   Neo



</td>
<td valign="top">

**Deprecation of Parameters** 

</td>
<td valign="top">

-   `sapHighlightTextColor`.
-   `sapButton_Emphasized_FontWeight` - please use `font-family: var(---sapButton_Emphasized_FontFamily); font-weight: normal;` instead.



</td>
<td valign="top">

Info only

</td>
<td valign="top">

Deprecated

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry
-   Neo



</td>
<td valign="top">

**Enhanced Description for Tile Parameters** 

</td>
<td valign="top">

The descriptions of tile control parameters have been updated to better explain their usage and visual effects, helping users to configure them more accurately.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

**Use of SAP Standard Icons** 

</td>
<td valign="top">

The theme designer web app now uses SAP’s standard icons for the "Add Preview Pages" button and the expert theming toolbar, ensuring consistency with SAP’s iconography.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

**Enhanced Typography Filter** 

</td>
<td valign="top">

The typography type filter now exclusively displays font families, excluding font colors. This improvement simplifies the process of locating font family parameters within expert theming.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

**Select Testsuite Header** 

</td>
<td valign="top">

Clicking the test suite header within the preview pages pane to open the preview pages configuration was previously broken. This issue has been fixed, and the list of pages now displays correctly.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry
-   Neo



</td>
<td valign="top">

**Theming Base Content Version** 

</td>
<td valign="top">

The base theming content is updated to version 11.33.0. Review the changes at [https://github.com/SAP/theming-base-content/releases](https://github.com/SAP/theming-base-content/releases).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

**Tooltip for Parameters** 

</td>
<td valign="top">

A tooltip for parameter IDs is now available in the expert pane, allowing users to easily identify parameters even when the IDs are truncated due to limited space in the parameter column.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
<tr>
<td valign="top">

UI Theme Designer

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

**SAPUI5 Preview Version Mismatch Warning** 

</td>
<td valign="top">

When opening a SAPUI5 preview page that uses a different minor version than the theme repository, a warning dialog now appears to inform users of the version mismatch. The dialog has been styled as a warning instead of an error to prevent confusion and to avoid the impression that the theme designer web app is broken or unusable. Users can continue theming, but rendering issues in the preview may occur due to the version discrepancy.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

</td>
<td valign="top">

Technology

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

 

</td>
<td valign="top">

2026-02-03

</td>
<td valign="top">

2026-02-03

</td>
</tr>
</table>

