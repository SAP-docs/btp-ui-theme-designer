<!-- loiod3162e45aa9441389a7c7ce87c6de388 -->

# Creating a Role Collection

You can create your own role collections and add the theming roles to them.



## Prerequisites

-   You are a *manager* of your BTP subaccount.
-   Your SAP BTP global account administrator has entitled and subscribed the service that provides the roles you intend to add to the role collection. For more information, see [Entitling a Service](entitling-a-service-26c1006.md).

    > ### Note:  
    > For a PaaS setup, you need to create a service instance to access the provided roles. For more information, see [Creating a Service Instance](creating-a-service-instance-4b5273f.md).

-   You are in the SAP BTP cockpit. Make sure you are in the subaccount of the global account where you want to create role collections.



## Context

In the SAP BTP cockpit, role collections group individual roles. You can assign these collections to users. For more information, see [Building Roles and Role Collections for Applications](https://help.sap.com/docs/btp/sap-business-technology-platform/building-roles-and-role-collections-for-applications?version=Cloud).



## Procedure

1.  Create the Role Collection

    1.  In the navigation pane, expand the *Security* section.

    2.  Select *Role Collections*.

    3.  Choose *Create*.

    4.  Enter a *Name* \(for example, `Theming_Editor`\) and a *Description*.

    5.  Confirm with *Create*.


2.  Add Roles to the Collection

    1.  Select your new role collection from the list.

    2.  Choose *Edit*.

    3.  Under *Roles*, select the *Role Name* input field.

    4.  For *Application Identifier*, enter `sap-theming!b` and select the value that is auto-completed. This filters the list of roles to the ones provided by the UI theme designer service.

    5.  Select the roles you wish to include in your role collection. For available theming roles, see [Permissions](../Advanced-Information/permissions-c3fdb69.md).

    6.  Select *Add* to confirm.


3.  Select *Save* to confirm.




## Next Steps

Assign the role collection you created as described in [Assigning Role Collections to Users or User Groups](https://help.sap.com/docs/btp/sap-business-technology-platform/assigning-role-collections-to-users-or-user-groups?ai=true&version=Cloud) on SAP Business Technology Platform.

