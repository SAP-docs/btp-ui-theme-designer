<!-- loiocc6d67f1f0ac4fb1b402983b2bbfd670 -->

# Service Offboarding

How to disable the UI theme designer service.

To disable the service, you must complete the following tasks:

-   Disable the UI Theme Designer application

-   Delete custom themes




<a name="loiocc6d67f1f0ac4fb1b402983b2bbfd670__section_cw1_bcc_1lb"/>

## Disable the UI Theme Designer Application

If the *Disable* function of the *UI Theme Designer* service page is not available, you can disable the application manually:

1.  Open SAP BTP Cockpit.

2.  Navigate to your Neo subaccount.

3.  Go to *Applications* \> *Subscriptions*.

4.  Choose the *Unsubscribe* button for *UI Theme Designer*.


> ### Note:  
> This removes the access to the *UI Theme Designer* application from your account. It will not remove any custom themes in your account.



<a name="loiocc6d67f1f0ac4fb1b402983b2bbfd670__section_pnm_bcc_1lb"/>

## Delete Custom Themes

> ### Note:  
> Before you delete a theme, ensure that it is not currently being used by an application as it may make the application unusable.

You can delete custom themes using the following options:

-   Choose the *Delete* button in the *UI Theme Designer* application \(custom themes are stored as HTML5 applications in the UI Theme Designer\).
-   Delete the themes using the SAP BTP Cockpit:
    1.  Open SAP BTP Cockpit.

    2.  Navigate to your Neo subaccount.

    3.  Go to *Applications* \> *HTML5 Applications*.

    4.  Select the theme, and choose the *Delete* button.





<a name="loiocc6d67f1f0ac4fb1b402983b2bbfd670__section_h5x_bcc_1lb"/>

## Note on The Theming Service

The Theming Service is an integral part of the SAP BTP and you cannot deactivate it. Additionally, the Theming Service can only be used with custom themes.

