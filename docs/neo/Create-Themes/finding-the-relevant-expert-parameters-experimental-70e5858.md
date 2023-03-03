<!-- copy70e58588e47a482cbb5eaf2cc9764ecd -->

# Finding the Relevant Expert Parameters \(Experimental\)

The UI theme designer tools help you to find the Expert parameters that are relevant for the styling of specific UI elements.



<a name="copy70e58588e47a482cbb5eaf2cc9764ecd__section_krv_jqy_cqb"/>

## UI Element Highlighting

If you select a parameter in the *Expert* view, the UI elements that are affected by this parameter are highlighted in the preview area.



## **CSS Search**

With the CSS search option in the Expert tab, you can search for parameters used in CSS rules.

1.  Select a preview page \(for example the button control preview for UR\) and open the *Expert* tab.
2.  Select a UI element in the preview area.
3.  Open the context menu and choose *Inspect Element*.

    The developer tools open and display the CSS rules that apply to the selected UI element.

4.  Copy a CSS rule from the developer tools window \(for example, ***.urBtnStd***\).
5.  In the search field of the Expert tab, enter the search operator ***css:*** followed by the CSS rule you just copied \(for example, ***css: .urBtnStd***\).

    All parameters assigned to CSS rules which contain ***.urBtnStd*** are displayed in the parameter list.

    > ### Note:  
    > To perform an exact search, you enclose the search term in quotes \(for example, ***css: ".urBtnStd"***\). In this case, all parameters assigned to the specified CSS rule are displayed in the parameter list.




<a name="copy70e58588e47a482cbb5eaf2cc9764ecd__section_qxn_kqy_cqb"/>

## Searching for Parameter Names

In the search field for the Expert tab, you can enter the name or parts of a name of parameters. To search for more than one name \(part\) you can concatenate them with the vertical bar *|*. An example: To search for parameters containing the words "background" OR "base", please enter "background|base".

If you search this way, you see parameters with a name which contains the search term, but also parameters where the search term is part of the parameter value \(e.g. if the value contains LESS coding with another parameter name\). If you only want to find the search term within parameter names, you can prepend it with "id:" — e.g. “id:background”

As described above you can search for parameters which are used within a CSS rule by using "css:rulename" — e.g. "css: .urBtnStd".

