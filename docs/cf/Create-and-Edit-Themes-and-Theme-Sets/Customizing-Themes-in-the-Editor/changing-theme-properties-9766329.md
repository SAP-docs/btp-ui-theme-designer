<!-- loio97663296135e4d5eae6204e2811f355f -->

# Changing Theme Properties

You can change your theme properties. These include *Theme ID*, *Title*, *Vendor*, and *Fallback Theme ID*.



## Prerequisites

You are working in the editor as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).



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
    > You can't change the *Theme ID* directly. To change it, rename the theme as described in [Renaming Themes and Theme Sets](../renaming-themes-and-theme-sets-39a6269.md). To create a copy with a different Theme ID, duplicate the theme as described in [Duplicating Themes and Theme Sets](../duplicating-themes-and-theme-sets-ec77044.md).

    -   *Based On*: the technical identifier of the SAP theme your theme is based on.

    > ### Note:  
    > *Based On* cannot be changed directly. To create a copy based on a different SAP theme, migrate the theme as described in [Migrating Themes](../migrating-themes-cb63341.md).

    -   *Title*: the human-readable title of your theme.
    -   *Vendor* \(optional\): the human-readable name of the organization that provides the theme. The name must not start with “SAP” \(case-insensitive\).
    -   *Fallback Theme ID* \(optional\): the technical identifier of a theme to use as a fallback. For more information, see [Defining a Fallback Theme](defining-a-fallback-theme-af0f4e6.md).

4.  Select *OK* to confirm.




## Results

The properties of your theme are updated.



## Next Steps

Save your theme with the updated properties as described in [Saving Themes](saving-themes-c99d9df.md).

