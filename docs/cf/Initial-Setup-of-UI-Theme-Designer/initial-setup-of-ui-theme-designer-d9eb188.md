<!-- loiod9eb1888e2a6424a808f1b738bf5395f -->

# Initial Setup of UI Theme Designer

As an administrator, you can set up UI theme designer to create and edit themes and theme sets, applying your brand to your SAP Build Work Zone sites and applications.

The steps you need to take depend on your specific scenario.

You are likely already subscribed to a Software-as-a-Service \(SaaS\) application, such as SAP Build Work Zone. To get started: assign the necessary role collections to your designers and launch the theme designer.

Alternatively, if you are developing a custom application using a Platform-as-a-Service \(PaaS\) offering, or if you are using the UI theme designer for the SAP S/4HANA platform, you can integrate theming capabilities directly into your project. This approach lets you build your own SaaS application with integrated theming features, or to customize the appearance of your SAP S/4HANA environment.

> ### Note:  
> If you use SAP Build Work Zone, UI theme designer is already set up for you. Just assign the role collections **`Workzone_Admin`** and **`Workzone_Advanced_Theming`** \(for SAP Build Work Zone, advanced edition\) or **`Launchpad_Admin`** and **`Launchpad_Advanced_Theming`** \(for SAP Build Work Zone, standard edition\) to your designers. They can start theming immediately.



## Procedure

![Administrator flowchart for SAP Build Work Zone setup including
							decisions for SaaS or PaaS and role assignments.](images/Image_Map_Initial_Setup_569a37f.png)

To setup UI theme designer, follow these high-level steps:



### To setup UI theme designer for SaaS access:

1.  *Do you already use SAP Build Work Zone?* If not, you need to entitle and subscribe SAP Build Work Zone first as described in [Entitling a Service](entitling-a-service-26c1006.md).
2.  Assign the `Workzone_Admin/Workzone_Advanced_Theming` or `Launchpad_Admin/Launchpad_Advanced_Theming` role collections to your users as described in [SAP Business Technology Platform: Assigning Role Collections to Users or User Groups](https://help.sap.com/docs/btp/sap-business-technology-platform/assigning-role-collections-to-users-or-user-groups?ai=true&version=Cloud).



### To setup UI theme designer for PaaS access:

1. Entitle *UI Theme Designer Service* as described in [Entitling a Service](entitling-a-service-26c1006.md).

2. Create a service instance of the *UI Theme Designer Service* as described in [Creating a Service Instance](creating-a-service-instance-4b5273f.md).

*Do you only need API access, for example, to set up a destination or a communication arrangement?*

**To setup PaaS for API access:** 

3. Create a service key for the service instance you created as described in [SAP Business Technology Platform: Creating Service Keys](https://help.sap.com/docs/btp/sap-business-technology-platform/creating-service-keys?ai=true&locale=en-US).

**To setup PaaS for Application Router access:**

3. Bind the service instance you created as well as a service instance of the HTML5 Application Repository Service to your Application Router as described in [Integrating with Application Router](integrating-with-application-router-3f26353.md).

4. Create the necessary role collections as described in [Creating a Role Collection](creating-a-role-collection-d3162e4.md).

5. Assign the role collections you just created as described in [SAP Business Technology Platform: Assigning Role Collections to Users or User Groups](https://help.sap.com/docs/btp/sap-business-technology-platform/assigning-role-collections-to-users-or-user-groups?ai=true&version=Cloud).



> ### Note:  
> The UI theme designer service can be consumed by applications running in the Kyma environment. For details read [SAP Business Technology Platform: Using SAP BTP Services in the Kyma Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/using-sap-btp-services-in-kyma-environment).



## Next Steps

Start using UI theme designer as described in [Create and Edit Themes and Theme Sets](../Create-and-Edit-Themes-and-Theme-Sets/create-and-edit-themes-and-theme-sets-0d2d662.md). You can also use the created service key in your destination or communication arrangement as described in [Integration Scenarios](../Integration-Scenarios/integration-scenarios-f04b3a0.md).

