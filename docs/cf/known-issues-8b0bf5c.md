<!-- loio8b0bf5c76c8b4f53b0240b85ecf76353 -->

# Known Issues

A list of common issues you may encounter when using the UI theme designer, along with recommended solutions.

**Known Issues With Solutions**


<table>
<tr>
<th valign="top">

Symptom

</th>
<th valign="top">

Reason

</th>
<th valign="top">

Solution

</th>
</tr>
<tr>
<td valign="top">

A CSS request is blocked or refuses to load.

</td>
<td valign="top">

The CSS file is requested from a different domain, so the browser blocks it due to the same-origin policy.

</td>
<td valign="top">

Update your Content Security Policy \(CSP\) `style-src` rule to include `*` or the correct allowed domains. For more information, see SAP Note [3419459](https://me.sap.com/notes/3419459).

</td>
</tr>
<tr>
<td valign="top">

Unable to use a web font or self-hosted font in a theme.

</td>
<td valign="top">

The UI theme designer does not provide built-in support for web or self-hosted fonts.

</td>
<td valign="top">

Define the font file using a `@font-face` rule in your custom CSS. For more information see SAP Note [3534039](https://me.sap.com/notes/3534039).

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

A SAP theme is applied instead of a custom theme to a SAPUI5 backend application integrated into a SAP Build Work Zone site, even though the custom theme is correctly applied to the site.

</td>
<td valign="top">

**Reason 1:** The integrated SAPUI5 appplication runs with a SAPUI5 version which is not supported anymore and therefore is deleted from the SAPUI5 CDN.

</td>
<td valign="top">

Update your backend system to a supported SAPUI5 version. For more information, see SAP Note [3342088](https://me.sap.com/notes/3342088).

</td>
</tr>
<tr>
<td valign="top">

**Reason 2:** The SAPUI5 version of the application does not support the base SAP theme of your theme.

</td>
<td valign="top">

Define a fallback theme for your theme with a base SAP theme supported for the older SAPUI5 version. For more information, see [Defining a Fallback Theme](defining-a-fallback-theme-af0f4e6.md).

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

A SAP theme is applied instead of a custom theme to all applications and SAP Build Work Zone sites.

</td>
<td valign="top">

**Reason 1:** The theme is based on a deprecated SAP theme.

</td>
<td valign="top">

Ensure your custom theme is based on a supported SAP theme. If your current base theme is deprecated, migrate your theme to a supported SAP theme. For more information, see [Migrating Themes](migrating-themes-cb63341.md).

</td>
</tr>
<tr>
<td valign="top">

**Reason 2:** The theme contains a compilation error.

</td>
<td valign="top">

Open the UI theme designer, edit your theme, and select *Save* and *Publish*. Review and resolve any compilation errors that appear. Then, test your application again with the custom theme.

</td>
</tr>
<tr>
<td valign="top">

Custom CSS is not editable in the UI theme designer editor.

</td>
<td valign="top">

Your user does not have permission to edit custom CSS.

</td>
<td valign="top">

Ask you administrator to assign the role *CustomCssEditor* to your user. For more information, see SAP Note [3087666](https://me.sap.com/notes/3087666).

</td>
</tr>
<tr>
<td valign="top">

The *Publish* action is disabled or not available in the UI theme designer.

</td>
<td valign="top">

Your user does not have permission to publish themes.

</td>
<td valign="top">

Ask you administrator to assign the role *Publisher* to your user. For more information, see SAP Note [3087666](https://me.sap.com/notes/3087666).

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

An internal error \(THEME\_SAVE\_ERROR, 504 gateway timeout\) occurs when attempting to save a theme while using the UI theme designer in a developer scenario.

</td>
<td valign="top">

**Reason 1:** This issue may occur if your application is using an outdated version of the application router.

</td>
<td valign="top">

Update the application router to the latest version as described in SAP Note [3659305](https://me.sap.com/notes/3659305).

</td>
</tr>
<tr>
<td valign="top">

**Reason 2:** You have implemented a before-request handler in your application router that consumes the UI theme designer request streams.

</td>
<td valign="top">

Either avoid reading the stream or ensure the request body remains available for the UI theme designer service. For more information, see SAP Note [3659305.](https://me.sap.com/notes/3659305.)

</td>
</tr>
<tr>
<td valign="top">

Unable to access or use the UI theme designer in a SAP BTP trial account.

</td>
<td valign="top">

The UI theme designer is not available directly in SAP BTP, Cloud Foundry edition. It is offered as part of SAP Build Work Zone.

</td>
<td valign="top">

Request a SAP Build Work Zone trial and use the UI theme designer from within SAP Build Work Zone.

To open the UI theme designer:

1.  Go to the user menu in SAP Build Work Zone.
2.  Select *Theme Manager*.
3.  Select *Launch UI Theme Designer*.

For more information, see SAP Note [2975285](https://me.sap.com/notes/2975285).

</td>
</tr>
<tr>
<td valign="top">

A SAP Build Work Zone site is not usable when a specific theme is applied.

</td>
<td valign="top">

A theme assigned to the SAP Build Work Zone site renders the site unusable. As a result, you cannot open the appearance dialog to select a different theme and resolve the issue yourself.

</td>
<td valign="top">

Start the SAP Build Work Zone site with the `sap-theme` URL parameter to temporarily apply a standard SAP theme.

For example, add `?sap-theme=sap_horizon` to the end of your site URL.

Once the site loads with the temporary theme:

1.  Open the user menu.

2.  Select *Settings*.

3.  Go to *Appearance*.
4.  Change the theme to a working one.



</td>
</tr>
</table>

