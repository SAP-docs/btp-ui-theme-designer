<!-- loio80f09047d6714daaa2cff78c20cb6fef -->

# Self-Hosting Themes for Use Without the UI Theme Designer Service

You can self-host themes and theme sets for use without the UI Theme Designer service. This can be necessary if your users not have access to the UI Theme Designer service, for example, because your applications run in an environment without the UI Theme Designer service, or because you want to provide unauthenticated access to your themes and theme sets.

To self-host themes, export your theme or theme set with *Source Files + CSS Resources + Base Theme Resources* selected. Also select the UI technologies your applications need, as described in [Exporting Themes and Theme Sets](Create-and-Edit-Themes-and-Theme-Sets/exporting-themes-and-theme-sets-26e5140.md). Unzip the exported theme or theme set. Host the unzipped content in your preferred location. Use the root of the hosted content as the Theme Root when you pass the `sap-theme` URL parameter to your applications.

> ### Note:  
> -   When you export a theme or theme set, you export it for the specific UI technology versions available at that time. If your applications use UI technologies such as SAPUI5 and you update their versions, export the theme or theme set again for the updated versions.
> -   An exported theme set doesn't include themes that are appearances of that theme set. To self-host a theme set: also self-host the themes that are appearances of that theme set.



## Prerequisites

You have exported your theme or theme set with *Source Files + CSS Resources + Base Theme Resources* as described in [Exporting Themes and Theme Sets](Create-and-Edit-Themes-and-Theme-Sets/exporting-themes-and-theme-sets-26e5140.md).



## Procedure

1.  Unzip the exported theme or theme set. This results in a directory that has a structure as described in [Overview of SAP Theming Content](About-Themes/overview-of-sap-theming-content-91ebfe2.md).
2.  Host the unzipped theme or theme set on your own infrastructure.



## Example

This example shows how to serve `my_theme` when the following conditions are met:

-   You have exported the theme with *Source Files + CSS Resources + Base Theme Resources* and *UR and UI5* selected as `my_theme.zip`;
-   It is on your own infrastructure – from a simple `python -m http.server`, to `nginx`, or HTML5 Repository ;
-   Use it in the `sap-theme` URL parameter of your application at `https://example.com/my-application`. Trust the `http://localhost:8000` theme root as described in [Supporting the sap-theme URL Parameter](supporting-the-sap-theme-url-parameter-ab10b7d.md).

```
# 1: unzip the exported theme to my_theme
unzip -qd my_theme my_theme.zip
# 2: (optional) inspect the exported theme
tree --noreport -L 1 my_theme
# => my_theme
# => ├── Base
# => ├── UI5
# => ├── UR 
# => ├── exportThemesInfo.json 
# => └── neo-app.json
# 3: serve my_theme via http(s) (could be any http server)
python -m http.server -d my_theme
# => Serving HTTP on :: port 8000 (http://[::]:8000/) ...
# 4: start your application
open https://example.com/my-application?sap-theme=my_theme@http://localhost:8000
```



## Results

You’ve made your theme or theme set available on your own infrastructure, without any connection to the UI Theme Designer service.



## Next Steps

Go ahead to use your theme or theme set from your own infrastructure for applications, with your own URL as the Theme Root.

Remember to update the theme or theme set when your applications’ UI technology versions change.

