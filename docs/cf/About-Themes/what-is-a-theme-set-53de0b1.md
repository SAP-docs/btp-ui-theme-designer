<!-- loio53de0b11cdd048719f9646eef01f6c67 -->

# What is a Theme Set?

A theme set provides multiple themes so users can choose the appearance that best matches their system preferences.

SAP Build Work Zone sites and applications use a theme set to switch between light, dark, and high-contrast appearances based on users' operating system settings. For more information on how to work with theme sets, see [Create and Edit Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/create-and-edit-themes-and-theme-sets-0d2d662.md).



## What Can You Customize in a Theme Set?

In a theme set, you can select themes as appearances for the following environments:

-   a low-contrast light environment \(*Light Theme*\)
-   a low-contrast dark environment \(*Dark Theme*\)
-   a high-contrast light environment \(*Light High-Contrast Theme*\)
-   a high-contrast dark environment \(*Dark High-Contrast Theme*\)

For details on the properties you can customize, see [Customizing Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/customizing-theme-sets-ca5d6be.md).

For information about the theme sets that SAP provides, see [Overview of SAP Theming Content](overview-of-sap-theming-content-91ebfe2.md).

> ### Note:  
> Only themes based on Horizon- or Quartz-like themes can be used as appearances in theme sets.



## Structure of a Theme Set

A theme set is a list of technical identifiers for themes and the conditions in which these identifiers apply.

These conditions may include:

-   **Contrast:** `LOW` or `HIGH`. Contrast is usually evaluated based on the `prefers-contrast` CSS media feature. The values `no-preference` and `low` map to `LOW`. The values `custom` and `more` map to `HIGH`. For more information, see [MDN: prefers-contrast](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-contrast).
-   **Color scheme:** `LIGHT` or `DARK`. The color scheme is usually evaluated based on the `prefers-color-scheme` CSS media feature. For more information, see [MDN: prefers-color-scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-color-scheme).

One theme may be marked as the default.

The first theme that matches all conditions is selected.

If no theme matches, the default theme is selected. If there is no default, the first theme in the list is selected.

> ### Note:  
> A theme set does not include the themes themselves. It only references them by their technical identifiers. This has several important implications:
> 
> -   To publish a theme set, you need to publish all referenced themes. For more information, see [Publishing Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/publishing-themes-and-theme-sets-f4889a4.md).
> -   To transport a theme set, you need to transport all its appearances before you import the theme set. For details, see [Exporting Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/exporting-themes-and-theme-sets-26e5140.md) and [Importing Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/importing-themes-and-theme-sets-5e3c430.md).
> -   Renaming or deleting a theme that a theme set references can cause serious issues. Consider these actions carefully. For guidance, see [Renaming Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/renaming-themes-and-theme-sets-39a6269.md) and [Deleting Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/deleting-themes-and-theme-sets-0729728.md).
> -   Deleting a theme set does not affect its appearances. These remain as individual themes.
> -   Theme sets cannot be migrated, as there is nothing to migrate.
> -   A theme can appear in multiple theme sets. It can also be used as a standalone theme at the same time.
> -   Any theme can be used as any appearance. For example, you can use a theme based on High-Contrast Black \(Horizon\) as the low-contrast light appearance.



## Example

To set up an automated “night shift” switch from a light to a dark version of your theme, follow these steps:

1. Start with a light theme, as described in [Create and Edit Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/create-and-edit-themes-and-theme-sets-0d2d662.md). *For this example, assume the theme is based on *Morning Horizon* and uses the technical identifier `my_horizon`.*

2. Migrate your theme to a different theme that uses a dark base, as described in [Migrating Themes](../Create-and-Edit-Themes-and-Theme-Sets/migrating-themes-cb63341.md). Double-check the migration results as described in [Customizing Themes in the Editor](../Create-and-Edit-Themes-and-Theme-Sets/Customizing-Themes-in-the-Editor/customizing-themes-in-the-editor-aa4b233.md). *In this example, assume the theme is migrated to *Evening Horizon* and uses the technical identifier `my_horizon_dark`.* 

3. Create a theme set as described in [Creating New Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/creating-new-themes-and-theme-sets-72c730b.md). Select your two themes as the *Light Theme* and the *Dark Theme*. For now, leave the high-contrast themes at their default values. You can adjust these in steps six through eight below. *In this example, assume `my_horizon` is the light theme and `my_horizon_dark` is the dark theme. The technical identifier of the theme set is `my_horizon_set`.* 

4. You can't publish your theme set yet because the appearances aren't published. First, publish the individual themes as described in [Publishing Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/publishing-themes-and-theme-sets-f4889a4.md). Then, publish the theme set.

5. Go to the SAP Build Work Zone Theme Manager. Make the theme set available for end user selection as described in **How to apply the themes to your site** in [SAP Build Work Zone, advanced edition: Overview of Theming and Branding](https://help.sap.com/docs/build-work-zone-advanced-edition/sap-build-work-zone-advanced-edition/overview-of-theming-and-branding) and [SAP Build Work Zone, standard edition: Overview of Theming and Branding](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/overview-of-theming-and-branding).

If you want to include your own high-contrast appearances, you can:

6. Migrate your light theme to a light high-contrast theme. Review the results. *In this example: migrate `my_horizon` to `my_horizon_hcw` based on High-Contrast White \(Horizon\).* 

7. Migrate your dark theme to a theme that is a dark high-contrast theme. Review the results. *In the example, migrate `my_horizon_dark` to `my_horizon_hcb` based on High-Contrast Black \(Horizon\).* 

8. Edit your theme set to use the themes you created. *In the example: use `my_horizon_hcw` as the *Light High-Contrast Theme* and `my_horizon_hcb` as the *Dark High-Contrast Theme*.* 

9. Publish the themes and the theme set.

> ### Note:  
> You can also create all themes manually or use different migration paths. The Light Theme→Dark Theme, Light Theme→Light High-Contrast Theme and Dark Theme→Dark High-Contrast Theme paths usually have the biggest similarities, which implies less manual effort.



## Related Information

To make themes and theme sets available for users to select as an administrator in SAP Build Work Zone, see [SAP Build Work Zone, advanced edition: Overview of Theming and Branding](https://help.sap.com/docs/build-work-zone-advanced-edition/sap-build-work-zone-advanced-edition/overview-of-theming-and-branding) and [SAP Build Work Zone, standard edition: Overview of Theming and Branding](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/overview-of-theming-and-branding).

To select themes and theme sets as an end user in SAP Build Work Zone, see the **Appearance** section in [SAP Build Work Zone, advanced edition: Managing Your Settings](https://help.sap.com/docs/build-work-zone-advanced-edition/sap-build-work-zone-advanced-edition/managing-your-settings) and [SAP Build Work Zone, standard edition: Managing Your Settings](https://help.sap.com/docs/build-work-zone-standard-edition/sap-build-work-zone-standard-edition/managing-your-settings?version=Cloud).

