<!-- loio26a9a94647f44b66804364c691bf8122 -->

# Saving Themes

Administrators save themes to make them available for applying to SAPUI5 applications.



## Context

You have the option to save a theme draft and continue working on your theme at a later point in time. This means that only the LESS files defining the theme are saved.

In order for the theme to be applied to an application, the CSS files have to be built from the LESS files using the *Save&Build* function. For more information, see [Building and Publishing Themes](building-and-publishing-themes-459c640.md).

> ### Note:  
> Content in the *Target Pages* area is not an integral part of the theme itself. These pages and applications are, therefore, **not** stored with the theme but in the local storage of the browser. They remain there until the local storage is cleared.



## Procedure

1.  Choose *Theme* \> *Save*.

2.  In the *Save* dialog box, provide the following:


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
    
    The ID that applications reference in order to use the theme, for example using the `sap-theme` URL parameter.

    For more information, see [Applying Custom Themes to Standalone Apps](../Use-Case-Scenarios/applying-custom-themes-to-standalone-apps-e6ede69.md).
    
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

    The theme name that will be displayed in the theme list on the start screen after the theme.
    
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

4.  Choose *OK*.




<a name="loio26a9a94647f44b66804364c691bf8122__result_N10063_N10012_N10001"/>

## Results

When you restart the UI theme designer, your theme is displayed in the list on the start screen.

You or other users can select the theme. You have the following options:

-   To make further adjustments to the theme, choose *Open*.
-   To use the theme as a template to create another theme, choose *Copy*.

Now you can go ahead and build and publish your theme. For more information, see [Building and Publishing Themes](building-and-publishing-themes-459c640.md).

