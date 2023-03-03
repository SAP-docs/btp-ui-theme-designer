<!-- loio905a31927b6d4a8c9c3056efbcbfe3e7 -->

# Setting up Permissions for a Custom Identity Provider

Customers with their own identity provider \(IDP\) can change the authorization and permissions settings in their SAP BTP subaccount so that they can use the UI theme designer tool.



<a name="loio905a31927b6d4a8c9c3056efbcbfe3e7__section_ydf_qbv_4bb"/>

## Context

To launch the UI theme designer, the user requires permission to create, read, and write HTML5 applications. The permission that they need is `AccountDeveloper`. However, if you use a custom IDP, the users are not listed in the *Members* section of the subaccount, and cannot, therefore, obtain the normal `AccountDeveloper` permission.

Therefore, you need to create an HTML5 application `AccountDeveloper` role, and give this permission to all users who will be using the UI theme designer.

Additionally, the GIT service requires that an e-mail address is passed for the user.

Let's get started.



<a name="loio905a31927b6d4a8c9c3056efbcbfe3e7__section_wbp_nhv_4bb"/>

## First set up the authorization settings

For more information, see [Setting Up Permissions for the UI Theme Designer](setting-up-permissions-for-the-ui-theme-designer-adbcaa6.md).



<a name="loio905a31927b6d4a8c9c3056efbcbfe3e7__section_jqy_v3l_ndb"/>

## Then set up the custom IDP

1.  Open SAP BTP cockpit for your subaccount.

2.  From the side panel, select *Security*, and then click *Trust*.

3.  Select the *Application Identity Provider* tab.

4.  Click your identity provider to open the detail settings.

5.  Make sure that the mapping for the email, first name, and last name attributes are maintained correctly.

    > ### Note:  
    > The correct principal attributes for SAP BTP are: `email` \(mandatory\), `firstname`, and `lastname`.
    > 
    > Please look up the corresponding names of your identity provider in the respective documentation.

6.  To test your settings, do the following:

    -   Copy the URL of the theme designer \(you can do this from the UI theme designer service page *Go to Service* link\).

    -   Close the browser completely or use a different browser/instance and open the theme designer from there.



**Result**:

The UI theme designer starts and you should see it running with your user name displayed in the right top corner of the screen.

