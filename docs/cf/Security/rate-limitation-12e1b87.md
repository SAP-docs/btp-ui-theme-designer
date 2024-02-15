<!-- loio12e1b87c922144c0883eb27e09984270 -->

# Rate Limitation

Rate limitation is an essential mechanism used in cloud services to control and manage the rate of incoming requests from users or applications.

It is a mechanism to restrict the number of requests that can be made within a specific time window. It helps prevent misuse, ensure fair usage, and maintain optimal performance and reliability of the service.

To protect the SAP UI Theme Designer services from overload or misuse by a specific client, rate limitation has been introduced as follows:

-   The limit is per tenant.

-   Requests sent at a lower rate are processed directly.

-   When the limit for a tenant is exceeded, a temporary exceeding of the normal rate limit occurs to accommodate sudden spikes in traffic or a short-lived upsurge of requests . It allows a certain number of requests to be processed immediately before reverting to the regular rate limit.

-   If the limit and the temporary upsurge is exceeded, subsequent requests are rejected with HTTP response code 429.


The following UI Theme Designer service APIs are protected with the following rate limits:


<table>
<tr>
<th valign="top">

API Endpoint

</th>
<th valign="top">

Maximum Request per Second \(rps\)

</th>
</tr>
<tr>
<td valign="top">

Microservice: https://theming-runtime.cfapps.<landscape\>.hana.ondemand.com

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

/themeroot/v1

</td>
<td valign="top">

10

</td>
</tr>
<tr>
<td valign="top">

/themeinfo/v1

</td>
<td valign="top">

10

</td>
</tr>
<tr>
<td valign="top">

/sap-themes/v1

</td>
<td valign="top">

10

</td>
</tr>
<tr>
<td valign="top">

Microservice: https://theming-repository.cfapps.<landscape\>.hana.ondemand.com

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

/themelist/v1

</td>
<td valign="top">

4

</td>
</tr>
</table>

