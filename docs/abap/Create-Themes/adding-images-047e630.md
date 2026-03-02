<!-- loio047e630535094c57b6f97abb738b9515 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Adding Images

You can upload and use your own images, they are stored within your theme.

Use the *Assign Image* dialog to drop images, utilize a file chooser, select an already uploaded image, or remove the selected image. You can also specify the image URL directly.



<a name="loio047e630535094c57b6f97abb738b9515__prereq_ycq_th3_3yb"/>

## Prerequisites

You are working in the editor as described in [Customizing Themes in the Editor](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/aa4b233eb1da4f30ae6d888424a92de5.html "In the editor you can make changes to themes and preview them.") :arrow_upper_right:.



## Procedure

1.  Find the image parameter you want to change. Image parameters have an image swatch next to their value input.
2.  Open the *Assign Image* dialog by selecting the image swatch, or [F4\].
3.  Choose the image you want to use from the *Assign Image* dialog by using one of the following options:
    -   Drop an image on *Drop image files here or press to browse*<span class="SAP-icons-V5"></span>.
    -   Select *Drop image files here or press to browse* to open a file chooser and upload an image.
    -   Choose an image already available in the theme from the *Assign Image* dialog.
    -   Pick *Do not use image* to not use an image.

4.  Select *OK* to confirm.

> ### Note:  
> -   If you know the URL of an image you want to use, you can also directly provide that as the value, instead of opening the **Assign Image** dialog. For example, you could use the value `url("https://example.com/logo.svg")`.
> -   Your whole theme must not exceed 100mb \(unpacked, 10mb gzipped\), including all images you upload. Individual images must not exceed 3mb \(unpacked\). Therefore keep an eye on the file size of your images.
> -   For best results, try to use SVGs where possible. For security reasons, SVGs in themes must not contain JavaScript.
> -   `sapCompanyLogo` is usually contained in a 6rem wide, 2rem high canvas.
> -   `sapFavicon` and `sapShell_Favicon` define the favicon displayed in browser tabs. For maximum browser compatibility, use a 16×16 pixel image in ICO format \(`image/x-icon`, `.ico` file extension\). While modern browsers support other formats \(PNG, SVG\), ICO format ensures consistent display across older browsers and various contexts \(like bookmarks or browser history\).



## Result

The preview updates automatically.



## Next Steps

Save your theme as described in [Saving Themes](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/c99d9df29d3c4a45a883e15ce2753178.html "You can save changes you made in your theme at any time during its creation and design.") :arrow_upper_right:.



## Related Information

Some SAP products offer built‑in logo customization. If your only goal is to change the logo, consider these lightweight options:

-   [SAP Cloud Identity Services: Configure Logo](https://help.sap.com/docs/cloud-identity-services/cloud-identity-services/configure-logo-for-application?version=Cloud)
-   [SAP SuccessFactors Learning: Login Style Theme Settings](https://help.sap.com/docs/successfactors-learning/offering-learning-to-extended-enterprise/login-style-theme-settings)
-   [SAP Integrated Business Planning: Personalize SAP Fiori Launchpad with Your Company Logo](https://help.sap.com/docs/SAP_INTEGRATED_BUSINESS_PLANNING/4bc5c371697441a2aa86826cc46a1b3f/71c0166b21c94d039f656102c74f6bcd.html)

