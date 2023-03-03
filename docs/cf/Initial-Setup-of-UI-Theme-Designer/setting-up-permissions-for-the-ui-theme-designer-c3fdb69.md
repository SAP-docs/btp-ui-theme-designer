<!-- loioc3fdb69e274f4d9bb33139763faa7a1f -->

# Setting up Permissions for the UI Theme Designer

To enable users to work with the UI theme designer, administrators must assign the UI theme designer permissions to the user's role.

Administrators need to add required roles to their role collections and assign them to the users.

The corresponding roles are:

-   `Editor (sap-theming)`: Create, edit, copy and delete custom themes \(but no change of Custom CSS possible\)

-   `CustomCssEditor (sap-theming)`: Create, edit, copy and delete custom themes \(including changes to Custom CSS\)
-   `Publisher (sap-theming)`: Publish custom themes \(but no editing\)
-   `Viewer (sap-theming)`: View custom themes in UI Theme Designer


> ### Note:  
> The role `CustomCssEditor` only disables the tab in the Theme Designer UI. There is no check against it in the backend.

> ### Note:  
> To use a custom theme with an application, no specific roles are required.



<a name="loioc3fdb69e274f4d9bb33139763faa7a1f__section_jzr_v3y_dgb"/>

## Procedure

This is how you assign the roles to role collections:

1.  Open the SAP BTP cockpit for your subaccount.

2.  Choose your global account.

3.  Go to *Subaccounts* in the left side panel.

4.  Select your subaccount on the Cloud Foundry environment.

5.  Go to *Security* in the left side panel and click *Role Collections*.

6.  Click the plus icon to add a new role collection to the subaccount.

7.  Enter a name and click *Create* to assign this role collection to your subaccount.

8.  From the list, choose your new role collection.

9.  Click *Edit* and search for the role *Editor* in the column *Role Name*. Choose the role and click *Add*.

10. Click *Save* to assign the role to your role collection.


