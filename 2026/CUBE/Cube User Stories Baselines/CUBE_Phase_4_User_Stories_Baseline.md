# CUBE User Stories — Phase 4 Baseline

**Purpose:** Reference baseline for comparing later CUBE phases against Phase 4. Use together with the Phase 2 and Phase 3 baselines when classifying later user stories as **Existing**, **New Feature**, or **Hybrid**.

**Phase 4 scope:**
- Day 1: 58 user stories
- Day 2: 61 user stories
- Day 3: 55 user stories
- Day 4: 36 user stories
- **Total: 210 user stories**

**Comparison guidance:**
- Compare later stories by underlying functionality, not wording alone.
- Use the User Story together with Description, Acceptance Criteria, Notes, and other provided context.
- A later story may be **Existing** if Phase 4 already covers the same capability, or **Hybrid** if the capability exists but the later phase adds a meaningful behavior, workflow, rule, field, integration, permission, UI change, or extension.

---

# Day 1

**Stories:** 58

## CUBE-PH4-D1-001
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Ticket Creation
- **Task Name:** Create Service Ticket When AM Is Unavailable
- **User Story:** As a Business Development Representative (BDR), I want to create a service ticket when the Account Manager is unavailable, so that urgent customer requests can still be started.
- **Description:** BDRs create delivery, swap, mobile, or service tickets only when the AM is unavailable and the request needs to be handled ASAP.
- **Acceptance Criteria:** 1. BDR can create a service ticket when the AM is unavailable, 2. Ticket creation supports urgent customer requests, 3. Ticket creation includes delivery, swap, mobile, or service ticket situations mentioned in the workshop, 4. BDR can create a ticket when the request needs to be made ASAP, 5. The ticket can continue into the fulfillment process
- **Timestamp:** Day 1, Part 1 [0:07:38 – 0:08:14]
- **Notes:** BDRs normally do not create service tickets unless the AM is unavailable or the BDR makes the sale.
- **Responsible:** TBD

## CUBE-PH4-D1-002
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Sales Fulfillment
- **Task Name:** Create Delivery and Fulfillment Tickets After BDR Sale
- **User Story:** As a Business Development Representative (BDR), I want to create the delivery service ticket and fulfillment ticket when I make a sale, so that the sale can move into fulfillment.
- **Description:** When the BDR makes the sale, the BDR creates the delivery service ticket and the fulfillment ticket as part of the standard process.
- **Acceptance Criteria:** 1. BDR can create a delivery service ticket after making a sale, 2. BDR can create a fulfillment ticket after making a sale, 3. Ticket creation is part of the standard sale process, 4. Ticket creation is not dependent on AM availability when the BDR made the sale, 5. The sale can proceed to fulfillment after the tickets are created
- **Timestamp:** Day 1, Part 1 [0:08:14 – 0:08:41]
- **Mockups:** NO MOCKUP
- **Notes:** This story is specific to sales made by the BDR.
- **Responsible:** TBD

## CUBE-PH4-D1-003
- **Group:** Product Setup
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Product to Sale Conversion
- **Task Name:** Mark Product as Sale After Quote Is Given
- **User Story:** As a Business Development Representative (BDR), I want to mark a quoted product as a sale when the customer wants to move forward, so that the sale can continue into fulfillment.
- **Description:** After pricing and product information are completed, the product can be marked as a sale when the customer agrees to move forward.
- **Acceptance Criteria:** 1. User can access the customer site and pricing tool, 2. User can select the requested product type, 3. User can enter the requested delivery date, 4. User can mark the quote as given, 5. User can mark the product as a sale when the customer wants to move forward
- **Timestamp:** Day 1, Part 1 [0:09:26 – 0:10:42]
- **Notes:** Product status is changed from the Status dropdown. Screenshot shows the Sale option available in the product status list.
- **Responsible:** TBD

## CUBE-PH4-D1-004
- **Group:** Site Information
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Site Details
- **Task Name:** Capture Placement and Site Access Details
- **User Story:** As a Business Development Representative (BDR), I want to enter placement instructions, gate codes, on-site contact information, and site hours, so that service and fulfillment teams have the information needed for delivery.
- **Description:** Placement instructions, on-site contact details, gate codes, and hours of operation are captured before the fulfillment ticket is created.
- **Acceptance Criteria:** 1. User can enter placement instructions, 2. User can view or enter the on-site contact, 3. User can enter gate code information when applicable, 4. User can enter hours of operation, 5. User can save the site information before creating the fulfillment ticket
- **Timestamp:** Day 1, Part 1 [0:11:21 – 0:12:46]
- **Notes:** Site hours are especially important when the customer keeps the unit on-site for over a month. Screenshot shows placement instructions being added as a placement note.
- **Responsible:** TBD

## CUBE-PH4-D1-005
- **Group:** Fulfillment Tickets
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Fulfillment Ticket Details
- **Task Name:** Display Placement Details on Fulfillment Ticket
- **User Story:** As a Business Development Representative (BDR), I want placement instructions visible on the fulfillment ticket, so that I do not have to manually retype placement information into ticket notes.
- **Description:** Placement instructions should be visible on the fulfillment ticket so users do not have to manually retype placement information into ticket notes.
- **Acceptance Criteria:** 1.Fulfillment ticket displays placement instructions, 2. Placement details come from the existing site or product information, 3. User does not need to retype placement instructions into ticket notes, 4. Fulfillment can view placement information from the ticket page, 5. Missing placement details are reduced during delivery coordination
- **Timestamp:** Day 1, Part 1 [0:13:55 – 0:15:53]
- **Notes:** This was identified after the BDR explained that she repeats product and placement information in ticket notes because those details may not be visible to fulfillment.
- **Responsible:** TBD

## CUBE-PH4-D1-006
- **Group:** Fulfillment Tickets
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Site Access Details
- **Task Name:** Display Gate Codes and Site Hours on Fulfillment Ticket
- **User Story:** As a Business Development Representative (BDR), I want gate codes and site hours visible on the fulfillment ticket, so that fulfillment and haulers have the access details needed for delivery coordination.
- **Description:** Gate codes and site hours should be visible on the fulfillment ticket so users do not have to manually duplicate site access details already captured elsewhere.
- **Acceptance Criteria:** 1.Fulfillment ticket displays gate code information when available, 2. Fulfillment ticket displays site hours when available, 3. Site access details are visible without relying only on ticket notes, 4. Fulfillment can use access details during hauler coordination, 5. User does not need to duplicate site access details already captured elsewhere.
- **Timestamp:** Day 1, Part 1 [0:15:30 – 0:16:31]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop mentions fulfillment saying they did not see gate code information, which caused follow-up calls when haulers needed access details.
- **Responsible:** TBD

## CUBE-PH4-D1-007
- **Group:** Fulfillment Tickets
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** On-Site Contacts
- **Task Name:** Show Multiple Site Contacts on Fulfillment Ticket
- **User Story:** As a Business Development Representative (BDR), I want all site-related contacts displayed on the fulfillment ticket, so that secondary on-site contacts are visible when needed.
- **Description:** Secondary on-site contacts should be visible on the fulfillment ticket instead of being manually added to ticket notes.
- **Acceptance Criteria:** 1. Fulfillment ticket can display more than one site-related contact, 2. Contacts related to the customer and site are visible on the fulfillment ticket, 3. Secondary on-site contact information does not need to be manually typed into notes, 4. Contact information supports fulfillment coordination, 5. Displayed contacts are tied to the relevant site or customer.
- **Timestamp:** Day 1, Part 1 [0:16:31 – 0:17:48]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop mentions showing all contacts related to the site that the product is for.
- **Responsible:** TBD

## CUBE-PH4-D1-008
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Requested Delivery Date
- **Task Name:** Carry Requested Delivery Date Into Fulfillment Ticket
- **User Story:** As a Business Development Representative (BDR), I want the requested delivery date to carry into the fulfillment ticket, so that fulfillment can work from the date captured on the product page.
- **Description:** The requested delivery date carries over from the product page into the fulfillment ticket, while the final delivery date may change after fulfillment contacts the hauler.
- **Acceptance Criteria:** 1. Fulfillment ticket displays the requested delivery date from the product page, 2. Requested delivery date is treated as requested rather than confirmed, 3. Date is available before fulfillment confirms hauler availability, 4. Fulfillment can update the final date after speaking with the hauler, 5. User can distinguish the requested delivery date from the confirmed delivery date.
- **Timestamp:** Day 1, Part 1 [0:17:52 – 0:18:18]
- **Notes:** The workshop clarifies that the requested date may change once fulfillment contacts the hauler. Screenshot shows Requested Delivery Date populated and Confirmed Delivery Date still empty.
- **Responsible:** TBD

## CUBE-PH4-D1-009
- **Group:** Fulfillment Tickets
- **Category:** Workflow
- **Epic:** Fulfillment Submission
- **Parent Task:** Send Fulfillment Ticket After Review
- **Task Name:** Send Fulfillment Ticket After Review Button
- **User Story:** As a Business Development Representative (BDR), I want to save the fulfillment ticket and send it to fulfillment, so that the fulfillment team can begin processing the delivery request.
- **Description:** After reviewing and saving the fulfillment ticket, the user sends it to fulfillment through a separate Send to Fulfillment action.
- **Acceptance Criteria:** 1. User can save the fulfillment ticket before sending it, 2. User can send the ticket to fulfillment after saving, 3. Send to Fulfillment action is separate from Save, 4. Ticket includes delivery-related details before submission, 5. Submission completes the BDR’s fulfillment ticket step
- **Timestamp:** Day 1, Part 1 [0:22:31 – 0:23:42]
- **Notes:** The process is handled as a two-click workflow: save first, then send to fulfillment.
- **Responsible:** TBD

## CUBE-PH4-D1-010
- **Group:** Notifications
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** AM Sale Alert
- **Task Name:** Notify AM When BDR Creates a Sale
- **User Story:** As an Account Manager (AM), I want to receive an automatic alert when a BDR creates a sale on my customer, so that I know the sale is ready for my follow-up steps.
- **Description:** When a BDR creates a sale for an AM-owned customer, the system should automatically alert the AM instead of requiring the BDR to send a manual email.
- **Acceptance Criteria:** 1.System sends an alert to the AM when a BDR creates a sale, 2. Alert identifies the AM’s customer and sale, 3. Alert replaces the manual email currently sent by the BDR, 4. Alert is triggered at the sale handoff point, 5. AM can continue the next steps after fulfillment confirms the delivery ticket.
- **Timestamp:** Day 1, Part 1 [0:23:42 – 0:24:52]
- **Mockups:** NO MOCKUP
- **Notes:** The AM needs to know about the sale because the customer belongs to the AM, even though the BDR handled the initial sale.
- **Responsible:** TBD

## CUBE-PH4-D1-011
- **Group:** Billing Preferences
- **Category:** Data Validation
- **Epic:** Core Flow
- **Parent Task:** Billing Preference Setup
- **Task Name:** Require Needed Billing Preference Fields Before Sale Progression
- **User Story:** As an Account Manager (AM), I want billing preference fields to clearly indicate required information, so that missing billing details can be corrected before the sale process continues.
- **Description:** Billing preference fields should clearly indicate required information before the user saves the billing preference and continues the sale workflow.
- **Acceptance Criteria:** 1.Billing preference form identifies required fields, 2. Missing required billing information prevents incomplete billing setup, 3. User receives validation before progressing in the sale workflow, 4. Billing preference can be saved only when required information is present, 5. Product sale progression uses a valid billing preference.
- **Timestamp:** Day 1, Part 1 [0:26:37 – 0:28:24]
- **Notes:** Fields required for sale progression should be clearly marked on the billing preference form instead of only triggering an error later.
- **Responsible:** TBD

## CUBE-PH4-D1-012
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Ticket Status
- **Task Name:** Display Service Ticket Status Based on Date Range
- **User Story:** As an Account Manager (AM), I want the service ticket status to reflect whether the ticket is pending, active, or inactive, so that I can understand where the ticket is in the service timeline.
- **Description:** Service ticket status starts as pending and changes based on whether the current date falls within the applicable service date or service cycle.
- **Acceptance Criteria:** 1. Service ticket starts in pending status, 2. Service ticket becomes active when the current date matches the applicable service timing, 3. Service ticket can become inactive after the applicable service period, 4. Status is calculated using the ticket’s service date or cycle date range, 5. Status applies to both single-date and cycle-based service tickets.
- **Timestamp:** Day 1, Part 1 [0:29:02 – 0:30:22]
- **Notes:** Delivery tickets use one service date, while monthly service tickets use start and end dates.
- **Responsible:** TBD

## CUBE-PH4-D1-013
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Dispatch Request Source
- **Task Name:** Capture Service Requester Information
- **User Story:** As an Account Manager (AM), I want to capture who requested a service, so that the customer-side request is documented even when the requester is not an existing site contact.
- **Description:** The service ticket should capture who called in or requested the service, even when that person is not already listed as an on-site contact or customer contact.
- **Acceptance Criteria:** 1. User can capture the person who requested the service, 2. Requester information can be recorded even when the person is not an existing contact, 3. Requester information remains available as a reference on the service ticket, 4. Requester capture is separate from fulfillment dispatch information, 5. Requester information supports delivery, monthly service, and miscellaneous service contexts.
- **Timestamp:** Day 1, Part 1 [0:30:22 – 0:32:33]
- **Notes:** The current dispatching fields are partly a holdover from when AMs handled the full process. The future process should separate customer-side request information from fulfillment dispatch details.
- **Responsible:** TBD

## CUBE-PH4-D1-014
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Standard Charge Status
- **Task Name:** Show Billing Setup Status on Service Ticket
- **User Story:** As an Account Manager (AM), I want the standard charge status to show whether billing setup is complete, so that I know what billing action is still required.
- **Description:** Standard charge status identifies missing billing requirements, such as a required line item, and later changes as the ticket moves through the invoicing process.
- **Acceptance Criteria:** 1. Standard charge status identifies when a required line item is missing, 2. Status reflects billing setup requirements based on ticket and product codes, 3. Status updates after the required line item is created, 4. Status identifies when invoicing is required, 5. Status supports AM dashboard visibility for pending billing actions.
- **Timestamp:** Day 1, Part 1 [0:33:29 – 0:34:36]
- **Notes:** The example shows a delivery ticket requiring a delivery line item.
- **Responsible:** TBD

## CUBE-PH4-D1-015
- **Group:** Service Tickets
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Ticket Snapshot Values
- **Task Name:** Keep Service Ticket Values Independent After Creation
- **User Story:** As an Account Manager (AM), I want service ticket values to be copied as a point-in-time snapshot, so that later product changes do not automatically alter already-created tickets.
- **Description:** Service ticket values such as dates, vendor information, and rates are copied when the ticket is created, allowing the ticket to preserve the values that were valid at that time.
- **Acceptance Criteria:** 1. Service ticket stores copied values from the product at creation time, 2. Later product changes do not automatically update existing ticket values, 3. Ticket values can be edited when corrections or customer changes are needed, 4. Snapshot behavior applies to key service information such as dates, vendor details, and rates, 5. User can update ticket-specific values without changing the original product record.
- **Timestamp:** Day 1, Part 1 [0:35:33 – 0:38:15]
- **Notes:** Snapshot behavior supports typo corrections, customer date changes, and pricing or rate changes without automatically affecting existing tickets.
- **Responsible:** TBD

## CUBE-PH4-D1-016
- **Group:** Service Tickets
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Vendor Information
- **Task Name:** Copy Vendor Information From Product to Service Ticket
- **User Story:** As an Account Manager (AM), I want vendor information to copy from the product page to the service ticket, so that the ticket contains the selected vendor and related vendor details.
- **Description:** Vendor information is copied from the product page into the service ticket and displayed as part of the ticket’s vendor details.
- **Acceptance Criteria:** 1. Service ticket copies the related vendor from the product page, 2. Ticket displays vendor lookup information, 3. Vendor details include available hauler contact information, 4. Ticket code is determined by the button used to create the ticket, 5. Copied vendor information remains part of the ticket snapshot.
- **Timestamp:** Day 1, Part 1 [0:38:15 – 0:39:35]
- **Notes:** The example uses the delivery ticket button with a hard-coded delivery ticket code. Screenshot shows the copied vendor information section on the service ticket.
- **Responsible:** TBD

## CUBE-PH4-D1-017
- **Group:** Service Tickets
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Rate Snapshot
- **Task Name:** Copy Customer and Vendor Rates Into Service Ticket
- **User Story:** As an Account Manager (AM), I want customer and vendor rates copied into the service ticket, so that line items can use the rates available when the ticket was created.
- **Description:** Customer and vendor rates are copied from the product into the service ticket, allowing line items to use the applicable rate based on the ticket type.
- **Acceptance Criteria:** 1.Service ticket copies customer rates from the product, 2. Service ticket copies vendor rates from the product, 3. Ticket stores the full rate card available at creation time, 4. Line items can use the applicable copied rate based on ticket type, 5. Later product rate changes do not automatically update copied ticket rates.
- **Timestamp:** Day 1, Part 1 [0:39:35 – 0:42:09]
- **Mockups:** NO MOCKUP
- **Notes:** Delivery, standard, relocation, and other rates may be needed depending on the ticket type.
- **Responsible:** TBD

## CUBE-PH4-D1-018
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** PO Number Updates
- **Task Name:** Allow PO Number Updates on Service Ticket
- **User Story:** As an Account Manager (AM), I want to update the PO number at the service ticket level, so that invoice information can be corrected without canceling every related ticket and line item.
- **Description:** PO information can carry over from the product page, but it may need to be updated at the service ticket level when the PO changes or needs correction for invoicing.
- **Acceptance Criteria:** 1. Service ticket displays the PO number copied from the product, 2. User can update the PO number at the service ticket level, 3. Updated PO number can support invoice correction, 4. User does not need to cancel every related service ticket only to correct PO information, 5. Ticket-level PO value remains available for the billing flow.
- **Timestamp:** Day 1, Part 1 [0:43:02 – 0:45:12]
- **Notes:** Customers may call when the PO number is not shown correctly on the invoice. Screenshot shows the editable PO # field on the service ticket.
- **Responsible:** TBD

## CUBE-PH4-D1-019
- **Group:** Billing Preferences
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Billing Preference Selection
- **Task Name:** Select Billing Preference on Service Ticket
- **User Story:** As an Account Manager (AM), I want billing preference information to carry into the service ticket and remain selectable, so that billing can be adjusted when a customer wants to use a different payment method.
- **Description:** The billing preference selected on the product carries into the service ticket by default, but it can be changed when needed for a specific service ticket.
- **Acceptance Criteria:** 1. Service ticket defaults to the billing preference selected on the product, 2. User can change the billing preference at the service ticket level, 3. Billing preference supports situations where the customer wants to use a different card or payment method, 4. User can correct a wrong billing preference, 5. Billing preference selection remains part of the ticket billing information.
- **Timestamp:** Day 1, Part 1 [0:45:12 – 0:46:20]
- **Notes:** Nichole states that billing preference sometimes has to be changed at every level. Screenshot shows the Billing Preferences tab on the service ticket.
- **Responsible:** TBD

## CUBE-PH4-D1-020
- **Group:** Billing Preferences
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Billing Preference Hierarchy
- **Task Name:** Add and Select Billing Preference Across Customer Hierarchy
- **User Story:** As an Account Manager (AM), I want to add and select billing preferences at different customer hierarchy levels, so that billing can be configured flexibly for customers, sites, products, and service tickets.
- **Description:** Billing preferences should be configurable at different hierarchy levels, allowing users to apply or override billing selections for a customer, site, product, or service ticket when needed.
- **Acceptance Criteria:** 1. User can select a billing preference at applicable hierarchy levels, 2. User can add a billing preference where billing preference selection is available, 3. Billing preferences can be configured at customer, site, product, and service ticket levels, 4. System supports overriding prior billing preference selections, 5. User receives a warning when a billing preference change may affect multiple sites or products.
- **Timestamp:** Day 1, Part 1 [0:46:20 – 0:49:30]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop mentions using a warning when a billing preference change may affect many sites or products.
- **Responsible:** TBD

## CUBE-PH4-D1-021
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Cancellation Prerequisites
- **Task Name:** Cancel Service Ticket Only After Line Items Are Canceled or Credited
- **User Story:** As an Account Manager (AM), I want service ticket cancellation to depend on related line item status, so that billed items are reversed before the ticket is canceled.
- **Description:** Service tickets can be canceled only after related line items are canceled or credited, ensuring billed items are properly reversed before the cancellation is completed.
- **Acceptance Criteria:** 1. Service ticket can be canceled only after related line items are canceled or credited, 2. Unbilled line items can be canceled, 3. Billed line items must be credited back before cancellation, 4. Invoicing acts as the system freeze point, 5. Cancellation follows the reverse order of billing actions.
- **Timestamp:** Day 1, Part 1 [0:52:48 – 0:55:22]
- **Notes:** Once something is billed and reaches Intacct, it becomes the stopping point and must be reversed before the service ticket can be canceled. Screenshot shows the service ticket cancellation dropdown.
- **Responsible:** TBD

## CUBE-PH4-D1-022
- **Group:** Sales Dashboard
- **Category:** Reporting
- **Epic:** Core Flow
- **Parent Task:** BDR Sales Tracking
- **Task Name:** Track BDR Sales and Cancellations
- **User Story:** As a Business Development Representative (BDR), I want to track my actual sales and cancellations, so that I can understand changes that affect my commission.
- **Description:** BDRs need visibility into credited sales, canceled sales, and changes to their sales count so they can understand how cancellations affect their monthly commission tracking.
- **Acceptance Criteria:** 1. BDR can view sales credited to them, 2. BDR can see when credited sales are canceled, 3. Dashboard shows changes that reduce the sales count, 4. BDR can identify which sales were canceled, 5. Canceled sales include a visible cancellation or no-sale reason when available.
- **Timestamp:** Day 1, Part 1 [1:00:00 – 1:02:16]
- **Mockups:** NO MOCKUP
- **Notes:** BDRs may think they made a certain number of sales, but later discover the report shows fewer because some sales were canceled.
- **Responsible:** TBD

## CUBE-PH4-D1-023
- **Group:** Sales Dashboard
- **Category:** Reporting
- **Epic:** Core Flow
- **Parent Task:** Re-Engaged Customer Credit
- **Task Name:** Track BDR Credit for Re-Engaged Customers
- **User Story:** As a Business Development Representative (BDR), I want re-engaged customer sales tracked automatically, so that I do not have to manually report them to receive credit.
- **Description:** Re-engaged customer sales should be tracked automatically when a BDR handles the call and makes the sale, instead of requiring the BDR to track those sales manually.
- **Acceptance Criteria:** 1. System identifies re-engaged customers based on the defined time frame, 2. BDR receives credit when they answer and sell to a re-engaged customer, 3. Re-engaged customer sales appear in the same reporting mechanism as new customer sales, 4. BDR does not need to manually track these sales in a separate Excel sheet, 5. Reporting supports visibility into credited re-engagement sales.
- **Timestamp:** Day 1, Part 1 [1:02:53 – 1:05:48]
- **Mockups:** NO MOCKUP
- **Notes:** The re-engagement period is one year for the BDR team. Re-engaged customer sales are currently tracked manually because the system does not automatically credit them as BDR sales.
- **Responsible:** TBD

## CUBE-PH4-D1-024
- **Group:** Service Tickets
- **Category:** Workflow
- **Epic:** Core Flow
- **Parent Task:** Manual Service Ticket Confirmation
- **Task Name:** Keep Manual Confirmation Before Service Ticket Creation
- **User Story:** As an Account Manager (AM), I want to manually review and confirm service ticket creation, so that I can catch mistakes before tickets and line items are created.
- **Description:** Manual confirmation gives users a chance to review key information and correct mistakes before service tickets and related line items are created.
- **Acceptance Criteria:** 1. User manually initiates service ticket creation, 2. User has a chance to review information before saving, 3. Manual review supports correction of pricing or setup errors, 4. System does not automatically create all tickets and line items without user confirmation, 5. User can identify mistakes before continuing the flow.
- **Timestamp:** Day 1, Part 1 [1:07:22 – 1:09:36]
- **Mockups:** NO MOCKUP
- **Notes:** Nichole states that users catch errors at this stage and that the manual step is necessary in her opinion.
- **Responsible:** TBD

## CUBE-PH4-D1-025
- **Group:** Line Items
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Applicable Line Item Buttons
- **Task Name:** Show Applicable Line Item Buttons Based on Ticket Type
- **User Story:** As an Account Manager (AM), I want the system to show applicable line item options based on the service ticket type, so that I can create only the line items relevant to that ticket.
- **Description:** Line item options are displayed based on the ticket code, allowing users to create the correct line item for the service ticket type.
- **Acceptance Criteria:** 1. Delivery ticket displays the delivery line item option, 2. Standard service ticket displays the applicable rental and service line item option, 3. Line item options are based on the ticket code, 4. Non-applicable line item options are not shown, 5. User can create the applicable line item from the service ticket.
- **Timestamp:** Day 1, Part 1 [1:09:40 – 1:11:41]
- **Notes:** The current line item buttons are individually programmed and could be improved later. Screenshot shows a delivery line item created from the service ticket flow.
- **Responsible:** TBD

## CUBE-PH4-D1-026
- **Group:** Line Items
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Per Unit Charges
- **Task Name:** Show Quantity for Per-Unit Delivery and Removal Charges
- **User Story:** As an Account Manager (AM), I want quantity information visible before creating delivery or removal line items, so that I can catch per-unit charge issues earlier.
- **Description:** Quantity should be visible before line item creation when delivery or removal is charged per unit, so users can verify the calculated amount before continuing.
- **Acceptance Criteria:** 1. User can see the quantity tied to per-unit delivery or removal, 2. System identifies when delivery or removal is charged per unit, 3. User can identify multiplied charges before creating the line item, 4. Quantity supports review of the calculated amount, 5. User does not need to go one level deeper to catch this issue.
- **Timestamp:** Day 1, Part 1 [1:11:41 – 1:13:21]
- **Notes:** The example mentions three toilets and a quantity of three. Screenshot shows quantity, line item amount, and total on the line item page.
- **Responsible:** TBD

## CUBE-PH4-D1-027
- **Group:** Line Items
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Discount Application
- **Task Name:** Apply Flat or Percentage Discount to Line Item
- **User Story:** As an Account Manager (AM), I want to apply flat or percentage discounts to a line item, so that the final item total reflects the discount given to the customer.
- **Description:** Flat or percentage discounts can be applied to a line item, and the final item total updates based on the selected discount type.
- **Acceptance Criteria:** 1. User can select a flat discount, 2. User can enter the flat discount amount, 3. User can select a percentage discount, 4. System updates the item total after the discount, 5. Discount information remains visible on the service ticket line item display.
- **Timestamp:** Day 1, Part 1 [1:13:21 – 1:15:26]
- **Notes:** The item total updates after the discount is applied. Screenshot shows the Discount Type dropdown with flat and percentage discount options.
- **Responsible:** TBD

## CUBE-PH4-D1-028
- **Group:** Line Items
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Line Item Review
- **Task Name:** Expose Important Line Item Review Information Before Save
- **User Story:** As an Account Manager (AM), I want important billing, pricing, quantity, address, and PO information visible before saving a line item, so that I can catch mistakes without opening hidden tabs.
- **Description:** Key billing, pricing, quantity, address, and PO details should be visible in a simple review area before the user saves the line item.
- **Acceptance Criteria:** 1. User can review pricing information before saving, 2. User can review quantity before saving, 3. User can review address or site information before saving, 4. User can review billing preference, tax exemption, and PO information before saving, 5. Important review information is visible without requiring the user to open multiple tabs.
- **Timestamp:** Day 1, Part 1 [1:17:17 – 1:20:57]
- **Notes:** The workshop describes this as a checklist or recap of important information that could be wrong. Screenshot shows billing details separated under the Billing Information tab.
- **Responsible:** TBD

## CUBE-PH4-D1-029
- **Group:** Line Items
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Line Item Status
- **Task Name:** Update Service Ticket Status After Line Item Creation
- **User Story:** As an Account Manager (AM), I want the service ticket billing status to update after a line item is created, so that I know the next required billing action.
- **Description:** After the required line item is created, the service ticket status should update from line item required to the next billing step, such as invoicing required.
- **Acceptance Criteria:** 1. Service ticket recognizes when the required line item exists, 2. Standard charge status updates after line item creation, 3. Status changes from line item required to invoicing required, 4. Related line item invoice status affects service ticket status, 5. Status supports dashboard visibility for AM billing work.
- **Timestamp:** Day 1, Part 1 [1:23:17 – 1:24:54]
- **Notes:** Granular statuses from line items feed operational reports and dashboards. Screenshot shows a created line item with invoice status still showing no invoice.
- **Responsible:** TBD

## CUBE-PH4-D1-030
- **Group:** Product Cancellation
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Product Cancellation
- **Task Name:** Cancel Product-Related Tickets and Line Items From Product Level
- **User Story:** As an Account Manager (AM), I want product cancellation to cancel related unbilled service tickets and line items, so that I do not have to manually cancel each child record.
- **Description:** Product cancellation should allow related unbilled service tickets and line items to be canceled from the product level when the selected cancellation option supports that behavior.
- **Acceptance Criteria:** 1. User can cancel related unbilled service tickets from the product level, 2. User can cancel related unbilled line items from the product level, 3. Cancellation reason selected at the product level applies to related records, 4. Billed items are not automatically credited by this cancellation action, 5. Dry run items can be excluded when the cancellation option requires it.
- **Timestamp:** Day 1, Part 1 [1:43:43 – 1:46:49]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop distinguishes between canceling everything and canceling everything except dry run charges.
- **Responsible:** TBD

## CUBE-PH4-D1-031
- **Group:** Credits
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Billing Reversal
- **Task Name:** Auto-Reverse Billed Items Through Credits
- **User Story:** As an Account Manager (AM), I want an easier billing reversal option for billed items, so that I do not have to manually create credits for every billed line item.
- **Description:** Billed items should be reversible through a simplified credit process that creates the needed credit line items and reduces manual reversal work.
- **Acceptance Criteria:** 1. User can initiate a reversal for billed items, 2. System creates credit line items for billed items that need reversal, 3. Reversal can support multiple line items, 4. Reversal reduces manual credit creation work, 5. User can still handle special cases manually when needed.
- **Timestamp:** Day 1, Part 1 [1:48:51 – 1:52:52]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop gives an example where many services across products may need cancellation or credit, making manual reversal time-consuming.
- **Responsible:** TBD

