<!-- loio49c377f6ef4f4df0af5078f618fc2de7 -->

# Working With Dimension Parameters



The SAP Design System uses rem-based dimension parameters.

**rem** stands for **root em** and defines dimensions relative to the font size of the root element. This improves accessibility: Entire applications can be resized by simply changing the font size of the root element. This helps to meet [Success Criterion 1.4.4 \(Resize Text \(Level AA\)\)](https://www.w3.org/WAI/WCAG21/Understanding/resize-text) of the Web Content Accessibility Guidelines \(WCAG\) 2.1.

The actual value of 1 rem depends on the font size of the root element. The font size of the root element is determined at runtime when the application is loaded. Therefore, it can lead to unexpected results if different units, such as pixels and rems, are combined in a single computation that certain frameworks execute internally during compilation.

> ### Caution:  
> For these reasons, we strongly recommend using rems when changing dimension parameters in a custom theme.

To convert pixel values to rems, you can use the approximation of **1 rem = 16 px**. This is also used in the design phase of themes provided by SAP. Example for a 3 px `@sapButton_BorderWidth`: **3/16 = 0.1875 rem**

