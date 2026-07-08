<!-- loio066fb621527b4357a259cd09ca308bdd -->

# Theme Limits and Restrictions

The theme repository in the SAP BTP, Cloud Foundry environment enforces limits on the size of the theme, the number of themes per subaccount, allowed file types, and theme ID naming. Themes that violate these constraints can't be saved or uploaded.



<a name="loio066fb621527b4357a259cd09ca308bdd__size_limits"/>

## Size Limits


<table>
<tr>
<th valign="top">

Constraint

</th>
<th valign="top">

Limit

</th>
</tr>
<tr>
<td valign="top">

Theme archive \(ZIP\)

</td>
<td valign="top">

10 MB

</td>
</tr>
<tr>
<td valign="top">

Themes per subaccount

</td>
<td valign="top">

100

</td>
</tr>
<tr>
<td valign="top">

Extracted theme content

</td>
<td valign="top">

100 MB

</td>
</tr>
<tr>
<td valign="top">

Files per theme

</td>
<td valign="top">

10,000

</td>
</tr>
</table>



<a name="loio066fb621527b4357a259cd09ca308bdd__allowed_file_types"/>

## Allowed File Types

Only files of the following types are permitted in a theme:

-   Font files \(for example: WOFF, WOFF2\)
-   Image files \(for example: PNG, JPEG, GIF, SVG\)
-   LESS stylesheets \(`text/less`\)
-   CSS stylesheets \(`text/css`\)
-   JSON files \(`application/json`\)

> ### Caution:  
> SVG files must not contain `<script>` tags or event handler attributes.



<a name="loio066fb621527b4357a259cd09ca308bdd__theme_id_naming_rules"/>

## Theme ID Naming Rules

When naming a theme ID, observe the following rules:

-   The theme ID must be unique across all your themes.
-   The theme ID must start with an alphabetic character.
-   The theme ID must not start with `sap` or with an underscore \(`_`\).
-   Only alphanumeric characters and underscores \(`_`\) are allowed.
-   The maximum length is 30 characters.

Themes that exceed these limits or violate these restrictions are rejected during upload or storage.

