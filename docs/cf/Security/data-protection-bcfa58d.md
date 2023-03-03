<!-- loiobcfa58dfd8424d87bb5407f91ed06e4a -->

# Data Protection

Administrators must ensure that personal data is not saved when creating custom themes.



<a name="loiobcfa58dfd8424d87bb5407f91ed06e4a__section_jvb_22t_xcb"/>

## User-related data for custom themes on SAP BTP

-   No user-related data is stored

-   Changes on custom themes will be logged to the Audit Log of SAP BTP including the User ID




<a name="loiobcfa58dfd8424d87bb5407f91ed06e4a__section_cp3_plj_f2b"/>

## How to delete the user data?



User IDs will be deleted according to the retention policy of the Audit Log. For more information, see [Data Protection and Privacy](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7e513d31704a4a87831191e504ca850a.html).



<a name="loiobcfa58dfd8424d87bb5407f91ed06e4a__section_s32_tgt_xcb"/>

## Things you should know about personal data and other nonpublic data when creating custom themes

-   In the UI theme designer, you can upload arbitrary files into custom themes.

-   Custom themes must not contain any personal data or any other data that should not be exposed to the public - consider here also the metadata of the uploaded files.

-   Any authenticated user can access files of the custom themes.


