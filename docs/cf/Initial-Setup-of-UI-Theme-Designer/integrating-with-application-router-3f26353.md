<!-- loio3f26353066f44afdbaf568913ea28b70 -->

# Integrating with Application Router

You can integrate UI theme designer with your own Application Router by binding service instances of UI Theme Designer and HTML5 Application Repository.

Endpoints of the UI Theme Designer service are automatically available under `https://<your-approuter-host>/comsapuitheming.<endpoint>/`. For example, use `/comsapuitheming.themedesigner`/ for the theme designer web app.

> ### Note:  
> You don't need to configure manual routing. The UI Theme Designer service integrates automatically with the Application Router. You don't need to make any changes to the `xs-app.json` file.



## Prerequisites

-   You have created a service instance of the *HTML5 Application Repository* service in the *app-runtime* plan.
-   You have created a service instance of the *UI Theme Designer* service, as described in [Creating a Service Instance](creating-a-service-instance-4b5273f.md).
-   You use an Application Router, such as the `@sap/approuter` npm module. For more information, see [Application Router](https://help.sap.com/docs/btp/sap-business-technology-platform/application-router?version=Cloud) on SAP Business Technology Platform.



## Context

UI Theme Designer service provides its central routing information to the HTML5 Application Repository. When you bind your Application Router to a service instance of UI theme designer, it accesses this central routing information. This process automatically exposes the theming service endpoints. You don't need to configure routing manually, as you would in an `xs-app.json` file.

This automatic routing works for both standard and multi-tenant \(SaaS\) applications. As long as the required service bindings are present, the theming integration is enabled by default.



## Procedure

After you bind your Application Router to the service instances of UI theme designer and HTML5 Application Repository, you can access the theming service directly from your Application Router's URL. Replace `<your-approuter-host>` with the full hostname of your Application Router.



### To verify the connection with a health check:

Open `https://<your-approuter-host>/comsapuitheming.runtime/health/ping`.



### To launch the theme designer:

Open `https://<your-approuter-host>/comsapuitheming.themedesigner/`. For more information, see [Launching the Theme Designer Web App](../Create-and-Edit-Themes-and-Theme-Sets/launching-the-theme-designer-web-app-8f49dce.md).



## Related Information

SAP Business Technology Platform: [Application Router](https://help.sap.com/docs/btp/sap-business-technology-platform/application-router?version=Cloud)

npm: [@sap/approuter](https://www.npmjs.com/package/@sap/approuter)

