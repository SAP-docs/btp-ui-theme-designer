<!-- copyf98fe1066268405e8c30af68abe6a22f -->

# Protecting Access to UI Theme Designer

Add a role and assign it to the UI theme designer permission to restrict access to UI theme designer.



## Prerequisites

You are subscribed to the UI theme designer application.

See  <?sap-ot O2O class="- topic/xref " href="95338b0d57a74eea9f99db054b5a308e.xml" text="" desc="" xtrc="xref:1" xtrf="file:/home/builder/src/dita-all/xch1723619576420/loio224f0e792494418c8c4351fa75099a04_en-US/src/content/localization/en-us/f98fe1066268405e8c30af68abe6a22f.xml" output-class="" outputTopicFile="file:/home/builder/tp.net.sf.dita-ot/2.3/plugins/com.elovirta.dita.markdown_1.3.0/xsl/dita2markdownImpl.xsl" ?> .



## Context

In the SAP BTP cockpit, you can create custom roles and assign them to the defined permissions. If a user accesses an application path that starts with a path defined for a permission, the system checks whether the current user is a member of the assigned role. If no role is assigned to a defined permission, all authenticated users have access to the corresponding application path.

The corresponding permissions are:

-   `UIThemeDesignerPermission` - enables access to the UI theme designer tool.

-   `AccountDeveloper` - enables read/write access to the themes.

-   `SupportUser` - enables read access to the themes.


