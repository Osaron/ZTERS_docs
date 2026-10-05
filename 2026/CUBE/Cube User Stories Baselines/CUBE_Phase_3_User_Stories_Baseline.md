# CUBE User Stories — Phase 3 Baseline

**Purpose:** Reference baseline for comparing later CUBE phases against Phase 3. Use together with the Phase 2 baseline when classifying later user stories as **Existing**, **New Feature**, or **Hybrid**.

**Phase 3 scope:**
- Day 1: 21 user stories
- Day 2: 25 user stories
- Day 3: 28 user stories
- Day 4: 30 user stories
- Day 5: 20 user stories
- **Total: 124 user stories**

**Comparison guidance:**
- Compare later stories by underlying functionality, not wording alone.
- Use the User Story together with Description, Acceptance Criteria, Notes, and JT Notes where present.
- A later story may be **Existing** if Phase 3 already covers the same capability, or **Hybrid** if the capability exists but the later phase adds a meaningful behavior, workflow, rule, field, integration, permission, UI change, or extension.

---

# Day 1

**Stories:** 21

## CUBE-D1-001
- **Group:** Customer Management
- **Category:** UI/UX
- **Epic:** Customer Overview Redesign
- **Parent Task:** Customer Financial Snapshot
- **Task Name:** Display Accurate Customer Since Date
- **User Story:** As an Account Manager (AM), I want the Customer Since date to reflect the earliest confirmed relationship date, so that account tenure is historically accurate.
- **Description:** The workshop identified inconsistencies in historical tenure dates. The system must calculate the earliest valid engagement date from legacy records rather than relying on record creation timestamps. This ensures executive reporting reflects true customer longevity and prevents misleading tenure data.
- **Timestamp:** Day 1, Part 1 [1:48:30 – 1:50:10]
- **Notes:** Fixes legacy tenure inconsistencies. Prevents leadership misinterpretation. Requires backend reconciliation during migration.
- **Responsible:** TBD
- **JT Notes:** Will definitely require consideration for migration. Currently uses [Date Created] and [Volusion ID Entry Date] fields. Using actual sale dates makes more sense and would be improvement. Can remain formulaic and non-overrideable.

## CUBE-D1-002
- **Group:** Customer Management
- **Category:** UI/UX
- **Epic:** Customer Overview Redesign
- **Parent Task:** Line Item Reference Panel
- **Task Name:** Display Recent Line Items
- **User Story:** As an Account Manager (AM), I want to view recent line items directly in the customer profile, so that I can quickly understand billing activity without deep navigation.
- **Description:** Users expressed frustration navigating multiple levels to view transactions. The system must display recent activity in a summary panel to reduce navigation time and provide immediate context.
- **Timestamp:** Day 1, Part 2 [0:14 – 0:45]
- **Notes:** Solves being multiple levels deep without context. Requires optimized queries for performance.
- **Responsible:** TBD
- **JT Notes:** Clicking the item opens the item detail, not invoice. Invoice will be reachable from item detail.

## CUBE-D1-003
- **Group:** Billing & Recurring
- **Category:** Functional Logic
- **Epic:** Billing Preferences Management
- **Parent Task:** Billing Hierarchy Logic
- **Task Name:** Apply Billing Preference Hierarchy
- **User Story:** As an Account Manager (AM), I want billing preference hierarchy enforced, so that invoices always use the correct payment method.
- **Description:** The workshop emphasized billing inconsistencies when preferences are not clearly prioritized. The system must apply a strict hierarchy to prevent unintended payment methods.
- **Timestamp:** Day 1, Part 2 [0:03:25 – 0:06:30]
- **Notes:** Critical to automation. Prevents mischarges. Integrates with Authorize.net tokenization.
- **Responsible:** TBD
- **JT Notes:** Change to association with contact vs customer is still under consideration.

## CUBE-D1-004
- **Group:** Billing & Recurring
- **Category:** Automation
- **Epic:** Recurring Billing Engine
- **Parent Task:** Auto Invoice Creation
- **Task Name:** Automatically Generate Recurring Invoices
- **User Story:** As an Account Manager (AM), I want recurring invoices automatically generated, so that manual billing work is eliminated.
- **Description:** Recurring services require consistent billing cycles. The system must generate invoices based on configured schedules and billing hierarchy.
- **Timestamp:** Day 1, Part 2 [0:8:30 – 0:11:00]
- **Notes:** Reduces manual workload. Requires background scheduler. Must integrate with decline handling.
- **Responsible:** TBD

## CUBE-D1-005
- **Group:** Billing & Recurring
- **Category:** Functional Logic
- **Epic:** Credit & Adjustment Engine
- **Parent Task:** Credit Memo Creation
- **Task Name:** Generate Formal Credit Memo
- **User Story:** As an Account Manager (AM), I want to generate formal credit memos, so that refunds are traceable and compliant.
- **Description:** Credit memos must be formally documented and linked to original invoices for accounting transparency.
- **Timestamp:** Day 1, Part 2 [0:22:45 – 0:25:20]
- **Notes:** Prevents informal adjustments. Syncs with accounting system.
- **Responsible:** TBD

## CUBE-D1-006
- **Group:** Billing & Recurring
- **Category:** Integration
- **Epic:** Billing Preferences Management
- **Parent Task:** Credit Card Storage
- **Task Name:** Secure Tokenized Credit Card Storage
- **User Story:** As an Account Manager (AM), I want credit cards stored via tokenization, so that recurring charges are secure and compliant.
- **Description:** The system must integrate with Authorize.net and store only tokens to maintain PCI compliance.
- **Timestamp:** Day 1, Part 2 [0:23:40 – 0:25:20]
- **Notes:** This solves the friction of full-system transitions between Cube and Hub. The intent is to reduce cognitive load and preserve workflow continuity during billing preference setup
- **Responsible:** TBD

## CUBE-D1-007
- **Group:** Billing & Recurring
- **Category:** Functional Logic
- **Epic:** Recurring Engine
- **Parent Task:** Opt-Out Controls
- **Task Name:** Customer-Level Recurring Opt-Out
- **User Story:** As an Account Manager (AM), I want to apply an opt-out flag to a customer’s recurring billing configuration, so that automated billing and/or processing actions are suspended without deleting the recurring setup.
- **Description:** Recurring automation must respect opt-out flags to allow controlled suspension of automated billing behavior without deleting recurring configurations.
- **Timestamp:** Day 1, Part 2 [0:09:45 – 0:11:20]
- **Notes:** Prevents unintended automation. Integrates with recurring engine.
- **Responsible:** TBD

## CUBE-D1-008
- **Group:** Customer Management
- **Category:** Functional Logic
- **Epic:** Customer Interaction History
- **Parent Task:** Call Aggregation
- **Task Name:** Aggregate Calls by Phone
- **User Story:** As an Account Manager (AM), I want calls grouped by phone number, so that communication history is centralized.
- **Description:** Call logs must be consolidated under correct customer record to prevent fragmented interaction history.
- **Timestamp:** Day 1, Part 2 [0:29:08 – 0:31:43]
- **Notes:** Prevents duplicate customer creation and eliminates fragmented communication history across multiple phone numbers
- **Responsible:** TBD

## CUBE-D1-009
- **Group:** Customer Management
- **Category:** Functional Logic
- **Epic:** Customer Financial Controls Redesign
- **Parent Task:** Customer Credit Configuration
- **Task Name:** Customer Credit Information Tab Implementation
- **User Story:** As a Customer Success Manager (CSM), I want to view and manage customer credit limits and extended credit settings in a centralized Credit Information tab, so that financial exposure and billing eligibility are clearly controlled.
- **Description:** The Credit Information tab must serve as the authoritative source for: Customer credit limit, Extended credit approval, Billing restrictions tied to credit exposure
- **Timestamp:** Day 1, Part 1 [1:44:30 – 1:49:30]
- **Notes:** Extended Credit acts as a manual override to standard credit limits. Visibility of credit exposure must be clear to operational users before invoicing.
- **Responsible:** TBD

## CUBE-D1-010
- **Group:** Customer Management
- **Category:** UI/UX
- **Epic:** Documents & Attachments
- **Parent Task:** Document Upload
- **Task Name:** Upload Customer Documents
- **User Story:** As an Account Manager (AM), I want to upload and categorize documents within a Customer record, so that contracts, agreements, and operational files are centralized and contextually accessible.
- **Description:** Document storage must support categorization and secure retrieval.
- **Timestamp:** Day 1, Part 2 [0:38:00 – 0:39:30]
- **Notes:** Addresses lack of centralized contract storage and improves contextual visibility of customer agreements. Document types must support role-based conditional rendering.
- **Responsible:** TBD

## CUBE-D1-011
- **Group:** Customer Management
- **Category:** Functional Logic
- **Epic:** Documents & Attachments
- **Parent Task:** Entity Association
- **Task Name:** Associate Documents to Entity
- **User Story:** As an Account Manager (AM), I want documents to be associated with specific Customer, Site, or Product records, so that files are displayed contextually and operational context is preserved.
- **Description:** Documents must maintain relationship to relevant entity.
- **Timestamp:** Day 1, Part 2 [0:37:30 – 0:40:30]
- **Notes:** Ensures audit clarity. Avoid cascade delete issues.
- **Responsible:** TBD

## CUBE-D1-012
- **Group:** Customer Management
- **Category:** UI/UX
- **Epic:** Admin Controls
- **Parent Task:** Admin-Only Tab
- **Task Name:** Restrict Admin Fields
- **User Story:** As an Administrator (Admin), I want sensitive configuration fields to be accessible only through an Administrator-only interface, so that operational users cannot modify critical system settings.
- **Description:** Some fields must be restricted to prevent accidental misuse.
- **Timestamp:** Day 1, Part 2 [0:40:30 – 0:43:30]
- **Notes:** Prevents operational errors by isolating system-level conditional logic and configuration fields from standard users. Supports separation of duties.
- **Responsible:** TBD
- **JT Notes:** "Non-admin users must not be able to access admin-only fields via direct URL, API calls, or UI manipulation." may be umis-leading; "admin-only" in this context is a restriction from view for convenience/display purposes, not a security context. There ARE fields that should be defined by RBAC, but list is much smaller and not defined by this view.

## CUBE-D1-013
- **Group:** Customer Management
- **Category:** UI/UX
- **Epic:** Customer Overview Redesign
- **Parent Task:** Activity Snapshot Implementation
- **Task Name:** Display Customer Activity Snapshot
- **User Story:** As a Customer Success Manager (CSM), I want a summarized activity and financial snapshot on the Customer profile, so that I can quickly assess recent activity and exposure without drilling into individual records.
- **Description:** Snapshot provides quick operational awareness.
- **Timestamp:** Day 1, Part 1 [1:38:30 – 1:44:00]
- **Notes:** Reduces need to drill multiple levels (Customer → Site → Product → Service Ticket) to determine recent activity
- **Responsible:** TBD
- **JT Notes:** This will be further clarified and defined in the UI Blocks (UI/UX display guidelines)

## CUBE-D1-014
- **Group:** Customer Management
- **Category:** Functional Logic
- **Epic:** Site Lifecycle Management
- **Parent Task:** Site Creation Workflow
- **Task Name:** Add Site Form with Validation & Conditional Controls
- **User Story:** As an Account Manager (AM), I want to create a new Site within a Customer record with validated address fields and configurable processing flags, so that operational setup is accurate and compliant from the start.
- **Description:** When an AM selects “Add Site” within a Customer record, the system must present a structured form that: Captures service address, Validates required fields, Displays map integration, Enforces required Zip entry, Applies operational processing flags (e.g., opt-outs), Restricts note creation until the record is saved
- **Timestamp:** Day 1, Part 1 [1:11:00 – 1:16:30]
- **Notes:** The Add Site workflow must prevent incomplete or inconsistent site records from being created.
- **Responsible:** TBD
- **JT Notes:** This will be need to be further clarified and defined; site address will require further new features (street/terrain view, etc)

## CUBE-D1-015
- **Group:** Core Platform
- **Category:** Data Integrity
- **Epic:** Historical Data Integrity
- **Parent Task:** Migration Validation
- **Task Name:** Validate Historical Data During Migration
- **User Story:** As an Account Manager (AM), I want historical customer data to be reviewed and validated during system transition, so that legacy inconsistencies (e.g., incorrect customer start dates) are corrected before operational use.
- **Description:** Migration must reconcile tenure, billing, and vendor cost inconsistencies.
- **Timestamp:** Day 1, Part 1 [1:45:30 – 1:48:50]
- **Mockups:** NO MOCKUP
- **Notes:** High go-live risk area. Requires data audit script.
- **Responsible:** TBD

## CUBE-D1-016
- **Group:** Customer Management
- **Category:** UI/UX
- **Epic:** Reviews & Feedback
- **Parent Task:** Negative Review Flagging
- **Task Name:** Flag Low Ratings (Reviews)
- **User Story:** As a Customer Success Manager (CSM), I want negative customer reviews (low satisfaction scores) flagged and surfaced prominently, so that I can take corrective action quickly.
- **Description:** Reviews must surface performance issues quickly.
- **Timestamp:** Day 1, Part 2 [0:36:22 – 0:37:45]
- **Notes:** Supports service quality monitoring.
- **Responsible:** TBD

## CUBE-D1-017
- **Group:** Customer Management
- **Category:** Reporting
- **Epic:** Customer Financial Visibility Redesign
- **Parent Task:** Collections & Invoice Management Panel
- **Task Name:** Customer Collections and Invoice Summary View
- **User Story:** As an Account Manager (AM), I want a Collections and Invoices tab within the Customer profile that displays outstanding invoices and allows me to download a full invoice report, so that I can proactively manage collections and communicate accurate balances to the customer.
- **Description:** Account Managers (AMs) rely on this tab to check all the customer invoice records
- **Timestamp:** Day 1, Part 2 [0:25:00 – 0:28:00]
- **Notes:** This tab directly supports collections workflow.
- **Responsible:** TBD

## CUBE-D1-018
- **Group:** Customer Management
- **Category:** Reporting / UI/UX
- **Epic:** Customer Snapshot Dashboard
- **Parent Task:** Customer Snapshot Analytics Panel
- **Task Name:** Year-over-Year Site Growth Visualization
- **User Story:** As a Customer Success Manager (CSM), I want a dynamic Customer Snapshot tab that visualizes site growth by month and year, so that I can quickly understand customer expansion trends over time.
- **Description:** The Customer Snapshot tab provides a high-level analytical overview of customer site activity.
- **Timestamp:** Day 1, Part 2 [0:26:10 – 0:29:00]
- **Notes:** Must be performant even for large historical datasets.
- **Responsible:** TBD
- **JT Notes:** This will be further clarified and defined in the UI Blocks (UI/UX display guidelines)

## CUBE-D1-019
- **Group:** Customer Management
- **Category:** Functional Logic
- **Epic:** Credit & Refund Adjustment
- **Parent Task:** Refund & Credit Memo Management
- **Task Name:** Refund memos
- **User Story:** As a Customer Success Manager (CSM), I want a Refunds tab that displays credit memos and refund requests associated with a customer, so that financial adjustments are transparent and traceable.
- **Description:** Not all corrections require full credit memo.
- **Timestamp:** Day 1, Part 2 [0:38:00 – 0:42:10]
- **Notes:** Separate from formal credit memo.
- **Responsible:** TBD
- **JT Notes:** Antiquated process; not needed

## CUBE-D1-020
- **Group:** Customer Management
- **Category:** Functional Logic
- **Epic:** Customer Workflow & Task Management
- **Parent Task:** Customer-Level Task Tracking
- **Task Name:** Customer Tasks Tab Implementation
- **User Story:** As an Account Manager (AM), I want a Tasks tab within the Customer profile to create, assign, and track operational follow-up tasks, so that service actions and communications are properly managed and visible across the team.
- **Description:** It allows internal users to: Create tasks, Assign tasks to specific employees (e.g., CSS), Track status (Completed, etc.), Associate tasks with specific Sites and Products, Document follow-up actions (e.g., removal confirmation, quote follow-up, redelivery)
- **Timestamp:** Day 1, Part 1 [0:45:35 – 0:48:20]
- **Notes:** Prevents follow-ups from being lost in email chains.
- **Responsible:** TBD