## CUBE-PH4-D1-032
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Variable Service Frequency
- **Task Name:** Support Flexible Service Frequency for Non-Standard Schedules
- **User Story:** As an Account Manager (AM), I want to handle variable service frequency within a service cycle, so that customers with changing weekly service needs do not require many separate extra service tickets and line items.
- **Description:** Variable service schedules should allow known non-standard service frequencies to be captured within a cycle, reducing the need to create multiple extra service tickets and line items for the same customer schedule.
- **Acceptance Criteria:** 1. User can document a non-standard service schedule, 2. User can account for a total number of services within a cycle, 3. User can avoid creating a separate ticket for every individual extra service when a flexible schedule is known up front, 4. Line item description can reflect the flexible schedule, 5. Customer-facing billing can remain simpler than multiple individual service charges.
- **Timestamp:** Day 1, Part 1 [1:53:44 – 2:00:00]
- **Mockups:** NO MOCKUP
- **Notes:** The example describes service increasing from once a week to multiple times a week as site headcount changes.
- **Responsible:** TBD

## CUBE-PH4-D1-033
- **Group:** Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Cycle Service Tickets
- **Task Name:** Create Standard Service Ticket Based on Cycle Dates
- **User Story:** As an Account Manager (AM), I want standard service tickets to use calculated cycle start and end dates, so that service cycles are created consistently from the delivery date and cycle time.
- **Description:** Standard service ticket dates are calculated from the delivery date and the selected cycle time, such as a 28-day service cycle for portable toilets.
- **Acceptance Criteria:** 1. Standard service ticket calculates the cycle start date, 2. Standard service ticket calculates the cycle end date, 3. Cycle dates use the delivery date and configured cycle time, 4. User cannot manually edit formula-based cycle dates in the same way as a single delivery date, 5. System can calculate the next cycle after each created service ticket.
- **Timestamp:** Day 1, Part 1 [2:03:03 – 2:10:20]
- **Mockups:** NO MOCKUP
- **Notes:** The example uses a 28-day portable toilet service cycle.
- **Responsible:** TBD

## CUBE-PH4-D1-034
- **Group:** Service Tickets
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Billing Cycle Preview
- **Task Name:** Show Future Billing Cycle Dates
- **User Story:** As an Account Manager (AM), I want to preview future billing cycle dates, so that I can provide customers with the expected billing cycle schedule without manually counting dates.
- **Description:** Future billing cycle dates should be available as a preview based on the delivery date and selected cycle time, without requiring the user to create all future service tickets.
- **Acceptance Criteria:** 1.User can view future billing cycle date ranges, 2. Cycle preview uses the delivery date, 3. Cycle preview uses the selected cycle time, 4. Preview updates when the billing cycle changes, 5. User can access the preview without creating all future service tickets.
- **Timestamp:** Day 1, Part 1 [2:11:14 – 2:15:15]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop suggests a clickable section similar to a call log where cycle dates can be viewed when needed.
- **Responsible:** TBD

## CUBE-PH4-D1-035
- **Group:** Removal Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Pre-Scheduled Removal
- **Task Name:** Create Removal Ticket When Removal Date Exists
- **User Story:** As an Account Manager (AM), I want to create a removal ticket when a removal date exists, so that pre-scheduled removals can be captured in the product flow.
- **Description:** A removal ticket can be created when a removal date is entered, allowing pre-scheduled removals to be captured even when future service tickets may still be required.
- **Acceptance Criteria:** 1. User can enter a removal date, 2. Removal ticket button becomes available when a removal date exists, 3. User can create a pre-scheduled removal ticket, 4. Removal ticket can exist before all intermediate service tickets are created, 5. Removal ticket date is used by the system when evaluating future service cycles.
- **Timestamp:** Day 1, Part 1 [2:16:31 – 2:18:47]
- **Notes:** The workshop clarifies this may be out of operational order but is supported by the system.
- **Responsible:** TBD

## CUBE-PH4-D1-036
- **Group:** Service Tickets
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Removal Stop Logic
- **Task Name:** Stop Automatic Service Cycles Based on Removal Date
- **User Story:** As an Account Manager (AM), I want the system to stop creating additional service cycles when the removal date falls within the current cycle, so that customers are not charged after the scheduled removal.
- **Description:** Automatic service cycle creation should stop when the scheduled removal date falls within the active or next applicable service cycle.
- **Acceptance Criteria:** 1. System evaluates the removal date against the current service cycle, 2. System continues creating cycles until the removal date is reached, 3. System stops creating future service cycles when the removal date falls within the cycle, 4. System prevents charging the customer beyond the scheduled removal point, 5. Canceling the removal ticket and removal date allows future service ticket creation again.
- **Timestamp:** Day 1, Part 1 [2:19:11 – 2:23:01]
- **Notes:** The removal ticket gives automations a stopping place. Screenshot shows a rental and service ticket with cycle start and end dates used in the service cycle flow.
- **Responsible:** TBD

## CUBE-PH4-D1-037
- **Group:** Extra Service Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Ad Hoc Extra Service
- **Task Name:** Create Extra Service Ticket With Manual Service Date
- **User Story:** As an Account Manager (AM), I want to create an ad hoc extra service ticket with a manually entered service date, so that customer-requested additional services can be billed and tracked.
- **Description:** Extra service tickets are used for ad hoc services that are not part of the standard delivery, removal, or recurring service cycle, so the service date must be entered manually.
- **Acceptance Criteria:** 1. Extra service button becomes available when a service rate exists, 2. User can manually enter the extra service date, 3. User can enter dispatch information for the extra service, 4. Extra service ticket uses the extra service ticket code, 5. Extra service line item becomes available from the extra service ticket.
- **Timestamp:** Day 1, Part 1 [2:23:01 – 2:24:50]
- **Notes:** The example describes an additional cleaning outside the included weekly service. Screenshot shows the Extra Service button available in the Create Service Ticket section.
- **Responsible:** TBD

## CUBE-PH4-D1-038
- **Group:** Damage Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Damage Charges
- **Task Name:** Create Damage Ticket With Manual Hauler and Customer Charges
- **User Story:** As an Account Manager (AM), I want to create a damage ticket with manually entered hauler and customer charges, so that non-standard damage costs can be captured and billed.
- **Description:** Damage tickets are used for non-standard damage charges that are not captured in the regular product rates, so hauler and customer charges must be entered manually.
- **Acceptance Criteria:** 1. User can create a damage ticket, 2. User can enter the hauler charge for the damage, 3. User can enter the customer charge for the damage, 4. User can describe the damage or problem, 5. User can enter the date the damage was reported.
- **Timestamp:** Day 1, Part 1 [2:25:45 – 2:28:40]
- **Notes:** Examples include a burned toilet or removed hand sanitizer. Screenshot shows the Damage ticket code and non-recurring charge fields.
- **Responsible:** TBD

## CUBE-PH4-D1-039
- **Group:** Damage Tickets
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Rental Protection Reminder
- **Task Name:** Show Rental Protection Context on Damage Tickets
- **User Story:** As an Account Manager (AM), I want damage tickets to show whether the customer has portable toilet rental protection, so that I know whether the customer charge should be waived or whether the protection program can be offered.
- **Description:** Damage tickets should show whether the customer has rental protection, helping the user determine whether the customer charge applies or whether the protection program should be mentioned.
- **Acceptance Criteria:** 1. Damage ticket shows whether the customer has rental protection, 2. System reminds the user when the customer charge should be zero because protection exists, 3. System shows when protection is not active, 4. User can use the rental protection context when discussing damage charges with the customer, 5. Damage ticket supports the damage charge workflow with rental protection visibility.
- **Timestamp:** Day 1, Part 1 [2:28:58 – 2:31:13]
- **Mockups:** NO MOCKUP
- **Notes:** Damage charges may be an opportunity to mention the protection program when the customer is not already enrolled.
- **Responsible:** TBD

## CUBE-PH4-D1-040
- **Group:** Miscellaneous Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Miscellaneous Charges
- **Task Name:** Create Miscellaneous Ticket for Ad Hoc Charges
- **User Story:** As an Account Manager (AM), I want to create miscellaneous tickets for ad hoc charges, so that charges that do not fit standard ticket types can still be captured.
- **Description:** Miscellaneous tickets are used for flexible, ad hoc charges that do not fit another standard ticket type.
- **Acceptance Criteria:** 1. User can create a miscellaneous ticket, 2. User can enter the applicable charge information, 3. User can describe the miscellaneous reason or context, 4. User can create one or more miscellaneous line items from the ticket, 5. Miscellaneous ticket supports ad hoc cases without requiring a predefined type list.
- **Timestamp:** Day 1, Part 1 [2:31:13 – 2:34:48]
- **Mockups:** NO MOCKUP
- **Notes:** Standby fees are mentioned as a common miscellaneous use case.
- **Responsible:** TBD

## CUBE-PH4-D1-041
- **Group:** Dry Run Tickets
- **Category:** Data Validation
- **Epic:** Core Flow
- **Parent Task:** Dry Run Reason
- **Task Name:** Require Dry Run Reason on Dry Run Ticket
- **User Story:** As an Account Manager (AM), I want the dry run reason to be required, so that every dry run charge has a clear explanation.
- **Description:** Dry run tickets should require a dry run reason before saving, so each dry run charge has a documented explanation.
- **Acceptance Criteria:** 1. Dry run ticket includes a dry run reason field, 2. Dry run reason is required before saving, 3. User cannot create a dry run charge without selecting a reason, 4. Dry run reason appears in the line item description when applicable, 5. Dry run reason supports reporting and customer invoice clarity.
- **Timestamp:** Day 1, Part 1 [2:38:45 – 2:44:50]
- **Notes:** The workshop also mentions reviewing the dry run reason list. Screenshot shows the available dry run reason options.
- **Responsible:** TBD

## CUBE-PH4-D1-042
- **Group:** Relocation Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Relocation Charges
- **Task Name:** Create Relocation Ticket and Line Item
- **User Story:** As an Account Manager (AM), I want to create a relocation ticket and relocation line item, so that customer-requested unit moves can be billed and tracked.
- **Description:** Relocation tickets are used when a customer requests a unit to be moved from one location to another, and the related relocation charges need to be captured.
- **Acceptance Criteria:** 1. User can create a relocation ticket, 2. User can enter the hauler relocation fee, 3. User can enter the customer relocation fee, 4. System uses the relocation ticket code from the button, 5. Relocation line item becomes available from the relocation ticket.
- **Timestamp:** Day 1, Part 1 [2:45:00 – 2:46:12]
- **Mockups:** NO MOCKUP
- **Notes:** The example given is moving a unit from one side of the property to another.
- **Responsible:** TBD

## CUBE-PH4-D1-043
- **Group:** Roll-Offs
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Rental Pricing Visibility
- **Task Name:** Show Roll-Off Rental Pricing Details on Ticket
- **User Story:** As an Account Manager (AM), I want roll-off rental pricing details visible on the ticket, so that I can understand what rental period and rate are being billed.
- **Description:** Roll-off rental pricing details such as days included, rental rate, rental interval, and rental period should be visible on the ticket so the user can confirm what is being billed.
- **Acceptance Criteria:** 1. Ticket displays days included, 2. Ticket displays rental rate, 3. Ticket displays rental interval, 4. Ticket displays rental period, 5. User can review rental pricing details without navigating away from the ticket.
- **Timestamp:** Day 1, Part 1 [2:47:22 – 2:51:25]
- **Mockups:** NO MOCKUP
- **Notes:** The example involves a block rental and confusion around the rental period being billed.
- **Responsible:** TBD

## CUBE-PH4-D1-044
- **Group:** Invoices
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Invoice Creation Navigation
- **Task Name:** Provide Direct Create Invoice Link From Applicable Records
- **User Story:** As an Account Manager (AM), I want a direct Create Invoice link from the applicable record, so that I can open the correct invoice creation flow without selecting the wrong customer or site.
- **Description:** A direct Create Invoice link should be available from the relevant record so users can access the correct invoice creation flow without manually searching for the customer or site.
- **Acceptance Criteria:** 1. Applicable records provide a direct Create Invoice action, 2. Direct link opens invoice creation for the correct customer context, 3. Direct link reduces manual searching or filtering, 4. Direct link helps prevent selecting the wrong customer, 5. User can create the invoice from the relevant line item, service ticket, or product context.
- **Timestamp:** Day 1, Part 1 [2:51:54 – 2:54:13]
- **Mockups:** NO MOCKUP
- **Notes:** The missing button demonstrated its value when the wrong customer was selected during the workflow.
- **Responsible:** TBD

## CUBE-PH4-D1-045
- **Group:** Invoices
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Site-Level Billing
- **Task Name:** Group Billable Line Items by Site and PO
- **User Story:** As an Account Manager (AM), I want billable line items grouped by site and PO, so that invoices reflect site-level tax requirements and customer billing structure.
- **Description:** Billable line items are grouped by site because taxes depend on the site address, and PO differences can also separate invoice groups.
- **Acceptance Criteria:** 1. Invoice creation groups billable line items by site, 2. Site grouping supports tax jurisdiction requirements, 3. Different sites appear as separate billing groups, 4. PO differences can separate billing, 5. User can review billable line items within each site or PO group.
- **Timestamp:** Day 1, Part 1 [2:54:13 – 2:56:32]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop mentions multiple sites for the same customer and PO-based grouping.
- **Responsible:** TBD

## CUBE-PH4-D1-046
- **Group:** Invoices
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Invoice Payment Options
- **Task Name:** Select Invoice Creation and Payment Submission Option
- **User Story:** As an Account Manager (AM), I want to choose whether to create an invoice only, create an invoice with partial payment, or create an invoice with full payment, so that I can match the customer’s billing situation.
- **Description:** HUB provides options to create an invoice only, create an invoice with partial payment, or create an invoice with full payment.
- **Acceptance Criteria:** 1. User can create an invoice without submitting payment, 2. User can create an invoice and submit partial payment, 3. User can create an invoice and submit full payment, 4. User can use invoice-only option when payment should not be submitted immediately, 5. User can use full payment option for the majority of standard cases.
- **Timestamp:** Day 1, Part 1 [2:56:32 – 2:57:54]
- **Notes:** Screenshot is from HUB and shows the invoice payment options available after billable line items are selected. Batch payment is mentioned as one reason to create invoices without assigning payment immediately.
- **Responsible:** TBD

## CUBE-PH4-D1-047
- **Group:** Invoices
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Declined Payment Tracking
- **Task Name:** Track Declined Payment Transaction on Invoice
- **User Story:** As an Account Manager (AM), I want declined payment transactions recorded on the invoice, so that I can see when an invoice was created but payment failed.
- **Description:** When a payment is declined after invoice creation, the invoice remains created and the declined transaction is recorded for tracking.
- **Acceptance Criteria:** 1. System creates the invoice even when payment is declined, 2. Invoice status reflects unpaid when payment fails, 3. Rejected transaction is attached to the invoice, 4. User can access transaction status from the invoice context, 5. Related line items show invoice and payment status changes.
- **Timestamp:** Day 1, Part 1 [2:57:54 – 3:00:54]
- **Mockups:** NO MOCKUP
- **Notes:** The declined transaction record comes from the HUB invoicing process. If you attach the HUB screenshot for this story, mention that the payment attempt happens in HUB while the resulting invoice and transaction status are reflected back in the related invoice/line item flow.
- **Responsible:** TBD

## CUBE-PH4-D1-048
- **Group:** Credits
- **Category:** Data Validation
- **Epic:** Core Flow
- **Parent Task:** Credit Eligibility
- **Task Name:** Lock Credit Creation After 180 Days
- **User Story:** As an Account Manager (AM), I want credit creation locked after the allowed dispute period, so that old billed items cannot be credited back without the required control.
- **Description:** Credit creation should be locked for billed items older than 180 days, preventing regular users from crediting charges outside the allowed billing dispute window.
- **Acceptance Criteria:** 1. System checks invoice or line item age before allowing credit, 2. Credit button is not available for items older than 180 days, 3. User cannot credit old items without the required approval path, 4. Recent billed line items remain eligible for credit, 5. Lockout supports the six-month billing dispute rule described in the workshop.
- **Timestamp:** Day 1, Part 1 [3:03:59 – 3:06:33]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop uses an old service ticket example to show that the credit button is not available. The 180-day rule is also shown in the HUB billing flow message.
- **Responsible:** TBD

## CUBE-PH4-D1-049
- **Group:** Credits
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Credit Line Items
- **Task Name:** Create Credit Line Item Against Billed Line Item
- **User Story:** As an Account Manager (AM), I want to create a credit line item against a billed line item, so that the original charge can be partially or fully reversed.
- **Description:** Credit line items are created against eligible billed line items and act as negative records used to reverse the original charge.
- **Acceptance Criteria:** 1. User can access the credit action from an eligible billed line item, 2. System creates a credit line item tied to the original line item, 3. Credit line item can represent a full credit, partial credit, or tax-only credit, 4. Credit line item follows a different path than a regular line item, 5. Credit line item supports creation of a credit memo later.
- **Timestamp:** Day 1, Part 1 [3:06:33 – 3:09:19]
- **Mockups:** NO MOCKUP
- **Notes:** The credit memo works as the reverse of an invoice, using credit line items instead of regular line items.
- **Responsible:** TBD

## CUBE-PH4-D1-050
- **Group:** Credits
- **Category:** Data Validation
- **Epic:** Core Flow
- **Parent Task:** Credit Amount Validation
- **Task Name:** Prevent Credit Amount From Exceeding Original Charge
- **User Story:** As an Account Manager (AM), I want the system to prevent credits greater than the original line item amount, so that credit calculations cannot exceed what was charged.
- **Description:** Credit amounts should be validated against the maximum available credit for the line item, preventing users from crediting more than the original billed amount.
- **Acceptance Criteria:** 1. System displays the maximum credit available for the line item, 2. User cannot enter a credit amount greater than the original charge, 3. System accounts for prior credits when calculating remaining credit, 4. Credit total counts down from the original line item amount, 5. Validation prevents incorrect credit math.
- **Timestamp:** Day 1, Part 1 [3:09:38 – 3:10:59]
- **Notes:** The system should not allow giving back more than was charged. Screenshot shows the maximum credit amount and credit type options.
- **Responsible:** TBD

## CUBE-PH4-D1-051
- **Group:** Credits
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Credit Calculator
- **Task Name:** Use Credit Calculator for Percentage, Flat, or Tax Credit
- **User Story:** As an Account Manager (AM), I want a credit calculator available when creating a credit, so that I can calculate percentage, flat, or tax-related credit values.
- **Description:** The credit calculator helps users calculate credit subtotal, tax, and total values using percentage or dollar-based inputs.
- **Acceptance Criteria:** 1. User can calculate credit based on a percentage, 2. User can calculate credit based on a dollar amount, 3. Calculator can show the calculated credit subtotal, 4. Calculator can show calculated credit tax, 5. Calculator can show the calculated credit total before saving.
- **Timestamp:** Day 1, Part 1 [3:11:03 – 3:12:55]
- **Notes:** Nichole did not know the calculator was available, so visibility or training may be needed. Screenshot shows the Credit Calculator section with Percent and Dollar options.
- **Responsible:** TBD

## CUBE-PH4-D1-052
- **Group:** Credits
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Credit Calculator Visibility
- **Task Name:** Make Credit Calculator More Visible
- **User Story:** As an Account Manager (AM), I want the credit calculator to be visible without needing to expand a hidden section, so that I can easily use it when creating credits.
- **Description:** The credit calculator should be visible in the credit creation flow instead of being hidden by default, so users can find and use it when calculating credits.
- **Acceptance Criteria:** 1. Credit calculator is visible in the credit creation flow, 2. User does not need to expand a hidden section to find the calculator, 3. Calculator remains available when creating credit line items, 4. Calculator supports users who need help calculating credits, 5. Visibility reduces missed use of an existing feature.
- **Timestamp:** Day 1, Part 2 [0:00:18 – 0:02:50]
- **Notes:** Nichole confirmed that other users also did not know the credit calculator existed. Screenshot shows the calculator expanded and visible in the credit flow.
- **Responsible:** TBD

## CUBE-PH4-D1-053
- **Group:** Credits
- **Category:** Workflow
- **Epic:** Core Flow
- **Parent Task:** CSS Credit Approval
- **Task Name:** Notify CSS When Credit Approval Is Needed
- **User Story:** As a Customer Support Specialist (CSS), I want to receive a system notification when a credit requires approval, so that I can approve credits without relying on email.
- **Description:** Credit approval requests should generate an in-system notification for CSS users instead of relying on email communication.
- **Acceptance Criteria:** 1. System notifies CSS when a credit requires approval, 2. Notification appears inside CUBE instead of relying only on email, 3. CSS can identify the credit line item that needs approval, 4. Approval request is tied to the credit workflow, 5. Notification reduces dependency on manual email communication.
- **Timestamp:** Day 1, Part 2 [0:03:05 – 0:04:03]
- **Mockups:** NO MOCKUP
- **Notes:** The current approval process is handled through email. Justin identifies an in-system CUBE notification as the preferred improvement.
- **Responsible:** TBD

## CUBE-PH4-D1-054
- **Group:** Credits
- **Category:** Permissions
- **Epic:** Core Flow
- **Parent Task:** Credit Memo Processing
- **Task Name:** Allow AM to Process Credit Memo After CSS Approval
- **User Story:** As an Account Manager (AM), I want to process the credit memo after CSS approval, so that I can complete the customer-specific credit workflow without handing the action back to CSS.
- **Description:** After CSS approves a credit, the AM should be able to process the related credit memo instead of requiring CSS to complete both the approval and processing steps.
- **Acceptance Criteria:** 1. CSS approval remains required before credit memo processing, 2. Approved credit becomes available for AM processing, 3. AM can process the credit memo after approval, 4. CSS is not required to perform both approval and processing, 5. Workflow supports customer-specific handling such as whether to send the credit memo.
- **Timestamp:** Day 1, Part 2 [0:07:27 – 0:08:24]
- **Mockups:** NO MOCKUP
- **Notes:** Nichole mentions Tesla as an example where the AM needs control over how credit memos are handled.
- **Responsible:** TBD

## CUBE-PH4-D1-055
- **Group:** Containers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Container Accessories
- **Task Name:** Capture Storage Container Lock as an Accessory
- **User Story:** As an Account Manager (AM), I want storage container locks captured as accessories, so that common lock requests can be documented when quoting or managing storage containers.
- **Description:** Storage container locks are commonly requested and should be captured as accessories, while any one-time or recurring cost handling can be reviewed as part of the product setup.
- **Acceptance Criteria:** 1. User can capture a lock as a storage container accessory, 2. Lock accessory can support common customer requests, 3. Accessory information remains tied to the storage container product, 4. Lock cost handling can support one-time or recurring pricing when applicable, 5. Accessory capture does not change the standard ticket and line item flow.
- **Timestamp:** Day 1, Part 2 [0:23:49 – 0:26:25]
- **Mockups:** NO MOCKUP
- **Notes:** Locks are common for storage containers, but the workshop does not confirm whether lock charges should be broken out separately on invoices.
- **Responsible:** TBD

## CUBE-PH4-D1-056
- **Group:** Fencing
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Secondary Cycle Time
- **Task Name:** Calculate Fencing Service Cycles Using Primary and Secondary Cycle Times
- **User Story:** As an Account Manager (AM), I want fencing service tickets to calculate dates using primary and secondary cycle times, so that long-term fencing rentals can follow the correct billing cadence.
- **Description:** Fencing rentals can use an initial long cycle, such as 24 months, followed by shorter secondary cycles, such as one year or one month.
- **Acceptance Criteria:** 1. First fencing service cycle uses the primary cycle time, 2. Subsequent fencing service cycles use the secondary cycle time, 3. System calculates next cycle dates from the prior cycle end date, 4. Secondary cycle dates update when the secondary cycle time changes, 5. Service ticket creation uses the correct cycle cadence for fencing.
- **Timestamp:** Day 1, Part 2 [0:30:14 – 0:36:25]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop identifies the current monthly service label as poorly labeled for cycle-based billing.
- **Responsible:** TBD

## CUBE-PH4-D1-057
- **Group:** Fencing
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Secondary Rental Rate
- **Task Name:** Use Secondary Rental Rate for Fencing Secondary Cycles
- **User Story:** As an Account Manager (AM), I want secondary fencing cycles to use the secondary rental rate, so that line items and expected hauler costs match the correct cycle pricing.
- **Description:** After the first fencing service cycle, subsequent cycles should use the secondary rental rate and the corresponding secondary hauler cost for line items and item receipt calculations.
- **Acceptance Criteria:** 1. First fencing cycle uses the standard rate, 2. Subsequent fencing cycles use the secondary rental rate, 3. Secondary rental rate is available on the service ticket pricing information, 4. Expected hauler cost uses the correct secondary rate, 5. Item receipt calculation reflects the correct secondary cycle cost.
- **Timestamp:** Day 1, Part 2 [0:36:25 – 0:39:13]
- **Mockups:** NO MOCKUP
- **Notes:** Justin identifies the incorrect secondary cycle expected hauler cost as a back-end correction needed for item receipts.
- **Responsible:** TBD

## CUBE-PH4-D1-058
- **Group:** Equipment Rentals
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Equipment Rental Rate Cycles
- **Task Name:** Review Daily Weekly and Monthly Rate Handling for Equipment Rentals
- **User Story:** As an Account Manager (AM), I want equipment rentals to support daily, weekly, and monthly rate considerations, so that rental charges can reflect how equipment providers bill beyond the initial rental period.
- **Description:** Equipment rentals may include daily, weekly, and monthly rates, so the system should account for how providers charge when rentals extend beyond the initial rental period.
- **Acceptance Criteria:** 1. Equipment rental product can account for daily rate information, 2. Equipment rental product can account for weekly rate information, 3. Equipment rental product can account for monthly rate information, 4. Extended rental periods can be evaluated against provider billing behavior, 5. Internal discussion determines whether secondary cycle or prorated handling is needed.
- **Timestamp:** Day 1, Part 2 [0:44:41 – 0:47:17]
- **Mockups:** NO MOCKUP
- **Notes:** Nichole agreed to make this an internal discussion point before confirming the improvement priority.
- **Responsible:** TBD

---

# Day 2

**Stories:** 61

## CUBE-PH4-D2-001
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Create Roll-Off Delivery Ticket
- **User Story:** As an Account Manager (AM), I want to create a roll-off delivery ticket with the required ticket code, dispatching information, and drop/start date, so that the roll-off can be delivered before the haul occurs.
- **Description:** Roll-offs are on-call services where the roll-off is delivered before the actual haul occurs. The delivery ticket captures the initial setup information, including the ticket code, dispatching details, and the drop/start date used to place the roll-off on site.
- **Acceptance Criteria:** 1. User can create a delivery ticket for a roll-off, 2. User can enter the required ticket code, 3. User can enter dispatching information, 4. User can enter a drop/start date for the roll-off delivery, 5. The delivery ticket can be saved before the related haul occurs.
- **Timestamp:** Day 2, Part 1 [10:23 – 11:23]
- **Notes:** Delivery/drop setup is the first part of the roll-off ticket chain. Rental, tonnage, weight ticket, haul completion, and removal behavior are handled in later roll-off stories.
- **Responsible:** TBD

## CUBE-PH4-D2-002
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Create Incomplete Roll-Off Haul Ticket
- **User Story:** As an Account Manager (AM), I want to create a roll-off haul ticket that can remain open until the haul physically occurs, so that the system can track pending on-call service activity.
- **Description:** After the roll-off is delivered, the haul ticket can remain open because the dumpster may still be on site and the haul may not have physically occurred yet. The ticket acts as a placeholder for the expected haul activity until the required completion details are available.
- **Acceptance Criteria:** 1. User can create a haul ticket after the delivery ticket, 2. Haul ticket can remain open while the dumpster is still on site, 3. System supports dispatch-related information for the pending haul, 4. System does not treat the haul ticket as complete until required haul details are entered, 5. Ticket can be updated later when the haul activity occurs.
- **Timestamp:** Day 2, Part 1 [11:23 – 12:36]
- **Notes:** Roll-off haul tickets differ from most standard service tickets because they may remain open for an extended period. The haul ticket is not necessarily completed at the time it is created.
- **Responsible:** TBD

## CUBE-PH4-D2-003
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Line Items
- **Task Name:** Track Rental and Tonnage on Roll-Off Hauls
- **User Story:** As an Account Manager (AM), I want roll-off haul tickets to track rental duration and tonnage usage, so that additional rental or tonnage charges can be billed when applicable.
- **Description:** Roll-off haul tickets can require additional billing when the dumpster remains on site longer than the included rental period or when the final tonnage exceeds the included tonnage. The haul ticket must support rental and tonnage tracking so that additional billable line items can be added when needed.
- **Acceptance Criteria:** 1. System tracks the rental period included for the roll-off haul, 2. System identifies when additional rental is required, 3. System tracks the tonnage included for the roll-off haul, 4. System supports final tonnage entry after the haul occurs, 5. System identifies when additional tonnage is required, 6. Additional rental and tonnage can be represented as billable line items.
- **Timestamp:** Day 2, Part 1 [12:36 – 14:52]
- **Notes:** Additional rental and tonnage may not be known when the haul ticket is first created. These values can be completed later after the haul occurs and the required rental or weight ticket information is available.
- **Responsible:** TBD

## CUBE-PH4-D2-004
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Capture Weight Ticket Information After Haul
- **User Story:** As an Account Manager (AM), I want to attach weight ticket information and enter final tonnage after a roll-off haul, so that the system can determine whether additional tonnage should be billed.
- **Description:** Weight ticket information is expected after the roll-off has been hauled. Once the haul occurs, the user can attach the weight ticket and enter the final tonnage so the system can compare it against the included tonnage and identify any additional tonnage charges.
- **Acceptance Criteria:** 1. User can enter the haul date after the roll-off is hauled, 2. User can attach weight ticket information, 3. User can enter final tonnage, 4. System compares final tonnage against the included tonnage, 5. System identifies whether additional tonnage should be billed.
- **Timestamp:** Day 2, Part 1 [14:26 – 15:03]
- **Mockups:** NO MOCKUP
- **Notes:** Weight ticket information is not available until after the haul occurs. This story should stay separate from the broader rental and tonnage tracking story because it focuses specifically on the supporting document and final tonnage entry.
- **Responsible:** TBD

## CUBE-PH4-D2-005
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Align Final Haul Date with Removal Date
- **User Story:** As an Account Manager (AM), I want the final roll-off haul date to align with the removal date when the dumpster is not returned, so that the system reflects the final haul as the physical removal activity.
- **Description:** When the customer confirms that the dumpster should not be returned after the haul, the final haul date and the removal date represent the same physical activity. In this scenario, the hauler removes the dumpster during the final haul instead of returning it to the site.
- **Acceptance Criteria:** 1. User can identify when a roll-off haul is the final haul, 2. User can enter a final haul date, 3. User can enter a removal date that matches the final haul date, 4. System treats the final haul as the physical removal activity, 5. System distinguishes the removal ticket from the physical removal action.
- **Timestamp:** Day 2, Part 1 [15:03 – 17:34]
- **Mockups:** NO MOCKUP
- **Notes:** The removal ticket acts as a bookend for the roll-off service chain. It confirms that no additional hauls are expected after rental, tonnage, and weight ticket details are completed.
- **Responsible:** TBD

