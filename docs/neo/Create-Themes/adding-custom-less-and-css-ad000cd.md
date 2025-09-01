<!-- copyad000cde148843e4a83262c446a350b3 -->

# Adding Custom LESS and CSS

Add custom LESS or CSS to make adjustments to your theme that are not possible by changing the values of the theming parameters provided in the *Quick*, *Detailed*, or *Expert* tab.



<a name="copyad000cde148843e4a83262c446a350b3__prereq_N1001D_N1001A_N10001"/>

## Prerequisites

-   You have created a theme or selected an existing one and opened it for editing.

-   You have added preview pages and selected one of them.




<a name="copyad000cde148843e4a83262c446a350b3__context_N10014_N10011_N10001"/>

## Context

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

2.  For SAPUI5 and Unified Rendering technologies, select the appropriate option in the technology dropdown, for all other technologies choose *Base*. **Note:** You can only select a technology from the *UI Technology* dropdown after you have chosen a preview page for that specific technology.

3.  Choose *Add Custom CSS*.

4.  Enter your LESS or CSS code in the editor.

    You want to define that the color of the whole page of an SAPUI5 application is the same as the brand color but with an opacity of 10%. To do so, you can use the SAPUI5 CSS class `sapUiBody` and reference the CSS custom property for the theming parameter `sapBrandColor`.

    ```
    .sapUiBody{ 
    	background-color: hsl(from var(--
    sapBrandColor) h s l / .1);
    }
    ```

5.  Choose *Apply*.




<a name="copyad000cde148843e4a83262c446a350b3__result_N10037_N10012_N10001"/>

## Results

The code you have entered is reflected in the application preview immediately afterwards.

