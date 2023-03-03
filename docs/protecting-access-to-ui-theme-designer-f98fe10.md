<!-- copyf98fe1066268405e8c30af68abe6a22f -->

# Protecting Access to UI Theme Designer

Add a role and assign it to the UI theme designer permission to restrict access to UI theme designer.



## Prerequisites

You are subscribed to the UI theme designer application.

See .



## Context

In the SAP BTP cockpit, you can create custom roles and assign them to the defined permissions. If a user accesses an application path that starts with a path defined for a permission, the system checks whether the current user is a member of the assigned role. If no role is assigned to a defined permission, all authenticated users have access to the corresponding application path.

The corresponding permissions are:

-   `UIThemeDesignerPermission` - enables access to the UI theme designer tool.

-   `AccountDeveloper` - enables read/write access to the themes.

-   `SupportUser` - enables read access to the themes.


