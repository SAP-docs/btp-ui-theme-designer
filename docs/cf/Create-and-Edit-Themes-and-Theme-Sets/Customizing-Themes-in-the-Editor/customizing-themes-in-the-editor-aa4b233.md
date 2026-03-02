<!-- loioaa4b233eb1da4f30ae6d888424a92de5 -->

<link rel="stylesheet" type="text/css" href="../../css/sap-icons.css"/>

# Customizing Themes in the Editor

In the editor you can make changes to themes and preview them.



## Prerequisites

You are editing a theme as described in [Editing Themes and Theme Sets](../editing-themes-and-theme-sets-04d4487.md).



## Overview of the Editor

The interface includes a shell bar with the *Theme Menu* and the theme title. The editor contains three panes:

-   The *Preview Pages* pane, which lists preview pages grouped by UI technologies;
-   The *Preview* pane, which shows the page selected in the *Preview Pages* pane;
-   The *Editor* pane, which provides guides and tools for editing the theme.

You can resize the panes by dragging the dividers.



## Theme Menu

In this menu you can access actions that affect the entire theme:

-   *Test Build* attempts to build the theme directly in the browser. Use it to check whether problems will occur when you publish your theme, as described in [Publishing Themes and Theme Sets](../publishing-themes-and-theme-sets-f4889a4.md). If it fails, double-check the changes you made to the theme by using the delta and error filters, as described in [Expert Theming](expert-theming-7b01607.md). Also, review your Custom CSS, as described in [Adding Custom CSS](adding-custom-css-895a4b0.md).
-   *Save*, *Save As*, and *Save & Publish* all save the changes you made, as described in [Saving Themes](saving-themes-c99d9df.md).
    -   *Save As* duplicates the theme to a new theme with the properties you specify, leaving the original theme unchanged.
    -   *Save & Publish* also publishes the theme and makes it available for use with applications. For more information, see [Publishing Themes and Theme Sets](../publishing-themes-and-theme-sets-f4889a4.md).

-   *Export* exports the theme to a zip archive, as described in [Exporting Themes and Theme Sets](../exporting-themes-and-theme-sets-26e5140.md).
-   *Properties* lets you edit the theme properties, except the Theme ID, as described in [Changing Theme Properties](changing-theme-properties-9766329.md).
-   *Close* closes the editor and returns you to the welcome page. The process is described in [Managing Themes and Theme Sets on the Welcome Page](../managing-themes-and-theme-sets-on-the-welcome-page-e358508.md).



## Preview Pages Pane

Within the editor, the *Preview Pages* pane lists available preview pages, organized by test suites and covering different aspects of various UI technologies. You can add more predefined previews and include your own applications. For more information, see [Selecting and Adding Preview Pages](selecting-and-adding-preview-pages-8988483.md).



## Preview Pane

The *Preview* pane displays the preview you selected in the *Preview Pages* pane. It provides a live view of how the changes you make to your theme affect controls or applications.

The preview toolbar includes:

-   The *Original/Preview* toggle switches between your custom theme \(*Preview*\) and the base theme \(*Original*\) in the preview pane to compare differences.
-   Depending on the UI technology of the preview, you can toggle between *Desktop/Mobile/Tablet* views. *Desktop* uses all available space. *Mobile* and *Tablet* display the preview on simulated device screens. When you select *Mobile* or *Tablet*, another toggle button appears that lets you switch between portrait and landscape mode.
-   *Full Width* <span class="SAP-icons-V5"></span>: Expands the *Preview* pane to fill the editor workspace and collapses the *Preview Pages* pane and the *Editor* pane. The shell bar with the *Theme Menu* remains visible.
-   *Play* <span class="SAP-icons-V5"></span>: Opens the preview in a new browser tab with the theme applied. If there are unpublished changes, you’ll be prompted to publish the theme first.
-   *Reload* <span class="SAP-icons-V5"></span>: Reloads the preview, useful for resolving preview issues or returning to a clean state.



## Editor Pane

Use the Editor pane to modify your theme. Here you make changes to the theme as described in [Changing Parameters](changing-parameters-0d328f8.md).

There are different approaches to theming, depending on the granularity you need:

-   [Quick Theming](quick-theming-e4d2a95.md) is the highest-level approach. It highlights the few parameters that have the most impact on the theme. This approach matches the Quick Theming application preview in SAPUI5 and Unified Rendering.
-   [Detailed Theming](detailed-theming-db09bb9.md) offers a curated list of parameters that have a significant impact on the theme.
-   [Mobile Theming](mobile-theming-6237538.md) is specifically designed for theming SAP Mobile Start. It matches the SAP Mobile Start application previews.
-   [Expert Theming](expert-theming-7b01607.md) provides full access to all themable parameters. You can filter these parameters based on different attributes. There should be a one-to-one mapping between parameter tags and SAPUI5 control previews.
-   *Palette* lets you define your own color parameters for [Reusing Color Parameters](reusing-color-parameters-16ed37f.md).
-   *CSS* allows [Adding Custom CSS](adding-custom-css-895a4b0.md) to themes in different UI technologies. Use this option with caution.

