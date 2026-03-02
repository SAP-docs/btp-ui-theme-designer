<!-- loio16ed37f3d20a48b49c71108017caf0a8 -->

<link rel="stylesheet" type="text/css" href="../../css/sap-icons.css"/>

# Reusing Color Parameters

You can create your own *Palette* of color parameters and reference them throughout your theme.



## Prerequisite

You are working in the editor as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).



## Procedure



### To create a palette parameter:

1.  In the *Editor* pane, select *Palette*.
2.  Enter the name of the parameter you want to create in the first input field. It must meet the following requirements:
    -   must be unique within your theme
    -   must contain only alphanumeric characters and underscores
    -   must start with an alphabetic character
    -   must not start with "SAP" \(case-insensitive\) or an underscore
    -   must not exceed 50 characters

3.  Choose the color of the parameter as described in [Changing Colors](changing-colors-b6900f3.md).
4.  Confirm with *Add palette parameter* <span class="SAP-icons-V5"></span>.



### To use a palette parameter:

1.  Change the value of a color parameter as described in [Changing Colors](changing-colors-b6900f3.md).
2.  In the color picker, select the palette parameter you want to use from the *Palette* section.
3.  Select *OK* to confirm.



## Result

The palette parameter you created is available in your theme in all UI technologies.



## Next Steps

Use your palette parameter.

To use your palette parameter as a CSS custom property, see the example in [Adding Custom CSS](adding-custom-css-895a4b0.md).