## CUBE-D1-021
- **Group:** Site Management
- **Category:** Functional Logic
- **Epic:** Site Service Configuration Workflow
- **Parent Task:** Site-Level Service Activation
- **Task Name:** Redirect to Site & Enable Pricing Tool Integration
- **User Story:** As an Account Manager (AM), I want to be redirected to the Site profile after creating it and immediately add a new service using the integrated Pricing Tool, so that I can configure billable services without leaving the workflow.
- **Description:** After saving a newly created Site, the system redirects the user to the Site information page. From there, the user can: Click “Add New Service”, Select product type (Toilet, Roll-off, Container, Fencing, Other Service, Equipment Rental, Front Load, Perm Roll-Off), Click “Get Pricing”, Be redirected to the Hub Pricing Tool.
- **Timestamp:** Day 1, Part 1 [1:12:30 – 1:15:30]
- **Notes:** This is a critical cross-system integration between Cube and Hub. Context preservation is essential (no retyping zip or site info).
- **Responsible:** TBD
- **JT Notes:** This will be further clarified and defined in the UI Blocks (UI/UX display guidelines) as well as additional intake customer flow. Pricing tool should be integrated into the flow/page if possible without redirect. Intake flow should define customer variables for products.

---

# Day 2

**Stories:** 25

## CUBE-D2-001
- **Group:** Pricing & Margin Engine
- **Category:** Functional Logic
- **Epic:** Vendor Pricing Management
- **Parent Task:** Vendor Cost Entry
- **Task Name:** Capture Vendor Base Rate
- **User Story:** As an Account Manager (AM), I want to capture and maintain a vendor’s base cost/rate for a service line item, so that margin calculations and suggested customer pricing are accurate and auditable.
- **Description:** Vendor cost is the starting point for Cube’s pricing logic: it drives suggested customer rates, margin calculations (targeting ~35% where applicable), and downstream approval workflows when margin falls below thresholds. The system must support entering vendor rates in a structured way (currency, validation rules), ensure changes are fully traceable (who/when/what changed), and preserve historical snapshots so previously approved quotes and posted invoices don’t get unintentionally recalculated after a cost update.
- **Timestamp:** Day 2, Part 2 [0:08 – 0:09:15]
- **Notes:** This is the “root input” for margin logic—if vendor cost is wrong, everything downstream (suggested price, approvals, disputes) becomes unreliable. Snapshot behavior is non-negotiable to avoid “why did my approved number change?” escalations.
- **Responsible:** TBD

## CUBE-D2-002
- **Group:** Pricing & Margin Engine
- **Category:** Calculation Engine
- **Epic:** Customer Pricing Calculation
- **Parent Task:** Suggested Rate Calculation
- **Task Name:** Apply 35 Percent Target Margin
- **User Story:** As an Account Manager (AM), I want the system to automatically calculate a suggested customer rate based on vendor costs and margin targets (35%), so that pricing is consistent, simplified, and aligned with profitability goals.
- **Description:** The system must aggregate all vendor-related charges (base cost, accessories, fuel, environmental fees, delivery, removal, taxes, service frequency adjustments, etc.), compute total vendor exposure, and apply a target margin (typically 35%) to generate a simplified customer-facing “standard rate.”
- **Timestamp:** Day 2, Part 2 [0:08 – 0:12:30]
- **Notes:** This is one of the heaviest calculation areas in the system. Must support different product logic (roll-offs vs toilets behave differently).
- **Responsible:** TBD

## CUBE-D2-003
- **Group:** Pricing & Margin Engine
- **Category:** Functional Logic
- **Epic:** Margin Governance & Approval Controls
- **Parent Task:** Low Margin Approval Process
- **Task Name:** Trigger and Route Low Margin Approvals
- **User Story:** As an Account Manager (AM), I want the system to automatically trigger approval workflows when margin falls below defined thresholds, so that pricing decisions remain controlled and financially compliant.
- **Description:** When the calculated margin on a quote or service falls below predefined thresholds, the system must automatically restrict progression and initiate an approval workflow. Margin thresholds are tiered. Depending on how low the margin is (e.g., below target %, below minimum %, or negative margin), different approval levels are required (e.g., CSS approval vs CSM approval vs higher management approval).
- **Timestamp:** Day 2, Part 2 [0:13:40 – 0:17:30]
- **Notes:** Threshold values must be configurable (not hard-coded). Approval routing must support role-based escalation. Must integrate with notification system.
- **Responsible:** TBD
- **JT Notes:** "CSM" designation likely to change.

## CUBE-D2-004
- **Group:** Pricing & Margin Engine
- **Category:** Product Configuration Logic
- **Epic:** Product Pricing Variability
- **Parent Task:** Quantity & Per-Unit Handling
- **Task Name:** Handle Product-Specific Quantity and Per-Unit Logic
- **User Story:** As an Account Manager (AM), I want product pricing to behave differently depending on product type and quantity rules, so that calculations reflect real-world vendor billing structures.
- **Description:** Different product lines have different quantity and billing behaviors. For example: Toilets and storage containers can use a quantity field (e.g., quantity = 5 identical units). Roll-offs must always be treated as individual product records (quantity fixed to 1), because service events, removals, and fills vary independently.
- **Timestamp:** Day 2, Part 2 [0:00:08 – 0:06:30]
- **Notes:** Supports data-driven vendor selection.
- **Responsible:** TBD

## CUBE-D2-005
- **Group:** Pricing & Margin Engine
- **Category:** Functional Logic
- **Epic:** Post-Quote Adjustment
- **Parent Task:** Vendor Cost Change
- **Task Name:** Recalculate Margin After Vendor Update
- **User Story:** As an Account Manager (AM), I want margin and suggested customer rates to recalculate automatically when vendor costs change before approval, so that profitability and approval requirements remain accurate.
- **Description:** Before a quote/service is approved, vendor costs may be updated (e.g., hauler quote comes back higher/lower, fuel/environmental changes, delivery/removal adjustments). When those vendor values change, Cube must immediately recalculate: Suggested customer pricing, Total margin ($ and %), Whether the pricing now requires low-margin approval
- **Timestamp:** Day 2, Part 2 [0:15:35 – 0:16:45]
- **Notes:** This prevents the “looks profitable → gets approved → later we realize vendor cost changed” failure mode. It’s also the direct trigger for low-margin gating—if this recalculation isn’t instant/reliable, approvals become meaningless and pricing risk goes up fast.
- **Responsible:** TBD

## CUBE-D2-006
- **Group:** Pricing & Margin Engine
- **Category:** Role-Based Access Control (RBAC)
- **Epic:** Margin Governance & Approval Controls
- **Parent Task:** Approval Authorization Enforcement
- **Task Name:** Restrict Low-Margin Approval Actions by Role
- **User Story:** As a Customer Support Specialist (CSS), I want only authorized roles (CSS and Admin) to be able to approve low-margin quotes, so that pricing governance rules cannot be bypassed.
- **Description:** Only users with CSS (Customer Support Specialist) or Admin roles may execute approval actions.
- **Timestamp:** Day 2, Part 2 [0:14:30 – 0:17:30]
- **Notes:** Primary governance safeguard.
- **Responsible:** TBD
- **JT Notes:** "CSM" designation likely to change.

## CUBE-D2-007
- **Group:** Pricing & Margin Engine
- **Category:** Seasonal Pricing Logic
- **Epic:** Seasonal & Conditional Pricing Controls
- **Parent Task:** Winterization Fee Application
- **Task Name:** Automatically Apply Winter Service Fee
- **User Story:** As an Account Manager (AM), I want winter service fees to be automatically applied during cold months, so that seasonal operational costs are consistently captured in pricing.
- **Description:** Certain products (e.g., portable toilets) incur additional costs during cold months due to winterization requirements. When a service date falls within configured cold months (e.g., December, January, February, March), the system must: Automatically recognize the winter period, Display a reminder message, Apply a per-unit winter service fee (e.g., $9 per unit), Include this fee in total pricing and margin calculations
- **Timestamp:** Day 2, Part 2 [0:01:30 – 0:05:30]
- **Notes:** This is conditional pricing logic based on calendar rules.
- **Responsible:** TBD
- **JT Notes:** The rules are based on census data (ie lookup from zip code table) not calendar rules. Margin calculates should exclude winterization feess (both customer and hauler)

## CUBE-D2-008
- **Group:** Pricing & Margin Engine
- **Category:** Calculation Engine
- **Epic:** Revenue & Margin Aggregation
- **Parent Task:** Quantity-Based Total Calculation
- **Task Name:** Scale Revenue and Margin by Quantity
- **User Story:** As an Account Manager (AM), I want total revenue, vendor cost, and margin to scale automatically based on quantity, so that financial metrics accurately reflect the number of units sold.
- **Description:** When multiple identical units are quoted (e.g., 4 portable toilets), the system must multiply: Vendor base cost, Customer-facing rate, Event charges (if per-unit), Seasonal charges (if applicable) Totals shown in the pricing panel (e.g., Initial Customer Charge, Initial Hauler Charge, Total Rental Charge, Length of Project Revenue) must reflect the aggregated value of all units. Margin must be calculated using total revenue vs total vendor cost, not per-unit values.
- **Timestamp:** Day 2, Part 2 [0:00:45 – 0:04:30]
- **Notes:** Requires product-level configuration for per-unit vs flat charges. Must avoid double multiplication errors.
- **Responsible:** TBD

## CUBE-D2-009
- **Group:** Pricing & Margin Engine
- **Category:** Calculation Engine
- **Epic:** Component-Level Pricing Transparency
- **Parent Task:** Delivery & Removal Pricing Structure
- **Task Name:** Separate Delivery and Removal Fee Calculation
- **User Story:** As an Account Manager (AM), I want delivery and removal charges calculated and displayed separately from rental rates, so that profitability can be evaluated per pricing component.
- **Description:** Delivery and removal charges must be treated as independent pricing components, not bundled into the standard rental rate.
- **Timestamp:** Day 2, Part 2 [0:08:30 – 0:12:00]
- **Notes:** Improves transparency in cost structure.
- **Responsible:** TBD

## CUBE-D2-010
- **Group:** Site Management
- **Category:** Functional Logic
- **Epic:** Customer → Site Lifecycle
- **Parent Task:** Site Creation & Linking
- **Task Name:** Create Site Linked to Customer
- **User Story:** As an Account Manager (AM), I want to create a new Site under an existing Customer, so that services can be configured and managed at the correct location level.
- **Description:** In the customer hierarchy, Sites represent service locations where products and services are delivered and managed. The system must support creating a Site directly under a Customer and storing the Site’s core attributes (address/location details, site-level settings, ownership/audit metadata). Once created, the user should land on the Site record to continue operational setup.
- **Timestamp:** Day 2, Part 1 [0:24:36 – 0:26:10]
- **Notes:** walks the Site page and its fields, and explicitly highlights the audit metadata (created date, last updated, owner).
- **Responsible:** TBD

## CUBE-D2-011
- **Group:** Site Management
- **Category:** Data Integrity
- **Epic:** Site Address & Location Intelligence
- **Parent Task:** ZIP-Based Location Mapping
- **Task Name:** Auto-Populate Site Attributes from ZIP Code
- **User Story:** As an Account Manager (AM), I want ZIP code relationships to drive automatic population of location-related fields, so that site records are consistent and routing/assignment logic works correctly.
- **Description:** During Day 2 – Part 1, they discuss that ZIP code is not just a simple address field: it is connected to internal “relationships” used to derive other operational attributes (for example, mapping ZIP to service area / branch / internal routing fields).
- **Timestamp:** Day 2, Part 1 [0:09:40 – 0:12:10]
- **Notes:** The key requirement is the relationship mapping behavior: ZIP is used to derive other internal location attributes.
- **Responsible:** TBD

## CUBE-D2-012
- **Group:** Site Management
- **Category:** UI/UX Improvement
- **Epic:** Site Address Validation & Mapping
- **Parent Task:** Automated Address Mapping Enhancement
- **Task Name:** Enhance Automated Street View / Map Preview for Site Address
- **User Story:** As an Account Manager (AM), I want the service address to automatically display an accurate map/street preview, so that I can visually confirm the correct location before saving the Site.
- **Description:** An improvement related to the automated street view/map behavior when entering a service address. When a user enters or searches for a service address: - The system should automatically geocode the address. - A map preview should update dynamically. -The visual marker must accurately represent the validated address. This visual confirmation helps prevent incorrect site setup, routing issues, and delivery errors.
- **Timestamp:** Day 2, Part 1 [21:30 – 23:30]
- **Notes:** Prevents incorrect site creation due to mistyped or partially matched addresses.
- **Responsible:** TBD
- **JT Notes:** We will also neet street and terrain view as an improvement

## CUBE-D2-013
- **Group:** Site Management
- **Category:** Functional Logic
- **Epic:** Site-Level Operational Controls
- **Parent Task:** Site Processing Configuration
- **Task Name:** Configure Site-Level Processing & Operational Flags
- **User Story:** As an Account Manager (AM), I want to configure operational processing flags at the Site level, so that automation, billing behavior, and special site requirements are controlled per location.
- **Description:** These flags allow configuration of site-specific overrides that influence: -Credit card (CC) processing -Line item processing automation -Rental protection opt-in status -Site-specific language needs -Contact-level behaviors These settings must apply at the Site level and override customer-level defaults where applicable.
- **Timestamp:** Day 2, Part 1 [23:30 – 27:30]
- **Notes:** Prevents inflated profitability reporting.
- **Responsible:** TBD

## CUBE-D2-014
- **Group:** Site Management
- **Category:** Functional Logic
- **Epic:** Site-Level Service Lifecycle
- **Parent Task:** Service Creation Entry from Site
- **Task Name:** Enable “Add New Service” from Site Record
- **User Story:** As an Account Manager (AM), I want to initiate new services directly from a Site record, so that services are created in the correct site context without navigating elsewhere.
- **Description:** This section provides product-specific entry points, including: - Add Toilet - Add Roll-off - Add Container - Add Fencing - Add Other Service - Add Equipment Rental - Add Front Load - Add Permanent Roll-Off Additionally, users can access pricing flows through: - Single Page Pricing -Get Pricing
- **Timestamp:** Day 2, Part 1 [30:45 – 33:30]
- **Notes:** N/A
- **Responsible:** TBD
- **JT Notes:** This will be further clarified and defined in the UI Blocks (UI/UX display guidelines)

## CUBE-D2-015
- **Group:** Site Management
- **Category:** Document Management
- **Epic:** Site-Level Documentation Handling
- **Parent Task:** Site Document Upload & Storage
- **Task Name:** Upload Service Agreement & Placement Maps at Site Level
- **User Story:** As an Account Manager (AM), I want to upload service-related documents at the Site level, so that agreements and placement maps are stored in the correct operational context.
- **Description:** The UI shows dedicated upload controls for: - Service Agreement - Placement Maps These documents are tied to the Site, not just the Customer, ensuring that operational and contractual documentation remains location-specific.
- **Timestamp:** Day 2, Part 1 [34:40 – 36:30]
- **Notes:** This is location-specific documentation management, not general customer document storage.
- **Responsible:** TBD
- **JT Notes:** Prominent documents will be further clarified and defined in the UI Blocks (UI/UX display guidelines). The documents themselves would reside in/migrate to general document storage

## CUBE-D2-016
- **Group:** Site Management
- **Category:** Operational Tracking
- **Epic:** Site-Level Service Execution Tracking
- **Parent Task:** Service Ticket Visibility & Management
- **Task Name:** Display and Manage Service Tickets by Product Type
- **User Story:** As an Account Manager (AM), I want to view and manage service tickets at the Site level across different product categories, so that operational status, dispatch, billing, and invoicing can be tracked in one place.
- **Description:** The visible tabs include: - Accounting Inquiries - Storage Containers - Roll-Offs - Toilets - Front Load - Perm Roll-Off - Other Services - Equipment Rental - Line Items - Documents - Fulfillment Tickets - Tasks Each tab contains a grid of service tickets relevant to that category, displaying operational and financial information such as: - Service Dates - Service Ticket Status - Dispatch Status - Standard Charge Status - Related Invoice - Minimum Invoice – Date Created - Record Owner
- **Timestamp:** Day 2, Part 1 [34:50 – 38:30]
- **Notes:** This is a visibility and tracking feature
- **Responsible:** TBDD17C17:M17N17E17:M17B17:M17A17:M17N17E17:M17
- **JT Notes:** This will be further clarified and defined in the UI Blocks (UI/UX display guidelines); tabs would include both product lists and associated service tickets.

