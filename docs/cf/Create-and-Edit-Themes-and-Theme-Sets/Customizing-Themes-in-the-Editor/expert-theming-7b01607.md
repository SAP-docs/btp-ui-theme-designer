<!-- loio7b01607cb9564f6d94087a6db995c350 -->

<link rel="stylesheet" type="text/css" href="../../css/sap-icons.css"/>

# Expert Theming

If you need to make changes beyond what [Quick Theming](quick-theming-e4d2a95.md) or [Detailed Theming](detailed-theming-db09bb9.md) offer, use expert theming. This option lets you browse all available parameters and make fine-tuned adjustments to your theme.



<a name="loio7b01607cb9564f6d94087a6db995c350__prereq_ycq_th3_3yb"/>

## Prerequisites

You are working in the editor as described in [Customizing Themes in the Editor](customizing-themes-in-the-editor-aa4b233.md).



<a name="loio7b01607cb9564f6d94087a6db995c350__context_N10015_N10012_N10001"/>

## Context

Expert theming provides access to all parameters, including main and control-specific parameters.

For more information about SAP’s theming concept, see [SAP Design System: Theming](https://www.sap.com/design-system/fiori-design-web/foundations/visual/theming). For details on the parameter hierarchy, refer to [SAP Design System: Design Tokens](https://www.sap.com/design-system/fiori-design-web/v1-142/foundations/visual/design-tokens) and [Theme Parameter Dependencies](../../Advanced-Information/theme-parameter-dependencies-18d80b4.md).

You can filter parameters by:

-   Type
-   Tags
-   Changed \(delta\) parameters
-   Parameters with calculation errors
-   Control picker
-   Search



<a name="loio7b01607cb9564f6d94087a6db995c350__steps_rl1_m4r_y3b"/>

## Procedure

1.  In the *Editor* page, select *Expert*.

2.  Use the available filters and search options to find relevant parameters:

    -   *Type Filter*: Show only parameters of a specific type \(all, color :art:, typography <span class="SAP-icons-V5"></span>, dimension <span class="SAP-icons-TNT-V3"></span>, image <span class="SAP-icons-V5"></span>\).
    -   *Delta Filter* <span class="SAP-icons-V5"></span>: Show only changed parameters.
    -   *Error Filter* <span class="SAP-icons-V5"></span> Show only parameters with errors. Errors can occur when values are invalid or when parameters depend on other parameters that contain errors.
    -   *Tags*: Open the tag view <span class="SAP-icons-V5"></span> and select one or more tags to filter parameters. Only parameters that match all selected tags are shown \(tags are combined using a logical AND\). Selecting a control’s tag helps you find parameters relevant to that control. Control tags correspond to the names of the control preview pages.
    -   *Search Field*: Enter a term to search by parameter ID, description, source value, or calculated value. Example: Searching for `sapBrandColor` finds all related parameters and values containing that ID in the calculation function.
    -   *Search Query*: Use `id:`qualifier to search for specific parameter IDs. Only the OR operator | is supported in the search text. Example: `id:sapError|sapWarning` filters for all parameters that contain `sapError` or `sapWarning`.
    -   *Control Picker*: Activate the control picker <span class="SAP-icons-V5"></span>, select a control in the preview, and automatically filter parameters influencing that control. The control picker copies relevant parameter IDs to the search field using the `id:` qualifier and runs the search. All matching parameters are displayed in the list. To reset the list, clear the search field.

    > ### Note:  
    > The control picker works best for preview pages from the SAPUI5 Controls and SAPUI5 Applications test suites. It is not available for cross-origin preview pages. For details, see [Selecting and Adding Preview Pages](selecting-and-adding-preview-pages-8988483.md).

3.  Change the parameter values according to your needs as described in [Changing Parameters](changing-parameters-0d328f8.md).




## Results

The preview updates automatically.



## Next Steps

Save your theme as described in [Saving Themes](saving-themes-c99d9df.md).

