<!-- loiobfe0aa3a3a6b4c46bc9c4b0b86b67dbb -->

# Theme Fallback

Theme fallback is a multi‑phase mechanism that ensures a valid theme by checking custom, SAP, flavor, and default options when the requested theme is unavailable or invalid.

The theming service on SAP BTP, Cloud Foundry implements a theme fallback mechanism to ensure that applications always receive a valid theme, even when the originally requested theme is unavailable, invalid or fails to compile. The mechanism operates through multiple phases, each with specific logic for finding the next best available theme.

For every theme request, the fallback process begins with the requested theme and continues through a series of fallback options. These include custom fallback chains, SAP theme counterparts, color-scheme-based fallbacks \(“flavor”, for example light, dark, high-contrast black or high-contrast white\), default themes, and a final last-resort attempt. Each theme is validated in turn, and the first valid theme found is used.



## Fallback Phases

The fallback process is organized as a sequence of validation phases that the system walks through until it finds a valid theme or exhausts all options.

Themes are validated in each phase; if a valid theme is identified, the fallback process stops. Themes are considered only once and, if present in multiple phases, are applied only in the first phase. A phase stops early if a cycle is detected; that is, if the same theme appears in the same phase more than once.



### Phase 1: Custom Fallback Chain

You can define a fallback theme for a custom theme. For more information, see [Defining a Fallback Theme](defining-a-fallback-theme-af0f4e6.md). If the fallback is itself a custom theme, it can define its own fallback, creating a chain. As this chain is processed, any SAP themes extended by these custom themes are collected as "preferred SAP themes".



### Phase 2: Preferred SAP Themes

The preferred SAP themes collected in Phase 1 are iterated.



### Phase 3: Flavor Fallback Chain

Some SAP themes define a “flavor fallback theme”. This allows, for example, High Contrast Black \(Horizon\) to fall back to High Contrast Black \(Quartz\). If the initially requested custom theme is based on such an SAP theme, this chain is followed.



### Phase 4: Default Fallback Chain

The service checks the fallback chain of the default theme defined by the Base framework.



### Phase 5: Final Fallback Actions

If all other fallback options fail, the system performs the following last-resort actions:

-   Retrieve the theme from the latest successfully compiled patch for the requested UI framework version.
-   If the requested UI framework is UI5:
    -   Retrieve the SAP theme that the originally requested theme depends on.
    -   Retrieve the global default theme \(Quartz Light\), not the Base framework default theme.

-   If no valid theme can be determined, respond with 400 Bad Request and hand over fallback resolution to the UI framework.




### Example: `custom_belize_hcb` based on `sap_belize_hcb`

To illustrate the phases, consider a custom theme `custom_belize_hcb` that is based on `sap_belize_hcb` and defines `custom_hcb` based on `sap_hcb` as its fallback theme. Requesting a UI5 `library.css` for this theme with SAPUI5 1.136 will dive deep into the fallback chain, because SAPUI5 1.136 removed support for Belize themes.

**Phase 1: Custom Fallback Chain** 

-   `custom_belize_hcb`, the initially requested theme → extends `sap_belize_hcb`, which is not supported by SAPUI5 1.136 → has a fallback theme: `custom_hcb`, continue with that.
-   `custom_hcb`, the fallback theme of `custom_belize_hcb` → extends `sap_hcb`, which is not supported by SAPUI5 1.136 → does not have a fallback theme, continue with phase 2.

**Phase 2: Preferred SAP Themes**

-   `sap_belize_hcb`, the theme `custom_belize_hcb` extends → not supported by SAPUI5 1.136 → more preferred SAP themes collected in phase 1, continue with them.
-   `sap_hcb`, the theme `custom_hcb` extends → not supported by SAPUI5 1.136 → no more preferred SAP themes, continue with phase 3.

**Phase 3: Flavor Fallback Chain**

-   `sap_horizon_hcb`, the flavor fallback theme of `sap_belize_hcb` → supported by SAPUI5 1.136. → finish fallback with redirect to `sap_horizon_hcb`.

