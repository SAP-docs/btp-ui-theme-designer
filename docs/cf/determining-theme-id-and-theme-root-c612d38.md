<!-- loioc612d38c739c4c0b87b7608436d0ce83 -->

# Determining Theme ID and Theme Root

You can use the endpoints of the UI Theme Designer service to validate a desired theme ID and determine its optimized theme root. This is usually done by SAP Build Work Zone. You only have to do it if you launch themeable applications outside the SAP Build Work Zone shell.



## Prerequisites

-   You know your Application Router URL. See [Integrating with Application Router](Initial-Setup-of-UI-Theme-Designer/integrating-with-application-router-3f26353.md) and [Launching the Theme Designer Web App](Create-and-Edit-Themes-and-Theme-Sets/launching-the-theme-designer-web-app-8f49dce.md) to find your Application Router URL.
-   You are authenticated against [SAP Business Technology Platform: SAP Authorization and Trust Management Service](https://help.sap.com/docs/btp/sap-business-technology-platform/sap-authorization-and-trust-management-service-in-cloud-foundry-environment?version=Cloud), with no specific roles necessary.

> ### Note:  
> You may have configured your Application Router to expose the UI Theme Designer service endpoints at dedicated routes in addition to `/comsapuitheming.repository` and `/comsapuitheming.runtime`. Then use the routes you defined instead. For more information, see [Integrating with Application Router](Initial-Setup-of-UI-Theme-Designer/integrating-with-application-router-3f26353.md) for details.



## Procedure



### To get information about a theme or theme set

The runtime endpoint provides information of specific themes or theme sets via the `/themeinfo/v1` API. You need this to retrieve an optimized theme root for the theme or theme set you want to apply. The optimized theme root contains all information that makes a version of a theme or theme set unique. Responses of the optimized theme root can be cached infinitely, improving performance for subsequent requests.

Request `/comsapuitheming.runtime/themeinfo/v1/<theme-id>` from your Application Router URL. The response is a JSON that has the following TypeScript type:

```
type ThemeInfo = {
  id: string,
  url: string,
  version: string
} & ({
  type: "STANDARD",
  extends: string
} | {
  type: "SET",
  set: {
    themes: {
      id: string,
      colorScheme: "LIGHT" | "DARK",
      contrast: "LOW" | "HIGH",
      default?: boolean
    }[]
  }
});
```

The information you’re most likely after is the `url`, which is the optimized theme root to be used when requesting theme resources from the UI Theme Designer service. Combine `id` and `url` for the `sap-theme` URL parameter for applications as `sap-theme=<id>@/comsapuitheming.runtime<url>`.



### To list available themes and theme sets

The repository endpoint provides a list of the themes and theme sets available for a specific version of a specific UI technology. You need this if you want to be certain that a specific theme or theme set exists for the UI technology and version you selected. It lists available themes for a specific version of a specific UI technology.

To retrieve this list, request `/comsapuitheming.repository/themelist/v1/~v=<ui-technology>:<version-of-that-ui-technology>` from your Application Router URL. If you want the theme list to include theme sets, you have to explicitly add `filter-types=STANDARD,SET` as a query parameter. For example, if your Application Router URL was `https://my-application-router.eu10.hana.ondemand.com`, and you wanted to list all themes and theme sets available for SAPUI5 1.136.14, you would request `https://my-application-router.eu10.hana.ondemand.com/comsapuitheming.repository/themelist/v1/~v=UI5:1.136.14?filter-types=STANDARD,SET`.

The response is a JSON that has the following TypeScript type:

```
type ThemeList = ({
  id: string,
  label: string,
  vendor: string,
  avatarRuntimeUrl: string,
  deprecated: boolean,
  creationTime: string,
  activationTime: string,
  tags?: string[]
} & ({
  type: "STANDARD",
  textDirections: string,
  extends?: string
} | {
  type: "SET",
  set: {
    themes: {
      id: string,
      colorScheme: "LIGHT" | "DARK",
      contrast: "LOW" | "HIGH",
      default?: boolean
    }[];
  }
}))[];
```



### To list available UI technologies and their versions

The repository endpoint provides a list of the available UI technologies. You need this if you want to be certain that a specific version of a specific UI technology exists before carrying on. Usually, all versions of *Base* and *UR* that have been released in the last 365 days, as well as all versions of UI5 in cloud provisioning are available. For more information about SAPUI5 versions, see [Available SAPUI5 Versions on SAP Business Technology Platform](https://ui5.sap.com/versionoverview.html). But to double-check, you can access `/sap-themes/.theme-repository-versions.json` of the repository endpoint.

To retrieve this list, request `/comsapuitheming.repository/sap-themes/.theme-repository-versions.json` from your Application Router URL.

The response is a JSON that has the following TypeScript type:

```
type ThemeRepositoryVersions = {
  mVersions: {
    Base: string[];
    UI5: string[];
    UR: string[];
  }
}
```



## Example

The following example shows how to start an application with the right `sap-theme` URL parameter for a given Application Router URL, theme and UI technology with version.

```
const APPLICATION_ROUTER_URL = 'https://example.com';
const THEME_ID = 'my_theme';
const UI_TECHNOLOGY = 'UI5';
const UI_TECHNOLOGY_VERSION = '1.136.14';
const APPLICATION = '/my-application'

// 1. check if UI technology is available in requested version
// (you can omit this step if your code is resilient against unavailable UI technology versions)
const themeRepositoryVersionsRequest = await fetch(`${APPLICATION_ROUTER_URL}/comsapuitheming.repository/sap-themes/.theme-repository-versions.json`);
if (!themeRepositoryVersionsRequest.ok) throw new Error('Error fetching .theme-repository-versions.json.');

const {mVersions} = await themeRepositoryVersionsRequest.json();
if (!(UI_TECHNOLOGY in mVersions)) throw new Error(`UI technology ${UI_TECHNOLOGY} not available.`);
if (!(UI_TECHNOLOGY_VERSION in mVersions[UI_TECHNOLOGY]) throw new Error(`Version ${UI_TECHNOLOGY_VERSION} of ${UI_TECHNOLOGY} not available.`);

// 2. check if the theme is available for the requested UI technology version
// (you can omit this step if your code is resilient against unavailable themes)
const themeListRequest = await fetch(`${APPLICATION_ROUTER_URL}/comsapuitheming.repository/themelist/v1/~v=${UI_TECHNOLOGY}:${UI_TECHNOLOGY_VERSION}?filter-types=STANDARD,SET`);
if (!themeListRequest.ok) throw new Error('Error fetching theme list.');

const themeList = await themeListRequest.json();
if (!themeList.some(({id}) => id === THEME_ID)) throw new Error(`${THEME_ID} not available for UI technology ${UI_TECHNOLOGY} in version ${UI_TECHNOLOGY_VERSION}`);

// 3. retrieve the correct theme root
const themeInfoRequest = await fetch(`${APPLICATION_ROUTER_URL}/comsapuitheming.runtime/themeinfo/v1/${THEME_ID}`);
if (!themeInfoRequest.ok) throw new Error(`Error fetching theme info for theme ${THEME_ID}.`);

const {url} = await themeInfoRequest.json();

// 4. start the application with the right sap-theme URL parameter
location.href = `${APPLICATION_ROUTER_URL}${APPLICATION}?sap-theme=${THEME_ID}@/comsapuitheming.runtime${url}`;
```



## Result

With the `url` from `/themeinfo/v1`, you know the optimized theme root for your desired theme. Browsers can cache theme resources from this optimized theme root indefinitely. For this reason you need to determine the optimized theme root regularly. For example, at the start of a user session. Otherwise, users won’t see updates of the theme they use.



## Next Steps

Launch applications with the `sap-theme` URL parameter created from the validated theme ID and the optimized theme root – `&sap-theme=${themeId}@${themeRoot}`. To learn what steps applications need to take to support this, see [Supporting the sap-theme URL Parameter](supporting-the-sap-theme-url-parameter-ab10b7d.md).

