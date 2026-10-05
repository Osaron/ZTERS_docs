# CUBE User Stories — Phase 2 Baseline

**Purpose:** Compact reference baseline for comparing later CUBE user stories and classifying them as **Existing**, **New Feature**, or **Hybrid**.

**Classification rule:**
- **Existing** — the capability is already covered by Phase 2.
- **New Feature** — the capability is not represented in Phase 2.
- **Hybrid** — the core capability exists in Phase 2, but the later story introduces a meaningful addition, change, extension, validation, workflow, field, UI behavior, integration, permission, or business rule.

**Verified totals:** Day 1 = 121 | Day 2 = 148 | Day 3 = 169 | **Total = 438**

---

# Day 1

**Stories:** 121

## Day 1 — Story 001
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Vendor Pricing App
- **Task Name:** View PSP and Managed Service Provider counts
- **User Story:** As an SPM specialist, I want a vendor pricing dashboard that clearly summarizes preferred and managed Service Providers so I can quickly understand which providers have active pricing zones and PSP status.
- **Description:** Design a dashboard screen for the Vendor Pricing module that shows high-level counts and breakdowns of Service Providers (e.g., Preferred / PSP vs Managed / non-PSP) and highlights those with pricing zones configured but no longer flagged as PSP.
- **Acceptance Criteria:** - Dashboard displays total number of Service Providers with pricing zones, broken down into PSP and Managed categories - Each count is clickable and drills down to a filtered list of providers - PSP vs Managed status is visually distinct (icons, badges, or color tags) - Screen matches navigation structure agreed for Cube (Vendor Pricing as a sub-module) - UX reviewed and confirmed usable by at least one SPM specialist

## Day 1 — Story 002
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Vendor Pricing App
- **Task Name:** Filter and search Service Providers in pricing app
- **User Story:** As an SPM specialist, I want to search and filter Service Providers within the Vendor Pricing app so I can quickly locate a provider before creating or updating pricing zones.
- **Description:** Provide search and filter controls on the Vendor Pricing list view so users can locate a Service Provider by name, ID, status (PSP/Managed), product line, or geography before opening their pricing context.
- **Acceptance Criteria:** list view includes a free - text search (name, ID) and filters for PSP status, product type (toilets, dumpsters, containers, fencing), and active / @inactive status - @Applying filters updates the list without a full page reload in the prototype flow - Selected Service Provider row clearly shows name, ID, and PSP / @Managed badge - From a Selected row, user can open detail view or jump to pricing zones with a single obvious action

## Day 1 — Story 003
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Create Pricing Zone for Service Provider
- **Task Name:** Create / Edit Pricing Zone
- **User Story:** As an SPM specialist, I want a guided form to create a new Pricing Zone for a Service Provider so that all required information (zone type, geography, link to Service Provider) is captured consistently.
- **Description:** Design a Pricing Zone create/edit form that is opened from a Service Provider context, pre-filling the Service Provider link and clearly marking required fields (zone type, zone label/name, geography definition).
- **Acceptance Criteria:** - User can open "Add Pricing Zone" from a Service Provider detail screen - Service Provider is pre-linked and displayed read-only on the form - Required fields (e.g., Zone Type, Zone Name/Label, Effective Status) are visually indicated - Validation prevents saving an incomplete zone and displays inline error messaging - Cancel returns the user to the previous context without losing other data

## Day 1 — Story 004
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Configure Zone Geography
- **Task Name:** Configure Address/Distance-based Pricing Zone
- **User Story:** As an SPM specialist, I want to configure an address/distance-based Pricing Zone so the system can automatically calculate which ZIP codes belong to that zone based on miles from a depot address.
- **Description:** Within the Pricing Zone form, provide a UI for the "Address / Distance-based" option where the user can enter a radius in miles and select or confirm the depot address, and the system then displays the calculated coverage area (ZIP list preview).
- **Acceptance Criteria:** - Selecting Zone Type = "Address / Distance-based" reveals fields for "Depot Address" and "Radius (miles)" - Depot Address defaults to the Service Provider's main or W-9 address but can be changed to another depot - On entering a radius and confirming the depot, UI shows a generated preview (e.g., count of ZIP codes, expandable list) before saving - User can edit radius and depot and see updated preview without losing other data

## Day 1 — Story 005
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Configure Zone Geography
- **Task Name:** Configure ZIP-list-based Pricing Zone
- **User Story:** As an SPM specialist, I want to define a ZIP-list-based Pricing Zone so that I can explicitly control which ZIP codes belong to a Service Providerâ€™s service area.
- **Description:** Allow the user to define a Pricing Zone where the geography is a manually curated list of ZIP codes, editable from the UI, with import and inline editing options.
- **Acceptance Criteria:** - Selecting Zone Type = "ZIP List" reveals a control for managing one or more ZIP codes - User can add ZIP codes individually, paste a comma/line-separated list, or bulk-import from clipboard - ZIP codes are validated for format; invalid entries are clearly flagged for correction - After save, the resulting ZIP list is visible and editable from the Pricing Zone detail view

## Day 1 — Story 006
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Link Pricing Zones to Service Provider
- **Task Name:** View Service Provider Pricing Zones
- **User Story:** As an SPM specialist, I want to see all Pricing Zones associated with a Service Provider so I can verify coverage and avoid overlapping or conflicting zones.
- **Description:** On the Service Provider detail screen, display a structured list/table of that providerâ€™s Pricing Zones (zone name, type, geography summary, product coverage, status) with quick access to view or edit each zone.
- **Acceptance Criteria:** - Service Provider detail view contains a Pricing Zones section/table - Each row shows: Zone ID, Zone Name, Zone Type (ZIP/Address-based), short geography summary (e.g., radius or ZIP count), and active/inactive status - Each row has actions to open zone detail or edit the zone - UX supports sorting and/or filtering zones when a provider has multiple zones

## Day 1 — Story 007
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Search Pricing by Address
- **Task Name:** Enter address and view applicable Service Provider pricing
- **User Story:** As a Fulfillment or SPM user, I want to enter a site address into the Pricing Tool and see which Service Provider pricing applies so that I can quickly quote the correct rate.
- **Description:** Design the Pricing Tool screen where the user enters a full job-site address, and the system determines applicable Service Provider zones and displays relevant pricing rows for the products at that location.
- **Acceptance Criteria:** - Pricing Tool input section includes structured address fields or a single validated address field - After submission, pricing results are shown in a results grid scoped to that location - If the location is covered by an address/distance-based PSP zone, that zoneâ€™s pricing is used; if not, fallbacks (e.g., statistical pricing) are visible - Loading / no-results / error states are defined in the UI

## Day 1 — Story 008
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Adjust Pricing Tool View
- **Task Name:** Switch between role-based Pricing Tool views
- **User Story:** As a user in different roles (Account Manager, Fulfillment, SPM), I want to switch between role-based views in the Pricing Tool so I can see the information most relevant to my job (e.g., PSP details vs customer-facing pricing).
- **Description:** Provide a view toggle control on the Pricing Tool results page (e.g., tabs or segmented control) that changes columns/fields shown depending on whether the user selects Account Manager, Fulfillment, or Service Provider Team view.
- **Acceptance Criteria:** - UI includes clearly labeled view options (e.g., "Account Manager", "Fulfillment", "Service Provider Team") - Each view adjusts visible columns/fields in the pricing results (e.g., internal cost vs customer price vs operational fields) - Currently selected view is visually highlighted and persists during interaction within the session - UX makes it obvious that switching views does not change underlying pricing, only the presentation

## Day 1 — Story 009
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Distinguish PSP vs Statistical Pricing
- **Task Name:** Indicate PSP vs statistical model pricing in results
- **User Story:** As a user in the Pricing Tool, I want to clearly see which rows come from PSP confirmed rates versus statistical model pricing so I can trust and interpret the numbers correctly.
- **Description:** In the Pricing Tool results grid, visually differentiate rows that are PSP-based (confirmed provider pricing) from those using statistical model pricing, using icons/labels and a simple legend.
- **Acceptance Criteria:** - Each pricing row includes a small indicator showing source: PSP (e.g., "P" icon/badge) or Statistical (e.g., "S" icon/badge) - A legend or hover help explains what PSP vs Statistical means in non-technical terms - PSP rows are visually distinct but still readable/accessible (no color-only reliance) - UX ensures indicators are consistent wherever pricing rows appear in the app

## Day 1 — Story 010
- **Feature:** Service Provider Pricing Management
- **Parent Task:** Manage Pricing Records
- **Task Name:** Import pricing records for a product type from clipboard
- **User Story:** As an SPM specialist, I want to bulk import pricing records for a given product type from a clipboard/pasted spreadsheet so I can load or update many rates efficiently without manual entry.
- **Description:** Within a Pricing Zone detail screen, allow the user to add or update pricing records for a specific product type (e.g., toilets) by pasting tabular data from a spreadsheet via an "Import from Clipboard" interaction.
- **Acceptance Criteria:** - Pricing Zone detail has a clear action (e.g., "Import pricing from clipboard") scoped to a product type - Import UI explains the expected column order/format (e.g., product code, delivery, rental, service frequency) - After paste, the user sees a preview grid and can confirm or cancel before committing - On confirm, records are added/updated in the zone and visible in the prices list

## Day 1 — Story 011
- **Feature:** Service Provider Pricing Management
- **Parent Task:** SPM â€“ Manage PSP Pricing
- **Task Name:** Paste pricing from spreadsheet into pricing records grid
- **User Story:** As an SPM user, I want to paste pricing from a spreadsheet into the pricing records grid so I can quickly update multiple Service Provider prices without manual data entry for each record.
- **Description:** SPM users (roles like Amber/Sandra) currently receive pricing in spreadsheets and use an "import from clipboard" function to populate pricing records in bulk. The UI should clearly guide them to copy properly formatted columns from Excel/Sheets and map them into pricing fields for a selected Service Provider and zone.
- **Acceptance Criteria:** Given I AM an SPM user on a Service Providerâ€™s pricing Zone, when I choose an import-@From-clipboard action, then I see clear instructions and a paste area for the pricing rows and columns. - when I paste valid, properly formatted rows, then the system shows a preview with column mapping before commit. - when I confirm the import, then the system creates/@updates pricing records and shows a success summary with counts and any row-@level errors.

## Day 1 — Story 012
- **Feature:** Service Provider Pricing Management
- **Parent Task:** SPM â€“ Manage PSP Pricing
- **Task Name:** Restrict pricing upload/edit UI to SPM roles
- **User Story:** As a system administrator, I want pricing upload/edit controls visible only to SPM roles so that Service Providers and non-SPM users cannot accidentally change internal pricing.
- **Description:** Today, only people in Amber/Sandraâ€™s role know and use the pricing upload workflow, but technically the Quickbase app isnâ€™t hard-locked. In Cube, the UI should explicitly enforce that only SPM roles see actions like "Import pricing", "Bulk edit pricing", and "Delete pricing record" for Service Provider rate cards.
- **Acceptance Criteria:** Given I log in as an SPM user, when I view a Service Providerâ€™s pricing, then I see buttons/menus for uploading, editing, and deleting pricing records. -@ Given I log in as a non-SPM internal user, when I view the same Screen, then I can see pricing but I do not see upload/@edit/@delete actions. - Given I log in as a Service Provider in the portal, then I cannot directly edit internal pricing records used by the pricing tool.

## Day 1 — Story 013
- **Feature:** Service Provider Pricing Management
- **Parent Task:** SPM â€“ Manage PSP Pricing
- **Task Name:** Upload pricing file from Service Provider portal as â€œpending reviewâ€
- **User Story:** As an SPM user, I want pricing files uploaded by Service Providers in the portal to appear as pending pricing changes I can review and approve so we avoid re-keying data while still controlling final rate cards.
- **Description:** Service Providers can upload pricing spreadsheets in the current hub, but those files are just handed to the PSP team, who manually re-enter data. In Cube, when a Service Provider uploads a pricing file in the portal, the system should parse it into a structured "pending pricing changes" object that SPM can open, validate, and approve, instead of manually copying from the spreadsheet.
- **Acceptance Criteria:** - Given a Service Provider uploads a correctly formatted pricing file in the portal, then the system stores it as a pending pricing change batch linked to that Service Provider and product type(s). - When an SPM user opens the pending batch in the admin UI, then they see parsed rows, mapped fields, and validation warnings (if any). - When the SPM user clicks "Approve", then the pending batch is applied to live pricing records and marked as approved with timestamp and user. - When the SPM user clicks "Reject", then no pricing records change and the Service Provider can be notified with a reason.

## Day 1 — Story 014
- **Feature:** Service Provider Pricing Management
- **Parent Task:** SPM â€“ Manage PSP Pricing
- **Task Name:** Quick review & approval of pending pricing uploads
- **User Story:** As an SPM user, I want a streamlined review screen for pending pricing uploads so I can quickly scan, validate, and approve or reject pricing changes from multiple Service Providers without manual rework.
- **Description:** Justin describes a future improvement where Service Providers could upload pricing "already in the format" and SPM only needs to look at it and click a boolean to approve. Cube should provide a review UI that shows summary info (Service Provider, product type, geography, number of rows changed) and lets SPM drill into details before toggling an approval state.
- **Acceptance Criteria:** - Given there are one or more pending pricing batches, when I open the pricing upload review screen, then I see a sortable/filterable list (by Service Provider, date uploaded, product line, status). - When I click into a batch, then I see side-by-side current vs proposed pricing or at least clear before/after values per row. - When I approve or reject a batch, then the list updates immediately with the new status and my action is logged (who, when, what decision).

## Day 1 — Story 015
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Records Management
- **Task Name:** Clarify Pricing Upload Methods
- **User Story:** As a Service Provider Specialist, I need the system to clearly present the available pricing upload methods so I can consistently choose the correct one.
- **Description:** Current pricing updates use three Quickbase import options (clipboard import, file import, table-to-table import), but only clipboard import is commonly used. Users are unclear which methods are supported or recommended. The UI should guide specialists toward the correct upload path.
- **Acceptance Criteria:** UI provides a clear explanation of Each upload method.\n-@ UI labels which method is recommended for PSP pricing updates.\n-@ users can successfully choose a method without confusion.\n-@ no hidden or ambiguous import actions.

## Day 1 — Story 016
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Records Management
- **Task Name:** Surface Rarely-Used Import Tools
- **User Story:** As a UI/UX designer, I need to expose or hide rarely-used Quickbase import options appropriately so specialists are not overwhelmed by unnecessary choices.
- **Description:** Ezequiel expresses confusion about import types and which are actually used. Table-to-table import is used for system automation (recurring billing), not for daily PSP pricing updates. The UI should prioritize commonly used actions while still allowing access to advanced options in an organized, non-confusing way.
- **Acceptance Criteria:** - Frequently used actions (clipboard import) appear primary.\n- Advanced imports grouped under an â€œAdvanced Toolsâ€ section.\n- Helper text explains when to use each method.\n- Users can find all options but are not confused by hierarchy.

## Day 1 — Story 017
- **Feature:** Recurring Billing Automation
- **Parent Task:** Recurring Service Tickets
- **Task Name:** Visualize Table-to-Table Automation
- **User Story:** As a UI/UX designer, I need to visualize how automated table-to-table imports create recurring billing records so that the new ERP design can accommodate this automation in a transparent way.
- **Description:** Justin explains that recurring billing uses table-to-table imports to copy metadata such as prices, service provider, and product details into new ticket records. UI should surface where automation occurs so users understand when records are system-generated vs manually created.
- **Acceptance Criteria:** system-@generated records clearly labeled.\n-@ UI surfaces automation logs or traceability.\n-@ users can distinguish automated vs manual records.\n-@ no confusion on where pricing values originated.

## Day 1 — Story 018
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Template Handling
- **Task Name:** Support Template-Based Pricing Upload
- **User Story:** As a Service Provider Specialist, I need the pricing upload interface to support template-based uploads (like Angelaâ€™s macro spreadsheet) so pricing can be added cleanly without errors.
- **Description:** Amber demonstrates that PSP pricing relies on a macro-enabled Excel template with dropdowns and validated fields. Only yellow/asterisk fields map correctly to pricing records. The UI must support drag-and-drop or structured template upload and prevent wrong column mapping.
- **Acceptance Criteria:** UI accepts structured template files.\n-@ system validates Required fields before import.\n-@ UI warns If hauler ID or pricing Zone ID is missing.\n-@ clear mapping preview before completing upload.

## Day 1 — Story 019
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Records Management
- **Task Name:** Prevent Incorrect Hauler/Zone Mapping
- **User Story:** As a Service Provider Specialist, I need safeguards that prevent pricing uploads from being assigned to the wrong Service Provider or pricing zone.
- **Description:** Amber and Justin discuss that incorrect IDs in spreadsheets can create erroneous pricing records. The UI must warn users when IDs donâ€™t match the selected Service Provider or zone before committing an import.
- **Acceptance Criteria:** UI cross-@checks hauler ID and pricing Zone ID.\n-@ users cannot upload pricing for mismatched IDs.\n-@ UI highlights mismatches in red before import.\n-@ import is blocked until corrected.

## Day 1 — Story 020
- **Feature:** PSP Pricing Management
- **Parent Task:** Bulk Import Pricing Records
- **Task Name:** Map Columns During Clipboard Import
- **User Story:** As a UI/UX designer, I need to design an intuitive column-mapping interface so PSP users can visually confirm that each imported spreadsheet column matches the correct system field, preventing mismatches before uploading pricing records.
- **Description:** - UI displays each imported column name beside the matching system field name. - Users can uncheck row-1 header detection. - System visually flags mismatches or duplicate column names. - User can manually correct mappings before import.
- **Acceptance Criteria:** column-@mapping interface matches Figma prototype. -@ Errors display correctly for duplicates/@mismatches. -@ users can successfully import After correcting mappings.

## Day 1 — Story 021
- **Feature:** PSP Pricing Management
- **Parent Task:** Bulk Import Pricing Records
- **Task Name:** Column Mismatch Error Handling
- **User Story:** As a UI/UX designer, I need a clear error-flagging UI that identifies mismatched or duplicated column headers during import, so users instantly know what to fix.
- **Description:** UI shows pinpointed warnings when two columns share the same header. -@ UI highlights the problematic fields in context. -@ user receives guidance on how to fix the mismatch.
- **Acceptance Criteria:** error state visually consistent across system. -@ users can resolve mismatches and retry import successfully.

## Day 1 — Story 022
- **Feature:** PSP Pricing Management
- **Parent Task:** Bulk Import Pricing Records
- **Task Name:** View Imported Pricing Records
- **User Story:** As a UI/UX designer, I need the system to show a confirmation view of newly imported pricing records so users can verify the import was successful before leaving the screen.
- **Description:** UI shows number of new records created. -@ new records appear in a clean list/@table view. - records reflect correct Zone, product type, and fields.
- **Acceptance Criteria:** Confirmation Screen reviewed and approved. -@ data displays accurately and matches the imported file.

## Day 1 — Story 023
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Record Editing
- **Task Name:** Grid Edit for Pricing Records
- **User Story:** As a UI/UX designer, I need to provide a spreadsheet-style grid edit view so PSP users can quickly modify multiple pricing records at once (e.g., removing fuel surcharge), without opening individual records.
- **Description:** grid supports inline editing of fields. -@ Changes save in bulk. -@ system prevents unauthorized users From accessing grid edit. -@ UI indicates unsaved changes.
- **Acceptance Criteria:** grid edit functions validated. -@ inline updates save correctly. -@ Permission restrictions tested.

## Day 1 — Story 024
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Record Editing
- **Task Name:** Delete Pricing Record
- **User Story:** As a UI/UX designer, I need a safe deletion flow so PSP users can remove a pricing record while reducing accidental deletions (e.g., with confirmation or soft delete).
- **Description:** delete action requires Confirmation step. -@ Soft delete flag supported If enabled. -@ UI warns user about impact of deleting live pricing.
- **Acceptance Criteria:** delete Confirmation modal implemented. -@ Soft delete logic functional. -@ Deleted records do not break pricing tool.

## Day 1 — Story 025
- **Feature:** System Infrastructure
- **Parent Task:** Data Protection
- **Task Name:** Soft Delete Architecture
- **User Story:** As a UI/UX designer, I need a standardized soft delete pattern so users understand when data is archived instead of permanently removed, improving safety across the Cube.
- **Description:** - UI visually distinguishes â€œdeleted/archivedâ€ items. - Soft-deleted items are hidden by default with filter to show them. - Restore option available for authorized roles.
- **Acceptance Criteria:** Soft delete pattern Approved for global use. -@ Figma flows include delete/@restore screens. -@ Backend supports Soft delete flag.

## Day 1 — Story 026
- **Feature:** PSP Pricing Management
- **Parent Task:** Manual Pricing Entry
- **Task Name:** Add Single Pricing Record via Form
- **User Story:** As a UI/UX designer, I need a simple â€œAdd Pricing Recordâ€ form so PSP users can add individual records (e.g., containment, sanitizer) without doing a bulk import.
- **Description:** form supports Selecting pricing Zone &@ product type. -@ All Required fields clearly indicated. -@ UI validates entries before saving.
- **Acceptance Criteria:** form design approved. - @Required fields tested. - @single - @record creation successfully writes to database.

## Day 1 — Story 027
- **Feature:** PSP Pricing Management
- **Parent Task:** Manual Pricing Entry
- **Task Name:** Single-Record Form Creation
- **User Story:** As a UI/UX designer, I need to provide a dedicated 'Add New Pricing Record' form so PSP users can manually add a single pricing record without relying on bulk imports.
- **Description:** - 'Add New Pricing Record' button visible in pricing zone UI. - Form auto-populates context (zone, hauler). - Required fields visually marked. - Validation prevents incomplete/invalid entries.
- **Acceptance Criteria:** Feature validated with PSP team; form tested end-to-end; record appears immediately with correct zone and hauler associations.

## Day 1 — Story 028
- **Feature:** PSP Pricing Management
- **Parent Task:** Manual Pricing Entry
- **Task Name:** Support for Low-Usage Features
- **User Story:** As a UI/UX designer, I need to understand whether manual pricing entry is actually needed so the system only includes UI components that users will use.
- **Description:** Decision documented based on stakeholder input. -@ UI either includes a minimal manual-@entry form or removes it entirely. -@ no hidden or unused actions.
- **Acceptance Criteria:** Decision finalized; Figma updated; unnecessary UI removed or cleaned up.

## Day 1 — Story 029
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Zone Auto-Search
- **Task Name:** Ensure Pricing Zone Field Accepts Full Concatenated ID
- **User Story:** As a UI/UX designer, I need the pricing-record form to accept and correctly search concatenated IDs (VendorID + ZoneID).
- **Description:** search bar matches full concatenated IDs. -@ Hint text explains Required ID format. -@ partial matches still suggest correct zones.
- **Acceptance Criteria:** Search implemented; Figma approved; search tested to correctly match concatenated IDs.

## Day 1 — Story 030
- **Feature:** System Architecture
- **Parent Task:** Pricing Zone Identifier
- **Task Name:** Concatenated VendorID + ZoneID Identifier
- **User Story:** As a UI/UX designer, I need readable composite identifiers so users immediately understand which hauler a zone belongs to.
- **Description:** Composite ID consistently displayed. -@ no duplicate IDs. -@ Filtering and search work with Composite IDs.
- **Acceptance Criteria:** Composite identifier visible in all Figma screens; dev confirms final format.

## Day 1 — Story 031
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Flags & Controls
- **Task Name:** Support DNUs at Vendor, Zone, and Pricing Levels
- **User Story:** As a UI/UX designer, I need distinct DNU toggles for vendor, zone, and pricing-record levels to prevent quoting invalid data.
- **Description:** clear icons and toggles for Each DNU layer. -@ pricing Tool auto-@hides DNUâ€™d items. -@ UI shows warnings where needed.
- **Acceptance Criteria:** DNU indicators implemented; pricing tool correctly excludes disabled records/zones/vendors.

## Day 1 — Story 032
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Zone Deactivation
- **Task Name:** DNU a Pricing Zone
- **User Story:** As a UI/UX designer, I need the ability to DNU an entire pricing zone so all pricing under it is disabled.
- **Description:** DNU toggle at Zone level. -@ Zone visually marked inactive. -@ pricing Tool hides All prices tied to the zone.
- **Acceptance Criteria:** Zone-level DNU tested; pricing tool suppressed all related rates.

## Day 1 — Story 033
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Record Display
- **Task Name:** Surface PSP Suggested Rates & Margins
- **User Story:** As a UI/UX designer, I need pricing records to display vendor rate, suggested customer price, and calculated margin.
- **Description:** clean layout grouping Vendor price, customer price, and margin. -@ Margin updates on edit. -@ matches sales master product calculations.
- **Acceptance Criteria:** Pricing display implemented; validated against sales product data; PSP team sign-off obtained.

## Day 1 — Story 034
- **Feature:** PSP Pricing Management
- **Parent Task:** Accessory Pricing
- **Task Name:** Support Accessory Pricing
- **User Story:** As a UI/UX designer, I need optional accessory-charge sections (containment trays, sanitizer, rigging cages) to be cleanly represented in pricing records.
- **Description:** Accessory section collapsible. -@ supports optional fields. -@ pricing Tool recognizes accessories.
- **Acceptance Criteria:** Accessory pricing validated; UI behaves as expected; tool shows correct totals.

## Day 1 — Story 035
- **Feature:** PSP Pricing Experiments
- **Parent Task:** A/B Test Controls
- **Task Name:** Flag Pricing Records for A/B Tests
- **User Story:** As a UI/UX designer, I need toggles that allow pricing records to be marked as Test Group or Control Group.
- **Description:** clear toggle interaction. -@ Tooltip explaining pricing experiment. -@ pricing Tool logic stays intact.
- **Acceptance Criteria:** Experiment flags displayed; PSP team reviews behavior; design approved.

## Day 1 — Story 036
- **Feature:** Data Synchronization
- **Parent Task:** Webhook Triggering
- **Task Name:** Trigger Sync When Related Records Change
- **User Story:** As a UI/UX designer, I need a 'Sync Pricing' action so users can refresh pricing records when related data changes.
- **Description:** Sync button visible on pricing record. -@ shows progress/@loading state. -@ updates pricing Tool data.
- **Acceptance Criteria:** Sync button works; updated values confirmed in pricing tool; dev team validates webhook behavior.

## Day 1 — Story 037
- **Feature:** PSP Pricing Management
- **Parent Task:** Sync Controls
- **Task Name:** Bulk Sync via Grid Edit
- **User Story:** As a UI/UX designer, I need grid-edit mode to support bulk syncing to update stale pricing.
- **Description:** Bulk checkbox available. -@ UI displays number of records affected. -@ Sync completes without errors.
- **Acceptance Criteria:** Bulk sync tested with multiple zones; UI shows confirmation badge.

## Day 1 — Story 038
- **Feature:** PSP Pricing Management
- **Parent Task:** Record Refresh Behavior
- **Task Name:** Allow Sync from Pricing Tool
- **User Story:** As a UI/UX designer, I need a 'Refresh Pricing' button in the pricing tool to sync data without leaving the quoting flow.
- **Description:** Refresh option visible. -@ shows spinner or progress state. -@ new pricing loads immediately.
- **Acceptance Criteria:** Refresh confirmed working; pricing updates appear instantly in tool.

## Day 1 — Story 039
- **Feature:** PSP Pricing Management
- **Parent Task:** Clipboard Import Process
- **Task Name:** Map & Validate Columns
- **User Story:** As a Service Provider Specialist, I want a clear interface that helps me correctly map spreadsheet columns to system fields so I can confidently upload pricing records without mismatches.
- **Description:** The system should display a clean column-mapping screen that clearly shows both incoming spreadsheet column names and expected field names. The UI should warn users when duplicate column names exist (e.g., two 'removal charge' columns) and highlight mismatches. Users should be able to toggle whether the first row is a header and must see real-time validation feedback before confirming the import.
- **Acceptance Criteria:** â€¢ Users can see both imported column names and expected field names side-by-side  â€¢ System highlights mismatched or duplicate columns  â€¢ UI supports toggling header-row detection  â€¢ Upload cannot proceed if unresolved mismatches exist  â€¢ Successful upload generates visible confirmation

## Day 1 — Story 040
- **Feature:** PSP Pricing Management
- **Parent Task:** Clipboard Import Process
- **Task Name:** Handle Fuzzy Matching Errors
- **User Story:** As a Service Provider Specialist, I want the system to clearly warn me when column names do not match expected field labels so I can correct them before submitting.
- **Description:** Quickbaseâ€™s fuzzy matching often guesses wrong, creating errors. The new UI should clearly identify which fields failed to match and why. It should highlight problematic rows and provide recommended matches. Errors such as 'two columns share the same name' must surface visibly and early.
- **Acceptance Criteria:** â€¢ System detects duplicate column names  â€¢ System lists all mismatched fields with suggested corrections  â€¢ Users can manually override mappings  â€¢ Import is blocked until errors resolve

## Day 1 — Story 041
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Record Review
- **Task Name:** View Imported Pricing Records
- **User Story:** As a Service Provider Specialist, I want to visually confirm that newly imported pricing records display correctly in the pricing zone so I can verify accuracy.
- **Description:** After import, users return to the pricing zone UI and must see all imported product pricing records organized by zone. UI should clearly show which product categories now contain data and allow expanding/collapsing them.
- **Acceptance Criteria:** â€¢ New pricing records appear immediately in the zone  â€¢ UI groups pricing by product type  â€¢ Records contain all imported field values  â€¢ No missing or duplicated rows

## Day 1 — Story 042
- **Feature:** PSP Pricing Management
- **Parent Task:** Grid Edit
- **Task Name:** Inline Edit Pricing Records
- **User Story:** As a Service Provider Specialist, I want inline editing (grid edit) so I can quickly update multiple pricing records at once without opening each individually.
- **Description:** The user selects grid edit mode to bulk-update fields, such as removing fuel surcharges or adjusting accessory pricing. UI must support fast tabbing, in-place editing, mass save, and validation. Only authorized roles should have access, given high risk.
- **Acceptance Criteria:** â€¢ Grid edit is role-restricted  â€¢ Inline editing supports bulk modifications  â€¢ Unsaved changes show warning  â€¢ Save applies all updates with validation

## Day 1 — Story 043
- **Feature:** PSP Pricing Management
- **Parent Task:** Record Deletion
- **Task Name:** Delete Pricing Records Safely
- **User Story:** As a Service Provider Specialist, I want a safe way to delete pricing records so old or irrelevant pricing does not appear in the pricing tool.
- **Description:** Currently deletion immediately erases the record permanently (dangerous). The new UI should support soft delete, confirmation dialogs, and the ability to restore deleted pricing records.
- **Acceptance Criteria:** â€¢ Delete button requires confirmation  â€¢ Soft-delete hides record from UI but retains it for auditing  â€¢ Restore option available to authorized users

## Day 1 — Story 044
- **Feature:** System Infrastructure
- **Parent Task:** Soft Delete
- **Task Name:** Implement Soft Delete Systemwide
- **User Story:** As a System Admin, I want soft delete available for all pricing-related entities so accidental data loss is prevented.
- **Description:** Quickbase has no real soft delete. The new system must implement soft delete for pricing records, zones, products, and provider records. Deleted items hide from UI but remain recoverable.
- **Acceptance Criteria:** â€¢ Soft delete available for all pricing entities  â€¢ Deleted items hidden but restorable  â€¢ UI shows 'Deleted' filter for admins

## Day 1 — Story 045
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Zone Management
- **Task Name:** Upload Zip-List Pricing Manually
- **User Story:** As a Service Provider Specialist, I want the ability to upload or enter zip-codes for a zone manually so I can define service areas without using address-based radiuses.
- **Description:** Amber demonstrates copying zip codes manually. UI should allow pasting or uploading zip lists cleanly and provide validation for invalid or duplicate zip codes.
- **Acceptance Criteria:** â€¢ UI accepts pasted zip list  â€¢ Detects invalid or duplicate zips  â€¢ Displays resulting service area summary

## Day 1 — Story 046
- **Feature:** PSP Pricing Management
- **Parent Task:** Manual Entry
- **Task Name:** Add Pricing Record via Form
- **User Story:** As a Service Provider Specialist, I want a simple form to manually add a single pricing record so I can enter new products without relying on spreadsheet imports.
- **Description:** Justin reveals a feature Amber has never used: manually adding a pricing record via a form. The new UI should support a clean form for adding one-off pricing entries, with clear required fields, product selection, zone selection, pricing fields, accessory fields, and validation.
- **Acceptance Criteria:** â€¢ Form supports adding a single record  â€¢ Required fields marked clearly  â€¢ Product selection tied to product master  â€¢ Pricing fields grouped and labeled  â€¢ Validation prevents incomplete submissions

## Day 1 — Story 047
- **Feature:** PSP Pricing Management
- **Parent Task:** Manual Entry
- **Task Name:** Zone Lookup Behavior
- **User Story:** As a Service Provider Specialist, I want the system to correctly detect zone IDs when entering them in forms so I donâ€™t accidentally assign records to the wrong zone.
- **Description:** Amber notes the form only recognized the zone when searched, not when typing the full zone ID. Designers must ensure the zone lookup supports exact ID entry, auto-completion, and error feedback.
- **Acceptance Criteria:** â€¢ Form supports entering exact zone ID  â€¢ Auto-complete shows valid zones  â€¢ Errors shown for invalid IDs

## Day 1 — Story 048
- **Feature:** PSP Pricing Management
- **Parent Task:** Record Identification
- **Task Name:** Display Human-Readable Zone IDs
- **User Story:** As a Service Provider Specialist, I want zone IDs to be displayed clearly so I can easily identify and select the correct zone when entering pricing.
- **Description:** Justin explains the zone ID is a concatenation of the vendor ID and pricing zone record ID. UI should show this clearly, ideally with tooltip explanations.
- **Acceptance Criteria:** â€¢ Zone IDs display in UI clearly  â€¢ Tooltips explain structure  â€¢ Zone picker supports search by ID or vendor

## Day 1 — Story 049
- **Feature:** Pricing Strategy
- **Parent Task:** DNUs
- **Task Name:** Mark Pricing Records or Zones as Do Not Use
- **User Story:** As a Service Provider Specialist, I want to mark zones or individual pricing records as Do Not Use so the pricing tool does not quote outdated or invalid rates.
- **Description:** Amber explains DNUs prevent incorrect pricing. UI needs clear toggles for: DNU vendor, DNU zone, and DNU individual product pricing. Each should visually warn users when active.
- **Acceptance Criteria:** â€¢ DNU options displayed clearly  â€¢ Pricing tool hides DNU records  â€¢ Tooltips explain why items are hidden  â€¢ Admins can override if needed

## Day 1 — Story 050
- **Feature:** Pricing Engine
- **Parent Task:** Vendor DNUs
- **Task Name:** Handle Vendor-Level Do Not Use Rules
- **User Story:** As a system user, I want vendor-level DNU to override all zones and pricing records so that deactivated vendors cannot be used accidentally.
- **Description:** Justin differentiates vendor DNUs from zone/product DNUs. UI should show vendor status clearly and disable selection in the pricing tool.
- **Acceptance Criteria:** â€¢ Vendor DNU blocks all associated records  â€¢ UI displays vendor status clearly  â€¢ Pricing tool prevents selection

## Day 1 — Story 051
- **Feature:** Pricing Engine
- **Parent Task:** Margin Display
- **Task Name:** Show Suggested Customer Price Based on Vendor Rate
- **User Story:** As an Account Manager or Coordinator, I want the UI to display suggested customer prices calculated from vendor rates so I can quote accurately.
- **Description:** Amber demonstrates that product pages show suggested prices based on embedded pricing logic. UI must replicate that logic inside CUBE with clear breakdown of margins.
- **Acceptance Criteria:** â€¢ Suggested price shown next to vendor rate  â€¢ Tooltip explains calculation  â€¢ Margin visible for transparency

## Day 1 — Story 052
- **Feature:** PSP Pricing Management
- **Parent Task:** Pricing Experiments
- **Task Name:** A/B Test Pricing Margins
- **User Story:** As a Pricing Manager, I want to designate pricing records as part of a test or control group so we can measure the effects of reduced margins on sales volume.
- **Description:** Amber explains prior experiments where PSP margins were altered. UI must include selection fields for Test Group vs Control Group and allow reporting.
- **Acceptance Criteria:** â€¢ UI provides test group selector  â€¢ Pricing tool applies correct margin rules  â€¢ Reports can filter by experiment type

## Day 1 — Story 053
- **Feature:** System Infrastructure
- **Parent Task:** Synchronization
- **Task Name:** Trigger Sync When Related Data Changes
- **User Story:** As a System Admin, I want record changesâ€”such as DNU status or zone updatesâ€”to sync correctly to the pricing tool even if those changes occur on related objects.
- **Description:** Justin explains Quickbase limitations: webhooks only fire on direct data changes, not lookup data. New system must trigger updates when related data changes.
- **Acceptance Criteria:** â€¢ System detects related-data changes  â€¢ Sync triggers automatically  â€¢ No stale pricing data in hub

## Day 1 — Story 054
- **Feature:** System Infrastructure
- **Parent Task:** Bulk Sync
- **Task Name:** Bulk-Trigger Webhook Sync
- **User Story:** As a Service Provider Specialist, I want an easy UI button to trigger sync updates on pricing zones or records after DNU or field changes.
- **Description:** Amber confirms this functionality is presently used manually. Designers need to provide a simple, visible sync button.
- **Acceptance Criteria:** â€¢ Sync button available  â€¢ Confirms success  â€¢ Sync covers all dependent objects

## Day 1 — Story 055
- **Feature:** System Infrastructure
- **Parent Task:** Bulk Sync
- **Task Name:** Clarify Sync Workflow
- **User Story:** As a Service Provider Specialist, I want the UI to clearly show when and why a manual sync is needed so I can perform updates confidently.
- **Description:** Amber describes that she already uses a bulk-sync approach. UI should clarify conditions requiring sync and display recent sync history.
- **Acceptance Criteria:** â€¢ Sync requirement clearly displayed  â€¢ History log visible  â€¢ Error handling included

## Day 1 — Story 056
- **Feature:** PSP Pricing Management
- **Parent Task:** Sync & Mass Update
- **Task Name:** Handle Large-Scale Pricing Changes
- **User Story:** As a Service Provider Specialist, I want a clear UI distinction between when to use grid edit versus when to use bulk-update/sync actions so I know the safest and most efficient method for updating many pricing records.
- **Description:** The discussion clarifies that grid edit is ideal for small updates, while the bulk-sync button is required for sweeping changes affecting hundreds of records. The new UI should visually communicate when each option is appropriate and prevent mistakes. A tooltip or helper panel should explain:  â€¢ When a user should use grid edit  â€¢ When bulk update is recommended  â€¢ Risks of accidentally editing too many records via grid edit  â€¢ Safeguards for high-volume actions
- **Acceptance Criteria:** â€¢ UI displays guidance text or tooltips explaining each method  â€¢ Bulk update button visually separated from grid edit  â€¢ Warnings appear before large updates (>50 records)  â€¢ Role-based restrictions enforced

