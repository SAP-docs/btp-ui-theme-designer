<!-- loio5e3c4306f8d64f829f32285aa95a23db -->

# Importing Themes and Theme Sets

You can import themes and theme sets as an archive file from your local hard disk.



## Prerequisites

You are on the welcome page as described in [Managing Themes and Theme Sets on the Welcome Page](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/e3585083d5ef4478b455d8773d5b25c0.html "On the welcome page, you can manage themes and theme sets - create new ones, edit, publish, export, delete, rename, duplicate and migrate them.") :arrow_upper_right:.



## Procedure

1.  Select the *Import* button.

2.  Drag and drop a zip file archive from your local files to the *Import* dialog box or select the box to call up a file browser. For more information about the structure of themes, see [What is a Theme?](../About-Themes/what-is-a-theme-71bcf85.md)

3.  Confirm with *Import*.




## Next Steps

Edit your theme as described in [Customizing Themes in the Editor](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/aa4b233eb1da4f30ae6d888424a92de5.html "In the editor you can make changes to themes and preview them.") :arrow_upper_right:, or edit your theme set as described in [Customizing Theme Sets](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/ca5d6beed238406bafa899420f03469b.html "You can create theme sets to define light, dark, and high‑contrast appearances for your theme.") :arrow_upper_right:.

> ### Note:  
> -   You can only import themes from other environments if the theme is based on a SAP theme supported by the SAP BTP, Cloud Foundry environment. For example, you can’t import a theme based on Blue Crystal or Tradeshow.
> -   If the source environment supports additional UI technologies not available in the target environment, this theming information will be removed during import and will not be available in the imported theme. For example, theming content of the WebClient UI or NetWeaver Business Client frameworks will be removed.
> -   Theme sets do not contain their appearances. You must first import each referenced theme separately. Themes that are not available will be replaced with the default theme.