## CUBE-PH4-D2-006
- **Group:** Roll-Offs
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Keep Roll-Off Haul Open Until Follow-Up Ticket Is Expected
- **User Story:** As an Account Manager (AM), I want a roll-off haul ticket to remain open until rental, tonnage, and follow-up ticket requirements are completed, so that unresolved billing or service activity is not missed.
- **Description:** Roll-off haul tickets can remain open for weeks or months because the next haul may not occur immediately and required details, such as weight tickets, final tonnage, or additional rental, may be completed later. The haul ticket should remain incomplete until the required information is resolved and the next expected ticket, such as another haul or a removal ticket, can be handled.
- **Acceptance Criteria:** 1. Haul ticket can remain open after initial entry, 2. System supports long-running roll-off haul tickets, 3. System allows rental and tonnage details to be added after the ticket is created, 4. System keeps the haul ticket incomplete until required billing or service details are resolved, 5. System supports continuation to the next expected ticket, such as another haul or a removal ticket.
- **Timestamp:** Day 2, Part 1 [18:09 – 20:20]
- **Mockups:** NO MOCKUP
- **Notes:** Roll-off haul tickets are different from most standard service tickets because they are not always completed at the time of entry. They may remain open until the next haul occurs and all rental, tonnage, and weight ticket details are accounted for.
- **Responsible:** TBD

## CUBE-PH4-D2-007
- **Group:** Roll-Offs
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Create Next Haul Based on Previous Haul Date
- **User Story:** As an Account Manager (AM), I want the system to create the next roll-off haul ticket when the previous haul date is entered and no removal date exists, so that ongoing roll-off service activity can continue.
- **Description:** When a roll-off haul date is entered and the product does not have a removal date, the system creates another haul ticket because the dumpster remains active and additional haul activity may still be needed. If the haul date matches the removal date, the system can make the removal ticket option available.
- **Acceptance Criteria:** 1. System checks whether the previous haul date is entered, 2. System checks whether the roll-off product has a removal date, 3. System creates another haul ticket when the haul date exists and no removal date exists, 4. System supports continued roll-off haul activity, 5. System can make the removal ticket option available when the haul date matches the removal date.
- **Timestamp:** Day 2, Part 1 [20:23 – 21:04]
- **Mockups:** NO MOCKUP
- **Notes:** This story defines the ticket-chain behavior for ongoing roll-off service. A new haul ticket should only be available when the previous haul activity has enough date information to continue the chain.
- **Responsible:** TBD

## CUBE-PH4-D2-008
- **Group:** Roll-Offs
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Block Next Haul When Previous Haul Date Is Missing
- **User Story:** As an Account Manager (AM), I want the system to prevent another roll-off haul ticket when the previous haul date is missing, so that incomplete haul activity cannot be bypassed.
- **Description:** A new roll-off haul ticket cannot be created when the previous haul ticket does not have a haul date. Without the haul date, the current service is still considered incomplete because the system does not have the end date for the last haul.
- **Acceptance Criteria:** 1. System validates whether the previous haul date is present, 2. System blocks another haul ticket when the previous haul date is missing, 3. System identifies that there is no end date for the last haul, 4. System treats the current haul as incomplete, 5. User cannot continue the roll-off haul chain until the missing haul date is entered.
- **Timestamp:** Day 2, Part 1 [21:04 – 22:05]
- **Mockups:** NO MOCKUP
- **Notes:** This validation prevents users from creating another haul while the current haul is still open-ended. In the transcript, the system message shown for this condition is “No end date for last haul.”
- **Responsible:** TBD

## CUBE-PH4-D2-009
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Dispatching
- **Task Name:** Show Service Date Required for Open Haul
- **User Story:** As an Account Manager (AM), I want the dispatch status to show “Service Date Required” when a roll-off haul date is missing, so that I can identify haul tickets that have not been dispatched yet.
- **Description:** A roll-off haul is not technically dispatched until the haul date is entered, because the physical hauling activity happens at the end of the on-call service. When the haul date is missing, the system should show the dispatch status as “Service Date Required.”
- **Acceptance Criteria:** 1. System checks whether the haul date is missing, 2. System displays “Service Date Required” as the dispatch status when the haul date is missing, 3. System treats the haul as not technically dispatched until the haul date is entered, 4. System keeps the ticket open while the dumpster is still on site, 5. User can identify open haul tickets that still need a service date.
- **Timestamp:** Day 2, Part 1 [22:05 – 23:01]
- **Mockups:** NO MOCKUP
- **Notes:** This status supports the roll-off on-call workflow. The haul ticket may exist as a placeholder while the dumpster remains on site, but dispatch is not complete until the actual haul date is entered.
- **Responsible:** TBD

## CUBE-PH4-D2-010
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Pricing
- **Task Name:** Calculate Standard Charge Using Rental and Tonnage Delta
- **User Story:** As an Account Manager (AM), I want the system to calculate the roll-off standard charge using included rental days, included tons, hauler rates, and margin, so that the suggested customer price reflects the offered roll-off package.
- **Description:** Roll-off standard charges are calculated by comparing what the hauler includes with what ZTERS offers to the customer. The system uses values such as included rental days, included tons, rental rates, disposal rates, and margin to calculate the suggested customer price.
- **Acceptance Criteria:** 1. System supports included rental days, 2. System supports included tons, 3. System supports hauler rental and disposal rate values, 4. System calculates the difference between hauler-included values and customer-included values when applicable, 5. System applies margin to calculate the suggested customer price, 6. Suggested price fields display the calculated roll-off package values.
- **Timestamp:** Day 2, Part 1 [23:01 – 25:48]
- **Notes:** This story covers the initial suggested price calculation for the roll-off package. Later rental or tonnage overages are handled separately when the haul is completed and actual rental or weight ticket information is available.
- **Responsible:** TBD

## CUBE-PH4-D2-011
- **Group:** Roll-Offs
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Pricing
- **Task Name:** Allow Deviations from Standard Roll-Off Package
- **User Story:** As an Account Manager (AM), I want to adjust included rental days and included tons for roll-off pricing, so that the quoted package can match the service provider terms or the customer’s specific service needs.
- **Description:** Roll-off pricing does not always follow the standard package. Included rental days and included tons may be adjusted when the service provider offers different terms, when the customer needs a longer rental period, or when the material type requires a different tonnage setup, such as concrete dumpsters.
- **Acceptance Criteria:** 1. User can adjust included rental days, 2. User can adjust included tons, 3. System supports matching the service provider’s included rental or tonnage values, 4. System supports customer-specific scenarios such as longer rental periods, 5. System recalculates suggested pricing and margin based on the adjusted package values.
- **Timestamp:** Day 2, Part 1 [25:54 – 27:47]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop gives examples where ZTERS may deviate from the standard package, including concrete dumpsters, customer requests for 30 days, and cases where service providers include more rental days or more tons than the default package.
- **Responsible:** TBD

## CUBE-PH4-D2-012
- **Group:** Roll-Offs
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Create Removal Ticket to Close Roll-Off Chain
- **User Story:** As an Account Manager (AM), I want to create a removal ticket after the final removal date is entered, so that the roll-off service chain can be closed.
- **Description:** A removal ticket becomes available after the final removal date is entered. For roll-offs, the removal ticket closes out the dumpster service chain and confirms that no additional core haul activity is expected after the final haul/removal process is completed.
- **Acceptance Criteria:** 1. User can enter the final removal date, 2. System checks whether the last haul has an end date, 3. System makes the removal ticket available when the required date conditions are met, 4. User can create the removal ticket, 5. Removal ticket closes the roll-off service chain.
- **Timestamp:** Day 2, Part 1 [28:43 – 30:10]
- **Notes:** The screenshot shows the blocking state before removal ticket creation, where the system still displays “No Removal Date” and “No End Date for Last Haul.” The removal ticket should only become available after the required final removal and last haul date conditions are satisfied.
- **Responsible:** TBD

## CUBE-PH4-D2-013
- **Group:** Roll-Offs
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Prevent Standard Service Tickets After Removal Ticket
- **User Story:** As an Account Manager (AM), I want the system to prevent additional standard roll-off service tickets after a removal ticket is created, so that no core haul activity can continue after the roll-off service chain is closed.
- **Description:** After the removal ticket is created, the roll-off service chain is considered closed. The system should prevent users from creating additional standard haul tickets after removal, while still allowing non-core/ad hoc ticket types when applicable, such as damage or miscellaneous tickets.
- **Acceptance Criteria:** 1. System allows another haul on the same day before the removal ticket is created, 2. System prevents additional standard haul tickets after the removal ticket is created, 3. System treats the removal ticket as the closing record for the roll-off chain, 4. System allows only applicable non-core/ad hoc ticket types after removal, 5. User cannot continue the standard roll-off service chain after removal.
- **Timestamp:** Day 2, Part 1 [30:28 – 31:34]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript clarifies that matching the haul date and removal date does not automatically block another haul ticket. The restriction starts after the removal ticket is created. After that, only ad hoc ticket types such as damage or miscellaneous remain available.
- **Responsible:** TBD

## CUBE-PH4-D2-014
- **Group:** Billing
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Invoicing
- **Task Name:** Create Invoice from Line Items
- **User Story:** As an Account Manager (AM), I want invoices to be created from service ticket line items, so that customer invoices reflect the actual billable charges instead of the service ticket record itself.
- **Description:** Invoices are created from the line items attached to service tickets. The service ticket provides supporting information for the invoicing process, but the invoice itself is made up of the related billable line items.
- **Acceptance Criteria:** 1. Invoice is created from service ticket line items, 2. Service ticket can have one or more billable line items, 3. Service ticket information is available during the invoicing process, 4. Invoice total is based on the related line items, 5. Invoice creation remains part of the Hub process.
- **Timestamp:** Day 2, Part 1 [31:46 – 34:24]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript clarifies that service tickets do not create invoices directly. The line items are what actually appear on the invoice, while service ticket information is used as supporting context during the Hub invoicing process.
- **Responsible:** TBD

## CUBE-PH4-D2-015
- **Group:** Billing
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Invoicing
- **Task Name:** Support One-to-Many Invoice Relationships
- **User Story:** As an Account Manager (AM), I want one invoice to include multiple eligible line items from one or more service tickets, so that related billable charges can be invoiced together when allowed.
- **Description:** One invoice can include many line items. Since one service ticket can also have many line items, an invoice can include charges associated with multiple service tickets when those line items are eligible to be billed together.
- **Acceptance Criteria:** 1. One service ticket can have multiple line items, 2. One invoice can include multiple line items, 3. One invoice can include line items associated with multiple service tickets, 4. System excludes line items that are already attached to an invoice, 5. System considers PO separation when determining whether line items can be billed together.
- **Timestamp:** Day 2, Part 1 [33:29 – 34:03]
- **Mockups:** NO MOCKUP
- **Notes:** This story focuses on invoice relationships and grouping logic. The transcript clarifies that invoices are one-to-many with line items, and service tickets are also one-to-many with line items. By association, one invoice can include line items from multiple service tickets.
- **Responsible:** TBD

## CUBE-PH4-D2-016
- **Group:** Other Services
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Support One-Time Service Ticket for Other Services
- **User Story:** As an Account Manager (AM), I want Other Services to use a one-time service ticket, so that services that are not delivered, rented, serviced, and removed can be handled correctly.
- **Description:** Other Services are intended for one-time services rather than rented products that require delivery, recurring service, and removal. For regular Other Services, the system should support a single service ticket that records the service date and the related charges.
- **Acceptance Criteria:** 1. System supports a single service ticket for regular Other Services, 2. System does not require a delivery/service/removal ticket chain for regular Other Services, 3. User can enter the service date for the one-time service, 4. User can record charges related to the completed service, 5. Grease traps are excluded from this Other Services behavior.
- **Timestamp:** Day 2, Part 1 [34:24 – 37:02]
- **Mockups:** NO MOCKUP
- **Notes:** Grease traps are excluded from this Day 2 Part 1 discussion because they were temporarily included under Other Services but are expected to be handled separately with CWS.
- **Responsible:** TBD

## CUBE-PH4-D2-017
- **Group:** Other Services
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Pricing
- **Task Name:** Enforce Minimum Margin for Other Services
- **User Story:** As an Account Manager (AM), I want the system to enforce the minimum margin for Other Services, so that low-margin service records cannot be saved.
- **Description:** Other Services require a minimum margin before the record can be saved. If the entered vendor rate and customer charge do not meet the required margin, the system should stop the user from saving the record and indicate that the margin is insufficient. Other services had a specific $100 margin expectation and the page would not save with a $50 margin.
- **Acceptance Criteria:** 1. System validates the margin before saving an Other Services record, 2. System compares the customer charge against the hauler/vendor charge, 3. System prevents saving when the margin is below the required amount, 4. System shows feedback when the margin is insufficient, 5. User can update the pricing to meet the required margin before saving.
- **Timestamp:** Day 2, Part 1 [37:02 – 38:07]
- **Notes:** The screenshot shows the pricing fields used to evaluate the margin, including customer charge, total hauler charge, margin, and vendor rate. The transcript gives the example of a $100 margin expectation and explains that the page would not save with only a $50 margin.
- **Responsible:** TBD

## CUBE-PH4-D2-018
- **Group:** Other Services
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Product Line Logic
- **Task Name:** Support Junk Removal as an Other Service
- **User Story:** As an Account Manager (AM), I want junk removal to be supported as an Other Service, so that customers can receive a lower-cost alternative when a full roll-off dumpster is not needed or there is not enough space for one.
- **Description:** Junk removal is one of the most common services handled under Other Services. It is used when the customer needs items removed but does not need a fully rented roll-off dumpster, or when there is not enough space to place a dumpster at the site.
- **Acceptance Criteria:** 1. System supports junk removal under Other Services, 2. User can create a one-time service ticket for junk removal, 3. System supports junk removal when a full roll-off dumpster is not needed, 4. System supports junk removal when there is not enough space for a dumpster, 5. Junk removal can be billed as an Other Service.
- **Timestamp:** Day 2, Part 1 [38:07 – 39:45]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript describes junk removal as a lower-cost alternative to a full roll-off rental. This story should stay focused on junk removal as a supported service type, not on the broader catch-all behavior of Other Services.
- **Responsible:** TBD

## CUBE-PH4-D2-019
- **Group:** Other Services
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Field Requirements
- **Task Name:** Avoid Unnecessary Placement Note Requirements
- **User Story:** As an Account Manager (AM), I want the system to avoid requiring placement notes for Other Services when placement information does not apply, so that service records are not blocked by irrelevant field requirements.
- **Description:** Other Services can include services where placement information is not applicable, such as cleaning or power washing. The system should apply field requirements based on the selected service type instead of enforcing placement notes across all Other Services.
- **Acceptance Criteria:** 1. System evaluates field requirements based on the selected Other Service type, 2. System does not require placement notes when placement information does not apply, 3. User can save an Other Services record without placement notes when the service does not require them, 4. System can still support placement notes when they are relevant to the selected service, 5. Field validation for Other Services is separate from product lines where placement notes are required.
- **Timestamp:** Day 2, Part 1 [39:45 – 41:07]
- **Notes:** The transcript specifically calls out that a placement note does not make sense for services like cleaning a house or power washing a driveway. The screenshot shows Placement Notes as an available note type, but it does not directly show the validation behavior.
- **Responsible:** TBD

## CUBE-PH4-D2-020
- **Group:** Other Services
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Dispatching
- **Task Name:** Autofill Dispatch Log from Call Information
- **User Story:** As an Account Manager (AM), I want dispatch log information to autofill from the call when available, so that dispatch-related fields can be completed more efficiently.
- **Description:** The Dispatch Log can autofill call-related information during the Other Services workflow. This helps reduce manual entry by carrying over available call details into dispatch fields such as who called in, when the call occurred, and who is handling the dispatch.
- **Acceptance Criteria:** 1. System autofills dispatch log information when call data is available, 2. System displays autofilled values in the Dispatch Log section, 3. User can review the autofilled dispatch information, 4. User can complete any remaining dispatch fields manually, 5. Autofill behavior does not prevent the user from saving or continuing the ticket.
- **Timestamp:** Day 2, Part 1 [41:07 – 41:24]
- **Notes:** The transcript only confirms that the autofill behavior exists and was useful during the Other Services walkthrough. The screenshot supports the Dispatch Log context, but it also includes a Grease Trap Manifest Received checkbox, so avoid using that part as evidence for this story unless documenting grease traps separately.
- **Responsible:** TBD

## CUBE-PH4-D2-021
- **Group:** Other Services
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Product Categorization
- **Task Name:** Use Other Services as Catch-All Category
- **User Story:** As an Account Manager (AM), I want services that do not fit into a predefined product category to be recorded under Other Services, so that non-standard customer requests can still be managed.
- **Description:** Other Services works as a catch-all category for customer requests that do not belong to the predefined product lines. This allows ZTERS to manage non-standard services when the business decides to fulfill them, even if the request does not have a dedicated product category.
- **Acceptance Criteria:** 1. System provides Other Services as a catch-all category, 2. User can record services that do not fit predefined product categories, 3. System supports an undefined “Other” option when no specific service type applies, 4. User can manage non-standard customer requests under Other Services, 5. Other Services remains separate from predefined product categories.
- **Timestamp:** Day 2, Part 1 [41:27 – 44:54]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript gives examples of unusual services that could be handled under Other Services when appropriate, such as driveway repair, parking lot striping, or even highly discretionary customer requests. This story should stay focused on categorization flexibility, not fulfillment or pricing.
- **Responsible:** TBD

## CUBE-PH4-D2-022
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Provider Selection
- **Task Name:** Support Manual Provider Search for Other Services
- **User Story:** As an Account Manager (AM), I want the fulfillment process to support manual provider searching when no listed provider is available, so that uncommon Other Services requests can still be fulfilled.
- **Description:** Some Other Services requests may not have an existing PSP or provider available in the system. In those cases, the fulfillment process should support manual provider search, including contacting providers outside the existing provider list, capturing the provider cost, and applying the required markup before selling the service to the customer.
- **Acceptance Criteria:** 1. System supports cases where no existing provider is available, 2. User can proceed with manual provider search, 3. User can record provider information outside the existing PSP list when needed, 4. User can record provider cost, 5. User can apply margin or markup before selling the service to the customer.
- **Timestamp:** Day 2, Part 1 [45:23 – 47:33]
- **Mockups:** NO MOCKUP
- **Notes:** This applies especially to non-standard services such as power washing or similar requests where ZTERS may not already have a provider in the system. Keep this story focused on the manual provider search process, not on provider ranking or best-match suggestions.
- **Responsible:** TBD

## CUBE-PH4-D2-023
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Provider Selection
- **Task Name:** Evaluate Providers by Cost, Rating, and Reliability
- **User Story:** As an Account Manager (AM), I want available providers to be evaluated by cost, ratings, reviews, and reliability, so that provider selection is not based only on the lowest price.
- **Description:** When there is no PSP available, the fulfillment team may review providers that have serviced the area before or are already stored in the system. Provider selection should consider average cost, ratings, reviews, and reliability so the user can choose a provider that balances price with service quality.
- **Acceptance Criteria:** 1. System can show provider cost information, 2. System can show provider ratings, 3. System can show provider reviews or reliability indicators, 4. User can compare providers using both price and service quality, 5. User can select a provider after evaluating cost, ratings, reviews, and reliability.
- **Timestamp:** Day 2, Part 1 [49:34 – 51:44]
- **Mockups:** NO MOCKUP
- **Notes:** Provider selection should not automatically favor the lowest price. A slightly higher-cost provider may be preferred when ratings and reliability are stronger, since poor provider performance can create extra operational or billing issues later.
- **Responsible:** TBD

## CUBE-PH4-D2-024
- **Group:** Service Providers
- **Category:** UX/UI
- **Epic:** Core Flow
- **Parent Task:** Provider Selection
- **Task Name:** Show Best-Match Provider Options
- **User Story:** As an Account Manager (AM), I want the system to show best-match provider options based on cost, ratings, reliability, and usage, so that provider selection requires less manual searching.
- **Description:** When no PSP is available, the system should help users identify provider options that may be worth evaluating. Best-match options can consider factors such as cost, rating, reliability, and previous usage so the fulfillment team does not need to search manually from scratch.
- **Acceptance Criteria:** 1. System can display suggested provider matches for evaluation, 2. Suggested matches can consider cost, ratings, reliability, and usage history, 3. User can review suggested providers before selecting one, 4. System supports reducing manual provider search when no PSP is available, 5. Suggested providers are presented as recommendations, not automatic selections.
- **Timestamp:** Day 2, Part 1 [51:44 – 53:33]
- **Mockups:** NO MOCKUP
- **Notes:** This is an improvement over the current manual evaluation process. Suggested providers should support decision-making, but the user still needs to review the options before selecting a provider.
- **Responsible:** TBD

## CUBE-PH4-D2-025
- **Group:** Other Services
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Service Tickets
- **Task Name:** Limit Other Services to Service, Dry Run, and Miscellaneous Ticket Types
- **User Story:** As an Account Manager (AM), I want regular Other Services to use only the applicable service, dry run, and miscellaneous ticket types, so that one-time services do not follow an unnecessary delivery/service/removal chain.
- **Description:** Regular Other Services should not follow the same delivery, recurring service, and removal ticket chain used by rental-based product lines. The system should support the actual one-time service ticket and still allow applicable exception ticket types, such as dry run or miscellaneous, when service complications occur.
- **Acceptance Criteria:** 1. System does not create a delivery/service/removal chain for regular Other Services, 2. System supports one actual service ticket for the completed service, 3. System allows dry run tickets when the service cannot be completed, 4. System allows miscellaneous tickets when applicable, 5. System prevents additional standard service or removal tickets for regular Other Services.
- **Timestamp:** Day 2, Part 1 [53:39 – 56:54]
- **Notes:** Dry run can apply when the provider cannot complete the service, such as when access is blocked. Miscellaneous tickets remain available for non-core adjustments, but regular Other Services should still behave as one-time services rather than rental chains.
- **Responsible:** TBD

## CUBE-PH4-D2-026
- **Group:** Product Codes
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Product Master
- **Task Name:** Identify Product Codes by State Prefix
- **User Story:** As an Account Manager (AM), I want product codes to include the applicable state prefix and product/service code, so that state-based product and tax code variants can be identified correctly.
- **Description:** Product codes are prefixed by state, such as TX or NY, and that every product code has a tax code variant. Product codes use a state prefix combined with the product/service code. This allows the system to maintain state-specific product code variants and support tax code handling across different states.
- **Acceptance Criteria:** 1. Product code includes the applicable state abbreviation prefix, 2. Product code identifies the product and service combination, 3. System supports state-based product code variants, 4. Product code variants support tax code handling, 5. System can distinguish product code variants across different states.
- **Timestamp:** Day 2, Part 1 [57:03 – 58:17]
- **Notes:** The screenshot shows the product code suffix value, such as RO_20, but not the full state-prefixed code. Use this screenshot only as supporting context for product code structure, not as direct evidence of the state prefix.
- **Responsible:** TBD

## CUBE-PH4-D2-027
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Ticket Mapping
- **Task Name:** Map Fulfillment Tickets to Actionable Service Activities
- **User Story:** As an Account Manager (AM), I want fulfillment tickets to be created for actionable service activities, so that haulers are contacted only when coordination is required.
- **Description:** Fulfillment tickets are created for service activities that require action from the fulfillment team or communication with a hauler. Examples include deliveries, hauls, removals, and extra services. Standard recurring rental or service cycles do not always require a fulfillment ticket because the hauler is expected to continue the recurring service without being contacted each cycle.
- **Acceptance Criteria:** 1. System creates fulfillment tickets for service activities that require hauler coordination, 2. Delivery activities can generate fulfillment tickets, 3. Haul activities can generate fulfillment tickets, 4. Removal and extra service activities can generate fulfillment tickets, 5. Standard recurring rental or service cycles do not automatically require a fulfillment ticket every cycle.
- **Timestamp:** Day 2, Part 1 [1:13:31 – 1:15:08]
- **Notes:** The diagram is a strong supporting mockup for this story because it shows how service tickets connect to work orders/fulfillment tickets and line items. Keep this story focused on service-ticket-to-fulfillment-ticket mapping, not provider selection or invoicing logic.
- **Responsible:** TBD

## CUBE-PH4-D2-028
- **Group:** Billing
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Invoicing
- **Task Name:** Bill Eligible Line Items Together by Site and PO Conditions
- **User Story:** As an Account Manager (AM), I want eligible line items to be billed together when they belong to the same site and are not separated by PO requirements, so that related charges can be included on the same invoice.
- **Description:** Line items can be billed together when they are available for billing and meet the required grouping conditions. Items can be grouped by site, but separate PO numbers require separate invoices. Line items that are already attached to an invoice should not be available for billing again.
- **Acceptance Criteria:** 1. System identifies line items available for billing, 2. System excludes line items that are already attached to an invoice, 3. System can group eligible line items by site, 4. System separates line items when PO numbers are different, 5. User can create one invoice from eligible unbilled line items when grouping conditions are met.
- **Timestamp:** Day 2, Part 1 [1:15:08 – 1:17:51]
- **Notes:** Use the diagram as the main mockup for this story. It shows how line items from service tickets can be grouped into an invoice, while still keeping the site and product structure visible. PO separation is the key condition that prevents otherwise related line items from being billed together.
- **Responsible:** TBD

## CUBE-PH4-D2-029
- **Group:** Service Providers
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Hauler Management
- **Task Name:** Add Vendor to Intacct from Service Provider Record
- **User Story:** As an Account Manager (AM), I want a service provider to be added to Intacct before invoicing when needed, so that vendor records are available for downstream accounting processes.
- **Description:** Service providers may need to be added to Intacct before the invoice process occurs. The system should support a manual trigger that sends the provider information through Hub so the vendor record can be created in Intacct when required.
- **Acceptance Criteria:** 1. User can manually trigger the service provider to be added to Intacct, 2. System sends the service provider information through Hub, 3. Hub creates or adds the vendor record in Intacct, 4. The process supports cases where the vendor is needed before invoice creation, 5. The vendor setup process does not depend only on invoice-time vendor creation.
- **Timestamp:** Day 2, Part 1 [1:18:26 – 1:20:03]
- **Notes:** Use the diagram only as general process context. A more specific mockup would be the service provider field or control used to trigger the Intacct vendor creation. This story should stay focused on vendor synchronization with Intacct, not invoice generation itself.
- **Responsible:** TBD

## CUBE-PH4-D2-030
- **Group:** Service Providers
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Hauler Authorization
- **Task Name:** Validate Service Provider Authorization Requirements
- **User Story:** As an Account Manager (AM), I want service provider authorization to depend on current insurance, current W-9, and required provider information, so that only eligible providers can be used.
- **Description:** Service providers must meet authorization requirements before they can be used in the workflow. Authorization depends on required provider information, insurance on file, W-9 on file, and documents that are not missing or expired.
- **Acceptance Criteria:** 1. System checks whether insurance is on file, 2. System checks whether W-9 is on file, 3. System checks whether required provider information is complete, 4. System checks whether required documents are missing or expired, 5. System prevents unauthorized providers from being used when authorization requirements are not met.
- **Timestamp:** Day 2, Part 1 [1:20:03 – 1:22:15]
- **Notes:** The hauler record should clearly show authorization-related fields such as Verified, Authorized, Insurance on File, W9 On File, and DNU. Missing or expired required documents should prevent the provider from being treated as eligible for normal use.
- **Responsible:** TBD

## CUBE-PH4-D2-031
- **Group:** Service Providers
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Hauler Authorization
- **Task Name:** Support Temporary Authorization for Service Providers
- **User Story:** As an Account Manager (AM), I want to temporarily authorize a service provider when required information is still pending, so that the provider can be used for a limited time while authorization requirements are completed.
- **Description:** Temporary authorization as a limited-use process when a hauler is needed for a site but required W-9/COI information is not yet available. Temporary authorization allows a service provider to be used for a limited period when the provider is needed for service but required authorization information is still pending. The system should require a reason, track the most recent temporary authorization date, and maintain a count of how many times the provider has been temporarily authorized.
- **Acceptance Criteria:** 1. User can mark a service provider as temporarily authorized, 2. System requires a temporary authorization reason or explanation, 3. System records the most recent temporary authorization date, 4. System increments the temporary authorization count, 5. Temporary authorization allows the provider to be used only during the allowed temporary period.
- **Timestamp:** Day 2, Part 1 [1:22:15 – 1:24:50]
- **Notes:** Temporary authorization should be treated as an exception, not the normal provider approval path. The screenshot shows the key tracking fields needed for this process, including the explanation, log, count, and most recent authorization date.
- **Responsible:** TBD

## CUBE-PH4-D2-032
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Hauler Status
- **Task Name:** Use Service Provider Statuses to Control Availability
- **User Story:** As an Account Manager (AM), I want service provider availability to be controlled by a single status, so that only authorized and verified or temporarily authorized providers can be used.
- **Description:** Service provider availability should be controlled through a clear status model. Statuses such as Draft, Pending Verification, Authorized, Temp Authorized, Suspended, DNU, Merged, and Deleted help distinguish why a provider can or cannot be used. Only providers that are authorized and verified, or temporarily authorized within the allowed period, should be available for use.
- **Acceptance Criteria:** 1. System supports Draft status for providers that have never been submitted or used, 2. System supports Pending Verification status when submitted information has not been fully reviewed, 3. System supports Authorized status when verification, current COI, and W-9 requirements are met, 4. System supports Temp Authorized status during the allowed temporary authorization period, 5. System supports Suspended status when required documents are missing or expired after prior verification, 6. System prevents provider use when the status is DNU, Merged, Deleted, Suspended, Pending Verification, or Draft.
- **Timestamp:** Day 2, Part 1 [1:25:09 – 1:29:19]
- **Notes:** A single status should make provider availability easier to understand than separate yes/no fields. DNU should act as a hard block, while Merged and Deleted can be hidden from most lists depending on the final design. Temporary authorization should expire automatically and fall back to Suspended or Pending Verification based on whether the provider had been verified before.
- **Responsible:** TBD