## Day 1 — Story 057
- **Feature:** Product & Pricing Architecture
- **Parent Task:** Product Field Variability
- **Task Name:** Support Product-Specific Pricing Fields
- **User Story:** As a Product Designer, I want the system to dynamically show only relevant pricing fields for each product type so users arenâ€™t overwhelmed by irrelevant information.
- **Description:** Justin explains that pricing varies drastically across product categories. Toilets have sanitizer, containment, winterization fields; dumpsters have tonnage, disposal type, included days; fencing and storage have other unique fields. The UI must automatically adjust which pricing fields appear based on product type, preventing clutter and reducing errors.
- **Acceptance Criteria:** â€¢ UI hides irrelevant fields for each product type  â€¢ Required fields clearly marked per product  â€¢ Product type selection dynamically updates the form  â€¢ Metadata stored cleanly without bloating the main table

## Day 1 — Story 058
- **Feature:** Product & Pricing Architecture
- **Parent Task:** Shared vs Unique Fields
- **Task Name:** Clarify Shared vs Product-Specific Pricing Attributes
- **User Story:** As a Product Designer, I want the UI to visually separate standard pricing fields from product-specific metadata so users understand which fields always apply and which depend on the product.
- **Description:** Ezequiel and Justin discuss that every product shares core pricing fields (delivery, removal, rental daily/weekly/monthly) but also contains many unique fields. The UI should present a â€œCore Pricingâ€ section and a â€œProduct-Specific Pricingâ€ section to improve clarity.
- **Acceptance Criteria:** â€¢ UI sections clearly labeled  â€¢ Core fields always appear  â€¢ Product-specific section updates dynamically  â€¢ Fields grouped logically

## Day 1 — Story 059
- **Feature:** Product & Pricing Architecture
- **Parent Task:** Suggested Pricing Logic
- **Task Name:** Display Customer Suggested Price with Margin Breakdown
- **User Story:** As a Sales or Coordination user, I want the UI to clearly show how customer pricing is calculated from vendor pricing so I can quote confidently.
- **Description:** Justin explains customer pricing is always calculated based on vendor cost multiplied by defined margins. The UI must display:  â€¢ Vendor rate  â€¢ Margin %  â€¢ Suggested customer rate  â€¢ Optional explanation tooltip indicating formula
- **Acceptance Criteria:** â€¢ Suggested price displayed next to vendor cost  â€¢ Tooltip explains calculation  â€¢ Margin visible and editable based on permissions  â€¢ Suggested price updates in real time

## Day 1 — Story 060
- **Feature:** System Architecture
- **Parent Task:** Legacy Table Design
- **Task Name:** Visualize & Simplify Legacy Product Tables
- **User Story:** As a Developer or Designer, I want a clear visualization of the current 8-table Quickbase structure so I understand why the new system must consolidate and redesign the product schema.
- **Description:** Anthony and Justin explain that Quickbase limitations forced splitting product data across 8 separate tables (one per product type). UI/UX teams need context so the prototype doesnâ€™t accidentally replicate this flawed structure.
- **Acceptance Criteria:** â€¢ Documentation panel or design notes explain legacy structure  â€¢ UI does NOT replicate 8 tables  â€¢ Consolidated product model supports all product types

## Day 1 — Story 061
- **Feature:** System Architecture
- **Parent Task:** Storage Limitations
- **Task Name:** Support Scalable Data Storage (Avoid 500MB Limits)
- **User Story:** As a System Architect, I need the new system to avoid the limitations that forced Quickbase to split product tables so we can store all product data efficiently and scalably.
- **Description:** Justin documents that Quickbase tables max out at 500MB, causing the split. UI/UX must assume a unified architecture and design around consolidated views rather than table-specific screens.
- **Acceptance Criteria:** â€¢ No UI references â€œproduct table #1â€“#8â€  â€¢ Unified product dashboard  â€¢ Clean metadata structure for variable fields

## Day 1 — Story 062
- **Feature:** System Architecture
- **Parent Task:** Metadata Table Strategy
- **Task Name:** Store Product Metadata in a Dedicated Metadata Table
- **User Story:** As a System Architect, I want product-specific metadata stored in a separate table (e.g., JSON or structured fields) so product complexity does not bloat the main product table.
- **Description:** Dhaval suggests a product metadata table storing variable fields to avoid extreme table width. UI must read this metadata dynamically to render product-specific pricing fields.
- **Acceptance Criteria:** â€¢ Metadata table supports flexible structure  â€¢ UI dynamically renders fields based on metadata  â€¢ Clean API delivering metadata to front-end

## Day 1 — Story 063
- **Feature:** System Infrastructure
- **Parent Task:** History Log
- **Task Name:** Show Change History for Pricing Records
- **User Story:** As a Service Provider Specialist, I want the UI to show a clear change history for pricing records so I can audit who changed what and when.
- **Description:** Justin and Amber mention that Quickbase already tracks history, but itâ€™s inconsistent. The new UI must provide a clean timeline-style view of:  â€¢ Field changes  â€¢ Old vs new values  â€¢ User who made the change  â€¢ Timestamp  â€¢ Bulk update indicators
- **Acceptance Criteria:** â€¢ History visible on each pricing record  â€¢ Filters for date, user, field  â€¢ Support for bulk update grouping

## Day 1 — Story 064
- **Feature:** Pricing History & Auditability
- **Parent Task:** Delta Tracking
- **Task Name:** Display Pricing Change Deltas
- **User Story:** As a PSP Specialist, I want a clear visual interface showing pricing history changes with deltas so I can quickly understand what changed and why without digging through raw data.
- **Description:** Justin explains that Quickbase tracks pricing changes by showing old and new values, highlighting numerical differences. The UI needs to transform this into a user-friendly timeline-style interface.  The UI should:  â€¢ Clearly show old vs new prices  â€¢ Highlight deltas visually (color or bold)  â€¢ Group changes by pricing field (delivery, removal, rental, etc.)  â€¢ Provide timestamps for when changes occurred  â€¢ Allow PSP Specialists to quickly explain adjustments to accounting or customers
- **Acceptance Criteria:** â€¢ Timeline view displays old/new values & delta  â€¢ Highlighting draws attention to changed fields  â€¢ Users can filter by field (e.g., delivery, rental)  â€¢ History loads within <2 seconds  â€¢ No raw backend technical fields visible

## Day 1 — Story 065
- **Feature:** Pricing History & Auditability
- **Parent Task:** Export & Reference Needs
- **Task Name:** Make Pricing History Easily Exportable
- **User Story:** As a User, I want the pricing history to be easily exportable so I can share or review changes for accounting, billing disputes, and VM ticket investigations.
- **Description:** Ezequiel asks if pricing history must remain separated or exportable. Justin confirms itâ€™s informational, but necessary for referencing in billing disputes and provider disagreements.  UI must include an â€œExport Historyâ€ button to CSV or PDF for quick review.
- **Acceptance Criteria:** â€¢ Export button present in UI  â€¢ Export includes timestamps, user, old value, new value, delta  â€¢ Exports match on-screen data exactly  â€¢ PDF formatting preserves timeline structure

## Day 1 — Story 066
- **Feature:** Pricing History & Auditability
- **Parent Task:** Historical Tracking
- **Task Name:** Show Full Pricing Timeline for All Products
- **User Story:** As a PSP Specialist, I want each productâ€™s pricing timeline accessible within the UI so I can view how pricing evolved and track contextual reasons for changes.
- **Description:** Justin notes pricing history applies across all product types but Quickbase logging is inconsistent in some modules.  The new UI should unify presentation across products and ensure:  â€¢ Every productâ€™s pricing timeline is accessible  â€¢ Change events include timestamps  â€¢ Delta logic is applied uniformly  â€¢ Users can navigate older history easily
- **Acceptance Criteria:** â€¢ Timeline UI consistent across all product types  â€¢ Ability to scroll chronologically or filter  â€¢ History loads even for long timelines  â€¢ Clear indicators for big price shifts

## Day 1 — Story 067
- **Feature:** Pricing History & Auditability
- **Parent Task:** Global Logging Strategy
- **Task Name:** Define Unified Audit Log Strategy
- **User Story:** As a System Designer, I want a clearly defined audit logging strategy so the UI knows exactly what pricing change events to display and in what format.
- **Description:** Justin states audit logging varies by module today. Some tracking is turned off due to performance limitations.  The new system should centralize:  â€¢ What fields produce audit logs  â€¢ How deltas are calculated  â€¢ How old/new values are stored  â€¢ How history is displayed  The UI must rely on a predictable API response.
- **Acceptance Criteria:** â€¢ Audit events standardized and documented  â€¢ UI receives a unified structure (JSON)  â€¢ UI supports filtering, grouping, and bulk viewing  â€¢ No hidden fields needed to interpret logs

## Day 1 — Story 068
- **Feature:** Pricing History & Auditability
- **Parent Task:** Automated Change Capture
- **Task Name:** Ensure UI Reflects Automation-Captured Changes
- **User Story:** As a User, I want the UI to show automated history entries clearly so I understand the source of each change, even if no user manually edited the record.
- **Description:** Diego asks how history entries are created. Justin confirms every history entry is created automatically by an automation when any pricing field changes.  UI must show entries as automation-generated, including old/new values.
- **Acceptance Criteria:** â€¢ UI visually distinguishes automation events from manual ones  â€¢ â€œAutomation triggered by [User]â€ displayed  â€¢ All three values captured (old, new, delta)  â€¢ Automated events appear immediately

## Day 1 — Story 069
- **Feature:** Pricing History & Auditability
- **Parent Task:** Multi-Field Change Handling
- **Task Name:** Support 3-Field Delta Logic for Each Pricing Field
- **User Story:** As a Designer, I want the UI to display all three relevant values for each changed pricing field so users clearly understand the change.
- **Description:** Justin explains that each pricing change includes:  1. Old value  2. New value  3. Delta (calculated)  The UI must display these elegantlyâ€”ideally with:  â€¢ Old value in gray  â€¢ New value in bold  â€¢ Delta visually highlighted (color-coded)
- **Acceptance Criteria:** â€¢ All 3 values appear for every changed field  â€¢ Layout readable and uncluttered  â€¢ Mobile version supports stacked layout  â€¢ Delta color indicates increase/decrease

## Day 1 — Story 070
- **Feature:** PSP Ownership & Roles
- **Parent Task:** Ownership Visibility
- **Task Name:** Display PSP Specialist Ownership in UI
- **User Story:** As a PSP Specialist, I want the UI to clearly show who is responsible for each Service Provider so accountability and communication are smooth.
- **Description:** Diego asks about record ownership. Justin explains PSP Specialists own certain haulers and all of their associated pricing zones.  UI should display ownership prominently:  â€¢ PSP owner name  â€¢ Contact  â€¢ Assignment metadata  â€¢ Reassignment workflow (future enhancement)
- **Acceptance Criteria:** â€¢ Owner name visible on Service Provider profile  â€¢ Tooltip explains ownership responsibility  â€¢ Filters allow sorting by owner  â€¢ Ownership present in pricing records and zones

## Day 1 — Story 071
- **Feature:** Pricing History & Auditability
- **Parent Task:** User Identification
- **Task Name:** Show Which User Triggered Pricing Change
- **User Story:** As a User, I want the UI to show which person triggered a pricing change so I can understand context during escalations or accounting reviews.
- **Description:** Amber asks if the UI could show who triggered a change instead of always showing Justin (due to automation ownership).  UI enhancement needed:  â€¢ Show the actual user whose action triggered the automation  â€¢ Display both â€œtriggered byâ€ and â€œlogged by automationâ€
- **Acceptance Criteria:** â€¢ UI shows correct triggering user  â€¢ Automation owner not shown unless relevant  â€¢ Clear distinction between automation owner & triggering user

## Day 1 — Story 072
- **Feature:** Managed Vendors in Pricing
- **Parent Task:** Display Rules
- **Task Name:** Show Managed Vendor Pricing Logic
- **User Story:** As a UI/UX Designer, I need the interface to clearly show how pricing for managed (non-PSP) Service Providers is handled so users understand why pricing appears or is hidden in the tool.
- **Description:** Amber clarifies that pricing can be entered for a vendor even if they are not a PSP, because pricing helps evaluate performance and margins over time.  UI must show:  â€¢ PSP vs Managed labels  â€¢ Why pricing exists even if a vendor is not PSP-approved  â€¢ Context explaining managed vendor monitoring
- **Acceptance Criteria:** â€¢ UI labels: P = Premier, M = Managed, S = Statistical  â€¢ Managed vendor pricing visible only in fulfillment/service provider views  â€¢ Tooltips explain meaning of â€œManaged Pricingâ€

## Day 1 — Story 073
- **Feature:** Managed Vendors in Pricing
- **Parent Task:** User Permissions
- **Task Name:** Control Visibility of Managed Vendor Pricing
- **User Story:** As an Account Manager, I want the UI to hide managed vendor pricing unless I have permission so the pricing tool remains clean and accurate for my workflow.
- **Description:** Amber states managed pricing is NOT visible to Account Managers, only to fulfillment and SP teams.  UI must enforce:  â€¢ Different visibility per role  â€¢ Managed pricing indicators (M)  â€¢ Role-based view filtering
- **Acceptance Criteria:** â€¢ Managed pricing hidden from Account Managers  â€¢ Fulfillment/Service Provider views show P/S/M  â€¢ UI prevents accidental use of managed pricing

## Day 1 — Story 074
- **Feature:** Pricing Tool Enhancements
- **Parent Task:** Pricing Zone Icons
- **Task Name:** Display P / S / M Indicators in UI
- **User Story:** As a User, I want clear visual indicators (P, S, M) next to each vendor price so I immediately know what type of price I'm selecting.
- **Description:** Amber explains:  â€¢ P = Premier Service Provider  â€¢ S = Statistical Model  â€¢ M = Managed Vendor  UI must clearly show these in pricing results lists.
- **Acceptance Criteria:** â€¢ Indicator icons appear consistently on every pricing row  â€¢ Tooltip defines each symbol  â€¢ Indicators visible in all pricing tool modes (AM, Fulfillment, SP views)

## Day 1 — Story 075
- **Feature:** Pricing Adjustments
- **Parent Task:** Admin Tools
- **Task Name:** Surface Pricing Adjustment Rules in UI
- **User Story:** As a PSP Specialist, I want to see which pricing adjustments are currently active so I understand why the displayed price differs from base vendor pricing.
- **Description:** Dhaval explains the Pricing Adjustment Rules system:  â€¢ Increases/decreases by percentage or amount  â€¢ Apply to specific products, zip codes, PSPs, or statistical pricing  â€¢ Only a few rules are active in production  UI must show active adjustments and their effects.
- **Acceptance Criteria:** â€¢ Active adjustment rules displayed in a collapsible UI panel  â€¢ Adjustment impact calculated and shown on pricing rows  â€¢ â€œRule appliedâ€ tag shown under adjusted prices

## Day 1 — Story 076
- **Feature:** Pricing Adjustments
- **Parent Task:** Admin Workflow
- **Task Name:** Design UI for Creating Adjustment Rules
- **User Story:** As an Admin, I want a guided UI to create new pricing adjustment rules so I can safely modify system-wide pricing without errors.
- **Description:** Dhaval walks through rule creation:  UI must support:  â€¢ Naming a rule  â€¢ Priority selection  â€¢ Operation: increase/decrease  â€¢ Type: percentage or amount  â€¢ Geography selection (all-zips or specific zips)  â€¢ Pricing type selection (All, Statistical Only, PSP Only)  â€¢ Upload lists (e.g., PSP record IDs)  â€¢ Expiry dates  â€¢ Activation toggles
- **Acceptance Criteria:** â€¢ Form includes all fields with validation  â€¢ Prevents rule creation for â€œliveâ€ production conditions unless allowed  â€¢ Clear warning UX for risky changes  â€¢ Success confirmation on save

## Day 1 — Story 077
- **Feature:** Pricing Tool Enhancements
- **Parent Task:** System Alignment
- **Task Name:** Include Pricing Adjustments in Displayed Pricing
- **User Story:** As a User, I want the pricing tool to reflect adjustments so displayed prices always match real rules applied from the Adjustment Engine.
- **Description:** Dhaval explains that once rules are active, they modify the displayed prices automatically. UI must show:  â€¢ Final price after adjustment  â€¢ Breakdown: base price + rule  â€¢ Adjustment label at bottom of pricing table
- **Acceptance Criteria:** â€¢ Adjusted pricing calculation verified  â€¢ Visual indicator â€œAdjusted by Rule: [Rule Name]â€  â€¢ Users can expand/collapse rule impact detail

## Day 1 — Story 078
- **Feature:** Pricing Tool Enhancements
- **Parent Task:** Integration Planning
- **Task Name:** Ensure Pricing Tool Will Be Included in Cube MVP
- **User Story:** As a Product Owner, I want clarity on when the pricing tool and popup tool will be integrated into Cube so development teams can plan properly.
- **Description:** Anthony and Justin confirm the pricing tool is tightly integrated with PSP pricing and should be part of early Cube phases.  UI must be designed with future integration in mind.
- **Acceptance Criteria:** â€¢ Pricing tool workflow defined for MVP  â€¢ UI scoped alongside PSP pricing modules  â€¢ Dependencies documented

## Day 1 — Story 079
- **Feature:** Geographic Pricing Enhancements
- **Parent Task:** Map-Based Zones
- **Task Name:** Introduce Vector-Based Geographic Pricing Zones
- **User Story:** As a UI/UX Designer, I want to support drawing irregular service areas on a map so PSPs can define non-circular, non-zip-based pricing zones.
- **Description:** Justin describes future feature:  â€¢ Third pricing zone type (beyond radius & zip-list)  â€¢ â€œVector geographic selectable areaâ€  Use cases:  â€¢ Franchise limitations  â€¢ Unsafe regions  â€¢ Irregular service areas  UI must support interactive polygon drawing and editing.
- **Acceptance Criteria:** â€¢ Map tool supports polygon creation, editing, saving  â€¢ Zone stored as geo-coordinates  â€¢ Pricing tool correctly identifies address inside polygon

## Day 1 — Story 080
- **Feature:** Pricing Adjustments
- **Parent Task:** Rule Timing Controls
- **Task Name:** Add Start/End Dates for Pricing Adjustment Rules
- **User Story:** As an Admin, I want to configure pricing adjustment rules with both a start date and expiration date so that rules automatically activate and deactivate on schedule without manual intervention.
- **Description:** Diego questions whether rules can auto-disable after a fixed period. Anthony and Justin confirm rules currently have an expiration toggle but no defined start date. UI should support:  â€¢ Start date selector  â€¢ End/expiration date  â€¢ Status preview (â€œScheduledâ€, â€œActiveâ€, â€œExpiredâ€)  â€¢ Automatic activation/deactivation handling
- **Acceptance Criteria:** â€¢ Date pickers validated  â€¢ Rule state displayed in UI  â€¢ System automatically toggles Active = Yes/No based on dates

## Day 1 — Story 081
- **Feature:** Pricing Adjustments
- **Parent Task:** Admin Validation
- **Task Name:** Prevent Accidental Save on Live Rules
- **User Story:** As an Admin, I want the UI to prevent accidental saving of live pricing adjustment rules so that no unintended global price changes occur.
- **Description:** Justin panics when Amber nearly saves a rule. UI must add:  â€¢ â€œAre you sure?â€ modal for live rule edits  â€¢ Warning banner for production rules  â€¢ Save button disabled until user acknowledges risk
- **Acceptance Criteria:** â€¢ Warning modal appears for high-impact actions  â€¢ Save disabled unless confirmed  â€¢ UI logs admin confirmation

## Day 1 — Story 082
- **Feature:** Pricing Adjustments
- **Parent Task:** Migration Strategy
- **Task Name:** Move Pricing Adjustments Into Cube
- **User Story:** As a Product Owner, I want pricing adjustments migrated into Cube so pricing logic is centralized and we avoid maintaining duplicate logic in Hub.
- **Description:** Dhaval and Anthony explain:  â€¢ Pricing Adjustments currently sit on Hub (a layer over QuickBase values).  â€¢ Cube will eventually own pricing + adjustments + pop-up tool.  â€¢ Hub will be limited to AR/AP only.  UI design must anticipate this migration.
- **Acceptance Criteria:** â€¢ All adjustment-related UI mapped in Cube  â€¢ Duplicate logic eliminated  â€¢ Migration dependencies identified

## Day 1 — Story 083
- **Feature:** Pricing Tool Future Enhancements
- **Parent Task:** Address-Triggered Pricing
- **Task Name:** Auto-Display Pricing When Address is Entered
- **User Story:** As a User, I want pricing to appear automatically as soon as I enter a site address so I donâ€™t need to open a separate pricing tool window.
- **Description:** Justin describes future UX vision:  â€¢ User enters address  â€¢ System immediately detects vendor zones  â€¢ Pricing loads instantly before product selection  â€¢ Full results visible inline  Goal: Remove the separate pricing tool window entirely.
- **Acceptance Criteria:** â€¢ UI loads pricing automatically on address entry  â€¢ Results appear inline without any additional clicks  â€¢ No separate modal/page required

## Day 1 — Story 084
- **Feature:** Pricing Adjustments
- **Parent Task:** Rule History Tracking
- **Task Name:** Display Which Rules Were Applied to Saved Prices
- **User Story:** As a User, I want to know which pricing adjustment rule affected a saved customer quote so I can understand how the price was calculated when reviewing past records.
- **Description:** Dhaval explains that currently once prices are saved, the UI provides **no retroactive visibility** of the rule that modified them.  UI must:  â€¢ Display â€œApplied Adjustment: [Rule Name]â€  â€¢ Store adjusted + non-adjusted values  â€¢ Allow auditing months later
- **Acceptance Criteria:** â€¢ Saved pricing record displays:   â€“ Base vendor price   â€“ Adjusted price   â€“ Applied rule name  â€¢ Historical quotes show rule context

## Day 1 — Story 085
- **Feature:** Pricing Tool Workflow
- **Parent Task:** Quote Lifecycle
- **Task Name:** Clarify How Quotes Are Saved After Giving Prices to Customers
- **User Story:** As a UI/UX Designer, I need to ensure the quote-saving workflow supports real user behavior so pricing is captured consistently for follow-ups.
- **Description:** Amber and Justin clarify workflow:  â€¢ Quotes are saved almost every time a price is given verbally  â€¢ Saved even if customer has not agreed  â€¢ Helps during callbacks (â€œYou quoted me yesterdayâ€¦â€)  â€¢ Exception: when AM rattles off multiple prices and customer rejects all  UI must support saving quotes quickly and consistently.
- **Acceptance Criteria:** â€¢ Save button always available at pricing moment  â€¢ UI confirms price saved  â€¢ Quick history access for AM callbacks

## Day 1 — Story 086
- **Feature:** Product Tables Architecture
- **Parent Task:** Data Model Strategy
- **Task Name:** Decide on Replication Strategy for Product Tables
- **User Story:** As a Developer, I want clarity on how product tables will be replicated across modules so performance remains high and dependencies remain stable.
- **Description:** Justin clarifies:  â€¢ Sales Management product tables and Vendor Pricing product tables are exact replicas  â€¢ Replication chosen for performance reasons  â€¢ Only unique data per module is: pricing zones + merged product pricing + history  UI considerations: modules referencing products must show product metadata locally without API lag.
- **Acceptance Criteria:** â€¢ Clear replication strategy defined  â€¢ UI read operations do not depend on remote modules  â€¢ Product tables kept lightweight and synced

## Day 1 — Story 087
- **Feature:** Architecture Planning
- **Parent Task:** Performance Design
- **Task Name:** Replicate Static Product Tables Across Modules
- **User Story:** As a Systems Designer, I want static product master tables replicated across all modules that reference them so the UI loads instantly without cross-service calls.
- **Description:** Justin explains:  â€¢ Product master, product codes, product types, haulers are small + mostly static  â€¢ Replicating these avoids single-point-of-failure  â€¢ Needed in: Pricing Tool, Hauler Module, Sales Module, Accounting Module  â€¢ UX gains: faster dropdowns, instant product lookup, no network delay
- **Acceptance Criteria:** â€¢ Replicated tables consistent across modules  â€¢ Sync jobs validated  â€¢ No module depends on remote product lookups

## Day 1 — Story 088
- **Feature:** Architecture Planning
- **Parent Task:** Design Decisions
- **Task Name:** Determine Whether Pricing Lookup Uses Replication or API
- **User Story:** As a Developer, I want clarity on whether pricing (especially zip-specific pricing) should be retrieved via replicated tables or centralized API services.
- **Description:** Jose suggests an API for looking up zip-based pricing.  Team discusses:  â€¢ API possible  â€¢ Replication likely preferred for reliability + speed  â€¢ Discussion deferred to architecture review.
- **Acceptance Criteria:** â€¢ API vs Replication discussion documented  â€¢ Decision matrix created  â€¢ UX considerations mapped for both paths

## Day 1 — Story 089
- **Feature:** Architecture Planning
- **Parent Task:** Architecture Alignment
- **Task Name:** Confirm Replication Strategy for Cube
- **User Story:** As a Developer, I need final confirmation whether Cube will always replicate static product tables to avoid bottlenecks across modules.
- **Description:** Dhaval and Justin confirm:  â€¢ Product metadata is extensive + may require multiple discussions  â€¢ Replication is strongly preferred  â€¢ Cube should replicate all static tables for performance safety.
- **Acceptance Criteria:** â€¢ Replication strategy documented  â€¢ UI reflects local product metadata  â€¢ No API latency in UI interactions

## Day 1 — Story 090
- **Feature:** PSP Workflow & Meeting Flow
- **Parent Task:** Meeting Planning
- **Task Name:** Decide Whether to Review All Product Pricing Fields
- **User Story:** As a UX Facilitator, I want clarity on whether devs need the deep field-by-field walkthrough of every pricing type so the session stays efficient and focused.
- **Description:** Team discusses whether to review every granular pricing field (days included, roll-off metadata, product-specific data). Dhaval recommends postponing. Amber expresses fatigue. Decision: deprioritize and continue with higher-level flows.
- **Acceptance Criteria:** â€¢ Decision recorded in session  â€¢ Next steps clarified for product-field deep dive  â€¢ UX notes updated

## Day 1 — Story 091
- **Feature:** PSP Workflow & Meeting Flow
- **Parent Task:** Agenda Alignment
- **Task Name:** Confirm Focus on Flows Over Field-Level Details
- **User Story:** As a Product Owner, I want to keep the workshop focused on the main user flows instead of diving into all product metadata so devs stay aligned and productive.
- **Description:** Justin asks whether to skip the granular field-level walkthrough. Dhaval and Amber agree to defer. Team decides to focus on workflows, not individual field definitions.
- **Acceptance Criteria:** â€¢ Agenda updated  â€¢ Consensus captured  â€¢ UX scope adjusted

## Day 1 — Story 092
- **Feature:** PSP Workflow & Meeting Flow
- **Parent Task:** Time Management
- **Task Name:** Communicate Need to Continue Meeting Despite Fatigue
- **User Story:** As a Facilitator, I want to ensure the workshop stays on schedule even if participants are tired so we complete the high-priority topics.
- **Description:** Amber jokes about fatigue. Justin reminds her more PSP content still needs to be covered. Anthony suggests alternate scheduling to reduce overload.
- **Acceptance Criteria:** â€¢ Participants aligned on expectations  â€¢ Time constraints acknowledged

## Day 1 — Story 093
- **Feature:** PSP Workflow & Meeting Flow
- **Parent Task:** Scheduling
- **Task Name:** Resolve Conflict With Weekly PSP Meeting
- **User Story:** As a User, I want clarity on whether to attend overlapping meetings so I can prioritize the correct session.
- **Description:** Amber mentions the weekly PSP meeting starting soon. Justin directs the team to skip it because this dev workshop has priority. Anthony supports the decision.
- **Acceptance Criteria:** â€¢ Clear instruction given  â€¢ Calendar conflict resolved

## Day 1 — Story 094
- **Feature:** Break Management
- **Parent Task:** Time Block
- **Task Name:** Schedule a Short Break for the Team
- **User Story:** As a Participant, I want a scheduled break so I can return refreshed and continue learning effectively.
- **Description:** Anthony proposes a break. Justin and Alkhely agree. Team schedules a break until 10 minutes past the hour.
- **Acceptance Criteria:** â€¢ Break time announced  â€¢ Participants notified

## Day 1 — Story 095
- **Feature:** Internal Communication
- **Parent Task:** Informal Communication
- **Task Name:** Accommodate Team Banter During Breaks to Maintain Morale
- **User Story:** As a Designer, I want to understand natural team communication patterns so UI messaging and in-app workflows match real-world tone and culture.
- **Description:** Team jokes about smoking and break habits. Shows informal culture. Useful for crafting microcopy, error tone, and training materials.
- **Acceptance Criteria:** â€¢ Cultural tone documented  â€¢ UX notes updated

## Day 1 — Story 096
- **Feature:** Meeting Resumption
- **Parent Task:** Workshop Continuation
- **Task Name:** Resume Session After Break With Updated Context
- **User Story:** As a Facilitator, I want the team aligned on who is presenting next so the workshop flows smoothly.
- **Description:** Justin returns, reports issue with invite recipients missing the meeting. Clarifies that Amber will soon hand off to Pilar. Ensures no confusion.
- **Acceptance Criteria:** â€¢ Next presenter identified  â€¢ Missing-invite issue acknowledged

## Day 1 — Story 097
- **Feature:** Hauler Module UX
- **Parent Task:** Hauler Record UX
- **Task Name:** Introduce Hauler Page for PSP Discussion
- **User Story:** As a UX Designer, I want to understand the structure of the hauler page so I can design an intuitive layout for managing provider data.
- **Description:** Pelar begins walkthrough of a sample hauler:  â€¢ Shows provider name conventions  â€¢ Address, phone, state  â€¢ Provider specialist  â€¢ PSP flags (authorized, COI, W9)  â€¢ Yellow pricing-related flag
- **Acceptance Criteria:** â€¢ All hauler page components identified  â€¢ UI sections mapped  â€¢ Data groups understood

## Day 1 — Story 098
- **Feature:** Compliance & Documentation
- **Parent Task:** Compliance Requirements
- **Task Name:** Explain Mandatory COI and W9 Requirements
- **User Story:** As a User, I want to understand why COI and W9 are required so I know what must exist before a hauler becomes usable.
- **Description:** Justin explains:  â€¢ W-9 = tax identity requirement  â€¢ COI = certificate of insurance for liability protection  â€¢ Both must be on file for hauler to be â€œauthorizedâ€  â€¢ Required for all vendors regardless of PSP status
- **Acceptance Criteria:** â€¢ UI must enforce W9 + COI requirement  â€¢ Must display missing documents clearly  â€¢ Tooltips or helper text explain requirements

## Day 1 — Story 099
- **Feature:** Hauler Compliance & COI UX
- **Parent Task:** Compliance Rules
- **Task Name:** Display & Validate COI Requirements
- **User Story:** As a Compliance User, I want the UI to clearly surface required COI coverage fields so I can quickly verify whether a hauler meets minimum insurance criteria.
- **Description:** Pelar explains COI rules: hauler must carry General Aggregate coverage; must list ZTERS as certificate holder; must include authorized signature. UI must display these clearly and prevent approval without them.
- **Acceptance Criteria:** â€¢ General Aggregate coverage field visible and mandatory  â€¢ Certificate Holder field visible and mandatory  â€¢ COI Signature required  â€¢ UI blocks authorization if missing

## Day 1 — Story 100
- **Feature:** Hauler Page UX
- **Parent Task:** Information Layout
- **Task Name:** Show Pricing Notes & Required Flags
- **User Story:** As a UI Designer, I need to display pricing-related caution flags so users know when they must review notes before using a hauler.
- **Description:** Yellow 'pricing notes' flag indicates mandatory review. UI must highlight this to avoid missed context.
- **Acceptance Criteria:** â€¢ Yellow flag appears when pricing notes exist  â€¢ Tooltip or modal shows required notes  â€¢ Flag clears when no actionable notes remain

## Day 1 — Story 101
- **Feature:** Hauler Operational UX
- **Parent Task:** Service Attribute Fields
- **Task Name:** Display Hauler Capabilities (Miles, Same-Day, Expedited)
- **User Story:** As a Fulfillment User, I want to quickly see whether a hauler offers same-day delivery and how far they will travel so I can select the right hauler for urgent orders.
- **Description:** UI fields show willingness to travel, max miles, same-day availability, expedited delivery options.
- **Acceptance Criteria:** â€¢ Fields present & readable  â€¢ If not willing to travel, UI indicates constraint  â€¢ Filtering available via these fields

## Day 1 — Story 102
- **Feature:** Hauler Contact Management
- **Parent Task:** Contact Drawer
- **Task Name:** Support Multiple Contact Types with Preferred Communication
- **User Story:** As a Fulfillment Rep, I want clearly organized hauler contacts with preferred communication methods so I know exactly who to call for each need.
- **Description:** Pelar describes contact fields: primary contact, secondary, dispatch, accounting, PSP contacts, after-hours, etc. Preferred comms may be Email or Phone depending on user profile.
- **Acceptance Criteria:** â€¢ UI allows multiple contacts with type labels  â€¢ Preferred communication displayed visually  â€¢ Contact hierarchy clear (dispatch > primary > secondary)

## Day 1 — Story 103
- **Feature:** Hauler Contact Form
- **Parent Task:** Contact Creation
- **Task Name:** Provide a Simple Form to Add Hauler Contacts
- **User Story:** As a User, I want an intuitive form for adding new hauler contacts so I can maintain accurate provider info.
- **Description:** Form allows: contact type, name, title, phone, email, preferred method. Saves into contact table and appears immediately on UI.
- **Acceptance Criteria:** â€¢ Required fields validated  â€¢ Saves to correct hauler  â€¢ Contact appears in list instantly

## Day 1 — Story 104
- **Feature:** Data Model Modernization
- **Parent Task:** Field Consolidation
- **Task Name:** Convert Legacy Contact Fields Into Contact Records
- **User Story:** As a Developer, I want to remove outdated hauler-level contact fields so all contacts live in a single unified table.
- **Description:** Justin explains old legacy fields (contact, secondary phone, dispatch, etc.) must be removed and converted into individual contact records during Cube migration.
- **Acceptance Criteria:** â€¢ Conversion script maps old fields to new contact records  â€¢ Legacy fields no longer displayed in UI  â€¢ All data preserved

## Day 1 — Story 105
- **Feature:** Hauler Notes UX
- **Parent Task:** Notes UX
- **Task Name:** Display, Categorize, and Archive Hauler Notes
- **User Story:** As a User, I want to view, archive, and categorize notes so hauler history is accessible without cluttering active information.
- **Description:** Pelar shows: active notes, archived notes, note types like pricing issue, onboarding notes, PSP notes. She archives a Net 30 term note from onboarding.
- **Acceptance Criteria:** â€¢ Archiving moves note to Archive section  â€¢ Active view only shows active notes  â€¢ UI prevents confusion over outdated info

## Day 1 — Story 106
- **Feature:** Financial Terms UX
- **Parent Task:** Payment Terms
- **Task Name:** Explain and Display Net 30 Behavior
- **User Story:** As a User, I want clear visibility into Net 30 terms so I understand when haulers must be paid.
- **Description:** Pelar clarifies Net 30: payment due 30 days after delivery. Invoices submitted with PO. Accounting pays on net terms.
- **Acceptance Criteria:** â€¢ Net term shown on UI  â€¢ Tooltip or helper text explains term  â€¢ Must be editable by PSP team

## Day 1 — Story 107
- **Feature:** Notes Archiving Logic
- **Parent Task:** Note Type Handling
- **Task Name:** Ensure â€˜Archiveâ€™ Note Type Is Not Confused With System Archiving
- **User Story:** As a UX Architect, I want separate concepts for â€˜Note Type: Archiveâ€™ vs. â€˜System Archiveâ€™ so users donâ€™t misunderstand how data is stored.
- **Description:** Justin explains:  (1) Archive note type = moves note out of primary view  (2) System archive = strips text & writes to CSV to reduce table size  These are not the same.
- **Acceptance Criteria:** â€¢ UI differentiates Archive Note Type from System Archive  â€¢ System archive not user-triggered  â€¢ Note type doesnâ€™t delete data

## Day 1 — Story 108
- **Feature:** Rich Text Controls
- **Parent Task:** Rich Text Limitations
- **Task Name:** Implement Limited Rich Text Formatting to Prevent UI Abuse
- **User Story:** As a UX Designer, I want controlled rich-text formatting so notes can be readable without users creating giant, disruptive blocks of text.
- **Description:** Justin: Quickbase allows absurd formatting (256pt red text). Cube must limit font sizes and formatting but still support styled notes.
- **Acceptance Criteria:** â€¢ Font sizes capped (e.g., max 48â€“72pt)  â€¢ No oversized colors or page-breaking content  â€¢ Old notes safely converted

## Day 1 — Story 109
- **Feature:** Hauler Status UX
- **Parent Task:** Color Indicators
- **Task Name:** Use Color Codes (Green/Yellow) to Indicate Hauler Readiness
- **User Story:** As a User, I want clear visual color coding so I can instantly see hauler readiness or warning conditions.
- **Description:** Yellow = caution / required attention; green = ready/clean. UI must maintain this clarity.
- **Acceptance Criteria:** â€¢ Indicator colors standardized  â€¢ Hover explains indicator meaning  â€¢ Applies across hauler-related UI

## Day 1 — Story 110
- **Feature:** High-Density UI Layout
- **Parent Task:** Information Density
- **Task Name:** Support Large Amounts of Hauler Data Without Overwhelming Users
- **User Story:** As a UI Architect, I want a layout that can handle the hauler pageâ€™s large data footprint so information remains scannable.
- **Description:** Justin describes hauler page as one of the most data-dense screens: many tabs, notes, contacts, pricing, compliance. Requires thoughtful grouping and navigation.
- **Acceptance Criteria:** â€¢ Tabs logically grouped  â€¢ Sticky headers  â€¢ Collapsible sections for heavy data

## Day 1 — Story 111
- **Feature:** Hauler Availability UX
- **Parent Task:** Hauler Page â€“ Availability Management
- **Task Name:** View Stock Notices for a Hauler
- **User Story:** As a Fulfillment or PSP User, I want a clear Stock Notices section on the hauler page so I can quickly see which product sizes may be unavailable before I quote or schedule.
- **Description:** Pelar describes using Stock Notices to flag potential outages (e.g., 40-yard dumpsters in high demand, only one unit available and going on rent) and instructing internal users to call for availability before promising product to customers; users check this section regularly and it must clearly show notice date, creator, description, and affected products.
- **Acceptance Criteria:** Stock notices are visible on the hauler page in a dedicated area; each notice shows created date, creator, affected product types or sizes, and short instructions (e.g., call for availability); notices are sorted by recency and clearly distinguished from other notes; users can immediately tell if a hauler has any active stock constraints.

