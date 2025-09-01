<!-- loioaf0f4e6e87a04f87905c2d23eff2603b -->

# Defining a Fallback Theme

You can define a fallback theme in the UI theme designer.

A fallback theme is a theme that serves as a backup option when the main theme is invalid or cannot be compiled when requested by an application. For example, a theme is considered invalid if it is based on an SAP theme that is not supported for the requested UI technology version.

You can define a fallback theme in the UI theme designer to ensure that applications always receive proper styling and remain usable, even if the assigned theme is unavailable. Defining a fallback theme is especially recommended when you run applications with different UI technologies or versions, each supporting different SAP themes.



<a name="loioaf0f4e6e87a04f87905c2d23eff2603b__section_l43_3s4_jgc"/>

## Prerequisite

-   You have created and published a fallback theme, or you plan to use a standard SAP theme as the fallback.



<a name="loioaf0f4e6e87a04f87905c2d23eff2603b__section_smr_ns4_jgc"/>

## Procedure

1.  Open the UI theme designer and create a new theme or edit an existing one.
2.  Go to the *Theme* menu and select *Properties*.
3.  Enter the *Fallback Theme ID*.

    > ### Note:  
    > The Fallback Theme ID should be the ID of the theme you want to use as the fallback.

4.  Confirm with *OK*.
5.  In the *Theme* menu, select *Save & Publish*.



<a name="loioaf0f4e6e87a04f87905c2d23eff2603b__section_npp_ht4_jgc"/>

## Example

Let's consider a scenario where you have an SAP Build Work Zone site on SAP BTP, Cloud Foundry, running SAPUI5 version 1.136, and you integrate applications from an SAP S/4HANA system running SAPUI5 1.71. Your goal is to use the Horizon Morning theme as your base theme \(let's call it `my_theme`\). However, you encounter a compatibility issue:

Problem:

-   While `my_theme` works for the SAP Build Work Zone site, it is not supported for the SAP S/4HANA application because Horizon is not available for SAPUI5 1.71.

Recommended Solution:

1.  Create an additional theme based on Quartz \(e.g., `my_theme_quartz`\).
2.  To save time, use the *Migrate Theme* function to copy your customizations from `my_theme` to `my_theme_quartz`.
3.  Make any necessary adjustments to `my_theme_quartz`.
4.  Save and publish `my_theme_quartz`.
5.  Set `my_theme_quartz` as the fallback theme for `my_theme`.

Result:

-   When the SAP S/4HANA application runs with SAPUI5 1.71, `my_theme_quartz` will be used automatically as the fallback theme.

By following this approach, you ensure that both the SAP Build Work Zone site and the SAP S/4HANA application have compatible themes, even though they run on different SAPUI5 versions. The fallback theme \(`my_theme_quartz`\) provides a consistent styling for the SAP S/4HANA application when the main theme \(`my_theme`\) is not supported.

**Related Information**  


[SAPUI5 SAP Theme Support](https://sapui5.hana.ondemand.com/sdk/#/topic/38ff8c27b022475a92b591bcf6262551.html)

[SAP Note 2124106](https://me.sap.com/notes/2124106   "Unified Rendering SAP Theme Support")