## CUBE-D2-017
- **Group:** Site Management
- **Category:** UI / UX
- **Epic:** Site-Level Service Ticket Management
- **Parent Task:** Service Ticket Navigation Interface
- **Task Name:** Service Ticket Navigation Tabs
- **User Story:** As an Account Manager (AM), I want to navigate service tickets using categorized tabs within the Site record, so that I can quickly locate operational, billing, and fulfillment information by service type.
- **Description:** In the Site module, the Service Tickets section uses a tabbed interface to organize operational records across multiple service categories. Each tab represents a specific operational dataset associated with the Site. Selecting a tab loads the corresponding ticket grid without leaving the Site context. - Observed tabs include: - Accounting Inquiries - Storage Containers - Roll-Offs - Toilets - Front Load - Perm Roll Off - Other Services - Equipment Rental - Line Items - Documents - Fulfillment Tickets - Tasks Each tab displays a grid of records relevant to that category, allowing users to review operational activity, billing status, dispatch information, or related documentation.
- **Timestamp:** Day 2, Part 1 [37:50 – 45:30]
- **Notes:** This story defines UI structure only.
- **Responsible:** TBD
- **JT Notes:** This will be further clarified and defined in the UI Blocks (UI/UX display guidelines); tabs would include both product lists and associated service tickets.

## CUBE-D2-018
- **Group:** Site Management
- **Category:** Audit / Governance
- **Epic:** System Audit & Traceability
- **Parent Task:** Record Change Tracking
- **Task Name:** Site Record Log
- **User Story:** As an Admin (Admin), I want the system to record logs of user actions with timestamps, so that changes to Site records and related data can be audited and traced
- **Description:** These logs provide visibility into system activity such as: - Record creation - Record updates - Status changes - Operational updates Each log entry records the user responsible for the action and the timestamp when it occurred, enabling traceability and accountability across the platform.
- **Timestamp:** Day 2 – Part 1: ~47:30 – 49:30
- **Mockups:** NO MOCKUP
- **Notes:** This is an auditability feature, not a UI feature.
- **Responsible:** TBD
- **JT Notes:** Global user story. Will need a UI component, and further definition.

## CUBE-D2-019
- **Group:** Site Management
- **Category:** UI/UX
- **Epic:** Task Visibility & Follow-Up Management
- **Parent Task:** Task Dashboard Experience
- **Task Name:** Display Query-Driven Follow-Up Tiles for Ams
- **User Story:** As an Account Manager (AM), I want a task dashboard with query-driven tiles for follow-ups, so that I can quickly see what actions I need to take across customers and product lines.
- **Description:** Each tile represents a category of follow-up work (for example, inactive customer check-ins, delivery follow-ups, no-sale follow-ups) and is segmented by product line (e.g., PT, RO, SC, FEN, OS). These tiles are powered by background queries that count records matching certain conditions. The purpose is to let AMs identify follow-up priorities immediately without manually filtering lists.
- **Timestamp:** Day 2, Part 1 [0:51:30 – 0:54:30]
- **Notes:** This is explicitly described as being driven by background queries, so implementation should support configurable query definitions rather than hardcoding each tile.
- **Responsible:** TBD
- **JT Notes:** Tasks/dashboards are not specific to AMs, although we will have specific task dashboards and/or dashboard components by role. Categories/queries are subject to change and current dashboard should not be used as a design template. Tasks are not always driven explicitly by background queries (although the dashboard shown specifically is). Tasks are not part of Phase 3.

## CUBE-D2-020
- **Group:** Sales Management
- **Category:** Operational Workflow
- **Epic:** Task Management & Follow-Up Tracking
- **Parent Task:** Task Lifecycle Management
- **Task Name:** Create and Edit Tasks for Customer and Site Follow-Ups
- **User Story:** As an Account Manager (AM), I want to create and update tasks related to customers and sites, so that operational follow-ups and account actions can be tracked and completed.
- **Description:** This form allows users to create tasks associated with a specific Customer, Site, and Employee, enabling structured follow-up tracking for operational or account-related actions.
- **Timestamp:** Day 2, Part 1 [0:56:00 – 1:00:00]
- **Notes:** Tasks appear in the Task Dashboard tiles previously described
- **Responsible:** TBD
- **JT Notes:** Global user story; tasks can currently be related to: Customer/Site/Product/Hauler/Fulfillment Ticker (may be expanded in future)

## CUBE-D2-021
- **Group:** Sales Management
- **Category:** Workflow Automation
- **Epic:** Customer Interaction & Call Assistance
- **Parent Task:** Phone Call Support Tools
- **Task Name:** Provide Real-Time Customer Context During Incoming Calls
- **User Story:** As an Account Manager (AM), I want the system to surface relevant customer information and contextual prompts during phone calls, so that I can quickly respond to service requests and provide accurate quotes.
- **Description:** The idea is to enhance the system’s ability to assist Account Managers when they are handling incoming customer phone calls. When a customer calls to request a quote or service, the system could leverage API integrations and contextual pop-ups to automatically surface relevant information such as: - Customer account details - Existing sites - Current services - Service history - Pricing or quoting tools
- **Timestamp:** Day 2, Part 1 [1:35:00 – 1:38:00]
- **Notes:** This story describes a future enhancement, not necessarily existing functionality.
- **Responsible:** TBD

## CUBE-D2-022
- **Group:** Pricing
- **Category:** Workflow Improvement
- **Epic:** Pricing Tool Usability Enhancements
- **Parent Task:** Pricing Configuration Assistance
- **Task Name:** Auto-Populate Pricing Inputs Using a Guided Questionnaire
- **User Story:** As an Account Manager (AM), I want the system to guide me through a questionnaire that automatically fills relevant pricing tool fields, so that I can generate quotes faster and with fewer errors.
- **Description:** Currently, users may need to manually fill several pricing-related fields when preparing quotes for services. This process can be time-consuming and may lead to inconsistent inputs if the user is unsure which parameters are required. To improve usability, the system could introduce a guided questionnaire that asks structured questions about the service being quoted. Based on the user’s responses, the system would automatically populate relevant pricing fields in the Pricing Tool.
- **Timestamp:** Day 2, Part 1 [2:11:00 – 2:15:00]
- **Notes:** This is an enhancement to improve pricing workflow efficiency, not a replacement for the existing pricing interface.
- **Responsible:** TBD

## CUBE-D2-023
- **Group:** Sales Management
- **Category:** User Management / Operational Continuity
- **Epic:** Account Ownership Management
- **Parent Task:** Temporary Ownership Reassignment
- **Task Name:** Allow Temporary Reassignment of Customers and Service Tickets
- **User Story:** As a Sales Manager or System Administrator, I want to temporarily reassign customers, service tickets, and related records to another employee, so that service operations continue uninterrupted when an Account Manager is unavailable.
- **Description:** In these cases, another employee must be able to temporarily manage that employee’s customers, service tickets, and operational responsibilities. Currently, ownership fields such as Record Owner, Customer Owner, or Account Manager determine who is responsible for managing service requests and follow-ups. The system should support a temporary reassignment mechanism that allows another employee to take over responsibility for records during a defined period.
- **Timestamp:** Day 2, Part 1 [2:45:00 – 2:48:00]
- **Mockups:** NO MOCKUP
- **Notes:** This feature supports business continuity during employee absence.
- **Responsible:** TBD

## CUBE-D2-024
- **Group:** Sales Management
- **Category:** Sale Management
- **Epic:** Sale Lifecycle Management
- **Parent Task:** Sale Record Status Management
- **Task Name:** Allow Users to Set the Status of a Sale
- **User Story:** As a user managing a sale record, I want to select the appropriate status of the sale, so that the system reflects the current stage of the sales process.
- **Description:** The system provides a dropdown field labeled Status, which allows the user to define the current state of a sale. The selected status reflects the outcome or progress of the sales opportunity. From the interface shown in the demonstration, the available status options include: - No Sale -Quote in Progress -Hauler Quote -Canceled -Sale
- **Timestamp:** Day 2, Part 1 [3:01:00 – 3:10:00]
- **Notes:** Status should be the same throughtout the different product lines in Quickbase
- **Responsible:** TBD

## CUBE-D2-025
- **Group:** Sales Management
- **Category:** Service Configuration
- **Epic:** Service Setup
- **Parent Task:** Product Selection
- **Task Name:** Select Product Type When Configuring a Service
- **User Story:** As a user creating or managing a service record, I want to select a product type from a list of available options, so that the correct service equipment or unit type is associated with the service.
- **Description:** When configuring a service, the user must select a Product Type from a dropdown list in the Service Information section. This list contains predefined product types associated with a specific category. The dropdown displays multiple entries including information such as: - Standard Charge Abbreviation - Parent Product and Category - Product Type
- **Timestamp:** Day 2, Part 1 [3:21:00 – 3:30:00]
- **Notes:** N/A
- **Responsible:** TBD
- **JT Notes:** We would want this selection cleaner and more user friendly; the documented fields do not need display, only [Product Type]

---

# Day 3

**Stories:** 28

## CUBE-D3-001
- **Group:** Core Platform
- **Category:** Pricing Governance
- **Epic:** Pricing Control Framework
- **Parent Task:** Margin Approval Configuration
- **Task Name:** Configure Pricing Approval Rules
- **User Story:** As a System Administrator, I want to configure pricing approval rules based on margin thresholds and order conditions so that quotes requiring oversight trigger the appropriate approvals before a sale is finalized.
- **Description:** The system determines whether pricing approvals are required by evaluating business rules that compare customer pricing with hauler costs. These rules define when approvals such as CSM Approval or Low Margin Approval must be triggered to ensure pricing governance and profitability control.
- **Timestamp:** Day 3, Part 1 [0:10:00 – 0:14:00]
- **Notes:** This story is derived from the discussion explaining the core ZTERS business model, where profitability comes from the margin between customer pricing and hauler pricing, and where configurable approval rules determine when pricing requires oversight.
- **Responsible:** TBD

## CUBE-D3-002
- **Group:** Core Platform
- **Category:** Workflow Validation
- **Epic:** Sales Status Management
- **Parent Task:** Sale Status Validation Rules
- **Task Name:** Enforce Required Fields When Status Changes to Sale
- **User Story:** As an Account Manager (AM), I want the system to require specific pricing and service fields when a service status is marked as Sale, so that all necessary information is completed before the sale is finalized.
- **Description:** When a service record transitions from a quote or estimate to Sale status, the system validates that required pricing and service configuration fields are completed. These validations ensure that operational and financial data is properly recorded before the service proceeds to fulfillment. Required inputs may include delivery pricing, removal pricing, rental protection decisions, and other pricing attributes necessary for order execution.
- **Timestamp:** Day 3, Part 1 [0:15:00 – 0:22:00]
- **Notes:** This requirement is discussed when explaining how converting a quote into a Sale triggers validation rules requiring completion of pricing and service configuration fields before the order can proceed.
- **Responsible:** TBD

## CUBE-D3-003
- **Group:** Core Platform
- **Category:** Vendor Management
- **Epic:** Hauler Assignment
- **Parent Task:** Vendor Selection Validation
- **Task Name:** Select Eligible Haulers for Service Fulfillment
- **User Story:** As an Account Manager (AM), I want the system to display vendor eligibility when selecting a hauler, so that I can assign services only to approved vendors.
- **Description:** When configuring a service in the Toilets module, users must select a hauler responsible for service fulfillment. The system provides a searchable vendor list containing thousands of vendors and displays eligibility indicators that inform users whether a vendor can be used.
- **Timestamp:** Day 3, Part 1 [0:26:00 – 0:28:00]
- **Notes:** During the Toilets module walkthrough, Justin explains how vendor selection includes an eligibility indicator (“Can we use them?”) to help users avoid assigning services to vendors that are not approved or usable
- **Responsible:** TBD

## CUBE-D3-004
- **Group:** Core Platform
- **Category:** Workflow Validation
- **Epic:** Operational Readiness Checks
- **Parent Task:** Service Ticket Prerequisite Validation
- **Task Name:** Validate Required Conditions Before Creating Service Tickets
- **User Story:** As an Account Manager (AM), I want the system to validate required operational and billing conditions before allowing service tickets to be created, so that services are not dispatched with incomplete information.
- **Description:** service Tickets represent customer service requests related to a product or service, while Fulfillment Tickets represent the operational actions required to complete those requests. Currently, these tickets may be located in separate sections of the inter
- **Timestamp:** Day 3, Part 1 [0:29:00 – 0:35:00]
- **Notes:** During the Toilets module walkthrough, Justin explains that service tickets cannot be created until required billing, pricing, and operational fields are completed, which are surfaced in the Error validation section of the record.
- **Responsible:** TBD
- **JT Notes:** To be better defined in UI blocks and the provided list is non-exhaustive, but conceptually correct.

## CUBE-D3-005
- **Group:** Core Platform
- **Category:** Workflow Architecture
- **Epic:** Fulfillment Workflow Refactor
- **Parent Task:** Move Dispatch Logic to Fulfillment Layer
- **Task Name:** Relocate Dispatching from Product Records to Fulfillment Module
- **User Story:** As an Account Manager (AM), I want dispatching actions to occur at the Fulfillment level instead of the product level, so that service execution is managed through a centralized fulfillment workflow rather than individual product records.
- **Description:** Currently, dispatch-related fields and actions are located within individual product pages (such as the Toilets module). This approach couples operational dispatching with product configuration. The system should move dispatch operations to the Fulfillment layer, where dispatch scheduling and service execution can be managed consistently across all product types
- **Timestamp:** Day 3, Part 1 [0:32:00 – 0:35:00]
- **Notes:** During the workshop discussion, it is proposed that dispatching should no longer exist within product-level pages and instead be handled at the Fulfillment level, separating service execution from product configuration.
- **Responsible:** TBD

## CUBE-D3-006
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** Fulfillment Ticket Workflow
- **Parent Task:** Ticket Type Driven Fulfillment Forms
- **Task Name:** Adapt Fulfillment Ticket Fields Based on Ticket Type
- **User Story:** As an Account Manager (AM), I want the fulfillment ticket form to adjust its fields based on the selected ticket type, so that I can capture the correct operational information for each type of request.
- **Description:** The Fulfillment Ticket module allows users to create operational requests related to service delivery, maintenance, removal, scheduling, or information requests. When creating a fulfillment ticket, users select a Ticket Type that defines the nature of the request. Based on the selected ticket type, the system dynamically displays the relevant fields required to process that request. This ensures that users provide the correct operational details depending on the type of fulfillment action being performed.
- **Timestamp:** Day 3, Part 1 [0:36:00 – 0:40:00]
- **Notes:** Fulfillment Tickets support multiple operational request types, and the system dynamically adjusts required fields depending on the selected Ticket Type
- **Responsible:** TBD

## CUBE-D3-007
- **Group:** Core Platform
- **Category:** Product Page
- **Epic:** Fulfillment Ticket Management
- **Parent Task:** Service Scheduling Configuration
- **Task Name:** Store Service Cycles and Scheduling Dates in Fulfillment Tickets
- **User Story:** As an Account Manager (AM), I want fulfillment tickets to store service cycles and scheduling dates, so that the system accurately reflects when services should occur and how frequently they repeat.
- **Description:** Fulfillment tickets store scheduling information required to execute services. This includes requested service dates, confirmed service dates, and cycle information that determines how frequently a service should occur. These fields allow the system to coordinate service fulfillment according to customer requirements.
- **Timestamp:** Day 3, Part 1 [0:35:00 – 0:42:00]
- **Notes:** tickets store service scheduling dates and cycle information to define when services occur and how frequently they repeat.
- **Responsible:** TBD
- **JT Notes:** These things are being conflated. While 1. and 2. are correct (these dates ARE entered on a fulfillment ticket), the PRODUCT stores all of the necessary cycle information and calculated dates, NOT the fulfillment ticket. The fulfillment ticket is for a single service only.

