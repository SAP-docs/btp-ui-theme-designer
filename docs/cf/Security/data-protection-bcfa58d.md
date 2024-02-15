<!-- loiobcfa58dfd8424d87bb5407f91ed06e4a -->

# Data Protection

Administrators must ensure that no personal data is saved when creating custom themes.



<a name="loiobcfa58dfd8424d87bb5407f91ed06e4a__section_jvb_22t_xcb"/>

## User-Related Data for Custom Themes on SAP BTP

-   No user-related data is stored

-   Changes on custom themes will be logged to the Audit Log of SAP BTP including the User ID




<a name="loiobcfa58dfd8424d87bb5407f91ed06e4a__section_cp3_plj_f2b"/>

## How to Delete the User Data on SAP BTP



User IDs will be deleted according to the retention policy of the Audit Log. For more information, see [Data Protection and Privacy](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7e513d31704a4a87831191e504ca850a.html).



<a name="loiobcfa58dfd8424d87bb5407f91ed06e4a__section_w2k_st5_21c"/>

## User-Related Data on the UI

User preferences such as the selected preview pages are saved in the local browser storage.



### How to Delete User Data on the UI

To delete the user preferences in the local browser storage, open the user menu and choose *Clear Preferences*.



<a name="loiobcfa58dfd8424d87bb5407f91ed06e4a__section_s32_tgt_xcb"/>

## Personal Data and Other Non-Public Data When Creating Custom Themes

Here are some things you need to consider when you create custom themes:

-   In UI theme designer, you can upload arbitrary files into custom themes.

-   Be careful about the information contained in these files. Custom themes must not contain any personal data or any other data that should not be exposed to the public - consider also the metadata of the uploaded files here.

-   Any authenticated user can access files of the custom themes.


