<!-- loio0980cc66dfb54ca0923e25bf64812085 -->

# Finding the Relevant Expert Parameters \(Experimental\)

The UI theme designer tools help you to find the Expert parameters that are relevant for the styling of specific UI elements.

> ### Note:  
> The tools for finding parameters are experimental. Experimental features are not part of the officially delivered scope that SAP guarantees for future releases – this means that experimental features may be changed by SAP at any time for any reason without notice. Experimental features are NOT FOR PRODUCTIVE USE. You may not demonstrate, test, examine, evaluate or otherwise use the experimental features in a live operating environment or with data that has not been sufficiently backed up.
> 
> The purpose of experimental features is to get feedback at an early point of time allowing customers/partners to influence the future product accordingly. Please use the [UI Technology Community \(SCN\)](http://help.sap.com/disclaimer?site=http://scn.sap.com/community/ui-technology/content?filterID=contentstatus%5bpublished%5d~category%5bui-theme-designer) to provide feedback, accepting that Intellectual Property rights of the contributions or derivative works shall remain the exclusive property of SAP.



<a name="loio0980cc66dfb54ca0923e25bf64812085__section_krv_jqy_cqb"/>

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




<a name="loio0980cc66dfb54ca0923e25bf64812085__section_qxn_kqy_cqb"/>

## Searching for Parameter Names

In the search field for the Expert tab, you can enter the name or parts of a name of parameters. To search for more than one name \(part\) you can concatenate them with the vertical bar *|*. An example: To search for parameters containing the words "background" OR "base", please enter "background|base".

If you search this way, you see parameters with a name which contains the search term, but also parameters where the search term is part of the parameter value \(e.g. if the value contains LESS coding with another parameter name\). If you only want to find the search term within parameter names, you can prepend it with "id:" — e.g. “id:background”

As described above you can search for parameters which are used within a CSS rule by using "css:rulename" — e.g. "css: .urBtnStd".