## CUBE-D3-008
- **Group:** Core Platform
- **Category:** Product Page
- **Epic:** Sales Workflow
- **Parent Task:** Terms of Service Confirmation
- **Task Name:** Trigger Terms of Service Reminder When Marking Sale
- **User Story:** As an Account Manager (AM), I want the Terms of Service to automatically appear as a reminder when I mark a service as Sale, so that I remember to read and confirm the terms with the customer before finalizing the order.
- **Description:** When Account Managers complete a sale during a customer call, they are expected to read the Terms of Service to the customer, especially when collecting payment information such as credit card details. Currently, the Terms of Service are available within a tab on the product page, but the system does not actively remind the Account Manager to review them during the sales process. To improve compliance and ensure the terms are communicated consistently, the system should automatically display the Terms of Service as a reminder when the service status is changed to Sale. This reminder would appear as a sidebar or pop-up within the product page.
- **Timestamp:** Day 3, Part 1 [0:43:00 – 0:45:00]
- **Notes:** Account Managers typically read the Terms of Service during the sales call, and suggests adding an automatic reminder when the service is marked as a Sale to ensure the terms are consistently communicated to customers.
- **Responsible:** TBD

## CUBE-D3-009
- **Group:** Core Platform
- **Category:** Billing Configuration
- **Epic:** Billing Preferences Management
- **Parent Task:** Hierarchical Billing Preferences
- **Task Name:** Support Billing Preferences at Customer, Site, and Product Levels
- **User Story:** As an Account Manager (AM), I want billing preferences to be configurable at the customer, site, and product levels, so that billing settings can be tailored to the specific operational context of each service.
- **Description:** Billing preferences determine how services are invoiced and charged within the Cube platform. Currently, billing preferences may be configured at a limited level, but operational scenarios often require more granular control. The system should allow billing preferences to be configured hierarchically at multiple levels, including customer, site, and product. Each level should support a list of available billing preferences as well as a default preference that is automatically applied when creating services.
- **Timestamp:** Day 3, Part 1 [0:47:00 – 0:50:00]
- **Notes:** Billing preferences in Cube should become more granular and hierarchical, allowing configuration and defaults to exist at the customer, site, and product levels.
- **Responsible:** TBD
- **JT Notes:** Subject to possibly change, with includion of customer/site contacts.

## CUBE-D3-010
- **Group:** Core Platform
- **Category:** UI / UX
- **Epic:** Ticket Management Visibility
- **Parent Task:** Link Service Tickets and Fulfillment Tickets
- **Task Name:** Display Matching Fulfillment Tickets Next to Service Tickets
- **User Story:** As an Account Manager (AM), I want the system interface to display Service Tickets and their corresponding Fulfillment Tickets side by side, so that I can easily identify the fulfillment actions associated with each service request.
- **Description:** Service Tickets represent customer service requests related to a product or service, while Fulfillment Tickets represent the operational actions required to complete those requests. Currently, these tickets may be located in separate sections of the interface, making it harder for users to quickly understand their relationship. To improve usability, the system should align Service Tickets and Fulfillment Tickets within the same interface context, allowing users to easily view the operational fulfillment record associated with a service ticket.
- **Timestamp:** Day 3, Part 1 [0:55:00 – 0:58:00]
- **Notes:** UI improvement where Service Tickets and Fulfillment Tickets should be visually aligned, allowing users to easily understand the relationship between a service request and its operational fulfillment record.
- **Responsible:** TBD

## CUBE-D3-011
- **Group:** Core Platform
- **Category:** ARQ
- **Epic:** Quote Generation Workflow
- **Parent Task:** ARQ Quote Creation Process
- **Task Name:** Trigger ARQ Quote Creation from Product Page
- **User Story:** As an Account Manager (AM), I want to progress a service from estimate to formal quote and then create the ARQ quote, so that I can generate an official quote for the customer once the required information is available.
- **Description:** During the sales process, Account Managers may initially provide a preliminary price estimate before all service details are known. As additional information becomes available, such as the full service address and finalized pricing details, the quote can progress to a formal stage. The system supports this workflow through the Estimate Given, Quote Given, and Ready for ARQ indicators. Once the service information is complete and marked as Ready for ARQ, the Account Manager can create the official quote in the ARQ system. Selecting Create Quote opens the ARQ quote interface where the quote record is generated and managed.
- **Timestamp:** Day 3, Part 1 [0:59:00 – 1:05:00]
- **Notes:** the Estimate Given, Quote Given, and Ready for ARQ fields represent stages of the quoting workflow, allowing Account Managers to transition from early pricing estimates to the creation of a formal quote within the ARQ system.
- **Responsible:** TBD
- **JT Notes:** We would want the requisites driven in a more automated fashion as an improvement.

## CUBE-D3-012
- **Group:** Core Platform
- **Category:** ARQ
- **Epic:** Quote Creation & Delivery (ARQ)
- **Parent Task:** Create Quote Flow
- **Task Name:** Create Quote and Deliver to Customer
- **User Story:** As an Account Manager (AM), I want to create a formal quote from a drafted quote and send it to the customer, so that the customer receives the complete pricing and service details in a standardized format.
- **Description:** In the ARQ workflow, once a quote is drafted and the AM has indicated the appropriate state (Quote Given vs Estimate Given) and the quote is Ready for ARQ, the AM can proceed to generate the formal quote view and send it to the customer (email/text). The quote should present key information (customer/site/services totals) and support selecting multiple services under one quote.
- **Timestamp:** Day 3, Part 1 [0:59:00 – 1:15:00]
- **Notes:** the “Quote Given / Estimate Given” flags are manual, and Ready for ARQ is the gate to being able to create/send the quote
- **Responsible:** TBD
- **JT Notes:** We would want the requisites driven in a more automated fashion as an improvement.

## CUBE-D3-013
- **Group:** Products
- **Category:** Product Page – Roll-Offs
- **Epic:** Roll-Off Service Configuration
- **Parent Task:** Roll-Off Quote Setup
- **Task Name:** Capture Service Information for Roll-Off Services
- **User Story:** As an Account Manager (AM), I want to enter service details in the Roll-Off Service Information section when creating a quote, so that the system captures the operational parameters of the roll-off service such as container type, debris type, service dates, and project duration.
- **Description:** Within the Roll-Offs module, the Service Information section allows Account Managers to configure the operational details of a roll-off service during the quoting process. This section includes fields related to the container category, product type, debris type, delivery/removal dates, project duration, and additional service attributes. These fields provide the necessary information for pricing, scheduling, and fulfillment planning when managing roll-off container services.
- **Timestamp:** Day 3, Part 1 [1:30:00 – 1:40:00]
- **Notes:** The Debris Type selection influences the service configuration and pricing inputs for roll-off quotes, as demonstrated in the workshop when navigating the Roll-Off Service Information section.
- **Responsible:** TBD

## CUBE-D3-014
- **Group:** Products
- **Category:** Product Page – Roll-Offs
- **Epic:** Roll-Off Service Configuration
- **Parent Task:** Roll-Off Quote Setup
- **Task Name:** Configure Debris Types and Disposal Pricing
- **User Story:** As an Account Manager (AM), I want to select the debris type for a roll-off service and configure the associated disposal pricing, so that the quote reflects the correct disposal costs based on the type of material being removed.
- **Description:** Within the Roll-Offs module, the Debris Type field allows the Account Manager to identify the type of material being disposed of (e.g., construction, roofing, concrete, trash, dirt, etc.). The selected debris type is used in conjunction with disposal pricing fields within the Customer Quote section, where the AM can specify: -Tons included -Disposal rate -Disposal type (e.g., per ton) These values determine how disposal costs are calculated as part of the overall service quote for roll-off containers.
- **Timestamp:** Day 3, Part 1 [1:30:00 – 1:40:00]
- **Notes:** The rebate scenario applies to materials where the disposed material has recoverable value, resulting in a credit or reimbursement to the customer rather than a disposal charge.
- **Responsible:** TBD

## CUBE-D3-015
- **Group:** Products
- **Category:** Product Page – Roll-Offs
- **Epic:** Roll-Off Service Configuration
- **Parent Task:** Roll-Off Quote Setup
- **Task Name:** Track Rental Duration Using Days Counter
- **User Story:** As an Account Manager (AM), I want the system to calculate roll-off rental pricing based on the number of rental days instead of recurring service cycles, so that pricing reflects how long the container remains at the customer’s site.
- **Description:** Unlike other ZTERS products (such as portable toilets) that may use service cycles, roll-off containers are rented for a number of days. The system must track rental duration using a Days Included counter within the Customer Quote section. The quote defines how many days are included in the base rental and the associated rental rate and interval. If the container remains on site beyond the included days, additional rental charges may apply based on the configured pricing rules. This structure ensures that roll-off services are priced according to duration of use rather than scheduled service cycles.
- **Timestamp:** Day 3, Part 1 [1:40:00 – 1:55:00]
- **Notes:** Roll-off services use a duration-based rental model, where pricing depends on the number of days the container is kept at the site rather than a recurring service cycle.
- **Responsible:** TBD

## CUBE-D3-016
- **Group:** Products
- **Category:** Product Page – Roll-Offs
- **Epic:** Vendor Pricing & Margin Management
- **Parent Task:** Roll-Off Quote Setup
- **Task Name:** Manage Vendor Rates and Margin Calculations
- **User Story:** As an Account Manager (AM), I want to view and configure vendor (hauler) rates within the Vendor Rates tab, so that the system can calculate margins and suggest appropriate customer pricing for the roll-off service.
- **Description:** Within the Roll-Off product page, the Vendor Rates tab allows the Account Manager to configure the pricing received from the hauler (vendor) that will perform the service. The system compares the vendor rates with the customer quote values and calculates the resulting margin and margin percentage. The system may also generate a suggested price, which the AM can optionally apply to the quote. This enables ZTERS to ensure that the difference between customer charge and hauler charge produces an acceptable margin before the service is confirmed. The Vendor Rates section includes fields related to hauler pricing components such as standard rate, delivery rate, rental rate, disposal rate, rental interval, and included tonnage.
- **Timestamp:** Day 3, Part 1 [1:40:00 – 1:50:00]
- **Notes:** The Vendor Rates tab supports ZTERS’s pricing model, where profitability depends on the difference between what the customer pays and what the hauler charges for the service.
- **Responsible:** TBD

## CUBE-D3-017
- **Group:** Products
- **Category:** Product Page – Containers
- **Epic:** Container Service Configuration
- **Parent Task:** Container Quote Setup
- **Task Name:** Capture Container Service Information
- **User Story:** As an Account Manager (AM), I want to configure service details for storage containers within the Containers module, so that container rentals can be properly quoted and tracked for customer projects.
- **Description:** Within the Containers module, the Service Information section allows the Account Manager to configure the operational details of a storage container rental. These fields capture information about the container type, quantity, accessories, delivery schedule, and project duration. This configuration defines how the container service will be delivered to the customer and determines the pricing structure applied in the Customer Quote section.
- **Timestamp:** Day 3, Part 1 [2:06:00 – 2:10:00]
- **Notes:** The Containers module is used for storage container rentals, which differ from waste containers (Roll-Offs) but follow a similar configuration structure within the product page.
- **Responsible:** TBD

## CUBE-D3-018
- **Group:** Products
- **Category:** Product Page – Fencing
- **Epic:** Fencing Service Configuration
- **Parent Task:** Fencing Quote Setup
- **Task Name:** Capture Fencing Dimensions, Accessories, and Service Cycles
- **User Story:** As an Account Manager (AM), I want to configure fencing service details including dimensions, accessories, and project cycles, so that the system can correctly calculate pricing and manage fencing installations that may change during the project.
- **Description:** Within the Fencing module, the Service Information section allows the Account Manager to configure the parameters required to quote and manage a fencing installation. Unlike simpler services, fencing installations involve dimensional inputs and operational adjustments over time. The system must capture length and height of the fence, which determine the total fencing required. Accessories such as sandbags, windscreens, barbed wire, or wheels may also be included depending on the installation requirements. Fencing services also operate on billing cycles and may involve partial removals during the project, meaning that portions of the installed fencing can be removed before the full project ends. These operational factors require additional calculations to determine service pricing and duration
- **Timestamp:** Day 3, Part 1 [2:10:00 – 2:15:00]
- **Notes:** Fencing services require dimension-based calculations and operational flexibility, since installations can change during the project through accessory additions or partial fence removals.
- **Responsible:** TBD

## CUBE-D3-019
- **Group:** Products
- **Category:** Product Page – Fencing
- **Epic:** Fencing Service Management
- **Parent Task:** Fencing Quote and Service Lifecycle
- **Task Name:** Track Follow-Up Activities for Fencing Services
- **User Story:** As an Account Manager (AM), I want the system to support follow-up tracking for fencing installations, so that I can verify the condition of the fencing and address potential damage or service issues during the project.
- **Description:** During the workshop discussion of the Fencing module, it was noted that fencing installations often require post-installation follow-up because fences can be damaged, moved, or modified while on site. As a result, Account Managers frequently need to check in with the customer after delivery to confirm the installation is still in good condition. The system should support the ability to track or initiate follow-up actions related to fencing services, allowing Account Managers to maintain service quality and address issues that may arise during the rental period.
- **Timestamp:** Day 3, Part 1 [2:18:00 – 2:22:00]
- **Notes:** Fencing installations often require follow-up because panels can be damaged, moved, or altered during the project, making periodic checks an important part of service management.
- **Responsible:** TBD

## CUBE-D3-020
- **Group:** Products
- **Category:** Product Page – Fencing
- **Epic:** Fencing Vendor Pricing
- **Parent Task:** Fencing Quote Setup
- **Task Name:** Improve Vendor Rate Calculations for Fencing Services
- **User Story:** As an Account Manager (AM), I want the system to automatically calculate fencing vendor costs based on installation parameters, so that I do not have to manually determine complex pricing inputs when creating fencing quotes.
- **Description:** Within the Fencing module, the Vendor and Rates section determines the vendor (hauler) cost structure used to calculate service pricing and margins. Unlike other products, fencing pricing involves multiple operational variables such as panel length, number of panels, installation labor, rental duration, and transportation costs. During the workshop discussion, it was noted that this section currently requires significant manual input and interpretation. Improvements are needed so the system can better support the calculation of fencing vendor pricing by using the service configuration (such as fence dimensions and project length) to derive pricing values.
- **Timestamp:** Day 3, Part 1 [2:30:00 – 2:35:00]
- **Notes:** Fencing services involve dimension-based pricing and installation logistics, making automated calculation of vendor rates critical to simplifying the quoting process for Account Managers.
- **Responsible:** TBD

## CUBE-D3-021
- **Group:** Products
- **Category:** Product Page – Front Loads
- **Epic:** Front Load Service Management
- **Parent Task:** Front Load Quote Setup
- **Task Name:** Integrate Front Load Pricing with External System
- **User Story:** As an Account Manager (AM), I want Cube to capture Front Load service information while relying on external pricing systems, so that Front Load services can be managed without requiring all pricing logic to be calculated directly in Cube.
- **Description:** Cube must still support the ability to record the Front Load service configuration and special pricing elements, including overage charges and contamination-related margins. These values influence the final pricing structure but are primarily determined by the external system. The Cube interface therefore acts as a record and coordination layer, allowing Account Managers to manage the service record while relying on the external system for detailed pricing calculations.
- **Timestamp:** Day 3, Part 1 [2:46:00 – 2:55:00]
- **Notes:** Front Load services rely on external pricing logic managed through CWS systems, with Cube serving primarily as the service management and record interface for Account Managers.
- **Responsible:** TBD
- **JT Notes:** No. There is no external pricing system. While the FEL product has more detailed margin calculations/combinations than others, it uses the samew inbuilt pricing mechanisms.

