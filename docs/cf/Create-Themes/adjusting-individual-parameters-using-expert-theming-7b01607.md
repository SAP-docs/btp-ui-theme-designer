<!-- loio7b01607cb9564f6d94087a6db995c350 -->

# Adjusting Individual Parameters Using Expert Theming

If you want to change more than the *Quick* or *Detailed* panels could offer, you can use expert theming to make fine-tuned adjustments to your theme.



<a name="loio7b01607cb9564f6d94087a6db995c350__prereq_ycq_th3_3yb"/>

## Prerequisites

-   You have created a theme or selected an existing one and opened it for editing. For more information, see [Creating a New Theme](creating-a-new-theme-72c730b.md).

-   You have added preview pages and selected one of them. For more information, see [Adding Preview Pages](adding-preview-pages-8af60d3.md).




<a name="loio7b01607cb9564f6d94087a6db995c350__context_N10015_N10012_N10001"/>

## Context

Expert theming allows a finer grain of changes than Quick theming, supporting both cross UI technology parameters and UI technology-specific parameters. Expert parameters may evolve over time, potentially requiring maintenance after upgrades.

These parameters can influence many elements if they are very generic \(e.g. the default text color\), only some parameters of one control \(e.g. the different colors of lists\) or no other parameters at all \(e.g. the distance between two fields in a special control\).



<a name="loio7b01607cb9564f6d94087a6db995c350__steps_rl1_m4r_y3b"/>

## Procedure

1.  On top of the side panel on the right, choose *Expert*.

2.  Search for the parameters you need to change.

    You have the following filter and search options:

    -   Filter for parameters that have the same type. The following categories are available:

        ****


        <table>
        <tr>
        <th valign="top">

        Category Icon
        
        </th>
        <th valign="top">

        Description
        
        </th>
        </tr>
        <tr>
        <td valign="top">
        
        ![Show Colors Only](images/Show_Colors_Only_0aa8c11.png)
        
        </td>
        <td valign="top">
        
        Shows parameters with color value.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        ![Show Text Attributes Only](images/Show_Text_Attributes_Only_c718da5.png)
        
        </td>
        <td valign="top">
        
        Shows parameters related to typography.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        ![Show Dimensions Only](images/Show_Dimensions_Only_f6ab91b.png)
        
        </td>
        <td valign="top">
        
        Shows parameters with dimension value \(em, px, pt, % etc.\).
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        ![Show Images Only](images/Show_Images_Only_fdbb8a4.png)
        
        </td>
        <td valign="top">
        
        Shows parameters representing an image.
        
        </td>
        </tr>
        </table>
        
    -   Choose ![](images/Delta_Filter_f19cafd.png) to show changed parameters only.
    -   Choose ![](images/Control_Picker_2d4d775.png) to switch on the element picker mode.

        When you hover over an element in the preview area, it is highlighted. When you select the element, only parameters that are related to the selected element are displayed.

    -   Choose ![Tag View](images/Tag_View_fdc5ba6.png) to switch to the tag view.

        A list of toggle links with filter categories is displayed. Select a link to add all available parameters with that tag to the parameter list. Selecting additional links restricts the list of parameters displayed.

    -   Use the search input field to search for a string in the parameter name.

        For example, enter the search string `disabled` to filter for all parameters that define the visual appearance of disabled controls.

    -   You can find more possibilities to find the relevant parameters in [Finding the Relevant Expert Parameters \(Experimental\)](finding-the-relevant-expert-parameters-experimental-0980cc6.md).


    If you hover about a parameter name in the list, you get a popup with additional formation about the parameter. Here you find the name, a description, the current value, the last saved value and the original value, some more information about the parameter, and the tags which are assigned to this parameter. You have the possibility to copy the parameter name into the clipboard and you can restore the value to the last saved one or to the original value.

3.  Change the parameter values according to your needs.

4.  To switch between parameters of standard and contrast areas of themes based on SAP Belize, toggle the contrast switch in the value column header.

    With SAP Belize, there are some themeable “contrast” areas whose parameters are only displayed when this toggle is clicked.