## Day 1 — Story 112
- **Feature:** Hauler Availability UX
- **Parent Task:** Hauler Page â€“ Availability Management
- **Task Name:** Create and Maintain Ongoing Stock Notices
- **User Story:** As a PSP Specialist, I want to create stock notices with start dates and an explicit way to mark them as ongoing so I can track shortages that do not yet have a known end date.
- **Description:** When creating a new stock notice, the current system forces both a start and end date even if the end date is unknown; Pelar works around this by entering a placeholder end date (e.g., 10/28) and then manually following up weekly by email or phone with the owner to ask about availability, which is error-prone and not explicit in the UI.
- **Acceptance Criteria:** Stock notice form allows start date and either a real end date or a selectable 'ongoing' flag; if 'ongoing' is selected, the system does not require an artificial end date; ongoing notices are visually indicated (e.g., badge or label) so users know the shortage is still in effect until explicitly closed.

## Day 1 — Story 113
- **Feature:** Hauler Availability UX
- **Parent Task:** Hauler Page â€“ Availability Management
- **Task Name:** Track Follow-Up and Closure of Stock Notices
- **User Story:** As a PSP Specialist, I want a structured follow-up and verification workflow for stock notices so we only show active, confirmed shortages to internal users.
- **Description:** Justin explains there is currently no explicit verification process: the team manually follows up to see when items are back in stock but the system only has start and end dates; there is no status to indicate 'verified resolved' versus 'still pending review,' so outdated stock notices may remain visible longer than they should.
- **Acceptance Criteria:** Stock notices have a status lifecycle (e.g., Draft, Active, Needs Verification, Resolved); system can track last follow-up date and who updated it; resolved notices no longer appear as active on the hauler page but remain historically accessible; optional reminders can highlight notices that have not been re-verified within a defined period.

## Day 1 — Story 114
- **Feature:** Pricing Tool Integration
- **Parent Task:** PSP Pricing Integration
- **Task Name:** Hide Out-of-Stock Products in Pricing Tool Based on Stock Notices
- **User Story:** As a Sales or Fulfillment User, I want the pricing tool to automatically hide or mark out-of-stock products for a hauler when a stock notice exists so I donâ€™t waste time quoting something the vendor cannot provide.
- **Description:** Justin notes a current disconnect: stock notices and PSP pricing are separate; pricing tool still shows the PSPâ€™s top suggested price (e.g., 20-yard) even when a stock notice says that size is out of stock; this wastes time and causes internal calls asking if the hauler truly has inventory.
- **Acceptance Criteria:** Stock notices are linked to product types and specific PSP pricing records; when a product is flagged out-of-stock, its pricing is either hidden or clearly marked as unavailable in the pricing tool (e.g., via DNU flag or 'Out of Stock' badge); when the notice is resolved, pricing visibility is restored automatically; behavior is consistent across all views.

## Day 1 — Story 115
- **Feature:** Hauler Services & History
- **Parent Task:** Hauler Page â€“ Service Overview
- **Task Name:** View Product Lines and Historical Volume for a Hauler
- **User Story:** As a PSP Specialist or Vetting Analyst, I want a Services tab that shows which product lines a hauler carries and their historical and active volume so I can vet them and compare pricing performance over time.
- **Description:** Pelar shows the Services section displaying which product lines are supported (e.g., toilets, roll-offs, containers) and a grid of active, removed, and pending orders; the team uses this daily for price comparisons, PSP vetting, and cross-checking quarterly sales reports to confirm numbers match system data.
- **Acceptance Criteria:** Services tab clearly shows product-line checkboxes and per-line counts of historical, active, removed, and pending items; users can drill into historical records to see how many of each product type have been used; this data can be cross-referenced with quarterly sales reports; new PSPS can be evaluated using these counts.

## Day 1 — Story 116
- **Feature:** Hauler Services & History
- **Parent Task:** Hauler Page â€“ Service Overview
- **Task Name:** Display Office Hours and Order Cutoff Rules for Scheduling
- **User Story:** As a Fulfillment Rep, I want office hours and order cutoff times displayed for each hauler so I can schedule deliveries and calls at appropriate times.
- **Description:** Pelar explains that office hours indicate when phones will be answered (e.g., 7:00â€“17:00) even though trucks may operate earlier; an order cutoff time (e.g., 2:00 PM) defines the latest time to request next-day delivery; closed days (e.g., Sunday) are also shown so reps know when haulers wonâ€™t respond.
- **Acceptance Criteria:** Hauler page shows clearly formatted office hours per weekday, order cutoff time, and closed days; this information is visible to anyone scheduling orders; help text clarifies that deliveries may occur outside office hours but calls and coordination must respect these times.

## Day 1 — Story 117
- **Feature:** Hauler Services & History
- **Parent Task:** Hauler Page â€“ Service Overview
- **Task Name:** View Fulfillment Tickets and Order History for a Hauler
- **User Story:** As an Operations or PSP User, I want a view of all fulfillment tickets and their notes for a hauler so I can review their operational history and performance.
- **Description:** Pelar describes the Fulfillment tab as a historical list of tickets completed for the provider, including services, removals, deliveries, and quote requests; each entry has notes; there are many pages of records, giving a long operational history; much of this mirrors data already exposed under Services but filtered from a ticket perspective.
- **Acceptance Criteria:** Fulfillment tab lists all relevant tickets for the hauler with type, date, product, and notes; users can paginate through history and open a ticket to see full operational details; the view is read-only and optimized for review rather than data entry; it complements the Services view by focusing on ticket-level history.

## Day 1 — Story 118
- **Feature:** Quotes & Status UX
- **Parent Task:** Quote Model Clarification
- **Task Name:** Clarify Quote Meanings Across Product and Fulfillment Contexts
- **User Story:** As a Developer or Analyst, I want a clear model of what â€˜quoteâ€™ means in the system so I can design UIs and reports that distinguish product quote status from quote request tickets.
- **Description:** Justin explains that 'quote' is overloaded: a product can have statuses like sale, canceled, quote in progress, or hauler quote; separately, a Fulfillment ticket type can also be a quote request sent to operations to obtain pricing from a vendor; reports may show either quote-status products or quote-request fulfillment tickets, so the UI must make these distinctions obvious.
- **Acceptance Criteria:** UI and data model clearly separate product status (e.g., quote in progress) from fulfillment ticket type (quote request); labels, filters, and column headers distinguish these contexts; reports indicate whether they are listing quote-status products, quote tickets, or both; tooltips or documentation reinforce the difference.

## Day 1 — Story 119
- **Feature:** Quotes & Status UX
- **Parent Task:** Quote Model Clarification
- **Task Name:** Differentiate Vendor-Side Quotes from Customer-Side ARQ Quotes
- **User Story:** As a Product Designer, I want vendor-side quotes clearly separated from ARQ customer quotes so users donâ€™t confuse internal vendor pricing workflows with customer-facing quoting processes.
- **Description:** Anthony clarifies that the quotes being discussed on the hauler page are on the provider/vendor side and are not the same as ARQ quotes given to customers; Justin confirms that ARQ is customer-facing and separate, where the customer only sees the customer price and may never know which vendor is used.
- **Acceptance Criteria:** UI clearly labels vendor-side quote objects as hauler/vendor quotes and customer-side ARQ quotes as customer quotes; navigation between modules makes this separation obvious; ARQ UI does not expose vendor quote fields; cross-links, if any, are one-way and read-only for context.

## Day 1 — Story 120
- **Feature:** Hauler Management & Vendor Workflow
- **Parent Task:** Vendor/Product Relationship Logic
- **Task Name:** Quote & Product Association Rules
- **User Story:** As a specialist or developer, I want the system to clearly differentiate and visualize how quote requests attach to multiple haulers but only one hauler becomes the selected vendor for the actual product, so that users always understand the relationship between quotes, fulfillment tickets, and vendor selection.", "When a quote request is sent to multiple haulers, all of them appear attached to the fulfillment ticket, but ONLY the selected hauler appears as the vendor on the product itself. The UI must make this distinction visually obvious and prevent confusion between customer quotes (ARQ) and vendor quote requests. The system should clearly label that the pricing shown on vendor quotes represents what the vendor charges ZTERSâ€”not customer pricing. This row captures the logic described by Justin and Pelar regarding how multiple haulers may be contacted but only one becomes the chosen vendor for the product.
- **Acceptance Criteria:** 1. The system must display all haulers contacted in a quote request under fulfillment, but highlight only the selected vendor under the product's hauler field. 2. The UI must differentiate between (a) vendor quote request tickets and (b) customer quotes (ARQs). 3. Vendor pricing displayed must be clearly labeled as internal ZTERS cost. 4. When a vendor is selected, their association must be reflected only on the productâ€”not on other haulers contacted earlier. 5. No confusion should exist in the interface between quote statuses, fulfillment tickets, or product/hauler relationships.

## Day 1 — Story 121
- **Feature:** Vendor Management & Compliance
- **Parent Task:** Price Increase Logging
- **Task Name:** Automated Price Increase Integration
- **User Story:** As a specialist, I want a streamlined UI for logging vendor price increases and the system to automatically apply those increases across all affected pricing zones, so that I no longer need to manually update every individual PSP pricing record.
- **Description:** Price increases are currently logged manually in Quickbase and require specialists to update every PSP zone individually. Pelar described how haulers frequently send new pricing (e.g., $3 per ton increases or holiday surcharges). Justin emphasized major system gaps: there is no automated update, no end-date verification, and updates require editing dozens of pricing rows zone-by-zone. The desired experience is: the user enters a price increase, selects affected products (e.g., all roll-offs), enters amount or percentage, and Cube automatically updates all pricing records. Users also need the ability to log start dates, optional end dates (for holiday surges), and see the applied increases. The UI must remove opportunities for manual typos, which currently cause major margin miscalculations.
- **Acceptance Criteria:** 1. When a price increase is entered, the system must apply it automatically to all applicable pricing records (zones + products) without requiring manual edits. 2. UI must provide a selector for affected product categories (e.g., roll-offs). 3. User must enter an effective date and optionally an end date; UI must warn if no end date is provided. 4. System must show clear confirmation of all updated pricing values. 5. UI must clearly label this as vendor-to-ZTERS pricing, not customer pricing. 6. Manual editing of each zone should no longer be required. 7. The update must be logged and visible in the vendor's change history.

---

# Day 2

**Stories:** 148

## Day 2 — Story 001
- **Epic:** Vendor Management - Setup & Onboarding
- **Feature:** Hauler Creation Workflow
- **Parent Task:** Hauler Onboarding
- **Task Name:** Create New Hauler Record
- **User Story:** As a VM Specialist, I want a guided UI workflow that ensures all required fields are validated during hauler creation so that inconsistent or incomplete hauler data cannot be entered.
- **Description:** The team discusses that certain naming conventions and minimum required fields must be adhered to when creating a new hauler. Currently much relies on manual user discipline. Developers indicate some of this could be enforced programmatically. This story establishes a structured, enforced workflow for creating a new hauler record.
- **Acceptance Criteria:** - UI shows a dedicated 'Create Hauler' flow with clearly marked required fields. - Name format validation enforced (e.g., standardized naming pattern). - Phone, email, service area, and COI/W9 placeholders must be completed before a hauler can be saved. - If any required field is missing, the user receives inline error messaging.

## Day 2 — Story 002
- **Epic:** Vendor Management - Dashboard & Reporting
- **Feature:** Dashboards
- **Parent Task:** Operational Visibility
- **Task Name:** Team Dashboard Requirements
- **User Story:** As a VM Specialist, I need a dashboard that summarizes my daily KPIs, outstanding reviews, tasks, and required actions so that I can operate efficiently without searching multiple tabs.
- **Description:** Conversation reveals that VM specialists and PSP team members lack meaningful dashboards. They currently have no consolidated visibility into outstanding tasks, follow-ups, or KPIs. This story captures the requirement for a unified dashboard at login.
- **Acceptance Criteria:** Dashboard displays: overdue items, pending COI/W9, active pricing updates, onboarding items needing verification, PSP reviews, and VM tickets requiring action. -@ Dashboard Data refreshes automatically. - Filters for date ranges, hauler type, and task type.

## Day 2 — Story 003
- **Epic:** Vendor Management - Pricing Tool Enhancements
- **Feature:** Pricing Display Logic
- **Parent Task:** Price Rounding
- **Task Name:** Rounding PSP Display Prices
- **User Story:** As a system user, I want PSP pricing displayed rounded up to the nearest $5 increment so that customer-facing and internal pricing appears clean and standardized.
- **Description:** Team discusses recent OPS request: PSP pricing should round up to the next $5 increment (e.g., $24.20 â†’ $25). Devs confirm a card exists for this. Create user story for implementation.
- **Acceptance Criteria:** - PSP pricing values shown in UI must always round up to next $5 increment. - Does NOT alter stored raw hauler pricing. - A tooltip icon provides explanation of rounding logic.

## Day 2 — Story 004
- **Epic:** Vendor Management - Learning & Orientation
- **Feature:** PSP Understanding
- **Parent Task:** Education
- **Task Name:** PSP Concept Clarification
- **User Story:** As a new developer, I want a clear UI explanation of what PSP status means so I can understand how PSP designation affects pricing, quoting, and vendor selection.
- **Description:** Developers admit they previously misunderstood PSP, assuming it meant 'premium pricing' rather than internal designation of preferred haulers. System should improve clarity via UI explanations/tooltips.
- **Acceptance Criteria:** PSP indicator icon includes tooltip: definition, qualifications, how it affects pricing and selection. -@ Admin screen includes short inline explanation.

## Day 2 — Story 005
- **Epic:** Vendor Management - Hauler Setup Process
- **Feature:** Hauler Onboarding
- **Parent Task:** Required Steps
- **Task Name:** Display Required Onboarding Checklist
- **User Story:** As a VM Specialist, I want a system-generated onboarding checklist when creating a new hauler so that I know the required minimum steps: naming format, contact details, COI, W9, pricing setup, and PSP eligibility.
- **Description:** Justin and Pelar discuss that new users need to know *exactly which fields* are required to create a fully usable hauler. Many fields are optional today, causing inconsistency. Checklist should appear automatically.
- **Acceptance Criteria:** @ Checklist appears automatically during new hauler creation. -@ items become checked only when Data is valid. -@ UI prevents completion until mandatory items are met.

## Day 2 — Story 006
- **Epic:** Vendor Management â€“ Hauler Onboarding
- **Feature:** Hauler Search & Duplicate Prevention
- **Parent Task:** Search & Validation
- **Task Name:** Prevent Duplicate Haulers
- **User Story:** As a VM Specialist, I want the system to automatically detect possible duplicate haulers based on name, partial name, address, phone, or website so that I donâ€™t have to manually search across the entire database.
- **Description:** Pelar explains that manual searching for pre-existing haulers is currently required. Searching for common names like â€œjunkâ€ yields hundreds of results. The team wants automated detection similar to customer call-pop matching. The system should compare multiple fields and warn users before creating duplicates.
- **Acceptance Criteria:** - When creating a new hauler, the system auto-checks name, partial name, phone, address, and website. - UI displays a list of potential matches with status indicators (Verified, DNU, Active, Inactive). - User must explicitly confirm â€œThis is not a duplicateâ€ before continuing. - Warning appears if address or phone matches an existing hauler.

## Day 2 — Story 007
- **Epic:** Vendor Management â€“ Hauler Onboarding
- **Feature:** Hauler Verification Review
- **Parent Task:** Duplicate Review
- **Task Name:** Review & Validate Potential Duplicates
- **User Story:** As a VM Specialist, I want a UI screen that shows details of possible matching haulers so that I can quickly compare addresses, city, status, and DNU tags.
- **Description:** Pelar describes how she reviews city, address, and status (Verified/DNU) to determine if an existing hauler is the same entity. Today this requires clicking each record manually. This story establishes a structured comparison UI.
- **Acceptance Criteria:** - Comparison UI displays: name, address, city, phone, status (Verified/DNU), notes summary, COI/W9 status. - Ability to open each candidate in a new modal rather than full navigation. - Highlight matches where any field is identical.

## Day 2 — Story 008
- **Epic:** Vendor Management â€“ Hauler Status Management
- **Feature:** DNU Process Visibility
- **Parent Task:** Status Review
- **Task Name:** Explain Why a Hauler Is DNU
- **User Story:** As a VM Specialist, I want a dedicated DNU explanation section that summarizes why a hauler is marked â€œDo Not Useâ€ so I don't need to search for notes manually.
- **Description:** Pelar states that if a hauler is DNU, she must examine old notes, outdated documents, inactivity, or refusal to work with brokers. A structured field explaining DNU reason would prevent guesswork.
- **Acceptance Criteria:** - DNU Reason field required when switching a hauler to DNU. - UI section labeled â€œWhy This Hauler Is DNUâ€. - Historical log shows dates and who set the status. - Notes automatically pulled into a summary.

## Day 2 — Story 009
- **Epic:** Vendor Management â€“ Hauler Onboarding Workflow
- **Feature:** Initial VM Intake Workflow
- **Parent Task:** Onboarding Handoff
- **Task Name:** CD Intake Workflow Automation
- **User Story:** As a VM Specialist, I want the hauler onboarding flow to visually separate CDâ€™s initial steps from Specialist follow-up steps so that responsibilities are clear and structured.
- **Description:** Pelar explains that CD handles initial intake (name, address, phone, email, COI/W9 requests) and assigns the hauler to specialists who handle services, pricing, accounting, hours, and further validation. A UI-guided workflow can reduce confusion.
- **Acceptance Criteria:** - Workflow split into Phase 1 (CD Intake) and Phase 2 (Specialist Setup). - Each phase has required fields. - Automatic assignment and notifications. - UI labels show step ownership (CD vs Specialist).

## Day 2 — Story 010
- **Epic:** Vendor Management â€“ Hauler Onboarding
- **Feature:** Data Entry Validation
- **Parent Task:** Auto-Matching
- **Task Name:** Real-Time â€œPossible Matchâ€ Alerts
- **User Story:** As a VM Specialist, I want real-time suggestions while typing the hauler name, address, or phone number so I instantly see if similar haulers already exist.
- **Description:** Alkhely proposes auto-matching similar to customer matching so the system flags: partial name matches, address collisions, phone number matches, website domain overlaps. This prevents duplicates and reduces manual searching.
- **Acceptance Criteria:** - Real-time suggestions appear after 3 characters typed. - UI highlights match severity (Strong Match / Partial Match / Weak Match). - Clicking a match opens comparison modal. - User can confirm â€œProceed Anywayâ€.

## Day 2 — Story 011
- **Epic:** Vendor Management â€“ Naming Convention Enforcement
- **Feature:** Hauler Naming Rules
- **Parent Task:** Format Enforcement
- **Task Name:** Enforce Hauler Naming Convention
- **User Story:** As a system user, I want the hauler name field to enforce the required naming convention (e.g., â€œVendor Name â€“ City, STâ€) so that Intacct and internal systems remain synchronized.
- **Description:** Anthony asks why â€œâ€“ Houston, TXâ€ is required. Justin explains it is mandated for Intacct and for companies with multiple branches. The naming format must be enforced programmatically.
- **Acceptance Criteria:** - UI enforces naming format: â€œBusiness Name â€“ City, STâ€. - Validation shows error if missing dash, city, or state abbreviation. - Autofill suggests City, ST based on address entry.

## Day 2 — Story 012
- **Epic:** Vendor Management â€“ Data Consistency
- **Feature:** Address & City Validation
- **Parent Task:** Consistency Check
- **Task Name:** Warn When Name City Does Not Match Address City
- **User Story:** As a VM Specialist, I want a warning when the city in the haulerâ€™s name does not match the city in the address so I can correct inconsistent data.
- **Description:** Pelar notes this situation occurs frequently: â€œSometimes that Houston, TX will not match the city and state.â€ This generates confusion and downstream reporting issues.
- **Acceptance Criteria:** - System compares city/state in name vs address field. - Shows yellow alert: â€œCity/State in hauler name does not match address.â€ - Option to override with note reason.

## Day 2 — Story 013
- **Epic:** Vendor Management â€“ Hauler Naming & Multi-Location Support
- **Feature:** Hauler Naming Structure
- **Parent Task:** ID Consistency
- **Task Name:** Support Multi-City Hauler Naming
- **User Story:** As a VM Specialist, I want the system to support haulers whose corporate location differs from their operational depot location so that naming conventions remain intact while representing real service areas.
- **Description:** Pelar explains that some haulers are headquartered in one city (e.g., Houston) but operate other depots (e.g., Midland/Odessa). Their hauler name must follow the required â€œHQ City, STâ€ naming format, but the operational address may differ. This creates confusion today. The system must represent HQ location and operational depots without breaking naming rules.
- **Acceptance Criteria:** - Hauler name field tied to HQ location only. - New structured field for operational depot address(es). - UI clearly labels HQ vs operational addresses. - No validation errors when depot city â‰  HQ city.

## Day 2 — Story 014
- **Epic:** Vendor Management â€“ Address & Depot Management
- **Feature:** Depot Address Management
- **Parent Task:** Address Structuring
- **Task Name:** Capture Multiple Depot Addresses
- **User Story:** As a VM Specialist, I want the ability to add multiple depot addresses (yards, service hubs) directly on the hauler page so that the system reflects all operational areas even if pricing zones do not exist yet.
- **Description:** Justin states that depot addresses currently only exist if PSP pricing zones are created, leaving many haulers missing accurate yard coverage. National haulers like SiteBox operate many depots across the country. The team wants these addresses visible and linked even without pricing zones.
- **Acceptance Criteria:** - New â€œDepot Address Listâ€ section. - Add/Edit/Delete depots. - Each depot has Address, City, State, Zip, Service Region notes. - Depots displayed prominently on hauler profile. - Depots available as reference for pricing zone creation.

## Day 2 — Story 015
- **Epic:** Vendor Management â€“ Contact Information UI
- **Feature:** Contact Information Capture
- **Parent Task:** Contact Details
- **Task Name:** Collect and Organize All Contact Channels
- **User Story:** As a VM Specialist, I want a clean, structured layout for primary contact, secondary contact, dispatch phone, and general phone so I can enter contact info without confusion or redundant fields.
- **Description:** Pelar notes that there are too many phone number fields and some are redundant. Dispatch numbers, general numbers, and contact numbers are unclear and disorganized. A structured UI grouping is needed.
- **Acceptance Criteria:** - Phone numbers grouped under: Primary Contact Phone, Dispatch Phone, Billing Phone (optional). - All optional fields clearly labeled. - Redundant or legacy fields removed. - Field descriptions appear on hover.

## Day 2 — Story 016
- **Epic:** Vendor Management â€“ Document Compliance
- **Feature:** COI Compliance
- **Parent Task:** Document Upload
- **Task Name:** Upload COI & Auto-Track Requirements
- **User Story:** As a VM Specialist, I want to upload a COI and have all required insurance fields validated and auto-highlighted so that compliance can be confirmed without manual checking.
- **Description:** Pelar demonstrates uploading a COI and manually entering expiration, coverage amounts, and request dates. The system currently has no intelligent validation or automation.
- **Acceptance Criteria:** @ Uploading COI triggers required field prompts. -@ system checks for expiration date presence and formatting. -@ UI indicates missing mandatory coverage. -@ Page highlights incomplete fields until validated.

## Day 2 — Story 017
- **Epic:** Vendor Management â€“ Document Consolidation
- **Feature:** W9 Document Cleanup
- **Parent Task:** Attachment Management
- **Task Name:** Consolidate Legacy W9 Upload Fields
- **User Story:** As a system user, I want a single W9 upload field instead of multiple legacy fields so that document management is consistent and no outdated W9s remain.
- **Description:** Justin and Pelar discuss that historically there are 3 W9 fields, but only the bottom one is used. The others cause confusion and inconsistency.
- **Acceptance Criteria:** @ only one W9 upload field remains. -@ Legacy fields removed from forms. -@ Migration script moves existing W9s into the single field. -@ Error handling prevents accidental upload to retired fields.

## Day 2 — Story 018
- **Epic:** Vendor Management â€“ Tax Data Entry
- **Feature:** W9 Data Extraction
- **Parent Task:** Tax Information Entry
- **Task Name:** Enter W9 Tax Classification & EIN With Validation
- **User Story:** As a VM Specialist, I want structured fields for tax classification, EIN/SSN, and entity name with formatting validation so tax data cannot be entered incorrectly.
- **Description:** Pelar enters tax class (S Corp), EIN, and address data manually from the W9. These fields must be validated due to regulatory requirements.
- **Acceptance Criteria:** - EIN validated as 9-digit numeric. - Tax classification selectable via dropdown. - Address fields cannot be blank. - Upload required before saving these values.

## Day 2 — Story 019
- **Epic:** Vendor Management â€“ Address Validation
- **Feature:** Address Lookup Logic
- **Parent Task:** Geolocation Dependency
- **Task Name:** Warn When Address Cannot Be Mapped
- **User Story:** As a VM Specialist, I want the system to warn me when an address cannot be validated or mapped so I can correct it or flag it for admin review.
- **Description:** Pelar notes that some new areas or zip codes do not resolve in the map lookup, preventing field usage. This breaks the workflow and blocks data entry.
- **Acceptance Criteria:** - If address lookup fails, UI displays: â€œAddress not recognized â€“ verify spelling or flag for review.â€ - Allow override entry. - Log unrecognized addresses for DevOps review.

## Day 2 — Story 020
- **Epic:** Vendor Management â€“ Address Entry & Validation
- **Feature:** Address Validation
- **Parent Task:** Manual Override
- **Task Name:** Allow Manual Address Entry When Map Search Fails
- **User Story:** As a VM Specialist, I want the address entry system to allow manual input even when MapQuest/Mapbox cannot validate the address so that I can enter PO Boxes, new developments, and unmapped locations.
- **Description:** Pelar demonstrates that some addresses fail map lookup. Justin confirms it uses fuzzy matching. The team needs the ability to manually enter a street, city, state, and ZIP without being blocked by the mapping API.
- **Acceptance Criteria:** @ system accepts manual address entry without requiring validation from mapping API. - system allows PO Boxes, rural locations, and new developments. -@ UI displays clear warning when fuzzy match is used.

## Day 2 — Story 021
- **Epic:** Vendor Management â€“ Address Quality Enforcement
- **Feature:** Address Validation Rules
- **Parent Task:** Required Field Logic
- **Task Name:** Enforce Complete Address Structure
- **User Story:** As a VM Specialist, I want the system to validate that all required address components (Street, City, State, ZIP) are present so that incomplete or garbage addresses cannot be submitted.
- **Description:** Current Quickbase logic marks the entire address as â€œvalidâ€ if *any* subfield is filled, allowing incomplete or nonsensical addresses. Justin states we must require all components, not just one.
- **Acceptance Criteria:** - Street, City, State, ZIP must all be completed. - Reject entries missing required pieces. - Prevent gibberish-only entries (e.g., random keyboard hammer). - System explains which part is missing.

## Day 2 — Story 022
- **Epic:** Vendor Management â€“ COI & W9 Document Workflow
- **Feature:** Document Status Automation
- **Parent Task:** COI/W9 Status
- **Task Name:** Auto-Validate COI and W9 Documents
- **User Story:** As a VM Specialist, I want the system to auto-validate COI and W9 fieldsâ€”checking expiration dates, required fields, and file extensionsâ€”so that insurance and tax compliance cannot be incorrectly marked as complete.
- **Description:** Pelar manually enters request dates, expiration, and coverage amount. Justin explains many checks are formulaic today but incomplete; more complex automated validation is needed.
- **Acceptance Criteria:** - COI must include expiration date, coverage values, and attachment. - System verifies expiration is in the future. - W9 requires valid EIN/SSN format and complete tax classification. - System auto-updates â€œInsurance on Fileâ€ and â€œW9 on File.â€

## Day 2 — Story 023
- **Epic:** Vendor Management â€“ Verification Logic
- **Feature:** Hauler Verification
- **Parent Task:** Manual Approval
- **Task Name:** Require Manual Verification After Document Review
- **User Story:** As a VM Specialist, I want a manual â€œVerifiedâ€ action after reviewing documents so that human oversight confirms the COI/W9 attached are legitimate.
- **Description:** Justin explains Verified is intentionally manual because automation cannot catch incorrect documents (e.g., someone uploads a dog photo). Verification should remain a human step.
- **Acceptance Criteria:** - â€œVerifiedâ€ must remain a manual checkbox. - System only enables â€œVerifiedâ€ when COI & W9 are valid. - Verified cannot be checked if documents are expired or missing.

## Day 2 — Story 024
- **Epic:** Vendor Management â€“ Authorization Logic
- **Feature:** Authorization Status
- **Parent Task:** Automated Eligibility
- **Task Name:** Automatically Set â€œAuthorizedâ€ Based on Document Validity
- **User Story:** As a VM Specialist, I want the system to automatically determine whether a hauler is authorized to do business with us based on COI and W9 validity so authorization is always accurate.
- **Description:** Justin clarifies authorized is formulaic: if COI and W9 are valid and attached, the hauler is authorized. Expired documents must revoke authorization.
- **Acceptance Criteria:** @ Authorization field auto-@derives from document status. -@ system prevents manual Override except special temporary Authorization process. -@ Expired dates instantly revoke authorization.

## Day 2 — Story 025
- **Epic:** Vendor Management â€“ DNU Override
- **Feature:** Hauler Status
- **Parent Task:** DNU Enforcement
- **Task Name:** Apply Strict Do-Not-Use Override Across System
- **User Story:** As a VM Specialist, I want the â€œDo Not Useâ€ (DNU) flag to override all other statuses so that haulers cannot be accidentally used even if they have valid documents.
- **Description:** Justin explains DNU supersedes everything â€” regardless of insurance validity or verification, if marked DNU the hauler cannot be used.
- **Acceptance Criteria:** - DNU blocks hauler selection in all modules (pricing tool, fulfillment, PSP selection). - Warning banners displayed. - System disallows overrides except by Admin role.

## Day 2 — Story 026
- **Epic:** Vendor Management â€“ Hauler Lifecycle Status
- **Feature:** Hauler Status Workflow
- **Parent Task:** Lifecycle Design
- **Task Name:** Implement Unified Hauler Status Lifecycle
- **User Story:** As a system user, I want a clear hauler lifecycle (Draft â†’ Pending Verification â†’ Authorized â†’ Verified â†’ etc.) so the haulerâ€™s state is easy to understand without checking multiple checkboxes.
- **Description:** Justin introduces a new unified status model replacing scattered checkboxes. Status should reflect document presence, verification, and DNU state.
- **Acceptance Criteria:** @ status determined by COI/W9 validity, Verified flag, and DNU state. -@ Linear flow from Draft â†’ pending â†’ authorized â†’ Verified. -@ UI shows status as a badge or label.

## Day 2 — Story 027
- **Epic:** Vendor Management â€“ Minimum Hauler Requirements
- **Feature:** Hauler Creation
- **Parent Task:** Basic Setup
- **Task Name:** Define Minimum Required Fields to Create Hauler
- **User Story:** As a VM Specialist, I want the system to clearly enforce the minimum required fields for creating a new hauler so that I can save an initial record even if documents and secondary data are missing.
- **Description:** Ashish asks what the minimum fields are. Justin explains that only basic information (name, email, contact, address) is required upfront to create a hauler record. COI/W9 can be uploaded later. The onboarding process may take days or weeks as documents arrive.
- **Acceptance Criteria:** - System must allow creation with only: Provider Name, Contact Name, Email, Phone, Address (Street, City, State, ZIP). - No document requirements at creation step. - UI displays â€œDraft / Missing Documentsâ€ warnings. - Save button enabled when minimum fields complete.

## Day 2 — Story 028
- **Epic:** Vendor Management â€“ Missing Document Warnings
- **Feature:** UI Alerts
- **Parent Task:** Compliance Messaging
- **Task Name:** Display Missing Document Banner
- **User Story:** As a VM Specialist, I want a clear banner indicating missing or expired documents so that I know immediately which compliance items the hauler is lacking.
- **Description:** Pelar shows the orange notification box stating missing documents every time a hauler page is opened when COI/W9 are missing or expired.
- **Acceptance Criteria:** @ Banner appears prominently when COI/@W9 missing or expired. -@ Banner persists until documents are resolved. -@ Banner updates after new uploads.

## Day 2 — Story 029
- **Epic:** Vendor Management â€“ Document Expiration Logic
- **Feature:** Compliance Automation
- **Parent Task:** Expiration Rules
- **Task Name:** Apply Expiration Logic to COI and W9
- **User Story:** As a VM Specialist, I want COI and W9 records to automatically apply expiration rules so the system knows when a hauler should lose authorization.
- **Description:** COI expires 1 year from issue date. W9 expires 2 years from signed date. Pelar demonstrates document dates; Anthony verifies authorized should turn off automatically.
- **Acceptance Criteria:** - COI must auto-expire at 1 year. - W9 must auto-expire at 2 years. - Expired documents immediately revoke authorization. - UI shows expiration state.

## Day 2 — Story 030
- **Epic:** Vendor Management â€“ Auto-Revoke Authorization
- **Feature:** Authorization
- **Parent Task:** Auto Rules
- **Task Name:** Automatically Remove Authorization When Documents Expire
- **User Story:** As a VM Specialist, I want the system to automatically revoke authorization when COI/W9 expire so haulers cannot be accidentally used while non-compliant.
- **Description:** Anthony confirms authorized must be fully formulaic and auto-revoke when documents lapse. Justin confirms this is already partially implemented via form rules.
- **Acceptance Criteria:** - Authorization = false when COI or W9 expired. - No manual override except temporary override by management. - UI instantly updates.

## Day 2 — Story 031
- **Epic:** Vendor Management â€“ Save Hauler Record
- **Feature:** Hauler Creation
- **Parent Task:** Record Save
- **Task Name:** Save Initial Hauler Record
- **User Story:** As a VM Specialist, I want the system to save the newly created hauler record and redirect me to their full page so I can continue onboarding.
- **Description:** Pelar demonstrates saving the hauler record after documents and core fields are entered. The system loads the new hauler page.
- **Acceptance Criteria:** @ Save button stores all entered data. -@ Redirect to hauler profile. - system displays status, docs, and fields immediately.

## Day 2 — Story 032
- **Epic:** Vendor Management â€“ COI/W9 Activity Logging
- **Feature:** Audit Logs
- **Parent Task:** Upload Logging
- **Task Name:** Track COI and W9 Upload and Changes
- **User Story:** As a compliance user, I want the system to log each COI/W9 upload and status change so that we have full auditability for insurance and tax compliance.
- **Description:** Justin shows logs: COI last upload, who uploaded, timestamp, and related actions. Logs are crucial for business accountability.
- **Acceptance Criteria:** Log who uploaded document, when, and what changed. -@ display Log entries in a dedicated section. -@ Support multiple Log entries historically.

## Day 2 — Story 033
- **Epic:** Vendor Management â€“ PSP Eligibility Review
- **Feature:** PSP Qualification
- **Parent Task:** Pre-PSP Checks
- **Task Name:** Perform Pre-Approval Checks Before Marking PSP
- **User Story:** As a VM Specialist, I want the system to guide me through required pre-PSP checks so a hauler can be properly evaluated before Justin/management applies the PSP designation.
- **Description:** Pelar explains that specialists must confirm page cleanliness and completeness before sending to management for PSP approval. She cannot finalize PSP because only management can finalize the seal.
- **Acceptance Criteria:** @ system displays required pre-@PSP checklist. - must confirm documents valid, pricing zones complete, hauler Data confirmed. -@ only management can finalize PSP status.

## Day 2 — Story 034
- **Epic:** Vendor Management â€“ PSP Status Activation
- **Feature:** PSP Assignment
- **Parent Task:** PSP Promotion
- **Task Name:** Allow Management to Apply PSP Status
- **User Story:** As a manager, I want to promote a hauler to PSP status so they become available for premium routing and special logic within the system.
- **Description:** Justin states he can assign PSP status through management tools. Pelar outlines steps she performs before sending for approval.
- **Acceptance Criteria:** @ only management roles can apply PSP flag. -@ system requires all required fields and documents. -@ UI shows PSP seal once active.

## Day 2 — Story 035
- **Epic:** Vendor Management â€“ PSP Qualification Workflow
- **Feature:** PSP Approval
- **Parent Task:** PSP Requirements
- **Task Name:** Fill All PSP Minimum Requirements
- **User Story:** As a VM Specialist, I want a guided process to ensure all PSP-required fields (services, hours, accounting settings, justification, and pricing validations) are completed before submission to management, so that PSP approvals are consistent and error-free.
- **Description:** Pelar describes all fields that must be filled before management can approve PSP. This includes services offered, hours of operation, payment methods, fees, accounting preferences, pricing zones validated, last contact notes, and justification. This process is currently manual and spread across multiple UI sections.
- **Acceptance Criteria:** @ UI displays a structured PSP Minimum Requirements checklist. -@ Checklist must prevent submission unless all required fields are complete. -@ all fields visually grouped for clarity. - management receives a clean, complete dossier.

## Day 2 — Story 036
- **Epic:** Vendor Management â€“ Step-by-Step PSP Checklist UI
- **Feature:** UI/UX Workflow
- **Parent Task:** PSP Checklist
- **Task Name:** Provide a Guided Multi-Step PSP Checklist
- **User Story:** As a VM Specialist, I want a single consolidated PSP checklist interface so I don't have to navigate multiple tabs when preparing a hauler for PSP approval.
- **Description:** Justin states that the ideal UI should not require jumping around to 16 places. A clear step-by-step PSP checklist should capture hours, services, payment terms, fees, pricing, and required validations.
- **Acceptance Criteria:** @ Checklist appears as a structured multistep UI. -@ required fields are clearly marked. -@ Users receive visual progress indicators. -@ system blocks PSP submission until all Checklist steps are complete.

## Day 2 — Story 037
- **Epic:** Vendor Management â€“ Accounting Requirements for PSP
- **Feature:** PSP Requirements
- **Parent Task:** Accounting Validation
- **Task Name:** Capture Required Accounting and Payment Information
- **User Story:** As a VM Specialist, I want required accounting fields (payment terms, CC fees, late fees, preferred payment method) validated before PSP submission so that AP can rely on accurate financial data.
- **Description:** Pelar fills in payment terms, acceptable payment methods, fees, and notes AP usually updates parts of this later. These fields are mandatory for PSP review.
- **Acceptance Criteria:** - UI enforces required completion of accounting fields before PSP submission. - Conditional fields (e.g., credit card fee %) appear based on user choices. - AP can override with notes but cannot leave mandatory fields blank.

## Day 2 — Story 038
- **Epic:** Vendor Management â€“ Pricing Zone Validation for PSP
- **Feature:** Pricing Zones
- **Parent Task:** PSP Validation
- **Task Name:** Validate Pricing Zones Before PSP Approval
- **User Story:** As a VM Specialist, I want the system to confirm that pricing zones and associated pricing uploads are complete before a hauler can become a PSP.
- **Description:** Pelar states that management requires validated pricing zones and completed rate reviews. This is currently checked manually.
- **Acceptance Criteria:** - UI automatically confirms pricing zones completed. - If pricing missing, PSP submission blocked. - UI shows â€œPricing Zones Validatedâ€ indicator.