## CUBE-D3-022
- **Group:** Products
- **Category:** Product Page – Other Services
- **Epic:** Equipment Rental Service Management
- **Parent Task:** Equipment Rental Quote Setup
- **Task Name:** Configure Equipment Rental Service Information
- **User Story:** As an Account Manager (AM), I want to manage equipment rental services within the Equipment Rentals module, so that I can track delivery, rental cycles, and removal events for rented equipment.
- **Description:** The Equipment Rentals module allows Account Managers to create and manage service records for equipment rented to customers, such as telehandlers or other construction equipment. Within this module, the system must support the lifecycle of the equipment rental, including: - Equipment delivery to the job site - Rental cycle management during the project - Removal or pickup of the equipment once the rental period ends The module also stores the customer and site information associated with the rental, allowing Account Managers to manage equipment rentals similarly to other ZTERS services while accommodating the operational requirements specific to equipment.
- **Timestamp:** Day 3, Part 1 [2:50:00 – 2:56:00]
- **Notes:** Equipment rentals follow a delivery → rental cycle → removal lifecycle, similar to other rental-based services managed in Cube, but applied to construction equipment rather than containers or waste services.
- **Responsible:** TBD

## CUBE-D3-023
- **Group:** Products
- **Category:** Product Page – Equipment Rental
- **Epic:** Miscellaneous Service Management
- **Parent Task:** Other Services Quote Setup
- **Task Name:** Configure One-Time Service Operations
- **User Story:** As an Account Manager (AM), I want to create service records for miscellaneous operational services, so that services such as generator hookups, electrical work, or other job-site support tasks can be managed within Cube even if they do not belong to a standard product category.
- **Description:** The Other Services module is designed to support services that fall outside the primary ZTERS product offerings. These services are typically short-term operational tasks performed at the job site, such as generator hookups, electricians, or other temporary support services. Unlike recurring rental-based products, most services in this module are one-time services, commonly performed within a single day. While the system supports defining a service frequency, the expected use case is primarily one-time service execution. This module ensures that these operational services can still be tracked, quoted, and managed within Cube, even though they do not follow the operational patterns of the other product modules.
- **Timestamp:** Day 3, Part 1 [2:56:00 – 2:59:00]
- **Notes:** The Other Services module acts as a flexible category for operational services that do not fit into the standard ZTERS product offerings and are usually one-time, short-duration activities.
- **Responsible:** TBD
- **JT Notes:** Grease Traps are currently in this category, which is the only reason this section accepts cycles/etc. Once grease traps are logically separated, OS should revert to single services (eg no cycles/etc)

## CUBE-D3-024
- **Group:** Products
- **Category:** Product Page – Perm-Roll-Offs/Compactors
- **Epic:** Permanent Waste Service Management
- **Parent Task:** Permanent Roll-Off Quote Setup
- **Task Name:** Configure Permanent Roll-Off Services
- **User Story:** As an Account Manager (AM), I want to manage permanent roll-off and compactor services within Cube, so that long-term waste container services can be configured and tracked even though they do not follow the temporary project model used by standard roll-offs.
- **Description:** The Perm Roll-Off / Compactor module supports waste container services that remain permanently installed at the customer’s location, typically for ongoing commercial operations. During the workshop discussion, Justin explains that this module behaves as a combination of temporary roll-offs and recurring services. Like roll-offs, the service involves a waste container placed at the site. However, unlike temporary roll-offs, the container does not have a fixed project duration and is intended to remain at the site indefinitely.
- **Timestamp:** Day 3, Part 1 [3:00:00 – 3:10:00]
- **Notes:** Permanent roll-offs and compactors represent long-term waste management services, combining aspects of temporary roll-offs (container service) and recurring operational services (ongoing pickups and servicing).
- **Responsible:** TBD

## CUBE-D3-025
- **Group:** Core Platform
- **Category:** Product Page
- **Epic:** Service Lifecycle Tracking
- **Parent Task:** Product Follow-Up Monitoring
- **Task Name:** Track Automatic Pulls and Prescheduled Removals
- **User Story:** As an Account Manager (AM), I want to track products that require automatic pulls or prescheduled removals, so that I can proactively follow up on services that need operational action.
- **Description:** During the workshop discussion, Crystal mentioned the need for a way to monitor products that require follow-up actions, particularly services that will eventually need container pulls or scheduled removals. To support this workflow, the system should allow Account Managers to access reports or filters that identify services requiring these operational follow-ups. These reports help Account Managers maintain visibility into products that need attention and ensure that service removals or pulls are scheduled appropriately. - Automatic Pulls to Follow Up On - Prescheduled Removals and Automatic Follow-Up
- **Timestamp:** Day 3, Part 1 [3:30:00 – 3:37:00]
- **Notes:** This functionality helps Account Managers maintain visibility over services that require future operational actions, ensuring that product removals and pulls are properly managed.
- **Responsible:** TBD
- **JT Notes:** As an improvement, we would want to create automated notifications and/or tasks to track this

## CUBE-D3-026
- **Group:** Core Platform
- **Category:** Product Page
- **Epic:** Service Lifecycle Tracking
- **Parent Task:** Product Monitoring & Reporting
- **Task Name:** Customize Automatic Pull Follow-Up Reports
- **User Story:** As an Account Manager, I want to customize Automatic Pull follow-up reports, so that I can track upcoming container pulls based on my own preferred timing and workflow without affecting reports used by other users.
- **Description:** users can adjust report filters using the report builder, removing or modifying the 3-day threshold condition. Users can then save a personalized version of the report (e.g., tracking pulls 10 days in advance) without altering the default report used by others. The customized report can be: - Saved as a personal report - Visible only to the user - Stored under a personal report section - Generated using configurable filters such as: - Auto Pull Date threshold - Status -Removal conditions -Service dates This functionality allows users to adapt operational follow-up monitoring to their own workflows while preserving shared system reports.
- **Timestamp:** Day 3, Part 2 [0:04:00 – 0:07:00]
- **Notes:** The current Quickbase system distinguishes between temporary reports and saved personal reports, with temporary reports cached for a limited time before expiring.
- **Responsible:** TBD
- **JT Notes:** Personal reports and report modifications would be a system level story and not only applicable to this example.

## CUBE-D3-027
- **Group:** Core Platform
- **Category:** Financial Reporting / Product Page
- **Epic:** Financial Reporting Credit Card Charges
- **Parent Task:** Credit Card Decline Issue for Ams
- **Task Name:** Correct Invoice Reporting for Declined Credit Card Payments
- **User Story:** As an Account Manager, I want the monthly invoice report to correctly reflect credit card declines and successful payment dates, so that my monthly totals accurately represent the revenue that was actually collected.
- **Description:** When a credit card transaction declines, the invoice may later receive either: - a credit adjustment, or - a successful payment retry However, the reporting logic currently calculates totals using the invoice creation date, which causes incorrect monthly totals. This results in two issues: - Declined payments that receive credits create a negative value in reports, even though no payment was ever processed. - Payments that succeed later are attributed to the original invoice date rather than the payment date, causing the revenue to appear in the wrong month. The system should instead use the most recent successful transaction date to determine the correct reporting period and ensure that declined payments do not affect revenue totals.
- **Timestamp:** Day 3, Part 2 [0:08:00 – 0:11:00]
- **Notes:** This is an improvement
- **Responsible:** TBD

## CUBE-D3-028
- **Group:** Core Platform
- **Category:** Product Page / Site Page
- **Epic:** Site Intelligence & Planning
- **Parent Task:** Integrate Satellite View and Measurement Tools for Site Planning
- **Task Name:** Including a Measuring Tool into CUBE for site planning
- **User Story:** As an Account Manager, I want to view satellite imagery, street view, and measurement tools directly from the site page, so that I can evaluate site conditions and determine whether equipment such as dumpsters or fencing can be placed at the location without leaving the system.
- **Description:** Currently, users must open Google Maps separately, switch to satellite view, and use measurement tools to estimate distances such as driveway width or available placement area. Embedding these tools directly into the platform would streamline the workflow and reduce context switching. The system should allow users to: - View Street View of the service address - View Satellite imagery of the site - Use distance and area measurement tools - Inspect driveways, terrain, and site layout before scheduling equipment delivery This capability would support planning for several product types including: - Roll-off dumpsters - Fencing installations - Equipment rentals - Portable toilets The measurement functionality should be accessible from the Site Page, making it reusable across all products associated with the site.
- **Timestamp:** Day 3, Part 2 [0:20:00 – 0:24:00]
- **Mockups:** NOT PROVIDED
- **Notes:** This is an improvement
- **Responsible:** TBD

---

# Day 4

**Stories:** 30

## CUBE-D4-001
- **Group:** Reporting & Dashboard
- **Category:** Fulfillment Dashboard
- **Epic:** Fulfillment Operations Visibility
- **Parent Task:** Fulfillment Ticket Monitoring
- **Task Name:** Account Manager Fulfillment Dashboard
- **User Story:** As an Account Manager, I want to view a Fulfillment Dashboard displaying fulfillment tickets, ticket notes, delivery information, and operational status indicators, so that I can monitor fulfillment progress and quickly identify tickets that require attention.
- **Description:** The system should provide a Fulfillment Dashboard where Account Managers can review fulfillment tickets associated with their customers. The dashboard displays operational information such as ticket notes, delivery dates, customer and company names, assigned fulfillment representatives, and product types. The dashboard also includes visual status indicators summarizing ticket activity, such as the number of tickets created but not scheduled, tickets needing attention, assigned tickets, and fulfilled tickets. This allows Account Managers to quickly monitor fulfillment operations and detect potential issues.
- **Timestamp:** Day 4, Part 1 [0:07:41 – 0:12:00]
- **Notes:** Crystal demonstrates the Fulfillment Dashboard used by Account Managers to monitor fulfillment tickets and quickly identify operational issues requiring attention.
- **Responsible:** TBD

## CUBE-D4-002
- **Group:** Reporting & Dashboard
- **Category:** Task Dashboard
- **Epic:** Account Manager Operational Visibility
- **Parent Task:** Task Monitoring & Follow-Ups
- **Task Name:** Account Manager Task Dashboard
- **User Story:** As an Account Manager, I want to view a Task Dashboard summarizing operational tasks and follow-ups across different service categories, so that I can quickly identify pending tasks, service check-ins, delivery follow-ups, and other operational actions that require attention.
- **Description:** The system should provide a Task Dashboard for Account Managers displaying operational task indicators across different service categories such as Portable Toilets, Roll-Offs, Storage Containers, and Fencing. The dashboard displays visual counters highlighting tasks that require follow-up or action. These indicators help Account Managers monitor operational responsibilities such as inactive customer check-ins, delivery follow-ups, current service check-ins, removal follow-ups, and other service-related activities. Color-coded indicators allow users to quickly identify areas requiring attention.
- **Timestamp:** Day 4, Part 1 [0:10:00 – 0:14:00]
- **Notes:** Crystal demonstrates the Account Manager Task Dashboard, which summarizes operational follow-ups and service check-ins across multiple service categories to help AMs prioritize daily actions.
- **Responsible:** TBD

## CUBE-D4-003
- **Group:** Reporting & Dashboard
- **Category:** Task Dashboard
- **Epic:** Account Manager Operational Visibility
- **Parent Task:** Approval Monitoring
- **Task Name:** Pending Pricing Approvals Indicator
- **User Story:** I want to see a dashboard indicator showing quotes or pricing requests that are pending approval, so that I can follow up and prevent delays in completing customer quotes
- **Description:** The system should provide a dashboard indicator that highlights pricing or quote requests waiting for approval. This allows Account Managers to quickly identify when a quote requires leadership or margin approval before it can proceed. By surfacing pending approvals directly in the operational dashboards, Account Managers can proactively follow up with the appropriate approver and prevent quotes from remaining stalled in the system.
- **Timestamp:** Day 4, Part 1 [0:15:00 – 0:22:00]
- **Mockups:** NO MOCKUP PROVIDED
- **Notes:** Justin and Crystal discuss how quotes can sit waiting for approvals, highlighting the need for visibility so Account Managers know when approvals are pending and can follow up to avoid delays.
- **Responsible:** TBD

## CUBE-D4-004
- **Group:** Reporting & Dashboard
- **Category:** Billing & Payment Monitoring
- **Epic:** Billing Visibility
- **Parent Task:** Credit Card Payment Monitoring
- **Task Name:** Credit Card Decline Monitoring in CUBE
- **User Story:** As an Account Manager, I want to view and monitor credit card payment declines directly within CUBE, so that I can quickly identify unpaid invoices and follow up with customers without needing to access the HUB application.
- **Description:** Currently, credit card payment declines are managed through the HUB accounting interface, where users must navigate outside of CUBE to identify invoices that failed payment processing. This creates operational friction and delays when Account Managers need to follow up with customers regarding unpaid balances. The system should integrate credit card decline visibility into CUBE, allowing Account Managers to review invoices, payment status, customer details, and outstanding balances directly from the platform. This reduces the need to switch systems and improves response time for resolving failed payments.
- **Timestamp:** Day 4, Part 1 [0:24:00 – 0:28:00]
- **Notes:** Justin and Crystal explain that credit card declines are currently handled through the HUB accounting interface, but the workflow should be integrated into CUBE to allow Account Managers to track and follow up on failed payments more easily.
- **Responsible:** TBD

## CUBE-D4-005
- **Group:** Reporting & Dashboard
- **Category:** Billing & Payment Monitoring
- **Epic:** Billing Visibility
- **Parent Task:** Payment Notification Management
- **Task Name:** In-App Credit Card Payment Notifications
- **User Story:** As an Account Manager, I want to receive in-app notifications in CUBE when a credit card transaction succeeds or fails, so that I can monitor payment activity without relying on large volumes of email notifications.
- **Description:** Currently, payment transaction events such as credit card approvals or declines are communicated through email notifications, which can generate a high volume of messages and make it difficult for Account Managers to track important billing events. The system should provide in-app notifications within CUBE for payment transaction outcomes, allowing Account Managers to quickly see when payments are successful or declined without needing to monitor their email inbox.
- **Timestamp:** Day 4, Part 1 [0:31:00 – 0:34:00]
- **Notes:** Justin and Crystal discuss the issue of large volumes of email alerts for credit card transactions and suggest surfacing these notifications directly within CUBE to improve visibility and reduce email clutter.
- **Responsible:** TBD

## CUBE-D4-006
- **Group:** Reporting & Dashboard
- **Category:** Notification Center
- **Epic:** Operational Event Visibility
- **Parent Task:** In-App Notification Management
- **Task Name:** Account Manager Notification Widget
- **User Story:** As an Account Manager, I want a notification widget inside CUBE that aggregates important operational events, so that I can monitor system alerts without relying on large volumes of Quickbase email notifications.
- **Description:** Currently, many system events generate email notifications from Quickbase, which can result in a large number of messages and increase the risk of missing important operational information. Account Managers must often search through emails to identify relevant alerts related to their customers, services, or transactions. The system should provide a centralized in-app notification widget within CUBE where operational events are surfaced and organized. This allows Account Managers to review, manage, and prioritize notifications directly in the application instead of relying on external email alerts.
- **Timestamp:** Day 4, Part 1 [0:35:00 – 0:42:00]
- **Mockups:** NO MOCKUP PROVIDED
- **Notes:** Justin and Crystal discuss the issue of Quickbase sending excessive email notifications, which can cause users to miss important information. They mention the need for in-application notification visibility instead of relying on email alerts.
- **Responsible:** TBD

## CUBE-D4-007
- **Group:** Core Platform
- **Category:** Customer & Site Management
- **Epic:** Account Manager Workspace Improvements
- **Parent Task:** Customer and Site Navigation
- **Task Name:** Account Manager Customer and Site Search Bar
- **User Story:** As an Account Manager, I want functional search bars to quickly find customers and sites from the Account Manager home page, so that I can navigate directly to the correct customer or site record without browsing through multiple tables.
- **Description:** Account Managers frequently need to access customer and site records while managing quotes, services, and billing activities. Navigating through tables to locate specific records can slow down workflows and make it difficult to quickly retrieve the correct information. The system should provide search bars within the Account Manager home interface that allow users to search for customers and sites directly. This enables faster navigation to relevant records and improves overall usability for daily operations.
- **Timestamp:** Day 4, Part 1 [0:43:00 – 0:46:00]
- **Notes:** Crystal explains that Account Managers want direct search functionality for customers and sites from the AM workspace to quickly locate records without navigating through multiple Quickbase tables.
- **Responsible:** TBD
- **JT Notes:** Global search bar should have a definable context.

