<!-- loioc3fdb69e274f4d9bb33139763faa7a1f -->

# Permissions

UI theme designer defines different permissions, that administrators can set up access for editing themes.

> ### Note:  
> Users who only use a custom theme at runtime, such as in SAP Build Work Zone sites and applications, do not need any specific permissions.



## Context

The SAP BTP permission model follows a clear hierarchy:

1.  **Scope:** gives permission to perform a single action at a technical level. Scopes are specific to Cloud Foundry. Services define scopes and check them at the API level to authorize requests. Administrators can optionally configure scopes when they create service instances.
2.  **Role:** groups scopes that logically belong to job functions. Services expose these scopes in the SAP BTP subaccount.
3.  **Role Collection:** groups roles, often from different services, into packages that are assigned to end users.

    In summary, users receive role collections. These collections contain roles, and each role consists of scopes.




## Scopes

UI theme designer defines these scopes:

-   **Read:** View custom theme data.
-   **Write:** Create or modify custom themes.
-   **WriteCustomCss**: Edit the custom CSS within a theme.
-   **Publish:** Make a custom theme available for public use.
-   **ReadThemeList:** Read the list of available themes.



## Roles

UI theme designer exposes these roles:

-   **Viewer:** Allows read-only access to view custom themes in the theme designer. *This role includes only the **Read** scope.*
-   <code><b>Editor:</b></code> Allows users to create, edit, copy, and delete custom themes. This role does not grant permission to modify custom CSS. *This role includes the **Read** and **Write** scopes.*
-   **CustomCssEditor:** Includes all **Editor** permissions and additionally allows users to add and modify custom CSS via the *Custom CSS* tab in the theme designer. *This role includes the <code><b>Read</b></code>, <code><b>Write</b></code> and <code><b>WriteCustomCss</b></code> scopes.*

    > ### Note:  
    > -   The <code><b>CustomCssEditor</b></code> role only enables access to the tab in the theme designer. No back end validation of the CSS code is performed.
    > -   Working with Custom CSS has risks. You might want to withhold this role. See [Adding Custom CSS](../Create-and-Edit-Themes-and-Theme-Sets/Customizing-Themes-in-the-Editor/adding-custom-css-895a4b0.md) for details.


-   **Publisher:** Allows users to review changes and publish custom themes, making them available for consumption. This role does not include editing permissions. Separating the Editor and Publisher roles enables a four-eyes principle \(separation of duties\) for quality assurance. See [Publishing Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/publishing-themes-and-theme-sets-f4889a4.md) for details. *This role includes the <code><b>Read</b></code> and <code><b>Publish</b></code> scopes.*



## Role Collections

UI Theme Designer does not provide role collections.

You can include the theming roles in your own role collections as described in [Creating a Role Collection](../Initial-Setup-of-UI-Theme-Designer/creating-a-role-collection-d3162e4.md).

SAP Build Work Zone provides role collections that contain the these roles:

-   <code><b>Workzone_Admin</b></code> and <code><b>Workzone_Advanced_Theming</b></code> for SAP Build Work Zone, advanced edition
-   <code><b>Launchpad_Admin</b></code> and <code><b>Launchpad_Advanced_Theming</b></code> for SAP Build Work Zone, standard edition



## Related Information

[SAP Business Technology Platform: Security Administration: Managing Authentication and Authorization](https://help.sap.com/docs/btp/sap-business-technology-platform/security-administration-managing-authentication-and-authorization?version=Cloud)