## Day 2 — Story 039
- **Epic:** Vendor Management â€“ PSP Justification Checklist
- **Feature:** PSP Requirements
- **Parent Task:** Justification
- **Task Name:** Replace Free-Text PSP Justification with Structured Fields
- **User Story:** As a VM Specialist, I want a structured PSP justification checklist instead of a free-text field so PSP quality standards are consistent across the team.
- **Description:** Pelar currently writes free-text justification (â€œgreat additionâ€¦ wide service areaâ€), while Justin states this field was intended to become a checklist (non-overlap, service area, pricing, reliability, etc.).
- **Acceptance Criteria:** @ Replace text box with multi-@item checklist. -@ required fields: non-overlap verification, service coverage, pricing verification, reliability notes, document status. -@ prevent completion until all Checklist items addressed.

## Day 2 — Story 040
- **Epic:** Vendor Management â€“ Prevent PSP Overlap
- **Feature:** PSP Rules
- **Parent Task:** Coverage Validation
- **Task Name:** Validate PSP Coverage to Prevent Overlaps
- **User Story:** As a VM Specialist, I want the system to warn me if a PSP candidate overlaps an existing PSP in the same service area so we avoid duplicate PSP coverage.
- **Description:** Anthony asks if PSPs ever overlap; Pelar explains they try to avoid it manually but cluster-based pricing sometimes creates edge cases. Today there is no system validation.
- **Acceptance Criteria:** @ system runs automatic geographic +@ pricing zone overlap check. - If overlaps detected, UI warns User before submission. -@ warning must show the specific conflicting PSP.

## Day 2 — Story 041
- **Epic:** Vendor Management â€“ PSP Designation Role Restriction
- **Feature:** Permissions
- **Parent Task:** Role Control
- **Task Name:** Limit PSP Assignment to Management Roles
- **User Story:** As an administrator, I want PSP assignment restricted to management and vendor management roles so unauthorized staff cannot elevate haulers.
- **Description:** Conversation confirms only vendor management or administrators can apply PSP status. CSS/fulfillment cannot.
- **Acceptance Criteria:** - Only authorized roles see the PSP checkbox. - Attempt by unauthorized roles returns â€œAccess Denied.â€ - Audit log records who granted PSP.

## Day 2 — Story 042
- **Epic:** Vendor Management â€“ Modal Alerts for Status Issues
- **Feature:** UI Alerts
- **Parent Task:** Modal Warnings
- **Task Name:** Display Modal Alerts for Key Status Issues
- **User Story:** As a user, I want modal pop-up warnings when a hauler has critical status issues (unverified, unauthorized, red pricing notes) so I don't miss important conditions.
- **Description:** Diego asks if system warns users about manual validation needs. Justin confirms there are modal pop-ups (e.g., missing documents, red pricing notes).
- **Acceptance Criteria:** Modal triggers when: missing documents, unverified, unauthorized, red pricing notes, critical flags. -@ Modal must block interaction until dismissed. -@ Color coding matches severity.

## Day 2 — Story 043
- **Epic:** Vendor Management â€“ PSP Zone Conflict Warning
- **Feature:** PSP Rules
- **Parent Task:** Cluster Validation
- **Task Name:** Warn Users if Proposed PSP Conflicts with Existing PSP in Clusters
- **User Story:** As a VM Specialist, I want warnings when entering pricing zones or clusters that conflict with existing PSPs so I can correct issues before finalizing.
- **Description:** Justin describes this as a future improvementâ€”system should check zip codes and clusters while entering pricing zones and warn if the cluster already belongs to another PSP.
- **Acceptance Criteria:** @ automatic cluster conflict check. -@ warning message specifies conflicting PSP and zone. -@ User must resolve conflict or escalate.

## Day 2 — Story 044
- **Epic:** Vendor Management â€“ PSP Coverage Rules
- **Feature:** PSP Rules
- **Parent Task:** Coverage Criteria
- **Task Name:** Define PSP Coverage Criteria
- **User Story:** As a VM Specialist, I want clearly defined system-visible criteria for how close two PSPs can be in service area coverage so that PSP assignments remain consistent and avoid manual interpretation.
- **Description:** Diego asks how â€œclosenessâ€ is determined and whether criteria exist or are arbitrarily decided. Justin explains current logic: zip-codeâ€“based coverage, cluster-based pricing, radius-based calculations, and potential geospatial calculations for future phases.
- **Acceptance Criteria:** - UI shows clearly defined PSP coverage rules. - Rules documented directly on screen (zip list, radius limit, cluster boundaries). - PSP submission cannot proceed unless coverage falls within defined limits.

## Day 2 — Story 045
- **Epic:** Vendor Management â€“ Radius & Distance Validation
- **Feature:** Geospatial Logic
- **Parent Task:** Distance Validation
- **Task Name:** Automate Distance-Based Service Validation
- **User Story:** As a system, I want to calculate distance between depot and service locations using real drivable miles so that PSP and hauler coverage is evaluated accurately.
- **Description:** Justin explains that the pricing tool first identifies all zip codes in a radius and then performs precise street-level distance calculations using Googleâ€™s API. This ensures that servicing areas are realistic (not straight-line).
- **Acceptance Criteria:** - System performs two-step validation: (1) radius-to-zip conversion, (2) Google Maps API drivable distance calculation. - Distances stored and displayed on UI. - Validation triggers warnings for out-of-range coverage.

## Day 2 — Story 046
- **Epic:** Vendor Management â€“ Map-Based Zone Drawing
- **Feature:** Mapping Interface
- **Parent Task:** Zone Creation
- **Task Name:** Support Custom Map Zone Drawing
- **User Story:** As a VM Specialist, I want the ability to trace custom service areas on a map to define coverage zones so service boundaries reflect manual real-world exceptions.
- **Description:** Anthony and Justin discuss future addition: vector-based zone tracing. This would supplement radius and zip list methods. This becomes the third method of defining zones.
- **Acceptance Criteria:** @ mapping UI includes polygon-@drawing tools. - User can create, edit, and Save custom shapes. -@ Shapes convert automatically into ZIP lists for system compatibility.

## Day 2 — Story 047
- **Epic:** Vendor Management â€“ Service Area Map Visualization
- **Feature:** UI Enhancements
- **Parent Task:** Visual Maps
- **Task Name:** Display Service Area Maps on Hauler Page
- **User Story:** As a VM Specialist, I want service area maps displayed directly on the hauler page so I can visually confirm coverage without manually referencing external maps.
- **Description:** Pelar explains that she manually generates color-coded maps for every provider and wants these displayed directly in the UI so teams can quickly understand coverage. Justin confirms this would be an ideal improvement.
- **Acceptance Criteria:** @ hauler Page shows embedded coverage map. -@ map dynamically updates when zones or ZIP lists change. - Users can toggle between radius, ZIP list, and custom shape views.

## Day 2 — Story 048
- **Epic:** Vendor Management â€“ PSP Overlap Clarification
- **Feature:** PSP Rules
- **Parent Task:** Overlap Logic
- **Task Name:** Define Rule for Single PSP per Zip Code
- **User Story:** As a VM Specialist, I want each zip code to be assigned to no more than one PSP unless an approved exception exists so that pricing tool recommendations remain consistent.
- **Description:** Ashish asks whether only one PSP can exist per zip code. Pelar explains overlap is minimized manually, but exceptions exist due to cluster mixing and pricing advantages.
- **Acceptance Criteria:** - System enforces â€œ1 PSP per zip codeâ€ unless override is granted. - If overlap detected, system generates conflict warning highlighting zip code(s). - Override requires management approval.

## Day 2 — Story 049
- **Epic:** Vendor Management â€“ PSP Overlap Reasoning UI
- **Feature:** PSP Rules
- **Parent Task:** Overlap Resolution
- **Task Name:** Explain Overlap Decisions When PSPs Share Zip Codes
- **User Story:** As a VM Specialist, I want a structured UI to document and justify why one PSP covers overlapping zip codes when two providers partially overlap so that pricing logic remains transparent.
- **Description:** Justin asks how decisions are made when two PSPs overlap on 3 zip codes. Pelar explains decisions rely on distance, hub location, pricing differences, and service value. This is all manual today.
- **Acceptance Criteria:** @ UI provides structured overlap-@resolution form. -@ requires justification: Distance-@to-hub, pricing Comparison, service advantages. -@ Users cannot finalize PSP assignment without completing justification.

## Day 2 — Story 050
- **Epic:** Vendor Management â€“ Visual Cluster & Pricing Comparison
- **Feature:** Pricing Analysis
- **Parent Task:** Cluster Comparison
- **Task Name:** Provide Visual Pricing Comparison in Overlap Areas
- **User Story:** As a VM Specialist, I want a visual comparison tool showing pricing differences between overlapping PSPs in shared zip codes so I can choose the correct PSP based on value.
- **Description:** Pelar explains she uses maps and pricing manually to determine which PSP should own a zip when coverage overlaps (distance, AD pricing, etc.).
- **Acceptance Criteria:** @ tool compares pricing side-@by-@side for all PSPs touching a zip. -@ highlights best-@value PSP. -@ shows hub Distance and delivery fee logic.

## Day 2 — Story 051
- **Epic:** PSP Coverage Rules & Optimization
- **Feature:** PSP Assignment Logic
- **Parent Task:** Coverage Management
- **Task Name:** Prevent Multi-PSP Zip Code Assignment
- **User Story:** As a VM Specialist, I want the system to prevent multiple PSPs from being assigned to the same zip code so that the pricing tool displays only the correct PSP and avoids operational confusion.
- **Description:** Pelar explains that if multiple PSPs cover the same zip code, all will appear in the pricing tool unless blocked. The rule today: *first assigned PSP keeps the zip code* unless pricing changes drastically.
- **Acceptance Criteria:** @ system blocks assignment of a ZIP code already owned by another PSP. - If conflict exists, system displays a clear warning with the existing PSP name. -@ pricing tool only shows the assigned PSP for that zip.

## Day 2 — Story 052
- **Epic:** PSP Coverage Rules & Optimization
- **Feature:** PSP Assignment Logic
- **Parent Task:** Coverage Management
- **Task Name:** Manage First-Assignment Wins Logic
- **User Story:** As a VM Specialist, I want the system to follow a â€˜first-assignment winsâ€™ rule for PSPs unless overridden by pricing comparison so that coverage remains stable and predictable.
- **Description:** Pelar confirms that the first PSP assigned to a zip code keeps it unless a new provider presents materially better pricing. The current process is fully manual.
- **Acceptance Criteria:** - System enforces â€œfirst PSP winsâ€ logic by default. - Overrides require documented justification. - UI prevents accidental reassignment unless override is activated.

## Day 2 — Story 053
- **Epic:** PSP Pricing Comparisons
- **Feature:** Pricing Analysis
- **Parent Task:** Comparison Workflow
- **Task Name:** Trigger PSP Comparison on New Pricing
- **User Story:** As a VM Specialist, I want the system to automatically notify me to compare pricing whenever a provider submits updated rates so PSP coverage reflects current market value.
- **Description:** Pelar explains that *any time* a provider submits pricing, she performs comparisons manually. Justin notes comparisons occur daily and are operationally critical.
- **Acceptance Criteria:** @ system detects new pricing submissions. -@ automatic prompt suggests performing a PSP pricing comparison. -@ UI links directly to Comparison tool.

## Day 2 — Story 054
- **Epic:** PSP Pricing Comparisons
- **Feature:** Pricing Analysis
- **Parent Task:** Stability of PSP Zones
- **Task Name:** Maintain PSP Zip Ownership Unless Pricing Falls Out of Margin
- **User Story:** As a VM Specialist, I want the system to flag when a PSPâ€™s pricing increases enough to damage margin, so zip code ownership can be re-evaluated.
- **Description:** Current behavior: PSP keeps the zone unless pricing increases so much that margin turns red. Then another PSP may take over after review.
- **Acceptance Criteria:** - System monitors pricing updates and margin impacts. - Margin thresholds configurable. - Flag triggers a â€œReevaluate PSP for this zoneâ€ alert.

## Day 2 — Story 055
- **Epic:** Dynamic Zone Adjustment
- **Feature:** Zone Management
- **Parent Task:** Dynamic Coverage
- **Task Name:** Shrink PSP Coverage When Pricing Increases
- **User Story:** As a VM Specialist, I want coverage areas to auto-shrink when a PSP raises rates beyond acceptable thresholds so that only cost-effective coverage remains assigned.
- **Description:** Pelar describes manually shrinking PSP areas when a provider raises their pricing, especially in rural markets lacking alternatives.
- **Acceptance Criteria:** @ Automated check identifies zones with unacceptable pricing. -@ UI allows approving automatic shrink or manually adjusting. -@ system removes PSP from affected zones after approval.

## Day 2 — Story 056
- **Epic:** Dynamic Zone Adjustment
- **Feature:** Zone Management
- **Parent Task:** Competitive Monitoring
- **Task Name:** Detect When a Neighboring PSP Should Inherit Zip Codes
- **User Story:** As a VM Specialist, I want the system to detect when a nearby PSP becomes more competitive than the current one so reassignment is suggested proactively.
- **Description:** Justin notes that today the comparison is entirely manual; with automation, the system could identify when a competitor PSP becomes the better choice.
- **Acceptance Criteria:** @ system evaluates neighbor PSP pricing in adjacent zones. -@ suggests Reassignment when price difference crosses a threshold. -@ displays side-@by-@side Comparison for confirmation.

## Day 2 — Story 057
- **Epic:** Automated Price-Triggered Reviews
- **Feature:** Automation
- **Parent Task:** Trigger Framework
- **Task Name:** Auto-Reevaluate PSP Zones When Price Increases Are Logged
- **User Story:** As a VM Specialist, I want price increases to automatically trigger a full zone reevaluation so PSP assignments remain accurate without repeating multi-step manual work.
- **Description:** Justin emphasizes that a price increase should trigger a recalculation of margins, statistical models, PSP rents, and comparisonsâ€”currently all manual.
- **Acceptance Criteria:** @ price increase event triggers recalculation process. - system updates all affected pricing, margins, and comparisons. -@ Conflicts or changes highlighted in a report.

## Day 2 — Story 058
- **Epic:** Automated Reporting
- **Feature:** Automation
- **Parent Task:** Reporting
- **Task Name:** Generate Automatic PSP Impact Reports After Price Changes
- **User Story:** As a VM Specialist, I want automated reports showing which PSP zones may change after pricing adjustments so that I can quickly act on potential issues.
- **Description:** Pelar says a report â€œwould be great,â€ and Justin confirms this should accompany automated recalculation.
- **Acceptance Criteria:** @ Report lists all zones affected by pricing changes. -@ includes margin deltas and suggested actions. -@ Delivered via UI and email.

## Day 2 — Story 059
- **Epic:** PSP Competitive Management
- **Feature:** PSP Ranking & Evaluation
- **Parent Task:** Pricing & Market Position
- **Task Name:** Flag Non-Competitive PSPs
- **User Story:** As a VM Specialist, I want the system to detect when a PSP is no longer the best option in a zip code so that I can proactively reassign coverage and maintain competitive pricing.
- **Description:** Justin states the system should identify when a PSP is no longer best for an area/product. Today this is manually recognized. The system must analyze pricing, margins, and competing PSPs to detect when performance has fallen.
- **Acceptance Criteria:** - Algorithm identifies underperforming PSPs. - UI displays a â€œPSP No Longer Best Performerâ€ alert. - Displays alternatives with pricing comparison.

## Day 2 — Story 060
- **Epic:** PSP Agreements & Expectations
- **Feature:** PSP Program Rules
- **Parent Task:** Coverage Policies
- **Task Name:** Clarify Lack of Guaranteed Coverage
- **User Story:** As a VM Specialist, I need the system to reflect that PSP designation does not guarantee fixed territories so that PSP expectations match operational reality.
- **Description:** Pelar explains PSPs are not guaranteed territories; areas can be reduced or adjusted based on competition, pricing, or operational need.
- **Acceptance Criteria:** @ UI messaging explicitly states PSP status does not equal guaranteed coverage. -@ PSP onboarding UI includes This statement.

## Day 2 — Story 061
- **Epic:** PSP Area Assignment
- **Feature:** PSP Zone Assignment
- **Parent Task:** Coverage Selection
- **Task Name:** Approve Finalized PSP Coverage Area
- **User Story:** As a VM Specialist, I need a UI workflow to define, preview, and confirm the **exact** zones a PSP will be assigned before they become active so that expectations are documented.
- **Description:** Pelar manually selects the subset of service areas a PSP will actually get (they may request huge areas but VM limits them).
- **Acceptance Criteria:** - Ability to preview proposed service area. - Confirmation modal requiring reviewer notes. - PSP record stores â€œApproved Coverage Areaâ€ snapshot.

## Day 2 — Story 062
- **Epic:** PSP Coverage Adjustments
- **Feature:** Coverage Change Workflow
- **Parent Task:** Communication
- **Task Name:** Notify PSP When Coverage Shrinks
- **User Story:** As a VM Specialist, I want a workflow that notifies PSPs when their coverage shrinks so they are informed and expectations stay aligned.
- **Description:** Ashish asks whether PSPs are told when coverage shrinks. Today they are not. System should help deliver communication.
- **Acceptance Criteria:** @ system generates notification template. -@ VM can preview/@edit message. -@ Log stored under PSP record.

## Day 2 — Story 063
- **Epic:** Pricing Negotiation Tools
- **Feature:** Pricing Proposal Tool
- **Parent Task:** Negotiation
- **Task Name:** Generate Automated Price Decrease Proposals
- **User Story:** As a VM Specialist, I want the system to auto-generate price-decrease proposals using competitor pricing so negotiations are faster and consistent.
- **Description:** Pelar manually screenshots sections of her Excel comparison and sends price-decrease proposals. Today: 100% manual.
- **Acceptance Criteria:** @ tool generates proposal based on competitor pricing and target margins. -@ UI allows editing of suggested decrease amounts. -@ Export to PDF/@email.

## Day 2 — Story 064
- **Epic:** Pricing Negotiation Tools
- **Feature:** Pricing Proposal Tool
- **Parent Task:** Negotiation
- **Task Name:** Compare Market Pricing in System Instead of Excel
- **User Story:** As a VM Specialist, I want the comparison grid (currently Excel) to exist inside Cube so I donâ€™t have to maintain external spreadsheets.
- **Description:** Pelar: â€œWe do it straight Excelâ€¦ 7 hours out of 8 hours a day.â€ Justin: The #1 improvement is automating this into Cube.
- **Acceptance Criteria:** @ Comparison tool matches Excelâ€™s logic. - pulls PSP rates, statistical rates, and target margins. -@ allows recalculation and highlighting of deltas.

## Day 2 — Story 065
- **Epic:** Price Change Handling
- **Feature:** Automation
- **Parent Task:** Triggers
- **Task Name:** Trigger Pricing Review After Provider Price Change
- **User Story:** As a VM Specialist, I want the system to automatically start a competitive analysis workflow when a provider updates their prices.
- **Description:** Justin and Pelar explain competitive reviews must happen every time pricing changes. System should trigger this automatically.
- **Acceptance Criteria:** - Price updates create â€œReview Requiredâ€ task. - Link directly opens pricing comparison tool. - Detailed impact summary shown.

## Day 2 — Story 066
- **Epic:** PSP Status UI
- **Feature:** PSP Status & Indicators
- **Parent Task:** UI Indicators
- **Task Name:** Display PSP Seal as Status Indicator
- **User Story:** As a user, I want a clear visual PSP â€œsealâ€ to appear once a provider is approved so the page instantly communicates PSP status.
- **Description:** Justin shows that marking PSP adds a â€œsticker.â€ System should render a consistent, prominent badge.
- **Acceptance Criteria:** @ seal shown at top of hauler record. -@ includes tooltip explaining PSP benefits. -@ visible in search results.

## Day 2 — Story 067
- **Epic:** PSP Approval Workflow
- **Feature:** PSP Status & Indicators
- **Parent Task:** Approval Process
- **Task Name:** Show PSP Activation Event Log
- **User Story:** As a VM Specialist, I want a timestamped log entry showing who activated PSP status so that accountability and auditing are preserved.
- **Description:** Pelar refreshes and sees the PSP seal appear after Justin activated it. The system should log this activation clearly.
- **Acceptance Criteria:** system logs: User, date/time, previous status, new status. -@ visible in activity/@History section. -@ exportable.

## Day 2 — Story 068
- **Epic:** PSP Activation Workflow
- **Feature:** PSP Status & Indicators
- **Parent Task:** PSP Activation
- **Task Name:** Mark PSP as Assigned Specialist
- **User Story:** As a VM Specialist, I want the UI to allow me to claim ownership of a PSP record by adding my name so that internal teams know who manages the account.
- **Description:** Pelar updates the PSP record by clicking the pencil and inserting her name to indicate ownership. This is manual but essential for internal clarity.
- **Acceptance Criteria:** @ field to assign VM specialist. -@ field editable only by VM/@Managers. -@ assigned specialist displays prominently.

## Day 2 — Story 069
- **Epic:** PSP Activation Workflow
- **Feature:** PSP Status & Indicators
- **Parent Task:** Notifications
- **Task Name:** Trigger PSP Announcement Notification
- **User Story:** As a VM Specialist, I want the system to send a celebratory PSP activation notification so internal users know a new PSP is live.
- **Description:** Pelar states a â€œbell ringsâ€ when PSP is added. Justin jokes about real bells but implies a system event. Need UI notification.
- **Acceptance Criteria:** - Notification banner or toast displays. - Notification includes PSP name. - Appears to relevant roles (VM, Fulfillment, Sales).

## Day 2 — Story 070
- **Epic:** PSP Onboarding Analytics
- **Feature:** PSP Reporting
- **Parent Task:** Performance Metrics
- **Task Name:** Display PSP Adds Per Specialist
- **User Story:** As a VM Manager, I need a report showing each specialistâ€™s PSP additions by month/quarter so I can track performance goals.
- **Description:** Pelar shows the report displaying counts per specialist (hers, Jacobâ€™s, Julianaâ€™s).
- **Acceptance Criteria:** @ Report shows PSP adds per person. - Filterable by month, quarter, year. -@ Exportable to CSV.

## Day 2 — Story 071
- **Epic:** PSP Requirements Tracking
- **Feature:** PSP Goals
- **Parent Task:** Team Metrics
- **Task Name:** Track PSP Count Requirements
- **User Story:** As a VM Manager, I want the system to track quota requirements (2 per month per person) so performance evaluation is automated.
- **Description:** Pelar: requirement = 2/month, 6/quarter; team of 4.
- **Acceptance Criteria:** @ UI defines expected PSP quota. -@ Dashboard compares actual vs expected. -@ Alerts when someone falls behind.

## Day 2 — Story 072
- **Epic:** PSP Workflow
- **Feature:** PSP Process Flow
- **Parent Task:** Core Process
- **Task Name:** Clarify PSP Core Workflow
- **User Story:** As a user, I need the system to visually summarize core PSP workflow steps so I understand the required sequence.
- **Description:** Justin asks if the Quickbase workflow shown represents the core steps. Pilar confirms yes.
- **Acceptance Criteria:** @ Provide a visually rendered Workflow map. -@ accessible from PSP record. -@ Accurate representation of current process.

## Day 2 — Story 073
- **Epic:** Quarterly Check-ins
- **Feature:** Quarterly Reviews
- **Parent Task:** Check-in Records
- **Task Name:** Access Quarterly Check-in History
- **User Story:** As a VM Specialist, I want a single page showing quarterly check-ins for each provider so I can easily view past assessments.
- **Description:** Pelar explains each provider gets 4 check-ins per year and they live on one page with multiple reports.
- **Acceptance Criteria:** @ single screen lists Q1â€“Q4 entries. - each entry shows status, date, reviewer. -@ Filtering by year and provider.

## Day 2 — Story 074
- **Epic:** Quarterly Check-ins
- **Feature:** Quarterly Reviews
- **Parent Task:** Check-in Records
- **Task Name:** Open Incomplete Quarterly Check-in
- **User Story:** As a VM Specialist, I want the ability to quickly open an incomplete quarterly check-in so I can resume work without searching.
- **Description:** Pelar tries to locate one thatâ€™s â€œnot complete yetâ€ to show the team.
- **Acceptance Criteria:** - Incomplete check-ins flagged in UI. - Quick â€œresumeâ€ button. - Visual status indicator.

## Day 2 — Story 075
- **Epic:** UX Improvements
- **Feature:** General Navigation
- **Parent Task:** Break Handling
- **Task Name:** Need Temporary Pause Message
- **User Story:** As a user, I want the system to show a â€œsession pausedâ€ or equivalent indicator when presenters step away so the group knows process is temporarily halted.
- **Description:** Pelar announces 5-minute break; system currently has no indicator.
- **Acceptance Criteria:** - Optional UI â€œsession pausedâ€ banner. - Manual toggle for presenters. - Auto-timeout option.

## Day 2 — Story 076
- **Epic:** PSP Rules Engine
- **Feature:** Form Rules & Logic
- **Parent Task:** Validation Rules
- **Task Name:** Show Form Rules Driving PSP Behavior
- **User Story:** As a developer/analyst, I want a clear UI panel showing all automated rules, triggers, and modal warnings that fire in the PSP workflow so I understand the logic without digging into Quickbase internals.
- **Description:** Justin explains numerous modal warnings, logging triggers, rule-based validations, show/hide fields, restrictions, and automations.
- **Acceptance Criteria:** - Dedicated â€œRules & Automationâ€ panel. - Human-readable description of each rule. - Links to affected fields.

## Day 2 — Story 077
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Check-In Workflow
- **Parent Task:** VM Ticket Creation
- **Task Name:** Create Quarterly Check-In Ticket
- **User Story:** As a Vendor Management Specialist, I want to quickly create a Quarterly Check-In VM ticket using a streamlined UI so that I can begin the health check process without navigating multiple slow-loading pages.
- **Description:** User must select 'Quarterly Check-In' from a dropdown and assign the ticket to themselves. Slow-loading elements currently delay the workflow. A streamlined ticket creation interface is needed to reduce unnecessary clicks and automate default assignments.
- **Acceptance Criteria:** 1. User can create a Quarterly Check-In ticket with 2 clicks. 2. The system auto-populates assignment and status fields (In Progress). 3. Ticket saves without latency. 4. Confirmation appears on screen.

## Day 2 — Story 078
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Report Data Collection
- **Parent Task:** Sales & Opportunity Pull
- **Task Name:** View Opportunities and Sales Counts
- **User Story:** As a Specialist, I need a UI that clearly displays quarterly opportunities and sales totals for a service provider so I can calculate performance without manually cross-referencing separate systems.
- **Description:** Currently reports only show 'Previous 90 days', which does not align with calendar quarter boundaries. User manually calculates opportunities, sales, and percentages. The UI should allow selecting a quarter date range and instantly update totals.
- **Acceptance Criteria:** 1. User can filter by Quarter (Q1/Q2/Q3/Q4). 2. Opportunity and Sales totals populate instantly. 3. No manual counting required. 4. Data matches provider record counts.

## Day 2 — Story 079
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Report Accuracy & UX Improvements
- **Parent Task:** Quarterly Date Range Filter
- **Task Name:** Add Calendar Quarter Selector
- **User Story:** As a User, I want a calendar-quarter date filter so reports stop showing 'Previous 90 Days', preventing mismatch between system data and quarterly review requirements.
- **Description:** The current report is misleading because a rolling 90-day range does not match exact quarters. UI should provide a clean selector for Q1/Q2/Q3/Q4 based on calendar dates and instantly recalc metrics.
- **Acceptance Criteria:** 1. User can choose Q1/Q2/Q3/Q4. 2. The system recalculates Opportunity, Sales, Win Rate using that exact date range. 3. No manual correction or cross-check needed.

## Day 2 — Story 080
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Service Provider Activity Verification
- **Parent Task:** Record Alignment Check
- **Task Name:** Cross-Validate Sales Report Against Provider Page
- **User Story:** As a Specialist, I want the system to automatically compare sales counts from reports against the providerâ€™s service history so discrepancies no longer require manual auditing.
- **Description:** Currently the Specialist manually counts July/Aug/Sept deliveries and compares to the report. The system should auto-reconcile those values and flag mismatches.
- **Acceptance Criteria:** 1. The system displays both counts side-by-side. 2. If mismatched, a warning appears. 3. User can drill into the mismatched entries.

## Day 2 — Story 081
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Support Case Review
- **Parent Task:** Accounting Inquiry Lookup
- **Task Name:** Display Accounting Inquiry Count
- **User Story:** As a Specialist, I need to see the number of Accounting Inquiries (AIs) for the quarter in one click instead of scanning manually so that I accurately assess hauler performance.
- **Description:** The current process requires scrolling through accounting inquiry logs and visually counting entries. UI should summarize number of AIs per quarter automatically.
- **Acceptance Criteria:** 1. Quarter-based filter exists. 2. AI count displayed as a single value. 3. AI fault attribution (ZTERS vs Vendor) summarized.

## Day 2 — Story 082
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Vendor Management Tickets
- **Parent Task:** VM Ticket Lookup
- **Task Name:** Display VM Ticket Count
- **User Story:** As a Specialist, I need a quick view of how many Vendor Management tickets occurred in the quarter so that I can track performance trends without manual scanning.
- **Description:** Current method requires scrolling through VM ticket list and counting by eye. System should automatically total both resolved and active tickets per quarter.
- **Acceptance Criteria:** 1. Quarter filter available. 2. System summarizes total VM tickets. 3. Drill-down list available for details.

## Day 2 — Story 083
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Performance Summary UI
- **Parent Task:** Automated Metric Calculation
- **Task Name:** Auto-Calculate All Quarterly Metrics
- **User Story:** As a Specialist, I want the system to auto-calculate all quarterly performance metrics (targets, missed opportunities, avg revenue, expected revenue) so I no longer need external Word documents or manual math.
- **Description:** Currently requires copying numbers from several reports into a Word template and calculating target sales, missed opportunities, revenue totals, averages, etc. This is slow, repetitive, error-prone.
- **Acceptance Criteria:** 1. System auto-fills all quantitative fields for quarterly check-in. 2. All formulas match the official Word doc. 3. No external tools needed. 4. All values visible in one panel.

## Day 2 — Story 084
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Notes Capture
- **Parent Task:** Contextual Review Notes
- **Task Name:** Enhanced Quarterly Specialist Notes Section
- **User Story:** As a Specialist, I need an integrated Notes panel that shows prior quarterly notes side-by-side with the new entry so that I can reference previous feedback without opening separate pages.
- **Description:** Specialists currently open past notes manually to compare pricing changes, staffing updates, or operational issues. A split-view UI should allow historical and new notes to appear together.
- **Acceptance Criteria:** 1. Prior quarterly notes auto-load in a scrollable panel. 2. New note entry field visible simultaneously. 3. No manually opening previous quarters.

## Day 2 — Story 085
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Pricing Risk Alerts
- **Parent Task:** Price Change Monitoring
- **Task Name:** Detect Unannounced Price Increases
- **User Story:** As a Specialist, I want the system to warn me when a provider increases pricing without notifying Vendor Management so I can quickly address issues that would otherwise generate Accounting Inquiries.
- **Description:** Currently pricing increases are detected only when an AI appears. System should compare invoice totals to expected pricing and flag deviations proactively.
- **Acceptance Criteria:** 1. System auto-detects pricing deviations. 2. Notification banner appears on provider page. 3. Deviations logged for audit.

## Day 2 — Story 086
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Workflow Optimization
- **Parent Task:** Auto-Populate Known Provider Data
- **Task Name:** Auto-Fill Payment/Invoice Preferences
- **User Story:** As a Specialist, I want the quarterly screen to auto-fill known payment methods, invoicing preferences, and fee details so I only update changes rather than re-entering static info.
- **Description:** Currently specialists re-key payment preferences every quarter even though data rarely changes.
- **Acceptance Criteria:** 1. Payment method auto-populates from provider record. 2. Editable if changes exist. 3. â€œChange detectedâ€ highlights appear.

## Day 2 — Story 087
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Metrics Automation
- **Parent Task:** Quarterly Data Processing
- **Task Name:** Auto-Generate Target Sales and Performance Metrics
- **User Story:** As a Vendor Management Specialist, I want the system to automatically calculate target sales, missed opportunities, quarterly revenue totals, averages, and expected revenue so that I no longer need to perform multi-step manual calculations using external Word documents.
- **Description:** Specialists currently enter opportunities Ã— target close ratio, manually compute target sales, grab revenue per month, compute monthly averages and expected revenue, then retype the values into the quarterly form. This process is error-prone and time-consuming. Automating the calculations will ensure accuracy and reduce review time.
- **Acceptance Criteria:** 1. System auto-fills target sales based on defined close ratio. 2. Missed opportunities computed automatically. 3. Revenue totals auto-pulled from corresponding quarterly data. 4. All formulas match the existing Word guide exactly. 5. Specialist can override values if needed with audit logging.

## Day 2 — Story 088
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Metrics Automation
- **Parent Task:** Quarterly Data Entry
- **Task Name:** Auto-Fill Quarterly Revenue Fields
- **User Story:** As a Specialist, I want the UI to auto-populate quarterly revenue fields for July, August, and September (or correct quarter months) so I no longer need to retrieve and type them manually from separate reports.
- **Description:** System currently requires switching between multiple pages: revenue report, quarterly guide, VM ticket. The UI should pull the correct revenue per month and load it directly into the quarterly check-in panel.
- **Acceptance Criteria:** 1. System displays revenue for all three months of the selected quarter. 2. Revenue totals and average per sale computed automatically. 3. No manual retyping needed.

## Day 2 — Story 089
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Price Comparison Workflow
- **Parent Task:** Pricing Review
- **Task Name:** Auto-Detect Completed Price Comparison
- **User Story:** As a Specialist, I want the system to recognize when a price comp has already been completed and automatically populate the price comp status and date so I do not have to search or manually confirm it.
- **Description:** Specialists currently search previous price comps manually. System should store latest price comp date and status and auto-insert it into the quarterly form.
- **Acceptance Criteria:** 1. Last completed price comp date auto-populated. 2. Status displayed clearly (Competitive/Not Competitive). 3. Flags appear if pricing is outdated or expired.

## Day 2 — Story 090
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Payment Verification
- **Parent Task:** Payment Method UI
- **Task Name:** Smart Payment Issue Prompting
- **User Story:** As a Specialist, I need the system to automatically show a required 'Payment Notes' field only when a payment issue is marked 'Yes' so that I do not need to manage red asterisk validation manually.
- **Description:** Currently a red asterisk appears only after selecting 'Yes'. The system should trigger intelligent field expansion and prompt users with structured note requirements.
- **Acceptance Criteria:** 1. Selecting 'Yes' expands the notes field automatically. 2. Notes field becomes required. 3. Selecting 'No' collapses the field. 4. Validation prevents saving incomplete entries.

## Day 2 — Story 091
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Comparison Tools
- **Parent Task:** Quarter-over-Quarter Review
- **Task Name:** Side-by-Side Quarterly Comparison Panel
- **User Story:** As a Specialist, I want a side-by-side comparison UI that displays last quarterâ€™s key metrics next to the current quarter so I can quickly assess improvement or decline without manually opening old quarterly forms.
- **Description:** Currently specialists manually open the previous check-in to compare sales volume, pricing changes, staffing changes, and operational issues. The new UI should load prior quarter values automatically.
- **Acceptance Criteria:** 1. Previous quarter data displayed alongside current quarter entry. 2. Clear indicators show increase/decrease trends. 3. Zero need to manually open old records.

## Day 2 — Story 092
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Metric Flagging
- **Parent Task:** Performance Alerts
- **Task Name:** Auto-Generate Red Flags for Significant Changes
- **User Story:** As a Specialist, I want the system to automatically flag when key indicators (sales, opportunities, pricing) differ significantly from the previous quarter so I can identify issues quickly.
- **Description:** Examples: Sales dropping from 20 to 3, unexpected pricing changes, or patterns that historically lead to accounting inquiries. These should trigger auto-warnings.
- **Acceptance Criteria:** 1. Thresholds configurable (e.g., >30% drop). 2. UI displays warning banners or icons. 3. Flags appear in dashboards and the quarterly form.

## Day 2 — Story 093
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Data Consistency
- **Parent Task:** Provider Information Review
- **Task Name:** Auto-Fill Provider Payment and Invoicing Details
- **User Story:** As a Specialist, I want the quarterly check-in form to auto-populate payment method, invoicing preferences, and billing notes so I donâ€™t need to re-enter stable provider information each quarter.
- **Description:** Specialists today retype payment method, invoicing method, and billing conditions even though this information is already stored on the providerâ€™s page.
- **Acceptance Criteria:** 1. System retrieves existing provider payment settings. 2. Fields are editable if changes occur. 3. Versioning or change log is stored.

## Day 2 — Story 094
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Notes Management
- **Parent Task:** Historical Notes Awareness
- **Task Name:** Integrated Quarterly Notes Timeline
- **User Story:** As a Specialist, I need an easy-to-read notes history showing pricing changes, staff updates, service issues, or support escalations so I can reference previous touchpoints during a quarterly check-in.
- **Description:** Currently specialists manually read past notes to recall events such as price jumps or staffing changes. The UI should keep a chronological, filterable notes timeline.
- **Acceptance Criteria:** 1. Timeline loads automatically for selected provider. 2. Filter by quarter, category, or tag. 3. Notes are non-editable historical records.

## Day 2 — Story 095
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Pricing Change Monitoring
- **Parent Task:** Price Audit Tool
- **Task Name:** Detect Unreported Price Increases
- **User Story:** As a Specialist, I want the system to detect and alert me when a provider charges a higher price than expected, indicating a potential unreported price increase that may trigger an Accounting Inquiry.
- **Description:** Providers frequently increase pricing without notifying Vendor Management. The system should compare expected vs actual charges and issue alerts.
- **Acceptance Criteria:** 1. System compares invoice price to stored rate. 2. Alerts appear when variance exceeds threshold. 3. Alerts logged and linked to quarterly review.

## Day 2 — Story 096
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Provider Engagement Tools
- **Parent Task:** Provider Communication
- **Task Name:** Generate Automated Monthly or Quarterly Provider Health Summaries
- **User Story:** As a Specialist, I want the system to generate a positive, readable monthly or quarterly performance summary that can be emailed to providers so they remain informed and engaged.
- **Description:** These summaries could show service volume, revenue generated, trends, and selected KPIs. Today, specialists must deliver this verbally or manually.
- **Acceptance Criteria:** 1. Summary template customizable. 2. Auto-populated metrics. 3. Can be emailed directly. 4. Option for monthly or quarterly cadence.

## Day 2 — Story 097
- **Epic:** Quarterly Service Provider Health Review
- **Feature:** Quarterly Workflow Completion
- **Parent Task:** Ticket Closure
- **Task Name:** Auto-Insert Quarterly Summary Into VM Ticket
- **User Story:** As a Specialist, I want the system to automatically inject all quarterly summary data into the VM ticket resolution field so that I do not need to manually copy/paste the entire summary.
- **Description:** Currently specialists manually paste the compiled quarterly summary into the resolution summary. Automating this reduces double work.
- **Acceptance Criteria:** 1. System populates resolution summary on save. 2. User can review and edit before closing. 3. Closing the ticket stores the final version.

