<!-- loiof1f032537e30404695768e8f09b29791 -->

# Rebuilding Themes after Upgrades

Administrators may have to rebuild the stylesheet definitions of a theme after having upgraded an ABAP system to a higher support package \(SP\) or implemented a patch for the rendering of one of the supported UI technologies.



<a name="loiof1f032537e30404695768e8f09b29791__context_N10015_N10012_N10001"/>

## Context

Your themes are always based on SAP themes. If the SAP theme on which your theme is based was upgraded to a new version with a higher SP stack or patch, rendering issues may occur. To avoid them, you need to rebuild the CSS files of your theme.

> ### Note:  
> Upgrade safety is not provided for any changes made in the *CSS* tab. If you used custom CSS for your theme, you should be prepared to make manual adjustments after an upgrade or patch.



## Procedure

1.  Start the UI theme designer.

2.  In the welcome screen in the *Available Themes* section, select your custom theme. If you have several custom themes, you can use the search field to locate one.

3.  Choose *Rebuild*.

    The CSS files are built for the new version.




<a name="loiof1f032537e30404695768e8f09b29791__postreq_ohj_bb5_q2b"/>

## Next Steps

> ### Note:  
> For important information about upgrading themes for SAP GUI for HTML and Web Dynpro ABAP apps, refer to SAP Note [2574997](https://launchpad.support.sap.com/#/notes/2574997).

