<!-- loio25896d06a71a4bc190833c5947f6fdcd -->

# Integrating in Standalone SAPUI5 Applications

You can apply themes in standalone SAPUI5 applications.

For that, you specify the right *Theme ID* and *Theme Root*, and configure SAPUI5 to pass its version to the UI theme designer service. If you pass the theme root via bootstrap attributes or global configuration, you have to append `/UI5` to the theme root.



## Prerequisites

-   You have published a theme as described in [Publishing Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/publishing-themes-and-theme-sets-f4889a4.md).

-   You know the *Theme ID* and *Theme Root* you want to apply.




## Procedure

1.  Add the origin of the theme root to SAPUI5 *Theme Origin Allowlist*. For example:

    ```
    
      <meta name="sap-allowed-theme-origins"
         content="https://example.com">
    
    ```

2.  Start the application with *Theme ID*, *Theme Root* and the `versionedLibCss=true` configuration:
    -   **Via URL parameters:** append the URL parameters `sap-theme=${themeId}@${themeRoot}` and `sap-ui-versionedLibCss=true` to the application URL. For example:

        ```
        /your-application?sap-theme=your_theme@https://example.com&sap-ui-versionedLibCss=true
        ```

    -   **Via bootstrap attributes:** add `data-sap-ui-theme="${themeId}" data-sap-ui-theme-roots='{"${themeId}": "${themeRoot}/UI5"}' data-sap-ui-versionedLibCss="true"` to the bootstrap configuration of your application. For example:

        ```
        <script id="sap-ui-bootstrap"
                     src="resources/sap-ui-core.js"   
                     data-sap-ui-theme="your_theme"  
                     data-sap-ui-theme-roots='{"your_theme": "https://example.com/UI5"}'
                     data-sap-ui-versionedLibCss="true"></script>
        ```

    -   **Via global configuration:** add `{theme: `${themeId}`, "theme-roots": {[`${themeId}`]: `${themeRoot}/UI5`}, versionedlibcss: true}` to `globalThis["sap-ui-config"]` before starting SAPUI5. For example:

        ```
        globalThis["sap-ui-config"] = {   
                    ...globalThis["sap-ui-config"],   
                    theme: "your_theme",   
                    "theme-roots": {...globalThis["sap-ui-config"]["theme-roots"], your_theme: "https://example.com/UI5"}, 
                    versionedlibcss: true 
                  }
        ```



You can’t directly apply theme sets to standalone SAPUI5 applications. Instead, your application has to resolve the themes in the theme set to the theme that would actually apply based on the users system settings, and apply that. For details on the structure of a theme set, see [What is a Theme Set?](../About-Themes/what-is-a-theme-set-53de0b1.md).

For more information, see [SAPUI5 Demo Kit: Setting Themes](https://ui5.sap.com/#/topic/e9fc648661d84ed89360bbec3ae02611).

