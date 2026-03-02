<!-- loioaf0f4e6e87a04f87905c2d23eff2603b -->

# Defining a Fallback Theme

You can define a fallback theme ID for your themes. This serves as the primary option if end users experience a theme fallback.



<a name="loioaf0f4e6e87a04f87905c2d23eff2603b__section_l43_3s4_jgc"/>

## Prerequisites

-   You have created a different theme as described in [Create and Edit Themes and Theme Sets](../create-and-edit-themes-and-theme-sets-0d2d662.md), or you plan to use a standard SAP theme as the fallback.
-   You are working in the editor as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).



## Context

End users may experience a theme fallback. When this happens, the originally requested theme can’t be applied and a different theme is used. The order in which different themes are tried is described in [Theme Fallback](../../Advanced-Information/theme-fallback-bfe0aa3.md).

With the fallback theme ID you can influence the order, giving priority to your themes.



<a name="loioaf0f4e6e87a04f87905c2d23eff2603b__section_smr_ns4_jgc"/>

## Procedure

1.  Open the *Theme* menu.
2.  Select *Properties*. For more details, see [Changing Theme Properties](changing-theme-properties-9766329.md).
3.  Enter the technical identified of a theme of your choice as *Fallback Theme ID*.
4.  Confirm with *OK*.



## Result

The theme provided as a *Fallback ID* is used as the first candidate of the fallback described in [Theme Fallback](../../Advanced-Information/theme-fallback-bfe0aa3.md).



## Next Steps

Save your changes as described in [Saving Themes](saving-themes-c99d9df.md).



<a name="loioaf0f4e6e87a04f87905c2d23eff2603b__section_npp_ht4_jgc"/>

## Example

Let's consider a scenario where you have an SAP Build Work Zone site on SAP BTP, Cloud Foundry, running SAPUI5 version 1.136, and you integrate applications from an SAP S/4HANA system running SAPUI5 1.71. Your goal is to use the Morning Horizon theme as your base theme \(let's call it `my_theme`\). However, you encounter a compatibility issue:

**Problem:**

While `my_theme` works for the SAP Build Work Zone site, it is not supported for the SAP S/4HANA application because Morning Horizon is not available for SAPUI5 1.71.

**Recommended Solution:**

1.  Create an additional theme based on Quartz Light \(for example, `my_theme_quartz`\).
2.  To save time, use the *Migrate* function to copy your customization from `my_theme` to `my_theme_quartz` as described in [Migrating Themes](../migrating-themes-cb63341.md).
3.  Make any necessary adjustments to `my_theme_quartz` as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).
4.  Save and publish `my_theme_quartz`. For more information, see [Saving Themes](saving-themes-c99d9df.md) and [Publishing Themes and Theme Sets](../publishing-themes-and-theme-sets-f4889a4.md).
5.  Set `my_theme_quartz` as the fallback theme for `my_theme`.

**Result:**

When the SAP S/4HANA application runs with SAPUI5 1.71, `my_theme_quartz` will be used automatically as the fallback theme.

By following this approach, you ensure that both the SAP Build Work Zone site and the SAP S/4HANA application have compatible themes, even though they run on different SAPUI5 versions. The fallback theme \(`my_theme_quartz`\) provides a consistent styling for the SAP S/4HANA application when the main theme \(`my_theme`\) is not supported.



## Related Information

-   [Supported Combinations of Themes and Libraries](https://sapui5.hana.ondemand.com/sdk/#/topic/38ff8c27b022475a92b591bcf6262551.html) in the SAPUI5 documentation
-   Sap Note [2124106](https://me.sap.com/notes/2124106) - Visual themes for Unified Rendering based UI technologies

