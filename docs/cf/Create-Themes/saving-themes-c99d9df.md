<!-- loioc99d9df29d3c4a45a883e15ce2753178 -->

# Saving Themes

Administrators save themes to make them available for applying to applications.

You can save your theme at any time during its creation and design.

To save your theme, proceed with the following steps:

1.  Choose *Theme* \> *Save As...*.

2.  In the *Save As...* dialog box, provide the following information:


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
    
    The ID that applications reference in order to use the theme.
    
    </td>
    <td valign="top">
    
    -   Only alphanumeric characters and underscores are allowed.
    -   Must not start with `SAP`.
    -   Must not start with a number
    -   No special characters
    -   Must not contain dashes


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Title
    
    </td>
    <td valign="top">
    
    \(Optional\) The theme name that is displayed in the theme list on the start screen.
    
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
    
    \(Optional\) The name of the company that acts as the vendor of the theme.
    
    </td>
    <td valign="top">
    
    Must not start with `"SAP"`.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Fallback Theme ID
    
    </td>
    <td valign="top">
    
    \(Optional\) The ID of a theme which is used if the current theme isn't available in the UI framework.
    
    </td>
    <td valign="top">
    
    The ID of an existing theme
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Support RTL
    
    </td>
    <td valign="top">
    
    \(Optional\) Mark this checkbox if your theme also supports RTL languages.
    
    </td>
    <td valign="top">
    
     
    
    </td>
    </tr>
    </table>
    

You can also choose *Theme* \> *Save* to save a theme. If the theme wasn't saved before, you get the same dialog box as with *Save As...*

Your theme is saved as an HTML5 application in your SAP BTP subaccount \(same one as you used to open the UI theme designer\). This enables you to work on it again at a later date.

You can change the properties of the theme later via *Theme* \> *Properties*.

> ### Note:  
> In the backend there are stored two versions of the theme, the current active version and the latter version. There is no functionality to delete a specific version only. You could either delete the theme completely or if you want to remove undesired data \(e.g. if you accidently added confidential data to the theme\) you could change the theme accordingly and save and publish the theme twice.