## CUBE-PH4-D2-033
- **Group:** Service Providers
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Hauler Verification
- **Task Name:** Restrict Service Provider Verification to Service Provider Lead
- **User Story:** As a Service Provider Lead, I want to verify service providers through a restricted approval process, so that verification is controlled by the appropriate role.
- **Description:** Service provider verification should be restricted to the Service Provider Lead. The verification process confirms that the provider information has been reviewed, but verification remains separate from document expiration logic. A provider can remain verified while becoming suspended if required documents later become missing or expired.
- **Acceptance Criteria:** 1. Only the Service Provider Lead can verify a service provider, 2. Verification is handled through a restricted approval process, 3. Verification remains separate from document expiration status, 4. A verified provider can become suspended when required documents are missing or expired, 5. Verification status contributes to the provider’s overall availability status.
- **Timestamp:** Day 2, Part 1 [1:32:48 – 1:34:35]
- **Notes:** Verification should not be automatically unchecked when insurance or W-9 information expires. The provider can stay verified from a review standpoint, while the overall status changes to suspended because required documents are no longer valid.
- **Responsible:** TBD

## CUBE-PH4-D2-034
- **Group:** Employees
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** User Metadata
- **Task Name:** Maintain Employee Metadata for System Logic
- **User Story:** As an Account Manager (AM), I want employee metadata such as manager, department, active status, title, and CWS indicator to be available across the system, so that reporting, ownership, and workflow logic can use the correct employee context.
- **Description:** Employee metadata is used across the system for reporting, page conditions, record ownership, workflow logic, and CWS-specific behavior. The system needs access to key employee details such as manager or supervisor, title, department, active status, and CWS-related indicators when records are assigned, displayed, filtered, or processed.
- **Acceptance Criteria:** 1. System stores manager or supervisor metadata, 2. System stores employee title and department-related metadata, 3. System identifies whether an employee is active or inactive, 4. System supports CWS-related employee indicators, 5. Employee metadata can be used by reporting, page conditions, ownership logic, and workflow rules.
- **Timestamp:** Day 2, Part 1 [1:39:30 – 1:51:03]
- **Notes:** This story marks the transition from product/service-ticket behavior into employee metadata. Employee records are needed beyond authentication because several parts of the system depend on employee context, such as manager hierarchy, CWS logic, account ownership, reporting, and active/inactive status.
- **Responsible:** TBD

## CUBE-PH4-D2-035
- **Group:** Employees
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** User Metadata
- **Task Name:** Keep One-to-One Parity Between Users and Employee Metadata
- **User Story:** As an Account Manager (AM), I want each system user to have one corresponding employee metadata record, so that user access and employee context remain aligned in CUBE.
- **Description:** CUBE should maintain one-to-one parity between system users and employee metadata records. Each user record should have a matching employee metadata record so the system can consistently use employee context for ownership, reporting, permissions, and workflow logic.
- **Acceptance Criteria:** 1. Each system user has one corresponding employee metadata record, 2. Employee metadata remains aligned with the user record, 3. System avoids duplicate user-role combinations from the current QuickBase structure, 4. System supports deleting or soft-deleting CUBE users according to the final design, 5. Historical user handling is reviewed before old or denied users are removed.
- **Timestamp:** Day 2, Part 1 [1:51:13 – 1:55:24]
- **Notes:** This story builds on the employee metadata requirement. The goal is to avoid separate user and employee records drifting out of sync. Old, denied, duplicated, or historical users may need cleanup rules before migration, especially if past activity or audit history still depends on those records.
- **Responsible:** TBD

## CUBE-PH4-D2-036
- **Group:** Customers
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Customer Assignment
- **Task Name:** Capture BDR and Round-Robin Assign Customer to AM
- **User Story:** As a Business Development Representative (BDR), I want the customer record to capture me as the BDR who answered the call and then assign the customer to an AM through round robin, so that call origin and customer ownership are both retained.
- **Description:** When a customer record is created from the call flow, the system captures the BDR who answered the call and then reassigns the customer to the next AM in the round-robin assignment order. This keeps the original call ownership visible while assigning the customer record to the AM responsible for follow-up.
- **Acceptance Criteria:** 1. Customer record is created through the call flow, 2. System captures the BDR who answered the call, 3. System stores the BDR as the last assigned user or equivalent tracking field, 4. System identifies the next AM in the round-robin assignment order, 5. System reassigns the customer record owner to the selected AM, 6. System marks the round-robin reassignment as completed.
- **Timestamp:** Day 2, Part 1 [1:55:24 – 2:00:26]
- **Notes:** This story starts the customer assignment automation topic. The BDR remains traceable as the person who answered the call, while the AM becomes the customer record owner for follow-up. The screenshot can be used as the mockup because it shows the actual round-robin reassignment workflow.
- **Responsible:** TBD

## CUBE-PH4-D2-037
- **Group:** Customers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Customer Wizard
- **Task Name:** Keep Customer Creation APIs Compatible with New Call Wizard
- **User Story:** As an Account Manager (AM), I want the HUB Call Wizard to keep its customer creation API behavior compatible with CUBE, so that customer, site, product, pricing, task, and billing information can continue flowing correctly between HUB and CUBE.
- **Description:** The Call Wizard is a HUB feature that will be connected to CUBE. Its customer creation behavior should remain compatible with the existing assignment and customer flow logic, including customer creation, site creation, product/pricing flow, task creation, and billing preference capture.
- **Acceptance Criteria:** 1. HUB Call Wizard can create customer information, 2. HUB Call Wizard can create site information, 3. HUB Call Wizard can continue into product and pricing flow, 4. HUB Call Wizard can support task creation for related products, 5. HUB Call Wizard can capture billing preference, 6. Customer creation API behavior remains compatible with CUBE assignment automation.
- **Timestamp:** Day 2, Part 1 [2:00:50 – 2:03:21]
- **Mockups:** NO MOCKUP
- **Notes:** The Call Wizard should be documented as a HUB feature that connects to CUBE, not as a native CUBE screen. The key requirement is API compatibility so existing customer assignment and downstream flow logic continue working after integration.
- **Responsible:** TBD

## CUBE-PH4-D2-038
- **Group:** Customers
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Round Robin
- **Task Name:** Calculate AM Round-Robin Rank
- **User Story:** As an Account Manager (AM), I want my round-robin rank to be calculated from previous customer assignments, so that the next eligible AM receives the next customer in the assignment order.
- **Description:** The round-robin rank is calculated by comparing each included AM’s most recent assigned customer record against the other AMs in the assignment pool. The AM with the next eligible rank receives the next customer assignment and then moves to the back of the assignment order.
- **Acceptance Criteria:** 1. System includes only AMs marked for round-robin assignment, 2. System calculates each AM’s most recent customer assignment value, 3. System compares eligible AMs against the assignment pool, 4. System identifies the AM with the next eligible rank, 5. Assigned AM moves to the back of the assignment order after receiving a new customer.
- **Timestamp:** Day 2, Part 1 [2:03:21 – 2:07:12]
- **Notes:** The screenshot is a good mockup for this story because it shows the Round Robin Rank field and the formula behind the current QuickBase implementation. In CUBE, the same business behavior can be implemented differently as long as the assignment order remains fair and traceable.
- **Responsible:** TBD

## CUBE-PH4-D2-039
- **Group:** Customers
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Round Robin
- **Task Name:** Handle New Employees and Leave in Round Robin
- **User Story:** As an Account Manager (AM), I want new AMs and unavailable AMs to be handled correctly in the round-robin pool, so that customer assignments only go to eligible AMs.
- **Description:** The round-robin pool should include only AMs who are eligible to receive customer assignments. A new AM may need an initial assignment value before the system can calculate their position in the pool, while an AM who is temporarily unavailable can be removed from the pool until they return.
- **Acceptance Criteria:** 1. System allows a new AM to be included in the round-robin pool, 2. System requires an initial assignment value before a new AM can be ranked, 3. System supports a round-robin inclusion flag, 4. System excludes unavailable AMs from the assignment pool, 5. System resumes assignment eligibility when the AM is added back to the pool.
- **Timestamp:** Day 2, Part 1 [2:07:20 – 2:10:29]
- **Mockups:** NO MOCKUP
- **Notes:** This story depends on the round-robin ranking logic from D2-038. New AMs need a non-null assignment value so the system can calculate their place in line. AMs who are on leave or temporarily unavailable should be excluded from the assignment pool instead of receiving new customers.
- **Responsible:** TBD

## CUBE-PH4-D2-040
- **Group:** Customers
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Customer Records
- **Task Name:** Send Customer Updates to Intacct, Hub, or Portal
- **User Story:** As an Account Manager (AM), I want customer creation and customer name updates to trigger the required integrations, so that Intacct, Hub, and/or Portal remain aligned with CUBE customer data.
- **Description:** Customer records need to stay synchronized with related external systems. When a customer is created, the system should send the customer information to Intacct. When the customer name is updated, the system should trigger the required updates for Hub and/or Portal so customer data remains consistent.
- **Acceptance Criteria:** 1. System triggers an integration when a customer record is created, 2. System sends new customer data to Intacct, 3. System detects customer name updates, 4. System triggers Hub and/or Portal updates when the customer name changes, 5. Integration triggers help keep customer data aligned across connected systems.
- **Timestamp:** Day 2, Part 1 [2:11:54 – 2:12:36]
- **Notes:** A better mockup would show the customer record webhook, customer integration fields, or the customer record update process. The screenshot shared is more useful for the round-robin/customer assignment stories because it shows employee assignment fields rather than customer integration behavior.
- **Responsible:** TBD

## CUBE-PH4-D2-041
- **Group:** Customers
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Customer Assignment
- **Task Name:** Support Permanent Customer Reassignment
- **User Story:** As an Account Manager (AM), I want customer records to be permanently reassigned in bulk, so that customers can be redistributed to another AM when ownership changes are needed.
- **Description:** Customer records can be permanently reassigned using a reassignment report and automation that updates the customer record owner. The process allows users to filter customer records, set a reassigned-to value, and save the changes so ownership is updated without editing each customer record individually.
- **Acceptance Criteria:** 1. User can filter customer records by current owner, 2. User can update the reassigned-to value for one or more customer records, 3. System updates the customer record owner based on the reassigned-to value, 4. System supports bulk reassignment of multiple customer records, 5. System records reassignment context using fields such as last assigned to and reassigned to when applicable.
- **Timestamp:** Day 2, Part 1 [2:12:36 – 2:16:31]
- **Notes:** This process is separate from round-robin assignment. It is used when existing customer ownership needs to be changed permanently, such as redistributing customers from one AM to another. The screenshot is a good mockup because it shows the reassignment report used for this workflow.
- **Responsible:** TBD

## CUBE-PH4-D2-042
- **Group:** Customers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Customer Assignment
- **Task Name:** Show Temporary Assignment Context
- **User Story:** As an Account Manager (AM), I want temporary assignment context to be visible on customer records, so that users know when the main AM is out and who should be contacted temporarily.
- **Description:** Customer records should show when a main AM is out and another user is temporarily assigned to support the customer. This context helps users contact the correct person without permanently changing ownership or losing visibility of the original AM relationship.
- **Acceptance Criteria:** 1. System supports temporary employee assignment on customer records, 2. System supports active out-of-office context when applicable, 3. Customer page shows when the main AM is out, 4. Customer page shows the temporary contact responsible during that period, 5. User can understand the temporary assignment context without leaving the customer record.
- **Timestamp:** Day 2, Part 1 [2:16:31 – 2:18:36]
- **Mockups:** NO MOCKUP
- **Notes:** Temporary assignment should not be treated the same as permanent reassignment. The purpose is to show who should be contacted while the main AM is unavailable, while still preserving the original ownership context.
- **Responsible:** TBD

## CUBE-PH4-D2-043
- **Group:** Customers
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Customer Validation
- **Task Name:** Validate Customer Email and Portal Email Fields
- **User Story:** As an Account Manager (AM), I want customer email fields to support validation and portal access logic, so that customer records can remain consistent and portal usage is not blocked by missing or misaligned email data.
- **Description:** Customer records include multiple email fields, such as primary email, portal email, internal shared email, and external shared email. These fields should support customer validation, duplicate prevention, and portal access logic without preventing customers from using the portal when optional override fields are blank.
- **Acceptance Criteria:** 1. System supports primary email validation, 2. System supports portal email handling, 3. System supports internal and external shared email fields, 4. System can align or copy email values when required, 5. Portal access is not blocked only because optional shared or override email fields are blank, 6. Duplicate email or domain validation is supported where applicable.
- **Timestamp:** Day 2, Part 1 [2:18:36 – 2:24:04]
- **Notes:** Shared or portal-specific email fields should work as overrides or additional access fields when needed, not as blockers for normal portal access. If a customer provides a valid primary email, that email should remain usable unless a specific portal access rule overrides it.
- **Responsible:** TBD

## CUBE-PH4-D2-044
- **Group:** Customers
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Customer Type
- **Task Name:** Nullify Company Name for Personal Customers
- **User Story:** As an Account Manager (AM), I want the company name to be cleared when the customer type is personal, so that incorrect company names do not appear on invoices or related outputs.
- **Description:** When the customer type is personal, the company name field should be hidden and cleared. This prevents hidden or previously entered company name values from being used later in invoices, Hub processes, or other downstream outputs.
- **Acceptance Criteria:** 1. System detects when customer type is personal, 2. System hides the company name field for personal customers, 3. System clears the company name value when customer type is personal, 4. System prevents hidden company name values from flowing to invoices or related outputs, 5. Business customer type can still use the company name field.
- **Timestamp:** Day 2, Part 1 [2:24:10 – 2:25:09]
- **Mockups:** NO MOCKUP
- **Notes:** Hiding the company name field is not enough because an old or incorrect value could remain stored in the background. The value should be cleared when the customer is personal to avoid bad data appearing later in billing or customer-facing outputs.
- **Responsible:** TBD

## CUBE-PH4-D2-045
- **Group:** Customers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Calls
- **Task Name:** Show Direct Number Reminder for Paid Lead Source Calls
- **User Story:** As an Account Manager (AM), I want the system to identify when a customer called through a paid lead source and remind me to provide ZTERS’ direct number, so that repeat calls do not create unnecessary lead costs.
- **Description:** When the customer’s last call came through a paid lead source number, the customer record should show a reminder to provide ZTERS’ direct number. This helps prevent the customer from calling back through the paid tracking number and generating additional lead source charges.
- **Acceptance Criteria:** 1. System captures the customer’s last call source, 2. System identifies whether the last call came from a paid lead source, 3. System displays a direct number reminder when the last call source is paid, 4. Reminder includes the ZTERS direct number, 5. Reminder is not shown when the last call source does not require it.
- **Timestamp:** Day 2, Part 1 [2:25:09 – 2:26:26]
- **Mockups:** NO MOCKUP
- **Notes:** This behavior helps reduce repeated paid lead source charges. The reminder should be visible enough for the AM to share the direct number with the customer during follow-up or future communication.
- **Responsible:** TBD

## CUBE-PH4-D2-046
- **Group:** Customers
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Call Tracking
- **Task Name:** Relate Answered Calls to Lead Sources
- **User Story:** As an Account Manager (AM), I want answered phone calls to be related to lead sources based on the number the customer dialed, so that call reporting and paid lead tracking use the correct source.
- **Description:** Answered phone call records store call details such as the number the customer dialed, caller ID, answering agent, call status, and related customer information. The system should use the dialed number to associate the call with the correct lead source or advertising campaign for reporting and follow-up logic.
- **Acceptance Criteria:** 1. System stores answered phone call records, 2. System captures the number the customer dialed, 3. System captures caller and answering agent information, 4. System relates the dialed number to the correct lead source or campaign, 5. Call source data can support reporting and related customer reminders.
- **Timestamp:** Day 2, Part 1 [2:27:00 – 2:33:45]
- **Notes:** This story provides the data foundation for paid lead tracking and the direct number reminder. The dialed number is the key value used to determine where the call came from and whether it should be associated with a paid lead source.
- **Responsible:** TBD

## CUBE-PH4-D2-047
- **Group:** Customers
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Customer Flags
- **Task Name:** Capture Customer Risk and Special Handling Flags
- **User Story:** As an Account Manager (AM), I want customer records to capture risk and special handling flags, so that customer follow-up, service decisions, and account handling follow the recorded customer conditions.
- **Description:** Customer records should include flags and fields used for special handling, such as DNU, stop service, Spanish-only speaker, perfect sale, and re-engagement coupon reason. These indicators help users understand customer restrictions, service actions, language needs, sales tracking, and re-engagement context.
- **Acceptance Criteria:** 1. System supports a DNU flag, 2. System supports a stop service flag, 3. System supports a Spanish-only speaker flag, 4. System supports a perfect sale indicator, 5. System supports a re-engagement coupon reason field, 6. Customer handling logic can reference these flags when applicable.
- **Timestamp:** Day 2, Part 1 [2:33:45 – 2:35:44]
- **Mockups:** NO MOCKUP
- **Notes:** Keep this story focused on customer-level flags and handling indicators. DNU and stop service should be treated carefully because they affect whether the customer can be used or whether existing services should be stopped. Spanish-only speaker can support future routing or reassignment improvements, but this story should only capture the flag behavior unless routing is explicitly included elsewhere.
- **Responsible:** TBD

## CUBE-PH4-D2-048
- **Group:** Customers
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** HubSpot
- **Task Name:** Send CWS Inside Lead to HubSpot
- **User Story:** As an Account Manager (AM), I want CWS inside lead information to be sent to HubSpot, so that CWS lead records can be created in HubSpot from customer data.
- **Description:** CWS inside lead information is sent to HubSpot through an API process. When the required CWS lead fields are completed and saved, the system should send the customer and lead details to HubSpot so the corresponding lead records can be created.
- **Acceptance Criteria:** 1. User can complete the required CWS inside lead fields, 2. System triggers the HubSpot API process when the record is saved, 3. System sends the required customer and lead information to HubSpot, 4. HubSpot creates the corresponding lead records, 5. System stores or references returned HubSpot information when available.
- **Timestamp:** Day 2, Part 1 [2:37:20 – 2:39:09]
- **Mockups:** NO MOCKUP
- **Notes:** This story applies to CWS inside leads only. Keep it focused on sending the captured lead information to HubSpot, not on the later business-customer HubSpot process that runs after seven days.
- **Responsible:** TBD

## CUBE-PH4-D2-049
- **Group:** Customers
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** HubSpot
- **Task Name:** Send Business Customers to HubSpot After Seven Days
- **User Story:** As an Account Manager (AM), I want business customers to be sent to HubSpot after seven days, so that AMs have time to review and clean up customer information before HubSpot creation.
- **Description:** Business customer records are sent to HubSpot through a scheduled process after a seven-day waiting period. This delay gives the assigned AM time to review and complete customer information before the system creates the related company and contact records in HubSpot.
- **Acceptance Criteria:** System identifies business customer records, 2. Nightly process checks for business customers created seven days earlier, 3. System sends company data to HubSpot, 4. System sends contact data to HubSpot, 5. System writes HubSpot ID or URL information back to the customer record when available.
- **Timestamp:** Day 2, Part 1 [2:54:32 – 3:00:46]
- **Mockups:** NO MOCKUP
- **Notes:** This process is separate from the CWS inside lead flow. The seven-day delay gives AMs time to clean up or complete customer details before the business customer is pushed to HubSpot.
- **Responsible:** TBD

## CUBE-PH4-D2-050
- **Group:** Customers
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Account Manager Tasks
- **Task Name:** Create Follow-Up Tasks for New Business Customers
- **User Story:** As an Account Manager (AM), I want follow-up tasks to be created for new business customers, so that I can call, email, and research the customer before continued follow-up or HubSpot creation.
- **Description:** New business customers can trigger follow-up tasks for the assigned AM. These tasks support the AM’s next steps, including making an introduction call, sending an introduction or sell sheet email, and researching the customer on LinkedIn.
- **Acceptance Criteria:** 1. System creates an introduction call task, 2. System creates an introduction email or sell sheet task, 3. System creates a LinkedIn research task, 4. Tasks are assigned to the Account Manager, 5. Tasks receive a due date based on the scheduled task creation process.
- **Timestamp:** Day 2, Part 1 [2:55:06 – 2:58:37]
- **Mockups:** NO MOCKUP
- **Notes:** These tasks support AM follow-up before the business customer is pushed to HubSpot. The tasks should be assigned to the AM responsible for the customer and should help ensure the customer is reviewed, contacted, and researched after creation.
- **Responsible:** TBD

## CUBE-PH4-D2-051
- **Group:** Service Sites
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Site Management
- **Task Name:** Show Site-Level Past Due Warning and Approval
- **User Story:** As an Account Manager (AM), I want service sites to show past due customer warnings and approval requirements when applicable, so that site-level service activity reflects the customer’s credit status.
- **Description:** Service sites should display past due warnings when the related customer has a past due condition. The site page should pull customer credit status information and indicate when approval is required before continuing site-level service activity.
- **Acceptance Criteria:** 1. Site page displays a past due warning when applicable, 2. Site page pulls customer credit status information, 3. System identifies when approval is required, 4. User can see the warning before continuing site-level service activity, 5. Approval behavior aligns with the customer-level past due logic.
- **Timestamp:** Day 2, Part 1 [3:00:46 – 3:01:24]
- **Mockups:** NO MOCKUP
- **Notes:** This warning helps prevent users from continuing site-level activity without noticing the customer’s credit status. The site-level warning should stay aligned with customer-level credit and approval rules so the same risk condition is visible throughout the workflow.
- **Responsible:** TBD

## CUBE-PH4-D2-052
- **Group:** Service Sites
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Site Location
- **Task Name:** Capture Hawaii Island for Service Sites
- **User Story:** As an Account Manager (AM), I want the system to capture the island for Hawaii service sites, so that the correct service provider options can be identified for island-specific service availability.
- **Description:** Hawaii service sites need island information because service provider availability can vary by island. Some product lines may have only one or two usable providers for a specific island, so the system should capture the island to support accurate provider selection.
- **Acceptance Criteria:** 1. System identifies Hawaii service sites, 2. System requires or captures island information for Hawaii sites, 3. Island value supports service provider selection, 4. System supports product-line-specific provider limitations by island, 5. User can distinguish Hawaii service availability beyond the state value.
- **Timestamp:** Day 2, Part 1 [3:01:24 – 3:02:22]
- **Mockups:** NO MOCKUP
- **Notes:** Hawaii should not be handled only as a single state value for provider selection. Island-level information is needed because availability can be limited and product-specific, especially when only one provider can service a product line on a given island.
- **Responsible:** TBD

## CUBE-PH4-D2-053
- **Group:** Service Sites
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Site Location
- **Task Name:** Prevent Service in Uninsured New York City Areas
- **User Story:** As an Account Manager (AM), I want the system to identify New York City service areas where ZTERS cannot do business, so that uninsured service locations are blocked before service is processed.
- **Description:** Some New York City areas cannot be serviced because ZTERS is not insured to operate there. The system should use zip code metadata to identify uninsured locations and alert the user before service activity continues.
- **Acceptance Criteria:** System checks the service site zip code metadata, 2. System identifies uninsured New York City service areas, 3. System displays a cannot-do-business condition when the site is in an uninsured area, 4. User is alerted before proceeding with service, 5. System prevents service activity from continuing when the location is blocked due to insurance restrictions.
- **Timestamp:** Day 2, Part 1 [3:02:22 – 3:03:02]
- **Mockups:** NO MOCKUP
- **Notes:** This is a blocking location rule, not just an informational warning. The key condition is whether the zip code is marked as uninsured for the New York City area.
- **Responsible:** TBD

## CUBE-PH4-D2-054
- **Group:** Zip Codes
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Location Metadata
- **Task Name:** Use Zip Code Metadata for Franchise, Insurance, and Winterization Logic
- **User Story:** As an Account Manager (AM), I want zip code metadata to feed site and product logic, so that uninsured areas, possible franchise markets, and winterization requirements can be identified.
- **Description:** Zip code records store location metadata used by site and product workflows. This metadata includes uninsured indicators, possible franchise market indicators, and cold month or temperature information used to determine winterization requirements.
- **Acceptance Criteria:** Zip code record stores an uninsured indicator, 2. Zip code record stores a possible franchise indicator, 3. Zip code record stores cold month or temperature information, 4. Site records can use related zip code metadata, 5. Roll-off and toilet product logic can use applicable zip code metadata.
- **Timestamp:** Day 2, Part 1 [3:03:02 – 3:05:44]
- **Notes:** Zip code metadata works as a shared source for multiple location-based rules. Uninsured indicators support service restrictions, possible franchise indicators support roll-off/service provider review, and cold month data supports winterization logic for applicable product lines.
- **Responsible:** TBD

## CUBE-PH4-D2-055
- **Group:** Service Sites
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Notifications
- **Task Name:** Support Site-Level Order Summary Email Override
- **User Story:** As an Account Manager (AM), I want order summary emails to support a site-level recipient override, so that site-specific contacts can receive order summaries instead of only the customer’s primary email.
- **Description:** Order summary emails can use the customer’s primary email by default, but some service sites may require a different recipient. The system should support a site-level override so order summaries can be sent to the correct onsite or site-specific contact.
- **Acceptance Criteria:** 1. System uses the customer primary email as the default order summary recipient, 2. System supports a site-level recipient override, 3. User can enter or update the site-level order summary recipient, 4. Order summary emails are sent to the override recipient when one is provided, 5. If no override is provided, order summary emails use the default customer recipient.
- **Timestamp:** Day 2, Part 1 [3:05:44 – 3:07:31]
- **Mockups:** NO MOCKUP
- **Notes:** This is useful for customers with multiple sites where each site may have a different onsite contact. Current order summary emails are still sent from QuickBase and should eventually be moved to Hub, but the site-level override behavior should be preserved.
- **Responsible:** TBD

## CUBE-PH4-D2-056
- **Group:** Service Sites
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Tax Handling
- **Task Name:** Capture Site-Level Tax Exemption
- **User Story:** As an Account Manager (AM), I want tax exemption to be captured at the service site level, so that tax behavior reflects the state and location where the service is provided.
- **Description:** Tax exemption is tied to the service location because exemption rules depend on the state associated with the site address. The system should capture site-level tax exemption information and make it available to downstream product, line item, and billing processes.
- **Acceptance Criteria:** 1. System captures tax exemption information at the service site level, 2. Tax exemption is associated with the service site address or state, 3. Site tax exemption information can flow to related product records, 4. Site tax exemption information can flow to related line items, 5. Billing can use the site tax exemption information when applicable.
- **Timestamp:** Day 2, Part 1 [3:07:31 – 3:08:30]
- **Mockups:** NO MOCKUP
- **Notes:** Tax exemption should be handled at the site level because the same customer may have service locations in different states. This story should stay focused on tax exemption data flow from site to product, line item, and billing logic.
- **Responsible:** TBD

## CUBE-PH4-D2-057
- **Group:** Zsight
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** External System Updates
- **Task Name:** Send Record Updates to Zsight
- **User Story:** As an Account Manager (AM), I want relevant customer, site, hauler, front load, camera, and hauler quote updates to be sent to ZSight, so that ZSight receives the information it needs from the core flow records.
- **Description:** ZSight receives record updates through webhooks from different parts of the workflow, including customer, site, hauler, front load, camera, and hauler quote or maintenance-related records. These updates send the limited fields needed by ZSight when records are added or modified.
- **Acceptance Criteria:** 1. System supports update triggers for customer records, 2. System supports update triggers for site records, 3. System supports update triggers for hauler records, 4. System supports update triggers for front load, camera, and hauler quote or maintenance records, 5. ZSight receives only the fields required for its update process.
- **Timestamp:** Day 2, Part 2 [0:20 – 1:35]
- **Notes:** Use ZSight consistently as the product name. The screenshot shows the site webhook configuration, including ZSight - Update Site and Update CWS flag (for API listing page) - HUB. During CUBE migration, these webhooks should be reviewed to confirm which updates still need to be sent to ZSight and which belong to HUB/API listing behavior.
- **Responsible:** TBD

## CUBE-PH4-D2-058
- **Group:** Products
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Product Warnings
- **Task Name:** Display Product-Level Warnings and Status Indicators
- **User Story:** As an Account Manager (AM), I want product records to display inherited warnings and status indicators, so that tax exemption, stop service, inactive AM, temporary reassignment, and hauler eligibility conditions are visible before continuing the workflow.
- **Description:** Product records should display warnings and status indicators inherited from related customer, site, employee, and hauler records. These indicators help users identify important conditions such as tax exemption, stop service, inactive AM assignment, temporary reassignment, and hauler eligibility before continuing product-level work.
- **Acceptance Criteria:** 1. Product page displays tax exempt warning when applicable, 2. Product page displays stop service warning when applicable, 3. Product page identifies inactive account manager conditions, 4. Product page displays temporary reassignment warning when applicable, 5. Product page evaluates hauler eligibility before service ticket continuation
- **Timestamp:** Day 2, Part 2 [2:22 – 5:24]
- **Mockups:** NO MOCKUP
- **Notes:** Inactive AM assignment can affect billing in the current flow, so product-level visibility is important before users continue into service ticket or billing-related actions. This behavior should be reviewed in CUBE so inactive users can be handled correctly without relying on legacy workarounds.
- **Responsible:** TBD

## CUBE-PH4-D2-059
- **Group:** Products
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Hauler Eligibility
- **Task Name:** Block Service Ticket Continuation for Ineligible Haulers
- **User Story:** As an Account Manager (AM), I want the system to evaluate whether a selected hauler is authorized, verified, temporarily authorized, and not DNU, so that service tickets cannot continue with an ineligible hauler.
- **Description:** QuickBase currently allows selecting an ineligible hauler in some cases, but blocks progression when creating service tickets unless the hauler is eligible or temporarily authorized.
- **Acceptance Criteria:** 1. System evaluates authorized status, 2. System evaluates verified status, 3. System evaluates temporary authorization status, 4. System evaluates DNU status, 5. System blocks service ticket creation or continuation when the selected hauler is not eligible
- **Timestamp:** Day 2, Part 2 [5:24 – 6:59]
- **Mockups:** NO MOCKUP
- **Notes:** Current QuickBase behavior intentionally allows selection first so users can later complete temporary authorization; CUBE may handle visibility/selection differently.
- **Responsible:** TBD

## CUBE-PH4-D2-060
- **Group:** Products
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Ticket Availability
- **Task Name:** Determine Available Ticket Types by Product
- **User Story:** As an Account Manager (AM), I want ticket creation availability to be determined by the selected product and its applicable statuses, so that only valid ticket buttons are available for the product workflow.
- **Description:** Ticket availability is controlled by product-specific fields, form rules, statuses, and product master logic that define which ticket types can be created.
- **Acceptance Criteria:** 1. System determines ticket availability by product, 2. System uses product-specific guardrails, 3. System uses relevant ticket statuses, 4. System controls which ticket creation buttons are available, 5. System supports product-specific differences in ticket types
- **Timestamp:** Day 2, Part 2 [7:00 – 9:38]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop calls out the current product master/ticket availability logic as complex and likely needing redesign.
- **Responsible:** TBD

