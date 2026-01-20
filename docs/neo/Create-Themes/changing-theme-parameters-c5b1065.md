<!-- copyc5b1065178bd4eec84fa502807461da3 -->

# Changing Theme Parameters

The UI theme designer allows you to make changes at several technical levels.

Depending on the adaptations required to create your theme, you can switch between different editing modes.

****


<table>
<tr>
<th valign="top">

Quick Theming

</th>
<th valign="top">

Detailed Theming

</th>
<th valign="top">

Mobile Theming

</th>
<th valign="top">

Expert Theming

</th>
</tr>
<tr>
<td valign="top">

Allows some sweeping high-level changes that are very robust across UI technologies and versions thereof. Only a selected number of parameters is offered for editing.

</td>
<td valign="top">

Allows changes on a more detailed level. The parameters are grouped by semantics. Here more parameters are offered as for quick theming.

</td>
<td valign="top">

Allows changes only to parameters with an effect on native iOS and Android appilcations built with SAP Mobile Start. For more information, see [Themes for Custom Corporate Branding](https://help.sap.com/docs/SAP_MOBILE_START/386859cc981742f3b6bb31f7e0d8a168/ca3c655f811e415e862298575a003608.html) in the SAP Mobile Start for iOS – Administration Guide. Mobile theming is only available for custom themes based on the Horizon theme family and newer.

</td>
<td valign="top">

Allows a finer grain of changes than quick and detailed theming. A greater number of parameters is offered for editing, which gives you advanced options for adapting themes.

</td>
</tr>
<tr>
<td valign="top">

The parameter set is independent of the application you selected for the preview.

</td>
<td valign="top">

Which parameters are available for editing is dependent on the following:

-   the theme you have selected as the base of your theme
-   the application you have selected for the preview



</td>
<td valign="top">

The parameter set is independent of the application you have selected in the preview, but is instead restricted to parameters with an effect on SAP Mobile Start applications.

</td>
<td valign="top">

Which parameters are available for editing is dependent on the following:

-   the theme you have selected as the base of your theme
-   the application you have selected for the preview



</td>
</tr>
<tr>
<td valign="top">

Changing the value of a quick theming parameter affects many controls at once.

</td>
<td valign="top">

Changing the value of a detailed theming parameter affects a smaller group of controls at once \(e.g. list parameters\).

</td>
<td valign="top">

Changing the value of mobile theming parameters affects many SAP Mobile Start controls at once. However, changes might not be reflected 1:1 from preview to application, as the preview is no native SAP Mobile Start application.

</td>
<td valign="top">

Changing the value affects either a specific control or groups or it can affect many other entries \(for more generic parameters\).

</td>
</tr>
<tr>
<td valign="top">

Quick theming parameters are displayed with a label rather than a technical name \(e.g *Highlight Color*\).

</td>
<td valign="top">

Detailed theming parameters are displayed with a label rather than a technical name and they are grouped semantically.

</td>
<td valign="top">

Mobile theming parameters are displayed with a label rather than a technical name and they are grouped semantically.

</td>
<td valign="top">

All parameters, including the quick theming parameters, are displayed with their technical name \(e.g. *sapHighlightColor*\).

</td>
</tr>
</table>

**Custom LESS and CSS**

In addition to quick and expert theming, SAPUI5 and Unified Rendering support custom LESS or CSS. You can add LESS and CSS rules in the text editor that is available in the *CSS* tab. This allows you to make further adjustments to your theme that are not possible by changing the values of the theming parameters. Custom CSS allows a lot of control, but is difficult to support since the standard CSS evolves with every release.

> ### Note:  
> Upgrade safety is not provided for any changes made in the *CSS* tab.