## Day 2 — Story 098
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** Document Management
- **Parent Task:** Centralized Document Access
- **Task Name:** Auto-Pull PSP Files From SharePoint Into Cube
- **User Story:** As a Vendor Management Specialist, I want Cube to automatically pull all PSP-related files (price comps, agreements, service area sheets) from SharePoint and similar repositories into a standardized in-app document section so I no longer have to search across multiple locations.
- **Description:** Files related to PSP setup and quarterly check-ins are currently scattered across SharePoint and external folders. Users must manually find, download, and reupload documents during workflows. A centralized document section should automatically sync all relevant files by provider.
- **Acceptance Criteria:** 1. System automatically fetches and displays all PSP files by provider. 2. Files appear in a single UI section with filters. 3. Sync occurs without duplicate uploads. 4. Permissions follow existing vendor management rules.

## Day 2 — Story 099
- **Epic:** PSP Quarterly Automation
- **Feature:** Quarterly Processing
- **Parent Task:** Quarterly Workflow Automation
- **Task Name:** Eliminate Manual Math Steps for Quarterly Check-In
- **User Story:** As a Specialist, I want the system to remove all manual math (percentages, ratios, revenue averaging) from the quarterly check-in process so I no longer need calculators or spreadsheets to complete the required quarterly report.
- **Description:** Specialists currently perform every calculation manually: opportunity counts Ã— target close ratio, missed opportunities, averages, percent to goal, quarterly totals, and expected revenue. Eliminating this significantly reduces time and error risk.
- **Acceptance Criteria:** 1. All quarterly computational fields auto-populate. 2. No calculator use required. 3. UI displays formulas transparently for audit. 4. Specialist can override with notes. 5. Calculations match prior quarterly guide.

## Day 2 — Story 100
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** Points & Productivity
- **Parent Task:** Quarterly Check-In Scoring
- **Task Name:** Auto-Award Points After Completing Quarterly Check-In
- **User Story:** As a Specialist, I want points to be automatically awarded when I complete a quarterly check-in so productivity metrics remain accurate without manually tying them to spreadsheet-heavy work.
- **Description:** Currently specialists complete extensive manual work but receive the same points regardless of complexity. Once math is eliminated and automation is added, point assignment should be tied to actual workflow completion inside Cube.
- **Acceptance Criteria:** 1. Points awarded automatically when quarterly check-in is closed. 2. Points visible on user dashboard. 3. No duplicate points awarded. 4. Manager view displays team totals.

## Day 2 — Story 101
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** PSP Dashboard
- **Parent Task:** PSP Task Visibility
- **Task Name:** Custom PSP Specialist Dashboard With Relevant Metrics Only
- **User Story:** As a PSP Specialist, I want a dashboard that shows only the metrics relevant to my daily work (open VM tickets, open AIs, providers needing outreach) so I am not forced to navigate irrelevant company-wide dashboards.
- **Description:** The current Quickbase home dashboard displays generalized system-wide stats that do not help specialists start their day. A new PSP-focused dashboard must provide personalized information tied only to the logged-in specialist.
- **Acceptance Criteria:** 1. Dashboard loads specialist-specific VM tickets. 2. Dashboard shows accounting inquiries tied to their assigned PSPs. 3. No irrelevant global or company-wide widgets shown. 4. Dashboard loads in <2 seconds.

## Day 2 — Story 102
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** PSP Dashboard
- **Parent Task:** PSP To-Do Panel
- **Task Name:** Show Assigned Open VM Tickets on Dashboard
- **User Story:** As a Specialist, I need my dashboard to clearly show all open VM tickets assigned to me so I can begin my day without manually searching for outstanding work.
- **Description:** Specialists currently locate tickets manually, leading to delays, missed priorities, and confusion. Displaying open tickets directly on the dashboard removes the need for navigation and improves response time.
- **Acceptance Criteria:** 1. Widget lists open VM tickets assigned to logged-in user. 2. Sort by due date, priority, or status. 3. Clicking opens ticket detail. 4. Zero display of tickets belonging to other specialists.

## Day 2 — Story 103
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** PSP Dashboard
- **Parent Task:** Accounting Inquiry Visibility
- **Task Name:** Show Open Accounting Inquiries Assigned to PSP Specialist
- **User Story:** As a Specialist, I want any accounting inquiries tied to my PSP providers to appear on my dashboard so I can follow up proactively.
- **Description:** Accounting inquiries impact PSP relationships and often reveal pricing or service issues. Specialists need immediate visibility to resolve them quickly.
- **Acceptance Criteria:** 1. Dashboard shows all AIs tied to provider relationships assigned to the specialist. 2. Results auto-refresh daily. 3. AIs link to detailed discrepancy view.

## Day 2 — Story 104
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** PSP Dashboard
- **Parent Task:** Role-Based Filtering
- **Task Name:** Specialist Dashboard Should Filter to â€œMine Onlyâ€ By Default
- **User Story:** As a Specialist, I want the dashboard to show only my tickets and my accounting inquiries by default so that I do not have to filter the view manually each morning.
- **Description:** The current dashboard displays system-wide information. Specialists do not share accounts and do not need to see teammatesâ€™ workloads.
- **Acceptance Criteria:** 1. Default filter = logged-in user. 2. No cross-specialist data shown. 3. Performance remains optimal with filtered dataset.

## Day 2 — Story 105
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** Administrative Dashboard
- **Parent Task:** Admin View
- **Task Name:** Global Ticket Dashboard for Managers
- **User Story:** As an Admin or Manager, I want to view all PSP-related tickets, inquiries, and workload metrics across all specialists so I can monitor productivity and intervene when workloads spike.
- **Description:** Admin-level users need the opposite of specialists: a global view across all PSP specialists to check bottlenecks, overdue items, and metrics.
- **Acceptance Criteria:** 1. Manager dashboard shows all specialists' tickets with filters by user. 2. Supports sorting, filtering, and exporting. 3. Access restricted to admin roles.

## Day 2 — Story 106
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** Administrative Dashboard
- **Parent Task:** Hierarchy-Aware Reporting
- **Task Name:** Create Multi-Level Reporting Views for PSP Team
- **User Story:** As a Manager, I want multi-level reporting options that show data by individual specialist, by team, and by entire department so I can analyze PSP performance at different levels of granularity.
- **Description:** This allows comparisons such as: individual performance vs. team goals, cross-specialist throughput, or quarterly workload distribution.
- **Acceptance Criteria:** 1. Reporting supports three levels: individual, team, department. 2. Views switchable via toggle. 3. Data remains accurate and consistent across levels.

## Day 2 — Story 107
- **Epic:** PSP Dashboard & Workflow Improvements
- **Feature:** Administrative Dashboard
- **Parent Task:** Role-Based View Logic
- **Task Name:** Role-Based Report Switching Between Specialist and Admin Views
- **User Story:** As a System User, I want Cube to automatically load the correct dashboard (Specialist View or Admin View) depending on my role so I do not have to manually navigate to different report pages.
- **Description:** Pilar only needs her own data; Sandra needs the full team. The system should decide what to show automatically.
- **Acceptance Criteria:** 1. Specialist role â†’ loads filtered personal dashboard. 2. Admin role â†’ loads global dashboard. 3. Permissions enforced in backend. 4. Toggle available only if permitted.

## Day 2 — Story 108
- **Epic:** Vendor Management - Non-PSP Workflows
- **Feature:** Role Delineation & Workflow Separation
- **Parent Task:** Non-PSP Workflow Logic
- **Task Name:** Define Non-PSP Handling Rules
- **User Story:** As a vendor management specialist (non-PSP), I want the system to automatically route PSP-related tickets to the assigned PSP specialist so that I only see and manage the tickets relevant to my responsibility scope.
- **Description:** The transcript confirms that Sidi should not handle PSP haulers, PSP AIs, PSP VM tickets, or PSP pricing-related tasks. The system must enforce this separation by auto-routing tickets and preventing PSP data from appearing in non-PSP work queues.
- **Acceptance Criteria:** 1) System auto-routes all PSP-flagged tickets to the assigned PSP specialist. 2) Non-PSP specialists never see PSP tickets unless manually reassigned by a manager. 3) UI displays a confirmation message indicating auto-routing. 4) Audit log records routing.

## Day 2 — Story 109
- **Epic:** Vendor Management - Dashboards
- **Feature:** Dashboard Improvements
- **Parent Task:** Specialist Daily Workflow
- **Task Name:** Filtered VM Ticket Dashboard for Non-PSP Specialists
- **User Story:** As a VM specialist, I want a dashboard that shows only the VM tickets assigned to me and excludes PSP-related tickets so that I can immediately see what requires my action each day.
- **Description:** Transcript shows current dashboard is unusable and shows all tickets mixed together. Sidi manually filters tickets every morning. A dedicated filtered dashboard is needed showing only: open non-PSP VM tickets assigned to the logged-in specialist.
- **Acceptance Criteria:** 1) Dashboard loads with pre-filtered list of non-PSP tickets. 2) Logged-in specialist only sees their own assigned tickets. 3) No PSP tickets appear. 4) Load time under 2 seconds. 5) Must allow sorting by priority.

## Day 2 — Story 110
- **Epic:** Vendor Management - Prioritization
- **Feature:** Ticket Prioritization UI
- **Parent Task:** Ticket Visibility & Sorting
- **Task Name:** Critical Tickets First View
- **User Story:** As a VM specialist, I want the dashboard to highlight and surface critical-priority VM tickets so that I can quickly identify the most urgent items and address them first.
- **Description:** Transcript shows Sidi always handles critical tickets first and wants them surfaced without manual filtering. UI should visually emphasize critical items and place them at the top.
- **Acceptance Criteria:** 1) Critical tickets appear in a dedicated â€œCritical Priorityâ€ section or automatically sort to top. 2) Clear visual indicator (badge, highlight, or color). 3) Can click to expand full ticket detail. 4) Works on desktop and mobile.

## Day 2 — Story 111
- **Epic:** Vendor Management - UX Enhancements
- **Feature:** Dashboard Shortcut
- **Parent Task:** Home Screen Optimization
- **Task Name:** Add Direct VM Ticket Access From Dashboard
- **User Story:** As a VM specialist, I want a direct dashboard shortcut that takes me straight to my filtered VM ticket list so I do not need to maintain browser tabs or navigate through multiple screens.
- **Description:** Transcript shows Sidi keeps a personal saved browser tab because dashboard is not useful. She requests dashboard shortcut for instant access.
- **Acceptance Criteria:** 1) Dashboard contains a â€œMy VM Ticketsâ€ button. 2) Clicking opens the filtered view showing only userâ€™s non-PSP tickets. 3) Navigation requires max 1 click. 4) Role-based filtering enforced.

## Day 2 — Story 112
- **Epic:** Vendor Management - Role Coverage
- **Feature:** Role Sharing & Backup Rules
- **Parent Task:** Team Workflows
- **Task Name:** Unified VM/COI/W9 Permissions for Backup Coverage
- **User Story:** As a VM specialist, I want the system to allow me and Delicia to fully cover each otherâ€™s roles (VM tickets, COIs, W-9s) so that work continues smoothly when one of us is out.
- **Description:** Transcript confirms Delicia and Sidi cover each other: COIs/W9s when one is out and VM tickets when the other is out. System must ensure shared access and permissions.
- **Acceptance Criteria:** 1) Role permissions allow both users to view/edit COIs, W-9s, and VM tickets. 2) Dashboard adjusts dynamically when a specialist is covering. 3) Audit logs show who performed the work. 4) No access restriction errors occur.

## Day 2 — Story 113
- **Epic:** Vendor Management â€“ Ticket Intake & Routing
- **Feature:** Ticket Routing Logic
- **Parent Task:** Assignment Rules
- **Task Name:** Automatic PSP vs Non-PSP Routing Determination
- **User Story:** As a VM specialist, I want the system to automatically determine whether a VM ticket should be routed to a PSP specialist or to me based on the service providerâ€™s PSP status so that I no longer need to manually act as the â€œtraffic copâ€ for every new ticket.
- **Description:** Transcript shows Sidi manually checks every incoming ticket to determine whether a hauler is PSP-managed. She assigns PSP tickets to PSP specialists and keeps others for herself. This routing is currently manual, error-prone, and requires her to inspect each page. System must automate this logic using hauler metadata.
- **Acceptance Criteria:** 1) System identifies PSP status from hauler record. 2) Automatically assigns PSP tickets to the assigned PSP specialist. 3) Automatically assigns non-PSP tickets to the VM specialist. 4) UI indicator explains the routing logic. 5) Routing appears in audit log.

## Day 2 — Story 114
- **Epic:** Vendor Management â€“ Ticket Intake & Routing
- **Feature:** Dashboard Toggle
- **Parent Task:** Assignment Flexibility
- **Task Name:** Toggle Between â€œMy Ticketsâ€ and â€œAll Ticketsâ€
- **User Story:** As a VM specialist, I want a toggle that switches between (1) my assigned + unassigned tickets and (2) all VM tickets, so that I can cover other specialistsâ€™ workload when needed but still default to my own work.
- **Description:** Transcript shows Sidi needs to handle her own tickets but also occasionally must step in to work tickets assigned to others or reassign misrouted PSP tickets. A toggle is required for switching views quickly.
- **Acceptance Criteria:** 1) Dashboard loads in â€œMy Ticketsâ€ mode by default. 2) Toggle instantly switches to â€œAll Ticketsâ€ mode. 3) Counts update dynamically. 4) System maintains filters when switching back. 5) Permission rules prevent unauthorized access.

## Day 2 — Story 115
- **Epic:** Vendor Management â€“ Ticket Intake & Routing
- **Feature:** Auto-Assignment Enhancements
- **Parent Task:** Traffic-Cop Workflow Removal
- **Task Name:** Automated Assignment of New/Unassigned Tickets
- **User Story:** As a VM specialist, I want new tickets that arrive unassigned to automatically assign themselves to the appropriate resource (PSP or VM) so I no longer have to manually assign every incoming ticket.
- **Description:** Transcript shows every newly submitted ticket is unassigned. Sidi manually inspects each one, determines its category, and assigns it. Automation should replace manual evaluation.
- **Acceptance Criteria:** 1) System checks hauler record or ticket metadata. 2) Assigns to correct person within 1 second. 3) Shows a UI toast: â€œTicket auto-assigned to X based on hauler type.â€ 4) Prevents tickets from remaining unassigned for more than 30 seconds.

## Day 2 — Story 116
- **Epic:** Vendor Management â€“ New Service Provider Intake
- **Feature:** New Provider Intake Flow
- **Parent Task:** Intake Process
- **Task Name:** Unified New Service Provider Workflow
- **User Story:** As a VM specialist, I want a single, unified intake workflow for new service providers so that requests from AMs, Fulfillment, or providers themselves no longer cause confusion or result in fragmented processes.
- **Description:** Transcript shows two inconsistent processes: (1) AMs sometimes create hauler pages first, (2) sometimes VM receives raw information and must build the page, and (3) there are two separate meaning fields for â€œnew provider.â€ A unified flow is needed.
- **Acceptance Criteria:** 1) System presents one standardized â€œNew Provider Intakeâ€ form. 2) Form captures: who submitted, whether provider is requesting to work with us vs. we need to use them urgently, required fields, attachments. 3) System auto-creates hauler page if missing. 4) Eliminates dual-field confusion.

## Day 2 — Story 117
- **Epic:** Vendor Management â€“ UX Cleanup
- **Feature:** Field Meaning Clarity
- **Parent Task:** Form Design
- **Task Name:** Clarify the Two â€œNew Providerâ€ Fields
- **User Story:** As a user, I want clear wording, tooltips, and examples distinguishing â€œprovider wants to work with usâ€ vs â€œwe need to use them immediatelyâ€ so that staff no longer misinterpret these fields.
- **Description:** Transcript shows both Justin and Sidi agree the two inputs are confusing and users canâ€™t tell which field applies. Sidi developed her own interpretation because the UI does not explain the difference.
- **Acceptance Criteria:** 1) Two field labels rewritten with precise language. 2) Each includes a tooltip explaining correct use case. 3) UI validation requires choosing the correct one. 4) System warns if contradictory selections occur.

## Day 2 — Story 118
- **Epic:** Vendor Management â€“ Workflow Intelligence
- **Feature:** Hauler Record Verification
- **Parent Task:** Data Validation Automation
- **Task Name:** Detect Existing Hauler Pages Before Intake
- **User Story:** As a VM specialist, I want the system to detect when a hauler already exists so that duplicate hauler pages are never created and intake is streamlined automatically.
- **Description:** Transcript shows this scenario: The ticket claims â€œnew service providerâ€ but a hauler page already exists because Sierra (AM) created it earlier. System must detect and adjust workflow accordingly.
- **Acceptance Criteria:** 1) System checks for existing hauler record by name, phone, EIN, or email. 2) If found, system displays: â€œExisting Hauler Found â€“ Page Linked Automatically.â€ 3) Prevents duplicate hauler creation. 4) Links ticket to existing hauler.

## Day 2 — Story 119
- **Epic:** Vendor Management â€“ Intake & Request Simplification
- **Feature:** Field Consolidation
- **Parent Task:** New Provider Request Fields
- **Task Name:** Unify New Provider Request Inputs
- **User Story:** As a VM specialist, I want the system to replace the two confusing â€˜new provider requestâ€™ fields with a single, unified field so that the intake process is clear, simplified, and aligned with how I actually process these requests.
- **Description:** Sidi states the two existing fields (provider wants to work with us vs. we need to work with them urgently) cause confusion and that she processes both identically. Transcript confirms both types are treated as critical and handled the same way. The UI must consolidate these inputs into one clear field.
- **Acceptance Criteria:** 1) One consolidated field replaces both legacy fields. 2) Tooltip explains that this field covers all new provider scenarios. 3) Historical data migrated cleanly. 4) Forms validate correctly with no user confusion. 5) No workflows break due to removal of old fields.

## Day 2 — Story 120
- **Epic:** Vendor Management â€“ Hauler Creation Rules
- **Feature:** Permissions & Governance
- **Parent Task:** Hauler Page Creation
- **Task Name:** Restrict Hauler Page Creation to VM Specialists
- **User Story:** As a VM specialist, I want only VM staff to be able to create new hauler pages so that duplicate pages, inaccurate data entry, and unnecessary hauler records are eliminated.
- **Description:** Transcript shows frequent issues: account managers and fulfillment teams create hauler pages prematurely, incorrectly, or for providers we cannot even use. This results in duplicate pages, unused pages, and incorrect data that Sidi must later fix. Restricting creation prevents bad data from entering the system.
- **Acceptance Criteria:** 1) Only VM-role users can create new hauler pages. 2) Non-VM attempt triggers a guided â€œSubmit New Provider Ticket Insteadâ€ workflow. 3) System logs creation source. 4) No duplicates created through non-VM pathways.

## Day 2 — Story 121
- **Epic:** Vendor Management â€“ Duplicate Prevention
- **Feature:** Duplicate Detection
- **Parent Task:** Data Integrity
- **Task Name:** Automatic Detection of Existing Hauler Pages Before Creation
- **User Story:** As a VM specialist, I want the system to automatically detect existing hauler records by phone, email, EIN, and company name so that duplicate hauler pages are never created.
- **Description:** Sidi describes constant duplication because non-VM staff do not check first. Sidi manually searches by phone/email/domain to find existing pages. System must do this automatically before allowing creation.
- **Acceptance Criteria:** 1) System checks multiple identifiers before creating a hauler: phone, email, domain, EIN, normalized name. 2) If matches found, UI displays: â€œExisting Hauler Detected: Link Instead of Create.â€ 3) Duplicate creation blocked. 4) Overrides require VM-level approval.

## Day 2 — Story 122
- **Epic:** Vendor Management â€“ Intake Cleanup
- **Feature:** Inactive Provider Filtering
- **Parent Task:** System Cleanliness
- **Task Name:** Prevent Creation of Hauler Pages for Providers We Cannot Use
- **User Story:** As a VM specialist, I want the system to block creation of hauler pages for providers we cannot legally, logistically, or operationally work with so that the system does not fill with unusable providers.
- **Description:** Sidi states that AMs sometimes submit companies we cannot work with, causing unnecessary pages that later â€œjust sit there.â€ This leads to clutter and complaints. System should validate eligibility before creation.
- **Acceptance Criteria:** 1) Intake flow includes eligibility rules (service area, insurance requirements, compliance status). 2) If not eligible, system blocks creation and instructs AM to decline provider. 3) VM receives no unusable pages.

## Day 2 — Story 123
- **Epic:** Vendor Management â€“ Relationship Management
- **Feature:** Related Hauler Mapping
- **Parent Task:** Company Linking
- **Task Name:** Improve Understanding of â€œRelated Hauler (Purchasing)â€ Field
- **User Story:** As a VM specialist, I want the system to clarify and enforce correct usage of the â€œrelated hauler purchasingâ€ field so that staff understand when to link a hauler to an acquired company.
- **Description:** Transcript: Sidi explains this field is intended for scenarios where one company bought another. Justin and others admit the meaning is unclear. UI must clarify purpose and guide proper use.
- **Acceptance Criteria:** 1) Field label rewritten (e.g., â€œAcquired Company / Former Ownershipâ€). 2) Tooltip describes usage with an example. 3) Form validation prevents using it on unrelated tickets. 4) System links records correctly in back-end.

## Day 2 — Story 124
- **Epic:** Vendor Management â€“ Ticket Intake UI
- **Feature:** New Hauler Form
- **Parent Task:** Required Fields
- **Task Name:** Expand Minimum Required Fields for New Hauler Intake
- **User Story:** As a VM specialist, I want the new hauler intake section to include all required fields (email, full address, phone, etc.) so that I no longer must manually re-collect missing critical data from submitters.
- **Description:** Transcript shows current intake fields are incomplete (missing email, city/state often empty). Staff place info in random boxes. Sidi must correct it manually. Form must enforce completeness.
- **Acceptance Criteria:** 1) Required fields include: company name, full business address, billing address, email, phone, service areas, contact name. 2) Form cannot submit unless complete. 3) Clear inline validation.

## Day 2 — Story 125
- **Epic:** Vendor Management â€“ Contact Validation
- **Feature:** Address Accuracy
- **Parent Task:** Data Cleanup
- **Task Name:** Enforce Proper Collection of Business vs Billing Addresses
- **User Story:** As a VM specialist, I want the system to clearly differentiate business address vs billing address and require both when needed so that incorrect or partial data stops entering the system.
- **Description:** Transcript shows staff often enter only billing address, or put the wrong address in the wrong place, and Sidi must manually correct it. System must enforce proper collection.
- **Acceptance Criteria:** 1) Clearly separated â€œBusiness Addressâ€ and â€œBilling Addressâ€ sections. 2) Tooltip guidance + examples. 3) Required fields validated. 4) Form warns user if same address appears repeatedly.

## Day 2 — Story 126
- **Epic:** Vendor Management â€“ Address Clarification
- **Feature:** Address Fields
- **Parent Task:** Business vs Billing Address
- **Task Name:** Clarify and Enforce Correct Address Usage
- **User Story:** As a VM specialist, I want the UI to clearly distinguish which address is intended for billing vs business so that I no longer guess which address should populate the hauler record and avoid inconsistent data entry.
- **Description:** Sidi and Justin discuss confusion around which address belongs where: top section is interpreted as business address, but often ends up being billing; Intacct feeds billing address automatically; users donâ€™t know which address becomes part of the name. The system must clearly label, guide, and enforce correct usage.
- **Acceptance Criteria:** 1) Labels explicitly say â€œBusiness Address (Physical Location)â€ and â€œBilling Address (Intacct Synced).â€ 2) Tooltip explains relationship with COI/W9 and Intacct sync. 3) UI prevents saving if business address is empty. 4) Intacct-sync indicator explains where the billing address originated.

## Day 2 — Story 127
- **Epic:** Vendor Management â€“ Intacct Sync Visibility
- **Feature:** Intacct Integration
- **Parent Task:** Vendor Sync Status
- **Task Name:** Improve Visibility of Intacct-Generated Billing Address
- **User Story:** As a VM specialist, I want the UI to clearly show when the billing address is auto-synced from Intacct so that I do not confuse it with a manually entered business address.
- **Description:** Justin explains the Intacct back-end sync, including the â€œprint asâ€ logic and the Boolean override for early vendor creation. Sidi didnâ€™t know this, leading to misuse. UI must show origin and purpose of synced billing address.
- **Acceptance Criteria:** 1) Billing address field displays a â€œSynced from Intacctâ€ badge. 2) Tooltip shows last sync timestamp. 3) When override checkbox is used, UI displays â€œWill sync immediately to Intacct.â€ 4) Billing address is read-only unless user has specific permissions.

## Day 2 — Story 128
- **Epic:** Vendor Management â€“ Contact Standardization
- **Feature:** Hauler Contacts
- **Parent Task:** Primary Contact Migration
- **Task Name:** Convert Primary Contact Fields into Contact Records
- **User Story:** As a VM specialist, I want the primary contact fields to automatically convert into their own contact record so that contact management becomes consistent and no longer split between the hauler page and the contacts table.
- **Description:** Transcript: Justin explains the cube model requires removing the first contact from the haulerâ€™s main fields and converting it into a contact record like all others. Current system inconsistently stores the first contact separately and additional contacts in a table; this must be unified.
- **Acceptance Criteria:** 1) System automatically creates a primary contact record on page creation. 2) UI removes standalone primary contact fields. 3) Import script migrates existing primary fields to contact records. 4) VM confirms data accuracy across a test set.

## Day 2 — Story 129
- **Epic:** Vendor Management â€“ Contact Structure Redesign
- **Feature:** Hauler Contacts
- **Parent Task:** Multi-Contact Structure
- **Task Name:** Support Multiple Contact Types with Dedicated Fields
- **User Story:** As a VM specialist, I want each contact to support fields such as landline, mobile, SMS, after-hours, dispatching, billing, and primary so that every contact method is categorized correctly and not mixed together in free-form fields.
- **Description:** Transcript shows confusion: Sidi uses â€œadd hauler contactâ€ only for secondary contacts, while the main contact is improperly stored in hauler fields. Justin describes future model: each contact should have a structured record with all necessary numbers and types. UI must fully support this.
- **Acceptance Criteria:** 1) Contact record includes: Landline, Mobile, SMS, After-hours, Billing contact, Dispatch contact, Primary flag. 2) UI enforces selection of a contact type (Primary, Secondary, Dispatching, Billing, After Hours). 3) No duplicate phone entries. 4) Hauler page displays contacts grouped by type.

## Day 2 — Story 130
- **Epic:** Vendor Management â€“ Email Cleanup
- **Feature:** Email Fields
- **Parent Task:** Primary Email Logic
- **Task Name:** Prevent Duplicate Email Placement Across UI
- **User Story:** As a VM specialist, I want the system to prevent duplicate email entries and clarify primary email assignment so that mass emails do not accidentally send duplicates and contact data remains clean.
- **Description:** Transcript shows users frequently place the same email in multiple fields due to unclear UI distinctions. This leads to duplicate mass emails and clutter. Contact records will eliminate this redundancy but must enforce primary selection.
- **Acceptance Criteria:** 1) â€œPrimary Emailâ€ is selectable via a dropdown on a contact record. 2) UI prevents duplicate placement of the same email across multiple contact records. 3) Warning appears if email matches another record for the same hauler. 4) Hauler page displays only one primary email.

## Day 2 — Story 131
- **Epic:** Vendor Management â€“ Contact Migration
- **Feature:** Data Migration
- **Parent Task:** Legacy Field Removal
- **Task Name:** Remove Legacy Email/Phone Fields and Replace With Contact Records
- **User Story:** As a PM/UX designer, I want to remove legacy hauler-level email/phone fields that were created before the contacts subtable existed so that all communication data lives within the standardized contact system.
- **Description:** Justin states this entire section (â€œmain email, primary email, website, portal credsâ€) will be removed in the Cube and replaced with contact records. Migration must safely transpose existing data.
- **Acceptance Criteria:** 1) All legacy fields mapped to contact records. 2) No data loss in migration. 3) Hauler UI redesign excludes legacy fields entirely. 4) Stakeholders validate at least 10 migrated records for accuracy.

## Day 2 — Story 132
- **Epic:** Vendor Management â€“ Notes Optimization
- **Feature:** Notes Handling
- **Parent Task:** Field Conversion
- **Task Name:** Convert Frequently Repeated Notes Into Structured Fields
- **User Story:** As a VM specialist, I want repeatedly documented information (e.g., payment terms) converted into structured fields so I do not have to enter them into free-form notes every time.
- **Description:** Justin asks Sidi what she always puts in notes. She confirms she routinely places payment terms there because accounting fields changed and she avoids that tab. System needs structured field for payment terms.
- **Acceptance Criteria:** 1) New field: â€œPayment Terms (Hauler Provided).â€ 2) UI places it within vendor management area rather than accounting-only area. 3) Required when onboarding. 4) VM confirms they no longer place payment terms into notes.

## Day 2 — Story 133
- **Epic:** Vendor Management â€“ Accounting Field Clarification
- **Feature:** Accounting Tab
- **Parent Task:** Field Ownership
- **Task Name:** Clarify Which Payment Fields VM Should Enter vs. Accounting
- **User Story:** As a VM specialist, I want clear guidance on which payment-related fields I should complete so that I no longer avoid the Accounting tab due to fear of disrupting accounting processes.
- **Description:** Transcript says Sidi stopped entering payment details because changes were made and she wasnâ€™t sure what was safe, causing lost data. System needs explicit boundaries.
- **Acceptance Criteria:** 1) UI labels identify â€œVM-owned fieldsâ€ vs â€œAccounting-only fields.â€ 2) Fields greyed out if not VM editable. 3) Tooltip explains workflow. 4) Training hint banner appears for first-time users.

## Day 2 — Story 134
- **Epic:** Vendor Management â€“ Payment Method UI
- **Feature:** Payment Fields
- **Parent Task:** Payment Workflow
- **Task Name:** Use Dedicated Payment Type Fields
- **User Story:** As a VM specialist, I want the UI to clearly support selecting accepted payment methods (Visa, MC, Discover, AmEx, etc.) so that I no longer type these into notes and can rely on structured, reportable data.
- **Description:** Sidi admits she was placing accepted payment types into notes because she didnâ€™t know the drop-down allowed multiple selections. Justin confirms the field supports multi-select. UX must ensure discoverability, enforce correct use, and stop relying on notes.
- **Acceptance Criteria:** 1) Multi-select payment method field is clearly labeled and visible. 2) A tooltip explains that multiple credit card types may be selected. 3) User cannot save if field is required and left empty. 4) Notes no longer needed for payment method logging.

## Day 2 — Story 135
- **Epic:** Vendor Management â€“ Reduce Note Overuse
- **Feature:** Notes Optimization
- **Parent Task:** Replace Notes With Fields
- **Task Name:** Convert Repeated Note Content Into Structured Controls
- **User Story:** As a VM specialist, I want the system to replace repeated note entries (e.g., â€œaccepts Visa/MasterCard/AmExâ€) with proper UI fields so I can reduce manual typing and avoid inconsistent data entry.
- **Description:** Sidi regularly placed payment acceptance information into notes because she feared modifying accounting fields. Justin clarified fields exist and should be used. The system must eliminate confusion and guide proper data placement.
- **Acceptance Criteria:** 1) Fields related to payment acceptance are in a VM-safe section. 2) Notes field is not used for any payment-related information. 3) Training pop-up appears when editing payment method fields for the first time. 4) Audit shows 0 new payment details in notes after rollout.

## Day 2 — Story 136
- **Epic:** Vendor Management â€“ Additional Note Categories
- **Feature:** Notes Handling
- **Parent Task:** Note Type Review
- **Task Name:** Identify Notes Frequently Used for Required Servicing
- **User Story:** As a VM specialist, I want defined structured fields for data I repeatedly enter as â€œrequired servicingâ€ notes so that critical operational requirements are not buried inside free-form notes.
- **Description:** Justin asks which items belong in notes vs. fields. Sidi mentions she uses notes for â€œrequired servicingâ€ needs. These should likely be structured fields to ensure they are surfaced properly.
- **Acceptance Criteria:** 1) UI displays structured field(s) for servicing requirements. 2) Notes field is reserved for unique, non-recurring details. 3) Servicing fields are included in workflows and reporting. 4) Validation ensures servicing details cannot be omitted.

## Day 2 — Story 137
- **Epic:** Historical Change Logging â€“ Email Records
- **Feature:** Email Logging
- **Parent Task:** Email Change Tracking
- **Task Name:** Auto-Log Email Address Changes
- **User Story:** As a VM specialist, I want the system to automatically create a historical log entry whenever an email address is added, removed, or updated so that users relying on old addresses can verify what changed and when.
- **Description:** Dellisha explains they manually log new/removed email addresses because contacts do not show prior addresses. Users often backtrack old addresses. This must be automated and standardized.
- **Acceptance Criteria:** 1) Every email-address change triggers an auto-generated log entry with timestamp, old value, new value, and user. 2) No manual notes required. 3) UI view available for historical email changes. 4) Actions appear in an activity log accessible to VM, PSP, and AM teams.

## Day 2 — Story 138
- **Epic:** Historical Change Logging â€“ Service Products
- **Feature:** Product Logging
- **Parent Task:** Service Change Tracking
- **Task Name:** Auto-Log New or Removed Service Types
- **User Story:** As a VM specialist, I want any update to a haulerâ€™s available service types (e.g., new products added) to automatically generate a historical log entry so that changes are documented without manually writing notes.
- **Description:** Dellisha shares that when haulers start servicing new products, they enter them into the service list AND manually add a note because people look in notes first. This work should be automated.
- **Acceptance Criteria:** 1) Adding/removing a service automatically logs a timestamped note. 2) Log includes: user, old value, new value, and reason (if provided). 3) Service changes appear in the activity timeline. 4) VM does not need to manually type service details into notes.

## Day 2 — Story 139
- **Epic:** UI Awareness â€“ Email Change Visibility
- **Feature:** Email Address Structure
- **Parent Task:** Email Tracking UX
- **Task Name:** Provide UI Indicators for Email Address History
- **User Story:** As a VM specialist, I want quick visibility into prior email addresses so that I can understand historical use without searching through free-form notes.
- **Description:** Transcript: Justin questions why users need logs; Dellisha confirms many staff backtrack old emails, even when new ones exist. System must surface this history clearly and reduce dependency on notes.
- **Acceptance Criteria:** 1) UI contains â€œEmail Historyâ€ modal or section. 2) Shows prior values, who changed them, and when. 3) No need to scroll through notes. 4) Ability to filter by communication type.

## Day 2 — Story 140
- **Epic:** Note Reduction â€“ Automated Change Logging
- **Feature:** Notes Automation
- **Parent Task:** Streamlined Change Tracking
- **Task Name:** Automate Logging for Repetitive Note Types
- **User Story:** As a PM/UX designer, I want the system to automatically create standardized log entries for changes to services, contact emails, or other repeated changes so that VM specialists spend less time on administrative note-taking.
- **Description:** Justin states multiple repeated tasks could be automatedâ€”service changes, email changes, etc. UX must eliminate manual duplication.
- **Acceptance Criteria:** 1) Auto-logging triggered by service updates, email changes, and contact modification. 2) Log entries standardized. 3) Manual notes only needed for contextual explanations. 4) VM confirms time saved through automation.

## Day 2 — Story 141
- **Epic:** Hauler Management & Onboarding
- **Feature:** Hauler Notes & Documentation
- **Parent Task:** Notes Standardization
- **Task Name:** Capture Pricing & Product Notes
- **User Story:** As a VM Specialist, I want an automated place to record pricing and product details so that I donâ€™t have to repeatedly type this information into free-form notes.
- **Description:** VM specialists currently manually enter pricing, unit sizes, and tonnage rules (e.g., $30/ton, flat-rate hauler) into notes for non-PSP haulers. They also document what product sizes a hauler carries (30yd, 40yd, etc.). These repetitive notes should be captured in structured fields to eliminate redundant typing.
- **Acceptance Criteria:** system provides structured fields for pricing methods, tonnage rules, and product sizing -@ specialist can enter product sizes directly without using notes -@ information is automatically Saved and displayed in a Consistent UI -@ Data appears on hauler profile &@ relevant Reports

## Day 2 — Story 142
- **Epic:** Hauler Management & Onboarding
- **Feature:** Product Availability
- **Parent Task:** Service Tab Enhancements
- **Task Name:** Record Detailed Product Availability
- **User Story:** As a VM Specialist, I want to select detailed product sizes and types (e.g., 30yd, 40yd, ADA portable toilets) so that hauler capabilities can be understood without referring to notes.
- **Description:** Currently, specialists write granular product details (sizes and types offered) into notes because the â€œServicesâ€ section is too limited. Specialists also log what a hauler does *not* offer (e.g., does not carry trailers). UI needs structured checkboxes for sub-types under each service category.
- **Acceptance Criteria:** - Service tab supports expandable sub-categories (e.g., Roll-Offs â†’ 10yd/20yd/30yd/40yd)  - Toilets include ADA, event trailer, handwash, etc.  - UI displays selected and unselected product types clearly  - Notes no longer required for product availability documentation

## Day 2 — Story 143
- **Epic:** Hauler Management & Onboarding
- **Feature:** Product Unavailability Tracking
- **Parent Task:** Service Tab Enhancements
- **Task Name:** Indicate Products Not Offered
- **User Story:** As a VM Specialist, I want the service tab to implicitly show what a hauler does *not* offer so that I donâ€™t need to type â€œdoes not carry Xâ€ in notes.
- **Description:** Today specialists record product unavailability manually (e.g., â€œdoes not carry trailersâ€). A structured service list with checkboxes automatically implies all unchecked items are â€œnot offered,â€ eliminating redundant notes.
- **Acceptance Criteria:** - Unchecked items are automatically treated as â€œnot offeredâ€  - No separate text entry required to document unavailable services  - UI explains that unchecked = not offered

## Day 2 — Story 144
- **Epic:** Hauler Management & Onboarding
- **Feature:** Hauler Hours & Cutoff Times
- **Parent Task:** Onboarding Requirements
- **Task Name:** Capture Operating Hours in Onboarding
- **User Story:** As a VM Specialist, I want all hauler operating hours (open, close, cutoff times) to be required and standardized so fulfillment always sees accurate scheduling windows.
- **Description:** Hours are inconsistently entered because fields are not required. Specialists currently capture hours during onboarding or update calls. Making these required ensures scheduling accuracy for fulfillment.
- **Acceptance Criteria:** onboarding UI requires open time, close time, and cutoff time -@ fields have validation rules (e.g., cutoff cannot be after close time) -@ Hours display clearly in Fulfillment dashboards