## CUBE-D4-008
- **Group:** Core Platform
- **Category:** Customer & Site Management
- **Epic:** Account Manager Workspace Improvements
- **Parent Task:** Portal Request Visibility
- **Task Name:** Open Quote and Service Requests from Customer Portal
- **User Story:** As an Account Manager, I want to see open quote requests and service requests submitted through the customer portal directly within my CUBE workspace, so that I can quickly identify and respond to customer requests without needing to access the portal separately.
- **Description:** Customers can submit quote requests and service requests through the ZTERS customer portal, which is a separate application from CUBE. Account Managers need visibility into these requests so they can respond quickly and manage customer needs efficiently. The system should display open quote requests and open service requests from the portal within the Account Manager home interface, directly below the customer and site search bars. This allows Account Managers to immediately see pending customer requests when accessing their workspace.
- **Timestamp:** Day 4, Part 1 [0:45:00 – 0:49:00]
- **Notes:** Justin and Crystal explain that quote requests and service requests submitted through the customer portal should be visible in the Account Manager workspace, allowing AMs to monitor customer activity without navigating to the separate portal application.
- **Responsible:** TBD
- **JT Notes:** These will need to be merged into the products/;service tickets and have new delineators and notifications created (they are currently separate tables)

## CUBE-D4-009
- **Group:** Core Platform
- **Category:** Workflow Automation
- **Epic:** Customer Portal Integration
- **Parent Task:** Portal Request Automation
- **Task Name:** Automatic Creation of Portal Requests in CUBE
- **User Story:** As an Account Manager, I want customer quote requests and service requests submitted through the portal to automatically create records in CUBE, so that I can immediately see and act on customer requests without manually transferring information from the portal.
- **Description:** Customers can submit quote requests and service requests through the ZTERS customer portal, which currently exists as a separate system from CUBE. Account Managers must monitor these requests and ensure they are properly handled within their operational workflow. To improve efficiency, the system should automatically create the corresponding request records in CUBE whenever a request is submitted through the portal. This ensures that portal activity is immediately visible within the Account Manager workspace and can be managed through CUBE dashboards and reports.
- **Timestamp:** Day 4, Part 1 [0:49:00 – 0:52:00]
- **Mockups:** NO MOCKUP PROVIDED
- **Notes:** Justin explains that requests submitted through the customer portal should automatically create records in CUBE, ensuring that Account Managers can immediately see and manage customer requests without manual intervention.
- **Responsible:** TBD
- **JT Notes:** These will need to be merged into the products/;service tickets and have new delineators and notifications created (they are currently separate tables)

## CUBE-D4-010
- **Group:** Core Platform
- **Category:** Quote Request Automation
- **Epic:** Quote Management Workflow
- **Parent Task:** Quote Request Processing Automation
- **Task Name:** Automated Processing and Routing of Quote Requests
- **User Story:** As an Account Manager, I want quote requests to automatically trigger internal workflows in CUBE once they are submitted, so that requests are processed faster and do not rely on manual tracking or follow-up.
- **Description:** When a quote request is created, it typically contains customer information, site details, requested products, delivery timelines, and debris or service requirements. Account Managers currently need to manually review these requests and initiate the quoting process. To streamline operations, CUBE should support automation around quote requests, allowing the system to automatically process incoming requests and prepare them for quoting workflows. This includes organizing the request data, identifying the services required (e.g., roll-offs, toilets, fencing), and ensuring the request enters the correct operational process within the system.
- **Timestamp:** Day 4, Part 1 [0:52:00 – 1:00:00]
- **Notes:** During this section of the workshop they discuss how quote request data (customer info, site info, services needed, debris type, etc.) should automatically drive the internal quoting workflow rather than requiring manual coordination.
- **Responsible:** TBD

## CUBE-D4-011
- **Group:** Core Platform
- **Category:** Notifications
- **Epic:** Notification Management
- **Parent Task:** Priority-Based Notification System
- **Task Name:** High Priority Flag for Critical Notifications
- **User Story:** As an Account Manager, I want certain notifications to be automatically flagged as high priority based on the event type, so that I can immediately identify and act on the most critical issues affecting my customers or transactions.
- **Description:** Account Managers receive many system notifications related to customer accounts, service operations, transactions, and internal workflows. Without prioritization, important events can easily be overlooked among routine notifications. The notification system in CUBE should support priority-based classification, where certain event types automatically trigger high priority alerts. These priority indicators help Account Managers quickly identify situations requiring immediate attention, such as operational issues, financial problems, or urgent customer-related events.
- **Timestamp:** Day 4, Part 1 [1:07:00 – 1:10:00]
- **Mockups:** NO MOCKUP PROVIDED
- **Notes:** The team discusses improving the notification system so that important events are automatically flagged as high priority, helping Account Managers quickly focus on urgent issues.
- **Responsible:** TBD

## CUBE-D4-012
- **Group:** Core Platform
- **Category:** Customer Lookup
- **Epic:** Account Manager Productivity Tools
- **Parent Task:** Caller Identification Tools
- **Task Name:** Caller ID Customer Lookup Tool in CUBE
- **User Story:** As an Account Manager, I want to quickly search for a customer using their phone number when they call, so that I can immediately identify the customer account and access relevant information without leaving CUBE.
- **Description:** Account Managers frequently receive calls from customers requesting service information, pricing assistance, billing clarification, or operational support. In the current workflow, tools such as Caller Search / Caller ID lookup exist in HUB, allowing users to search for a customer using a phone number. To streamline operations and reduce system switching, CUBE should provide a built-in caller lookup capability that allows Account Managers to search for customers by phone number directly within the platform. This tool should retrieve the associated customer account and allow quick access to relevant customer data, improving response time during live customer interactions.
- **Timestamp:** Day 4, Part 1 [1:29:00 – 1:33:00]
- **Notes:** The team discusses how HUB currently includes a caller lookup tool and suggests that similar functionality should be available directly within CUBE to improve efficiency when responding to customer phone calls.
- **Responsible:** TBD

## CUBE-D4-013
- **Group:** Reporting & Dashboard
- **Category:** Billing Monitoring
- **Epic:** Account Manager Financial Visibility
- **Parent Task:** Billing Preference Monitoring
- **Task Name:** Inactive Billing Preferences Needing Attention Dashboard
- **User Story:** As an Account Manager, I want a dashboard showing customers with inactive billing preferences but active or pending products, so that I can quickly identify and resolve billing issues before invoices fail or payments are missed.
- **Description:** Customers may have active or pending services while their billing preferences are inactive or improperly configured, which can prevent invoices from being successfully processed. Without clear visibility into these situations, Account Managers may only discover the issue after billing failures occur. CUBE should provide a dashboard or report highlighting accounts with inactive billing preferences that still have active or pending services. This dashboard allows Account Managers to proactively identify billing configuration issues and correct them before they impact revenue or customer operations.
- **Timestamp:** Day 4, Part 1 [1:36:00 – 1:40:00]
- **Notes:** The team discusses a dashboard that identifies customers with inactive billing preferences while still having active or pending products, allowing AMs to proactively resolve billing configuration problems.
- **Responsible:** TBD

## CUBE-D4-014
- **Group:** Reporting & Dashboard
- **Category:** Sales Performance Dashboard
- **Epic:** Account Manager Performance Visibility
- **Parent Task:** Invoice Revenue Reporting
- **Task Name:** Total Invoices by Month Dashboard
- **User Story:** As an Account Manager, I want a dashboard showing my total invoiced revenue by month, so that I can easily track my sales performance and revenue trends over time.
- **Description:** Account Managers need visibility into their monthly invoicing performance to understand revenue trends, evaluate account growth, and monitor their sales activity over time. Currently, this information can exist across multiple reports or systems, making it harder to quickly assess performance. CUBE should provide a Total Invoices by Month dashboard that aggregates invoice totals by month for each Account Manager. This dashboard enables users to quickly review their historical invoiced revenue and identify patterns in their sales activity.
- **Timestamp:** Day 4, Part 1 [1:40:35 – 1:44:00]
- **Notes:** The team discusses a report that shows total invoiced revenue per month for each Account Manager, allowing AMs to track their sales performance over time.
- **Responsible:** TBD

## CUBE-D4-015
- **Group:** Reporting & Dashboard
- **Category:** Sales Performance Dashboard
- **Epic:** Account Manager Performance Visibility
- **Parent Task:** Comparative Revenue Reporting
- **Task Name:** Account Manager Invoice Revenue Scoreboard
- **User Story:** As an Account Manager, I want to view a scoreboard comparing invoice revenue across all Account Managers, so that I can benchmark my performance against my peers and understand relative sales performance.
- **Description:** Account Managers track their own monthly revenue through invoice reports, but they may also want visibility into how their performance compares to other Account Managers. This type of comparative reporting helps users understand their position relative to peers and encourages performance improvement. CUBE should provide a scoreboard-style report that aggregates invoice totals for each Account Manager and displays them side by side. This report can be accessed through the existing invoice dashboards and allows users to compare monthly totals and overall performance across the team.
- **Timestamp:** Day 4, Part 1 [1:42:00 – 1:45:00]
- **Notes:** The team discusses a scoreboard-style invoice report that allows Account Managers to compare their invoiced revenue with other AMs, functioning as a performance benchmark.
- **Responsible:** TBD

## CUBE-D4-016
- **Group:** Reporting & Dashboard
- **Category:** Customer Portal Management
- **Epic:** Customer Portal Integration
- **Parent Task:** Portal Access Management
- **Task Name:** Customer Web Portal Access Dashboard
- **User Story:** As an Account Manager, I want a centralized dashboard for accessing customer and vendor web portals, so that I can quickly submit invoices, track payments, or access work order systems without searching through external spreadsheets.
- **Description:** Account Managers frequently need to access customer or vendor web portals to submit invoices, track payments, upload documents, or manage work orders. Currently, these portal links are stored in a shared spreadsheet, requiring users to manually search through rows of links to find the correct portal. This process is inefficient and difficult to maintain. CUBE should provide a Customer Web Portal dashboard that centralizes portal access and organizes portal links in a structured interface. This allows Account Managers to quickly access the appropriate portal for a customer or vendor directly from the system without relying on external spreadsheets.
- **Timestamp:** Day 4, Part 1 [1:46:28 – 1:50:00]
- **Notes:** The team explains that the current Customer Web Portal dashboard simply redirects users to a spreadsheet containing portal links, which they consider inefficient and want to replace with a proper in-system portal directory.
- **Responsible:** TBD

## CUBE-D4-017
- **Group:** Reporting & Dashboard
- **Category:** Customer Contact Management
- **Epic:** Customer Operational Information
- **Parent Task:** After-Hours Contact Directory
- **Task Name:** After-Hours Client Contact Dashboard
- **User Story:** As an Account Manager, I want a centralized dashboard containing after-hours customer contact information, so that I can quickly reach the correct customer contact during urgent operational situations without searching through external spreadsheets.
- **Description:** Account Managers sometimes need to contact customers outside of normal business hours for urgent operational matters such as service issues, delivery coordination, or problem resolution. Currently, the contact information for these customers is stored in a shared spreadsheet known as the After Hours Client List. This spreadsheet contains customer names, account managers, phone numbers, contact titles, and additional operational notes. However, relying on spreadsheets makes the information harder to search and maintain. CUBE should provide an After-Hours Client Contact dashboard that centralizes this information in a structured interface so Account Managers can quickly locate the appropriate contact during urgent situations.
- **Timestamp:** Day 4, Part 1 [1:48:00 – 1:52:00]
- **Notes:** The team explains that the After Hours Client List is currently maintained as a spreadsheet, and they want this information to be accessible through a structured dashboard within CUBE.
- **Responsible:** TBD
- **JT Notes:** This will be merged with Customer/Site contacts initiative

## CUBE-D4-018
- **Group:** Reporting & Dashboard
- **Category:** Sales Performance Dashboard
- **Epic:** Account Manager Performance Visibility
- **Parent Task:** Personal Sales Metrics Dashboard
- **Task Name:** My Sales Performance Dashboard
- **User Story:** As an Account Manager, I want a personal sales performance dashboard that shows key metrics about my accounts and sales activity, so that I can monitor my performance, track revenue trends, and understand how my work activity relates to sales outcomes.
- **Description:** Account Managers need a consolidated view of their sales performance to understand how their activities translate into revenue and customer growth. The My Sales Performance dashboard provides visibility into several important indicators such as invoiced revenue trends, calls handled, customer conversion rates, and new customer revenue. This dashboard allows Account Managers to monitor performance over time and better understand the relationship between operational activity and financial results. By centralizing these metrics in one place, CUBE helps users track their productivity and evaluate how their efforts contribute to revenue generation and customer acquisition.
- **Timestamp:** Day 4, Part 1 [1:50:55 – 1:55:00]
- **Notes:** The team reviews the My Sales Performance dashboard, which combines several metrics such as invoiced revenue, calls handled, close rates, and new customer revenue to help Account Managers monitor their personal performance.
- **Responsible:** TBD

## CUBE-D4-019
- **Group:** Reporting & Dashboard
- **Category:** Sales Performance Dashboard
- **Epic:** Account Manager Performance Visibility
- **Parent Task:** Sales Success Monitoring
- **Task Name:** Success Meter Dashboard (Current Month and Last Month)
- **User Story:** As an Account Manager, I want a Success Meter dashboard showing my performance metrics for the current month and the previous month, so that I can monitor my sales activity, evaluate my close rate performance, and understand how much effort is needed to improve results.
- **Description:** Account Managers need visibility into their sales effectiveness and activity levels, particularly how many calls or interactions are required to generate new customers and maintain existing accounts. The Success Meter dashboard provides performance indicators that help AMs understand their progress toward sales goals. The dashboard includes metrics such as new and returning customer sites, call activity, and gauges indicating the number of calls needed to achieve specific close rate improvements. Providing views for both the current month and the previous month allows Account Managers to compare performance over time and evaluate trends in their sales activity.
- **Timestamp:** Day 4, Part 1 [1:54:05 – 1:57:00]
- **Notes:** The team reviews the Success Meter dashboards, which display sales performance indicators such as calls made, new customers, and close rate metrics for both the current month and the previous month.
- **Responsible:** TBD

## CUBE-D4-020
- **Group:** Reporting & Dashboard
- **Category:** Sales Performance Dashboard
- **Epic:** Account Manager Performance Visibility
- **Parent Task:** Year-over-Year Sales Reporting
- **Task Name:** Year-over-Year Sales Dashboard for Account Managers
- **User Story:** As an Account Manager, I want a dashboard that shows my new customers and site growth year over year, so that I can analyze long-term performance trends and understand how my sales activity compares across different years.
- **Description:** Account Managers need visibility into how their customer acquisition and site growth evolve over time. Short-term metrics such as monthly performance are useful, but long-term trends help users understand seasonal patterns, growth trajectories, and the effectiveness of their sales efforts across multiple years. The YoY Sales Account Manager dashboard provides visual charts showing new customers and new sites by month across multiple years. This allows Account Managers to compare performance year over year and identify patterns in customer acquisition and business growth.
- **Timestamp:** Day 4, Part 1 [1:56:00 – 1:59:00]
- **Notes:** The team reviews a Year-over-Year sales dashboard that visualizes monthly customer and site growth across multiple years to help Account Managers understand long-term sales trends.
- **Responsible:** TBD