## CUBE-PH4-D2-061
- **Group:** Products
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Pricing
- **Task Name:** Use Rate Records Instead of Recopying Pricing Fields
- **User Story:** As an Account Manager (AM), I want product pricing to reference reusable rate records when possible, so that pricing snapshots can be preserved without repeatedly copying the same rate fields across products, service tickets, and line items.
- **Description:** Current pricing values are copied from pricing sources to products, service tickets, and line items for snapshot purposes, and suggests using rate records or rate cards to preserve history more efficiently.
- **Acceptance Criteria:** 1. System supports reusable rate records or rate cards, 2. Product records can reference the applicable rate record, 3. Historical records preserve the rate used at that point in time, 4. Updated rates can be represented by new rate records instead of overwriting prior rates, 5. Products, service tickets, and line items avoid unnecessary repeated copies of the same rate data when a reference can preserve the snapshot
- **Timestamp:** Day 2, Part 2 [18:53 – 23:15]
- **Mockups:** NO MOCKUP
- **Notes:** This was discussed as a redesign recommendation for CUBE, especially for PSP rates, statistical model rates, custom rates, and pricing history.
- **Responsible:** TBD

---

# Day 3

**Stories:** 55

## CUBE-PH4-D3-001
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Pricing Warnings
- **Task Name:** Display Winterization Fee Reminder
- **User Story:** As an Account Manager (AM), I want the pricing tool to display a winterization fee reminder when zip code metadata indicates that winterization applies, so that I can identify the additional fee before continuing with pricing.
- **Description:** Winterization fee reminders are driven by zip code metadata and apply to toilet services during applicable winterization months. The reminder should appear at the pricing tool level, and the same logic may also be relevant for the customer wizard when pricing is handled there.
- **Acceptance Criteria:** 1. System reads winterization metadata from the zip code, 2. System displays a winterization fee reminder when winterization applies, 3. Reminder applies to toilet services, 4. Reminder appears before the user continues with pricing, 5. Reminder indicates that a winterization fee may apply, 6. Winterization logic can be reused by the pricing tool and future customer wizard pricing flow.
- **Timestamp:** Day 3, Part 1 [0:07:13 – 0:08:05]
- **Mockups:** NO MOCKUPS
- **Notes:** This should be available in the Hub pricing tool and carried into the CUBE pricing tool. It may also apply to the customer wizard later if pricing is handled there.
- **Responsible:** TBD

## CUBE-PH4-D3-002
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Site-Level Warnings
- **Task Name:** Display Site-Level Pricing Warnings
- **User Story:** As an Account Manager (AM), I want the pricing tool to display site-level warnings for uninsured New York City areas and possible roll-off franchise restrictions, so that I do not promise unsupported service or rates to the customer.
- **Description:** Site-level pricing warnings are driven by zip code metadata and should alert users when service may be restricted or unavailable. These warnings include uninsured New York City areas and possible franchise restrictions for roll-offs.
- **Acceptance Criteria:** 1. System reads site-level warning metadata from the zip code, 2. System displays a warning when the site is in an uninsured New York City area, 3. System displays a warning when the site may have roll-off franchise restrictions, 4. Warning appears before the user continues with pricing, 5. Warning helps prevent users from promising unsupported service or rates.
- **Timestamp:** Day 3, Part 1 [0:08:05 – 0:09:25]
- **Mockups:** NO MOCKUPS
- **Notes:** These warnings should be available at the pricing tool level and may also be relevant for the customer wizard if pricing is handled there. The roll-off franchise warning is especially important because users should not promise rates when franchise restrictions may apply.
- **Responsible:** TBD

## CUBE-PH4-D3-003
- **Group:** Toilets
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Recurring Ticket Creation
- **Task Name:** Automatically Create Recurring Toilet Service Tickets
- **User Story:** As the system, I want to automatically create recurring toilet service tickets based on the parent product record and cycle information, so that recurring toilet services do not have to be created manually.
- **Description:** Recurring toilet service tickets are created automatically through a scheduled backend process. The process uses the parent toilet record, cycle dates, product type, and recurring service setup to determine when a new ticket should be created.
- **Acceptance Criteria:** 1. System evaluates toilet parent records during the recurring ticket creation process, 2. System identifies whether the toilet product can have a recurring standard service ticket, 3. System uses cycle information to determine whether a new ticket is needed, 4. System copies relevant values from the parent toilet record into the new ticket, 5. System creates the recurring ticket only when the required recurring conditions are met.
- **Timestamp:** Day 3, Part 1 [0:09:52 – 0:12:45]
- **Mockups:** NO MOCKUPS
- **Notes:** This is the high-level automation story for recurring toilet ticket creation. Keep the detailed validation rules in the next story so this one does not become too broad.
- **Responsible:** TBD

## CUBE-PH4-D3-004
- **Group:** Toilets
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Recurring Ticket Criteria
- **Task Name:** Validate Toilet Recurring Ticket Creation Criteria
- **User Story:** As the system, I want to automatically create recurring toilet service tickets based on the parent toilet record and next cycle information, so that recurring toilet services do not have to be created manually.
- **Description:** Recurring toilet service tickets are created through a scheduled table-to-table import process named “Create Next Cycle.” The process copies eligible toilet records and creates the next service ticket when the recurring service conditions are met.
- **Acceptance Criteria:** 1. System evaluates toilet records during the recurring ticket creation process, 2. System uses the Create Next Cycle import to create eligible recurring tickets, 3. System identifies whether the toilet product requires a standard service ticket, 4. System uses next cycle information to determine whether a new ticket should be created, 5. System copies mapped toilet record values into the new ticket.
- **Timestamp:** Day 3, Part 1 [0:10:35 – 0:13:20]
- **Notes:** The screenshot shows the QuickBase import configuration for Toilet Tickets using the import name “Create Next Cycle.” This story should stay focused on the automation that creates the next recurring ticket; the detailed import conditions can be covered in the following validation story.
- **Responsible:** TBD

## CUBE-PH4-D3-005
- **Group:** Toilets
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Recurring Line Item Creation
- **Task Name:** Automatically Create Line Items for Recurring Toilet Tickets
- **User Story:** As the system, I want to automatically create line items for recurring toilet tickets, so that each generated recurring ticket has the required billable line item.
- **Description:** Recurring toilet line items are created automatically after recurring toilet tickets are generated. The process follows similar condition-based logic to make sure the required billing line item is created for the service ticket.
- **Acceptance Criteria:** 1. System evaluates generated recurring toilet tickets for line item creation, 2. System applies the required recurring conditions before creating the line item, 3. System creates a line item for each eligible recurring toilet ticket, 4. System copies the required ticket and billing values into the line item, 5. System makes the generated line item available for downstream billing.
- **Timestamp:** Day 3, Part 1 [0:13:20 – 0:14:34]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should stay separate from recurring ticket creation because the ticket and the line item are created through related but separate automation steps. The line item is the billable record that supports the Hub billing process after the recurring ticket is created.
- **Responsible:** TBD

## CUBE-PH4-D3-006
- **Group:** Core Platform
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Cron Coordination
- **Task Name:** Coordinate QuickBase and Hub Recurring Cron Timing
- **User Story:** As an Account Manager (AM), I want recurring tickets and line items to be generated before the Hub billing cron runs, so that recurring charges are available for same-night billing.
- **Description:** Iitems were getting ready around 3:30 AM while the Hub cron used to run at 2:00 AM, which caused line items to be skipped until the next day; the Hub cron timing was changed to 4:00 AM. Recurring ticket and line item generation must finish before the Hub recurring billing process runs. The timing matters because Hub can only bill the line items that already exist when its cron job executes.
- **Acceptance Criteria:** 1. QuickBase recurring ticket and line item generation completes before the Hub recurring billing cron runs, 2. Hub recurring billing runs only after generated line items are available, 3. Same-night billing is supported when recurring line items are created before the Hub process starts, 4. Recurring line items are not skipped because of cron timing, 5. Cron timing supports accurate recurring invoice totals and reconciliation.
- **Timestamp:** Day 3, Part 1 [0:14:08 – 0:15:50]
- **Notes:** The recurring line item imports shown in QuickBase run around 3:30 AM. Hub billing was moved later so generated line items are available before the billing process starts. This prevents recurring items from being skipped until the next day.
- **Responsible:** TBD

## CUBE-PH4-D3-007
- **Group:** Front Loads
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Recurring Ticket Creation
- **Task Name:** Automatically Create Monthly Front Load Tickets and Line Items
- **User Story:** As an Account Manager (AM), I want monthly front load tickets and line items to be created automatically, so that front load services can be prepared for monthly billing without manual ticket and line item creation.
- **Description:** Front load tickets and line items are created through the same recurring automation approach used for toilets. Front loads follow a monthly billing cadence and are normally processed on a specific day of the month.
- **Acceptance Criteria:** 1. System runs the front load recurring process on the scheduled monthly day, 2. System creates eligible front load tickets automatically, 3. System creates related line items for eligible front load tickets, 4. System applies condition-based logic before creating front load line items, 5. Generated front load line items are available for the monthly billing process.
- **Timestamp:** Day 3, Part 1 [0:16:10 – 0:17:05]
- **Notes:** The QuickBase import list includes “Automated Line Item Import - Front loads.” Front loads follow the same general recurring creation pattern as toilets, but they are handled on a monthly billing schedule instead of the toilet cycle pattern.
- **Responsible:** TBD

## CUBE-PH4-D3-008
- **Group:** Core Platform
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Historical Records
- **Task Name:** Prevent Recurring Creation for Archived Historical Tickets
- **User Story:** As an Account Manager (AM), I want archived or historical records to be excluded from recurring creation processes, so that old tickets or removed child records do not generate new tickets or line items incorrectly.
- **Description:** Recurring creation logic must exclude archived historical records and records where child tickets or line items were removed. This prevents old records from being picked up again by automated imports and avoids creating new tickets, line items, or billing activity for records that should no longer be processed.
- **Acceptance Criteria:** 1. System excludes archived historical records from recurring creation processes, 2. System does not recreate tickets or line items for records with removed children, 3. Automated imports use date-based criteria to avoid processing old records, 4. Automated imports check the children removed indicator before creating new records, 5. Recurring creation logic does not trigger billing or invoicing activity for excluded historical records.
- **Timestamp:** Day 3, Part 1 [0:17:05 – 0:19:15]
- **Notes:** The automated line item import includes criteria such as Date Created after 01-01-2024 and Toilet - History - Children Removed not checked. This story should stay focused on the import guardrails that prevent archived or cauterized records from being processed again.
- **Responsible:** TBD

## CUBE-PH4-D3-009
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Winterization Line Items
- **Task Name:** Create Winterization Line Items Only During Applicable Winter Months
- **User Story:** As an Account Manager (AM), I want winterization line items to be created only when winterization applies, so that toilet services include the correct winterization fee during applicable winter months.
- **Description:** Winterization is handled as a separate $9 line item for toilet services. The line item is created only when the winterization conditions are met for the applicable cycle and location.
- **Acceptance Criteria:** 1. System evaluates whether the toilet service cycle is eligible for winterization, 2. System creates the winterization line item only when winterization applies, 3. Winterization line item uses the $9 winter service fee, 4. System does not create a winterization line item when winterization is not applicable, 5. Winterization line item logic follows the same winterization conditions used by the pricing reminder.
- **Timestamp:** Day 3, Part 1 [0:19:15 – 0:20:05]
- **Notes:** QuickBase includes a saved import named “Winter Service Fee Automated Line Item Import.” This should stay separate from the pricing reminder story because this item represents the actual billable winterization charge, not just the warning shown during pricing.
- **Responsible:** TBD

## CUBE-PH4-D3-010
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Damage Insurance Line Items
- **Task Name:** Create Damage Insurance Line Items Only When Accepted
- **User Story:** As an Account Manager (AM), I want damage insurance line items to be created only when the customer accepts damage insurance, so that toilet services include the insurance fee only when it was selected.
- **Description:** Damage insurance is handled as a separate $9 line item for toilet services. The line item is created only when damage insurance has been accepted by the customer.
- **Acceptance Criteria:** 1. System checks whether damage insurance was accepted, 2. System creates the damage insurance line item only when insurance was accepted, 3. Damage insurance line item uses the $9 insurance fee, 4. System does not create a damage insurance line item when insurance was not accepted, 5. Damage insurance logic applies before adding the insurance line item.
- **Timestamp:** Day 3, Part 1 [0:20:05 – 0:20:45]
- **Notes:** QuickBase includes a saved import named “Damage Insurance Fee Automated Line Item Import.” This should stay separate from winterization because insurance is customer-selected, while winterization is condition-based.
- **Responsible:** TBD

## CUBE-PH4-D3-011
- **Group:** Toilets
- **Category:** Taxation
- **Epic:** Core Flow
- **Parent Task:** California and Indiana Taxability
- **Task Name:** Split Toilet Rental and Service Line Items for California and Indiana
- **User Story:** As an Account Manager (AM), I want toilet rental and service charges to be split into separate line items for California and Indiana, so that rental and service can be taxed correctly based on state requirements.
- **Description:** California and Indiana require special handling because toilet rental and service have different taxability rules in those states. For these locations, the regular toilet charge must be split into separate service and rental line items with the appropriate tax treatment.
- **Acceptance Criteria:** 1. System identifies when the toilet service is located in California or Indiana, 2. System creates the standard service line item for the toilet ticket, 3. System creates one additional rental line item when state-specific tax handling applies, 4. Service and rental line items use their corresponding taxability treatment, 5. System prevents duplicate additional rental line items for the same ticket.
- **Timestamp:** Day 3, Part 1 [0:20:45 – 0:23:25]
- **Mockups:** NO MOCKUPS
- **Notes:** California and Indiana are exceptions to the normal toilet line item structure because rental and service are taxed differently. This story should stay separate from the standard toilet line item story because it exists specifically to handle state-based tax requirements.
- **Responsible:** TBD

## CUBE-PH4-D3-012
- **Group:** Core Platform
- **Category:** Automation
- **Epic:** Core Flow
- **Parent Task:** Recurring Automation Scope
- **Task Name:** Extend Recurring Automation to Applicable Product Lines
- **User Story:** As an Account Manager (AM), I want recurring ticket and line item automation to support applicable product lines, so that recurring services can be created consistently without designing each product line as a separate manual process.
- **Description:** Recurring automation can be designed to support product lines that follow recurring service or billing cycles, such as containers, storage containers, fencing, front loads, and permanent roll-offs. Product-specific billing rules still need to be respected where special handling is required.
- **Acceptance Criteria:** 1. System supports recurring automation for product lines with recurring service or billing cycles, 2. System creates recurring service tickets when the product line and cycle rules allow it, 3. System creates related recurring line items when billing rules allow it, 4. System respects product-specific billing requirements and exceptions, 5. Shared recurring automation logic is reused where the same recurring pattern applies.
- **Timestamp:** Day 3, Part 1 [0:23:25 – 0:26:35]
- **Mockups:** NO MOCKUPS
- **Notes:** This should be treated as an improvement or design direction, not as confirmation that every product line must be fully automated in the same way. Some products may still require special handling because of billing rules, manual review needs, or product-specific operational complexity.
- **Responsible:** TBD

## CUBE-PH4-D3-013
- **Group:** Core Platform
- **Category:** Data Integrity
- **Epic:** Core Flow
- **Parent Task:** Archived Children Handling
- **Task Name:** Track Removed Children for Archived Tickets and Line Items
- **User Story:** As an Account Manager (AM), I want archived records to retain historical ticket and payment totals when child records are removed, so that reporting and status logic can remain accurate without recreating missing tickets or line items.
- **Description:** Archived records can retain summarized historical information after child tickets and line items are removed. The children removed indicator helps formulas and statuses ignore missing child records while keeping key historical totals available for reference.
- **Acceptance Criteria:** 1. System stores a children removed indicator for archived records, 2. System retains historical ticket counts when child records are removed, 3. System retains historical customer paid totals when available, 4. System retains historical hauler paid totals when available, 5. System uses the children removed indicator to prevent formulas and statuses from treating missing children as active work.
- **Timestamp:** Day 3, Part 1 [0:26:35 – 0:30:15]
- **Notes:** The History section includes fields for historical ticket count, customer paid total, hauler paid total, and children removed status. This supports archived-record handling by preserving key reporting values while preventing removed child records from triggering new billing, ticket, or line item activity.
- **Responsible:** TBD

## CUBE-PH4-D3-014
- **Group:** Core Platform
- **Category:** Notification
- **Epic:** Core Flow
- **Parent Task:** Recurring Billing Reminders
- **Task Name:** Track Recurring Billing Reminder Checks and Sent Status
- **User Story:** As an Account Manager (AM), I want recurring billing reminders to track whether a customer notification should be sent and whether it was already sent, so that upcoming billing cycle reminders are not missed or duplicated.
- **Description:** Recurring billing reminders can be used to notify customers before an upcoming billing cycle. The process tracks whether the reminder should be sent, whether it was sent, and when it was sent, so the same notification is not processed repeatedly.
- **Acceptance Criteria:** 1. System evaluates whether a recurring billing reminder should be sent, 2. System tracks the reminder check used by the billing reminder process, 3. System records whether the reminder was sent, 4. System records the date or time when the reminder was sent, 5. System prevents the same billing reminder from being sent repeatedly.
- **Timestamp:** Day 3, Part 1 [0:30:55 – 0:33:05]
- **Mockups:** NO MOCKUPS
- **Notes:** This process needs verification before implementation because it was unclear whether the recurring billing reminder process is still active. The fields discussed include the Monday email API check, reminder sent status, and sent timestamp.
- **Responsible:** TBD

## CUBE-PH4-D3-015
- **Group:** Toilets
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Product-Specific Fields
- **Task Name:** Show Toilet-Specific Fields Only When Relevant
- **User Story:** As an Account Manager (AM), I want toilet-specific fields to display only when they are relevant to the selected toilet setup, so that the form shows the correct accessory, setup, and event-related information without unnecessary fields.
- **Description:** Toilet records include unique setup and accessory fields that are not shared by all product lines. These fields support differences between construction recurring toilets and event toilets, as well as toilet-specific options such as holding tanks, event time, hand sanitizer, locking hasp, pump rates, restroom trailers, rigging cages, and water accessibility.
- **Acceptance Criteria:** 1. System displays toilet-specific fields only for toilet product records, 2. System shows event-related fields when the toilet setup is for an event, 3. System shows accessory-related rate fields only when the related accessory or setup applies, 4. System supports toilet-specific fields such as holding tank gallons, hand sanitizer rate, locking hasp rate, pump rate, restroom trailer type, rigging cage rate, and water accessibility, 5. System hides toilet-specific fields when they are not relevant to the selected toilet setup.
- **Timestamp:** Day 3, Part 1 [0:33:05 – 0:36:05]
- **Notes:** The screenshot lists toilet-specific setup and accessory fields used for product line handling. This story should focus on form behavior and field visibility, not on billing calculations. The form should avoid showing unnecessary toilet fields unless the selected setup, accessory, or event type requires them.
- **Responsible:** TBD

## CUBE-PH4-D3-016
- **Group:** Roll-Offs
- **Category:** Approval
- **Epic:** Core Flow
- **Parent Task:** New Jersey Approval
- **Task Name:** Require New Jersey Team Approval for New Jersey Roll-Off Jobs
- **User Story:** As a New Jersey Team member, I want roll-off jobs in New Jersey to require approval before the job proceeds, so that ZTERS meets the required approval process for New Jersey waste service operations.
- **Description:** Roll-off jobs located in New Jersey require approval from a member of the New Jersey Team before the job can proceed. This approval is specific to New Jersey roll-off work and must be completed by one of the users assigned to that team.
- **Acceptance Criteria:** 1. System identifies when a roll-off job is located in New Jersey, 2. System requires approval from the New Jersey Team before the job proceeds, 3. System prevents the New Jersey roll-off job from continuing without the required approval, 4. Approval records that the job was reviewed by an authorized New Jersey Team member, 5. Requirement applies specifically to roll-off jobs in New Jersey.
- **Timestamp:** Day 3, Part 1 [0:37:25 – 0:41:20]
- **Mockups:** NO MOCKUPS
- **Notes:** This approval is specific to New Jersey roll-off jobs and should not be treated as a general approval for all roll-offs. The New Jersey Team role is valid here because it is directly referenced as the group responsible for this approval.
- **Responsible:** TBD

## CUBE-PH4-D3-017
- **Group:** Roll-Offs
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Rebates
- **Task Name:** Capture Roll-Off Rebate Information When Recyclable Debris Applies
- **User Story:** As an Account Manager (AM), I want to capture rebate information for roll-off services when recyclable debris applies, so that expected rebates and rebate handling details can be tracked on the related service tickets.
- **Description:** Roll-off rebates apply when the debris type may be recyclable and may generate money back, such as recyclable metal. Rebate information should identify whether a rebate is expected and how the rebate should be handled.
- **Acceptance Criteria:** 1. System supports rebate fields for applicable roll-off services, 2. System identifies whether a rebate is expected for the roll-off debris type, 3. System captures how the rebate should be handled, 4. System carries rebate information into the related service ticket, 5. System shows rebate fields only when rebate information is applicable.
- **Timestamp:** Day 3, Part 1 [0:41:20 – 0:42:20]
- **Notes:** The shared screenshot is useful for roll-off context, but it does not directly show the rebate fields. It shows the Vendor and Rates section, including roll-off rate and disposal details. Keep this story focused on rebate handling for recyclable debris, and use a more specific rebate screenshot later if available.
- **Responsible:** TBD

## CUBE-PH4-D3-018
- **Group:** Roll-Offs
- **Category:** Notification
- **Epic:** Core Flow
- **Parent Task:** Auto Pull Reminder
- **Task Name:** Notify AM Before Auto Pull Rental Period Ends
- **User Story:** As an Account Manager (AM), I want to be notified before a roll-off auto pull occurs, so that I can inform the customer and coordinate an extension when the rental period is extendable.
- **Description:** Roll-off vendors may use automatic pull rules at the end of the rental period. When auto pull is selected, the AM should be notified before the dumpster is pulled so the customer can be informed or an extension can be coordinated when allowed.
- **Acceptance Criteria:** 1. System identifies roll-off records with auto pull selected, 2. System sends or displays a reminder before the scheduled auto pull, 3. Reminder notifies the AM that the dumpster will be pulled from the site, 4. Reminder indicates whether the auto pull is extendable or not extendable, 5. Reminder supports coordination with the service provider when the customer requests an extension.
- **Timestamp:** Day 3, Part 1 [0:42:20 – 0:44:20]
- **Mockups:** NO MOCKUPS
- **Notes:** Auto pull is specific to roll-off rentals where the vendor may remove the dumpster at the end of the rental period without a separate customer request. This reminder should help the AM notify the customer before the pull occurs and confirm whether an extension is possible.
- **Responsible:** TBD

## CUBE-PH4-D3-019
- **Group:** Zsight Monitors
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Product-Specific Fields
- **Task Name:** Support Zsight Monitor-Specific Fields and Recurring Bill Reminders
- **User Story:** As an Account Manager (AM), I want ZSight Monitor records to store monitor, QA, inventory, assignment, and installation information, so that ZSight camera details can be tracked in one place.
- **Description:** ZSight Monitor records store the information needed to identify, verify, assign, and track a monitor. The record includes monitor details such as serial number and ZSight FLID, QA information, inventory dates, storage location, assignment status, deployable status, out-of-service status, prototype status, notes, and installation notes.
- **Acceptance Criteria:** 1. System stores ZSight monitor identification fields such as serial number and ZSight FLID, 2. System tracks QA information such as QA status, QA by, and QA date, 3. System tracks inventory information such as inventory received date and storage location, 4. System stores monitor status fields such as assigned, deployable, out of service, and prototype, 5. System stores general notes and installation notes for the ZSight Monitor record.
- **Timestamp:** Day 3, Part 1 [0:47:45 – 0:48:45]
- **Notes:** The screenshot shows the ZSight Monitor record used to track camera details, QA status, inventory information, assignment status, and installation notes. This should be treated as a ZSight Monitor data management story, not as a Front Load or Container story.
- **Responsible:** TBD

## CUBE-PH4-D3-020
- **Group:** Fencing
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Product-Specific Fields
- **Task Name:** Support Fencing-Specific Rates and Accessories
- **User Story:** As an Account Manager (AM), I want fencing records to support fencing-specific rates, accessories, and billing cycle fields, so that fencing services can capture the required product-specific pricing and setup details.
- **Description:** Fencing products require additional product-specific information, including extra rates, accessories, secondary billing rates, and billing cycles. These fields support fencing setup and pricing details, even though the product-level process follows the same general pattern as other products.
- **Acceptance Criteria:** 1. System supports fencing-specific rate fields, 2. System supports fencing accessory fields, 3. System captures secondary billing rate information, 4. System captures fencing billing cycle information, 5. System keeps fencing-specific fields separate from unrelated product-line fields.
- **Timestamp:** Day 3, Part 1 [0:48:45 – 0:50:00]
- **Mockups:** NO MOCKUPS
- **Notes:** This should stay focused on fencing-specific fields and setup data. Fencing does not appear to have a unique product-level process in this section; the main difference is the number of extra rates, accessories, and billing cycle fields. Any primary vs. secondary cycle behavior should be handled in a separate ticket-level story if needed.
- **Responsible:** TBD

## CUBE-PH4-D3-021
- **Group:** Front Loads
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** ZSight Cameras
- **Task Name:** Relate ZSight Cameras to Front Load Records
- **User Story:** As an Account Manager (AM), I want ZSight Monitor records to be related to Front Load records, so that monitor details, installation information, and related photos can be tracked for monitored front load services.
- **Description:** ZSight Monitor records are related to front load services and can be used to track camera/monitor information, installation details, installer information, installation status, install dates, access code, notes, and photos. The monitor information is connected through the existing fulfillment ticket and hauler quote structure used for installation work.
- **Acceptance Criteria:** 1. System relates ZSight Monitor records to the applicable Front Load record, 2. System displays ZSight monitor details such as monitor ID, FLID, and installation status, 3. System captures installer and installation information, 4. System stores projected and actual install dates where available, 5. System supports ZSight installation notes and related installation photos.
- **Timestamp:** Day 3, Part 1 [0:50:00 – 0:52:30]
- **Notes:** Use ZSight as the product name. The screenshot shows the ZSight Monitor section inside a Hauler Quote used for ZSight installation work. The bottom section includes placement/installation photos, so this story should mention photo tracking if the user story is intended to cover the installation record, not only the front load relationship.
- **Responsible:** TBD

## CUBE-PH4-D3-022
- **Group:** Front Loads
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** ZSight Removal Warning
- **Task Name:** Display ZSight Camera Warning Before Front Load Removal
- **User Story:** As an Account Manager (AM), I want the system to warn me when a Front Load has a ZSight camera installed, so that the camera can be removed before a container removal is scheduled.
- **Description:** Front Load records with an installed ZSight camera should display a clear warning before a container removal is scheduled. The warning helps ensure the camera is removed first and prevents the container from being removed while the monitor is still installed.
- **Acceptance Criteria:** 1. System identifies when a Front Load record has an installed ZSight camera, 2. System displays a visible warning on the Front Load record, 3. Warning tells the user that the ZSight camera must be removed before container removal is scheduled, 4. Warning appears before the user proceeds with container removal, 5. Warning is not displayed when no ZSight camera is installed.
- **Timestamp:** Day 3, Part 1 [0:52:30 – 0:54:10]
- **Notes:** Use ZSight as the product name. The screenshot shows the exact warning banner displayed on the Front Load record. This story should focus on the warning shown before removal, not on ZSight monitor inventory or installation tracking.
- **Responsible:** TBD

## CUBE-PH4-D3-023
- **Group:** Front Loads
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** ZSight Installation Records
- **Task Name:** Use Fulfillment Ticket and Hauler Quote Structure for ZSight Installation Records
- **User Story:** As an Account Manager (AM), I want ZSight installation records to use the existing fulfillment ticket and hauler quote structure, so that installer details, installation status, verification fields, notes, and photos can be tracked through the established workflow.
- **Description:** ZSight installation and maintenance records reuse the existing fulfillment ticket and hauler quote workflow. The hauler quote is used to identify the installer and capture ZSight-specific installation information, including installation status, installer contact details, verification fields, notes, and related photos.
- **Acceptance Criteria:** 1. System supports ZSight installation or maintenance records through the existing fulfillment ticket structure, 2. System uses the hauler quote to identify the installer or installation vendor, 3. System captures ZSight installation status and installer contact details, 4. System stores ZSight-specific notes and verification fields, 5. System supports related ZSight installation photos where available.
- **Timestamp:** Day 3, Part 1 [0:52:30 – 0:56:30]
- **Mockups:** NO MOCKUPS
- **Notes:** Use ZSight as the product name. This story should be supported with the Hauler Quote screenshot that includes the ZSight Monitor section, not only the Front Load service information screenshot. The current Front Load screenshot helps with general Front Load context, but it does not show the full ZSight installation workflow.
- **Responsible:** TBD

## CUBE-PH4-D3-024
- **Group:** Front Loads
- **Category:** Data Management
- **Epic:** Core Flow
- **Parent Task:** ZSight Inventory
- **Task Name:** Track ZSight Camera Inventory Owned by ZTERS
- **User Story:** As an Account Manager (AM), I want ZTERS-owned ZSight cameras to be tracked as inventory records, so that serial numbers, QA status, storage location, assignment, deployment, and installation notes can be maintained.
- **Description:** ZSight cameras are owned by ZTERS and tracked as inventory records. Each camera record should store identification, QA, inventory, assignment, deployment, and installation information so the team can manage camera availability and usage.
- **Acceptance Criteria:** 1. System stores each ZSight camera as an inventory record, 2. System captures the camera serial number, 3. System captures QA status and QA details, 4. System captures inventory received date and storage location, 5. System tracks assignment, deployment, and installation notes.
- **Timestamp:** Day 3, Part 1 [0:56:54 – 1:00:20]
- **Mockups:** NO MOCKUPS
- **Notes:** Use ZSight as the product name. This story should focus on the camera inventory record, not the installation workflow. The inventory record is used to track the physical camera owned by ZTERS, including whether it has been QA’d, where it is stored, whether it is assigned or deployable, and any installation notes.
- **Responsible:** TBD

