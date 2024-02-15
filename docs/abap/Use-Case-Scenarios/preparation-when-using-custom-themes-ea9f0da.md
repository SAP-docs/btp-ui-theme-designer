<!-- loioea9f0daaf1d949ce8f5ac06949617fe5 -->

# Preparation When Using Custom Themes

Several prerequisites must be met so that your custom themes can be applied to an application.



This set up is for a system where only custom themes are used. The custom themes were created in a different system using UI theme designer and transported to this system. For example a custom theme created in a test or productive system.

-   The theme must be published to the server.

-   The following Internet Communication Framework \(ICF\) service node must be activated:

    `/sap/public/bc/themes`

    To perform this step, launch IMG activity *Activate ICF service for using custom themes*. You access the IMG activity in the SAP Customizing Implementation Guide by choosing *SAP NetWeaver* \> *UI Technologies* \> *UI Theme Designer* \> *Maintain Custom Themes* \> *Activate ICF service for using custom themes*.

-   If you use SAP Web dispatcher, the following parameters must be set:


    <table>
    <tr>
    <th valign="top">

    Parameter Name
    
    </th>
    <th valign="top">

    Required Value
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    `wdisp/add_client_protocol_header`
    
    </td>
    <td valign="top">
    
    `true`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `wdisp/handle_webdisp_ap_header`
    
    </td>
    <td valign="top">
    
    -   `1`
    -   `2`


    
    </td>
    </tr>
    </table>
    
    For more information, open SAP Help Portal at [http://help.sap.com](http://help.sap.com) and search for `SAP Web Dispatcher Parameters - Reference`.

    Also see SAP Note [2037174](https://me.sap.com/notes/2037174).


