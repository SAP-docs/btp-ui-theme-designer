<!-- loio5eeab0ecad6a457b8f7e1bc6f9027cbe -->

# Auditing and Logging Information

As an administrator, you can find a list of the security events that the UI theme designer logs to your *Audit Log*.



To view the audit logs use the *Audit Log Viewer*. For more information, see [SAP Audit Log Viewer service for the Cloud Foundry Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/audit-log-viewer-for-cloud-foundry-environment?&version=Cloud).

**Security events written in audit logs**


<table>
<tr>
<th valign="top">

Event grouping

</th>
<th valign="top">

What events are logged

</th>
<th valign="top">

How to identify related log events

</th>
<th valign="top">

Additional information

</th>
</tr>
<tr>
<td valign="top" align="center" rowspan="3">

General

</td>
<td valign="top">

Theme activation

</td>
<td valign="top">

**ThemeDesigner**: theme version activated

</td>
<td valign="top">

This event is logged when a theme is successfully published and activated for end users.

</td>
</tr>
<tr>
<td valign="top">

Theme change

</td>
<td valign="top">

**ThemeDesigner**: change theme

</td>
<td valign="top">

This event is logged every time users save changes to a theme. It occurs even if the theme isn't currently published.

</td>
</tr>
<tr>
<td valign="top">

Theme deleted

</td>
<td valign="top">

**ThemeDesigner**: delete theme

</td>
<td valign="top">

This event is logged when a theme is permanently deleted

</td>
</tr>
</table>



The corresponding theme ID is always included in the event.

**Related Information**  


[Audit Logging in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/f92c86ab11f6474ea5579d839051c334.html)

[Data Protection and Privacy](https://help.sap.com/docs/btp/sap-business-technology-platform/data-protection-and-privacy?version=Cloud)

