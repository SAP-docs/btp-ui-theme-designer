<!-- loioe3585083d5ef4478b455d8773d5b25c0 -->

# Managing Themes and Theme Sets on the Welcome Page

On the welcome page, you can manage themes and theme sets - create new ones, edit, publish, export, delete, rename, duplicate and migrate them.



## Prerequisites

You have launched the Theme Designer web app as described in [Launching the Theme Designer Web App](launching-the-theme-designer-web-app-8f49dce.md).



## Welcome Page Overview

![Welcome page of the UI theme designer web app with theme selection and
							create a new theme button.](images/Image_map_UI_Theme_Designer_welcome_page_915a582.png)



<a name="loioe3585083d5ef4478b455d8773d5b25c0__section_kwc_tcq_13c"/>

## New Themes and Theme Sets

The top-right corner of the welcome page allows to *Create a New Theme* or *Create a New Theme Set*. Both will take you to a dialog where you can provide details. For more information, see [Creating New Themes and Theme Sets](creating-new-themes-and-theme-sets-72c730b.md).

You can also *Import* a theme or theme set from somewhere else. For more information, see [Importing Themes and Theme Sets](importing-themes-and-theme-sets-5e3c430.md) and [Transporting Themes Between Systems](../Administration/transporting-themes-between-systems-ebc8f52.md).

You can select a specific SAPUI5 version to preview your themes, ensuring that the preview reflects exactly how your themes appear with that version.



<a name="loioe3585083d5ef4478b455d8773d5b25c0__section_pv5_kdq_13c"/>

## Existing Themes and Theme Sets

The main part of the welcome page shows all existing themes and theme sets. You can use the search field on the left to filter the list.



### Actions

You can select a theme or theme set to perform one of the following actions:

-   *Edit* a theme or theme set as described in [Editing Themes and Theme Sets](editing-themes-and-theme-sets-04d4487.md).
-   *Publish* a theme or theme set as described in [Publishing Themes and Theme Sets](publishing-themes-and-theme-sets-f4889a4.md).
-   *Export* a theme or theme set as described in [Exporting Themes and Theme Sets](exporting-themes-and-theme-sets-26e5140.md).
-   *Delete* a theme or theme set as described in [Deleting Themes and Theme Sets](deleting-themes-and-theme-sets-0729728.md).
-   *Rename* a theme or theme set as described in [Renaming Themes and Theme Sets](renaming-themes-and-theme-sets-39a6269.md).
-   *Duplicate* a theme or theme set as described in [Duplicating Themes and Theme Sets](duplicating-themes-and-theme-sets-ec77044.md).
-   *Migrate* a theme as described in [Migrating Themes](migrating-themes-cb63341.md). Theme sets cannot be migrated.

In the *Details* menu you can view:

-   General information about the theme and theme set, such as:
    -   Vendor and technical ID. For more information, see [Changing Theme Properties](Customizing-Themes-in-the-Editor/changing-theme-properties-9766329.md).
    -   Date the theme was created, last published and last modified
    -   Current status

-   Theme-specific details:
    -   Prominent colors
    -   Base theme
    -   Build status for the selected SAPUI5 version

-   Theme-set-specific details:
    -   Technical IDs of the included light, dark and high contrast appearances.




### States

A theme or theme set can have one of the following states:

-   *Never Published* - The theme is saved but has never been published. It cannot be applied to applications. Choose *Publish* to make it available for applications.
-   *Modified* - The theme has been changed after publishing. The latest changes are not applied to applications. Choose *Publish* to activate the updated version and make the changes available.
-   *Published* - The theme has been published. It is ready to be applied to an application.

