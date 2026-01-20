<!-- copy4b944c563e82441ca016e8b8edb5658e -->

# Exporting Themes

Administrators use the export function to download themes as zip files from the UI theme designer to a local hard disk.



<a name="copy4b944c563e82441ca016e8b8edb5658e__steps_hzb_k1n_pl"/>

## Procedure

1.  Choose *Theme* \> *Export*.

2.  In the *Export* dialog box that appears, enter these values:


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
    
    The ID that applications can reference to invoke the theme.
    
    </td>
    <td valign="top">
    
    -   Use only alphanumeric characters.
    -   Don't start with `SAP`.
    -   Don't use numbers, special characters, or dashes


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Title
    
    </td>
    <td valign="top">
    
    The theme name that is displayed in the theme list on the welcome screen.
    
    </td>
    <td valign="top">
    
    Don't start with `"SAP"`.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Vendor \(Optional\)
    
    </td>
    <td valign="top">
    
    The name of the company that acts as the vendor of the theme.
    
    </td>
    <td valign="top">
    
    Must not start with `"SAP"`.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Support RTL \(Optional\)
    
    </td>
    <td valign="top">
    
    Right-to-left languages, such as Hebrew and Arabic, require different stylesheets and images than left-to-right \(LTR\) languages.
    
    </td>
    <td valign="top">
    
    Select this field to create stylesheets for both LTR and RTL languages.
    
    </td>
    </tr>
    </table>
    
3.  \(Optional\) Display the *Optional Settings \(for Experts\)* settings to select additional resources \(in addition to the source files\) necessary to rebuild the theme in another system or region host. The following table outlines a use case for each available option:


    <table>
    <tr>
    <th valign="top">

    Option
    
    </th>
    <th valign="top">

    Use-Case Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Source files only \(Default\)
    
    </td>
    <td valign="top">
    
    To transport a theme to another system, only the source files are strictly necessary to rebuild the theme on the target system.

    You should use this option only if you want to transport the source files and do not want to use the CSS files at runtime. If you want to use such an exported theme at runtime you have to rebuild the theme on the target system.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Source files + CSS resources
    
    </td>
    <td valign="top">
    
    Use this option if the theme is to be deployed directly to the runtime \(the required CSS files are also included\).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Source files + CSS resources + base theme resources
    
    </td>
    <td valign="top">
    
    Use this option to download the zip file from an SAP BTP subaccount to somewhere outside of SAP BTP.

    For example, to export to a non-SAP platform or to an SAP platform that doesn't support the theme repository.
    
    </td>
    </tr>
    </table>
    
    You may also deselect the UI technologies that you don't need in your custom theme.

    > ### Note:  
    > Unsure which option to select? We advise that you keep to the default values recommended by the system.

    > ### Note:  
    > All options support the import of the zip file into the UI theme designer running on SAP BTP. You can always import the transferred theme back again to your original system when you need to make changes to it.

4.  To export your theme, click *Export*.

    A *Zip* folder containing the theming files is created in your *Downloads* folder on your hard disk.