## Day 2 — Story 145
- **Epic:** Hauler Management & Onboarding
- **Feature:** Onboarding Workflow
- **Parent Task:** Onboarding Efficiency
- **Task Name:** Reduce Time Spent Asking Repetitive Questions
- **User Story:** As a VM Specialist, I want a streamlined onboarding UI so I donâ€™t have to ask haulers 20 minutesâ€™ worth of questions verbally.
- **Description:** Specialists currently spend long calls collecting every detail (payment terms, hours, contact info, equipment, services). This frustrates haulers and wastes time. A single onboarding workflow should gather all required fields efficiently.
- **Acceptance Criteria:** @ UI consolidates required onboarding fields into one guided Workflow -@ hauler can optionally self-@submit details online -@ mandatory fields clearly indicated

## Day 2 — Story 146
- **Epic:** Hauler Management & Onboarding
- **Feature:** Onboarding Form Automation
- **Parent Task:** Send Form to Hauler
- **Task Name:** Hauler Self-Service Onboarding Form
- **User Story:** As a VM Specialist, I want to email haulers a structured onboarding form so they can enter details themselves, reducing call time and missing details.
- **Description:** CD currently created her own manual form to gather details like hours, cutoff times, contacts, payment terms, and services. The system should generate a formal version automatically and log responses.
- **Acceptance Criteria:** @ system can generate a secure hauler onboarding form -@ form includes all required onboarding fields -@ Returned Data maps automatically into hauler record

## Day 2 — Story 147
- **Epic:** Hauler Management & Onboarding
- **Feature:** Recurring Hauler Updates
- **Parent Task:** Automated Periodic Validation
- **Task Name:** Automated Periodic Hauler Update Request
- **User Story:** As a VM Specialist, I want the system to periodically send haulers their current stored information and allow them to update anything that has changed.
- **Description:** Specialists currently update info manually only when haulers call in, send emails, or during occasional follow-up checks. Automating periodic â€œplease review your hauler profileâ€ reminders would maintain accuracy without manual outreach.
- **Acceptance Criteria:** @ Automated Email sends at a configurable frequency -@ hauler receives a summary of all info on file -@ hauler can update via form -@ Confirmation Saved to History

## Day 2 — Story 148
- **Epic:** Hauler Management & Onboarding
- **Feature:** Vendor Management (General Updates)
- **Parent Task:** Ongoing Maintenance
- **Task Name:** Capture Contact Changes Automatically
- **User Story:** As a VM Specialist, I want contact-related changes (e.g., new emails, removed emails) logged automatically so I donâ€™t have to document them manually in notes.
- **Description:** Specialists currently log contact changes manually so others know what used to be on file. With structured contact records and automated audit logging, this manual step becomes unnecessary.
- **Acceptance Criteria:** @ system automatically logs Email add/@remove events -@ Log is visible in the hauler History section -@ No need for free-@form notes about Contact changes

---

# Day 3

**Stories:** 169

## Day 3 — Story 001
- **Epic:** PSP & VM â€“ Core Module Integration
- **Feature:** Vendor Management â€“ Cross-Department User Inclusion
- **Parent Task:** Expand User Coverage
- **Task Name:** Include VM Staff Outside VM Tables
- **User Story:** As a system architect, I need to include Andrew (who works primarily in service tickets rather than VM tables) in the migration scope so that all vendor-related responsibilities across the department are represented in user stories.
- **Description:** Andrewâ€™s responsibilities include tonnage collection, event toilet confirmations, and camera vendor coordination (Stallion, Central Force). These processes do not occur inside the vendor management tables but intersect with vendor data and service tickets. Including him ensures that all VM workflowsâ€”including those triggered outside the hauler tableâ€”are considered during Cube migration.
- **Acceptance Criteria:** - Andrewâ€™s workflows are documented and included in the migration mapping.\n- Any features or processes he relies upon are analyzed for gaps during the Cube redesign.\n- VM cross-functional dependencies are identified (tonnage â†’ accounting, event toilets â†’ fulfillment, camera trailers â†’ AMs).

## Day 3 — Story 002
- **Epic:** PSP & VM â€“ Core Module Integration
- **Feature:** Workflow Integration
- **Parent Task:** Identify Cross-Module Touchpoints
- **Task Name:** Document Andrewâ€™s Non-VM-Table Workflows
- **User Story:** As a product owner, I want Andrewâ€™s service-ticket-based workflows documented so the Cube can support vendor-related actions that occur in non-VM tables.
- **Description:** Andrewâ€™s work touches product/service tickets rather than hauler records. His involvement must still be mapped for full vendor servicing continuity: tonnage calls, event toilet confirmations, and security camera trailer orders.
- **Acceptance Criteria:** @ list of Andrewâ€™s workflows is documented.\n-@ dependencies between Andrewâ€™s Tasks and VM Data are identified.\n- integration points with hauler Data, product records, service tickets, and billing are mapped.

## Day 3 — Story 003
- **Epic:** PSP â€“ Address & Compliance
- **Feature:** Address Validation & Standardization
- **Parent Task:** Automate Country Field
- **Task Name:** Force Country = USA for All Hauler Addresses
- **User Story:** As a system, I need to automatically set the haulerâ€™s address country field to USA to prevent Avalara and Intacct billing errors caused by missing country codes.
- **Description:** Legacy Quickbase allows addresses without country fields, causing Avalara tax validation failures and Intacct sync issues. Cube must auto-populate â€œUSAâ€ regardless of UI visibility.
- **Acceptance Criteria:** @ Country field is auto-@set to USA on create/@update.\n-@ Avalara does not reject the address.\n-@ Intacct accepts the vendor address without errors.

## Day 3 — Story 004
- **Epic:** PSP â€“ Logging & Audit Trails
- **Feature:** Audit Logging
- **Parent Task:** Change Tracking
- **Task Name:** Log User When 'Do They Bill Haul As' Flag is Updated
- **User Story:** As a VM manager, I need changes to billing-related flags to be logged with user info so that financial-impacting field changes can be audited.
- **Description:** The 'bill haul as' flag is critical for AP/AR alignment. Cube must capture which user changed it, when, and what it was changed from/to.
- **Acceptance Criteria:** audit Log stores timestamp, old value, new value, User ID.\n-@ Log displayed in hauler History UI.\n-@ No impact to UI performance.

## Day 3 — Story 005
- **Epic:** PSP â€“ PSP Status Management
- **Feature:** PSP Approval
- **Parent Task:** Status Logging
- **Task Name:** Log PSP Sign-Off & PSP Sign-Off Complete
- **User Story:** As a VM supervisor, I need PSP sign-off events logged so we know who approved PSP status and when.
- **Description:** PSP designation is a high-impact status. Current system logs via web hook; Cube must preserve and improve this audit trail.
- **Acceptance Criteria:** @ PSP sign-@off and completion are auto-@logged.\n- User, timestamp, and triggering action stored.\n-@ PSP workflows do not break.

## Day 3 — Story 006
- **Epic:** PSP â€“ Intacct Compliance
- **Feature:** Intacct Sync
- **Parent Task:** Vendor Name Parity
- **Task Name:** Sync Hauler Name Changes to Intacct for Manually Added Vendors
- **User Story:** As a system, I need hauler name changes in Cube to automatically update Intacct so vendor records remain in parity.
- **Description:** Manually created vendors via the â€œAdd vendor to Intacctâ€ Boolean do not auto-sync name updates. Cube must ensure parity for accounting and AP processes.
- **Acceptance Criteria:** @ name updates push instantly to Intacct through the API.\n-@ Sync errors logged and retried.\n-@ Accounting confirms name parity across systems.

## Day 3 — Story 007
- **Epic:** Z-Site Integration
- **Feature:** Z-Site API Sync
- **Parent Task:** Vendor Data Matching
- **Task Name:** Auto-Sync Vendor Basic Info to Z-Site When Updated in Cube
- **User Story:** As a system, I need vendor name, address, and phone updates to sync automatically to Z-Site so camera/IoT workflows use accurate data.
- **Description:** Z-Site uses an external API and must stay aligned with Cube vendor data. Current Quickbase uses a web hook; Cube must replace it with a robust service layer.
- **Acceptance Criteria:** name, address, phone, and primary fields Sync automatically.\n-@ API authentication via token.\n-@ Error handling includes retry queue +@ Admin view.

## Day 3 — Story 008
- **Epic:** Tonnage Management
- **Feature:** Tonnage Collection
- **Parent Task:** Daily/Weekly Workflow
- **Task Name:** Document Andrewâ€™s Daily Tonnage Workflow
- **User Story:** As a tonnage coordinator, I need a defined workflow for requesting, capturing, and recording tonnage so Cube can support a more structured process.
- **Description:** Andrew calls/email haulers to get tonnage data. This workflow directly affects billing, reporting, and vendor scoring. Cube must surface tasks, automated reminders, and data entry controls.
- **Acceptance Criteria:** - Workflow steps documented (call/email, follow-up, entry).\n- Required fields for tonnage reflected in spec.\n- Gaps identified for automation opportunities.

## Day 3 — Story 009
- **Epic:** Event Toilet Confirmation
- **Feature:** Event Products
- **Parent Task:** Weekly Confirmation Task
- **Task Name:** Document Weekly Event Toilet Confirmation Process
- **User Story:** As a VM analyst, I need the Cube to support the weekly process of confirming event toilets every Thursday to ensure fulfillment accuracy.
- **Description:** Andrew performs weekly confirmations for event toilets; Cube needs UI and reminders to support this cadence.
- **Acceptance Criteria:** @ weekly event toilet task documented.\n-@ required Data fields identified.\n-@ Workflow represented in future state mapping.

## Day 3 — Story 010
- **Epic:** Camera Vendor Management
- **Feature:** Camera Products (Stallion, Central Force)
- **Parent Task:** Process Mapping
- **Task Name:** Map Camera Trailer Vendor Workflow
- **User Story:** As a product owner, I need to map the workflow for mobile security camera trailer orders so that Cube can standardize the process and identify missing requirements.
- **Description:** Andrew coordinates with vendors like Stallion and Central Force. Account managers enter orders, create hauler pages, and billing flows normally. Cameras behave like toilets/roll-offs but may include unique data elements later.
- **Acceptance Criteria:** - Workflow documented (Order â†’ Vendor coordination â†’ Billing).\n- Dependencies between AM, VM, and vendor validated.\n- Identify any special fields (none given in transcript).

## Day 3 — Story 011
- **Epic:** Camera Vendor Management
- **Feature:** Camera Product Handling
- **Parent Task:** Data Consistency
- **Task Name:** Confirm No Special Quickbase Requirements for Camera Vendors
- **User Story:** As a VM analyst, I need confirmation that camera vendors do not require unique fields so Cube does not create unnecessary complexity.
- **Description:** Andrew confirms that setting up a camera vendor uses the same fields and workflow as any other vendor (toilets, roll-offs). No special data is required.
- **Acceptance Criteria:** @ verification documented.\n-@ No new fields required unless future interviews reveal more.\n-@ camera items use standard product +@ hauler structure.

## Day 3 — Story 012
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Tonnage Retrieval Workflow
- **Parent Task:** Daily Workflow Execution
- **Task Name:** Access Tonnage Report and Export to Spreadsheet
- **User Story:** As a tonnage coordinator, I need a fast way to access the tonnage report and export it into a customizable view so I can organize the list based on my workflow without manual workarounds.
- **Description:** Andrew opens the â€œTonnage report â€“ Service Providersâ€ table, switches to the legacy style, exports it to Excel, and rearranges/hides columns manually. This is done because Quickbase cannot yet replicate Excelâ€™s flexibility for grouping, hiding columns, sorting, filtering, and color-coding.
- **Acceptance Criteria:** @ User can Export or view a tonnage list with full sorting/@Filtering options.\n-@ User can rearrange/@hide columns without leaving Cube.\n-@ Export to XLS/@CSV still available.\n-@ Load time remains fast even with large datasets.

## Day 3 — Story 013
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Tonnage Table UI
- **Parent Task:** Report View Experience
- **Task Name:** Replace Deprecated Report Style and Maintain Functionality
- **User Story:** As a user, I need the new Cube report view to preserve all functionality currently available in the old Quickbase â€œprevious styleâ€ report so none of my workflows break when Quickbase disables it.
- **Description:** The old Quickbase report style is being removed soon. Andrew relies on it because it displays information more compactly for him. Losing it without an equivalent replacement will disrupt his process.
- **Acceptance Criteria:** @ new Cube interface must fully Replace the old-@style report.\n- Row density, column visibility options, sorting, and Filtering must match or exceed current behavior.\n-@ No workflows should regress when Quickbase disables the old style.

## Day 3 — Story 014
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Tonnage Data Manipulation
- **Parent Task:** Spreadsheet-Like Controls
- **Task Name:** Provide Excel-Like Inline Tools (Hide Columns, Color Code, Highlight)
- **User Story:** As a tonnage coordinator, I want Excel-like tools within Cube so I can rearrange columns, filter, and color-code rows directly in the UI instead of exporting to Excel.
- **Description:** Andrew exports to Excel because Cube cannot do column rearrangement, hide/show toggles, color tags, bulk formatting, or high-contrast reference indicators. His workflow is dependent on these controls to quickly isolate target accounts.
- **Acceptance Criteria:** @ Cube allows Row Color tagging.\n-@ Cube allows column visibility toggles and drag-@to-@reorder.\n-@ sorting and Filtering available directly in UI.\n-@ User preferences are Saved between sessions.

## Day 3 — Story 015
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Tonnage Sorting
- **Parent Task:** Automated Aging Filter
- **Task Name:** Automatically Exclude Recent Tickets (Last 2â€“3 Days)
- **User Story:** As a tonnage coordinator, I need the system to automatically hide tonnage tickets from the past 2â€“3 days so I can focus only on items ready for follow-up, without manually filtering them out each morning.
- **Description:** Andrew manually filters and deletes (or hides) all entries from today, yesterday, and the day before because haulers need time before tonnage is available. These items are never worked immediately.
- **Acceptance Criteria:** - System supports a configurable â€œaging thresholdâ€ filter (e.g., hide tickets < 3 days old).\n- Default tonnage list automatically applies this filter.\n- User can override or adjust the threshold.\n- Filter persists across sessions.

## Day 3 — Story 016
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Tonnage Prioritization
- **Parent Task:** Visual Priority System
- **Task Name:** Highlight Oldest Tonnage Requests by Aging Buckets
- **User Story:** As a coordinator, I need automatic visual indicators that highlight older, harder-to-get tonnages so I can quickly identify priority follow-ups.
- **Description:** Andrew manually color codes older entries (red for very old, white for active, yellow for items with recent email attempts). Without this, he must visually scan large lists.
- **Acceptance Criteria:** - Cube assigns color labels automatically (e.g., red for >14 days, orange for 7â€“14 days, white for <7 days).\n- User can override color labels manually.\n- Priority colors update as items age.

## Day 3 — Story 017
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Tonnage Follow-Up Workflow
- **Parent Task:** Email Attempt Tracking
- **Task Name:** Tag Tonnage Items with â€œE-mailedâ€, â€œCalledâ€, or â€œNo Responseâ€
- **User Story:** As a user, I need the ability to mark tonnage line items with follow-up status (e.g., emailed, called, left voicemail) so I can track communication attempts without relying on Excel highlighting.
- **Description:** Andrew highlights rows yellow after sending emails and red/white based on urgency. He also references his notes in Quickbase but visually needs the spreadsheet markers to manage workflow.
- **Acceptance Criteria:** - Cube field for â€œFollow-Up Statusâ€ with values: Email Sent, Called, Voicemail, No Response, Completed.\n- Status changes visually displayed on the list.\n- Quick inline update buttons to mark status without opening each record.\n- History log persists attempts.

## Day 3 — Story 018
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Vendor Communication
- **Parent Task:** Hauler Behavior Recording
- **Task Name:** Store Vendor-Specific Rules (Flat Rates, Weighing Rules, Contact Preferences)
- **User Story:** As a tonnage coordinator, I need hauler-specific behaviors documented so that I know at a glance whether they weigh dumpsters, charge flat rates, or prefer calls vs. emails.
- **Description:** Andrew examines hauler notes every time before calling to check if they weigh dumpsters, use flat rates, have do-not-call tags, or have special instructions. This step is repeated for every vendor interaction.
- **Acceptance Criteria:** - Hauler page has structured fields for: â€œWeighs Dumpstersâ€, â€œFlat Rate Onlyâ€, â€œTonnage Contact Emailâ€, â€œTonnage Preferred Methodâ€, â€œDo Not Call for Tonnageâ€.\n- These fields appear directly inside the tonnage workflow UI.\n- Notes only used for true free-form details.

## Day 3 — Story 019
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Contact Management
- **Parent Task:** Active Tonnage Contact Lookup
- **Task Name:** Surface Verified Tonnage Email/Phone Directly in Tonnage Workflow
- **User Story:** As a coordinator, I want the correct tonnage contact (email and phone) displayed immediately when viewing a tonnage line so I donâ€™t need to dig through vendor contact lists.
- **Description:** Andrew manually checks hauler notes to confirm updated emails and then checks the contact tab if the note is outdated. This slows every call/email.
- **Acceptance Criteria:** @ tonnage record automatically displays the Verified vendor tonnage contact.\n-@ shows secondary fallback contacts when needed.\n-@ Alerts If Email was recently updated by VM.\n-@ prevents using outdated Contact info.

## Day 3 — Story 020
- **Epic:** Tonnage Management & Vendor Interaction
- **Feature:** Communication Workflow
- **Parent Task:** Call/E-mail Process
- **Task Name:** Support Both Call and Email Follow-Up Paths Based on Hauler Type
- **User Story:** As a user, I need the system to guide me depending on whether a hauler requires calling, email, or auto-sent invoices so my workflow is consistent and mistakes are minimized.
- **Description:** Andrew knows from memory which haulers automatically send tonnage, require calls, or require emails. This tribal knowledge is not documented and has to be re-learned by new staff.
- **Acceptance Criteria:** - Hauler profile includes a structured value: â€œTonnage Retrieval Method = Auto-Provided / Call Required / Email Requiredâ€.\n- Tonnage workflow automatically triggers the appropriate action.\n- Auto-send emails where applicable.\n- Provide call script or email template where applicable.

## Day 3 — Story 021
- **Epic:** Tonnage Collection Improvements
- **Feature:** Hauler Tonnage Management
- **Parent Task:** Structured Hauler Metadata
- **Task Name:** Replace Notes with Structured Tonnage Fields
- **User Story:** As a tonnage collector, I want structured fields instead of free-form notes so I can reliably track hauler behaviors such as invoice-sending habits, whether they charge for copies, and whether they are flat-rate, without relying on memory or tribal knowledge.
- **Description:** Currently, Andrew relies heavily on notes and personal knowledge to determine whether a hauler sends invoices automatically, charges for tonnage copies, uses a flat-rate landfill, or should not be contacted. The Cube should provide explicit fields such as: 'Do Not Call for Tonnages', 'Do Not Contact for Tonnages (Charges for Info)', 'Tonnage Contact Email', 'Hauler Sends Daily/Weekly Invoices', 'Flat Rate Hauler', 'Provides Tonnage Info', etc. These structured fields must populate reporting views so tonnage staff and backup staff can instantly understand rules without cross-referencing notes.
- **Acceptance Criteria:** a structured set of Checkbox, dropdown, and Contact fields replaces reliance on notes for tonnage rules. -@ fields appear on the hauler profile and pull into the tonnage report. -@ Users can update these fields without technical help. -@ Reports automatically filter haulers based on these fields. -@ Backup staff (e.g., Shelly) can work without needing tribal knowledge.

## Day 3 — Story 022
- **Epic:** Tonnage Collection Improvements
- **Feature:** Tonnage Rules & Report Enhancements
- **Parent Task:** Automated Exclusion Rules
- **Task Name:** Auto-Exclude Haulers That Should Not Be Contacted
- **User Story:** As a tonnage collector, I want the tonnage report to auto-remove haulers marked as 'Do Not Call' or 'Do Not Contact' so I never waste time working records I should skip.
- **Description:** Andrew currently must manually review notes and personal memory to determine which haulers: (1) always send their invoices automatically, (2) are flat-rate and provide no tonnage, (3) charge fees for tonnage inquiry, or (4) should never be contacted for any reason. Cube should automatically filter these out of the tonnage report based on structured fields.
- **Acceptance Criteria:** - Tonnage report supports filtering by new structured fields. - Haulers marked 'Do Not Call for Tonnages' or 'Do Not Contact for Tonnages' never appear in the queue. - Flat-rate haulers that do not provide tonnage never appear unless explicitly enabled. - Report loads without additional user filtering.

## Day 3 — Story 023
- **Epic:** Tonnage Collection Improvements
- **Feature:** Tonnage Contact Management
- **Parent Task:** Tonnage-Specific Contacts
- **Task Name:** Store Dedicated Tonnage Contact Info
- **User Story:** As a tonnage collector, I want a dedicated tonnage contact field on the hauler so I always know who to reach out to without searching notes or guessing.
- **Description:** Andrew currently relies on notes or prior memory to identify the correct tonnage contact. There is no designated field for 'Tonnage Contact Email' or 'Tonnage Contact Phone'. This causes errors when backup team members participate.
- **Acceptance Criteria:** - Haulers include dedicated 'Tonnage Contact Email', 'Tonnage Contact Phone', and 'Preferred Contact Method'. - These populate directly into tonnage reports. - Backup staff can work tonnage without needing tribal knowledge.

## Day 3 — Story 024
- **Epic:** Tonnage Collection Improvements
- **Feature:** Hauler Metadata Expansion
- **Parent Task:** Flat-Rate Behavior Controls
- **Task Name:** Identify Flat-Rate Hauler Behavior for Tonnage Logic
- **User Story:** As a tonnage collector, I want to identify whether a hauler is flat-rate so the system knows whether tonnage info is optional or unavailable, improving report accuracy.
- **Description:** Flat-rate haulers do not charge additional tonnage, but ZTERS still likes collecting tonnage for additional customer billing revenue. The system should differentiate between haulers that are flat-rate (and may never provide tonnage) vs. those who do charge tonnage.
- **Acceptance Criteria:** - Field exists for 'Flat-Rate Hauler'. - Field exists for 'Provides Tonnage Info (Even if Flat-Rate)'. - Tonnage report excludes haulers that never provide tonnage. - Tonnage report highlights haulers who *may* provide info optionally.

## Day 3 — Story 025
- **Epic:** Tonnage Collection Improvements
- **Feature:** Tonnage Fee Protection
- **Parent Task:** Avoid Contacting Haulers That Charge for Tonnage Copies
- **Task Name:** As a tonnage collector, I want a field that flags haulers who charge fees for copies so backup staff knows not to contact them and avoids unnecessary costs.
- **User Story:** Andrew knows certain haulers charge $25 per tonnage copy. Backup staff (e.g., Shelly) may email them unknowingly, incurring charges. Cube must provide a clear field that prevents these haulers from being contacted.
- **Description:** - Field exists: 'Charges For Tonnage Copies'. - If enabled, report auto-excludes the hauler. - Warning banners appear on the hauler profile. - Backup staff cannot accidentally contact these haulers.
- **Acceptance Criteria:** @ field implemented and tested. -@ tonnage Report fully excludes these haulers. -@ UI warnings appear clearly. -@ Backup User Workflow validated in QA.

## Day 3 — Story 026
- **Epic:** Tonnage Collection Improvements
- **Feature:** Tonnage Workflow Improvements
- **Parent Task:** Comprehensive Tonnage Contact Rules
- **Task Name:** Support Dual Rules: 'Do Not Call' and 'Do Not Contact'
- **User Story:** As a tonnage collector, I want the system to support both 'Do Not Call' and 'Do Not Contact' rules so that different reasons for contact restrictions are accurately represented.
- **Description:** Some haulers allow calls but not emails; others do not permit any contact; others will send invoices automatically. Cube must differentiate these conditions rather than bundling them in notes.
- **Acceptance Criteria:** - Two distinct fields exist: 'Do Not Call for Tonnages' and 'Do Not Contact for Tonnages'. - Report logic respects both rules. - UI clearly explains each ruleâ€™s purpose.

## Day 3 — Story 027
- **Epic:** Tonnage Collection Improvements
- **Feature:** Invoice Retrieval Optimization
- **Parent Task:** Integrated Invoice Lookup
- **Task Name:** Centralize Vendor Invoice Access for Tonnage Collection
- **User Story:** As a tonnage collector, I want invoice lookup integrated into the Cube so I no longer have to manually search Rossum or other systems to find tonnage invoices.
- **Description:** Andrew currently searches Rossum manually because Rossum archives only show ~3 months. Sometimes tonnage is captured in sectioned 'weight tickets', sometimes in a standard invoice. Cube should surface all invoice-supported tonnage directly.
- **Acceptance Criteria:** @ Cube shows Linked invoices and extracted tonnage values directly on the service ticket or hauler. -@ multiple sources (Rossum, AP flow, attached invoices) consolidate into a single view. -@ tonnage Report indicates when invoice-@supported tonnage already exists.

## Day 3 — Story 028
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Hauler Tonnage Management
- **Parent Task:** Tonnage Contact Rules
- **Task Name:** Add Explicit Tonnage Contact Rules
- **User Story:** As a tonnage collector, I want clear checkbox fields for tonnage behavior (e.g., always sends invoices, do not call, do not contact, flat-rate no-tonnage) so I donâ€™t rely on tribal knowledge and can process tonnage efficiently.
- **Description:** Current tonnage behavior is hidden inside notes or Andrewâ€™s memory. The system needs new structured fields to indicate: (1) Hauler always sends tonnage via invoice, (2) Hauler should never be contacted for tonnage, (3) Hauler is flat-rate and does not provide tonnage, (4) Specific tonnage contact person/email. These fields must display on the tonnage workflow report to eliminate manual searching.
- **Acceptance Criteria:** â€¢ New fields exist: â€œAlways Sends Tonnage Invoiceâ€, â€œDo Not Call for Tonnageâ€, â€œDo Not Contact for Tonnageâ€, â€œFlat-Rate â€“ No Tonnageâ€, and â€œTonnage Contactâ€.  â€¢ Fields appear on hauler profile and the tonnage report.  â€¢ When checked, the tonnage report automatically hides haulers based on rules.  â€¢ Andrew can process tonnage without referencing notes.

## Day 3 — Story 029
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Tonnage Report UI Improvements
- **Parent Task:** Tonnage Report Refinements
- **Task Name:** Filter Out Haulers Not Requiring Contact
- **User Story:** As a tonnage collector, I want the tonnage report to automatically exclude haulers marked as â€œDo Not Call,â€ â€œDo Not Contact,â€ or â€œAlways Sends Invoice,â€ so I donâ€™t waste time reviewing entries I should not act on.
- **Description:** Andrew currently filters out haulers manually in Excel. The system should automatically hide rows that he would skip due to behavior captured in the new fields. This removes the need to export, sort, hide, and color-code manually.
- **Acceptance Criteria:** â€¢ Tonnage report updates dynamically based on the new rules/checkboxes.  â€¢ Rows excluded correctly and only action-required haulers remain.  â€¢ Sorting by oldest/newest remains intact.  â€¢ Report requires no Excel export to identify actionable items.

## Day 3 — Story 030
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Tonnage Report UI Improvements
- **Parent Task:** Display Helpful Data on Report
- **Task Name:** Show Tonnage Contact + Rules on Report
- **User Story:** As a tonnage collector, I want the tonnage report to show the haulerâ€™s tonnage contact, flat-rate indicator, and tonnage behavior rules so I have all necessary context without clicking into the hauler profile.
- **Description:** The current workflow requires opening hauler pages and notes to check tonnage practices. The report should surface all essential fields (tonnage contact, rules, flat-rate status, product-specific tonnage availability) in-line.
- **Acceptance Criteria:** â€¢ Report shows: Tonnage Contact Name, Tonnage Contact Email, Flat-Rate indicator, Tonnage behavior checkboxes.  â€¢ No need to open separate hauler records.  â€¢ No missing context when making calls.

## Day 3 — Story 031
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Hauler Tonnage Management
- **Parent Task:** Replace Notes With Structured Data
- **Task Name:** Replace Tonnage Notes With Data Fields
- **User Story:** As a tonnage collector, I want structured fields for hauler tonnage practices so I do not rely on informal notes that are inconsistent and hard to report on.
- **Description:** Notes currently store critical info such as flat-rate behavior, invoice frequency, and whether a hauler sends tonnage daily. These must be replaced with data fields for reliability and automation.
- **Acceptance Criteria:** â€¢ All repeated info currently in notes is captured by new standardized fields.  â€¢ Notes are only used for situational comments, not rules.  â€¢ Data appears in reports.

## Day 3 — Story 032
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Hauler Tonnage Management
- **Parent Task:** Flat-Rate Hauler Logic
- **Task Name:** Auto-Exclude Flat-Rate Haulers
- **User Story:** As a tonnage collector, I want flat-rate haulers who never provide tonnage to auto-disappear from the tonnage report so I donâ€™t waste effort calling them.
- **Description:** Flat-rate haulers often cannot provide tonnage. The report should hide them automatically when the checkbox â€œFlat-Rate â€“ No Tonnage Providedâ€ is selected.
- **Acceptance Criteria:** â€¢ Flat-rate haulers excluded automatically.  â€¢ User can override using a checkbox if tonnage is needed for revenue-capture.  â€¢ No manual filtering required.

## Day 3 — Story 033
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Tonnage Contact Management
- **Parent Task:** Avoid Hauler Contact Fees
- **Task Name:** Add Field: Hauler Charges for Tonnage Requests
- **User Story:** As a tonnage collector, I want to mark haulers who charge for tonnage copies so the system blocks or warns when staff attempt to contact them.
- **Description:** Some haulers charge $25 per tonnage request. Without a field that prevents contact, support staff might unknowingly trigger fees.
- **Acceptance Criteria:** â€¢ New checkbox exists: â€œHauler Charges for Tonnage Requests.â€  â€¢ System warns or blocks contact attempts on the report.  â€¢ Hauler row visually indicates â€œFee Risk.â€

## Day 3 — Story 034
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Tonnage Contact Management
- **Parent Task:** Communication Rules
- **Task Name:** Add Global Rule: Do Not Contact for Tonnage
- **User Story:** As a tonnage collector, I need a â€œDo Not Contact for Tonnageâ€ control so staff avoid accidental outreach when haulers supply information automatically.
- **Description:** A stronger rule is needed beyond â€œDo Not Call.â€ Some haulers should never be contacted in any way because they send invoices automatically or charge for info.
- **Acceptance Criteria:** â€¢ New checkbox â€œDo Not Contact for Tonnage.â€  â€¢ Report hides these haulers by default.  â€¢ UI shows a clear indicator when viewing hauler pages.

## Day 3 — Story 035
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Invoice/Tonnage Integration
- **Parent Task:** Rossum Integration Enhancements
- **Task Name:** Add Rossum Invoice Search Shortcut
- **User Story:** As a tonnage collector, I want a button on the hauler page that opens a pre-filtered Rossum invoice search for that hauler so I donâ€™t manually search for invoices in another system.
- **Description:** Andrew currently has to open Rossum manually, type hauler names, and locate invoices across limited archives. A direct shortcut saves time.
- **Acceptance Criteria:** â€¢ Button exists on the hauler page.  â€¢ Opens Rossum filtered by hauler name automatically.  â€¢ Supports rapid access for invoice-based tonnage lookup.

## Day 3 — Story 036
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Inbound Email Processing
- **Parent Task:** Tonnage Email Routing
- **Task Name:** Correct the â€œReply-Toâ€ Email for Tonnage Requests
- **User Story:** As a tonnage collector, I want the automated tonnage request emails to send with a â€œreply-toâ€ address of tonnage@zters.com so haulers stop replying to dispatch by mistake.
- **Description:** Haulers click â€œReplyâ€ and responses currently route to dispatch@ instead of the tonnage inbox. This forces Andrew to rely on CD to forward important emails manually.
- **Acceptance Criteria:** â€¢ Outgoing tonnage email template updated with correct â€œReply-To.â€  â€¢ Hauler replies automatically reach tonnage@zters.com.  â€¢ No additional forwarding needed.

## Day 3 — Story 037
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Inbound Email Processing
- **Parent Task:** Dispatch Integration
- **Task Name:** Identify and Parse Tonnage Emails Sent to Dispatch
- **User Story:** As a tonnage collector, I want the system to detect tonnage emails incorrectly routed to dispatch@ and auto-process them the same way as emails sent to tonnage@ so no tonnage data is lost.
- **Description:** Haulers unable to access the portal send weight tickets to dispatch, which the system currently does not parse. Andrew must manually search dispatch messages.
- **Acceptance Criteria:** â€¢ System identifies tonnage attachments in dispatch inbox.  â€¢ Emails are parsed through the same tonnage automation.  â€¢ Entries created automatically in the product/service ticket fields.

## Day 3 — Story 038
- **Epic:** Tonnage Workflow Enhancements
- **Feature:** Inbound Email Processing
- **Parent Task:** UI Visibility of Tonnage Origin
- **Task Name:** Show Origin of Tonnage Entry
- **User Story:** As a tonnage collector, I want entries to show whether they originated from tonnage@ or dispatch@ so I can troubleshoot missing or misrouted tonnage.
- **Description:** Currently, Andrew checks if entries are â€œblue (Anthony)â€ vs â€œnot blueâ€ to guess their origin. This should be explicit.
- **Acceptance Criteria:** â€¢ New field shows source inbox: â€œReceived Via Dispatchâ€ or â€œReceived Via Tonnage Email.â€  â€¢ Visible on Tonnages tab and reports.  â€¢ Helps identify misrouting patterns.

## Day 3 — Story 039
- **Epic:** Tonnage Processing & Automation
- **Feature:** Tonnage Email UI/UX Improvements
- **Parent Task:** Tonnage Email Template Redesign
- **Task Name:** Improve Visibility of Submit Tonnage CTA
- **User Story:** As a hauler submitting tonnage data, I want the â€œSubmit Detailsâ€ button to be clearly visible at both the top and bottom of the email so I can easily submit required tonnage information without scrolling or missing it.
- **Description:** Current tonnage request emails hide the submit button far down the page, causing haulersâ€”and even internal staffâ€”to miss it. The UI/UX must be redesigned so the CTA is bold, centered, and duplicated at top and bottom of the email template.
- **Acceptance Criteria:** 1. The submit button appears immediately upon email open (top). 2. The submit button also appears at the end of the email (bottom). 3. Button is visually prominent (large, bold, accessible contrast). 4. Users confirm they can locate the CTA in under 2 seconds. 5. Rendering must work even when CSS fails.

## Day 3 — Story 040
- **Epic:** Tonnage Processing & Automation
- **Feature:** Unified Tonnage Email Routing
- **Parent Task:** Tonnage Email Routing Fix
- **Task Name:** Route All Tonnage Replies to Correct Mailbox
- **User Story:** As a tonnage processor, I want hauler replies to route to tonnage@zeters.com instead of dispatch so that I no longer miss tonnage results or require CD to manually forward them.
- **Description:** Hauler â€œreplyâ€ actions send emails to dispatch because automated tonnage requests currently use dispatch as the from-address. This causes lost data and manual work. System needs to route all tonnage replies to the correct inbox automatically.
- **Acceptance Criteria:** 1. Tonnage request emails use tonnage@zeters.com as the â€œFromâ€ address. 2. Reply-to header is set to tonnage@zeters.com. 3. Hauler replies arrive directly in tonnage inbox without forwarding. 4. No tonnage replies appear in dispatch inbox.

## Day 3 — Story 041
- **Epic:** Tonnage Processing & Automation
- **Feature:** Tonnage Email Routing
- **Parent Task:** Tonnage Inbox Consolidation
- **Task Name:** Ensure All Automated Tonnage Emails Go to Same Inbox
- **User Story:** As a tonnage processor, I want all tonnage-related emailsâ€”manual or automatedâ€”to land in the same inbox so I donâ€™t have to check multiple email accounts.
- **Description:** Currently automated system responses and manual emails arrive in different inboxes (dispatch + tonnage), causing confusion, missed tonnage, and forwarding. Unified routing is required.
- **Acceptance Criteria:** 1. All tonnage emails reach tonnage@zeters.com. 2. No tonnage emails appear in dispatch inbox. 3. Routing validated across multiple haulers. 4. All internal processors confirm all tonnage is centralized.

## Day 3 — Story 042
- **Epic:** Tonnage Processing & Automation
- **Feature:** Email Parsing & Handling
- **Parent Task:** Dispatch Inbox Parsing Improvement
- **Task Name:** Identify and Auto-Process Tonnage Replies Received in Dispatch
- **User Story:** As a tonnage processor, I want emails containing weight tickets or tonnage information that accidentally arrive in the dispatch inbox to be identified and processed automatically so I no longer have to manually review or forward them.
- **Description:** Some haulers cannot access the portal and reply with tonnage data directly to dispatch. These messages currently bypass automation entirely. The system should auto-detect tonnage content arriving in dispatch and process it like those in the tonnage inbox.
- **Acceptance Criteria:** 1. System scans dispatch inbox for keywords (tonnage, tons, weight ticket, scale ticket, landfill, etc.). 2. Matching emails are automatically pulled into processing queue. 3. Parsed data maps identically to tonnage inbox processing. 4. Items flagged for review if parsing fails.

## Day 3 — Story 043
- **Epic:** Tonnage Processing & Automation
- **Feature:** Bad Email Detection
- **Parent Task:** Bad Email Alerting & VM Ticket Trigger
- **Task Name:** Flag Invalid Hauler Emails and Auto-Generate VM Ticket
- **User Story:** As a tonnage processor, I want the system to automatically detect bounced or undeliverable tonnage emails and trigger a VM ticket so that bad hauler contact info is corrected immediately.
- **Description:** Andrew receives automated bounce messages showing the hauler email address is invalid. Currently there is no workflow, causing outdated contacts and failed tonnage requests. System should auto-detect and escalate.
- **Acceptance Criteria:** 1. Any bounce/undeliverable email for a hauler triggers automatic detection. 2. System identifies the hauler via email matching. 3. VM ticket created with details of the failure + hauler name + failed email + timestamp. 4. Ticket assigned to VM queue.

## Day 3 — Story 044
- **Epic:** Tonnage Processing & Automation
- **Feature:** Bad Email Detection
- **Parent Task:** Hauler Contact Validation
- **Task Name:** Allow Quick Lookup of Hauler by Email
- **User Story:** As a tonnage processor, I want the ability to search haulers by any email address so I can quickly identify the correct hauler when a bounce occurs.
- **Description:** Andrew had difficulty identifying the hauler associated with a failed email. The system must allow robust search by email fields.
- **Acceptance Criteria:** 1. Hauler search returns results for any email (primary, secondary, tonnage-specific, billing). 2. Search results include hauler name, page link, and all stored emails. 3. Search is accessible from global search.

## Day 3 — Story 045
- **Epic:** Tonnage Processing & Automation
- **Feature:** Hauler Ownership Changes
- **Parent Task:** Hauler Buyout Handling
- **Task Name:** Record & Surface Hauler Buyout Status
- **User Story:** As a tonnage processor, I want buyout information displayed prominently so I understand why an email is invalid or why tonnage is routed differently.
- **Description:** Example: Angelo SRM was bought out by GFL. The email no longer works, and only a note on the hauler page indicates the buyout. This should be surfaced automatically in workflows.
- **Acceptance Criteria:** 1. If hauler is marked â€œAcquired by another vendor,â€ system displays banner on hauler record. 2. Auto-suggest updated contact info. 3. Auto-route tonnage requests to new owner if applicable.

