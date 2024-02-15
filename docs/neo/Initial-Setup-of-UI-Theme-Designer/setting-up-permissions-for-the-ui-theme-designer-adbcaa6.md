<!-- loioadbcaa6fad6a4b81bf94b0ae3c54ec3c -->

# Setting Up Permissions for the UI Theme Designer

To enable users to work with the UI theme designer, administrators must assign the UI theme designer permissions to the user's role.

The permission required to use the UI theme designer is `UIThemeDesignerPermission`.

When you as administrator add a role and assign it to this permission, all users assigned to this role will be able to access the UI theme designer.

This is how you assign the permission:



1.  Open the SAP BTP cockpit for your subaccount.

2.  Go to *Services* and click the *UI Theme Designer* tile.

3.  Enable the *UI Theme Designer* service if it is not already enabled.

4.  On the UI Theme Designer service page, click *Configure Service*.

5.  Click *Roles* in the left side panel.

6.  Click *New Role* and add a new role with the name `AccountDeveloper`.

7.  Assign users to the new role.

8.  Click *Destinations & Permissions*, and assign the new `AccountDeveloper` role to the `UIThemeDesignerPermission` application permission.

    > ### Note:  
    > You can also use another role to prevent the start of the tool, but the back-end functionality, such as loading and saving themes, is always bound to the `AccountDeveloper` permission.

9.  Select the checkbox *Always Apply Permission* to enforce the permission check when the UI theme designer is started from the SAP Fiori launchpad.

    > ### Note:  
    > This permission applies only to the tool; the back-end permission is always enforced.

10. Now go back to the cockpit overview page to create a group and assign the role to the group.

11. Click *Security* \> *Authorizations*.

12. Click *New Group* and enter the name of the group for the UI theme designer users

    For example, `ThemeDesignerDev`.

13. Click *Assign* to assign the `AccountDeveloper` role to the group.