## CUBE-PH4-D3-025
- **Group:** Front Loads
- **Category:** Approval
- **Epic:** Core Flow
- **Parent Task:** Front Load Removal Approval
- **Task Name:** Require Approval Before Front Load Removal Ticket Creation
- **User Story:** As an Account Manager (AM), I want front load removals to require a removal request and approval before a removal ticket can be created, so that permanent services are not removed by mistake.
- **Description:** Front Loads are permanent services and are not expected to be removed frequently. Before a removal ticket can be created, the record should require a removal request, a removal reason, and the required approval.
- **Acceptance Criteria:** 1. System displays a removal request option for Front Load records, 2. System requires a removal request before the removal workflow can proceed, 3. System requires a removal reason before approval, 4. System requires approval before a removal ticket can be created, 5. System prevents Front Load removal ticket creation until the required approval is complete.
- **Timestamp:** Day 3, Part 1 [1:03:25 – 1:04:15]
- **Notes:** The screenshot shows the Removal Request checkbox in the Front Load service information section. This story should focus on the approval gate for Front Load removal, especially because these services are considered permanent and should not be removed accidentally.
- **Responsible:** TBD

## CUBE-PH4-D3-026
- **Group:** Front Loads
- **Category:** Reporting
- **Epic:** Core Flow
- **Parent Task:** New Service Classification
- **Task Name:** Identify Actual New Front Load Services Versus New Records for Existing Services
- **User Story:** As an Account Manager (AM), I want to distinguish actual new Front Load services from new records created for existing services, so that reporting can accurately separate new service setup from hauler migration records.
- **Description:** Front Load records may be created either for an actual new service or because an existing service was moved to a different hauler. The system should identify this difference so reporting does not count hauler migration records as new services.
- **Acceptance Criteria:** 1. System captures whether a Front Load record represents an actual new service, 2. System distinguishes actual new service setup from records created for existing services, 3. System supports reporting based on the new service classification, 4. System preserves historical separation when a service moves to a different hauler, 5. System prevents hauler migration records from being counted as actual new services.
- **Timestamp:** Day 3, Part 1 [1:04:15 – 1:05:35]
- **Mockups:** NO MOCKUPS
- **Notes:** This story is mainly for reporting accuracy. Front Load records can be recreated when the service changes haulers, but those records should not always count as new services. The classification helps keep service growth and migration reporting clean.
- **Responsible:** TBD

## CUBE-PH4-D3-027
- **Group:** Grease Traps
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Expected Service Date
- **Task Name:** Calculate Grease Trap Next Expected Service Date from Frequency
- **User Story:** As an Account Manager (AM), I want grease trap records to calculate the next expected service date from the service frequency, so that upcoming grease trap services can be tracked without treating them as fixed rental cycles.
- **Description:** Grease traps use a frequency of service to estimate when the next service should occur. For example, a 90-day frequency can be used to calculate the next expected service date, but the actual service may still depend on customer follow-up and whether the grease trap is ready to be serviced.
- **Acceptance Criteria:** 1. System stores the grease trap frequency of service, 2. System calculates the next expected service date using the last service date and frequency, 3. System treats the calculated date as an expected service date rather than a fixed rental cycle end date, 4. System supports reporting for upcoming expected grease trap services, 5. System allows the actual service date to differ from the expected service date.
- **Timestamp:** Day 3, Part 1 [1:06:20 – 1:12:20]
- **Notes:** The screenshot shows the Grease Trap service information section with Frequency of Service = 90 Days. This story should focus on expected scheduling logic, not on creating a strict recurring rental cycle. Grease trap service timing is more flexible because the service may happen later depending on customer confirmation and actual need.
- **Responsible:** TBD

## CUBE-PH4-D3-028
- **Group:** Grease Traps
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Grease Trap Service Tickets
- **Task Name:** Use Grease Trap Service Date as the Actual Service Date
- **User Story:** As an Account Manager (AM), I want grease trap service tickets to use a service date for the actual service, so that the ticket reflects when the grease trap service is scheduled or performed instead of treating it as a rental cycle.
- **Description:** Grease trap service tickets use a service date to represent when the actual service is expected or performed. The date should not be treated as the start of a rental cycle. Grease trap scheduling uses the service date for the current service and a separate expected date for the next service.
- **Acceptance Criteria:** 1. System displays a service ticket option using the grease trap service date, 2. System treats the service date as the actual scheduled service date, 3. System does not treat grease trap service tickets as a start-to-end rental cycle, 4. System supports a separate next expected service date for future follow-up, 5. Grease trap service ticket reporting uses the service date instead of a rental cycle range.
- **Timestamp:** Day 3, Part 1 [1:10:20 – 1:15:50]
- **Notes:** The screenshot shows the Grease Trap Create Service Ticket section with a service button tied to a specific date. This story should focus on how grease trap service tickets use the actual service date, while the previous story covers how the next expected service date is calculated from the frequency of service.
- **Responsible:** TBD

## CUBE-PH4-D3-029
- **Group:** Permanent Roll-Offs
- **Category:** Approval
- **Epic:** Core Flow
- **Parent Task:** Permanent Service Removal Approval
- **Task Name:** Require Removal Approval for Permanent Roll-Offs
- **User Story:** As an Account Manager (AM), I want permanent roll-off removals to require a removal request and approval before removal can proceed, so that permanent services are not removed without the required review.
- **Description:** Permanent Roll-Offs follow the same CWS removal control concept discussed for Front Loads. Because these services are intended to be permanent, a removal request and approval should be required before a removal ticket can be created.
- **Acceptance Criteria:** 1. System requires a removal request before a Permanent Roll-Off removal can proceed, 2. System requires approval before a removal ticket can be created, 3. System prevents Permanent Roll-Off removal ticket creation until approval is complete, 4. System applies the removal approval workflow to Permanent Roll-Off records, 5. System supports the CWS removal control approach used for permanent services.
- **Timestamp:** Day 3, Part 1 [1:15:50 – 1:16:50]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should stay separate from the Front Load removal approval story because the same approval concept applies to a different product line. Permanent Roll-Off removals should be controlled because removing a permanent service usually means the service is ending or the contract is being lost.
- **Responsible:** TBD

## CUBE-PH4-D3-030
- **Group:** Permanent Roll-Offs
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Waste Diversion
- **Task Name:** Track Waste Diversion Separately from Rebates
- **User Story:** As an Account Manager (AM), I want Permanent Roll-Offs to track waste diversion separately from rebates, so that landfill diversion and monetary rebate tracking remain distinct.
- **Description:** Waste diversion identifies whether material from a Permanent Roll-Off was diverted from a landfill and sent to a recycling or processing center. This is different from rebate tracking because diverted material may not always generate money back.
- **Acceptance Criteria:** 1. System captures whether waste was diverted from a landfill, 2. System keeps waste diversion tracking separate from rebate tracking, 3. System supports recyclable material reporting for Permanent Roll-Offs, 4. System allows diverted material to be tracked even when no rebate applies, 5. System supports rebate tracking separately when recyclable material has monetary value.
- **Timestamp:** Day 3, Part 1 [1:16:50 – 1:18:40]
- **Mockups:** NO MOCKUPS
- **Notes:** Waste diversion should be used to support recycling or landfill-diversion reporting. Rebates should remain separate because some recyclable materials may be diverted without generating money back, while other materials, such as scrap metal, may qualify for a rebate.
- **Responsible:** TBD

## CUBE-PH4-D3-031
- **Group:** Permanent Roll-Offs
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Vendor Selection
- **Task Name:** Support Multiple Vendor Roles for Permanent Roll-Offs
- **User Story:** As an Account Manager (AM), I want Permanent Roll-Offs to support multiple vendor links, so that different vendors can be assigned for disposal, equipment rental, installation, maintenance, and monitor rental.
- **Description:** Permanent Roll-Offs can require multiple vendors because different companies may handle different parts of the service. A vendor link should connect the Permanent Roll-Off or compactor record to the selected vendor and identify the vendor service role.
- **Acceptance Criteria:** 1. System allows a Permanent Roll-Off or compactor record to have multiple vendor links, 2. System allows users to select the vendor for each vendor link, 3. System captures the vendor service role for the selected vendor, 4. System supports vendor roles such as disposal, equipment rental, installation, maintenance, and monitor rental, 5. System displays vendor eligibility indicators such as whether the vendor can be used.
- **Timestamp:** Day 3, Part 1 [1:18:40 – 1:25:45]
- **Notes:** The screenshot shows the Vendor Link form for a Perm Roll-Off/Compactor record. This story should focus on setting up multiple vendor relationships for the same permanent service. Vendor links are important because Permanent Roll-Offs may use separate vendors for disposal, rental, installation, maintenance, or monitor-related services.
- **Responsible:** TBD

## CUBE-PH4-D3-032
- **Group:** Permanent Roll-Offs
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Item Receipts
- **Task Name:** Associate Permanent Roll-Off Tickets and Line Items to the Correct Vendor Role
- **User Story:** As an Account Manager (AM), I want Permanent Roll-Off tickets and line items to be associated with the correct vendor role, so that item receipts can be created for the appropriate vendor.
- **Description:** Permanent Roll-Offs can include different charge types, such as setup, rental, haul, monitor rental, dry run, relocation, contamination, and other rates. Each charge should be associated with the correct vendor role so item receipts can be generated for the vendor responsible for that service.
- **Acceptance Criteria:** System identifies the vendor role related to each Permanent Roll-Off charge, 2. System supports setup charges tied to the installation or setup vendor, 3. System supports rental or monitor rental charges tied to the appropriate rental vendor, 4. System supports haul charges tied to the waste disposal vendor, 5. System supports item receipt creation when the correct vendor relationship is available.
- **Timestamp:** Day 3, Part 1 [1:21:40 – 1:25:45]
- **Notes:** The screenshot shows Permanent Roll-Off vendor rates grouped by setup, rental, haul, fees/taxes, and additional rates. This story should stay focused on connecting each charge type to the correct vendor role so the item receipt process can identify who should be paid.
- **Responsible:** TBD

## CUBE-PH4-D3-033
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Core Flow
- **Parent Task:** Product Master
- **Task Name:** Define Product Master Tables for Product Lines, Product Types, Ticket Codes, and Product Codes
- **User Story:** As an Account Manager (AM), I want product lines, product types, ticket codes, and product codes to be defined in the product master structure, so that products, tickets, and line items can use the correct business logic.
- **Description:** The product master structure defines how product lines, product types, ticket codes, and product codes relate to each other. Product lines identify the main product categories, product types identify the specific products, ticket codes define applicable service ticket types, and product codes support line item combinations.
- **Acceptance Criteria:** 1. System stores product line records for the main product categories, 2. System stores product type records under the applicable product line, 3. System stores ticket code records for applicable service ticket types, 4. System stores product code records used for line item combinations, 5. Product master relationships support product, ticket, and line item logic.
- **Timestamp:** Day 3, Part 1 [1:41:40 – 1:48:10]
- **Notes:** The diagram shows the product master relationship between Products, Product Types, Ticket Codes, and Product Codes. This should stay as the high-level data model story. More detailed stories can cover product code construction, line item satisfaction, and Intacct/Avalara billing behavior separately.
- **Responsible:** TBD

## CUBE-PH4-D3-034
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Core Flow
- **Parent Task:** Product Code Redesign
- **Task Name:** Preserve Required Intacct Product Code Concepts During CUBE Redesign
- **User Story:** As an Account Manager (AM), I want CUBE to preserve the required Intacct product code logic during any product master redesign, so that billing can continue using the correct product code, product line, and tax code information.
- **Description:** CUBE may redesign the current product master structure, but the final billing outputs still need to remain compatible with Intacct. Any redesign must preserve the logic needed to generate or identify the correct product code, product line, and tax code for line items.
- **Acceptance Criteria:** 1. System preserves the ability to generate or identify the required Intacct product code, 2. System preserves the product line information required for billing, 3. System preserves the tax code information required for billing and tax processing, 4. Product master redesign does not break line item billing outputs, 5. Existing working logic can be replicated if a full redesign is not feasible for MVP.
- **Timestamp:** Day 3, Part 1 [1:48:14 – 1:50:36]
- **Notes:** The full diagram shows that product master data eventually feeds Product Tickets and Line Items. The database structure can be improved in CUBE, but the billing outputs still need to match what Intacct requires. This should be treated as a redesign guardrail, not as a requirement to copy the current QuickBase structure exactly.
- **Responsible:** TBD

## CUBE-PH4-D3-035
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Service Ticket Buttons
- **Task Name:** Create Service Tickets from Product-Level Buttons with Predefined Ticket Codes
- **User Story:** As an Account Manager (AM), I want product-level service ticket buttons to create the correct service ticket type, so that delivery, rental, removal, and other service tickets are generated with the appropriate predefined ticket code.
- **Description:** Product-level service ticket buttons are configured to create specific ticket types. When a user selects a button, the ticket opens with the predefined ticket code and relevant product information copied from the parent product record.
- **Acceptance Criteria:** 1. System opens a new service ticket from the selected product-level button, 2. System applies the predefined ticket code associated with the selected button, 3. System copies relevant product information into the new service ticket, 4. Delivery buttons create delivery ticket records where applicable, 5. Rental and removal buttons create the corresponding ticket records where applicable.
- **Timestamp:** Day 3, Part 1 [1:50:36 – 1:54:40]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on how product-level buttons create the correct service ticket type. The ticket code is already predefined by the button, and the new ticket receives copied product information from the parent product record.
- **Responsible:** TBD

## CUBE-PH4-D3-036
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** Core Flow
- **Parent Task:** Product Type Filtering
- **Task Name:** Filter Product Type Options by Product Line and Category
- **User Story:** As an Account Manager (AM), I want product type options to be filtered by product line and category, so that I can select only the product types that are relevant to the current product setup.
- **Description:** Product type options are filtered based on the selected product line and category. For example, when the toilet category is set to Event, the Product Type dropdown should show only event-related toilet product types.
- **Acceptance Criteria:** 1. System filters product type options based on the selected product line, 2. System filters product type options based on the selected category when category metadata applies, 3. System shows event-related toilet product types when the category is Event, 4. System hides unrelated product types from the dropdown, 5. System allows the user to select only product types that match the current product setup.
- **Timestamp:** Day 3, Part 1 [1:54:40 – 1:57:20]
- **Notes:** The screenshot shows the Product Type dropdown filtered after Category is set to Event. This story should focus on dropdown filtering and selection accuracy. The filtering helps prevent users from selecting product types that do not match the selected product line or category.
- **Responsible:** TBD

## CUBE-PH4-D3-037
- **Group:** Core Platform
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Line Item Availability
- **Task Name:** Enable Line Item Creation Only When Required Conditions Are Met
- **User Story:** As an Account Manager (AM), I want line item creation buttons to appear only when the required conditions are met, so that line items are created only when they are applicable, valid, and ready for billing.
- **Description:** Line item creation depends on several ticket and billing conditions. The system should make a line item button available only when the required rates, billing preference, ticket code, product code, and line item status conditions are satisfied.
- **Acceptance Criteria:** 1. System checks that the required rates are available, 2. System checks that the billing preference is valid and portal ready, 3. System validates the applicable ticket code and product code logic, 4. System checks whether the required line item already exists, 5. System displays only the line item buttons that are applicable to the current ticket context.
- **Timestamp:** Day 3, Part 1 [1:57:20 – 2:03:20]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on button availability and validation before line item creation. The button should not appear just because the ticket exists; the required billing, product code, and line item conditions must also be satisfied.
- **Responsible:** TBD

## CUBE-PH4-D3-038
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Line Item Creation
- **Task Name:** Open New Line Items with Inserted Values Without Auto-Saving
- **User Story:** As an Account Manager (AM), I want line item buttons to open a new line item with prefilled values without automatically saving it, so that I can review the generated billing details before creating the record.
- **Description:** Line item buttons open a new line item in add/edit mode and insert relevant values from the ticket, product, customer, site, vendor, and billing preference. The record should remain unsaved until the user reviews the information and saves it manually.
- **Acceptance Criteria:** 1. System opens a new line item in add/edit mode after the user clicks the line item button, 2. System prepopulates customer, site, ticket, vendor, and product code information where applicable, 3. System prepopulates billing information such as billing preference, billing company, billing email, billing address, and payment details where available, 4. System does not automatically save the new line item, 5. User can review the inserted values before saving the record.
- **Timestamp:** Day 3, Part 1 [2:05:09 – 2:07:10]
- **Notes:** The screenshot shows the Add Line Item page with multiple values already inserted, including product code, related vendor, related ticket, billing preference, billing company, billing email, and payment details. This story should focus on review-before-save behavior, not on button availability.
- **Responsible:** TBD

## CUBE-PH4-D3-039
- **Group:** Core Platform
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Intacct Product Codes
- **Task Name:** Generate Related Product Code for Intacct and Tax Processing
- **User Story:** As an Account Manager (AM), I want line items to generate the correct related product code, so that billing and tax processing can use the required Intacct product code information.
- **Description:** Line items use product, product type, service type, state, and other required values to generate or identify the related product code. The product code is then used to support Intacct billing and tax processing.
- **Acceptance Criteria:** 1. System generates or identifies the related product code for the line item, 2. System uses product, product type, service type, and state information where applicable, 3. System displays the product code on the line item record, 4. System uses the product code to support Intacct billing requirements, 5. System uses the related product code information to support tax code processing.
- **Timestamp:** Day 3, Part 1 [2:07:10 – 2:12:00]
- **Notes:** The screenshot shows the Product Code field populated on the Add Line Item page. This story should focus on how the line item receives the correct product code for Intacct and tax processing, not on the general prefilled values behavior covered in the previous story.
- **Responsible:** TBD

## CUBE-PH4-D3-040
- **Group:** Core Platform
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Required Line Items
- **Task Name:** Validate Required Core Product Line Items for Tickets
- **User Story:** As an Account Manager (AM), I want tickets to validate whether the required core product line item exists, so that a ticket is not considered complete when only optional or non-core line items have been added.
- **Description:** Tickets may require a core product line item to satisfy the standard charge requirement. Optional line items, such as winterization, insurance, or miscellaneous charges, should not satisfy the main required charge unless the required core product line item also exists.
- **Acceptance Criteria:** 1. System identifies the required core product line item for the ticket, 2. System checks whether the required core product line item exists, 3. System does not treat insurance, winterization, or miscellaneous line items as the required core product line item, 4. System keeps the ticket incomplete when the required core product line item is missing, 5. System updates the standard charge status based on required line item completion.
- **Timestamp:** Day 3, Part 1 [2:12:00 – 2:18:30]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on ticket completion and line item satisfaction. Optional line items can exist on the ticket, but they should not satisfy the required standard charge unless the core product line item is also present.
- **Responsible:** TBD

## CUBE-PH4-D3-041
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Invoicing Requirements
- **Task Name:** Determine When Line Item Invoicing Is Required
- **User Story:** As an Account Manager (AM), I want tickets to determine when line item invoicing is required, so that billing requirements are evaluated correctly before invoicing.
- **Description:** Line item invoicing requirements are determined from ticket status, cancellation status, product-specific rules, and required line item logic. The system should identify whether a ticket still needs invoicing action before it can be considered complete from a billing perspective.
- **Acceptance Criteria:** 1. System evaluates whether line items are required for the ticket, 2. System evaluates whether the ticket has been canceled, 3. System applies product-specific invoicing requirement rules, 4. System supports special invoicing requirements such as California and Indiana additional rental handling, 5. System uses the resulting status to determine whether invoicing action is still required.
- **Timestamp:** Day 3, Part 1 [2:18:30 – 2:24:40]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on billing status and invoicing readiness. It should stay separate from the required core line item story because a ticket may have line item requirements, cancellation rules, product-specific billing rules, and state-specific exceptions that all affect whether invoicing is still required.
- **Responsible:** TBD

## CUBE-PH4-D3-042
- **Group:** Core Platform
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Item Receipt Process
- **Task Name:** Create Item Receipt Inputs When Vendor Payment Is Ready
- **User Story:** As an Account Manager (AM), I want service tickets to provide the required vendor payment information when vendor payment is ready, so that item receipt inputs can be created for the appropriate vendor.
- **Description:** Item receipt processing depends on vendor payment information captured on the service ticket. When the ticket is ready for vendor payment, the process should use the required vendor payment fields, payment method, total hauler charge, and related PO information to support item receipt creation.
- **Acceptance Criteria:** 1. System identifies when a service ticket is ready for vendor payment, 2. System captures the total hauler charge required for vendor payment, 3. System captures the vendor payment method where available, 4. System captures the related PO number where available, 5. System supports item receipt creation when the required vendor payment information is available.
- **Timestamp:** Day 3, Part 1 [2:24:40 – 2:27:30]
- **Notes:** The screenshot shows the Vendor Payment section on a service ticket, including total hauler charge, payment method, and PO number. This story should focus on the ticket-level inputs needed for item receipt processing, not on vendor role setup.
- **Responsible:** TBD

## CUBE-PH4-D3-043
- **Group:** Core Platform
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Opt-Outs and Cancellation
- **Task Name:** Apply Opt-Out and Cancellation Logic Across Customer, Site, and Product Levels
- **User Story:** As an Account Manager (AM), I want opt-out and cancellation logic to apply across customer, site, and product levels, so that billing, ticket creation, and cancellation behavior are controlled consistently.
- **Description:** Opt-out logic can apply at the customer, site, and product levels. Cancellation logic must also prevent users from canceling records incorrectly when related line items or billing activity still need to be handled first.
- **Acceptance Criteria:** System supports opt-outs at the customer level, 2. System supports opt-outs at the site level, 3. System supports opt-outs at the product level, 4. System prevents ticket cancellation when active non-canceled line items exist, 5. System requires line item cancellation or credit handling before the related ticket can be canceled.
- **Timestamp:** Day 3, Part 1 [2:27:30 – 2:30:20]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should cover both opt-out inheritance and cancellation guardrails. Opt-outs help prevent records from continuing through automated creation or billing when they should be excluded. Cancellation should work backward, meaning line items or credits must be handled before the parent ticket can be canceled.
- **Responsible:** TBD

## CUBE-PH4-D3-044
- **Group:** Roll-Offs
- **Category:** Functional Logic
- **Epic:** Core Flow
- **Parent Task:** Tonnage Status
- **Task Name:** Calculate Roll-Off Additional Tonnage Requirements After Final Tonnage Is Entered
- **User Story:** As an Account Manager (AM), I want roll-off tickets to calculate additional tonnage requirements after final tonnage is entered, so that extra tonnage charges can be identified when the included tons are exceeded.
- **Description:** Roll-off tickets require final tonnage after the haul is completed. The system compares the final tonnage against the included tons and calculates any required additional tonnage so the correct tonnage line item can be created when needed.
- **Acceptance Criteria:** System captures final tonnage after the roll-off haul is completed, 2. System compares final tonnage against the included tons, 3. System calculates required additional tonnage when final tonnage exceeds the included tons, 4. System identifies when a tonnage line item is required, 5. System allows the ticket to proceed when tonnage is marked unavailable.
- **Timestamp:** Day 3, Part 1 [2:30:20 – 2:34:30]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on roll-off tonnage status after the haul occurs. Final tonnage is needed to determine whether additional tonnage charges apply. If the vendor does not provide tonnage, the ticket can still move forward by marking tonnage as unavailable.
- **Responsible:** TBD

## CUBE-PH4-D3-045
- **Group:** Grease Traps
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Grease Trap Verification
- **Task Name:** Track Grease Trap Verification and Manifest Fields
- **User Story:** As an Account Manager (AM), I want grease trap tickets to include verification and manifest tracking fields, so that completed grease trap services can be reviewed and confirmed after the service.
- **Description:** Grease trap tickets include manual tracking fields used to verify completed service activity. These fields help users confirm whether the grease trap service was reviewed after completion and whether a required manifest was received.
- **Acceptance Criteria:** 1. System supports grease trap verification fields on grease trap tickets, 2. System supports manifest received tracking where a manifest is required, 3. System allows users to mark completed verification steps, 4. System keeps grease trap verification fields specific to grease trap tickets, 5. System supports operational follow-up without triggering additional billing or automation logic.
- **Timestamp:** Day 3, Part 1 [2:34:30 – 2:37:20]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on manual post-service verification for grease trap tickets. The verification and manifest fields are used for operational tracking after the service is completed, not for calculating the service date or creating the ticket.
- **Responsible:** TBD

## CUBE-PH4-D3-046
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Core Flow
- **Parent Task:** Product Master Tables
- **Task Name:** Maintain Product Line, Product Type, Ticket Code, and Product Code Definitions
- **User Story:** As an Account Manager (AM), I want product master tables to maintain product line, product type, ticket code, and product code definitions, so that CUBE can determine which products, tickets, and line items are valid throughout the core flow.
- **Description:** Product master tables maintain the definitions used to support product setup, ticket creation, line item validation, and billing logic. These tables include product lines, product types, ticket codes, and product codes used to determine valid combinations throughout the flow.
- **Acceptance Criteria:** System maintains product line records with product line codes, 2. System maintains product type records with granular product information, 3. System maintains ticket code records with applicable and required line item metadata, 4. System maintains product code records used for line item and billing logic, 5. Product master definitions support filtering, validation, and billing behavior throughout the core flow.
- **Timestamp:** Day 3, Part 1 [2:37:20 – 2:47:50]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should stay only if it is positioned as a master data maintenance story. D3-033 already covers the high-level product master structure, so this one should focus on maintaining the definitions and metadata that drive product setup, ticket validation, line item logic, and billing behavior.
- **Responsible:** TBD

## CUBE-PH4-D3-047
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Core Flow
- **Parent Task:** Product Code Construction
- **Task Name:** Build Product Code Combinations from Product, Ticket, Debris, and State Values
- **User Story:** As an Account Manager (AM), I want product code combinations to be built from product, ticket, debris, state, and related values, so that CUBE can generate the correct product code for line items and billing.
- **Description:** Product code combinations are built by combining multiple values from the product and ticket flow. These values may include product abbreviation, product type, ticket code, debris or descriptor values, and state information used to match the required billing code structure.
- **Acceptance Criteria:** 1. System uses product abbreviation in product code construction, 2. System uses ticket code in product code construction, 3. System uses debris or descriptor values when applicable, 4. System uses state information for state-specific product code combinations, 5. System builds product code combinations that support line item and billing requirements.
- **Timestamp:** Day 3, Part 1 [2:47:50 – 3:00:20]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on the construction logic behind product codes. Product code values are not based on a single field; they are assembled from multiple product, ticket, location, and descriptor values. Keep this separate from the Intacct story, which focuses on the final billing output.
- **Responsible:** TBD

## CUBE-PH4-D3-048
- **Group:** Core Platform
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Hub Billing Flow
- **Task Name:** Send Product Code, Tax Code, and Product Line to Hub for Invoicing
- **User Story:** As an Account Manager (AM), I want line item billing data to be sent to Hub with product code, tax code, product line, and relevant billing information, so that Hub can create the invoice and send the result to Intacct.
- **Description:** Line item billing data is sent to Hub for invoice processing. The data sent to Hub should include the product code, tax code, product line, and other relevant billing details required to create the invoice and support the downstream Intacct process.
- **Acceptance Criteria:** 1. System sends line item billing data to Hub, 2. System includes the product code in the data sent to Hub, 3. System includes the tax code in the data sent to Hub, 4. System includes the product line in the data sent to Hub, 5. Hub uses the received line item data to support invoice creation and Intacct processing.
- **Timestamp:** Day 3, Part 1 [3:00:20 – 3:05:10]
- **Mockups:** NO MOCKUPS
- **Notes:** This story should focus on the handoff from CUBE/QuickBase line items to Hub for billing. Product code construction and Intacct code logic are covered in separate stories; this one is specifically about sending the required billing data to Hub so invoicing can continue downstream.
- **Responsible:** TBD

## CUBE-PH4-D3-049
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Core Flow
- **Parent Task:** Field Relationship Mapping
- **Task Name:** Map Product Master Fields Through Products, Tickets, Product Codes, and Line Items
- **User Story:** As an Account Manager (AM), I want key product master fields to flow through products, tickets, product codes, and line items, so that filtering, validation, line item satisfaction, and billing logic can work correctly.
- **Description:** Product master fields are passed through the core flow using lookups, summaries, predefined ticket codes, formula-generated product codes, and values injected by create buttons. These relationships help determine which product types, tickets, and line items are valid at each step.
- **Acceptance Criteria:** 1. System maps product master fields into product records, 2. System maps ticket code fields into product tickets, 3. System summarizes line item information back to the related ticket where needed, 4. System passes required product code information into line items, 5. Field relationships support filtering, validation, line item satisfaction, and billing logic.
- **Timestamp:** Day 3, Part 1 [3:05:10 – 3:11:33]
- **Notes:** The diagram shows how product master data flows from Products, Product Types, Ticket Codes, and Product Codes into Product Tickets and Line Items. This story should focus on field movement and relationship mapping across the flow, not on defining the product master tables themselves.
- **Responsible:** TBD

## CUBE-PH4-D3-050
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Core Flow
- **Parent Task:** Product Code Management
- **Task Name:** Modify Product Codes Only When Product or Service Definitions Change
- **User Story:** As an Account Manager (AM), I want product codes and ticket definitions to be modified only when a new product, service, product type, or billing distinction is added, so that the product master setup remains stable unless a fundamental change is required.
- **Description:** Product code and ticket definition changes should be limited to fundamental product or billing changes. New product codes may be needed when a new product, service, product type, or line-item-level billing distinction is introduced.
- **Acceptance Criteria:** 1. System allows product code updates when a new product or service is added, 2. System allows product code updates when a new product type is added, 3. System supports new product codes for billing distinctions such as winterization or insurance, 4. Ticket type definitions remain unchanged unless the service definition requires a change, 5. Product code setup remains stable when no fundamental product or billing change exists.
- **Timestamp:** Day 3, Part 2 [0:25 – 1:15]
- **Mockups:** NO MOCKUPS
- **Notes:** This is mainly a product master maintenance rule. Ticket types rarely change, while product codes are added when new line-item-level distinctions are needed. This helps avoid unnecessary changes to a complex product code structure.
- **Responsible:** TBD

## CUBE-PH4-D3-051
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Core Flow
- **Parent Task:** Line Item Satisfaction
- **Task Name:** Summarize Line Item Status Back to Product Tickets
- **User Story:** As an Account Manager (AM), I want line item information to summarize back to the product ticket, so that the ticket can determine whether required line items, core product line items, and additional rental requirements are satisfied.
- **Description:** Line item information is summarized back to the related product ticket to support ticket status, line item satisfaction, and operational guardrails. These summaries help determine whether the ticket has the required core product line item, whether additional rental requirements apply, and whether required line item conditions are complete.
- **Acceptance Criteria:** 1. System summarizes core product line item status back to the related product ticket, 2. System summarizes additional rental line item status where applicable, 3. System identifies whether required line items are missing, 4. System uses summarized line item information to update ticket status, 5. System supports ticket-level validation based on line item completion.
- **Timestamp:** Day 3, Part 2 [2:50 – 5:35]
- **Mockups:** NO MOCKUPS
- **Notes:** Important for ticket statuses and operational dashboards. This supports whether a ticket is ready, incomplete, or still missing required billing actions. It should stay focused on the summary relationship between line items and product tickets, not on the creation of the line items themselves.
- **Responsible:** TBD

