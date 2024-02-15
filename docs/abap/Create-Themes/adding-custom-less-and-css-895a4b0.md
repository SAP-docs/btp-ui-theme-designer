<!-- loio895a4b03cf664b79976d12f019c68b12 -->

# Adding Custom LESS and CSS

Add custom LESS or CSS to make adjustments to your theme that are not possible by changing the values of the theming parameters provided in the *Quick*, *Detailed*, or *Expert* tab.



<a name="loio895a4b03cf664b79976d12f019c68b12__prereq_N1001D_N1001A_N10001"/>

## Prerequisites

-   You have created a theme or selected an existing one and opened it for editing. For more information, see  <?sap-ot O2O class="- topic/xref " href="72c730b60f6b41b0bfed63b474007b51.xml" text="" desc="" xtrc="xref:1" xtrf="file:/home/builder/src/dita-all/ylx1673875864142/loio6e2d9e0fb80d4d788707c20ca8ff4bd9_en-US/src/content/localization/en-us/895a4b03cf664b79976d12f019c68b12.xml" output-class="" current-file="file:/home/builder/tp.net.sf.dita-ot/2.3/plugins/com.elovirta.dita.markdown_1.3.0/xsl/dita2markdownImpl.xsl" ?> .

-   You have added preview pages and selected one of them. For more information, see  <?sap-ot O2O class="- topic/xref " href="8af60d39007a4847919f8dcbbb7a7b16.xml" text="" desc="" xtrc="xref:2" xtrf="file:/home/builder/src/dita-all/ylx1673875864142/loio6e2d9e0fb80d4d788707c20ca8ff4bd9_en-US/src/content/localization/en-us/895a4b03cf664b79976d12f019c68b12.xml" output-class="" current-file="file:/home/builder/tp.net.sf.dita-ot/2.3/plugins/com.elovirta.dita.markdown_1.3.0/xsl/dita2markdownImpl.xsl" ?> .


> ### Note:  
> Select the preview application for the UI technology for which you want to add custom CSS or LESS.



<a name="loio895a4b03cf664b79976d12f019c68b12__context_N10014_N10011_N10001"/>

## Context

The following UI technologies support custom LESS and CSS:

-   SAPUI5
-   Unified Rendering technologies \(Web Dynpro ABAP, FPM\)

> ### Note:  
> SAP does not take responsibility for changes you make using the CSS tab.
> 
> Note the following when you create custom CSS:
> 
> -   Do not use custom CSS for changes that can be made using the parameters available in the *Quick*, *Detailed*, or *Expert* tab.
> -   CSS or HTML structures of applications and UI technologies might change after upgrades or patches. If you use custom CSS for your theme, you should be prepared to make manual adjustments after an upgrade or patch.
> 
> -   If a preview page uses more than one technology, you get a dropdown menu to decide for which technology the custom LESS/CSS should be changed.



## Procedure

1.  On top of the side panel on the right, choose *CSS*.

2.  Choose *Add Custom CSS*.

3.  Enter your LESS or CSS code in the editor.

    You want to define that the color of the whole page of an SAPUI5 application is the same as the brand color but with an opacity of 10%. To do so, you can use the SAPUI5 CSS class `sapUiBody` and reference the theming parameter `sapBrandColor`.

    ```
    .sapUiBody{ 
    background-color:fade(@sapBrandColor,10);
    }
    ```

    If you now change the brand color using the *Quick* tab, the color of the whole page adjusts automatically.

    You can also define your own LESS variables and reuse them within your coding.

4.  Choose *Apply*.




<a name="loio895a4b03cf664b79976d12f019c68b12__result_N10037_N10012_N10001"/>

## Results

The code you have entered is reflected in the application preview immediately afterwards.

