<!-- copy2eac04bee3bf4805a2a4c5a25b82c6e8 -->

# Custom Themes: Important Things to Know

Consider the following important information before you start working with UI theme designer.




<table>
<tr>
<td valign="top">

What kinds of changes can I make in a custom theme?

</td>
<td valign="top">

The UI theme designer allows you to make changes at several technical levels.

</td>
</tr>
<tr>
<td valign="top">

Which platforms and UI technologies are supported in a custom theme?

Which SAP standard themes can I use as the base of a custom theme?

</td>
<td valign="top">

See SAP Note [1852400](https://me.sap.com/notes/1852400).

</td>
</tr>
<tr>
<td valign="top">

How compatible is a custom theme?

</td>
<td valign="top">

Themes are designed to work with a variety of browsers, but a custom theme only works properly for the version and patch of the UI technology it was built for. If the UI technology has changed, for example via an upgrade, any custom theme will need to be rebuilt to ensure it works properly.

</td>
</tr>
<tr>
<td valign="top">

How can I apply my custom themes to an application?

</td>
<td valign="top">

It is currently not possible to use the UI theme designer to directly theme an application running on a different server. This is due to the security restrictions. Either the application needs to be installed on an instance running the UI theme designer, or the UI theme designer needs to be installed on the instance running the application. Since you need to rebuild themes after an upgrade, we do not recommended deploying custom themes on a server without the UI theme designer installed.

</td>
</tr>
<tr>
<td valign="top">

Which browsers are supported for custom themes?

</td>
<td valign="top">

Support for various browsers varies depending on which SAP standard theme the custom theme is based, as well as which UI technology is considered. Compatibility is also influenced by any custom CSS that is added to the custom theme.

See Product Availability Matrix \(PAM\):[https://support.sap.com/release-upgrade-maintenance/pam.html](https://support.sap.com/release-upgrade-maintenance/pam.html)

</td>
</tr>
</table>