## CUBE-PH4-D3-052
- **Group:** Core Platform
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Service Ticket Availability
- **Task Name:** Control Service Ticket Button Availability Using Product Criteria and Existing Tickets
- **User Story:** As an Account Manager (AM), I want service ticket buttons to appear only when the product criteria and existing ticket conditions allow them, so that users can create only valid service tickets.
- **Description:** Service ticket button availability depends on product-level criteria and existing ticket activity. The system should evaluate dates, charges, existing ticket counts, ticket types, and required prior actions before allowing users to create a new service ticket.
- **Acceptance Criteria:** 1. System evaluates required product dates before allowing ticket creation, 2. System evaluates required charges before allowing ticket creation, 3. System checks existing ticket counts and ticket types, 4. System blocks ticket creation when required prior ticket activity is incomplete, 5. System displays only service ticket buttons that are valid for the current product context.
- **Timestamp:** Day 3, Part 2 [7:50 – 12:20]
- **Mockups:** NO MOCKUPS
- **Notes:** Ticket codes may be predefined in the buttons, but button visibility depends on additional product and operational criteria outside the product master relationship. This story should focus on the guardrails that decide whether a ticket button is available.
- **Responsible:** TBD

## CUBE-PH4-D3-053
- **Group:** Core Platform
- **Category:** Workflow Validation
- **Epic:** Core Flow
- **Parent Task:** Line Item Automation Decision
- **Task Name:** Keep Standard Line Item Creation Reviewable Before Invoice Creation
- **User Story:** As an Account Manager (AM), I want standard line item creation to remain reviewable before invoice creation, so that amounts, taxes, and billing details can be checked before the actual invoice is created.
- **Description:** Standard line items may be eligible for automation in some cases, but users still need a review point before invoice creation. The current process allows line item amounts to be checked, and the draft invoice also provides another review point for taxes, state, and final invoice details.
- **Acceptance Criteria:** 1. System allows users to review standard line items before invoice creation, 2. System allows users to verify line item amounts before invoicing, 3. System supports draft invoice review after line item creation, 4. Draft invoice review includes tax, state, and billing amount validation, 5. Full automation of standard line item creation requires stakeholder confirmation before implementation.
- **Timestamp:** Day 3, Part 2 [12:26 – 15:10]
- **Mockups:** NO MOCKUPS
- **Notes:** Do not treat full automation as a confirmed requirement. Some standard line items may be possible to automate, but review checkpoints are still important because users currently check both the line item and the draft invoice before the final invoice is created.
- **Responsible:** TBD

## CUBE-PH4-D3-054
- **Group:** Core Platform
- **Category:** Reporting
- **Epic:** Core Flow
- **Parent Task:** Operational Dashboard Tasks
- **Task Name:** Display Missing Billing and Line Item Tasks on Operational Dashboards
- **User Story:** As an Account Manager (AM), I want operational dashboards to show missing line items, billing-required items, tonnage-required items, unpaid items, and related pending tasks, so that I can identify the work that still needs to be completed.
- **Description:** Operational dashboards should summarize pending work based on ticket and billing statuses. Instead of sending individual notifications for each missing line item or billing task, the dashboard should show grouped counts and reports that help users find records requiring action.
- **Acceptance Criteria:** 1. System displays records with missing required line items on operational dashboards, 2. System displays billing-required records on operational dashboards, 3. System displays tonnage-required roll-off records where applicable, 4. System displays billed but unpaid records for follow-up, 5. System groups pending work through statuses, reports, or summary counts.
- **Timestamp:** Day 3, Part 2 [15:13 – 18:45]
- **Mockups:** NO MOCKUPS
- **Notes:** This should be handled through dashboard reporting, not individual bell notifications or emails. The dashboard is the operational place where users identify what still needs line items, billing, tonnage completion, payment follow-up, or other pending action.
- **Responsible:** TBD

## CUBE-PH4-D3-055
- **Group:** Core Platform
- **Category:** Integration
- **Epic:** Core Flow
- **Parent Task:** Line Item Webhooks
- **Task Name:** Restrict Line Item Webhook Updates to Creation, Cancellation, Credit Approval, and Recurring Billing Process Changes
- **User Story:** As an Account Manager (AM), I want line item webhook updates to be limited to approved update events, so that Hub/MySQL receives controlled changes for creation, cancellation, credit approval, and recurring billing processing.
- **Description:** Line items are sent to Hub/MySQL when they are created, but general edits should not trigger unrestricted webhook updates. Only specific events should update Hub/MySQL, including cancellation, credit line item approval, and recurring bill process changes.
- **Acceptance Criteria:** 1. System sends line item data to Hub when the line item is created, 2. System sends a webhook update when a line item is canceled, 3. System sends a webhook update when a credit line item is approved, 4. System sends a webhook update when the recurring bill process field changes, 5. System does not send unrestricted webhook updates for general line item edits.
- **Timestamp:** Day 3, Part 2 [43:50 – 48:35]
- **Mockups:** NO MOCKUPS
- **Notes:** Line items are intentionally locked down after creation. If users make a mistake, the expected process is to cancel the line item and recreate it. General edits should not trigger broad webhook updates because Hub/MySQL should only receive controlled line item changes.
- **Responsible:** TBD

---

# Day 4

**Stories:** 36

## CUBE-PH4-D4-001
- **Group:** Core Platform
- **Category:** Documentation
- **Epic:** Core Flow Reference
- **Parent Task:** Data Mapping Reference
- **Task Name:** Document Product Ticket Matrix
- **User Story:** As a CUBE developer, I want a product ticket reference matrix that identifies service ticket, fulfillment ticket, and line item applicability by product line so that ticket setup rules can be standardized across CUBE.
- **Description:** The product ticket matrix defines which ticket types and line items apply to each product line. It identifies whether each item is always applicable, sometimes applicable, not applicable, or dependent on specific conditions such as rates or service type. This matrix is used as a reference when standardizing service ticket behavior across CUBE.
- **Acceptance Criteria:** 1. The matrix lists each product line covered by the core flow, 2. The matrix identifies the ticket types associated with each product line, 3. The matrix indicates whether each ticket type is always applicable, sometimes applicable, or not applicable, 4. The matrix identifies whether related line items apply to each ticket type, 5. Conditional applicability rules are documented when a ticket or line item depends on rates or service conditions, 6. The matrix can be used as a reference when standardizing service ticket setup in CUBE.
- **Timestamp:** Day 4, Part 1 [0:03:40 – 0:05:35]
- **Notes:** This is a documentation/reference story. The matrix should be treated as a guide for ticket and line item applicability across product lines. In the transcript, “work order” terminology is clarified as fulfillment ticket terminology, so CUBE documentation should use consistent naming where possible.
- **Responsible:** TBD

## CUBE-PH4-D4-002
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Product Setup
- **Parent Task:** Product Code Setup
- **Task Name:** Pull Product Setup Values
- **User Story:** As a CUBE developer, I want product setup values to be pulled from the selected product line and product type so that CUBE can generate the required product codes, standard charge abbreviation, and category references used by the core flow.
- **Description:** Product setup starts with the selected product line and product type. Based on those selections, CUBE needs to identify the product abbreviation, product type abbreviation, standard charge abbreviation, parent product/category, and other code combinations used for filtering, setup rules, and downstream ticket or line item logic.
- **Acceptance Criteria:** 1. The product record uses the selected product line as part of the setup logic, 2. The product record uses the selected product type as part of the setup logic, 3. The system identifies the product abbreviation from the selected product line, 4. The system identifies the product type abbreviation from the selected product type, 5. The system generates or identifies the standard charge abbreviation, 6. The system identifies the parent product/category when the selected product requires one.
- **Timestamp:** Day 4, Part 1 [0:05:45 – 0:07:25]
- **Notes:** The example shown in the transcript uses a Construction ADA Toilet, but the code structure applies to the broader product and ticket code setup. The screenshots also show how product abbreviation, product type abbreviation, standard charge abbreviation, product/category references, ticket codes, and Intacct product codes are connected.
- **Responsible:** TBD

## CUBE-PH4-D4-003
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Cycle Management
- **Parent Task:** Cycle Date Calculation
- **Task Name:** Calculate Next Cycle Dates
- **User Story:** As a CUBE developer, I want the product record to calculate the next cycle start and end dates from the delivery date, cycle time, and existing service tickets so that recurring service cycles can be generated in the correct sequence.
- **Description:** Cycle dates are calculated from the product’s delivery date, cycle time, and existing service ticket history. When no standard service tickets exist, the next cycle starts on the delivery date. Once service tickets exist, the next cycle starts after the latest cycle end date, and the next cycle end date is calculated using the applicable cycle duration.
- **Acceptance Criteria:** 1. If no standard service tickets exist, the next cycle start date uses the delivery date, 2. If standard service tickets exist, the next cycle start date uses the maximum cycle end date plus one day, 3. The next cycle end date is calculated from the next cycle start date and the configured cycle time, 4. The system supports cycle durations such as 28-day cycles, 5. The system updates cycle dates based on the most recent completed service cycle, 6. The calculated dates can be used by downstream ticket creation and recurring service logic.
- **Timestamp:** Day 4, Part 1 [0:07:25 – 0:10:45]
- **Notes:** The screenshot shows the QuickBase formula for Next Cycle Start Date: if Standard Service Tickets Count is greater than zero, the formula uses Maximum Cycle End Date plus one day; otherwise, it uses the Delivery Date. This story captures the cycle formula behavior explained before ticket creation.
- **Responsible:** TBD

## CUBE-PH4-D4-004
- **Group:** Toilets
- **Category:** Workflow Validation
- **Epic:** Dispatching Status
- **Parent Task:** Delivery Dispatch Requirement
- **Task Name:** Flag Delivery Dispatching Required
- **User Story:** As a CUBE developer, I want products marked as sale to be flagged when delivery dispatching is required so that missing delivery tickets or open delivery dispatch tasks are visible in the product status workflow.
- **Description:** Delivery dispatching is required when a product is in Sale or legacy Sale Complete status and the system detects that the delivery process has not been completed. The flag is triggered when no delivery service ticket exists or when there are open delivery dispatch tasks associated with the product.
- **Acceptance Criteria:** 1. The system evaluates delivery dispatching only when the product is in Sale or legacy Sale Complete status, 2. If no delivery service ticket exists, delivery dispatching is marked as required, 3. If open delivery dispatch tasks exist, delivery dispatching remains required, 4. If the product does not meet the sale-status condition, delivery dispatching is not triggered by this logic, 5. The delivery dispatching flag feeds product-level status or reporting workflows, 6. The logic accounts for legacy Sale Complete records during migration or status evaluation.
- **Timestamp:** Day 4, Part 1 [0:11:15 – 0:14:05]
- **Notes:** The screenshot shows the Delivery Dispatching Required formula checking Sale Complete or Sale status, Delivery Service Tickets Count = 0, and open delivery dispatch tasks. The transcript also clarifies that Sale Complete is an old status equivalent to Sale and may need migration handling separately.
- **Responsible:** TBD

## CUBE-PH4-D4-005
- **Group:** Core Platform
- **Category:** Data Migration
- **Epic:** Legacy Status Migration
- **Parent Task:** Sale Complete Conversion
- **Task Name:** Handle Legacy Sale Complete Values
- **User Story:** As a CUBE developer, I want legacy Sale Complete values to be recognized as Sale during migration and status evaluation so that historical product records continue to trigger the correct core flow logic.
- **Description:** Sale Complete is a legacy status that is functionally equivalent to Sale. During migration and core flow rebuild, CUBE needs to account for records that still use Sale Complete so those records continue to behave like active sale records in formulas, status checks, reporting, and downstream workflow logic.
- **Acceptance Criteria:** 1. Legacy Sale Complete values are identified during migration analysis, 2. Sale Complete is treated as equivalent to Sale in rebuilt status logic, 3. Existing formulas or conditions that reference Sale Complete are reviewed during migration, 4. Historical records using Sale Complete continue to trigger sale-based workflow logic, 5. Sale Complete handling does not create duplicate or conflicting sale statuses in CUBE, 6. The migration approach defines whether Sale Complete values are converted to Sale or supported as legacy-equivalent values.
- **Timestamp:** Day 4, Part 1 [0:11:35 – 0:13:05]
- **Notes:** This story is related to delivery dispatching logic, but it is not limited to dispatching. The main purpose is to ensure legacy Sale Complete records continue working anywhere the core flow depends on Sale status. Justin mentions that Sale Complete is an old status equivalent to Sale and may need to be changed to Sale during migration.
- **Responsible:** TBD

## CUBE-PH4-D4-006
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Reporting Status
- **Parent Task:** Status Workflow
- **Task Name:** Display Granular Report Status
- **User Story:** As a CUBE user, I want the report status to display the next required action for a product so that I can quickly identify whether dispatching, service tickets, line items, invoicing, or payment still need attention.
- **Description:** Report status combines multiple product and ticket-level checks into one user-facing status field. It identifies whether the product still requires delivery dispatching, removal dispatching, other dispatching, a standard service ticket, a removal ticket, a line item, invoicing, or payment follow-up.
- **Acceptance Criteria:** 1. Report status is evaluated only when the product is in Sale or legacy Sale Complete status, 2. Report status displays delivery dispatching requirements when delivery dispatching is required, 3. Report status displays removal or other dispatching requirements when those conditions apply, 4. Report status displays service ticket or removal ticket requirements when required tickets are missing, 5. Report status displays line item or invoicing requirements when billing-related steps are incomplete, 6. Report status updates as each required workflow step is completed.
- **Timestamp:** Day 4, Part 1 [0:14:05 – 0:16:35]
- **Notes:** The screenshot shows the Report Status formula combining several conditions into one rich text field, including Delivery Dispatching Required, Removal Dispatching Required, Dispatching Required, Standard Service Required, Removal Ticket Required, Line Item Required, Invoicing Required, and payment-related checks. Justin also mentions that this logic may be separated into a more granular workflow in CUBE instead of remaining as one long combined status field.
- **Responsible:** TBD

## CUBE-PH4-D4-007
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Standard Service Logic
- **Parent Task:** Service Ticket Requirement
- **Task Name:** Flag Standard Service Required
- **User Story:** As a CUBE developer, I want the product record to flag when standard service is required so that users and automated processes can identify when a standard service ticket is missing or about to be needed for the next billing cycle.
- **Description:** Standard service is required when a product is in Sale or legacy Sale Complete status and the product needs a standard service ticket for the current or upcoming cycle. The logic checks whether standard service tickets already exist, whether the next cycle is approaching, whether the service occurs before removal, and whether the product should still be processed.
- **Acceptance Criteria:** 1. The system evaluates standard service requirements only for products in Sale or legacy Sale Complete status, 2. If no standard service tickets exist, the product is flagged as requiring standard service, 3. If the maximum cycle end date is within the configured warning window, the product is flagged as requiring standard service, 4. The system does not require standard service when the removal date falls before or within the current service logic, 5. The standard service required flag feeds product-level status, reporting, and recurring automation criteria, 6. The flag is not triggered for records excluded from processing by historical or migration-related conditions.
- **Timestamp:** Day 4, Part 1 [0:18:00 – 0:22:05]
- **Notes:** The screenshot shows the Standard Service Required formula using variables for Sale/Sale Complete status, Standard Service Tickets Count, Maximum Cycle End Date, Removal Date, and historical child-removal logic. The transcript explains that this flag helps warn users when a standard service ticket is missing or when the next cycle is about to require one, and it also feeds the table-to-table process that creates recurring service tickets.
- **Responsible:** TBD

## CUBE-PH4-D4-008
- **Group:** Core Platform
- **Category:** Automation
- **Epic:** Recurring Ticket Creation
- **Parent Task:** Table-to-Table Criteria
- **Task Name:** Create Next Cycle Service Ticket Automatically
- **User Story:** As a CUBE developer, I want the recurring service ticket creation process to use defined eligibility criteria so that CUBE automatically creates the next cycle service ticket only when the product is ready for recurring service.
- **Description:** Recurring service tickets are created through an automated process after the initial service ticket has been created manually. The automation uses eligibility criteria such as Standard Service Required, recurring approval, opt-out status, portal-ready billing preference, valid cycle dates, monthly service count, cycle time, assigned hauler, and the next cycle start date.
- **Acceptance Criteria:** 1. The automation requires Standard Service Required to be checked, 2. The automation requires the product to be approved for recurring processing, 3. The automation excludes records where Opt Out Line Item is checked, 4. The automation requires Billing Preference - Portal Ready to be checked, 5. The automation requires valid cycle data, including Next Cycle End Date, Cycle Time, and Next Cycle Start Date, 6. The automation requires at least one monthly service and an assigned Hauler ID before creating the next cycle service ticket.
- **Timestamp:** Day 4, Part 1 [0:22:21 – 0:27:05]
- **Notes:** The screenshot shows the QuickBase table-to-table import criteria for creating toilet tickets. Justin clarifies that the first ticket must be created manually, and the automation only runs after at least one monthly service exists. The Next Cycle Start Date condition shown in the screenshot checks whether the date is on or before four days in the future, while the transcript also mentions a similar three-day warning window in the standard service logic.
- **Responsible:** TBD

## CUBE-PH4-D4-009
- **Group:** Core Platform
- **Category:** UI/UX
- **Epic:** Status Display
- **Parent Task:** Humanized Status Display
- **Task Name:** Display Computed Service Status Instead of Raw Boolean
- **User Story:** As a CUBE user, I want computed backend status flags to be displayed as clear, human-readable status messages so that I can understand the next required action without interpreting raw boolean fields.
- **Description:** Computed backend flags are used to determine which status messages should appear in the product workflow. Instead of showing raw checkbox or boolean values, CUBE should display clear messages such as Delivery Dispatching Required, Service Ticket Required, Line Item Required, Invoicing Required, or payment-related status messages when the related conditions apply.
- **Acceptance Criteria:** 1. Raw boolean or checkbox fields are not displayed directly as workflow instructions to users, 2. Computed backend flags are converted into human-readable status messages, 3. The status display includes dispatching-related messages when dispatching flags are true, 4. The status display includes service ticket or removal ticket messages when ticket requirements are true, 5. The status display includes line item, invoicing, or payment messages when billing-related conditions are true, 6. The displayed status message helps users identify the next required action in the workflow.
- **Timestamp:** Day 4, Part 1 [0:27:08 – 0:29:30]
- **Notes:** The screenshot shows computed fields such as Delivery Dispatching Required, Removal Dispatching Required, Dispatching Required, and Standard Service Required being translated into readable report status text. Justin explicitly says the boolean itself is not directly shown in the UI, but the data computed from that boolean is shown in a humanized way.
- **Responsible:** TBD

## CUBE-PH4-D4-010
- **Group:** Core Platform
- **Category:** Data Migration
- **Epic:** QuickBase Data Export
- **Parent Task:** Historical CSV Backups
- **Task Name:** Use Full CSV Backups for Large Historical Migration
- **User Story:** As a CUBE developer, I want large historical QuickBase data to be migrated from full CSV backups so that archived records and high-volume tables can be restored into CUBE without relying on QuickBase’s limited export process.
- **Description:** Historical QuickBase data may need to be restored from full CSV backups instead of the standard QuickBase export tool. QuickBase exports are limited in size, while QUNect backups can contain full table exports, including very large CSV files and records that were previously archived or removed from QuickBase.
- **Acceptance Criteria:** 1. The migration process does not rely on the standard QuickBase export tool for large historical tables, 2. Full CSV backups are used when QuickBase export limits prevent complete data extraction, 3. Archived or removed records are identified from available backup CSV files, 4. Missing historical records can be compared against current data before being restored, 5. Large CSV files are processed in an environment with sufficient resources, 6. The migration approach supports table-by-table restoration into CUBE.
- **Timestamp:** Day 4, Part 1 [0:29:44 – 0:35:05]
- **Mockups:** NO MOCKUP
- **Notes:** Justin explains that QuickBase CSV export is limited to 10 MB, while QUNect backups can produce much larger CSV files, including files several gigabytes in size. Some archived child history records may only exist in those backup files, so those backups are required for historical restoration.
- **Responsible:** TBD

## CUBE-PH4-D4-011
- **Group:** Toilets
- **Category:** Workflow Validation
- **Epic:** Ticket Creation Buttons
- **Parent Task:** Service Ticket Button Rules
- **Task Name:** Control Service Ticket Button Availability
- **User Story:** As an Account Manager (AM), I want service ticket creation buttons to appear only when the required conditions are met so that I cannot create tickets out of sequence or create invalid service tickets.
- **Description:** Service ticket buttons are controlled by lockout rules that evaluate the current product and ticket conditions before allowing ticket creation. For standard service tickets, the logic checks whether a delivery ticket already exists, whether a removal ticket has already been created, and whether the next cycle start date conflicts with the removal date.
- **Acceptance Criteria:** 1. The standard service ticket button is unavailable when no delivery ticket exists, 2. The standard service ticket button is unavailable when a removal service ticket has already been created, 3. The system checks whether the next cycle start date is after the removal date, 4. If the next cycle start date is after the removal date, the button displays a warning instead of allowing standard service ticket creation, 5. If no lockout condition applies, the standard service ticket button is available, 6. Button availability is controlled by system logic and not by manual user selection.
- **Timestamp:** Day 4, Part 1 [0:35:12 – 0:37:35]
- **Notes:** The screenshot shows the RT Standard Service formula using variables such as DeliveryCreated, Removaldate, and DDate to control whether the button or warning text is displayed. This story is limited to service ticket button availability and lockout behavior, not the full ticket creation process.
- **Responsible:** TBD

## CUBE-PH4-D4-012
- **Group:** Core Platform
- **Category:** Documentation
- **Epic:** Field Mapping
- **Parent Task:** Formula Field Documentation
- **Task Name:** Identify Critical Formula and Summary Fields
- **User Story:** As a CUBE developer, I want critical formula and summary fields to be identified by table and process so that the team can rebuild the required logic without reviewing every QuickBase field manually.
- **Description:** QuickBase contains a large number of fields across the product tables, including formula fields, summary fields, lookup fields, reporting fields, trigger fields, and fields that are no longer used. CUBE needs a focused field mapping approach that identifies the fields required for product setup, ticket creation, line item logic, status calculation, reporting, and migration.
- **Acceptance Criteria:** 1. Critical formula fields are identified by table and process, 2. Summary fields used by setup logic, ticket counts, line item counts, and status logic are identified, 3. Field comments or labels are reviewed to understand whether a field is used for process, trigger, report, summary, API, or do-not-use purposes, 4. Equivalent fields across product tables are mapped when they support the same business logic, 5. Deprecated or unused fields are excluded from the core rebuild unless they are required for migration history, 6. The field mapping helps developers trace important logic before rebuilding it in CUBE.
- **Timestamp:** Day 4, Part 1 [0:38:36 – 0:46:30]
- **Notes:** The screenshot shows the Toilets Settings table displaying 700 fields, which supports Justin’s point that not every field can be documented manually. Justin mentions that field comments may use shorthand such as PRC, TRG, RPT, SUM, ZCorp, and DNU, and that the team should focus on the fields that drive the main structure and process logic.
- **Responsible:** TBD

## CUBE-PH4-D4-013
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Summary Queries
- **Parent Task:** Ticket Status Aggregation
- **Task Name:** Aggregate Ticket Counts by Required Status
- **User Story:** As a CUBE developer, I want product-level summary counts for service tickets to drive ticket and billing status logic so that CUBE can identify when service tickets, line items, or invoices are still required.
- **Description:** Product-level status logic depends on summary counts from related service tickets. These counts identify whether required tickets exist, whether delivery or service tickets are missing, whether related tickets still need line items, and whether related tickets still need invoicing. CUBE needs equivalent summary logic so product status can accurately reflect incomplete workflow steps.
- **Acceptance Criteria:** 1. The system counts related service tickets by ticket type, 2. The system identifies when required delivery or service tickets are missing, 3. The system counts service tickets that still require line items, 4. The system counts service tickets that still require invoicing, 5. Product-level status logic uses these counts to determine whether setup or billing is incomplete, 6. Summary counts are updated when related tickets, line items, or invoices change.
- **Timestamp:** Day 4, Part 1 [0:46:30 – 0:49:50]
- **Notes:** The screenshot shows a formula using Service & Rental Tickets Count, Delivery Service Tickets Count, Service Tickets Line Item Required - First Cycle, and Service Tickets Invoice Required - First Cycle. Justin explains that QuickBase uses many similar summary queries to evaluate ticket existence, line item requirements, invoicing requirements, and payment status. This story focuses on product-level summary logic, not the individual formulas for each ticket type.
- **Responsible:** TBD

## CUBE-PH4-D4-014
- **Group:** Core Platform
- **Category:** Technical Dependency
- **Epic:** Formula Dependencies
- **Parent Task:** Dependency Traceability
- **Task Name:** Trace Formula Dependencies Before Changing Logic
- **User Story:** As a CUBE developer, I want formula and button dependencies to be traceable before logic is rebuilt or changed so that dependent fields, buttons, and downstream processes are not broken during implementation.
- **Description:** Formula fields and buttons can depend on multiple formulas, lookup fields, summary fields, and related-table values. Before rebuilding this logic in CUBE, developers need to understand which fields a formula or button depends on and which downstream processes may be affected by changes.
- **Acceptance Criteria:** 1. Developers can identify the fields used by formula-driven buttons, 2. Developers can trace dependencies across formula fields, lookup fields, summary fields, and related-table values, 3. Developers can identify downstream fields or processes affected by a formula change, 4. Button logic is reviewed before being rebuilt or modified in CUBE, 5. Cross-table dependencies are documented when they affect core flow behavior, 6. High-risk logic is not rebuilt without reviewing its dependency impact.
- **Timestamp:** Day 4, Part 1 [0:52:08 – 0:53:40]
- **Mockups:** NO MOCKUP
- **Notes:** Justin shows a dependency diagram for a button and explains that one button can depend on many fields across several formula, lookup, and summary layers. This story focuses on dependency traceability during the CUBE rebuild, not on recreating QuickBase’s dependency diagram UI exactly.
- **Responsible:** TBD

## CUBE-PH4-D4-015
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Delivery Ticket Setup
- **Parent Task:** Create Delivery Ticket
- **Task Name:** Create Delivery Ticket with Copied Product Values
- **User Story:** As an Account Manager (AM), I want the delivery ticket to be created with the required product, site, billing, hauler, and rate details so that the delivery service ticket is prefilled with the information needed for dispatching and downstream processing.
- **Description:** Delivery ticket creation uses the RT Delivery Ticket logic to pass product-level values into the new delivery service ticket. The delivery ticket is prefilled with values such as delivery date, site information, quantity, frequency of service, onsite contact details, hauler ID, billing preference, and service-related rate fields. After the ticket is created, the system evaluates whether dispatch information is complete and flags the ticket when dispatching is still required.
- **Acceptance Criteria:** 1. The delivery ticket is created with the correct delivery ticket code, 2. The delivery ticket receives the delivery date, site details, quantity, and frequency of service from the product record, 3. The delivery ticket receives onsite contact information and Hauler ID when available, 4. The delivery ticket receives the related billing preference and applicable service or hauler rate fields, 5. The system evaluates whether required dispatch information is complete after ticket creation, 6. If required dispatch information is missing, the delivery ticket is flagged as requiring dispatching.
- **Timestamp:** Day 4, Part 1 [1:00:00 – 1:04:59]
- **Notes:** The RT Delivery Ticket screenshot shows multiple product-level values being passed into the delivery ticket through field IDs, including delivery date, site details, quantity, frequency of service, onsite contact information, Hauler ID, billing preference, and rate-related fields. Justin creates a delivery ticket during the demo and explains that values are pulled automatically. He does not fill out dispatch information, so the system flags dispatching as required.
- **Responsible:** TBD

## CUBE-PH4-D4-016
- **Group:** Pricing
- **Category:** Data Integrity
- **Epic:** Rate Snapshotting
- **Parent Task:** Ticket Pricing Snapshot
- **Task Name:** Preserve Ticket Pricing at Creation Time
- **User Story:** As a CUBE developer, I want ticket pricing and hauler rate details to be captured at the time the ticket is created so that existing tickets and line items keep their original pricing even if product-level pricing changes later.
- **Description:** Ticket pricing is captured as a snapshot when the service ticket is created. The ticket stores the current customer pricing, vendor pricing, hauler rate details, and related pricing values from the product record. This prevents later changes at the product level from modifying the pricing already assigned to existing tickets or line items.
- **Acceptance Criteria:** 1. The ticket captures the current customer pricing when it is created, 2. The ticket captures the current vendor or hauler pricing when it is created, 3. Existing ticket pricing does not change when product-level pricing is updated later, 4. Existing ticket hauler or vendor rate details do not change when product-level hauler information is updated later, 5. Line item pricing can use the ticket-level pricing snapshot, 6. Historical ticket and line item pricing remains consistent after upstream product changes.
- **Timestamp:** Day 4, Part 1 [1:05:56 – 1:08:18]
- **Notes:** The screenshot shows the Pricing tab on the service ticket, including customer pricing values such as standard rate, delivery rate, removal rate, winterization rate, dry run rate, service rate, service rate after hours, relocation rate, and rental protection charge, as well as vendor pricing values such as standard rate, delivery rate, removal rate, fuel/environmental percent, fuel/environmental dollars, tax percent, and tax dollars. Justin explains that pricing and hauler information are copied from the product to the ticket, and then from the ticket to the line item, to preserve the values that existed at the time the ticket was created. He also states that this current copy-based approach is inefficient, but the original purpose was to snapshot pricing in time.
- **Responsible:** TBD

## CUBE-PH4-D4-017
- **Group:** Pricing
- **Category:** Data Integrity
- **Epic:** PSP Pricing Metadata
- **Parent Task:** Store Original and Edited Pricing Values
- **Task Name:** Store Original and Edited Pricing Values
- **User Story:** As a CUBE developer, I want original PSP pricing values to be stored separately from edited pricing values so that CUBE can preserve the pricing source while still allowing adjusted rates to be used on the product.
- **Description:** PSP pricing metadata stores the original pricing values returned from the pricing tool, including pricing identifiers and original charge amounts. If users edit pricing values during the pricing flow, CUBE should keep the original pricing tool values for reference while saving the edited values as the current product pricing.
- **Acceptance Criteria:** 1. The system stores the original PSP pricing identifiers when pricing is selected from the pricing tool, 2. The system stores the original pricing tool charge values separately from editable product pricing fields, 3. Edited pricing values are saved as the current product pricing when users adjust rates, 4. Original pricing tool values remain unchanged after edits, 5. The product record reflects the adjusted current rates when edits are made, 6. CUBE can compare original pricing tool values against edited product pricing values when needed.
- **Timestamp:** Day 4, Part 1 [1:08:21 – 1:12:15]
- **Notes:** The screenshot shows Pricing Tool metadata, including Vendor Pricing RID, Pricing Tool - Vendor List, Pricing Tool - Pref Vendor Used, Pricing Tool Rental Charge, Pricing Tool Delivery Charge, and Standard Charge (Hauler) (Calculated). Justin explains that if pricing can be edited in Base44, the original pricing tool values should still be saved separately while the edited values are saved into the active rate fields. This allows CUBE to preserve the original PSP pricing source and still support adjusted rates.
- **Responsible:** TBD

