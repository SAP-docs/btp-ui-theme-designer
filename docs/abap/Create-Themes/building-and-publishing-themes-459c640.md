<!-- loio459c6409eb2f4b7bb4113f6a8eda3fdd -->

# Building and Publishing Themes

Once you have finished editing your theme, you need to build CSS files so the theme can be applied to an application.



## Context

A theme consists of LESS files and resources \(for example images\). During the build process, CSS files are generated from the LESS files. After the CSS generation, your theme can be applied to a running application.



<a name="loio459c6409eb2f4b7bb4113f6a8eda3fdd__steps_tct_yv3_tj"/>

## Procedure

1.  Choose *Theme* \> *Save&Build*.

2.  In the *Save&Build* dialog box, provide the following:


    <table>
    <tr>
    <th valign="top">

    Parameter
    
    </th>
    <th valign="top">

    Description
    
    </th>
    <th valign="top">

    Values
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Theme ID
    
    </td>
    <td valign="top">
    
    The ID that applications can reference in order to use the theme, for example using the `sap-theme` URL parameter.
    
    </td>
    <td valign="top">
    
    -   Only alphanumeric characters are allowed.
    -   Must not start with `"SAP"`.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Title
    
    </td>
    <td valign="top">
    
    \(Optional\)

    The theme name that is displayed in the theme list on the start screen.
    
    </td>
    <td valign="top">
    
    Must not start with `"SAP"`.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Vendor
    
    </td>
    <td valign="top">
    
    \(Optional\)

    The name of the company that acts as the vendor of the theme.
    
    </td>
    <td valign="top">
    
    Must not start with `"SAP"`.
    
    </td>
    </tr>
    </table>
    
3.  Decide whether you require a Right-to-Left \(RTL\) version of your theme.

    Right-to-left languages, such as Hebrew and Arabic, require different stylesheets and images than left-to-right \(LTR\) languages.

    Mark the *Create RTL theme* checkbox to create stylesheets for both LTR and RTL languages.

4.  Choose *Save&Build*.




<a name="loio459c6409eb2f4b7bb4113f6a8eda3fdd__result_N10063_N10012_N10001"/>

## Results

Your theme can now be applied to a running application.

For more information, see [Applying Custom Themes to Standalone Apps](../Use-Case-Scenarios/applying-custom-themes-to-standalone-apps-e6ede69.md).

When you restart the UI theme designer, your theme is displayed in the list on the start screen.

You or other users can select the theme. You have the following options:

-   To make further adjustments to the theme, choose *Open*.
-   To use the theme as a template to create another theme, choose *Copy*.