## CUBE-D4-021
- **Group:** Reporting & Dashboard
- **Category:** Customer Feedback Dashboard
- **Epic:** Customer Experience Monitoring
- **Parent Task:** Customer Review Tracking
- **Task Name:** Account Manager Customer Reviews Dashboard
- **User Story:** As an Account Manager, I want a dashboard showing customer reviews and ratings related to my accounts, so that I can monitor customer satisfaction, identify issues, and recognize positive feedback about service delivery.
- **Description:** Customer feedback provides important insight into service quality and customer satisfaction. Account Managers need visibility into how customers rate their experience with services such as delivery, product quality, and overall service performance. The Reviews dashboard for Account Managers aggregates customer review data and displays both summary metrics and detailed feedback. This includes average ratings for categories such as customer service, delivery/product experience, and product removal/service. It also provides access to individual customer comments and ratings, allowing Account Managers to review feedback and respond to service quality trends.
- **Timestamp:** Day 4, Part 1 [1:58:22 – 2:00:00]
- **Notes:** The team reviews a customer review dashboard that aggregates feedback and ratings for Account Managers, providing visibility into service quality and customer satisfaction.
- **Responsible:** TBD

## CUBE-D4-022
- **Group:** Reporting & Dashboard
- **Category:** Vendor Management
- **Epic:** Vendor Support Workflow
- **Parent Task:** Vendor Management Request Submission
- **Task Name:** Submit Vendor Management Request Form
- **User Story:** As an Account Manager, I want a form in CUBE to submit Vendor Management requests, so that I can report vendor-related issues and request support from the Vendor Management team without leaving the system.
- **Description:** Account Managers sometimes encounter situations that require assistance from the Vendor Management team, such as vendor issues, purchasing inquiries, accounting questions, or onboarding new haulers. Currently, these requests may be handled through informal channels or external communication, which can make tracking and resolution more difficult. CUBE should provide a Vendor Management Request submission form that allows Account Managers to create and track requests directly within the platform. The form should allow users to categorize the request, assign a priority level, provide detailed information about the issue, and attach supporting documentation when necessary.
- **Timestamp:** Day 4, Part 1 [2:01:07 – 2:04:00]
- **Notes:** The team discusses a Vendor Management request form used by Account Managers to submit issues or inquiries related to vendors, purchasing, or accounting, enabling structured tracking and resolution of vendor-related requests.
- **Responsible:** TBD

## CUBE-D4-023
- **Group:** Employee Engagement
- **Category:** Recognition Program
- **Epic:** Employee & Vendor Recognition
- **Parent Task:** Nomination Submission
- **Task Name:** Nominate Employee or Vendor of the Month
- **User Story:** As an Account Manager (AM), I want to nominate an employee or vendor who exceeded expectations, so that their contributions and service can be recognized through the Employee/Vendor of the Month program.
- **Description:** ZTERS encourages recognition of exceptional service and performance from both internal employees and external vendors. To support this initiative, the platform provides a Nomination dashboard where employees can submit nominations for individuals or vendors who demonstrate outstanding performance or customer service. The nomination form allows users to submit the nominee’s information along with a reason for the nomination. Submissions are tracked in the system and may be reviewed to select monthly winners. Selected nominations may also be highlighted in company communications such as newsletters.
- **Timestamp:** Day 4, Part 1 [2:02:08 – 2:03:30]
- **Notes:** The system includes a Nomination dashboard where employees can nominate coworkers or vendors for recognition, supporting the organization’s Employee/Vendor of the Month program.
- **Responsible:** TBD

## CUBE-D4-024
- **Group:** Finance & Accounts Receivable
- **Category:** Outstanding Balance Monitoring
- **Epic:** Accounts Receivable Visibility
- **Parent Task:** Overdue Customer Balance Tracking
- **Task Name:** Open Balance Report – AM Balances Greater Than 60 Days
- **User Story:** As an Account Manager, I want a dashboard showing customers with open balances older than 60 days, so that I can identify overdue accounts and follow up with customers to resolve outstanding payments.
- **Description:** Account Managers need visibility into customers with overdue balances in order to reduce financial risk and ensure timely collections. The Open Balance Report – AM Balances > 60 Days dashboard displays customers whose invoices remain unpaid beyond a defined aging threshold. The report allows Account Managers to quickly identify delinquent accounts, review the amount owed, and see how long balances have been outstanding. By surfacing these aging balances in a centralized report, Account Managers can prioritize follow-ups with customers and coordinate with the Accounts Receivable team when necessary.
- **Timestamp:** Day 4, Part 1 [2:10:20 – 2:12:00]
- **Notes:** The team demonstrates a financial dashboard that highlights customers with balances older than 60 days, enabling Account Managers to monitor overdue accounts and take action.
- **Responsible:** TBD

## CUBE-D4-025
- **Group:** Finance & Accounts Receivable
- **Category:** Collections Monitoring
- **Epic:** Accounts Receivable Visibility
- **Parent Task:** Customer Collections Tracking
- **Task Name:** Collections Report – Account Manager Customer Totals
- **User Story:** As an Account Manager, I want a report showing the total number of customer accounts requiring collections attention, so that I can monitor which customers have outstanding balances and prioritize follow-ups.
- **Description:** Account Managers are responsible for maintaining healthy customer relationships while also ensuring that outstanding balances are addressed. The Collections Report – AM's Customer Totals dashboard provides a consolidated view of customers with accounts that require collection attention. The report displays customers associated with the Account Manager and highlights accounts with outstanding balances or collections activity. This allows Account Managers to quickly identify which customers require follow-up regarding unpaid invoices and coordinate with the Accounts Receivable team when necessary.
- **Timestamp:** Day 4, Part 1 [2:12:23 – 2:14:00]
- **Notes:** The system includes a Collections Report that summarizes customer accounts requiring collections follow-up for each Account Manager, helping monitor outstanding balances and prioritize customer outreach.
- **Responsible:** TBD

## CUBE-D4-026
- **Group:** Finance & Accounts Receivable
- **Category:** Credit Risk Monitoring
- **Epic:** Customer Credit Management
- **Parent Task:** Customer Credit Limit Monitoring
- **Task Name:** AM Customers Approaching Credit Limit Dashboard
- **User Story:** As an Account Manager, I want a report showing customers approaching their credit limit, so that I can proactively address credit issues before new orders are impacted.
- **Description:** Account Managers must monitor customer credit limits to ensure that customers can continue placing orders without interruptions. When customers approach their assigned credit limit, additional orders may be restricted or require financial review. The AM Customers Approaching Credit Limit dashboard provides Account Managers with visibility into customers nearing their credit limit. The report displays customer accounts, company names, and their current credit limits, allowing Account Managers to proactively identify accounts that may require attention.
- **Timestamp:** Day 4, Part 1 [2:17:12 – 2:18:30]
- **Notes:** The team demonstrates a report showing customers approaching their credit limit, helping Account Managers proactively monitor accounts that may soon require credit review or payment follow-up.
- **Responsible:** TBD

## CUBE-D4-027
- **Group:** Sales Operations
- **Category:** Account Ownership Management
- **Epic:** Account Manager Coverage & Reassignment
- **Parent Task:** Temporary Account Manager Reassignment
- **Task Name:** Temporary Reassignment of Account Manager Responsibilities
- **User Story:** As a Customer Support Supervisor (CSS), I want to temporarily reassign an Account Manager’s accounts to another Account Manager, so that customer accounts continue to be managed when an Account Manager is unavailable.
- **Description:** Account Managers may occasionally be unavailable due to vacation, leave, or other circumstances. During these periods, another Account Manager may need temporary visibility and responsibility over the affected accounts to ensure continuity of service. The system should allow authorized users (such as CSS roles) to temporarily reassign accounts from one Account Manager to another. Once reassigned, the substitute Account Manager should be able to view relevant dashboards, customer records, and reports associated with those accounts.
- **Timestamp:** Day 4, Part 1 [2:23:28 – 2:25:00]
- **Mockups:** NO MOCKUP PROVIDED
- **Notes:** It prevents account management gaps when someone is absent.
- **Responsible:** TBD

## CUBE-D4-028
- **Group:** Reporting & Dashboard
- **Category:** Recurring Billing Monitoring
- **Epic:** Recurring Service Billing Management
- **Parent Task:** Equipment Rental Billing Verification
- **Task Name:** Recurring Equipment Rental Billing Check Dashboard
- **User Story:** As an Account Manager, I want a dashboard showing recurring equipment rental billing records, so that I can verify that equipment rental services are being billed correctly and consistently
- **Description:** Some services, such as equipment rentals, involve recurring billing over a period of time. It is important to verify that these services are billed correctly throughout the duration of the rental and that billing stops appropriately when the service ends. The Recurring Equipment Rental Billing Check dashboard provides visibility into active or recent rental service records and their associated billing details. The report includes key information such as customer identifiers, equipment quantity, service frequency, service completion dates, and removal dates.
- **Timestamp:** Day 4, Part 1 [2:35:18 – 2:37:00]
- **Notes:** The team demonstrates a report used to verify recurring equipment rental billing, ensuring that rental services are correctly tracked and billed during their active lifecycle.
- **Responsible:** TBD
- **JT Notes:** This type of reporting is system wide, and not just in the context of ER like the example.

## CUBE-D4-029
- **Group:** Reporting & Dashboard
- **Category:** Accounting Inquiry Management
- **Epic:** Accounting Issue Visibility
- **Parent Task:** High Priority Accounting Inquiry Monitoring
- **Task Name:** Dedicated Dashboard for High Priority Accounting Inquiries
- **User Story:** As an Account Manager, I want a dedicated dashboard showing my high priority accounting inquiries, so that I can quickly identify and resolve urgent accounting issues related to my customers.
- **Description:** Account Managers frequently need to review and resolve accounting inquiries related to billing issues, vendor errors, refunds, or payment discrepancies. Currently, high priority accounting inquiries appear embedded within the main Account Manager dashboard, making them easy to overlook. To improve visibility and accessibility, the system should provide a dedicated dashboard accessible through a navigation button or menu option. This dashboard will display all high-priority accounting inquiries associated with the Account Manager, including relevant details such as issue status, related vendors, customer accounts, issue descriptions, and action notes.
- **Timestamp:** Day 4, Part 1 [2:36:50 – 2:38:00]
- **Notes:** Potentially an improvement
- **Responsible:** TBD
- **JT Notes:** This would also be applicable to fulfillment.

## CUBE-D4-030
- **Group:** Core Platform
- **Category:** Search & Navigation
- **Epic:** Unified Record Search
- **Parent Task:** Invoice Lookup Improvements
- **Task Name:** Search Invoices Using PO / Job Number
- **User Story:** As an Account Manager, I want to search invoices using a PO or Job Number, so that I can quickly locate invoices even when the invoice number is not available.
- **Description:** Account Managers frequently need to locate invoices when customers reference a PO number or job number instead of the invoice number. Currently, users often have to open multiple invoices or search manually to identify the correct billing record. The system should allow users to search using the PO or Job Number associated with a product or service record. When the search is executed, the system should return the relevant product record and allow users to access all invoices associated with that product.
- **Timestamp:** Day 4, Part 2 [0:11:00 – 0:14:00]
- **Mockups:** NO MOCKUP PROVIDED
- **Notes:** The team explains that users often search invoices using PO numbers rather than invoice numbers, and that the new CUBE system should allow invoice lookup through PO / Job Number associated with the product record.
- **Responsible:** TBD
- **JT Notes:** This should be solved by context driven global search

---

# Day 5

**Stories:** 20

## CUBE-D5-001
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** Customer Management
- **Parent Task:** Customer Account Monitoring
- **Task Name:** Credit Limit Warning Indicator
- **User Story:** As a Customer Success Specialist (CSS), I want to see a clearly highlighted warning message when a customer is approaching their credit limit so that I can quickly identify accounts that may require payment or billing review before continuing service operations.
- **Description:** When viewing a Customer record, the system should display a visible warning indicator if the customer's outstanding balance is approaching their configured credit limit. The warning should appear prominently in the Customer Information section, near the Credit Status field, using a visually distinct style (e.g., highlighted text, badge, or colored label).
- **Timestamp:** Day 5, Part 1 [0:08:00 – 0:10:00]
- **Notes:** Requested during the workshop to provide a clear visual alert for CSS users when a customer is nearing their credit limit, improving visibility and preventing service or billing issues.
- **Responsible:** TBD
- **JT Notes:** This is not resticted to CSS users, it is for all users.

## CUBE-D5-002
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** Customer Analytics & Reporting
- **Parent Task:** Customer Dashboard Improvements
- **Task Name:** Improve “New Sites by Month – YOY” Chart Visibility and Usability
- **User Story:** As a Customer Success Specialist (CSS), I want the “New Sites by Month – YOY” chart on the customer page (Customer Snapshot tab) to provide clearer and more useful information so that I can quickly understand customer growth trends without needing to interpret a complex chart.
- **Description:** The current “New Sites by Month – YOY” chart displayed on the customer record page provides a year-over-year visualization of newly created sites, but workshop participants indicated that the chart is difficult to interpret and does not provide immediate operational value. The system should improve the chart’s usability by presenting the information in a clearer and more meaningful way, allowing CSS users to quickly understand how a customer’s number of sites is growing over time.
- **Timestamp:** Day 5, Part 1 [0:10:30 – 0:12:00]
- **Notes:** During the workshop, participants indicated that the current YOY new sites chart is not very useful in its current form and suggested improving the visualization to make it more meaningful for operational users.
- **Responsible:** TBD

## CUBE-D5-003
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** Customer Site Management
- **Parent Task:** Site View Improvements
- **Task Name:** Display Site Spending Column in Customer Sites View
- **User Story:** As a Customer Success Specialist (CSS), I want to see the total spending per site directly in the Sites view under a customer record so that I can quickly identify which sites generate the most revenue.
- **Description:** Within the Customers module, the Sites/Leads tab displays a table listing all sites associated with a customer. During the workshop, CSS users indicated that it would be helpful to see the total spending per site directly within this table. Adding a spending column would allow CSS users to quickly evaluate the revenue contribution of each site without needing to navigate to multiple pages or run additional reports.
- **Timestamp:** Day 5, Part 1 [0:13:00 – 0:14:30]
- **Notes:** Requested improvement to help CSS users quickly identify high-value sites within a customer account without needing to run separate reports.
- **Responsible:** TBD

## CUBE-D5-004
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Customer Risk Monitoring
- **Parent Task:** Fraud Detection Alerts
- **Task Name:** Display Fraud Warning Based on Declined Credit Card Transactions
- **User Story:** As a Customer Success Specialist (CSS), I want the system to display a fraud warning on the Site page when a customer has multiple declined credit card transactions within a short period so that sales and operations teams are aware of potential payment risk.
- **Description:** Within the Sites module, the system should display a fraud warning indicator when a customer account has a high number of declined credit card transactions within a defined time window. This warning helps operational teams recognize potential fraud or payment risk associated with the customer. The warning should appear prominently within the Customer Information section of the Site page and be triggered when the number of declined credit card transactions reaches a configured threshold within a one-week period.
- **Timestamp:** Day 5, Part 1 [0:17:50 – 0:21:00]
- **Notes:** The fraud warning is triggered based on the number of declined credit card transactions within a one-week period, allowing sales and support teams to be aware of potential fraudulent or high-risk payment activity.
- **Responsible:** TBD
- **JT Notes:** This is not resticted to CSS users, it is for all users. It should show on the customer page and all related pages (including sites) not just the site page as indicated.

## CUBE-D5-005
- **Group:** Core Platform
- **Category:** Workflow Automation
- **Epic:** Credit and Payment Controls
- **Parent Task:** Past Due Approval Workflow
- **Task Name:** Automatic Notification to CSS for Past Due Approval Requests
- **User Story:** As a Customer Success Specialist (CSS), I want to automatically receive a notification when a customer with past due payments requests service so that I can review and approve or reject the request without relying on manual communication from the Account Manager.
- **Description:** Currently, when a customer account has past due payments, the Account Manager (AM) must manually notify the Customer Success Specialist (CSS) to request approval before proceeding with services or orders. This manual process introduces delays and risks of missed approvals. The system should automatically detect when a past-due customer attempts to proceed with service and generate an approval request notification to the CSS. The CSS should be able to review the request and approve or reject it directly within the system.
- **Timestamp:** Day 5, Part 1 [0:22:00 – 0:25:00]
- **Notes:** Current process relies on manual communication from AM to CSS. The goal is to automate the approval workflow for past-due customers requesting services.
- **Responsible:** TBD

