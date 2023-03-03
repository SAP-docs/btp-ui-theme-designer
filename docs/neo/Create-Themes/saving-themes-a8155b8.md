<!-- loioa8155b8322e241fbb5c389a125091421 -->

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
    -   Must not start with ***SAP***.
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

    Must not start with ***"SAP"***.


    
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

    Must not start with ***"SAP"***.


    
    </td>
    </tr>
    </table>
    

Your theme is saved as an HTML5 application in your SAP BTP subaccount \(same one as you used to open the UI theme designer\). This enables you to work on it again at a later date.

> ### Note:  
> In the backend there is stored the complete history of the theme, including all versions which were saved in the past. There is no functionality to delete a specific version only. You could delete the theme completely if you want to delete the history \(e.g. if you accidently added confidential data to the theme\). If you delete a theme which should still be used, you should export the theme before the deletion, and immediately afterwards you should import, save and publish it. During the short time when the theme is not available, the end users could get a fallback to an SAP theme instead of the custom theme.

