<!-- loio4b5273f3002347aca282c3abe426a7e5 -->

# Creating a Service Instance

You can create service instances of the UI theme designer service, with the standard plan. These allow secure access to the API. Integrate them with your Application Router, or use them for direct API access, such as in a communication arrangement.



## Prerequisites

-   You are a *Space Developer* of the Cloud Foundry space of your SAP BTP subaccount.
-   Your SAP BTP global account administrator has entitled UI theme designer as described in [Entitling a Service](entitling-a-service-26c1006.md).
-   You are in the SAP BTP cockpit, in the Cloud Foundry space where you want to create the service instance.



## Context

For more information, see [Creating Service Instances](https://help.sap.com/docs/btp/sap-business-technology-platform/creating-service-instances?ai=true&locale=en-US) in SAP Business Technology Platform.



## Procedure

1.  From *Services*, select *Service Marketplace*.

2.  Select the *UI Theme Designer* tile.

3.  Choose *Create*.

4.  In the instance configuration dialog:

    1.  **Optional:** Enter *UI Theme Designer* as a service. This option is usually pre-selected.

    2.  **Optional:** Select the *standard* plan. This option is usually pre-selected.

    3.  Enter a `cli`-friendly *Instance Name*, such as `theming-service`.

    4.  Confirm by selecting *Create*. You don't need to configure the service instance *Parameters* \(by choosing *Next*\).


    > ### Note:  
    > If you manage your SAP BTP subaccounts, you can also create a service instance from the subaccount overview in the SAP BTP cockpit.




## Next Steps

Integrate these service instances with your Application Router as described in [Integrating with Application Router](integrating-with-application-router-3f26353.md). You can also create service keys as described in [Creating Service Keys](https://help.sap.com/docs/btp/sap-business-technology-platform/creating-service-keys?version=Cloud) in SAP Business Technology Platform. Use these keys for API access, such as in communication arrangements as described in [Integration Scenarios](../Integration-Scenarios/integration-scenarios-f04b3a0.md).