## CUBE-D5-006
- **Group:** Core Platform
- **Category:** Workflow Improvement
- **Epic:** Credit and Payment Controls
- **Parent Task:** Past Due Override Management
- **Task Name:** Allow Past Due Override from Product Pages
- **User Story:** As a Customer Success Specialist (CSS), I want to override a customer's past due balance directly from product or service pages so that I do not need to navigate back to the Customer page to apply the override.
- **Description:** Currently, CSS users can override a customer’s past due balance restriction only from the Customer page using the “Override Past Due Balance Until” field. When CSS users are working within product or service pages (e.g., toilets, roll-offs, containers), they cannot apply this override directly. This requires the CSS to leave the current workflow, navigate to the Customer page, apply the override, and then return to the product page. The system should allow the same override functionality to be accessible from product/service pages where the past-due restriction prevents the user from proceeding.
- **Timestamp:** Day 5, Part 1 [0:30:30 – 0:33:30]
- **Notes:** Currently the override functionality exists only on the Customer page. CSS users requested the ability to apply the same override directly within product/service workflows to avoid switching between pages.
- **Responsible:** TBD
- **JT Notes:** Overrides will need to be available: heirarchial and granular (Customer>Site>Product)

## CUBE-D5-007
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** Customer Ownership Management
- **Parent Task:** Customer Record Owner Reassignment
- **Task Name:** Improve Customer Record Owner Change Process
- **User Story:** As a Customer Success Specialist (CSS), I want a simpler way to change the customer record owner so that I can quickly reassign accounts without navigating through a complex user selection process.
- **Description:** Currently, changing the Record Owner of a customer requires opening a Quickbase user selector and manually searching through the list of users or groups. This process is slow and inefficient when CSS users frequently need to reassign accounts. The system should improve the Record Owner Change workflow by making the user selection process faster and easier, allowing CSS users to quickly locate and assign the correct owner when updating customer records.
- **Timestamp:** Day 5, Part 1 [0:35:30 – 0:39:00]
- **Notes:** Discussion highlighted that customer ownership reassignment occurs frequently, so the current Quickbase user selection process should be optimized for faster execution.
- **Responsible:** TBD

## CUBE-D5-008
- **Group:** Core Platform
- **Category:** Security & Compliance
- **Epic:** System Audit and Traceability
- **Parent Task:** Platform Activity Logging
- **Task Name:** Implement Robust Audit Log for Customer and Product Changes
- **User Story:** As a Customer Success Specialist (CSS), I want the system to maintain a detailed audit log of changes made within Customer and Product pages so that all modifications can be tracked for accountability and troubleshooting.
- **Description:** CSS users are able to make various changes across the Customer module and Product pages within the system. Currently, the visibility into who made changes, when they were made, and what values were modified is limited. CUBE should implement a robust audit logging system that records all relevant modifications across key modules. This log should allow administrators and authorized users to track changes to customer records, product configurations, and other operational data.
- **Timestamp:** Day 5, Part 1 [0:42:00 – 0:45:00]
- **Mockups:** NO MOCKUP AVAILABLE
- **Notes:** Workshop discussion emphasized the need for a more robust audit trail within CUBE to track modifications performed by CSS users across customer and product records.
- **Responsible:** TBD
- **JT Notes:** Overall system user story; not limited to this context.

## CUBE-D5-009
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** System Notification
- **Parent Task:** Approval Notification Improvements
- **Task Name:** Improve Email Notification Formatting for Approval Events
- **User Story:** As a Customer Success Specialist (CSS), I want system-generated approval notification emails to be clearly formatted and easy to read so that I can quickly understand the details of the change or approval action.
- **Description:** When a CSS performs actions such as approving a Past Due approval request, the system sends an automatic email notification. Currently, these notifications are poorly formatted, making the content difficult to read and the information hard to interpret. CUBE should improve the structure and formatting of system-generated notification emails so that users can easily identify the key details, including the customer involved, the action performed, and the changes made.
- **Timestamp:** Day 5, Part 1 [0:43:30 – 0:46:00]
- **Notes:** During the workshop demonstration, the CSS showed a system notification email generated after a Past Due approval, noting that the current formatting is difficult to read and should be improved for usability.
- **Responsible:** TBD

## CUBE-D5-010
- **Group:** Core Platform
- **Category:** Workflow Automation
- **Epic:** Customer Ownership Management
- **Parent Task:** Bulk Customer Operations
- **Task Name:** Enable Bulk Customer Actions from Customer Module
- **User Story:** As a Customer Success Specialist (CSS), I want to filter customers by Account Manager and perform bulk actions so that I can efficiently manage large groups of customer accounts.
- **Description:** CSS users frequently need to perform operational changes affecting multiple customers, such as reassigning accounts when an Account Manager leaves or when customer portfolios are redistributed. Currently, these updates must be performed individually, which is time-consuming and inefficient. The system should provide a Customer management view that allows CSS users to filter customers by Account Manager and perform bulk or mass actions on the resulting records. These actions may include operations such as mass reassignment of customer ownership.
- **Timestamp:** Day 5, Part 1 [0:45:30 – 0:49:00]
- **Notes:** Workshop discussion highlighted the need for CSS users to efficiently manage large portfolios of customer accounts, particularly during account redistribution or personnel changes.
- **Responsible:** TBD
- **JT Notes:** While true, this should not be confused with overall system bulk actions (e.g. favorite, delete, etc.)

## CUBE-D5-011
- **Group:** Core Platform
- **Category:** UI/UX Improvement
- **Epic:** Customer Financial Visibility
- **Parent Task:** Collections Information Visibility
- **Task Name:** Highlight Most Recent Collection Note in Customer View
- **User Story:** As a Customer Success Specialist (CSS), I want to easily see the most recent collection note date on the customer page so that I can quickly understand the latest collections activity without reviewing all historical notes.
- **Description:** CSS users frequently consult the Collections Notes section within the Customer module to review customer payment discussions, balances, and follow-up actions. Currently, the notes appear as a list of entries ordered by date, requiring users to manually review the records to identify the most recent update. The system should highlight or prominently display the most recent collection note date in a visible location on the customer page so that CSS users can quickly identify the latest collections interaction.
- **Timestamp:** Day 5, Part 1 [0:59:00 – 1:02:00]
- **Notes:** CSS mentioned that they frequently rely on the collections notes when reviewing customer financial status and want the most recent update to be immediately visible.
- **Responsible:** TBD

## CUBE-D5-012
- **Group:** Sales Operations
- **Category:** Sales Incentives
- **Epic:** Perfect Sale Bonus Tracking
- **Parent Task:** Perfect Sale Qualification Logic
- **Task Name:** Track Perfect Sale Bonus Eligibility and Payout
- **User Story:** As a Customer Success Specialist (CSS), I want the system to identify when a site qualifies as a Perfect Sale and track whether the bonus payout has been issued so that sales incentives can be managed accurately.
- **Description:** A Perfect Sale occurs when an Account Manager sells all core service categories to a single site, including portable toilets, roll-offs/dumpsters, storage containers, and fencing. When this condition is met, the Account Manager becomes eligible for a Perfect Sale bonus payout of $100. The system should track whether a site qualifies as a Perfect Sale and allow the payout status to be recorded through a Perfect Sale Paid Out indicator within the Customer module.
- **Timestamp:** Day 5, Part 1 [1:02:30 – 1:05:00]
- **Notes:** Perfect Sale bonuses are paid to Account Managers when all core service categories are sold to a single site, providing a $100 incentive for full-service sales.
- **Responsible:** TBD
- **JT Notes:** Additiuonal criteria: timeframe of sale date(s) must be included.

## CUBE-D5-013
- **Group:** Billing Operations
- **Category:** Workflow Management
- **Epic:** Credit Processing Workflow
- **Parent Task:** Credit Approval Monitoring
- **Task Name:** Provide View for Unprocessed Approved Credits
- **User Story:** As a Customer Success Specialist (CSS), I want to view all approved credits that have not yet been processed so that I can ensure they are reviewed and applied in a timely manner.
- **Description:** CSS users need visibility into credits that have already been approved but are still pending processing. Without a dedicated view, it becomes difficult to track which credits require action and ensure they are properly applied to invoices or customer accounts. The system should provide an Unprocessed / Approved Credits view that allows CSS users to easily identify, review, and process credits that are awaiting completion.
- **Timestamp:** Day 5, Part 1 [1:22:30 – 1:25:00]
- **Notes:** During the workshop discussion, CSS users described using this view as an operational queue to track approved credits that still need to be processed.
- **Responsible:** TBD

## CUBE-D5-014
- **Group:** Sales Operations
- **Category:** Reporting & Analytics
- **Epic:** Sales Team Performance Dashboard
- **Parent Task:** Automated Team KPI Tracking
- **Task Name:** Provide Automated Sales Team Performance Dashboard
- **User Story:** As a Customer Success Specialist (CSS), I want to view my team’s performance metrics in an automated dashboard so that I can monitor Account Manager performance without relying on manual spreadsheets.
- **Description:** CSS users currently rely on a manually maintained Team Tracking Spreadsheet to monitor the performance of Account Managers within their team. This spreadsheet tracks several operational and sales KPIs such as sales totals, expected sales, margins, new customers, new sites, multi-product sales, and collections metrics. CUBE should provide an automated team performance dashboard that aggregates these metrics directly from system data, eliminating the need for manual spreadsheet tracking and providing real-time visibility into team performance.
- **Timestamp:** Day 5, Part 1 [1:26:30 – 1:32:00]
- **Notes:** The CSS demonstrated an internal team tracking spreadsheet used to monitor sales team KPIs and explained that this information should be automatically generated within CUBE.
- **Responsible:** TBD

## CUBE-D5-015
- **Group:** Pricing & Margin Control
- **Category:** Approval Workflow
- **Epic:** Low Margin Approval Process
- **Parent Task:** Margin Exception Handling
- **Task Name:** Require Approval and Reason for Low Margin Deals
- **User Story:** As a Customer Success Specialist (CSS), I want to approve low-margin deals and provide a reason for the exception so that pricing decisions are properly reviewed and documented.
- **Description:** Certain deals may fall below the expected profit margin threshold due to operational constraints, customer negotiations, or pricing adjustments. When this occurs, the system should require an approval from the appropriate role (Lead or CSS/CSM) before the deal can proceed. During the approval process, the approver must select a Low Margin Reason explaining why the margin exception is allowed. This ensures transparency and provides a documented justification for low-margin pricing decisions.
- **Timestamp:** Day 5, Part 1 [1:38:30 – 1:42:00]
- **Notes:** The workshop discussion highlighted the need to document margin exceptions and provide visibility into the reasons behind low-margin deals.
- **Responsible:** TBD

## CUBE-D5-016
- **Group:** Sales Operations
- **Category:** Reporting & Analytics
- **Epic:** Sales Performance Reporting
- **Parent Task:** Close Ratio Visibility
- **Task Name:** Display Close Ratio Report on CSS Dashboard
- **User Story:** As a Customer Success Specialist (CSS), I want to view the Close Ratio Report directly from my dashboard so that I can quickly evaluate sales performance across personal and business queues.
- **Description:** CSS users currently rely on Close Ratio Reports to evaluate how effectively Account Managers convert opportunities into closed sales. Although the report exists, it is not easily accessible within the system and requires additional navigation to locate. CUBE should provide a dashboard-accessible Close Ratio Report that clearly breaks down performance metrics by personal queues and business queues, allowing CSS users to quickly analyze sales conversion performance.
- **Timestamp:** Day 5, Part 1 [1:42:30 – 1:45:30]
- **Notes:** During the workshop discussion, the CSS explained that the Close Ratio Report already exists but should be more easily accessible and integrated into the dashboard with clearer breakdowns between queue types.
- **Responsible:** TBD

## CUBE-D5-017
- **Group:** Sales Operations
- **Category:** Reporting & Analytics
- **Epic:** Close Ratio Performance Tracking
- **Parent Task:** Account Manager Conversion Metrics
- **Task Name:** Provide Close Ratio Dashboard for Account Managers
- **User Story:** As an Account Manager (AM), I want to view my close ratio metrics on a dashboard so that I can track how effectively I convert opportunities into customers.
- **Description:** Account Managers rely on close ratio metrics to evaluate their sales performance and understand how effectively they convert leads into closed deals. The Close Ratio Dashboard provides visibility into conversion statistics, including the number of opportunities handled and the percentage that result in successful sales. The dashboard should present these metrics in a clear format and allow AMs to view conversion performance across personal queues and business queues, helping them identify trends and areas for improvement
- **Timestamp:** Day 5, Part 1 [1:57:30 – 2:00:00]
- **Notes:** During the workshop discussion, participants emphasized that the Close Ratio Dashboard is an important performance metric used by Account Managers to monitor their sales conversion rates.
- **Responsible:** TBD

## CUBE-D5-018
- **Group:** Sales Operations
- **Category:** Workflow Integration
- **Epic:** Sales Communication and Quoting Workflow
- **Parent Task:** Customer Call and Pricing Workflow
- **Task Name:** Support Integration Between Customer Call Records and Pricing Tool
- **User Story:** As an Account Manager (AM), I want to access customer call information and quickly generate quotes using the pricing tool so that I can efficiently respond to customer inquiries during or after sales calls.
- **Description:** Account Managers often conduct customer calls using communication tools such as Dialpad, where conversations are recorded and transcribed. After discussing service requirements with the customer, the AM must switch to the Hub pricing tool to calculate service quotes. CUBE should support this workflow by allowing AMs to easily transition from customer communication records to the pricing tool, ensuring a smoother process for generating quotes and responding to customer requests.
- **Timestamp:** Day 5, Part 1 [2:00:00 – 2:18:00]
- **Mockups:** NO MOCKUP AVAILABLE
- **Notes:** During the workshop demonstration, the Account Manager used Dialpad to conduct and record a customer call and then switched to the Hub pricing tool to generate a quote, illustrating a common sales workflow.
- **Responsible:** TBD

## CUBE-D5-019
- **Group:** Sales Operations
- **Category:** Payment Processing
- **Epic:** Secure Payment Method Management
- **Parent Task:** Credit Card Capture Workflow
- **Task Name:** Add Credit Card Using Authorize.Net Secure Form
- **User Story:** As an Account Manager (AM), I want to securely add a customer's credit card through an Authorize.Net form so that payment information can be stored safely and used for billing.
- **Description:** When adding a new credit card for a customer, the system must use the Authorize.Net payment gateway API to securely capture the payment information. Due to security and compliance requirements, sensitive card information should not be stored directly in CUBE. The system should present a secure modal form or embedded payment interface that allows the user to enter credit card information through Authorize.Net. Once submitted, the payment method token should be stored in CUBE for future billing transactions.
- **Timestamp:** Day 5, Part 1 [2:30:30 – 2:33:30]
- **Notes:** During the discussion, Justin mentioned that adding a credit card requires using the Authorize.Net API and suggested implementing a separate modal or form to securely collect payment information.
- **Responsible:** TBD

## CUBE-D5-020
- **Group:** Sales Operations
- **Category:** User Experience Improvement
- **Epic:** Account Manager Workflow Efficiency
- **Parent Task:** Centralized Customer Information Access
- **Task Name:** Consolidate Customer Information to Reduce Multi-Tab Workflow
- **User Story:** As an Account Manager (AM), I want to access all necessary customer information from a centralized interface so that I do not need to open multiple browser tabs while managing a customer.
- **Description:** Account Managers often need to collect and verify multiple pieces of information when working with customers, including contact details, service history, pricing information, and billing data. Currently, AMs must open several browser tabs to gather this information from different parts of the system. CUBE should provide a more consolidated workflow that allows AMs to view and manage key customer information within a single interface, reducing context switching and minimizing the risk of errors.
- **Timestamp:** Day 5, Part 2 [0:07:30 – 0:10:00]
- **Notes:** During the workshop discussion, AMs highlighted that managing multiple open tabs is a major pain point in their workflow and suggested consolidating customer information within CUBE.
- **Responsible:** TBD

---
