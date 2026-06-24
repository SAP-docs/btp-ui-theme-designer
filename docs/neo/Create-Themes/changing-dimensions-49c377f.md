<!-- loio49c377f6ef4f4df0af5078f618fc2de7 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Changing Dimensions

SAP themes are based on font sizes relative to the root element \(the unit `rem`\). You can change dimension parameters using `rem`-based values. Other units will lead to calculation errors. Use with caution: dimension parameters affect the layout of SAP Build Work Zone sites and applications.



## Prerequisites

You use [Expert Theming](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/7b01607cb9564f6d94087a6db995c350.html "If you need to make changes beyond what or offer, use expert theming. This option lets you browse all available parameters and make fine-tuned adjustments to your theme.") :arrow_upper_right:.



## Procedure

1.  Select *Dimensions* <span class="SAP-icons-TNT-V3"></span> from the type filter.

2.  Enter a `rem`-based value for the parameter you want to change. See “ems and rems” in [MDN: CSS values and units](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Values_and_units) for details on the unit `rem`. To convert `px`-based values to `rem`, use the approximation that 1rem equals 16px, as this is the default browser setting. For example, to achieve a `sapButton_BorderWidth` of 3px, use `3px * 1rem/16px = 3rem/16 = 0.1875rem`.

    > ### Note:  
    > Dimension parameters support only single values. Shorthand values \(like `0.125rem 0.25rem`\) are not supported.




## Results

The preview updates automatically.



## Next Steps

Save your theme as described in [Saving Themes](https://help.sap.com/viewer/09f6818d8e064537973102d6289e2aca/Cloud/en-US/c99d9df29d3c4a45a883e15ce2753178.html "You can save changes you made in your theme at any time during its creation and design.") :arrow_upper_right:.

