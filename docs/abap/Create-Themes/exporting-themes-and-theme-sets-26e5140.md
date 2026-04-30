<!-- loio26e5140268f94045b3b031c4027fff4d -->

# Exporting Themes and Theme Sets

You can export themes and theme sets as a zip archive.



## Prerequisites

-   You are on the welcome page as described in [Managing Themes and Theme Sets on the Welcome Page](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/e3585083d5ef4478b455d8773d5b25c0.html "On the welcome page, you can manage themes and theme sets - create new ones, edit, publish, export, delete, rename, duplicate and migrate them.") :arrow_upper_right:.
-   You have created a theme or theme set as described in [Create and Edit Themes and Theme Sets](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/0d2d662651d443288b5dce463acf4193.html "As a designer, you can create themes and theme sets to apply your brand to SAP Build Work Zone sites and applications.") :arrow_upper_right:.



## Context

When you export a theme, you can configure the contents of the zip archive depending on your use case. For example, you can include built CSS resources or even the resources of the base theme. With that, you can transport themes and theme sets between systems as described in [Transporting Themes Between Systems](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/ebc8f52da8ea43d58335501c8d87ddcc.html "") :arrow_upper_right:.



<a name="loio26e5140268f94045b3b031c4027fff4d__steps_hzb_k1n_pl"/>

## Procedure

1.  Select the theme or theme set you want to export.

2.  Choose *Export*.

3.  **Optional:** Update the properties of the theme as described in [Changing Theme Properties](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/97663296135e4d5eae6204e2811f355f.html "You can change your theme properties. These include Theme ID, Title, Vendor, and Fallback Theme ID.") :arrow_upper_right: or of the theme set as described in [Customizing Theme Sets](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/ca5d6beed238406bafa899420f03469b.html "You can create theme sets to define light, dark, and high‑contrast appearances for your theme.") :arrow_upper_right:. Select *Support RTL* to build files that support right-to-left languages such as Arabic or Hebrew.

    > ### Note:  
    > Updating the properties does not modify the theme or theme set itself. Just the theme or theme set in the exported zip archive will have the updated properties.

4.  **Optional:** Configure export settings for themes.

    When exporting themes, you can expand the *Optional Settings \(for Experts\)* panel to select additional resources beyond the source files that are needed to rebuild the theme in the target environment.

    -   *Source Files Only*: The exported zip archive contains only the source files strictly necessary to import the theme in the theme designer of the target system. Use this option if you plan to import the theme into a theme designer.
    -   *Source Files + CSS Resources*: The exported zip archive also contains the built CSS files. Use this option if you plan to import the theme into SAP Mobile Start. For more information, see [Themes for Custom Corporate Branding](https://help.sap.com/docs/mobile-start/mobile-start-administration-guide/themes-for-custom-corporate-branding-overview?version=2.5) in the SAP Mobile Start help pages.
    -   *Source Files + CSS Resources + Base Theme Resources*: The exported zip archive also contains the resources of the base theme, such as fonts and images. Use this option if you plan to self-host the theme in an environment without the UI theme designer.
    -   UI technologies: Deselect the UI technologies that you don't need in the export zip archive. All UI technologies that are selected will be included in the archive. For example, if you export to SAP Mobile Start or Fundamental Library, deselect everything.

5.  Confirm with *Export*.




## Results

This will download a zip archive based on your choices. To get more information about the structure of the zip archive, see [What is a Theme?](../About-Themes/what-is-a-theme-71bcf85.md)

> ### Note:  
> An exported zip archive of a theme set doesn't include the themes that are the appearances of that theme set. You need to export them separately.



## Next Steps

Import your theme or theme set in your target environment as described in [Importing Themes and Theme Sets](importing-themes-and-theme-sets-5e3c430.md).

> ### Note:  
> You can also export themes from the *Theme* menu of the editor under *Theme* \> *Export...*. For more information, see [Customizing Themes in the Editor](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/aa4b233eb1da4f30ae6d888424a92de5.html "In the editor you can make changes to themes and preview them.") :arrow_upper_right:.

