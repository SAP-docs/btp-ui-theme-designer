<!-- loiof987d5ffccd743cf88b0865c3bbbbe4f -->

# Creating a New Theme

Administrators create themes using the *Create New Theme* wizard in the UI theme designer.



## Prerequisites

Use transaction `/UI5/THEME_DESIGNER` in your ABAP back-end system.

For supported browsers, see [Custom Themes: Important Things to Know](../Get-Started/custom-themes-important-things-to-know-8882c96.md).

> ### Remember:  
> Keep in mind that you must be assigned the following authorization objects for permanent write access to the UI theme designer \(create, update, delete themes\):
> 
> -   Authorization object: /UI5/THEME
> -   ACTVT \(Activity\): 02 \(Change\)
> -   /UI5/THMID \(Theme Id\): \* = all themes
> 
> Administrators can assign the relevant authorization objects to specific users using transaction *Role Maintenance* \(`PFCG`\).
> 
> Without these authorizations, you can create and edit temporary themes that you can export but **not save**.



<a name="loiof987d5ffccd743cf88b0865c3bbbbe4f__steps_vyz_yrg_nj"/>

## Procedure

1.  On the welcome screen, choose *Create Theme* to start the wizard.

    Select an SAP standard theme as your base theme. Note that you are not editing the SAP standard theme itself; rather, you are adjusting a copy of it and saving it under a new name.

    Check the dependencies between the SAP theme and the UI technologies that support it.

    Choose the theme that is closest to the design you want to achieve.

2.  Choose *Create Theme*.

    The wizard closes and you're directed to the editor screen.


**Related Information**  


[Adding Target Content](adding-target-content-6f99f7f.md "Administrators add target content in order to preview any changes they make to the theme.")

