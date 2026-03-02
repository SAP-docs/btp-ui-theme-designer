<!-- loio26c100668d0047af9db9141ab1d92571 -->

# Entitling a Service

Entitling is the process of assigning permissions and quotas for a specific service or application from your global account to subaccounts. After you entitle a service, users can see it in the subaccount's service marketplace and create instances of it.



<a name="loio26c100668d0047af9db9141ab1d92571__prereq_x1w_ztb_1lb"/>

## Prerequisites

-   You are an administrator of your SAP BTP global account.
-   You are in the SAP BTP Cockpit, within the subaccount of the global account where you want to assign service entitlements.



## Context

For more information, see [Managing Entitlements and Quotas Using the Cockpit](https://help.sap.com/docs/btp/sap-business-technology-platform/managing-entitlements-and-quotas-using-cockpit?version=Cloud) in SAP Business Technology Platform.



## Procedure

1.  In the navigation pane, choose *Entitlements*.

2.  Select *Edit* to switch to edit mode.

3.  Choose *Add Service Plans*.

4.  In the dialog:

    1.  Search for the desired service. Usually *SAP Build Work Zone* for a SaaS setup, or *UI Theme Designer*for a PaaS setup.

    2.  Select the service.

    3.  Select the service plan you want to assign. For a PaaS setup, select *standard* for *UI Theme Designer*.

    4.  Confirm with *Add \[x\] Service Plans*.


5.  Enter the desired quota.

6.  Confirm with *Save*.




## Results

The service is entitled for your subaccount.