## Day 3 — Story 046
- **Epic:** Tonnage Processing & Automation
- **Feature:** Erroneous Tonnage Email Detection
- **Parent Task:** Inactive Hauler Logic
- **Task Name:** Prevent Emails to Inactive/Bought-Out Haulers
- **User Story:** As a tonnage processor, I want the system to prevent automated tonnage request emails from being sent to haulers who are marked inactive or bought out so that we avoid bouncebacks and eliminate unnecessary confusion.
- **Description:** A hauler bought out by GFL (no services since 2024) still received automated tonnage request emails, triggering bouncebacks. The system must detect inactive/bought-out status and suppress automated tonnage requests.
- **Acceptance Criteria:** 1. Any hauler marked inactive or with acquisition flag is excluded from automated emails. 2. Automated system verifies hauler has active roll-offs before sending. 3. Bounce rate for inactive haulers is 0%. 4. UI shows warning if user attempts to manually trigger a request.

## Day 3 — Story 047
- **Epic:** Tonnage Processing & Automation
- **Feature:** Hauler Roll-Off Validation
- **Parent Task:** Roll-Off Linkage Verification
- **Task Name:** Validate Active Roll-Offs Before Triggering Automated Emails
- **User Story:** As a system, I need to verify that a hauler has active roll-off services before sending automated tonnage emails so that outdated or irrelevant hauler contacts are not contacted.
- **Description:** Bouncebacks indicated the system attempted to email a hauler with no roll-offs since 2024. Automated logic must validate roll-off presence and stop emails when none exist.
- **Acceptance Criteria:** 1. Before sending emails, system queries active roll-off records. 2. If zero active roll-offs, system suppresses outgoing emails. 3. Audit log records suppression event. 4. QA confirms no email is sent when no active roll-offs exist.

## Day 3 — Story 048
- **Epic:** Tonnage Processing & Automation
- **Feature:** Bad Email Handling
- **Parent Task:** Bounce Email Reporting
- **Task Name:** Forward Bounce Errors to Helpdesk Automatically
- **User Story:** As a tonnage processor, I want bounceback/undeliverable tonnage emails automatically forwarded to help@zeters.com so I no longer have to manually forward them and developers can diagnose issues sooner.
- **Description:** Justin and Anthony instructed Andrew to manually forward bounce emails and paste hauler links for research. This should be automated so support receives bounce events instantly.
- **Acceptance Criteria:** 1. Bounceback emails detected system-wide. 2. System auto-forwards bounce message + hauler metadata + roll-off metadata to helpdesk. 3. VM ticket automatically created. 4. Manual forwarding no longer required.

## Day 3 — Story 049
- **Epic:** Tonnage Processing & Automation
- **Feature:** UI/UX Email Handling
- **Parent Task:** Email Client Assistance
- **Task Name:** Improve Forward/Reply Button Visibility in Internal Email Viewer
- **User Story:** As an internal user, I want clearly visible forward/reply controls in the email viewer so I do not struggle to locate basic email actions during processing.
- **Description:** Andrew struggled to find the forward button in the UI, indicating poor visibility or placement. Frequent use requires fast access.
- **Acceptance Criteria:** 1. Forward, Reply, Reply-All buttons must be visually prominent and top-aligned. 2. Icons must have tooltip labels. 3. Buttons must remain visible regardless of email length. 4. Usability test: user locates button in <3 seconds.

## Day 3 — Story 050
- **Epic:** Tonnage Processing & Automation
- **Feature:** Helpdesk Workflow
- **Parent Task:** Bounce Issue Escalation
- **Task Name:** Auto-Populate Hauler Context When Forwarding Bounce Emails
- **User Story:** As a tonnage processor, I want the system to automatically attach the hauler link and metadata when a bounceback is processed so that helpdesk can diagnose issues without me manually copying the hauler page.
- **Description:** Andrew was instructed to copy/paste hauler links manually when forwarding bounce emails. This should be automated.
- **Acceptance Criteria:** 1. Forwarded bounce packets include hauler URL, hauler ID, hauler name. 2. System includes email address that failed. 3. Forward requires zero manual enrichment. 4. Helpdesk confirms they have all needed info.

## Day 3 — Story 051
- **Epic:** Tonnage Backlog Management
- **Feature:** Tonnage Queue Prioritization
- **Parent Task:** Old Tonnage Prioritization
- **Task Name:** Add Workflow to Prioritize Aged Tonnage Items Before Billing Expiry
- **User Story:** As a tonnage processor, I want a prioritized view of older tonnage requests so that I can retrieve missing tonnage before the billing window closes and avoid lost revenue.
- **Description:** Andrew explained that older tonnage (e.g., April) may soon become non-billable. The current system only highlights recent items (red row logic) and fails to surface aging high-risk items.
- **Acceptance Criteria:** 1. System flags aged tonnage requests approaching billing cutoff. 2. A priority queue groups aged items before newer items. 3. UI sorting allows â€œOldest First.â€ 4. Color coding distinguishes billing-risk items from new ones.

## Day 3 — Story 052
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Cadence Logic
- **Parent Task:** Email Frequency Rules
- **Task Name:** Define Automated Tonnage Email Cadence
- **User Story:** As a system owner, I want a clear and configurable cadence for automated tonnage request emails so that haulers are contacted consistently without overwhelming them.
- **Description:** The team confirms automated tonnage emails are currently sent up to three times and then stop. Andrew confirms older tonnage requests become unreachable because the system stops contacting haulers, leaving large clusters of unresolved tonnage.
- **Acceptance Criteria:** 1. Cadence rules are configurable (e.g., weekly Ã— 3). 2. UI shows cadence status per hauler/ticket. 3. System stops after configured attempts. 4. Analytics report displays last attempt date for each item.

## Day 3 — Story 053
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Hauler Response Behavior
- **Parent Task:** Grouped Request Delivery
- **Task Name:** Group All Outstanding Tonnage Requests in a Single Email
- **User Story:** As a hauler, I want to receive all pending tonnage requests in one grouped email so that I do not receive dozens of fragmented daily/weekly requests.
- **Description:** Andrew explains that haulers (e.g., Sarabia) refuse to respond to individual user emails and only respond to the automated grouped system. However, the current grouping only groups items from the same date, not all outstanding tonnage items, causing massive backlog growth.
- **Acceptance Criteria:** 1. Grouping algorithm includes all outstanding items for that hauler regardless of service date. 2. One weekly email per hauler containing full list. 3. Portal form shows combined list. 4. Regression test ensures no duplicates or missed items.

## Day 3 — Story 054
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Grouping Logic
- **Parent Task:** Multi-Date Consolidation
- **Task Name:** Fix Grouping to Include All Old Tonnage Items
- **User Story:** As a tonnage processor, I want the automated email grouping engine to include older outstanding tonnage items so backlog does not grow month after month.
- **Description:** Current logic groups only by matching service date. Andrew shows haulers have 15â€“20 older tickets spanning 10/30â€“11/14 but only receive grouped emails for 11/14 items. This prevents timely billing and increases lost-revenue risk.
- **Acceptance Criteria:** 1. Grouping queries return all open tonnage with â€œmissing tonnage = true.â€ 2. Date filters removed unless intentionally configured. 3. Batch email includes full list. 4. Backlog decreases when automation runs.

## Day 3 — Story 055
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Email Content Construction
- **Parent Task:** Single Consolidated Payload
- **Task Name:** Bundle All Tonnage Into One â€œAction Requiredâ€ Request
- **User Story:** As a hauler, I want one unified request containing all outstanding tonnage lines so that I can respond once instead of handling multiple submissions.
- **Description:** Justin states emails should say: â€œHere is everything we need from youâ€”20 items.â€ Instead, system sends only subsets. This contradicts original design intent and haulersâ€™ expectations.
- **Acceptance Criteria:** 1. Email body lists all outstanding roll-offs. 2. Submission portal displays all required entries. 3. Response logs map each item to the correct service ticket. 4. Hauler test confirms they receive and respond to one message only.

## Day 3 — Story 056
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Trigger Logic
- **Parent Task:** Query Scope Expansion
- **Task Name:** Expand Trigger Query to Include Retroactive Tonnage Items
- **User Story:** As a developer, I want the trigger logic to backfill all outstanding tonnage items whenever a new trigger fires so that no items are left behind due to date-based logic.
- **Description:** Kelly explains the trigger was built to only send items with the same trigger date. Anthony and Andrew confirm it should instead send all missing tonnage items regardless of date.
- **Acceptance Criteria:** 1. Trigger queries all unfulfilled tonnage items for that hauler. 2. Date-based filtering is optional and configurable. 3. QA validates that old + new items appear together. 4. Logs show included item count.

## Day 3 — Story 057
- **Epic:** Automated Tonnage Request Engine
- **Feature:** System Behavior Adjustment
- **Parent Task:** Outstanding Items Processing
- **Task Name:** Ensure Weekly Trigger Sends All Missing Tonnage, Not Just New Items
- **User Story:** As a product owner, I want weekly automated workflows to pull all missing tonnage so haulers can respond to complete lists instead of partial subsets.
- **Description:** Anthony clarifies system intent: â€œIf there are multiple tonnage requests for one hauler, they ALL get grouped into one email.â€ Actual system behavior contradicts this by only processing the items sharing the same service date.
- **Acceptance Criteria:** 1. Weekly run includes every open item. 2. No partial grouping. 3. Weekly logs show correct inclusion count. 4. Old items no longer accumulate into backlog.

## Day 3 — Story 058
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Requirements Alignment
- **Parent Task:** Spec Interpretation
- **Task Name:** Correct the Interpretation of the Original Requirements Document
- **User Story:** As a system analyst, I want the system logic to reflect the original requirement that all outstanding tonnage requests be grouped so hauler interactions remain efficient and predictable.
- **Description:** Anthony reads the requirements aloud: â€œIf there are multiple tonnage requests for one hauler, they ALL get grouped.â€ Current implementation interprets grouping incorrectly, grouping only items sharing one date.
- **Acceptance Criteria:** 1. Requirements doc updated to explicitly define grouping rules. 2. Developer notes updated to remove ambiguity. 3. QA test cases added for multi-date grouping. 4. Behavior matches stakeholder expectations.

## Day 3 — Story 059
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Tonnage Grouping Logic
- **Parent Task:** Eligibility Rules
- **Task Name:** Determine Which Tonnage Items Should Be Included in Automated Requests
- **User Story:** As a system owner, I want the system to correctly determine which tonnage items are ready to be requested so we avoid missing older items or requesting items prematurely.
- **Description:** Kelly raises a scenario where a hauler has 20 outstanding tonnages but only the earliest 5 are currently eligible; the system lacks clear logic to distinguish â€œreadyâ€ vs. â€œnot ready,â€ leading to confusion. Team confirms intent is to always request all pending items that should logically be requested.
- **Acceptance Criteria:** 1. System defines readiness rules (e.g., service completed, vendor expected to provide tonnage). 2. UI indicator shows â€œready,â€ â€œnot ready,â€ and reason. 3. Automated grouping includes all eligible items. 4. No premature requests generated.

## Day 3 — Story 060
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Tonnage Grouping Logic
- **Parent Task:** Full Inclusion
- **Task Name:** Always Include All Eligible Outstanding Items
- **User Story:** As a tonnage processor, I want automated grouping to always include all outstanding items so backlog does not grow due to partial requests.
- **Description:** Justin clarifies the requirement: â€œWe need all 20.â€ Current system only groups based on a specific date slice, missing older queued items.
- **Acceptance Criteria:** 1. System fetches all items with missing tonnage regardless of date. 2. UI shows complete list count. 3. Automated email includes all eligible entries. 4. No date-based omissions.

## Day 3 — Story 061
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Misinterpreted Requirements
- **Parent Task:** Clarification
- **Task Name:** Correct Misinterpreted Eligibility and Grouping Logic
- **User Story:** As a systems analyst, I want the original requirements reinterpreted correctly so the system functions as intended.
- **Description:** Kelly attempts to justify excluding 15 items that â€œarenâ€™t ready,â€ but Andrew and Anthony confirm that is not the correct intent. The system misunderstood the grouping requirement.
- **Acceptance Criteria:** 1. Requirements doc updated with strict grouping rules. 2. No conditional exclusion unless explicitly defined. 3. UI and backend updated to reflect corrected logic. 4. QA tests added to prevent future misinterpretation.

## Day 3 — Story 062
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Prioritization Logic
- **Parent Task:** Oldest-First Processing
- **Task Name:** Process Older Pending Tonnages Before Newer Ones
- **User Story:** As a tonnage processor, I want the system to prioritize older outstanding tonnages so billing deadlines are not missed for old items.
- **Description:** Andrew states only current-day tonnage requests get triggered; older ones (e.g., 10/30, 11/12, 11/13) are never re-queried, causing critical billing delays.
- **Acceptance Criteria:** 1. System automatically flags old tonnage items as â€œpriority overdue.â€ 2. UI separates â€œcurrentâ€ vs â€œoverdue.â€ 3. Automated emails always include overdue items. 4. Aging report available.

## Day 3 — Story 063
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Trigger Logic
- **Parent Task:** Retroactive Fetching
- **Task Name:** Trigger Engine Must Retrieve Older Items Retroactively
- **User Story:** As a product owner, I want the trigger logic to retrieve older items when a new item appears so no historical items are skipped.
- **Description:** Justin clarifies current logic: only the items with todayâ€™s date trigger the process. Older items are ignored entirely. This contradicts operational needs.
- **Acceptance Criteria:** 1. Trigger logic updated to fetch â€œall missing tonnage itemsâ€ for that hauler everytime a new one triggers. 2. No date filtering unless explicitly configured. 3. Regression tests confirm old items now included.

## Day 3 — Story 064
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Aging Workflow
- **Parent Task:** Recurring Requests
- **Task Name:** Implement Monthly Reattempt Process for Aged, Previously Attempted Items
- **User Story:** As a product strategist, I want monthly retries for aged unresolved tonnage items so revenue is not lost due to abandoned items.
- **Description:** Justin explains items older than several months (e.g., July) never get retriggered after the initial three attempts. He proposes a recurring monthly retry workflow.
- **Acceptance Criteria:** 1. Items marked â€œaged unresolvedâ€ after initial cadence is exhausted. 2. Monthly retry workflow triggers automatically. 3. UI shows retry history. 4. Hauler receives additional grouped request including all unresolved aged items.

## Day 3 — Story 065
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Volume Management
- **Parent Task:** Email Load Management
- **Task Name:** Ensure Grouping Expands Without Increasing Email Frequency
- **User Story:** As a hauler, I want to receive only one email per week while still seeing all outstanding tonnage items to avoid feeling overwhelmed.
- **Description:** Kelly notes haulers previously complained about too many emails. Anthony clarifies grouping should increase item count inside the emailâ€”not the email frequency.
- **Acceptance Criteria:** 1. Weekly frequency fixed at 1 email. 2. Email body grows with outstanding item count. 3. UI shows â€œitems in grouped emailâ€ count. 4. No hauler receives more than one weekly request.

## Day 3 — Story 066
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Email Payload
- **Parent Task:** Dynamic Content Expansion
- **Task Name:** Support Expanding Email Payload Without Triggering Additional Emails
- **User Story:** As a system owner, I want the system to dynamically expand grouped requests without generating additional emails so communications remain predictable.
- **Description:** Kelly notes earlier pushback about high email volume. Justin clarifies that the number of items inside the grouped email should grow, but email count must not increase.
- **Acceptance Criteria:** 1. Email system supports variable-size item lists. 2. System logs validate that only one email is sent regardless of item volume. 3. Haulers confirm receipt of single grouped email.

## Day 3 — Story 067
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Communication Strategy
- **Parent Task:** Hauler Experience
- **Task Name:** Improve Hauler Experience by Stabilizing Request Frequency
- **User Story:** As a hauler, I want stable, predictable communication so I can process tonnage requests efficiently without confusion.
- **Description:** Team confirms: one email per week is fine, regardless of item count. Frequency should not change, only content.
- **Acceptance Criteria:** 1. Weekly email schedule documented. 2. Hauler-facing UI clarifies cadence. 3. Portal form always matches grouped content. 4. No duplicate requests generated.

## Day 3 — Story 068
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Email Cadence Rules
- **Parent Task:** Weekly Email Policy
- **Task Name:** Enforce Maximum Weekly Email Frequency
- **User Story:** As a hauler, I want to receive no more than one tonnage-request email per week so communications are predictable and not overwhelming.
- **Description:** Anthony clarifies the system must *never* send more than one tonnage request per hauler per week, regardless of how many outstanding items exist. Kelly expresses concern about volume, but Anthony reiterates Chadâ€™s directive that weekly frequency is mandatory and capped.
- **Acceptance Criteria:** 1. System restricts each hauler to one outbound email per 7-day cadence. 2. UI displays countdown until next allowable send. 3. Backend rejects attempts to generate more than one weekly email per hauler. 4. Audit logs clearly show weekly enforcement.

## Day 3 — Story 069
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Email Cadence Rules
- **Parent Task:** Internal Alignment
- **Task Name:** Standardize Cadence Per Chadâ€™s Instructions
- **User Story:** As a system owner, I want the automated tonnage email process to follow the single source of truth (Chadâ€™s directive) so all teams operate consistently.
- **Description:** Anthony states all prior interpretations are supersededâ€”emails must follow the once-per-week cadence and no 3-email max rule. Kelly notes Annette and Angelaâ€™s pushback but Anthony confirms their feedback is no longer applicable.
- **Acceptance Criteria:** 1. Requirements doc updated to reflect latest authoritative rules. 2. All team members aligned. 3. Flowcharts and Figma updated. 4. Tests validate weekly cadence is always applied.

## Day 3 — Story 070
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Grouping Logic
- **Parent Task:** Historical Inclusion
- **Task Name:** Include Historical Missing Tonnages During Weekly Sends
- **User Story:** As a tonnage processor, I want each weekly email to include all missing historical tonnages so older items are not forgotten.
- **Description:** Kelly admits the original automation only looked at new triggers and ignored older items. Anthony confirms intent was always to include all unfilled items, regardless of age.
- **Acceptance Criteria:** 1. Query logic must fetch all open tonnage-missing items. 2. Grouped email content includes historical items. 3. UI for hauler portal displays consolidated historical list. 4. No older items excluded due to lack of recent triggers.

## Day 3 — Story 071
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Escalation Workflow
- **Parent Task:** Manual Follow-Up
- **Task Name:** Define When Human Outreach Begins for Aged Tonnages
- **User Story:** As a VM agent, I want a clear guideline for when extremely old tonnage items require personal outreach so revenue is not lost.
- **Description:** Kelly notes there must be a point where humans step in for extremely old tonnages. Anthony states Andrew is already doing this based on the list. Andrew confirms he manually reaches out for older items weekly.
- **Acceptance Criteria:** 1. System flags items exceeding â€œagedâ€ threshold (e.g., 60â€“90 days). 2. UI shows â€œRequires Manual Contact.â€ 3. Andrew receives an auto-generated task list weekly. 4. Workflow states when calls vs. emails vs. escalation occur.

## Day 3 — Story 072
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Aging Prioritization
- **Parent Task:** UI Prioritization
- **Task Name:** Prioritize Older Tonnages in UI and Reporting
- **User Story:** As a tonnage processor, I want older tonnage entries to be clearly prioritized so I can focus on revenue-critical items first.
- **Description:** Andrew explains his primary focus is older tonnages. But current automated emails focus only on new ones, not the older backlog. He highlights inconsistent hauler responses and difficulties.
- **Acceptance Criteria:** 1. UI highlights items by aging tiers (e.g., 0â€“3 days, 4â€“14 days, 15â€“60 days, >60 days). 2. Sorting defaults to oldest-first. 3. Reports display aging reasons. 4. Filters allow Andrew to target oldest items quickly.

## Day 3 — Story 073
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Unresponsive Hauler Management
- **Parent Task:** Persistent Outreach
- **Task Name:** Continue Emailing Non-Responsive Haulers Weekly Until Tonnage is Provided
- **User Story:** As a system, I want to continue sending grouped weekly tonnage requests to unresponsive haulers so outstanding items are not abandoned.
- **Description:** Justin confirms: â€œContinue to hit them with emails until they give us the damn tonnage.â€ Anthony states this matches the original intent. Andrew supports this since many haulers only respond to repeated reminders.
- **Acceptance Criteria:** 1. Emails continue indefinitely until tonnage field is filled. 2. No â€œstop after X attemptsâ€ logic. 3. UI shows â€œweekly reminder active.â€ 4. System logs show continuous weekly attempts.

## Day 3 — Story 074
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Workflow Revision
- **Parent Task:** Process Documentation
- **Task Name:** Revise Flow Charts to Reflect Updated Tonnage Email Behavior
- **User Story:** As a product owner, I want updated diagrams and instructions so the automation reflects the real operational process.
- **Description:** Anthony explains his flow charts will be revised, especially around grouping and weekly cadence. Missing logic (historical inclusion) will be added.
- **Acceptance Criteria:** 1. Figma diagrams updated. 2. Text specs updated. 3. Version control shows changes. 4. Dev, QA, and VM teams re-aligned.

## Day 3 — Story 075
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Weekly Cron Execution
- **Parent Task:** System-Driven Weekly Batch
- **Task Name:** Execute Weekly Cron to Re-Evaluate All Outstanding Tonnages
- **User Story:** As a system, I want a weekly cron job to re-evaluate *all* tonnage-missing items so outdated reliance on per-ticket triggers is eliminated.
- **Description:** Justin suggests eliminating â€œtrigger-based logicâ€ entirely and replacing with a weekly full data sweep: all missing tonnages > X days should be sent automatically.
- **Acceptance Criteria:** 1. Weekly cron executes full query without relying on â€œtriggerâ€ records. 2. Cron respects weekly send limits. 3. Historical + new items included. 4. Cron logs showed correct runs.

## Day 3 — Story 076
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Billing Risk Management
- **Parent Task:** Revenue Preservation
- **Task Name:** Prevent Loss of Revenue by Escalating Aged Missing Tonnages
- **User Story:** As a finance-aware user, I want the system to help prevent loss of billable revenue by ensuring old missing tonnages are identified and escalated.
- **Description:** Andrew warns missing tonnage for 4â€“6 months jeopardizes ability to bill customers. Without persistent outreach and aging alerts, ZTERS loses money.
- **Acceptance Criteria:** 1. System flags â€œbilling riskâ€ items. 2. UI shows risk level. 3. Weekly email + manual outreach workflows align. 4. Reporting shows potential lost revenue.

## Day 3 — Story 077
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Criteria Clarification
- **Parent Task:** Request Logic
- **Task Name:** Clarify Conditions for When Tickets Should Be Marked to Send
- **User Story:** As a developer, I want clear conditions for marking tickets to send so logic is not misinterpreted again.
- **Description:** Anthony states criteria: tickets send 7 days after scheduled removal IF and ONLY IF tonnage field is blank. Kelly notes dev team misinterpreted original rules.
- **Acceptance Criteria:** 1. Condition explicitly defined: send request when tonnage field is blank AND removal date â‰¥ 7 days old. 2. No other triggers affect this. 3. Logic documented and testable.

## Day 3 — Story 078
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Documentation Alignment
- **Parent Task:** Cross-Team Understanding
- **Task Name:** Ensure Dev, QA, VM Have Unified Understanding of New Rules
- **User Story:** As a product owner, I want all teams aligned so the automation behaves exactly as intended.
- **Description:** Kelly explains QA and dev believed the original build was correct because requirements lacked specific provisions for historical items. Andrew explains SMEs werenâ€™t involved early enough.
- **Acceptance Criteria:** 1. Shared updated requirements doc. 2. Kickoff meeting with all teams. 3. SME review mandatory before development. 4. QA checklist updated.

## Day 3 — Story 079
- **Epic:** Automated Tonnage Request Engine
- **Feature:** SME Involvement
- **Parent Task:** Process Accuracy
- **Task Name:** Ensure SME Participation Before and During Design
- **User Story:** As a project manager, I want subject matter experts involved early so critical operational details are not missed.
- **Description:** Andrew states he wasnâ€™t included in initial requirements-building, causing gaps. Justin agrees this was the root problem.
- **Acceptance Criteria:** 1. SME participation required in discovery. 2. User interviews documented. 3. SME acceptance criteria captured. 4. SME signs off before development.

## Day 3 — Story 080
- **Epic:** Automated Tonnage Request Engine
- **Feature:** SME Collaboration
- **Parent Task:** Requirements Alignment
- **Task Name:** SME Inclusion for Accurate Rules
- **User Story:** As a product team, we want SMEs included in early discovery so critical operational rules are not missed.
- **Description:** Andrew explains he was excluded from early meetings and therefore misinformation entered requirements. His frontline expertise directly impacts accuracy of tonnage workflows.
- **Acceptance Criteria:** 1. SMEs must be required attendees for tonnage-related discovery. 2. Documentation includes SME validations. 3. UI/logic revisions cannot proceed without SME signoff. 4. Audit checklist updated.

## Day 3 — Story 081
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Logic Rules
- **Parent Task:** Grouping & Marking Logic
- **Task Name:** Clarify Grouping and Marking Rules for Tonnage Emails
- **User Story:** As a developer, I want clear logic about when emails are grouped and when tickets are marked to send so automation behaves consistently.
- **Description:** Anthony documents rules: tickets send 7 days after removal; do not send if tonnage exists; send only when blank; group all vendor items into a single weekly email.
- **Acceptance Criteria:** 1. System applies new rule set consistently. 2. One grouped email per hauler per week. 3. Mark-to-send rule uses blank tonnage only. 4. QA cases confirm grouping logic.

## Day 3 — Story 082
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Historical Requests
- **Parent Task:** Continuous Emailing
- **Task Name:** Send All Missing Historical Tonnages Weekly
- **User Story:** As a tonnage processor, I want older outstanding tonnages to be included every week so revenue is not lost.
- **Description:** Andrew confirms older items must be included. Justin states continuous weekly sends of all missing items will assist revenue recovery.
- **Acceptance Criteria:** 1. Weekly cron pulls all missing tonnages regardless of age. 2. Email includes entire list. 3. UI marks all historical items in grouped email for clarity. 4. Logs show older items included.

## Day 3 — Story 083
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Revenue Preservation
- **Parent Task:** Oldest Tonnage Priority
- **Task Name:** Prioritize and Capture Older Unbilled Tonnages to Prevent Revenue Loss
- **User Story:** As a billing-aware user, I want older uncollected tonnages captured so ZTERS does not lose billable revenue.
- **Description:** Andrew stresses older items represent revenue the company earned but hasnâ€™t billed. Justin and Andrew call this â€œmoney left on the table.â€
- **Acceptance Criteria:** 1. UI highlights aging tiers. 2. Weekly emails include oldest items. 3. Reporting shows revenue-at-risk. 4. Aging escalations available.

## Day 3 — Story 084
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Age Threshold Discussion
- **Parent Task:** Write-off Logic
- **Task Name:** Define Maximum Age Threshold for Automated Requests
- **User Story:** As a product owner, I need clarity on whether extreme-age tonnages (e.g., 6+ months) should still be emailed so automation handles them correctly.
- **Description:** Anthony asks whether very old items (e.g., 6 months) should still be sent. Andrew says yes â€” even old ones deserve follow-up. Justin notes a possible Chad-defined write-off threshold may be required.
- **Acceptance Criteria:** 1. Configurable age cutoff setting. 2. If cutoff defined, UI marks items as â€œwrite-off eligible.â€ 3. Automation excludes items past cutoff if instructed. 4. Stakeholder approval required.

## Day 3 — Story 085
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Write-Off Workflow
- **Parent Task:** Billing Policy
- **Task Name:** Establish Write-Off Process for Aged Tonnages
- **User Story:** As a finance-aligned team, we want a write-off mechanism so extremely old tonnage items are handled cleanly.
- **Description:** Justin recommends Chad define a formal write-off period (e.g., 6 months), after which items are removed or set to 0 tonnage.
- **Acceptance Criteria:** 1. Write-off period configurable at admin level. 2. Items older than threshold auto-marked for removal or auto-zero tonnage. 3. Reports exclude written-off items. 4. Action logged.

## Day 3 — Story 086
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Data Integrity
- **Parent Task:** Unexpected Old Entries
- **Task Name:** Support Late-Added Historical Tonnage Items
- **User Story:** As a system, I want to detect when old tonnage entries are added late so they appear correctly in reports and automated requests.
- **Description:** Andrew notes new older tonnage tickets appeared this week for January, added after the fact.
- **Acceptance Criteria:** 1. System auto-detects late-created old items. 2. Such items are included in next weekly email. 3. UI highlights them as â€œlate added.â€ 4. Logs record date of creation vs. service date.

## Day 3 — Story 087
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Report Sync
- **Parent Task:** Report Filtering
- **Task Name:** Align Report Filters with Automated Email Logic
- **User Story:** As a developer, I want the report and automated cron to use identical filtering logic so outputs match.
- **Description:** Justin requests reviewing Quickbase filters to ensure automated email requests use the same conditions. He asks Andrew to open the filter.
- **Acceptance Criteria:** 1. Report fields mapped 1:1 to automation logic. 2. Filters documented. 3. Cron uses identical filter set. 4. QA tests confirm identical results.

## Day 3 — Story 088
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Filter Review
- **Parent Task:** UI Filtering
- **Task Name:** Display and Review Filters for End Date Conditions
- **User Story:** As a processor, I want clarity on the report filters so I understand why items appear or donâ€™t appear.
- **Description:** Justin walks Andrew through â€œend date is not blank OR end date is not 2 days in the future,â€ explaining why some entries appear prematurely.
- **Acceptance Criteria:** 1. Filter conditions visible in UI. 2. Tooltips explain meaning of future end date rule. 3. User can adjust preview windows. 4. Report results update correctly.

## Day 3 — Story 089
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Filter Optimization
- **Parent Task:** Date Window Improvements
- **Task Name:** Adjust End-Date Logic to Avoid Showing Items Too Early
- **User Story:** As a tonnage processor, I want the end-date filter to avoid showing new tickets too early so I can focus on actionable items.
- **Description:** Justin notes current filter includes entries with end dates 2 days in the future, which Andrew cannot action. He suggests adjusting window.
- **Acceptance Criteria:** 1. Future window configurable. 2. Default excludes future items unless needed. 3. UI option to toggle inclusion. 4. Filter update reflects in email logic.

## Day 3 — Story 090
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Tonnage Requirement Logic
- **Parent Task:** Formula Review
- **Task Name:** Review the Formula for â€œFinal Tonnage Requiredâ€
- **User Story:** As a dev team, we want clarity on the â€œfinal tonnage requiredâ€ formula so automated logic matches actual billing needs.
- **Description:** Justin indicates the main condition driving the report is â€œfinal tonnage requiredâ€ and wants to ensure dev understands exactly how itâ€™s calculated.
- **Acceptance Criteria:** 1. Formula documented and mapped. 2. Automated system mirrors formula. 3. QA validates formula output for sample tickets. 4. UI displays criteria details.

## Day 3 — Story 091
- **Epic:** Automated Tonnage Request Engine
- **Feature:** Field Review
- **Parent Task:** Data Mapping
- **Task Name:** Locate and Validate â€˜Final Tonnage Requiredâ€™ Field for Development
- **User Story:** As a developer, I want to locate the correct Quickbase field so I can map automation to the right data.
- **Description:** Justin begins searching for the field definition so devs can program automation correctly.
- **Acceptance Criteria:** 1. Field ID identified. 2. Mapping stored in dev documentation. 3. Cron uses correct field. 4. QA validates with several tickets.

## Day 3 — Story 092
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Report Navigation
- **Parent Task:** Field Identification
- **Task Name:** Locate Tonnage Status Fields
- **User Story:** As a developer, I want to identify which report contains the â€œFinal Tonnage Requiredâ€ field so I can correctly map logic in the automated system.
- **Description:** Justin realizes the target field is only found in a specific report (â€œTonnage Statusâ€), not globally searchable. He requests Andrew to confirm the report name to align automation logic.
- **Acceptance Criteria:** 1. Correct report name confirmed. 2. Field location documented for dev team. 3. QA validates correct mapping. 4. No mismatched fields in automation.

## Day 3 — Story 093
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Technical Review
- **Parent Task:** Formula Review
- **Task Name:** Extract Final Tonnage Logic for Dev Chat
- **User Story:** As a developer, I want complex Quickbase logic posted to chat so it can be analyzed asynchronously.
- **Description:** Justin notes the Final Tonnage Required logic is large and will be pasted separately into chat for technical review, not during live walkthrough.
- **Acceptance Criteria:** 1. Full formula pasted into dev chat. 2. Developers acknowledge receipt. 3. Logic included in documentation. 4. No missing formula conditions.

## Day 3 — Story 094
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Event Toilets
- **Parent Task:** Process Coverage
- **Task Name:** Identify Remaining Processes
- **User Story:** As a facilitator, I want to know remaining workflows Andrew intends to demo so the workshop covers all areas.
- **Description:** Andrew states the final item left to demonstrate is the Event Toilet process.
- **Acceptance Criteria:** 1. Remaining workflow identified. 2. Added to agenda. 3. Ready for demo.

## Day 3 — Story 095
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Data Entry Demonstration
- **Task Name:** Demonstrate How a Tonnage is Entered
- **User Story:** As a tonnage processor, I want to show the steps for entering tonnage so developers understand the workflow and edge cases.
- **Description:** Justin asks Andrew to simulate entering a tonnage. Andrew chooses a real pending one to walk through the full process including validation steps.
- **Acceptance Criteria:** 1. Full demonstration recorded. 2. All fields shown. 3. Steps documented for dev team. 4. Edge cases identified.

## Day 3 — Story 096
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Portal-Based Tonnages
- **Parent Task:** Portal Access Flow
- **Task Name:** Show Portal-Based Tonnage Retrieval
- **User Story:** As a processor, I want to demonstrate logging into a hauler portal to fetch tonnage so automation improvements can target high-friction flows.
- **Description:** Andrew attempts accessing â€œGotta Goâ€ portal; cannot retrieve data; moves to a simpler email-based tonnage instead.
- **Acceptance Criteria:** 1. UX friction noted. 2. Cases requiring portal work flagged. 3. Automation opportunities logged.

## Day 3 — Story 097
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Email-Based Tonnages
- **Parent Task:** Manual Reconciliation
- **Task Name:** Demonstrate Processing a Standard Emailed Tonnage
- **User Story:** As a processor, I want to show how emailed tonnage values (e.g., â€œ4.7â€) are reconciled and entered so developers understand manual workload.
- **Description:** Andrew shows an email containing only the tonnage value. He explains he must: verify drop date, verify haul date, validate against history, ensure no duplicate, then enter tonnage.
- **Acceptance Criteria:** 1. Steps documented: open email â†’ validate dates â†’ confirm correct ticket â†’ check system record. 2. Duplicate prevention rules captured. 3. Data entry process defined.

## Day 3 — Story 098
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Validation Workflow
- **Parent Task:** Date Verification
- **Task Name:** Verify Matching Dates Before Entry
- **User Story:** As a processor, I want to verify the haul date matches the dispatch ticket so incorrect tonnage is never assigned.
- **Description:** Andrew compares email date (11/6) to tickets, ensuring the correct ticket is located before entering tonnage.
- **Acceptance Criteria:** 1. Email date must match ticket drop/haul date. 2. System highlights mismatches. 3. Warning shown if multiple possible matches.

## Day 3 — Story 099
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Duplicate Prevention
- **Parent Task:** System Insert Identification
- **Task Name:** Identify Whether System Already Entered Tonnage
- **User Story:** As a processor, I want the UI to show when automation already entered tonnage so I donâ€™t re-enter it.
- **Description:** Andrew explains that blue-highlighted tonnage entries indicate automated system-created entries (â€œAnthony Buresâ€ submitter).
- **Acceptance Criteria:** 1. UI clearly marks automated entries. 2. Users can safely skip already-entered items. 3. No duplicate entries allowed.

## Day 3 — Story 100
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Duplicate Prevention
- **Parent Task:** Email Response Handling
- **Task Name:** Differentiate Tonnage Email Responses vs. Manual Needs
- **User Story:** As a processor, I want to understand which emails require action so I donâ€™t waste time reviewing automated confirmations.
- **Description:** Andrew states he checks responses from system emails (highlighted blue) but does not have to re-enter them unless manually verified.
- **Acceptance Criteria:** 1. System auto-classifies email responses. 2. Auto-entered responses bypass inbox review. 3. Outlook rule recommended for routing.

## Day 3 — Story 101
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Inbox Optimization
- **Parent Task:** Email Filtering
- **Task Name:** Automate Filtering of Auto-Entered Tonnage Responses
- **User Story:** As a processor, I want irrelevant confirmation emails automatically sorted so the inbox shows only actionable items.
- **Description:** Justin suggests creating Outlook rules to auto-move â€œTonnage Responseâ€ emails, reducing inbox clutter.
- **Acceptance Criteria:** 1. Outlook rule recommended. 2. Responses routed to folder. 3. Inbox contains only actionable requests.

## Day 3 — Story 102
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Inbox Workflow
- **Parent Task:** Flagging Logic
- **Task Name:** Clarify Why Emails Are Flagged
- **User Story:** As a processor, I want a clear system for flagging emails so I can track which tonnages still need work.
- **Description:** Andrew flags items he needs to return to later, even if they are already entered, for organizational purposes.
- **Acceptance Criteria:** 1. Flagging rules documented. 2. UI may support built-in follow-up indicators. 3. Flags no longer needed for auto responses.

## Day 3 — Story 103
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Inbox Streamlining
- **Parent Task:** Remove Non-Actionable Emails
- **Task Name:** Eliminate Non-Actionable Emails from Tonnage Queue
- **User Story:** As a processor, I want non-actionable tonnage confirmation emails removed so I only see emails requiring action.
- **Description:** Justin suggests removing these via automatic rules; Andrew agrees this can simplify workflow.
- **Acceptance Criteria:** 1. Non-actionable filtered. 2. Actionable-only list visible. 3. Inbox decluttered.

## Day 3 — Story 104
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Error Handling
- **Parent Task:** Invalid Tonnage Reports
- **Task Name:** Handle Hauler Responses Claiming â€œWe Never Dropped This Dumpsterâ€
- **User Story:** As a processor, I want a workflow for conflicting hauler messages so errors donâ€™t block billing.
- **Description:** Andrew describes: check site â†’ identify account manager â†’ identify fulfillment rep â†’ forward issue and escalate.
- **Acceptance Criteria:** 1. UI escalation button. 2. Workflow documented. 3. Error cases go to AM/FM automatically.

## Day 3 — Story 105
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Relationship Management
- **Parent Task:** Hauler Communication
- **Task Name:** Support Operational Relationship Between Andrew and Haulers
- **User Story:** As a processor, I want to maintain strong hauler relationships so issue resolution is faster.
- **Description:** Andrew explains haulers often call him directly for clarifications; relationships help resolve process issues.
- **Acceptance Criteria:** 1. CRM notes stored. 2. Contact history tracked. 3. Hauler preferences stored.

