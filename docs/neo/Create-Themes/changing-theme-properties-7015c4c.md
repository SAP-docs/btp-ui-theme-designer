<!-- copy7015c4cefad848fc99f069a5a722d250 -->

# Changing Theme Properties

You can change your theme properties. These include *Theme ID*, *Title*, *Vendor*, and *Fallback Theme ID*.



## Prerequisites

You are working in the editor as described in [Customizing Themes in the Editor](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/aa4b233eb1da4f30ae6d888424a92de5.html "In the editor you can make changes to themes and preview them.") :arrow_upper_right:.



## Procedure

1.  Open the *Theme* menu.

2.  Select *Properties*.

3.  Enter the properties you want to change:

    -   *Theme ID*: the technical identifier for the theme. This value is case-sensitive. It must meet the following requirements:
        -   must be unique across all your themes
        -   must contain only alphanumerical characters and underscores
        -   must start with alphabetic character
        -   must not start with "SAP", \(case-insensitive\)
        -   must not exceed 30 characters


    > ### Note:  
    > You can't change the *Theme ID* directly. To change it, rename the theme as described in [Renaming Themes and Theme Sets](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/39a6269c0d4c49e994fc5957dcc81409.html "You can rename themes and theme sets to change their properties.") :arrow_upper_right:. To create a copy with a different Theme ID, duplicate the theme as described in [Duplicating Themes and Theme Sets](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/ec77044b20ba4888a1d8de474f76a040.html "You can create a copy of an existing theme or theme set by duplicating it.") :arrow_upper_right:.

    -   *Based On*: the technical identifier of the SAP theme your theme is based on.

    > ### Note:  
    > *Based On* cannot be changed directly. To create a copy based on a different SAP theme, migrate the theme as described in [Migrating Themes](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/cb63341115d444ac8bec8bb44ad63498.html "Here's how you can migrate custom themes.") :arrow_upper_right:.

    -   *Title*: the human-readable title of your theme.
    -   *Vendor* \(optional\): the human-readable name of the organization that provides the theme. The name must not start with “SAP” \(case-insensitive\).
    -   *Fallback Theme ID* \(optional\): the technical identifier of a theme to use as a fallback. For more information, see [Defining a Fallback Theme](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/af0f4e6e87a04f87905c2d23eff2603b.html "You can define a fallback theme ID for your themes. This serves as the primary option if end users experience a theme fallback.") :arrow_upper_right:.

4.  Select *OK* to confirm.




## Results

The properties of your theme are updated.



## Next Steps

Save your theme with the updated properties as described in [Saving Themes](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/c99d9df29d3c4a45a883e15ce2753178.html "You can save changes you made in your theme at any time during its creation and design.") :arrow_upper_right:.