## CUBE-PH4-D4-018
- **Group:** Core Platform
- **Category:** Data Integrity
- **Epic:** No Sale Handling
- **Parent Task:** No Sale Reason Writeback
- **Task Name:** No Sale Reason Writeback
- **User Story:** As a CUBE developer, I want No Sale reasons captured from the HUB Call Wizard flow to write back to the correct customer or product record so that No Sale data is stored at the appropriate level.
- **Description:** No Sale reasons are captured during the Call Wizard flow and need to be stored against the correct record. When the No Sale reason is entered from the customer or site context, the value should write back to the related customer record. When the No Sale reason is entered from the product context, the value should write back to the related product record.
- **Acceptance Criteria:** 1. A No Sale reason entered from the customer context writes back to the customer record, 2. A No Sale reason entered from the site context writes back to the related customer record, 3. A No Sale reason entered from the product context writes back to the related product record, 4. The system does not create or depend on a site-level No Sale reason field, 5. The writeback behavior is consistent when the No Sale reason is captured through the HUB Call Wizard flow, 6. Required field IDs or API mappings are confirmed before implementation.
- **Timestamp:** Day 4, Part 1 [1:12:15 – 1:14:15]
- **Mockups:** NO MOCKUP
- **Notes:** Justin clarifies that there is no site-level No Sale reason. If the No Sale reason is entered from the site version of the flow, it should write back to the customer record. If it is entered from the product level, it should write back to the product record. The value appears to come from the HUB Call Wizard flow, but the final CUBE storage/writeback implementation should be confirmed during development.
- **Responsible:** TBD

## CUBE-PH4-D4-019
- **Group:** Pricing
- **Category:** Architecture
- **Epic:** Rate Card Architecture
- **Parent Task:** Pricing Record References
- **Task Name:** Reference Pricing Records Instead of Copying Full Rate Cards
- **User Story:** As a CUBE developer, I want products, service tickets, and line items to reference pricing record IDs instead of copying full rate card values so that CUBE can preserve pricing history while reducing duplicated pricing data.
- **Description:** Pricing records should be referenced by ID instead of copied repeatedly into products, service tickets, and line items. When standard PSP pricing, statistical pricing, or an existing pricing record is used, CUBE should link to that pricing record. When pricing is manually adjusted or custom pricing is required, CUBE should create or reference a separate custom pricing record while preserving the previous pricing reference for history.
- **Acceptance Criteria:** 1. Products can reference the active pricing record used for the current product pricing, 2. Service tickets can retain the pricing record that was active when the ticket was created, 3. Line items can reference the applicable pricing record instead of duplicating full rate card values, 4. Custom or manually adjusted pricing creates or references a separate pricing record, 5. Previous pricing references remain available for historical tracking, 6. The pricing structure reduces repeated rate card duplication across products, tickets, and line items.
- **Timestamp:** Day 4, Part 1 [1:14:15 – 1:21:25]
- **Mockups:** NO MOCKUP
- **Notes:** Justin presents this as the preferred future architecture for CUBE pricing. The goal is to avoid copying the same rate card values from product to ticket and from ticket to line item every time a record is created. Pricing history should be preserved through pricing record references instead of repeated snapshots of the full rate card.
- **Responsible:** TBD

## CUBE-PH4-D4-020
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Product and Ticket Codes
- **Parent Task:** Code Combination Logic
- **Task Name:** Generate Product and Ticket Code Combinations
- **User Story:** As a CUBE developer, I want product line, product type, state, category, and ticket code values to generate the required product and ticket code combinations so that CUBE can apply the correct filtering rules and workflow guardrails.
- **Description:** Product and ticket code combinations are built from several values, including product line, product type, state, product category, and ticket code. These combinations are used to identify values such as the basic product code prefix, basic product code, parent product and ticket code, and related product code references. CUBE needs this code logic to support filtering, setup rules, line item applicability, and downstream workflow validation.
- **Acceptance Criteria:** 1. The system uses product line as part of the product and ticket code combination logic, 2. The system uses product type as part of the product and ticket code combination logic, 3. The system includes state when generating Intacct or state-specific product code values, 4. The system uses product category and ticket code values when they are required for parent product or ticket code references, 5. Generated code combinations support filtering, setup rules, and workflow guardrails, 6. Nonessential suffix, prefix, or duplicate code fields are reviewed for simplification during the CUBE rebuild.
- **Timestamp:** Day 4, Part 1 [1:22:34 – 1:27:15]
- **Notes:** The screenshot shows generated administrative code values such as Basic Product Code Prefix, Basic Product Code, and Parent Product and Ticket Code. Justin explains that the current setup uses several code pieces and combinations for filtering and formulas, but he also notes that the current code setup is split into too many parts and should likely be simplified in CUBE.
- **Responsible:** TBD

## CUBE-PH4-D4-021
- **Group:** Toilets
- **Category:** Workflow Validation
- **Epic:** Line Item Creation
- **Parent Task:** Line Item Applicability Rules
- **Task Name:** Determine Applicable and Required Line Items
- **User Story:** As a CUBE developer, I want line item applicability to be determined from ticket code, product code, product type, and rate conditions so that only valid line item options are available for the service ticket.
- **Description:** Line item applicability is calculated before the user creates a line item. For delivery line items, the system checks whether the ticket code supports the delivery product code, whether the product type is a delivery type, whether the delivery amount is greater than zero, and whether the combined product code does not already include the delivery code. When these conditions are met, the delivery line item becomes applicable.
- **Acceptance Criteria:** 1. The system checks whether the ticket code includes the applicable product code for the line item type, 2. The system checks whether the product type matches the expected line item type, such as delivery, 3. The system checks whether the related rate amount is greater than zero when the line item depends on a rate, 4. The system verifies that the combined product code does not already include the generated line item code, 5. The line item option becomes available only when all applicability conditions are met, 6. Unrelated or invalid line item options remain unavailable for the service ticket.
- **Timestamp:** Day 4, Part 1 [1:28:00 – 1:36:50]
- **Notes:** The screenshot shows the Delivery formula in Toilet Tickets Settings. The formula checks Ticket Code - All Product Codes, Product Type with _DELIVERY, Delivery Amount greater than zero, and Combined Text Product Code using the Basic Product Code Prefix plus _DELIVERY. Justin explains this as part of the three-tier process: ticket code defines what could be required, product/code conditions determine applicability, and then the UI shows the line item button when the line item is applicable and required.
- **Responsible:** TBD

## CUBE-PH4-D4-022
- **Group:** Core Platform
- **Category:** Technical Integration
- **Epic:** QuickBase Button Behavior
- **Parent Task:** URL-Based Record Creation
- **Task Name:** Replicate URL-Based Add Record Behavior Where Needed
- **User Story:** As a CUBE developer, I want to understand QuickBase URL-based record creation buttons so that equivalent record creation behavior can be rebuilt in CUBE without relying on the old URL variable approach.
- **Description:** QuickBase uses URL-based button formulas to create related records and prefill field values. These formulas build a URL using the target table, API_GenAddRecordForm, and multiple field ID parameters. CUBE needs equivalent record creation behavior that passes the required values into the new record through application logic instead of relying on QuickBase URL formulas.
- **Acceptance Criteria:** 1. The existing QuickBase URL formula identifies the target table or database used for record creation, 2. The formula parameters and field IDs used to prefill the new record are mapped to the corresponding CUBE fields, 3. Required values passed through the URL are identified and documented, 4. CUBE recreates the same record creation behavior through application logic, 5. Users do not need to manually enter or modify URL strings, 6. The rebuilt process preserves the required source-to-target field mapping from the QuickBase button.
- **Timestamp:** Day 4, Part 1 [1:36:52 – 1:39:50]
- **Notes:** The screenshot shows the Delivery Charge field as a URL formula using URLRoot(), the line items database reference, API_GenAddRecordForm, and several _fid_ parameters to pass values into a new line item record. Justin clarifies that this is technically an API-style QuickBase process, but he describes it as URL variables rather than a modern authenticated API process.
- **Responsible:** TBD

## CUBE-PH4-D4-023
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Line Item Summary Logic
- **Parent Task:** Ticket-Level Line Item Status
- **Task Name:** Aggregate Line Item Status at Ticket Level
- **User Story:** As a CUBE developer, I want service tickets to summarize their related line items so that the ticket can identify whether required line items exist, have been invoiced, or remain unpaid.
- **Description:** Ticket-level status logic depends on summary counts from related line items. These counts determine whether the required line items have been created, whether line items are still missing, whether any line items have not been invoiced, and whether invoiced line items still have pending payment. CUBE needs equivalent ticket-level summary logic so service ticket status can accurately reflect incomplete billing steps.
- **Acceptance Criteria:** 1. The ticket counts related line items by required line item type, 2. The ticket identifies when required line items are missing, 3. The ticket identifies whether standard charge line items exist when required, 4. The ticket identifies whether required line items have not been invoiced, 5. The ticket identifies whether invoiced line items remain unpaid, 6. Ticket-level status updates when related line items, invoices, or payment statuses change.
- **Timestamp:** Day 4, Part 1 [1:40:03 – 1:46:40]
- **Mockups:** NO MOCKUP
- **Notes:** This story focuses on ticket-level line item summaries. Justin compares this logic to product-level ticket summaries, but at the service-ticket-to-line-item level. The goal is to allow the ticket to determine whether line items exist, whether they have been invoiced, and whether payment is still pending.
- **Responsible:** TBD

## CUBE-PH4-D4-024
- **Group:** Core Platform
- **Category:** Data Model
- **Epic:** Product Code Model
- **Parent Task:** Product and Service Codes
- **Task Name:** Differentiate Product Codes Used for Products and Services
- **User Story:** As a CUBE developer, I want product codes to represent both physical products and service-type codes so that CUBE can correctly support ticket-driven services such as delivery, haul, dry run, winterization, miscellaneous service, and removal.
- **Description:** Product codes are used for more than physical products. They also represent service-type codes tied to ticket behavior, such as dry run, winterization, miscellaneous service, monthly service, haul, and contamination. CUBE needs to preserve this distinction so ticket codes, product codes, tax codes, and line item logic can work correctly across product lines.
- **Acceptance Criteria:** 1. Product code records can represent physical product configurations, 2. Product code records can represent service-type codes tied to ticket behavior, 3. Service-type codes can be associated with ticket codes such as haul, dry run, winter, miscellaneous, monthly service, or contamination, 4. Product codes retain related metadata such as product abbreviation, related product, related ticket code, and tax code, 5. Ticket and line item logic can use service-type product codes when determining applicability, 6. The product code model supports both product and service entries without treating all records as physical products.
- **Timestamp:** Day 4, Part 1 [1:47:00 – 1:51:35]
- **Notes:** The screenshot shows the Product Codes table with examples such as PERM-RO haul product codes, FENCING_DRY-RUN, PT_WINTER, FEL_SERVICE ADJUSTMENT, PERM-RO_CONTAMINATION, and FENCING_MISC. Justin explicitly explains that product codes are a combination of actual products and services, not only physical products.
- **Responsible:** TBD

## CUBE-PH4-D4-025
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Invoicing Status
- **Parent Task:** Ticket Invoice Status from Line Items
- **Task Name:** Mark Ticket Invoiced When Any Related Line Item Has an Invoice
- **User Story:** As a CUBE developer, I want the service ticket to determine invoice status from its related line items so that the ticket can identify whether billing has already occurred without requiring a separate manual ticket-level invoice flag.
- **Description:** Service ticket invoice status is inferred from related line item data. If any related line item has an invoice associated with it, the ticket can be treated as invoiced for workflow and status purposes. The ticket also uses line item summary values to identify whether line items are missing, not invoiced, or unpaid.
- **Acceptance Criteria:** 1. The system checks related line items for invoice associations, 2. If at least one related line item has an invoice, the ticket is treated as invoiced, 3. The ticket identifies when related line items have not been invoiced, 4. The ticket identifies when invoiced line items remain unpaid, 5. Ticket-level billing status updates when related line item invoice or payment status changes, 6. The logic does not require users to manually update a separate ticket-level invoice flag.
- **Timestamp:** Day 4, Part 1 [1:51:35 – 1:52:55]
- **Notes:** The screenshot shows ticket-level line item summary fields such as Line Items, Line Items w/no Invoice, and Line Items Unpaid. Justin explains that if any line item under a ticket has a related invoice ID, the ticket can be treated as invoiced because users normally do not invoice only one line item and leave the rest uninvoiced. He acknowledges partial invoicing could technically happen, but the current operational logic does not handle it that way.
- **Responsible:** TBD

## CUBE-PH4-D4-026
- **Group:** Customers
- **Category:** Functional Logic
- **Epic:** Credit Status
- **Parent Task:** Fraud Warning Logic
- **Task Name:** Display Possible Fraud Warning in Credit Status
- **User Story:** As a CUBE user, I want the customer credit status to display a possible fraud warning when fraud approval conditions are met so that users can identify customers that may require additional review before continuing with the order flow.
- **Description:** Customer credit status includes fraud warning logic based on customer billing preference and fraud approval conditions. When the customer has multiple billing preferences and the fraud warning approval flag is active, the credit status should display a clear Possible Fraud Warning message before users proceed with related order or billing actions.
- **Acceptance Criteria:** 1. The system evaluates fraud warning logic from the customer credit status, 2. The system checks whether the customer has more than one new billing preference, 3. The system checks whether the customer matches the specific fraud warning customer condition shown in the formula, 4. The system checks whether Fraud Warning Approval is true, 5. When the required conditions are met, the credit status displays Possible Fraud Warning, 6. The warning is visually distinguishable from other credit status messages.
- **Timestamp:** Day 4, Part 1 [2:07:32 – 2:10:00]
- **Notes:** The screenshot shows the Customers Settings > Credit Status formula displaying a Possible Fraud Warning when the customer billing preference count, customer ID condition, and Fraud Warning Approval condition are met. This topic appears briefly after the break when Justin checks the fraud warning logic before returning to the main core flow discussion.
- **Responsible:** TBD

## CUBE-PH4-D4-027
- **Group:** Fulfillment
- **Category:** Functional Logic
- **Epic:** Dispatch Data
- **Parent Task:** Fulfillment Dispatch Requirements
- **Task Name:** Move Dispatch Information Logic to Fulfillment Tickets
- **User Story:** As a CUBE developer, I want dispatch information to be handled through fulfillment tickets so that dispatch details are captured in the workflow where fulfillment work is managed.
- **Description:** Dispatch information is currently captured on service tickets, including dispatch log details, vendor information, and related line item information. In CUBE, this dispatch information should be reviewed as part of the fulfillment workflow because fulfillment tickets are expected to manage the dispatch process. Ticket types that do not require dispatching, such as dry run or miscellaneous cases learned from the hauler, should not require unnecessary dispatch steps.
- **Acceptance Criteria:** 1. Dispatch information requirements are reviewed at the ticket-code level, 2. Fulfillment tickets capture or manage dispatch information in the future workflow, 3. Dispatch log details such as called in by, called in on, dispatched by, dispatched with, and dispatched on are considered in the fulfillment design, 4. Vendor information needed for dispatch is available in the fulfillment workflow, 5. Ticket types that do not require dispatching are identified and excluded from unnecessary dispatch requirements, 6. The new workflow avoids duplicating dispatch handling between service tickets and fulfillment tickets.
- **Timestamp:** Day 4, Part 1 [2:13:32 – 2:17:15]
- **Notes:** The screenshot shows dispatch-related information currently displayed on the service ticket, including Dispatch Log, Vendor Information, and Line Items. Justin explains that dispatch information currently lives on service tickets and is defined by ticket-code rules, but this information should move to the fulfillment process in CUBE. He also notes that some ticket types, such as miscellaneous or dry run tickets, may not require dispatching because the issue is usually learned from the hauler rather than dispatched back to the hauler.
- **Responsible:** TBD

## CUBE-PH4-D4-028
- **Group:** Fulfillment
- **Category:** Functional Logic
- **Epic:** Vendor Payment
- **Parent Task:** Vendor Payment Requirement
- **Task Name:** Determine When Vendor Payment Is Required
- **User Story:** As a CUBE developer, I want the system to determine when vendor payment is required for a service ticket so that vendor payment and item receipt processes are triggered only when the service type requires them.
- **Description:** Vendor payment requirement is currently driven by ticket code configuration. Some service tickets always require vendor payment, while others may only require vendor payment when a vendor charge exists. CUBE needs to determine whether vendor payment is expected for each service ticket so that downstream item receipt and vendor payment workflows are triggered correctly.
- **Acceptance Criteria:** 1. The system identifies whether vendor payment is required for the service ticket, 2. The vendor payment requirement can be derived from ticket-code configuration, 3. Tickets with optional vendor charges do not automatically require vendor payment, 4. Tickets with expected vendor payment trigger the related item receipt or vendor payment workflow, 5. Future logic can evaluate vendor rate-card values when vendor payment depends on whether a charge exists, 6. Vendor payment requirement logic supports fulfillment and downstream payment processing.
- **Timestamp:** Day 4, Part 1 [2:17:15 – 2:20:30]
- **Mockups:** NO MOCKUP
- **Notes:** Justin explains that Vendor Payment Required is currently pulled from the ticket code. He compares cases such as portable toilet delivery, where vendor payment may be optional depending on whether a delivery charge exists, with standard service, where vendor payment is expected. He also mentions that future logic could evaluate vendor rate-card values, such as whether a vendor delivery charge exists, instead of relying only on ticket-code configuration.
- **Responsible:** TBD

## CUBE-PH4-D4-029
- **Group:** Toilets
- **Category:** Functional Logic
- **Epic:** Recurring Charges
- **Parent Task:** Winterization and Additional Rental Flags
- **Task Name:** Calculate Winterization and Additional Rental Applicability
- **User Story:** As a CUBE developer, I want recurring service tickets to identify when winterization or additional rental line items are applicable so that CUBE can generate the correct extra charges only when the service cycle, state, and product conditions require them.
- **Description:** Recurring service tickets may require additional line items based on state-specific rental rules or winterization logic. California and Indiana can trigger additional rental handling, while winterization depends on whether the ticket belongs to a winter service cycle and whether the winter fee product code applies. These checks help determine whether extra line items, such as rental or winterization, should be available or generated.
- **Acceptance Criteria:** 1. The system identifies whether the service ticket is associated with California or Indiana, 2. The system evaluates whether additional rental logic applies for the service ticket, 3. The system identifies whether the ticket is part of a winter service cycle, 4. The system checks whether the winter fee product code applies, 5. The system uses rental and winterization codes when determining applicable extra line items, 6. Additional rental or winterization line items are available or generated only when the required conditions are met.
- **Timestamp:** Day 4, Part 1 [2:20:30 – 2:23:15]
- **Notes:** The screenshot shows fields used in recurring billing and winterization logic, including California or Indiana, Winter Service Cycle, Winter Fee Product Code Check, Cold Months List, Rental Code, Winterization Code, and Automated Line Item Process. Justin explains that California and Indiana logic applies to standard service tickets, not delivery tickets, and that winterization uses a separate winter service cycle and product code check.
- **Responsible:** TBD

## CUBE-PH4-D4-030
- **Group:** Core Platform
- **Category:** Data Integrity
- **Epic:** Line Item Creation
- **Parent Task:** Line Item Specific Rate Pull
- **Task Name:** Create Line Item with the Specific Applicable Amount
- **User Story:** As a CUBE developer, I want line item creation to pull only the amount relevant to the specific line item type so that line items store the correct charge without duplicating the full ticket rate card.
- **Description:** Line items do not need to copy every rate stored on the service ticket. When a line item is created, CUBE should use the amount that matches the specific line item type. For example, a delivery line item uses the delivery amount, while other line item types use their own applicable amounts, such as winterization, insurance, or service-related charges.
- **Acceptance Criteria:** 1. A delivery line item pulls only the delivery amount, 2. A winterization line item pulls only the winterization amount, 3. An insurance line item pulls only the insurance amount, 4. A service or rental line item pulls the applicable service or rental amount, 5. Line items do not duplicate the full ticket rate card, 6. Each line item stores the amount that corresponds to its product or service code.
- **Timestamp:** Day 4, Part 1 [2:24:00 – 2:28:30]
- **Mockups:** NO MOCKUP
- **Notes:** Justin explains that tickets copy all rate values, but line items pull only the specific amount relevant to the line item being created. This keeps the line item focused on the charge it represents, such as delivery, winterization, insurance, rental, or service, instead of copying every pricing field from the ticket.
- **Responsible:** TBD

## CUBE-PH4-D4-031
- **Group:** Core Platform
- **Category:** Integration
- **Epic:** Intacct Product Codes
- **Parent Task:** Product Code Validation
- **Task Name:** Validate Final Product Code Against Intacct
- **User Story:** As a CUBE developer, I want line item product codes to be selected from the Intacct product code list so that line items use valid product codes before they are sent to downstream invoicing processes.
- **Description:** Line item product codes are tied to Intacct product code data. The Product Code field on line items uses values from the Intacct Data product code list, which helps ensure that the product code assigned to a line item exists in the accounting product code reference before invoicing.
- **Acceptance Criteria:** 1. The line item Product Code field uses values from the Intacct product code reference list, 2. Users or system logic can only assign product codes that exist in the approved product code source, 3. The selected product code is stored on the line item, 4. Invalid or missing product codes are prevented before downstream invoicing, 5. Product code validation supports the HUB and Intacct invoicing flow, 6. The product code reference source is maintained so CUBE can validate line item product codes consistently.
- **Timestamp:** Day 4, Part 1 [2:28:30 – 2:31:20]
- **Notes:** The screenshot shows the Line Items Settings > Product Code field configured as a Text - Multiple Choice field with input from another field: Intacct Data > Product Codes: itemid. This supports Justin’s explanation that product codes must match Intacct product code data before line items continue into the invoicing process.
- **Responsible:** TBD

## CUBE-PH4-D4-032
- **Group:** Core Platform
- **Category:** Integration
- **Epic:** Employee and Tax Metadata
- **Parent Task:** Intacct Metadata Values
- **Task Name:** Pull Employee, Product Line, and Tax Metadata for Line Items
- **User Story:** As a CUBE developer, I want line items to pull the required Intacct, employee, tax, vendor, and product metadata so that downstream accounting and invoicing processes have the information they need.
- **Description:** Line items require several metadata values before they can support invoicing and accounting workflows. These values include product line, employee ID, tax-related fields, billing and service state, related vendor, related product code, recurring billing status, and product-code flags such as core product or additional rental. CUBE needs to populate these values consistently when a line item is created.
- **Acceptance Criteria:** 1. The line item stores the product line required for downstream accounting, 2. The line item stores the employee ID associated with the customer owner or related employee, 3. The line item stores tax-related fields such as Avalara tax, initial tax code, billing state, and service state when applicable, 4. The line item stores the related vendor when vendor information is required, 5. The line item stores the related product code and product-code flags such as core product or additional rental, 6. The metadata supports downstream invoicing, accounting, tax, and recurring billing logic.
- **Timestamp:** Day 4, Part 1 [2:31:20 – 2:35:10]
- **Notes:** The screenshot shows the Add Line Item screen with metadata fields such as Product Line, Employee ID, Avalara Tax, Related Product Code, Initial Tax Code, Billing State, Service State, Related Vendor, Recurring Bill Process, Core Product, Additional Rental, Employee Name, and Customer Owner Email. Justin explains that line items need the full Intacct product code, product line, employee ID, and tax code for downstream accounting processes. He also mentions that the employee ID is metadata from an external employee system, currently Paycor and later Paylocity, and should not be treated as the CUBE user ID.
- **Responsible:** TBD

## CUBE-PH4-D4-033
- **Group:** Core Platform
- **Category:** Functional Logic
- **Epic:** Tax Code Reference
- **Parent Task:** Product Code Reference Formula
- **Task Name:** Strip State Prefix to Reference Base Product Code
- **User Story:** As a CUBE developer, I want the line item to strip the state prefix from the full product code when referencing the base product code so that product-code metadata can be pulled correctly.
- **Description:** Line items use a full product code that includes the state prefix, such as TX_PT_DELIVERY. For product-code reference logic, CUBE needs to derive the base product code by removing the state prefix and using the remaining product code to reference the related product code record. This allows the line item to pull related metadata such as tax code, core product flag, and additional rental flag.
- **Acceptance Criteria:** 1. The line item receives or stores the full product code with the state prefix, 2. The system removes the state prefix when deriving the base product code reference, 3. The base product code is used to reference the related product code record, 4. The system pulls the applicable tax code from the related product code, 5. The system pulls product-code flags such as core product and additional rental when applicable, 6. The reference logic is documented so it can be rebuilt correctly in CUBE.
- **Timestamp:** Day 4, Part 1 [2:35:10 – 2:39:30]
- **Notes:** The screenshot shows a line item with Product Code TX_PT_DELIVERY, which includes the state prefix. Justin explains that the full product code is used for Intacct, but the state prefix is stripped out to reference the base product code, such as PT_DELIVERY, and pull related metadata. He also calls this a messy, non-best-practice relationship that needs to be understood during the CUBE rebuild.
- **Responsible:** TBD

## CUBE-PH4-D4-034
- **Group:** Roll-Offs
- **Category:** Functional Logic
- **Epic:** Billing in Arrears
- **Parent Task:** Perm Roll-Off Billing Status
- **Task Name:** Apply Perm Roll-Off Billing Requirements Only After Haul Date Exists
- **User Story:** As a CUBE developer, I want perm roll-off billing statuses to apply only after the haul or end date exists so that users are not warned about missing line items or billing before the haul has occurred.
- **Description:** Perm roll-offs are billed in arrears, so line item and billing requirements should not behave like immediate-billing services. For perm roll-off tickets, CUBE should wait until the haul date or end date exists before triggering line item required, billing required, or related status messages. Once the haul has occurred, the normal billing workflow can apply.
- **Acceptance Criteria:** 1. The system identifies perm roll-off tickets separately from immediate-billing ticket flows, 2. Line item required status does not appear before the haul date or end date exists, 3. Billing required status does not appear before the haul date or end date exists, 4. Once the haul date or end date exists, normal line item and billing requirements apply, 5. Product or ticket status formulas use the haul date or end date condition when evaluating perm roll-off billing requirements, 6. The rebuilt CUBE logic prevents premature billing warnings for perm roll-off tickets.
- **Timestamp:** Day 4, Part 1 [3:03:00 – 3:08:15]
- **Mockups:** NO MOCKUP
- **Notes:** Justin explains that perm roll-offs are billed in arrears, unlike temporary roll-offs or other immediate-billing services. The current logic can show line item or billing requirements too early because it behaves like the ticket should be billed immediately. For CUBE, the key rule is that perm roll-off billing statuses should not apply until the haul date or end date is populated. Justin says the concept is simple, but the implementation may touch multiple fields or formulas.
- **Responsible:** TBD

## CUBE-PH4-D4-035
- **Group:** Service Providers
- **Category:** Architecture
- **Epic:** Phase Scope
- **Parent Task:** Service Provider Module Scope
- **Task Name:** Define Service Provider Module Completion Scope
- **User Story:** As a CUBE project team member, I want the Service Provider module scope to include the related tables required for daily service provider work so that the module can be considered functionally complete before users are moved into CUBE.
- **Description:** The Service Provider module is not complete if it only includes the main service provider record. Service provider users also need related functionality such as PSP pricing zones, PSP pricing, VM tickets, VM activities, out-of-stock information, notes, documents, and other supporting records required for daily work. The project team needs to define which related tables are part of the Service Provider module scope before calling the phase complete.
- **Acceptance Criteria:** 1. The Service Provider module scope identifies the core service provider tables required for daily work, 2. PSP pricing zones and PSP pricing are evaluated as required scope for service provider functionality, 3. VM tickets, VM activities, and out-of-stock records are evaluated as part of the service provider workflow, 4. Notes and documents are evaluated as required supporting functionality for service provider users, 5. Related tables that are only reference-only are distinguished from tables required for daily operations, 6. The Service Provider phase is not considered complete until the required related functionality is defined.
- **Timestamp:** Day 4, Part 1 [3:09:30 – 3:28:45]
- **Mockups:** NO MOCKUP
- **Notes:** Justin explains that a service provider record alone is not enough for the Vendor Management or PSP team to function in CUBE. He specifically calls out PSP pricing zones, PSP pricing, VM tickets, VM activities, out-of-stock records, documents, and notes as related functionality that may be needed before users can realistically work from the Service Provider module. This story captures the phase-boundary and scope decision, not a UI requirement.
- **Responsible:** TBD

## CUBE-PH4-D4-036
- **Group:** Core Platform
- **Category:** Architecture
- **Epic:** Core Support Tables
- **Parent Task:** Notes and Documents Placement
- **Task Name:** Decide Whether Core Support Tables Are Shared or Module-Specific
- **User Story:** As a CUBE developer, I want the team to decide whether notes and documents should be shared across modules or stored within specific modules so that CUBE can balance reuse, performance, and module failure boundaries.
- **Description:** Notes and documents are used by multiple areas of the system, including service providers, customers, sites, and products. CUBE needs a clear architecture decision on whether these records should live in a shared core support module or be stored within the modules that use them most often. The decision should consider performance, inter-node transport calls, reuse, data ownership, and the impact of module failures.
- **Acceptance Criteria:** 1. The team identifies which modules need notes and documents, 2. The team compares shared core support storage against module-specific storage, 3. The decision considers inter-node transport calls when notes or documents are loaded from another module, 4. The decision considers performance for frequently accessed notes and documents, 5. The decision considers how module failures would affect access to notes and documents, 6. The selected structure is defined before migration to avoid rebuilding or moving the same data twice.
- **Timestamp:** Day 4, Part 1 [3:29:45 – 3:39:50]
- **Mockups:** NO MOCKUP
- **Notes:** Justin discusses the trade-off between storing notes and documents in a shared core support area versus keeping records closer to the modules that use them, such as hauler notes inside the Service Provider module. Jose favors a shared service approach for core tables, while Justin highlights the performance and inter-node transport impact of loading frequently used records from another module. This story captures the architecture decision, not a UI requirement.
- **Responsible:** TBD

---
