<!-- copya9a41519f39649f0ac35a7193d69acec -->

# Publishing Themes

Administrators publish their themes to make them available in the Theme Manager, from where they are assigned to sites and apps.



<a name="copya9a41519f39649f0ac35a7193d69acec__prereq_k33_zwp_y1b"/>

## Prerequisites

-   You have opened the UI theme designer from SAP Fiori Launchpad configuration cockpit in SAP BTP Portal.

-   You have saved your theme in the UI theme designer and can view it in the welcome screen.

-   You have resolved any issues or errors in your theme and it is ready to be published.




## Context

Once you have created a theme and saved it, you need to publish it to the Theme Manager in SAP BTP. Using the Theme Manager, you can then assign your theme to the relevant site and applications.



## Procedure

1.  In the welcome screen, select the theme you want to publish.

    In the *Details* section, the following information is visible:

    -   Validation-status message: If the build is successful, this field displays a link to the HTML5 application of your theme in your subaccount. The UI theme designer attempts to create this when you save the theme.

    -   *Status* property: This field displays one of the following messages

        -   *Never Published*

            The theme has been saved but has never been published.

        -   *Published*

            The theme has been published successfully.

        -   *Modified*

            The theme has been published and registered with the Theme Manager. if you make more changes to the published theme, you need to publish the theme again.



2.  To publish your theme, click on *Publish*. Alternatively, you can go to *Theme* \> *Save and Publish* in the editor. This not only saves your theme but registers the theme automatically with the Theme Manager.

    > ### Note:  
    > When you already use a theme and update it \(save & publish\), you might not see the changes because the theme is cached. To invalidate the cache, the Portal site must be published again. To do so, go to the Fiori Configuration cockpit and click *Publish*.

3.  Open the Theme Manager to see a list of your existing and available themes. You can then assign and publish the theme to your preferred site, or make the theme available for end user selection.

    > ### Tip:  
    > It takes a few minutes for a theme to become visible at runtime. Sometimes, it is necessary to enforce reloading of the application by clicking the *CTRL* button and the *Reload* button of the browser together, or by clearing the browser cache.

    > ### Note:  
    > If you launch the UI theme designer directly in the SAP BTP cockpit, there is no connection with the SAP Fiori launchpad configuration cockpit or the Theme Manager. When you publish a theme, the theme is validated and activated but **not registered with the Theme Manager**.
    > 
    > To register the theme, open the UI theme designer in the SAP Fiori launchpad configuration cockpit, locate your theme, and click the *Publish* button.


