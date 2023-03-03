<!-- loio8483ca25049f4332a9d0d66b6d4ac080 -->

# Data Protection

Administrators must ensure that personal data is not saved when creating custom themes.



<a name="loio8483ca25049f4332a9d0d66b6d4ac080__section_jvb_22t_xcb"/>

## User-related data for custom themes on SAP BTP

By saving a theme using UI theme designer for an SAP BTP subaccount or uploading a theme to SAP BTP by using the HTML5 Application upload in the cockpit, the following user-related data is created:

-   Full user name

-   E-mail address of the user who created or modified the custom theme in the system

-   Time and date


Once the data is saved, it becomes visible in the Git repository browser of the Git Service. To see the data, do the following:

1.  Log on to SAP BTP*Cockpit*

2.  Open the relevant subaccount.

3.  Click *Git Repositories*.

4.  Click the name of the relevant Git Repository.


Result: The user data is visible for the tags, changes, and files.

> ### Note:  
> The user data is not automatically deleted when the user's subaccount is removed.



<a name="loio8483ca25049f4332a9d0d66b6d4ac080__section_cp3_plj_f2b"/>

## How to delete the user data?



To delete the user data, do the following for each of the relevant themes:

1.  Open *UI theme designer* from the respective subaccount.

2.  Select the custom theme.

3.  Click *Export*.

4.  In the *Export* dialog, click *Export*.

5.  Click *Delete*.

6.  Confirm deletion.

7.  Click *Import*.

8.  Click the *\+* icon and select the previously exported theme.

9.  *Save* or *Save & Publish* from the edit page as required.


> ### Note:  
> Please be aware that the theme will be temporarily unavailable during this procedure. The change history will also be deleted.

For more information, see: [Git Service](https://help.sap.com/viewer/01ef8239651c40b5806686d4ec6d8944/Cloud/en-US/b8cd659181f549c9ba11af7cf51f5806.html).



<a name="loio8483ca25049f4332a9d0d66b6d4ac080__section_s32_tgt_xcb"/>

## Things you should know about personal data and other nonpublic data when creating custom themes

-   In the UI theme designer, you can upload arbitrary files into custom themes.

-   Custom themes must not contain any personal data or any other data that should not be exposed to the public - consider here also the metadata of the uploaded files.


> ### Note:  
> Themes published on SAP BTP can be accessed without any authentication checks. Anyone who knows the theme URL can access the theme content.

