<!-- loio3f26353066f44afdbaf568913ea28b70 -->

# Setting up Entitlements, a Service Instance, and Binding

In the SAP BTP cockpit, perform the following steps to set up entitlements, a service instance, and binding.



<a name="loio3f26353066f44afdbaf568913ea28b70__steps_esm_mbq_4nb"/>

## Procedure

1.  In your subaccount, go to *Entitlements* to add an entitlement for the UI Theme Designer service. To do so, click *Configure Entitlements* \> *Add Service Plans* and add the UI Theme Designer with plan *standard* to the relevant subaccount. Then click *Save*.

2.  Click on *Service Marketplace*, and click the UI Theme Designer tile.

3.  In the UI Theme Designer screen, click on *Create* to create a new instance for the UI Theme Designer service. Select the *standard* plan and choose an *Instance Name* \(e.g. "\[appName\]-theming", replace the \[appName\] with the name of you application\). Then click *Create*.

4.  Bind the UI Theme Designer instance to the app router module of your business application.

    1.  In SAP Business Application Studio, open the `mta.yaml` file of your project. In the *Resource* section, add a new resource for the UI Theme Designer. Replace the \[appName\] in the example with the name of your application.

        ```
        # UI Theme Designer
         
          - name: [appName]-theming
         
            parameters:
         
              service: theming
         
              service-plan: standard
         
            type: org.cloudfoundry.managed-service
        ```

    2.  In the *requires* section of the app router module, require the UI Theme Designer resource that you added in step a \(use the name of your application instead of \[appName\]\).

        ```
        requires:
         
              - name: [appName]-theming
        ```


5.  You must rebuild your project to make the binding effective.


