<!-- loio5e3c4306f8d64f829f32285aa95a23db -->

# Importing Themes and Theme Sets

You can import themes and theme sets as an archive file from your local hard disk.



## Prerequisites

You are on the welcome page as described in [Managing Themes and Theme Sets on the Welcome Page](managing-themes-and-theme-sets-on-the-welcome-page-e358508.md).



## Procedure

1.  Select the *Import* button.

2.  Drag and drop a zip file archive from your local files to the *Import* dialog box or select the box to call up a file browser. For more information about the structure of themes, see [What is a Theme?](../About-Themes/what-is-a-theme-71bcf85.md)

3.  Confirm with *Import*.




## Next Steps

Edit your theme as described in [Customizing Themes in the Editor](Customizing-Themes-in-the-Editor/customizing-themes-in-the-editor-aa4b233.md), or edit your theme set as described in [Customizing Theme Sets](customizing-theme-sets-ca5d6be.md).

> ### Note:  
> -   You can only import themes from other environments if the theme is based on a SAP theme supported by the SAP BTP, Cloud Foundry environment. For example, you can’t import a theme based on Blue Crystal or Tradeshow.
> -   If the source environment supports additional UI technologies not available in the target environment, this theming information will be removed during import and will not be available in the imported theme. For example, theming content of the WebClient UI or NetWeaver Business Client frameworks will be removed.
> -   Theme sets do not contain their appearances. You must first import each referenced theme separately. Themes that are not available will be replaced with the default theme.