## Day 3 — Story 106
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Workload Management
- **Parent Task:** Role Definition
- **Task Name:** Document Andrewâ€™s Secondary Responsibilities
- **User Story:** As a team, we want clarity on Andrewâ€™s non-entry workload so automation can relieve unnecessary burdens.
- **Description:** Andrew explains he spends time forwarding issues to AM/FM teams, assisting haulers, and handling unrelated support due to high contact volume.
- **Acceptance Criteria:** 1. Secondary tasks identified. 2. Automation opportunities flagged. 3. Workload documented for future staffing.

## Day 3 — Story 107
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Staffing Constraints
- **Parent Task:** Cross-Training Limitations
- **Task Name:** Identify Challenges with Backup Staff (Shelly)
- **User Story:** As a manager, I want to understand limitations in cross-training so backup workflows do not create operational issues.
- **Description:** Andrew explains Shelly lacks relationship knowledge and hauler nuances, which leads to incorrect communications and charge disputes.
- **Acceptance Criteria:** 1. Hauler preference profiles stored in system. 2. UI warns backup users. 3. Training notes included.

## Day 3 — Story 108
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Information Visibility
- **Parent Task:** Hauler Rules
- **Task Name:** Expose Hauler-Specific Rules in UI
- **User Story:** As a processor, I want the UI to show hauler-specific handling rules (e.g., who charges for weigh tickets) so backup staff avoid mistakes.
- **Description:** Andrew describes haulers who charge $25 for weigh tickets if emailed incorrectly; Shelly accidentally triggers these.
- **Acceptance Criteria:** 1. UI displays handling rules. 2. Warning appears before contacting hauler. 3. Rules editable by admins.

## Day 3 — Story 109
- **Epic:** Tonnage Processing UX & Workflow
- **Feature:** Report Improvements
- **Parent Task:** Visibility Enhancements
- **Task Name:** Expose Requirements for Better Visibility on Report
- **User Story:** As a processor, I want missing or costly hauler behaviors reflected in reports so workflow mistakes are avoided.
- **Description:** Justin suggests putting hauler rules and cost-impact indicators directly in Quickbase report.
- **Acceptance Criteria:** 1. Report includes hauler rule column. 2. Indicators visible. 3. Backup users avoid costly actions.

## Day 3 — Story 110
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Duplicate Prevention
- **Task Name:** Prevent Duplicate or Incorrect Tonnage Entry
- **User Story:** As a tonnage processor, I want the system to clearly indicate whether an entered tonnage matches multiple possible haul tickets for the same site and date so that I can avoid duplicates and ensure accurate billing.
- **Description:** When entering tonnage, the system must detect if multiple haul tickets exist for the same site and haul date; the UI should show a comparison indicator and highlight existing entries to prevent accidental duplication.
- **Acceptance Criteria:** The system flags duplicate-risk entries, displays comparison data, and blocks saving until the user confirms the correct haul match.

## Day 3 — Story 111
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Multi-Dumpster Support
- **Task Name:** Identify Correct Dumpster When Multiple Hauls Occurred Same Day
- **User Story:** As a tonnage processor, I want the UI to show all dumpsters and haul tickets for the same service site and date so I can determine which haul the weight belongs to.
- **Description:** The UI must display all candidate hauls for a date, including dumpster IDs, sizes, haul IDs, and any existing tonnages entered.
- **Acceptance Criteria:** The user can confidently select the correct haul; system logs the selection and removes the item from the pending list.

## Day 3 — Story 112
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Dual-Entry Conflict Handling
- **Task Name:** Show Side-by-Side Comparison When One User Enters From Invoice & Another From Hauler
- **User Story:** As a tonnage processor, I want to see a comparison when different processors enter tonnage from different sources so I can resolve conflicts without researching manually.
- **Description:** When two tonnages exist or are attempted, system must display invoice-based vs hauler-provided weights, dates, and sources for review.
- **Acceptance Criteria:** System blocks duplicates until user selects which value is authoritative and logs the resolution reason.

## Day 3 — Story 113
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Drop-Off Logic Improvement
- **Task Name:** Auto-Remove Completed Tonnages From the Processing List
- **User Story:** As a tonnage processor, I want items to drop off the report immediately after I enter their tonnage so I donâ€™t re-check or re-process cases that are already completed.
- **Description:** Once a tonnage is saved, it must no longer appear in â€œPending Tonnageâ€ reports or queues.
- **Acceptance Criteria:** Record disappears from pending lists instantly and reflects in completed-tonnage workflows.

## Day 3 — Story 114
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Duplicate Date Alert
- **Task Name:** Notify When Same Date Has Multiple Hauls
- **User Story:** As a tonnage processor, I want a warning when multiple hauls occurred on the same date for a site so I can verify that Iâ€™m matching the correct haul ticket.
- **Description:** System shows a yellow alert icon with text: â€œMultiple hauls occurred on this date. Please verify correct dumpster.â€
- **Acceptance Criteria:** Alert appears when applicable; user must confirm selection before saving.

## Day 3 — Story 115
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Uniqueness Confirmation
- **Task Name:** Confirm When Only One Haul Exists for a Date
- **User Story:** As a tonnage processor, I want a confirmation banner telling me there is only one haul for the date so I know I can safely enter the weight without checking for duplicates.
- **Description:** System checks if the haul date exists only once for that hauler/site; if so, shows a green banner: â€œUnique haul â€” no duplicates.â€
- **Acceptance Criteria:** Banner is displayed automatically and disappears after save; record completes without additional manual verification.

## Day 3 — Story 116
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Simplified Verification
- **Task Name:** Display Pre-Validated Context Before Entry
- **User Story:** As a tonnage processor, I want the system to verify uniqueness before I perform manual checks so I can reduce unnecessary time spent researching dates and dumpsters.
- **Description:** UI automatically performs a uniqueness and duplicate-risk analysis and shows results at the top of the entry screen.
- **Acceptance Criteria:** Processor can enter tonnage without scrolling through multiple screens; record saves successfully and logs verification state.

## Day 3 — Story 117
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Attachment & Entry
- **Task Name:** Enter Tonnage With Invoice & Weight Ticket Attached
- **User Story:** As a tonnage processor, I want the UI to streamline attaching weight tickets and invoices when entering tonnage so the process is fast, accurate, and traceable.
- **Description:** The system must allow attaching files directly at the moment of tonnage entry and store them in a consistent location along with required metadata.
- **Acceptance Criteria:** Tonnage entry saves successfully with files attached; attachments display in the siteâ€™s tonnage history without broken links.

## Day 3 — Story 118
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** System Attribution
- **Task Name:** Differentiate System-Entered vs User-Entered Tonnage
- **User Story:** As a tonnage processor, I want the system to clearly show who entered a tonnage (system vs staff) so I can identify source reliability and avoid confusion.
- **Description:** System must stamp user ID for manual entries and a clear â€œSystem â€” Automated Hub Entryâ€ label for automated ones.
- **Acceptance Criteria:** UI consistently displays correct attribution in all tonnage history and reporting screens.

## Day 3 — Story 119
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** System Name Standardization
- **Task Name:** Replace Developer or Account Names With a Neutral System Account
- **User Story:** As a tonnage processor, I want automated hub tonnage entries to show as a neutral 'System Account' instead of developer names so it is clear these were not manually processed.
- **Description:** System must no longer use individual employee names for automated processes; all must be standardized to a recognizable neutral label.
- **Acceptance Criteria:** All automated entries across all modules reflect the new system account identifier.

## Day 3 — Story 120
- **Epic:** Tonnage Collection & Validation
- **Feature:** Invoice & Weight Source Retrieval
- **Parent Task:** Locate Weight Tickets Across Multiple Sources
- **Task Name:** As a tonnage processor, I want easier access to weight tickets and invoices across Rossum, inboxes, and dispatch emails so I donâ€™t have to search multiple systems manually.
- **User Story:** UI must provide direct links to both parsed Rossum invoices and raw unparsed inbox sources; system should highlight which have weight attachments.
- **Description:** User can retrieve required files without manually checking multiple inboxes; system logs retrieval source.

## Day 3 — Story 121
- **Epic:** Tonnage Collection & Validation
- **Feature:** Invoice & Weight Source Retrieval
- **Parent Task:** Identify Missing Addresses in Invoices
- **Task Name:** Improve Visibility When Hauler Invoices Lack Addresses
- **User Story:** As a tonnage processor, I want the system to warn me when an invoice lacks a service address so I know I must perform additional verification.
- **Description:** System must detect missing address fields and display a warning banner with suggested next steps (site lookup, manual check, or cross-reference).
- **Acceptance Criteria:** Warning banner appears on upload or viewing; processor can proceed with informed context.

## Day 3 — Story 122
- **Epic:** Tonnage Collection & Validation
- **Feature:** Invoice & Weight Source Retrieval
- **Parent Task:** Raw-Source Fallback
- **Task Name:** Provide Access to Raw Emails When Parsed Rossum Data Is Insufficient
- **User Story:** As a tonnage processor, I want quick access to the original unparsed email when Rossum does not match or categorize the invoice so I donâ€™t miss weight information.
- **Description:** UI must include a â€œView Original Email Sourceâ€ link for every parsed Rossum item.
- **Acceptance Criteria:** User can retrieve and cross-check original documents without leaving Cube.

## Day 3 — Story 123
- **Epic:** Tonnage Collection & Validation
- **Feature:** Invoice & Weight Source Retrieval
- **Parent Task:** Unified Search
- **Task Name:** Search Invoices & Tickets Across All Available Sources
- **User Story:** As a tonnage processor, I want a unified search tool that searches across parsed Rossum, raw Rossum inbox, dispatch inbox, and tonnage inbox so I can find weight documents quickly.
- **Description:** Search must support hauler name, site address, invoice number, haul date, and tonnage values.
- **Acceptance Criteria:** Search returns results from all sources in one list; system logs where the file originated.

## Day 3 — Story 124
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Report-Driven Workflow
- **Task Name:** Support Tonnage Entry Driven Entirely From the Report View
- **User Story:** As a tonnage processor, I want the ability to complete 99% of my job using the Tonnage Report screen so I donâ€™t have to jump between multiple pages.
- **Description:** Report must show all fields, attachments, historical tonnage, uniqueness indicators, hauler rules, and include quick actions for entry.
- **Acceptance Criteria:** Processor completes tasks without leaving the main report; no workflow requires deep navigation.

## Day 3 — Story 125
- **Epic:** Tonnage Collection & Validation
- **Feature:** Tonnage Entry Workflow
- **Parent Task:** Uniqueness Verification Reduction
- **Task Name:** Automate Duplicate-Checking Work Andrew Manually Performs
- **User Story:** As a tonnage processor, I want the system to automate the duplicate checking I currently do manually so I can process tonnage faster.
- **Description:** System must check multiple dumpsters, haul dates, past entries, and provide clear â€œUniqueâ€ or â€œPossible Duplicateâ€ status.
- **Acceptance Criteria:** System resolves uniqueness 90%+ of the time without Andrew manually verifying the site page.

## Day 3 — Story 126
- **Epic:** Tonnage Collection & Validation
- **Feature:** Billing & Tonnage Calculations
- **Parent Task:** Calculate Total Tonnage Including Overages
- **Task Name:** As a tonnage processor, I want the system to automatically calculate total tonnage (included + overage) so I donâ€™t have to compute it manually.
- **User Story:** System must read an overage-only invoice and automatically add the haulerâ€™s included tonnage amount from contract settings.
- **Description:** System produces the correct total tonnage; user can override if needed with justification.

## Day 3 — Story 127
- **Epic:** Tonnage Collection & Validation
- **Feature:** Billing & Tonnage Calculations
- **Parent Task:** Show Included Tons on Report
- **Task Name:** Display Contractual Included Tons Next to Each Pending Ticket
- **User Story:** As a tonnage processor, I want included tonnage displayed on the report so I know whether the invoice represents full tonnage or only overage.
- **Description:** Report shows included tons per hauler/dumpster type without needing to open the site or contract.
- **Acceptance Criteria:** Processor enters accurate tonnage without performing external math or secondary lookups.

## Day 3 — Story 128
- **Epic:** Tonnage Collection & Validation
- **Feature:** Billing & Tonnage Calculations
- **Parent Task:** Auto-Calculate From Overages
- **Task Name:** Allow System to Compute Full Weight When Only Overage Is Provided
- **User Story:** As a tonnage processor, I want the system to compute full tonnage automatically when the hauler only sends the chargeable overage so I donâ€™t have to reconstruct the total.
- **Description:** System must detect when only overage is listed, pull included tonnage amount, auto-add, and propose the total.
- **Acceptance Criteria:** User reviews system-calculated total; system logs calculation source and reasoning.

## Day 3 — Story 129
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** Capture Confirmation Status
- **User Story:** As an Event Coordinator, I want each event toilet delivery to have a confirmation status recorded in-system so that supervisors can see which haulers have confirmed delivery for upcoming events.
- **Description:** Andrew currently confirms delivery by calling hundreds of haulers manually every Thursday, recording results in a spreadsheet outside the system. The system needs fields and UI that allow him to log the confirmation status, who confirmed it, and any notes, directly inside Quickbase/Cube.
- **Acceptance Criteria:** The UI allows Andrew to record: confirmation status, confirmation date, who confirmed, and notes. Data is visible in reports. Supervisors can view updated statuses in real time. No spreadsheet dependence.

## Day 3 — Story 130
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** Add Status Field to Report
- **User Story:** As a user, I want the event toilet report to show confirmation status inline so I can see at a glance what has been completed without needing additional documents.
- **Description:** Andrew must currently maintain a separate spreadsheet of confirmations. The report must include a 'Status' field showing: Confirmed, Not Confirmed, Unable to Reach, Cancelled, Fulfillment Pending, and internal notes.
- **Acceptance Criteria:** Report displays new status field; statuses change color based on type (e.g., green for confirmed).

## Day 3 — Story 131
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** Mark List Complete
- **User Story:** As a user, I want a 'Mark Day Complete' toggle so that when I finish all calls for an event week, the system can automatically send the completion summary to supervisors.
- **Description:** Andrew manually compiles a spreadsheet and emails it to supervisors when done. System should automate emailing the final compiled report.
- **Acceptance Criteria:** Button/toggle triggers: report summary generation, emailing, and saves a stamp indicating completion date.

## Day 3 — Story 132
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** High Volume Scaling Support
- **User Story:** As a user, I want the system to help manage extremely large weekly lists (often 100â€“200+ event toilets) so I can process confirmations efficiently.
- **Description:** Andrew calls hundreds of haulers each Thursday. UI must support fast workflow: filtering, grouping by hauler, bulk marking attempts, and notes.
- **Acceptance Criteria:** User can group by hauler, filter by region or date, and sort by status.

## Day 3 — Story 133
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Email Automation
- **Task Name:** Automated Hauler Reminder Emails
- **User Story:** As the system, I want to send automated Thursday reminder emails to haulers asking them to confirm event toilet deliveries, reducing manual phone calls.
- **Description:** Discussion acknowledges ROI potential. System should generate hauler email batches based on next week's scheduled event toilets.
- **Acceptance Criteria:** System generates batch email preview, groups by hauler, sends single email per hauler per Thursday.

## Day 3 — Story 134
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Ops Coordination
- **Task Name:** Ops Review Integration
- **User Story:** As a supervisor, I want a system-generated weekly summary so Ops can review which event toilets are confirmed, pending, or at risk.
- **Description:** Currently, supervisors only receive Andrewâ€™s spreadsheet via email. Summary should be visible in UI and emailed automatically.
- **Acceptance Criteria:** Ops receives summary report; summary includes totals: confirmed, pending, unreachable.

## Day 3 — Story 135
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** Event Type Importance Indicator
- **User Story:** As a user, I want the system to highlight high-risk events (weddings, corporate events, festivals) so I can prioritize calling those haulers first.
- **Description:** Andrew explains wedding deliveries are extremely critical and cause severe customer impact if missed.
- **Acceptance Criteria:** System labels important events; high-risk events appear at top; alerts provided.

## Day 3 — Story 136
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** Integrate Legacy Event Data
- **User Story:** As a user, I want existing event toilet dataâ€”previously handled by SysOpsâ€”to be integrated into the unified workflow.
- **Description:** Kelly notes a prior SysOps project created event toilet reporting. The new system must incorporate those datasets.
- **Acceptance Criteria:** Existing Quickbase event data appears in new workflow; no manual migration needed.

## Day 3 — Story 137
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Email Automation
- **Task Name:** Hub-Based Email Migration
- **User Story:** As a system owner, I want all event toilet communications migrated to the Hub to ensure proper logging and avoid Quickbase email limitations.
- **Description:** Justin notes Quickbase emails were previously discontinued due to logging issues. Event toilet messaging should follow the same migration pattern as tonnage communications.
- **Acceptance Criteria:** Hub template created; emails logged; replies tracked; no Quickbase emails sent.

## Day 3 — Story 138
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** Capture Confirmation Details
- **User Story:** As a user, I want fields to record who confirmed (hauler rep name), confirmation time, and outcome notes.
- **Description:** Andrew currently records details in a spreadsheet. These must be captured in-system.
- **Acceptance Criteria:** Fields exist for rep name, confirmation timestamp, and notes.

## Day 3 — Story 139
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** In-System Visibility
- **User Story:** As a supervisor, I want visibility into confirmation progress without depending on Andrewâ€™s email attachments.
- **Description:** Andrewâ€™s current email is the only record of confirmation.
- **Acceptance Criteria:** Supervisors can filter by date, hauler, and status. No spreadsheets required.

## Day 3 — Story 140
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Ops Coordination
- **Task Name:** Progress Monitoring Dashboard
- **User Story:** As Ops, I want a dashboard showing real-time progress each Thursday so we know when Andrew needs help.
- **Description:** Justin describes scenarios where Andrew might be overwhelmed (e.g., 200 calls, limited time). UI needs progress bars and auto-alert thresholds.
- **Acceptance Criteria:** Dashboard shows % complete, number left, risk items. Threshold alerts trigger notifications.

## Day 3 — Story 141
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Ops Coordination
- **Task Name:** Late-Day Alert System
- **User Story:** As the system, I want to automatically notify Ops if a large number of confirmations remain late on Thursday.
- **Description:** If it's 4:00 PM and many items remain unconfirmed, Ops needs to know immediately.
- **Acceptance Criteria:** Alert triggers when: time â‰¥ 4 PM AND unconfirmed count > threshold.

## Day 3 — Story 142
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** Event Toilet Weekly Confirmation
- **Parent Task:** Event Toilet Outreach
- **Task Name:** Spreadsheet Replacement
- **User Story:** As a user, I want the system to replace the need for external spreadsheets entirely.
- **Description:** The goal is to remove manual spreadsheet tasks and provide all capabilities in-system.
- **Acceptance Criteria:** System allows recording, filtering, grouping, exporting, and emailing without spreadsheets.

## Day 3 — Story 143
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** User Workflow & Process Improvements
- **Parent Task:** VM Team Support
- **Task Name:** Low-Hanging Fruit Enhancements
- **User Story:** As a user, I want certain small improvements (fields, checkboxes, report cleanups) added immediately within Quickbase so that I don't need to wait months for the full Cube build.
- **Description:** Justin explains that some enhancementsâ€”such as adding checkboxes, adding missing fields, improving report layout, and enabling automated emailsâ€”can be completed now without waiting for the long-term Cube implementation.
- **Acceptance Criteria:** Basic enhancements are deployed in Quickbase: additional fields exist, checkboxes function, automated email triggers work, and reports load cleanly.

## Day 3 — Story 144
- **Epic:** Event Toilet Confirmation Workflow
- **Feature:** User Workflow & Process Improvements
- **Parent Task:** VM Team Support
- **Task Name:** User Story Capture & Future Questions
- **User Story:** As a developer, I want to ask follow-up questions after reviewing recordings so I can understand Andrewâ€™s process fully.
- **Description:** Justin notes developers may feel overwhelmed and will produce more questions later. The system must ensure questions are tracked and not lost.
- **Acceptance Criteria:** Developers can log questions; product owner receives notifications; questions link back to user stories.

## Day 3 — Story 145
- **Epic:** Document & Reporting Integration
- **Feature:** Document Storage
- **Parent Task:** Hauler Document Management
- **Task Name:** Migrate Hauler Documents Into Cube Repository
- **User Story:** As a user, I want all hauler documents (currently in OneDrive/SharePoint) migrated into the Cube repository so that everyone can access them centrally.
- **Description:** Justin states hauler docs are currently scattered across OneDrive/SharePoint. They must be stored inside Cube for consistency, permissions, and unified access.
- **Acceptance Criteria:** All hauler docs uploaded into the Cube repository and linked to hauler profiles. Permissions match role-based rules.

## Day 3 — Story 146
- **Epic:** Data Integration & Modeling
- **Feature:** Cluster & Zone Data Mapping
- **Parent Task:** Statistical Model Integration
- **Task Name:** Expose Cluster Data in Cube
- **User Story:** As a user, I want cluster numbers (from the statistical model) mapped to zip codes inside the Cube so I can compare PSP zones with cluster performance data.
- **Description:** Cluster IDs exist only in Power BI/statistical model. They are not visible anywhere in Quickbase. Hauler team uses these clusters for comparisons and evaluations.
- **Acceptance Criteria:** Cube shows each zip codeâ€™s cluster ID(s); reports can group/filter by cluster; PSP zones show associated clusters.

## Day 3 — Story 147
- **Epic:** Data Integration & Modeling
- **Feature:** Cluster & Zone Data Mapping
- **Parent Task:** Statistical Model Integration
- **Task Name:** Create Cluster Table in Quickbase
- **User Story:** As an admin, I need a cluster table created in Quickbase to store zip-to-cluster relationships.
- **Description:** Kelly suggests creating a Quickbase table and importing cluster data from Power BI. This becomes the parent table for zip codes.
- **Acceptance Criteria:** Cluster table created; import script executed; zip code records linked to cluster records.

## Day 3 — Story 148
- **Epic:** UI/UX Navigation Improvements
- **Feature:** UI Navigation Optimization
- **Parent Task:** Role-Based Navigation
- **Task Name:** Tab Prioritization & Favorites
- **User Story:** As a user, I want to mark certain frequently used tabs as favorites so I can quickly access the areas I use most without being overwhelmed by 20+ tabs.
- **Description:** Anthony suggests allowing favorite tabs or hiding less-used tabs, but ensuring theyâ€™re still accessible somewhere so users donâ€™t think features disappeared.
- **Acceptance Criteria:** Users can set favorites; UI shows favorites first; non-favorites appear in secondary dropdown; nothing is permanently hidden.

## Day 3 — Story 149
- **Epic:** UI/UX Navigation Improvements
- **Feature:** UI Navigation Optimization
- **Parent Task:** Role-Based Navigation
- **Task Name:** Frequency-Based Tab Weighting
- **User Story:** As the system, I want to weight tabs by usage frequency so the UI presents commonly-used tabs more prominently.
- **Description:** Justin describes that across departments, virtually all tabs are neededâ€”so the UI should emphasize frequency instead of hiding content.
- **Acceptance Criteria:** System tracks usage frequency; UI automatically promotes commonly accessed groups; low-frequency tabs move into secondary groups.

## Day 3 — Story 150
- **Epic:** UI/UX Navigation Improvements
- **Feature:** UI Navigation Optimization
- **Parent Task:** Role-Based Navigation
- **Task Name:** Permission-Based Grayed-Out Buttons
- **User Story:** As a restricted user, I want disabled features to appear grayed-out with tooltips explaining my lack of permission, so I understand why I cannot click them.
- **Description:** Anthony explains that hiding buttons causes confusion in support calls. Grayed-out buttons with tooltips reduce support load.
- **Acceptance Criteria:** Buttons appear grayed out; tooltip states permission reason; user cannot interact with disabled controls.

## Day 3 — Story 151
- **Epic:** Hauler Pricing & Service Zones
- **Feature:** Zip Code List Enforcement
- **Parent Task:** PSP Pricing Zones
- **Task Name:** Validate Unique Zip Code Coverage
- **User Story:** As a VM user, I want the system to enforce uniqueness and validate overlaps in PSP zone zip code lists so that we avoid conflicting pricing coverage and bad routing decisions.
- **Description:** Current PSP pricing zones allow free-form zip code lists with little validation, creating overlaps and manual cleanup work. The new UI should guide users to build zones with validated, non-conflicting zip lists and surface any conflicts for resolution.
- **Acceptance Criteria:** When creating or editing a PSP zone, the UI validates zip codes in real time, flags overlaps with other zones for the same product and geography, and prevents saving obviously conflicting configurations unless explicitly overridden with a documented reason. A zone detail view clearly shows its zip coverage and any conflict indicators.

## Day 3 — Story 152
- **Epic:** Hauler Pricing & Service Zones
- **Feature:** Franchised Area Management
- **Parent Task:** PSP Pricing Zones
- **Task Name:** Represent Franchised Municipalities in Zone Logic
- **User Story:** As a VM user, I want franchised municipalities and zip codes modeled in the system so that the pricing and dispatch flows always route jobs to the only legally allowed hauler for that area.
- **Description:** Justin explains that some municipalities are franchised, meaning only a single hauler can legally provide service. Today this is partially flagged on the zip table but is not tied into pricing zones or selection logic, leading to incorrect hauler assignments in franchised areas.
- **Acceptance Criteria:** UI allows marking specific zips or sub-areas as franchised and assigning the mandated hauler. When a user quotes or books a job in that area, the system warns that only the franchised hauler is allowed and preselects that hauler, suppressing PSP or other hauler options unless a specific override path is followed.

## Day 3 — Story 153
- **Epic:** Hauler Pricing & Service Zones
- **Feature:** Customer Price Reference Handling
- **Parent Task:** Pricing Tool Cleanup
- **Task Name:** Clarify or Remove Calculated Customer Prices
- **User Story:** As a product owner, I want a clear UX decision around calculated customer prices (reference-only) so that we either present them purposefully or simplify the pricing tool by removing confusing, unused fields.
- **Description:** Justin notes that PSP pricing records contain vendor prices plus an automatically calculated customer price that is often only informational and duplicates calculations already made elsewhere. Some users find it useless, others occasionally reference it, creating UX ambiguity.
- **Acceptance Criteria:** The UI for PSP pricing clearly labels reference-only customer price values and distinguishes them from authoritative billing values, or those fields are removed entirely. Any remaining reference fields include hover help explaining their purpose and origin.

## Day 3 — Story 154
- **Epic:** Vendor Management Core Operations
- **Feature:** VM Activity Logging
- **Parent Task:** VM Tickets
- **Task Name:** Enforce Activity Log for VM Work
- **User Story:** As a VM agent, I want the system to require that I log calls and emails on VM tickets so that every resolution has a clear, auditable activity trail.
- **Description:** Justin describes that some VM team members diligently log every call and email, while others resolve tickets without any activity entries, making it impossible to see what work was done. The new system must enforce consistent logging before tickets can be closed.
- **Acceptance Criteria:** The ticket UI provides a guided activity log component where users select activity type (call, email, meeting, note), capture minimal required fields, and attach related correspondence. Attempting to close a ticket with no activity prompts a blocking error or guided reminder to add at least one activity.

## Day 3 — Story 155
- **Epic:** Vendor Management Core Operations
- **Feature:** PSP Justification & Scorecard
- **Parent Task:** VM Tickets
- **Task Name:** Checklist-Based PSP Justification
- **User Story:** As a VM manager, I want a structured PSP justification checklist instead of a free-text field so that decisions are consistent and support scorecards and reporting.
- **Description:** Justin reiterates that the current PSP justification is a single field and that they want a more comprehensive, structured scorecard-style breakdown (close rates, cluster coverage, pricing, service quality, etc.) rather than subjective notes.
- **Acceptance Criteria:** The PSP justification UI presents a checklist and scored fields (for service quality, price competitiveness, zone coverage, response time, complaints, etc.), plus optional notes. The system calculates an overall PSP score that can be used in reports and reviews.

## Day 3 — Story 156
- **Epic:** Hauler Data & Documents
- **Feature:** Hauler Contact Normalization
- **Parent Task:** Data Cleanup
- **Task Name:** Move Contacts Into Hauler Contacts Table
- **User Story:** As a data steward, I want all hauler contact information stored in a dedicated hauler contacts table so that contact management is consistent, scalable, and not duplicated in the hauler record.
- **Description:** Justin states that contact data is currently mixed into the hauler record and must be stripped out and moved into a proper hauler contacts table for future Cube usage. This applies to all roles and email/phone combinations linked to a hauler.
- **Acceptance Criteria:** The data model exposes a one-to-many relationship from hauler to contacts. The hauler detail UI shows a contacts sub-grid where users can add, edit, or deactivate contacts without touching core hauler fields. Old in-record contact fields are deprecated and read-only or removed.

## Day 3 — Story 157
- **Epic:** Hauler Data & Documents
- **Feature:** Document & Attachment Cleanup
- **Parent Task:** Data Cleanup
- **Task Name:** Consolidate Hauler Attachments Into Repository
- **User Story:** As an admin, I want miscellaneous file attachment fields removed and converted into structured documents so that hauler-related files are consistently stored, searchable, and not bloating records as opaque blobs.
- **Description:** Justin notes there are many miscellaneous attachment fields and redundant W9/COI-related blobs in the hauler record. These must be simplified, with key documents (COI, W9) kept in clear fields and all others pulled into a unified document repository.
- **Acceptance Criteria:** The new design replaces multiple ad-hoc attachment fields with a documents table linked to haulers (and possibly contacts). The hauler UI shows a document section with type, date, and status. Specific key-doc fields (like primary COI and W9) are handled with dedicated, clearly labelled slots if needed.

## Day 3 — Story 158
- **Epic:** Hauler Data & Documents
- **Feature:** Provider Portal Credential Visibility
- **Parent Task:** VM Hauler Maintenance
- **Task Name:** Promote Provider Portal Credentials In UI
- **User Story:** As a VM agent, I want provider portal URLs and credentials displayed prominently on the hauler screen so that I can quickly log into hauler portals while working cases.
- **Description:** Justin mentions that provider portal information is currently buried at the bottom of the contact tab and plans to move it up, indicating it is highly relevant for VM work.
- **Acceptance Criteria:** The hauler UI surfaces provider portal URL, username, and related notes in a top-level section or easily visible tab. Optional security-safe patterns (copy-to-clipboard, masked passwords) support frequent access without clutter.

## Day 3 — Story 159
- **Epic:** Hauler Relationship & Lifecycle
- **Feature:** Hauler Buyout Visibility
- **Parent Task:** Relationship Mapping
- **Task Name:** Show Buyout Links On Hauler Pages
- **User Story:** As a VM user, I want to clearly see when one hauler has been bought out by another so that I understand historical relationships and route work to the correct current entity.
- **Description:** Justin explains that when a hauler is bought out, they currently mark DNU and relate it to the new hauler via a VM ticket, but this relationship is not visible on the hauler pages themselves.
- **Acceptance Criteria:** The hauler UI shows a clear buyout section for each affected hauler: an old DNU hauler shows who purchased them, and the current hauler lists all absorbed haulers. This section is visually distinct and accessible without opening VM tickets.

## Day 3 — Story 160
- **Epic:** Out-of-Stock & Availability Management
- **Feature:** Out-of-Stock Notices
- **Parent Task:** Product-Level Availability
- **Task Name:** Granular Out-of-Stock Tracking By Product Type
- **User Story:** As a VM user, I want to mark specific product types as out of stock for a hauler so that pricing and quoting avoid offering products that cannot be fulfilled.
- **Description:** Justin describes current out-of-stock notices where VM tracks product shortages (like 10-yard dumpsters) with partial date logic but no granular product links or verification flags, resulting in quoting unavailable items.
- **Acceptance Criteria:** Out-of-stock notices can be created at the hauler and product-type level with clear start and expected end dates. The system prevents or warns against quoting products that are marked out of stock for that hauler during that period.

## Day 3 — Story 161
- **Epic:** Out-of-Stock & Availability Management
- **Feature:** Out-of-Stock Integration With Pricing
- **Parent Task:** Product-Level Availability
- **Task Name:** Sync Out-of-Stock Notices With PSP Pricing Records
- **User Story:** As a pricing user, I want out-of-stock notices to automatically adjust PSP pricing records so that the pricing tool does not surface haulers for products they cannot currently deliver.
- **Description:** Justin proposes tying out-of-stock notices directly to PSP pricing records so that, for example, Joe PSPâ€™s 10-yard pricing is automatically marked DNU while they are out of stock, instead of continuing to show as available in the pricing tool.
- **Acceptance Criteria:** When an out-of-stock notice is active for a hauler and product type, the associated PSP pricing records are auto-flagged as unavailable for selection in the pricing tool. When availability is reverified, a simple confirmation re-enables those records.

## Day 3 — Story 162
- **Epic:** Hauler Relationship & Check-Ins
- **Feature:** Hauler Checkup Workflow
- **Parent Task:** Non-PSP Hauler Management
- **Task Name:** Track Non-PSP Hauler Checkups
- **User Story:** As a VM manager, I want a structured checkup process and tracking for non-PSP haulers so that we know who has been reviewed, when, and by whom.
- **Description:** Justin notes that VM staff periodically call non-PSP haulers to verify information but have no report, schedule, or field tracking which haulers were checked, when it was done, or what was confirmed. They essentially draw names at random and do not record outcomes.
- **Acceptance Criteria:** Hauler records include fields for last checkup date, next due date, and last checked by, plus an activity log entry for each checkup. Reports can show overdue checkups and prioritize who should be contacted next.

## Day 3 — Story 163
- **Epic:** COI & Compliance Management
- **Feature:** COI Requirements Enforcement
- **Parent Task:** Compliance Rules
- **Task Name:** Enforce COI and Additional Insured Rules
- **User Story:** As a compliance owner, I want the system to enforce that valid COIs exist and that letters of authorization are not accepted so that we only do business with haulers who meet our risk requirements.
- **Description:** Justin explains that some team members misunderstand COI requirements and try to treat letters of authorization as acceptable, but policy is that haulers must provide a COI and may need additional insured confirmation for ZTERS.
- **Acceptance Criteria:** The UI for hauler compliance requires a valid COI document, captures coverage amounts and additional insured status, and blocks hauler activation if COIs are missing or expired. No fields exist for storing letters of authorization as an alternative, and help text clearly explains why.

## Day 3 — Story 164
- **Epic:** Pricing Automation & Adjustments
- **Feature:** Price Increase Automation
- **Parent Task:** Bulk Pricing Updates
- **Task Name:** Apply Percentage Price Changes Automatically
- **User Story:** As a pricing analyst, I want to apply percentage-based price increases across selected haulers and products so that I do not have to manually update dozens or hundreds of pricing records.
- **Description:** Justin describes a common scenario where a hauler calls and increases prices (for example, all toilets by 10 percent), and the team must manually find and update many pricing records or grid-edit them, which is error-prone.
- **Acceptance Criteria:** The pricing UI offers a bulk adjustment tool where users select hauler(s), product types, and target records (PSP or non-PSP) and specify a percentage or fixed increase. The system preview shows before/after values and applies adjustments in one operation.

## Day 3 — Story 165
- **Epic:** Grid & Report UX
- **Feature:** Table & Grid Experience
- **Parent Task:** Report Usability
- **Task Name:** Provide Spreadsheet-Like Report Grids
- **User Story:** As a power user, I want report tables in Cube to behave more like spreadsheets (sorting, filtering, resizing, basic color cues) so that I do not need to export data just to work efficiently.
- **Description:** Justin notes that users like Andrew default to spreadsheets because Quickbase tables are frustrating; he calls for a rich Laravel module for tables with better sorting, coloring, and resizing to match spreadsheet comfort.
- **Acceptance Criteria:** Core grid components in the app support multi-column sorting, inline filtering, adjustable column widths, optional conditional highlighting, and keyboard navigation. These features are consistent across hauler, pricing, and VM reports.

## Day 3 — Story 166
- **Epic:** Development Planning & Governance
- **Feature:** Database Design Support
- **Parent Task:** Hauler Module Planning
- **Task Name:** Prioritize Hauler Database Mapping
- **User Story:** As a product owner, I want to focus first on accurate hauler-related database mapping so that the dev team has a stable schema foundation before building UI flows and complex processes.
- **Description:** Kelly emphasizes that before heavy process work in Q1, the priority for the remainder of the year is validating table structures for PSP, VM, and some tonnage, so UI and functionality can grow on a solid model.
- **Acceptance Criteria:** Database diagrams for hauler, PSP, VM, and tonnage tables are reviewed, with key fields and relationships called out. Devs and PO agree on which tables need normalization, which can be reused, and which are â€œtrashâ€ that must be redesigned.

## Day 3 — Story 167
- **Epic:** Development Planning & Governance
- **Feature:** Collaboration Model
- **Parent Task:** Hauler Module Planning
- **Task Name:** Align Responsibilities for DB and Process Artifacts
- **User Story:** As a dev team, we want clarity on who produces database maps, flowcharts, and process lists so that we minimize duplicate work and know where to look for canonical documentation.
- **Description:** Justin and Dhaval discuss that Justin has detailed current-system DB maps, while the dev team will create a microservice-based schema that diverges slightly. Kelly stresses prioritizing schema and framework feedback so UX design can start in December.
- **Acceptance Criteria:** A shared documentation space (for example, a hauler research folder) exists containing current-system maps, proposed schema, and agreed responsibilities: Justin focuses on mapping and calling out problem areas; devs own microservice schema; UX relies on those artifacts for layouts.

## Day 3 — Story 168
- **Epic:** Development Planning & Governance
- **Feature:** Framework Feedback & UI Kickoff
- **Parent Task:** Platform Foundation
- **Task Name:** Complete Framework Feedback To Unblock UX
- **User Story:** As a framework reviewer, I want to finalize feedback on the application framework so that Ashish and Anthony can start designing hauler UI/UX prototypes on time.
- **Description:** Kelly reminds Justin that Ashish and Anthony are waiting for framework feedback and must begin design within about two weeks; without that, they cannot map fields or build screens for the hauler module.
- **Acceptance Criteria:** Framework options are reviewed and one chosen or refined. Feedback is documented and shared with UX and devs so that layout, routing, and component decisions are based on a stable foundation.

## Day 3 — Story 169
- **Epic:** Development Planning & Governance
- **Feature:** Workshop Closure & Next Steps
- **Parent Task:** Planning & Coordination
- **Task Name:** Break Out Videos and User Stories Per Topic
- **User Story:** As a project lead, I want recordings split and tagged per topic and backed by user stories so that developers can reference exactly the footage and stories they need when building features.
- **Description:** Anthony states he will break the long videos into topical segments and tie each to tasks so devs can rewatch relevant parts and pair them with user stories instead of scanning the entire workshop.
- **Acceptance Criteria:** A task list exists where each feature/user story links to both a short video segment and its text description. Devs can quickly jump from a story to the exact demonstration or explanation in the recording.

---
