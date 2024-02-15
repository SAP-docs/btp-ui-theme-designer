<!-- loioa681c0de71ce48bb8cc9735abcdc29b0 -->

# Initial Setup of UI Theme Designer

To use the UI theme designer, administrators must implement some initial configurations.



## SAP Notes

Implement SAP note [1852401](https://me.sap.com/notes/1852401).



## ICF Nodes

Activate the following Internet Communication Framework \(ICF\) service nodes:

-   `/sap/public/bc/themes`
-   `/sap/bc/theming`

To perform this step, launch IMG activity *Activate ICF service for UI theme designer*. You access the IMG activity in the SAP Customizing Implementation Guide by choosing *SAP NetWeaver* \> *UI Technologies* \> *UI Theme Designer* \> *Maintain Custom Themes* \> *Activate ICF service for UI theme designer*.



## Authorizations

For write access to the UI theme designer \(create, update, delete themes\), you must be assigned the following authorization object:

-   Authorization object: /UI5/THEME
-   ACTVT \(Activity\): 02 \(Change\)
-   /UI5/THMID \(Theme Id\): \* = all themes

Administrators can assign the relevant authorization objects to specific users using transaction *Role Maintenance* \(`PFCG`\).



## Browser Support

For a list of supported browsers, see [Supported Browsers](../Get-Started/supported-browsers-a8c11ef.md).



<a name="loioa681c0de71ce48bb8cc9735abcdc29b0__section_N10014_N10011_N10001"/>

## Clients

Since themes are client-specific, the client you use to start the UI theme designer must be the same as the client of the theme repository. In addition, both need to run on the same server.

