# CUBE User Stories — Phase 5 Baseline

**Purpose:** Reference baseline for comparing later CUBE phases against Phase 5. Use together with the Phase 2, Phase 3, and Phase 4 baselines when classifying later user stories as **Existing**, **New Feature**, or **Hybrid**.

**Phase 5 scope:**
- Day 1: 37 user stories
- Day 2: 49 user stories
- Day 3: 44 user stories
- Day 4: 40 user stories
- Day 5: 18 user stories
- **Total: 188 user stories**

**Comparison guidance:**
- Compare later stories by underlying functionality, not wording alone.
- Use the User Story together with Description, Acceptance Criteria, Notes, and other provided context.
- A later story may be **Existing** if Phase 5 already covers the same capability, or **Hybrid** if the capability exists but the later phase adds a meaningful behavior, workflow, rule, field, integration, permission, UI change, or extension.
- Phase 5 contains significant Fulfillment, Accounting, AP/AR, inquiry, collections, chargeback, credit, and quality-control workflows; avoid treating generic ticket/dashboard overlap as sufficient evidence of equivalence.

---

# Day 1

**Stories:** 37

## CUBE-PH5-D1-001
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Intake
- **Parent Task:** Invoice Collection
- **Task Name:** Import Supported Vendor Documents from Outlook into ROSSUM
- **User Story:** As an Accounts Payable Supervisor, I want vendor invoices received through the Invoices at ZTERS inbox to be imported through ROSSUM, so that invoice information can be extracted and made available for AP processing.
- **Description:** Vendor invoices are received through the shared Outlook inbox and ROSSUM pulls supported documents for data extraction before sending them to the Hub.
- **Acceptance Criteria:** 1. ROSSUM imports supported accounting documents received through the Invoices at ZTERS inbox, 2. Imported documents retain information identifying their source email, 3. ROSSUM extracts the available accounting information from each document, 4. Imported documents are routed to ROSSUM for classification and review, 5. Confirmed documents are transferred to the appropriate Hub processing section, 6. Emails or documents that cannot be imported automatically remain available for manual handling.
- **Timestamp:** Day 1, Part 1 [00:15:35 - 00:18:35]
- **Notes:** Approximately 10,000 vendor documents are received per month, with higher volume near the beginning of the month.
- **Responsible:** TBD

## CUBE-PH5-D1-002
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Intake
- **Parent Task:** Manual Invoice Collection
- **Task Name:** Handle Invoices Not Recognized by ROSSUM
- **User Story:** As an Accounts Payable Supervisor, I want vendor invoices that cannot be imported automatically to be manually retrieved and uploaded to ROSSUM, so that they can enter the standard invoice review and processing workflow.
- **Description:** Some vendor emails provide an invoice through a link or external portal instead of attaching a supported document. In these cases, an AP user must open the link, access the vendor portal when required, download the invoice, and upload it manually to ROSSUM for review.
- **Acceptance Criteria:** 1. Users can identify invoice emails that were not imported automatically, 2. Users can access invoice links or vendor portals from the original email, 3. Users can download the available invoice document, 4. ROSSUM provides an Upload action for manually retrieved documents, 5. Manually uploaded invoices enter the appropriate ROSSUM review queue, 6. Non-invoice communications can be excluded from invoice processing.
- **Timestamp:** Day 1, Part 1 [00:18:35 - 00:22:03]
- **Notes:** The workshop estimated that approximately 95% of invoices reach ROSSUM automatically and 5% require manual handling.
- **Responsible:** TBD

## CUBE-PH5-D1-003
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Intake
- **Parent Task:** Document Classification
- **Task Name:** Classify and Route Incoming Accounting Documents
- **User Story:** As an Accounts Payable Supervisor, I want ROSSUM to classify incoming accounting documents by type, so that each document is routed to the appropriate review and processing queue.
- **Description:** Documents initially enter the ROSSUM Inbox. ROSSUM evaluates each document and attempts to identify whether it is a bill, paid bill, payment receipt, or statement. Documents that cannot be classified confidently remain available for manual review.
- **Acceptance Criteria:** 1. Incoming documents initially appear in the ROSSUM Inbox, 2. ROSSUM attempts to determine the document type using its confidence result, 3. The identified type is displayed in the Document Type field, 4. Classified documents are routed to the corresponding Bills, Statements, or Payment Receipts queue, 5. Documents without a confident classification remain in Reviews for manual handling, 6. Users can review and correct an incorrect document classification.
- **Timestamp:** Day 1, Part 1 [00:23:02 - 00:27:55]
- **Notes:** Statements are useful for identifying outstanding invoices but contain less service detail than invoices.
- **Responsible:** TBD

## CUBE-PH5-D1-004
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Intake
- **Parent Task:** Extraction Review
- **Task Name:** Confirm Extracted Invoice Information
- **User Story:** As an Accounts Payable Supervisor, I want extracted invoice fields and line items reviewed before confirmation, so that accurate and searchable invoice information is transferred to the Hub.
- **Description:** ROSSUM displays the source invoice beside the extracted metadata, basic information, and line-item details. The reviewer compares the extracted values with the invoice and confirms or corrects them before completing the review.
- **Acceptance Criteria:** 1. ROSSUM displays the source invoice beside the extracted information, 2. The reviewer can verify the document type, document ID, and purchase order number, 3. The reviewer can verify the issue date, due date, and available billing or service period, 4. The reviewer can verify the customer information and service address when available, 5. The reviewer can review extracted line-item descriptions, quantities, rates, and amounts, 6. Incorrect extracted values can be corrected before the document is confirmed and transferred to the Hub.
- **Timestamp:** Day 1, Part 1 [00:23:02 - 00:30:40]
- **Notes:** The side-by-side review allows users to compare each extracted value directly with the source invoice.
- **Responsible:** TBD

## CUBE-PH5-D1-005
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Document Workflow
- **Task Name:** Organize AP Bills by Processing Status
- **User Story:** As an Accounts Payable Supervisor, I want invoice documents organized by processing status, so that I can quickly identify and access bills at each stage of the AP workflow.
- **Description:** The Hub Accounts Payable Bills page organizes invoice documents into status-based views. Each status tab displays the number of documents currently assigned to that stage and filters the table when selected.
- **Acceptance Criteria:** 1. The page provides an All view containing every available bill, 2. Bills are organized into New, In Progress, Inquiring, Ready for Intacct, Booked/Revisit Needed, Complete, Invalid, and Duplicate statuses, 3. Each status tab displays the number of documents it contains, 4. Selecting a status displays only the documents assigned to that status, 5. A document appears under the status representing its current processing stage, 6. Users can open a listed document from the selected status view.
- **Timestamp:** Day 1, Part 1 [00:28:33 - 00:31:58]
- **Notes:** Statuses represent different stages or outcomes of the AP workflow. Invalid covers documents that should not continue through invoice processing, while Duplicate identifies repeated invoice documents.
- **Responsible:** TBD

## CUBE-PH5-D1-006
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Work Assignment
- **Task Name:** Auto-Assign Oldest Invoices to AP Users
- **User Story:** As an Accounts Payable Supervisor, I want AP users to automatically assign themselves the oldest available invoices when their workload is below the permitted threshold, so that older invoices are prioritized and assigned to a visible owner.
- **Description:** From Accounts Payable > Reports > My Reports, AP users can use the Auto Assign function to receive additional invoices. The page displays the user's current total amount of new invoices and permits another assignment when that total is below $2,500.
- **Acceptance Criteria:** 1. The Auto Assign section displays the user's current total amount of new invoices, 2. Users can select Assign me more invoices when their assigned total is below $2,500, 3. The assignment process prioritizes the oldest available invoice dates, 4. Assigned invoices are associated with the user who requested them, 5. Users can preview the bills that will be automatically assigned, 6. Users can preview the related auto-assignment statistics before requesting additional invoices.
- **Timestamp:** Day 1, Part 1 [00:31:58 - 00:33:37]
- **Notes:** The assignment threshold is based on the total value of the user's new invoices rather than only the number of documents. The assigned user should remain visible on each invoice after assignment.
- **Responsible:** TBD

## CUBE-PH5-D1-007
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Vendor Matching
- **Task Name:** Match an Invoice to the Correct Service Provider
- **User Story:** As an Accounts Payable Supervisor, I want invoices matched to the correct service provider using the purchase order, linked site, and Vendor ID, so that AP can process the invoice against the correct vendor record.
- **Description:** The Hub uses the extracted purchase order to identify and link the related site. It then compares the extracted vendor information with the service providers associated with that site. A valid Vendor ID is required for the matching process to work effectively.
- **Acceptance Criteria:** 1. The system uses the extracted purchase order to identify the related site, 2. The linked Site ID and service address are displayed, 3. The extracted vendor name and address are displayed separately from the linked service provider information, 4. Vendor matching uses the Vendor ID associated with the service provider record, 5. The system displays a warning when the service provider does not have a Vendor ID, 6. Users can select or correct the linked service provider when an automatic match cannot be completed.
- **Timestamp:** Day 1, Part 1 [00:36:12 - 00:38:56]
- **Notes:** When only one service provider is associated with the linked site, the system may link it automatically. When multiple service providers are available, AP must verify and select the correct record by comparing the extracted vendor information.
- **Responsible:** TBD

## CUBE-PH5-D1-008
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Duplicate Management
- **Task Name:** Identify Duplicate Invoice Documents
- **User Story:** As an Accounts Payable Supervisor, I want duplicate invoices grouped with their original document, so that AP does not process and pay the same vendor invoice more than once.
- **Description:** The duplicate key uses the vendor ID and extracted document number, and related documents show their processing status in a linked table.
- **Acceptance Criteria:** 1. A duplicate key is created after the vendor is linked, 2. The key combines the vendor ID and extracted document number, 3. The oldest matching document is identified as the original, 4. Later matching documents receive a duplicate status, 5. Users can view every document in the duplicate group, 6. The group displays each document's current status and completion information when available.
- **Timestamp:** Day 1, Part 1 [00:38:56 - 00:40:55]
- **Mockups:** NO MOCKUP
- **Notes:** A large duplicate group may require AP to investigate why the vendor repeatedly sent the invoice.
- **Responsible:** TBD

## CUBE-PH5-D1-009
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Invoice Verification
- **Task Name:** Compare Extracted and Linked Invoice Information
- **User Story:** As an Accounts Payable Supervisor, I want extracted invoice information displayed beside the linked service provider and site information, so that I can verify the invoice was matched to the correct records before processing it.
- **Description:** The invoice document view displays the extracted document summary, service provider information, and service address alongside the corresponding records linked from the Hub. This allows AP to identify discrepancies before continuing with invoice processing.
- **Acceptance Criteria:** 1. The Document Summary displays the extracted document number, total, terms, invoice date, due date, and service span when available, 2. The Service Provider Info section displays the linked Vendor ID, name, and address, 3. The extracted service provider name and address are displayed separately from the linked values, 4. The Service Address section displays the extracted purchase order and address, 5. The linked Site ID and address are displayed beside the extracted service information, 6. Users can correct the linked service provider or site when the extracted and linked information does not correspond.
- **Timestamp:** Day 1, Part 1 [00:40:55 - 00:46:30]
- **Notes:** Users can unlink and relink the site or service provider when the original match is incorrect. The screenshot also shows a confirmation message after the service provider is mapped successfully.
- **Responsible:** TBD

## CUBE-PH5-D1-010
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Reference Information
- **Task Name:** Separate Vendor and Invoice Document Notes
- **User Story:** As an Accounts Payable Supervisor, I want vendor notes and invoice document notes displayed in separate sections, so that recurring vendor guidance is not confused with information related to a single invoice.
- **Description:** Vendor Notes contain guidance that applies to the linked service provider across multiple invoices, such as payment contacts or special payment instructions. The document Notes field records research, follow-up activities, or issues that apply only to the current invoice.
- **Acceptance Criteria:** 1. Vendor Notes are displayed in a dedicated section associated with the linked service provider, 2. Users can add a new vendor note from the invoice view, 3. Each vendor note displays its date, author, and content, 4. Hidden vendor notes can be displayed when needed, 5. Invoice-specific notes are entered in a separate Notes field under Document Processing Info, 6. Saving an invoice-specific note does not add or modify a vendor-level note.
- **Timestamp:** Day 1, Part 1 [00:44:18 - 00:49:15]
- **Notes:** Vendor notes may include payment contacts, payment instructions, or vendor-specific responsibilities. Invoice notes may document actions such as calling the service provider to clarify a charge. Assigned Back Notes are displayed separately when a completed document is returned for correction.
- **Responsible:** TBD

## CUBE-PH5-D1-011
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Completed Document Control
- **Task Name:** Reassign Completed Documents for Correction
- **User Story:** As an Accounts Payable Supervisor, I want completed invoice documents reassigned before protected fields are edited, so that payment decisions can be corrected without leaving completed records freely editable.
- **Description:** Completed documents lock their fields; reassignment is required when AP must change an amount, payment method, or other completed information.
- **Acceptance Criteria:** 1. Document fields become locked when the document reaches Completed status, 2. Locked fields cannot be edited directly, 3. A completed document can be reassigned for correction, 4. Reassignment restores access to the fields that require changes, 5. Users can change a previously selected payment method after reassignment, 6. The reassignment is recorded on the document.
- **Timestamp:** Day 1, Part 1 [00:47:10 - 00:49:50]
- **Mockups:** NO MOCKUP
- **Notes:** Examples included changing an amount that should no longer be paid or changing payment from Visa to check.
- **Responsible:** TBD

## CUBE-PH5-D1-012
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Invoice Review
- **Task Name:** Review Extracted Invoice Line Items and Source PDF
- **User Story:** As an Accounts Payable Supervisor, I want standardized extracted invoice line items and on-demand access to the source PDF, so that I can process the invoice from the extracted information and consult the original document when clarification is needed.
- **Description:** The Hub displays invoice information extracted by ROSSUM in a standardized line-item table. A PDF Preview is available beside the extracted information so AP can compare questionable values with the original invoice without leaving the document page.
- **Acceptance Criteria:** 1. The Extracted Information section displays the available billing or service period, 2. Extracted line items display the start date, end date, code, description, quantity, unit of measure, unit price, fees, and total amount when available, 3. Extracted totals display the available subtotal, fees, tax, amount paid, amount due, and line-item total, 4. Users can display the source invoice in the PDF Preview, 5. Users can hide the PDF Preview when it is not required, 6. Users can download the source PDF from the invoice view.
- **Timestamp:** Day 1, Part 1 [00:49:15 - 00:52:57]
- **Notes:** The objective is to let AP process invoices primarily from standardized extracted information while preserving direct access to the original invoice for verification.
- **Responsible:** TBD

## CUBE-PH5-D1-013
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Extraction Quality
- **Task Name:** Report ROSSUM Extraction Errors
- **User Story:** As an Accounts Payable Supervisor, I want to report incorrect extracted invoice information, so that extraction or review mistakes can be documented and shared with the ROSSUM team.
- **Description:** The Report Error function captures an explanation of the extraction problem and adds it to an error report reviewed by the person managing the ROSSUM team.
- **Acceptance Criteria:** 1. Users can report an error from the invoice document, 2. Users can describe the incorrect extraction, 3. The error is associated with the affected document, 4. The reviewer responsible for the ROSSUM confirmation remains identifiable, 5. Reported errors are added to a downloadable error list, 6. The error list can be provided to the ROSSUM team for review.
- **Timestamp:** Day 1, Part 1 [00:52:57 - 00:54:19]
- **Mockups:** NO MOCKUP
- **Notes:** The errors list is currently downloaded and shared with the ROSSUM team approximately once per month.
- **Responsible:** TBD

## CUBE-PH5-D1-014
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Auditability
- **Task Name:** View the Invoice Processing Audit Trail
- **User Story:** As an Accounts Payable Supervisor, I want an audit trail of invoice-processing changes, so that I can review how the document was imported, linked, assigned, classified, and updated throughout its workflow.
- **Description:** Each invoice record includes an expandable Audit Trail that records user actions and automatic system actions. This history helps AP identify how the invoice entered the Hub and how its related site, service provider, assignment, and duplicate information changed during processing.
- **Acceptance Criteria:** 1. Each invoice record includes an expandable Audit Trail section, 2. The audit trail records when the document is imported into the Hub, 3. Automatic site-linking actions are recorded, 4. Changes to the assigned AP user are recorded, 5. Service provider linking and duplicate-group creation are recorded, 6. Each entry identifies whether the change resulted from a user action or an automatic system process.
- **Timestamp:** Day 1, Part 1 [00:54:19 - 00:55:07]
- **Notes:** The screenshot confirms that the Audit Trail is located near the bottom of the invoice record, below the ROSSUM Details and duplicate-group information. The transcript demonstrates entries for import, automatic site linking, assignment, service provider linking, and automatic duplicate classification.
- **Responsible:** TBD

## CUBE-PH5-D1-015
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Invoice Processing
- **Parent Task:** Cost Audit
- **Task Name:** Compare Bills with Item Receipts and Vendor Invoices
- **User Story:** As an Accounts Payable Supervisor, I want pending item receipts, converted item receipts, and prior vendor invoices displayed for the linked site and service provider, so that I can compare the current bill with expected costs and previous payments.
- **Description:** After the service provider and site are linked, the Hub displays related Intacct records in separate Pending Item Receipts, Vendor Invoices, and Converted Item Receipts views. AP uses this information to verify billing periods, expected amounts, product details, and previously processed invoices.
- **Acceptance Criteria:** 1. The invoice view provides separate tabs for Pending Item Receipts, Vendor Invoices, and Converted Item Receipts, 2. Each tab displays the number of available related records, 3. Records display the Vendor ID, vendor name, date, document number, total, site address, Site ID, QuickBase order number, product details, and payment method when available, 4. Pending item receipts can be identified as exact or potential matches, 5. Users can search the records displayed in the selected tab, 6. Users can synchronize the displayed information with the source accounting data.
- **Timestamp:** Day 1, Part 1 [00:55:59 - 01:00:53]
- **Notes:** AP primarily reviews Pending Item Receipts and Vendor Invoices. The Hub displays this Intacct information directly so users do not have to leave the invoice record to perform the comparison.
- **Responsible:** TBD

## CUBE-PH5-D1-016
- **Group:** Fulfillment
- **Category:** Improvement
- **Epic:** Service Tickets
- **Parent Task:** Ticket Review
- **Task Name:** Display Quantity in Service-Ticket Line Items
- **User Story:** As a Fulfillment Representative, I want the service quantity displayed directly in the service ticket’s line-item history, so that AP and Fulfillment can verify the billed quantity without opening or editing the individual line item.
- **Description:** The service-ticket record includes a History section containing its related line items. Each row should display the recorded quantity alongside the product description, payment information, line-item amount, total, and invoice status.
- **Acceptance Criteria:** 1. The service-ticket History section includes a Quantity column, 2. Each line-item row displays its recorded quantity, 3. The quantity is visible without opening or editing the line item, 4. The displayed quantity corresponds to the related service-ticket line item, 5. Quantity is displayed alongside the product description and financial information, 6. AP and Fulfillment users can use the displayed quantity when comparing the service ticket with a vendor invoice.
- **Timestamp:** Day 1, Part 1 [01:00:53 - 01:01:39]
- **Notes:** The Quantity column was added to the QuickBase service-ticket view during the workshop. This visibility should be retained when the functionality is transferred to CUBE.
- **Responsible:** TBD

## CUBE-PH5-D1-017
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Inquiry Creation
- **Task Name:** Create an Accounting Inquiry from the Hub Invoice
- **User Story:** As an Accounts Payable Supervisor, I want to create an accounting inquiry directly from the Hub invoice, so that the invoice, vendor, site, document, and available dates do not have to be downloaded and entered again manually.
- **Description:** The current process requires downloading the invoice, navigating to the QuickBase site, creating the inquiry, selecting the vendor, entering dates, and attaching the file.
- **Acceptance Criteria:** 1. A Create Accounting Inquiry action is available from the invoice, 2. The related site is carried into the inquiry, 3. The linked vendor is carried into the inquiry, 4. The invoice document is attached or linked automatically, 5. Available invoice and due-date information is carried into the inquiry, 6. Users can navigate between the inquiry and the source Hub document.
- **Timestamp:** Day 1, Part 1 [01:06:06 - 01:08:45]
- **Mockups:** NO MOCKUP
- **Notes:** Accounting inquiries are created at the site level because one invoice can cover multiple products.
- **Responsible:** TBD

## CUBE-PH5-D1-018
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Vendor Selection
- **Task Name:** Search Related Vendors by Vendor ID
- **User Story:** As an Accounts Payable Supervisor, I want to search and select an inquiry's related vendor by vendor ID, so that I can identify the correct vendor when several records have similar company names.
- **Description:** AP frequently knows the vendor ID, and vendor names such as Waste Connections can return many related company records.
- **Acceptance Criteria:** 1. The related-vendor picker supports vendor ID searches, 2. Search results display the vendor ID, 3. Search results display the vendor name, 4. The vendor ID uniquely identifies the selected record, 5. Users can distinguish similarly named vendor records, 6. The selected vendor is linked to the accounting inquiry.
- **Timestamp:** Day 1, Part 1 [01:08:45 - 01:10:57]
- **Mockups:** NO MOCKUP
- **Notes:** Vendor ID and vendor name were identified as the two most important vendor-selection values.
- **Responsible:** TBD

## CUBE-PH5-D1-019
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Inquiry Summary
- **Task Name:** Optimize the Site Accounting-Inquiry Table
- **User Story:** As an Accounts Payable Supervisor, I want the site accounting-inquiry table to prioritize actionable information, so that I can review an inquiry’s status, issue, ownership, and resolution without excessive scrolling or opening every record.
- **Description:** The current QuickBase table contains redundant site information and multiple workflow checkbox columns that make the report difficult to review. The CUBE table should prioritize the fields AP uses to understand the issue, identify the service provider, and review the actions taken by Account Management and Fulfillment.
- **Acceptance Criteria:** 1. The table displays the date created, issue spotter, inquiry status, and issue, 2. Service provider name and Vendor ID appear near the beginning of the table, 3. AM and Fulfillment progress notes are available from the table, 4. AM actions taken, Fulfillment actions taken, and the AM invoice number are displayed when available, 5. Issue conclusion and resolution summary are displayed, 6. Redundant site details and individual workflow checkbox columns already represented by the inquiry status are excluded from the primary table view.
- **Timestamp:** Day 1, Part 1 [01:11:17 - 01:22:07]
- **Notes:** The screenshot represents the current QuickBase report before optimization. Columns such as New, Researching, Submitted for Approval, Approved, No Issue, and Close File were identified as unnecessary when the overall Status already communicates the inquiry stage.
- **Responsible:** TBD

## CUBE-PH5-D1-020
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Escalation Management
- **Task Name:** Create and Link a VM Ticket to an Accounting Inquiry
- **User Story:** As an Accounts Payable Supervisor, I want to create and view a VM ticket directly related to an accounting inquiry, so that I can escalate an unresolved service provider issue and track the escalation from the inquiry.
- **Description:** AP uses a VM ticket when an accounting inquiry requires assistance from Vendor Management or the assigned service provider specialist. The ticket should inherit the relevant inquiry and service provider information and maintain a direct relationship with the originating accounting inquiry.
- **Acceptance Criteria:** 1. Users can create a VM ticket from an accounting inquiry, 2. The related service provider name and Vendor ID are carried into the VM ticket, 3. Accounting Inquiry Assistance Needed is available as a VM ticket category, 4. The ticket can be created with High priority and Opening status, 5. The VM ticket maintains a direct relationship with the originating accounting inquiry, 6. The accounting inquiry displays the related VM ticket number, link, status, and assigned team member.
- **Timestamp:** Day 1, Part 1 [01:24:00 - 01:30:16]
- **Notes:** The current QuickBase form uses Service Provider Pricing Issue because a dedicated accounting-inquiry category is unavailable. It creates a ticket for the service provider, but the accounting inquiry is only identifiable when manually mentioned in the notes.
- **Responsible:** TBD

## CUBE-PH5-D1-021
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Vendor Context
- **Task Name:** Display Open Vendor VM Tickets on an Inquiry
- **User Story:** As an Accounts Payable Supervisor, I want open VM tickets for the inquiry's vendor displayed on the inquiry page, so that I can identify an existing vendor-wide issue that may also explain the current inquiry.
- **Description:** An open price-increase ticket for the same vendor may apply across multiple sites and prevent duplicate investigation.
- **Acceptance Criteria:** 1. The inquiry displays open VM tickets for the related vendor, 2. Closed VM tickets are excluded from the default display, 3. Each displayed ticket includes its identifying information, 4. Users can open a displayed VM ticket, 5. A VM ticket directly related to the current inquiry is visually distinguished, 6. Users can access the vendor record to review additional ticket history.
- **Timestamp:** Day 1, Part 1 [01:30:20 - 01:32:05]
- **Mockups:** NO MOCKUP
- **Notes:** Showing only open tickets was requested to avoid overcrowding the page.
- **Responsible:** TBD

## CUBE-PH5-D1-022
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Accounting Inquiries
- **Parent Task:** AP Research
- **Task Name:** Research an Inquiry Before Assigning Other Teams
- **User Story:** As an Accounts Payable Supervisor, I want an inquiry to begin in AP Researching with issue and progress notes, so that AP can attempt to resolve the discrepancy before requiring action from Fulfillment or the Account Manager.
- **Description:** AP first documents the suspected discrepancy, verifies quoted service rates, and may contact the vendor without sending the inquiry to another department.
- **Acceptance Criteria:** 1. New inquiries begin in AP Researching, 2. AP can document the suspected issue, 3. AP can compare billed rates with recorded rates, 4. AP can add progress notes while researching, 5. AP can contact the vendor before involving another team, 6. The inquiry remains assigned to AP unless another team's action is explicitly required.
- **Timestamp:** Day 1, Part 1 [01:32:19 - 01:37:18]
- **Mockups:** NO MOCKUP
- **Notes:** Rate details may require reviewing fulfillment-ticket notes because product pages store rolled-up vendor charges.
- **Responsible:** TBD

## CUBE-PH5-D1-023
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Cost Calculation
- **Task Name:** Calculate Expected Additional Vendor Cost
- **User Story:** As an Accounts Payable Supervisor, I want calculation support when recording expected additional vendor cost, so that I can calculate the variance between quoted and billed amounts without relying entirely on an external calculator.
- **Description:** AP currently performs calculations outside the inquiry and manually enters the expected additional cost.
- **Acceptance Criteria:** 1. Users can enter the quoted or expected amount, 2. Users can enter the billed amount, 3. Users can include the applicable quantity or number of service periods, 4. The system calculates the difference, 5. The calculated value can populate the expected additional vendor cost, 6. Users can adjust the calculation when the invoice contains more than one issue.
- **Timestamp:** Day 1, Part 1 [01:37:18 - 01:45:27]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop rejected excessive field granularity but supported a calculation aid or limited automatic calculation.
- **Responsible:** TBD

## CUBE-PH5-D1-024
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Form Usability
- **Task Name:** Prevent Keyboard Navigation from Selecting High Priority
- **User Story:** As an Accounts Payable Supervisor, I want keyboard tabbing to move through inquiry fields without selecting High Priority, so that an inquiry is marked urgent only through an intentional user action.
- **Description:** Participants reported that tabbing through the inquiry form could select the High Priority checkbox unintentionally.
- **Acceptance Criteria:** 1. Pressing Tab moves focus to the High Priority control, 2. Focusing the control does not change its value, 3. High Priority remains unselected by default, 4. The user must intentionally select High Priority, 5. Continuing to tab does not toggle the control, 6. The saved priority matches the user's intentional selection.
- **Timestamp:** Day 1, Part 1 [01:47:20 - 01:48:26]
- **Mockups:** NO MOCKUP
- **Notes:** The behavior was discussed as an existing QuickBase issue that should not be reproduced in CUBE.
- **Responsible:** TBD

## CUBE-PH5-D1-025
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Hub Integration
- **Task Name:** Synchronize Inquiry Information Back to the Hub
- **User Story:** As an Accounts Payable Supervisor, I want the inquiry link, issue notes, and status written back to the source Hub invoice, so that the invoice remains connected to its inquiry and is not processed again until the inquiry is resolved.
- **Description:** After creating an inquiry, AP currently copies the inquiry link and issue information into the Hub and manually changes the document to Inquiring.
- **Acceptance Criteria:** 1. The source Hub document stores a link to the created inquiry, 2. The inquiry stores a link to the source Hub document, 3. Inquiry issue information is available from the Hub document, 4. The Hub document moves to Inquiring when the inquiry is created, 5. The document remains in Inquiring while the issue is unresolved, 6. The invoice can return to processing after the inquiry is resolved.
- **Timestamp:** Day 1, Part 1 [01:48:26 - 01:50:55]
- **Mockups:** NO MOCKUP
- **Notes:** The source invoice is considered finished in the Hub until the related inquiry is resolved.
- **Responsible:** TBD

## CUBE-PH5-D1-026
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Accounting Inquiries
- **Parent Task:** Inquiry Resolution
- **Task Name:** Return Every Inquiry to AP for Closure
- **User Story:** As an Accounts Payable Supervisor, I want every accounting inquiry returned to AP after all required teams complete their work, so that AP can finalize the invoice, pay the vendor, and close the inquiry.
- **Description:** Inquiry resolution can be handled only by AP or can require Account Manager and Fulfillment participation, but AP performs the final close.
- **Acceptance Criteria:** 1. AP can resolve an inquiry without involving another team when appropriate, 2. AP can require Account Manager action, 3. AP can require Fulfillment action, 4. Completed team actions return the inquiry to the AP issue spotter, 5. AP reviews the final resolution before payment, 6. AP closes the inquiry after the invoice is booked and the vendor payment is handled.
- **Timestamp:** Day 1, Part 1 [01:50:55 - 02:10:22]
- **Mockups:** NO MOCKUP
- **Notes:** Inquiries also document vendor problems and support later vendor performance analysis.
- **Responsible:** TBD

## CUBE-PH5-D1-027
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Accounting Inquiries
- **Parent Task:** Approvals and Alerts
- **Task Name:** Notify Users at Each Inquiry Workflow Stage
- **User Story:** As an Accounts Payable Supervisor, I want responsible users notified when an accounting inquiry requires their action or approval, so that the inquiry moves through AP, Account Management, Fulfillment, and lead review.
- **Description:** Current email notifications correspond to workflow statuses; CUBE is expected to replace much of this with actionable internal alerts.
- **Acceptance Criteria:** 1. The Account Manager is notified when AM action is required, 2. The Fulfillment Representative is notified when Fulfillment action is required, 3. The CSS is notified when AM work is submitted for approval, 4. The Fulfillment lead is notified when Fulfillment work is submitted for approval, 5. The AP issue spotter is notified after required approvals are completed, 6. Alerts identify the inquiry and the action required from the recipient.
- **Timestamp:** Day 1, Part 1 [02:11:23 - 02:16:09]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop identified missing active notifications for both CSS and Fulfillment lead approval steps.
- **Responsible:** TBD

## CUBE-PH5-D1-028
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Accounting Inquiries
- **Parent Task:** Approval Controls
- **Task Name:** Require Approval for High Additional Vendor Costs
- **User Story:** As an Accounts Payable Supervisor, I want inquiries with more than $500 in actual additional vendor cost routed to an AP lead, so that a larger-than-expected payment receives additional review.
- **Description:** The current workflow requires AP lead approval when the final actual additional cost exceeds $500.
- **Acceptance Criteria:** 1. The inquiry stores the actual additional vendor cost, 2. The system compares that value with the $500 threshold, 3. Values above $500 require AP lead approval, 4. The AP lead receives an action notification, 5. The inquiry cannot complete the approval step before the AP lead responds, 6. The AP lead's decision is recorded on the inquiry.
- **Timestamp:** Day 1, Part 1 [02:12:15 - 02:16:09]
- **Mockups:** NO MOCKUP
- **Notes:** The threshold applies to actual additional cost rather than the initial expected additional cost.
- **Responsible:** TBD

## CUBE-PH5-D1-029
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Accounting Inquiries
- **Parent Task:** Performance Tracking
- **Task Name:** Track Inquiry Workflow Timestamps and Durations
- **User Story:** As an Accounts Payable Supervisor, I want each inquiry action timestamped with its responsible user and duration, so that response times and workflow bottlenecks can be measured by team and approval stage.
- **Description:** The current system records when required actions begin, when users start reviewing, when work is submitted, and when lead approvals occur.
- **Acceptance Criteria:** 1. The system timestamps each workflow-stage change, 2. The system records the user who completed each action, 3. Response time is calculated from assignment to review, 4. Approval time is calculated from submission to lead decision, 5. Total time is calculated for each team's required work, 6. Duration data is available for KPI reports.
- **Timestamp:** Day 1, Part 1 [02:18:38 - 02:23:57]
- **Mockups:** NO MOCKUP
- **Notes:** Existing reporting primarily distinguishes response times above or below 24 hours; the workshop requested more useful ranges while noting that final thresholds remain to be defined.
- **Responsible:** TBD

## CUBE-PH5-D1-030
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Inquiry Detection
- **Task Name:** Flag Potential Accounting Inquiries from Invoice Variances
- **User Story:** As an Accounts Payable Supervisor, I want invoice variances flagged as potential inquiries, so that AP receives assistance identifying mismatches without automatically creating unnecessary accounting inquiries.
- **Description:** A variance or item-receipt mismatch can suggest a problem, but rolled-up expected costs—especially for roll-offs—may legitimately differ from the invoice.
- **Acceptance Criteria:** 1. The system compares available invoice amounts with expected amounts, 2. A mismatch can be flagged as a potential inquiry, 3. The flag does not automatically create an inquiry, 4. The user can review the mismatch before deciding, 5. A Create Accounting Inquiry action is available from the flag, 6. Product-specific comparison limitations can be considered when displaying the flag.
- **Timestamp:** Day 1, Part 1 [02:24:19 - 02:26:40]
- **Mockups:** NO MOCKUP
- **Notes:** The group explicitly preferred flagging and assisted creation over automatic inquiry creation.
- **Responsible:** TBD

## CUBE-PH5-D1-031
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Actionable Notifications
- **Task Name:** Notify Responsible Users About Overdue Inquiry Actions
- **User Story:** As a Fulfillment Representative, I want an internal notification when my required inquiry action exceeds its defined time expectation, so that I can act before the inquiry remains unattended for an extended period.
- **Description:** The current process relies on reports and manual reviews; CUBE is expected to deliver focused, actionable notifications and avoid excessive email alerts.
- **Acceptance Criteria:** 1. Each action stage can have a defined time expectation, 2. The system detects when the assigned user has not completed the expected action, 3. The directly responsible user receives an internal notification, 4. The notification identifies the overdue inquiry and required action, 5. Users can clear or review notifications from a notification log, 6. Indirect stakeholders receive summarized information instead of repeated per-inquiry alerts when configured.
- **Timestamp:** Day 1, Part 1 [02:30:11 - 02:36:52]
- **Mockups:** NO MOCKUP
- **Notes:** Final timing thresholds were not established in this workshop and must remain configurable or TBD.
- **Responsible:** TBD

## CUBE-PH5-D1-032
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Status Visibility
- **Task Name:** Display Overall and Team-Specific Inquiry Statuses
- **User Story:** As an Accounts Payable Supervisor, I want separate overall, Account Management, Fulfillment, and AP statuses displayed prominently, so that I can understand inquiry progress without interpreting a single compound status.
- **Description:** The existing combined status can become blank or require many status combinations when more than one team is involved.
- **Acceptance Criteria:** 1. The inquiry displays an overall status, 2. The inquiry displays an Account Management status, 3. The inquiry displays a Fulfillment status, 4. The inquiry displays an AP status, 5. Statuses are visible near the top of the inquiry, 6. Visual indicators distinguish incomplete, in-progress, warning, and completed states.
- **Timestamp:** Day 1, Part 1 [02:38:27 - 02:47:46]
- **Mockups:** NO MOCKUP
- **Notes:** The proposed CUBE design uses consistent health and status blocks rather than one exponentially complex compound field.
- **Responsible:** TBD

## CUBE-PH5-D1-033
- **Group:** Accounting
- **Category:** Functional
- **Epic:** Accounting Inquiries
- **Parent Task:** Resolution Workflow
- **Task Name:** Capture Recurring Costs and Prevent Repeated Inquiries
- **User Story:** As a Fulfillment Representative, I want recurring vendor costs recorded and the related product pricing updated, so that future item receipts reflect the accepted cost and the same discrepancy does not repeatedly create inquiries.
- **Description:** When an inquiry identifies a continuing price increase or recurring charge, the responsible workflow must document it and update the source data used for later invoices.
- **Acceptance Criteria:** 1. Users can identify a resolved cost as recurring, 2. The recurring cost is documented on the inquiry, 3. The affected product or service is identified, 4. The related product-page vendor cost is updated through the responsible process, 5. Supporting documents can be attached when available, 6. Future expected costs use the updated vendor rate.
- **Timestamp:** Day 1, Part 1 [02:52:16 - 03:01:24]
- **Mockups:** NO MOCKUP
- **Notes:** A vendor-wide price increase may require a VM ticket and updates across multiple active product records.
- **Responsible:** TBD

## CUBE-PH5-D1-034
- **Group:** Fulfillment
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Fulfillment Ticket Selection
- **Task Name:** Select a Related Fulfillment Ticket from the Inquiry
- **User Story:** As a Fulfillment Representative, I want relevant fulfillment tickets displayed and selectable from the accounting inquiry, so that the correct representative and lead can be assigned without leaving the inquiry to search the site.
- **Description:** The inquiry is related to one vendor and site, but the site can contain many tickets across products and ticket types.
- **Acceptance Criteria:** 1. The inquiry displays tickets for the related vendor and site, 2. Tickets are collapsed by default, 3. Tickets are grouped first by product line, 4. Tickets are grouped by ticket type within each product line, 5. Quote Request and Delivery tickets are prioritized because they commonly contain pricing, 6. Ticket dates and record IDs are displayed to support selection.
- **Timestamp:** Day 1, Part 1 [03:08:00 - 03:19:40]
- **Mockups:** NO MOCKUP
- **Notes:** When no exact ticket exists, the current process is to select the most closely related or most recent relevant ticket.
- **Responsible:** TBD

## CUBE-PH5-D1-035
- **Group:** Fulfillment
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Fulfillment Assignment Validation
- **Task Name:** Require a Fulfillment Ticket When Fulfillment Action Is Required
- **User Story:** As a Fulfillment Representative, I want the system to require a related fulfillment ticket when Fulfillment action is selected, so that the inquiry is assigned to an identifiable Fulfillment Representative and lead.
- **Description:** The workshop found open Fulfillment-required inquiries without tickets because users could select the action checkbox and save without linking a ticket.
- **Acceptance Criteria:** 1. Selecting Fulfillment Action Required activates fulfillment-ticket validation, 2. The user must link a fulfillment ticket before saving and closing, 3. The system displays a clear validation message when no ticket is linked, 4. The user can return to the form and select a ticket, 5. The user can instead remove Fulfillment Action Required when Fulfillment is not needed, 6. The linked ticket supplies the Fulfillment Representative and lead information.
- **Timestamp:** Day 1, Part 1 [03:15:42 - 03:18:49]
- **Mockups:** NO MOCKUP
- **Notes:** The unused Fulfillment Ticket Not Applicable checkbox was removed during the workshop because the participants could not identify a current process for it.
- **Responsible:** TBD

## CUBE-PH5-D1-036
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Final Resolution Review
- **Task Name:** Allow AP to Reject and Return a Team Resolution
- **User Story:** As an Accounts Payable Supervisor, I want to reject an Account Management or Fulfillment resolution and return the inquiry for additional work, so that AP does not have to accept and pay a vendor amount it considers unsupported.
- **Description:** AP performs the final review and payment and requested a structured disagreement workflow comparable to a lead rejecting a submitted team action.
- **Acceptance Criteria:** 1. AP can mark that it disagrees with the submitted resolution, 2. AP can provide the reason for the disagreement, 3. The inquiry returns to the responsible team, 4. The team's prior approval state is reset when additional work is required, 5. The responsible user receives an actionable notification, 6. The inquiry cannot be closed until AP accepts the revised resolution.
- **Timestamp:** Day 1, Part 1 [03:53:54 - 03:59:48]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript example involved AP challenging a proposed full payment of $3,000 for old sandbags.
- **Responsible:** TBD

## CUBE-PH5-D1-037
- **Group:** Accounting
- **Category:** Improvement
- **Epic:** Accounting Inquiries
- **Parent Task:** Approval Controls
- **Task Name:** Capture Lead Approval Reasons and Notes
- **User Story:** As an Accounts Payable Supervisor, I want lead approvals to include an approval reason and separate progress notes, so that AP can understand why a CSS or Fulfillment lead accepted the proposed resolution.
- **Description:** Lead approval currently functions primarily as a checkbox, while supporting explanations may be entered in another team's progress-notes field. The approval should capture the lead's decision context separately.
- **Acceptance Criteria:** 1. Lead approval includes an approval-reason field, 2. The approval reason is selected from a dropdown, 3. The approving lead can enter progress notes, 4. Lead notes are stored separately from the representative's progress notes, 5. Required approval information must be completed before the approval is submitted, 6. AP can review the approval reason and lead notes before closing the inquiry.
- **Timestamp:** Day 1, Part 2 [00:06:57 - 00:08:24]
- **Mockups:** NO MOCKUP
- **Notes:** This supplements CUBE-PH5-D1-036 by documenting why a lead accepted a resolution; it does not duplicate AP's ability to reject and return the resolution.
- **Responsible:** TBD

---

# Day 2

**Stories:** 49

## CUBE-PH5-D2-001
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Inquiry Resolution
- **Parent Task:** Final AP Resolution
- **Task Name:** Complete Accounting Inquiry Final Resolution
- **User Story:** As an Accounts Payable Supervisor, I want to record the final conclusion, final action, actual additional cost, and resolution summary for an accounting inquiry so that it can be closed with a complete record of the outcome.
- **Description:** After the required approvals are completed, AP reviews the inquiry findings, selects the issue conclusion and final action, records the actual additional cost, and documents the final resolution. If pricing must be corrected, AP can also request an update to the applicable product page. The inquiry is closed after the invoice is booked in Intacct.
- **Acceptance Criteria:** 1. AP can select a final conclusion of Vendor Error, ZTERS Error, Unpredictable Activity, Price Increase, or No Issue, 2. Vendor Error and ZTERS Error allow AP to identify the specific type of error, 3. AP can select the final action taken, including paying in full, paying as adjusted, or logging an adjustment in Intacct, 4. AP can record the actual additional cost resulting from the inquiry, 5. AP can enter progress notes, a resolution summary, and request a product-page update when needed, 6. The inquiry can be closed after the invoice has been booked in Intacct and the final resolution has been documented.
- **Timestamp:** Day 2, Part 1 [00:06:02 – 00:15:24]
- **Notes:** “Pay as adjusted” applies when the invoice has not yet been paid and the payable amount is changed. “Log an adjustment in Intacct” applies when payment has already occurred and a refund or adjustment must be tracked.
- **Responsible:** TBD

## CUBE-PH5-D2-002
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Inquiry Resolution
- **Parent Task:** Tax-Only Issues
- **Task Name:** Capture Tax-Only Invoice Details
- **User Story:** As an Accounts Payable Supervisor, I want to document tax-only invoice issues using the applicable service provider, product line, and location details so that unavoidable taxes can be reflected in the relevant pricing information.
- **Description:** When tax is the only invoice discrepancy and the service provider cannot remove it, AP records the tax percentage and description. The current Product Page URL field should be replaced or supplemented with structured product-line and location information to identify where the tax applies.
- **Acceptance Criteria:** 1. A tax-only issue can be documented when tax is the only invoice discrepancy, 2. AP can record the service provider’s tax percentage, 3. AP can enter a description of the applicable tax, 4. The tax information is associated with the applicable service provider, 5. AP can select the applicable product line or product lines and identify the county and state, 6. AP can confirm when the applicable tax information has been updated.
- **Timestamp:** Day 2, Part 1 [00:15:24 – 00:24:56]
- **Notes:** The Product Page URL was considered the least useful existing field. Tax charges may vary by service provider and may already be included in the provider’s rates, so taxes should not be applied automatically based only on ZIP code or location.
- **Responsible:** TBD

## CUBE-PH5-D2-003
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Inquiry Management
- **Parent Task:** Multiple Issues
- **Task Name:** Track Multiple Issues Within One Accounting Inquiry
- **User Story:** As a Fulfillment Representative, I want to identify and track multiple issues within a single accounting inquiry, each with its own details and resolution, so that no invoice discrepancy is overlooked.
- **Description:** A single invoice may contain several discrepancies, such as taxes, a price increase, or overages. The current inquiry records only one final resolution, which can cause individual issues to be skipped or prevent users from documenting how each issue was resolved. Cube should allow each issue to be categorized, described, and resolved separately within the same inquiry.
- **Acceptance Criteria:** 1. A user can add more than one issue to an accounting inquiry, 2. Each issue can be assigned its own issue category, 3. Each issue includes a separate notes field for its supporting details, 4. Each issue includes its own resolution information, 5. Users can navigate between the issues associated with the inquiry, 6. An accounting inquiry can contain up to five separately tracked issues.
- **Timestamp:** Day 2, Part 1 [00:26:00 – 00:33:08]
- **Notes:** Workshop participants indicated that most inquiries contain no more than three issues, but agreed that supporting up to five would be sufficient. The screenshot illustrates the current limitation because only one Issue Conclusion and one related error type can be selected.
- **Responsible:** TBD

## CUBE-PH5-D2-004
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Inquiry Management
- **Parent Task:** Inquiry Status
- **Task Name:** Maintain One Overall Status Across Multiple Issues
- **User Story:** As a Fulfillment Representative, I want a single overall inquiry status while its individual issues are resolved independently so that the workflow remains understandable without multiplying statuses.
- **Description:** The inquiry should be treated holistically even when it contains several issues. Individual issues may reach different resolutions, but the inquiry remains open until all of them are resolved.
- **Acceptance Criteria:** 1. The inquiry uses one overall status regardless of the number of issues, 2. The overall workflow supports Open, In Progress, Ready to Close, and Closed states, 3. Individual issues can be worked and resolved separately, 4. A partial payment or short payment can be recorded while another issue remains unresolved, 5. The inquiry cannot be closed while any included issue remains unresolved, 6. The final status reflects completion of all issues
- **Timestamp:** Day 2, Part 1 [00:33:08 – 00:35:56]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop explicitly rejected creating separate full status blocks for every issue.
- **Responsible:** TBD

## CUBE-PH5-D2-005
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Inquiry Management
- **Parent Task:** Related Invoices
- **Task Name:** Notify Users When an Invoice Is Added
- **User Story:** As a Fulfillment Representative, I want newly added invoices to be visibly identified and communicated to inquiry participants so that ongoing issues and additional billing cycles are not overlooked.
- **Description:** Additional invoices may be attached to an existing open inquiry when the same issue continues into another billing cycle. The addition needs to be prominent and visible to everyone working the inquiry.
- **Acceptance Criteria:** 1. A new invoice can be added to an existing open inquiry, 2. The inquiry visibly indicates that multiple invoices are involved, 3. The system identifies when a new attachment or invoice was recently added, 4. Users working on the inquiry receive notice of the added invoice, 5. The added invoice remains associated with the same ongoing issue, 6. All invoices associated with the inquiry remain visible until the problem is resolved
- **Timestamp:** Day 2, Part 1 [00:36:01 – 00:37:38]
- **Mockups:** NO MOCKUP
- **Notes:** The exact notification presentation was not finalized.
- **Responsible:** TBD

## CUBE-PH5-D2-006
- **Group:** Documents
- **Category:** Functional
- **Epic:** Document Management
- **Parent Task:** Related Documents
- **Task Name:** Store Accounting Inquiry Files in the Documents Table
- **User Story:** As a Fulfillment Representative, I want accounting-inquiry files stored in the Documents table so that I can attach and access all related documents without being limited to two attachment fields.
- **Description:** Fulfillment may receive additional files from vendors while working on an accounting inquiry. Cube should replace the two individual attachment fields with a Documents table that lists all files associated with the inquiry and makes them visible from related records.
- **Acceptance Criteria:** 1. The two individual attachment fields are replaced by the Documents table, 2. Users can add more than two documents to an accounting inquiry, 3. All documents associated with the inquiry are displayed in a list, 4. Each uploaded document is linked to the applicable accounting inquiry, 5. Documents are also available from related records such as the site, hauler, and fulfillment ticket, 6. Documents can be categorized as accounting-inquiry documents.
- **Timestamp:** Day 2, Part 1 [00:37:38 – 00:40:07]
- **Notes:** Fulfillment may receive follow-up files from vendors that need to be retained attached for reference. The workshop confirmed that Cube will use a system-wide Documents table instead of individual attachment fields.
- **Responsible:** TBD

## CUBE-PH5-D2-007
- **Group:** Accounting Dashboards
- **Category:** Functional
- **Epic:** Operational Reporting
- **Parent Task:** Inactive Inquiries
- **Task Name:** Display Inactive Accounting Inquiries
- **User Story:** As an Accounts Payable Supervisor, I want inactive accounting inquiries displayed by age and last activity so that I can follow up without receiving constant notifications.
- **Description:** The dashboard should surface inquiries that have not been touched and order the oldest needing action first. Last modification should reset the inactivity position when work is documented.
- **Acceptance Criteria:** 1. The dashboard identifies open inquiries with no recent activity, 2. Inactive inquiries are ordered from oldest to newest, 3. Inactivity is based on the last modified date, 4. Adding or modifying a note updates the last modified date, 5. Users can open an inactive inquiry from the dashboard, 6. Periodic follow-up notifications can summarize inactive inquiries instead of sending continuous alerts
- **Timestamp:** Day 2, Part 1 [00:41:06 – 00:44:07]
- **Mockups:** NO MOCKUP
- **Notes:** A possible weekly reminder was discussed, but the cadence was not finalized.
- **Responsible:** TBD

## CUBE-PH5-D2-008
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Hub Integration
- **Parent Task:** Inquiry Creation
- **Task Name:** Create and Link Inquiries From the HUB
- **User Story:** As an Accounts Payable Supervisor, I want to create an accounting inquiry from a HUB invoice or receipt and attach additional documents later so that HUB and Cube records remain connected.
- **Description:** The workshop identified mismatched inquiry counts between QuickBase and the HUB. Creating inquiries from HUB documents and linking multiple invoices or receipts to one inquiry would improve traceability.
- **Acceptance Criteria:** 1. A user can create an accounting inquiry from a HUB invoice, 2. A user can create an inquiry from a HUB payment receipt when applicable, 3. The originating HUB document remains linked to the Cube inquiry, 4. Multiple HUB invoices can be linked to one inquiry, 5. Another invoice can be added to the same inquiry after initial creation, 6. Manual inquiry creation remains available when no HUB document can be used
- **Timestamp:** Day 2, Part 1 [00:45:28 – 00:50:11]
- **Mockups:** NO MOCKUP
- **Notes:** The stated goal was to tie as many inquiries as possible to HUB documents, not to require 100 percent HUB creation.
- **Responsible:** TBD

## CUBE-PH5-D2-009
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Inquiry Resolution
- **Parent Task:** Paid Charges
- **Task Name:** Flag Already-Paid Credit Card Charges
- **User Story:** As an Accounts Payable Supervisor, I want to mark an inquiry as already paid so that users understand that any recovery requires a refund rather than an invoice adjustment before payment.
- **Description:** Credit-card charges have already occurred and must be booked for reconciliation. The inquiry needs a clear paid indicator and only resolution choices that apply to a paid charge.
- **Acceptance Criteria:** 1. A user can flag an inquiry as already paid, 2. The paid status is visible to every department working the inquiry, 3. The originating receipt or paid document remains linked to the inquiry, 4. Pay as adjusted and pay this invoice are not offered for an already-paid charge, 5. The resolution can document acceptance of the charge as is or the need for a refund adjustment, 6. The inquiry can close after the adjustment is logged while refund follow-up continues through the accounting adjustment process
- **Timestamp:** Day 2, Part 1 [00:47:40 – 00:52:28]
- **Mockups:** NO MOCKUP
- **Notes:** Refund follow-up may continue in Intacct after the accounting inquiry is closed.
- **Responsible:** TBD

## CUBE-PH5-D2-010
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Priority Management
- **Parent Task:** High Priority
- **Task Name:** Identify High-Priority Accounting Inquiries
- **User Story:** As a Fulfillment Representative, I want high-priority accounting inquiries automatically and manually identified so that urgent or high-impact issues receive appropriate visibility.
- **Description:** High priority remains useful for issues involving age, dollar value, or urgent operational impact. The current dollar trigger did not work during the demonstration and thresholds may vary by product or CWS status.
- **Acceptance Criteria:** 1. A user can manually mark an inquiry as high priority, 2. The system can mark an inquiry high priority based on configured rules, 3. Priority rules can consider invoice age, dollar amount, and operational urgency, 4. Product type and CWS status can be considered when defining thresholds, 5. High-priority inquiries are visibly highlighted in reports and dashboards, 6. High-priority inquiries can trigger dedicated notifications
- **Timestamp:** Day 2, Part 1 [00:54:16 – 00:57:36]
- **Mockups:** NO MOCKUP
- **Notes:** Exact priority thresholds were explicitly left for later definition.
- **Responsible:** TBD

## CUBE-PH5-D2-011
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Approval Workflow
- **Parent Task:** AP Lead Approval
- **Task Name:** Reevaluate AP Lead Approval From Actual Cost
- **User Story:** As an Accounts Payable Supervisor, I want AP lead approval to reflect the actual additional cost and final action so that inquiries do not remain in an approval status after the customer is billed or the cost is reduced.
- **Description:** The current process may continue requiring AP lead approval because the expected additional cost remains populated even when the actual additional cost becomes zero. The approval logic needs to use the completed resolution information.
- **Acceptance Criteria:** 1. Expected additional cost remains available when the inquiry is created, 2. Actual additional cost can be entered during final resolution, 3. The final action is considered when determining whether AP lead approval is required, 4. An actual additional cost of zero is recognized after the customer is billed or the issue is resolved, 5. The status is reevaluated when the actual additional cost changes, 6. The $500 approval condition is applied to the applicable final cost rather than an unresolved blank value
- **Timestamp:** Day 2, Part 1 [00:57:39 – 00:59:41]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop described $500 as the current AP lead approval threshold.
- **Responsible:** TBD

## CUBE-PH5-D2-012
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Access Control
- **Parent Task:** Section Permissions
- **Task Name:** Restrict Inquiry Sections by Team
- **User Story:** As a Fulfillment Representative, I want each team to edit only its assigned inquiry section so that AP, Sales, and Fulfillment conclusions are not overwritten by unrelated users.
- **Description:** Cube permissions will restrict the editable portions of an accounting inquiry by team while leaving shared areas, such as documents, available where appropriate.
- **Acceptance Criteria:** 1. Account Managers can edit the Account Manager section, 2. Fulfillment users can edit the Fulfillment section, 3. AP users can edit the AP final-resolution section, 4. Users cannot edit another team's restricted resolution fields, 5. Shared areas such as documents remain available to applicable participants, 6. Permissions apply according to the user's assigned role or group
- **Timestamp:** Day 2, Part 1 [00:59:41 – 01:01:03]
- **Mockups:** NO MOCKUP
- **Notes:** The rules for manually triggering AM and Fulfillment action were still under discussion.
- **Responsible:** TBD

## CUBE-PH5-D2-013
- **Group:** Accounting Dashboards
- **Category:** Functional
- **Epic:** Operational Reporting
- **Parent Task:** Ready to Close
- **Task Name:** Show Inquiries Ready to Close
- **User Story:** As an Accounts Payable Supervisor, I want a Ready to Close dashboard bucket so that inquiries with all required approvals can be finalized promptly.
- **Description:** AP users need a consolidated view of inquiries that have obtained the required CSS and Fulfillment approvals and are ready for AP closure.
- **Acceptance Criteria:** 1. The dashboard includes a Ready to Close bucket, 2. An inquiry enters the bucket after its required approvals are complete, 3. Inquiries requiring one approval can enter after that approval is complete, 4. Inquiries requiring both approvals enter only after both are complete, 5. A user can open the inquiry from the Ready to Close bucket, 6. The bucket is distinct from New, In Progress, inactive, and Closed inquiries
- **Timestamp:** Day 2, Part 1 [01:01:35 – 01:03:37]
- **Mockups:** NO MOCKUP
- **Notes:** Ready to Close was identified as an important main status.
- **Responsible:** TBD

## CUBE-PH5-D2-014
- **Group:** Accounting Dashboards
- **Category:** Functional
- **Epic:** Operational Reporting
- **Parent Task:** Inquiry Aging
- **Task Name:** Compare Inquiry and Invoice Aging
- **User Story:** As a Fulfillment Director, I want accounting-inquiry aging shown by both inquiry creation date and invoice date so that I can distinguish workflow delay from the age of the underlying bill.
- **Description:** The current dashboard ages inquiries by creation date only. The workshop requested separate views or graphs for inquiry age and invoice age.
- **Acceptance Criteria:** 1. The dashboard calculates age from the inquiry creation date, 2. The dashboard separately calculates age from the invoice date, 3. Users can distinguish the two aging measures, 4. Aging can be displayed in defined buckets, 5. Open inquiries remain included until closed, 6. Users can access the underlying inquiry records from the aging view
- **Timestamp:** Day 2, Part 1 [01:04:27 – 01:05:19]
- **Mockups:** NO MOCKUP
- **Notes:** The exact aging buckets were not finalized in this discussion.
- **Responsible:** TBD

## CUBE-PH5-D2-015
- **Group:** Accounting Dashboards
- **Category:** Functional
- **Epic:** Operational Reporting
- **Parent Task:** Provider Analysis
- **Task Name:** View Open Inquiries by Service Provider
- **User Story:** As a Fulfillment Representative, I want open accounting inquiries grouped by service provider so that I can identify providers with multiple unresolved billing issues.
- **Description:** Open inquiries by service provider were considered useful for day-to-day work, unlike historical conclusion reports that do not focus on active issues.
- **Acceptance Criteria:** 1. The report includes only open accounting inquiries, 2. Inquiries are grouped by service provider, 3. The number of open inquiries for each provider is visible, 4. A user can access the provider's underlying open inquiries, 5. The report supports identifying providers with multiple active issues, 6. Closed issue conclusions are not substituted for the requested open-inquiry view
- **Timestamp:** Day 2, Part 1 [01:05:43 – 01:06:41]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript used the term hauler for the service provider.
- **Responsible:** TBD

## CUBE-PH5-D2-016
- **Group:** Accounting Dashboards
- **Category:** Functional
- **Epic:** Role-Based Reporting
- **Parent Task:** Inquiry Filters
- **Task Name:** Filter Inquiry Dashboards by Division and Responsible Party
- **User Story:** As a Fulfillment Director, I want role-based inquiry dashboards with CWS, team, user, and responsible-party filters so that I can review the work relevant to each group and employee.
- **Description:** Accounting inquiries involve several departments. Dashboard users need views for their own work, their team's work, CWS versus non-CWS work, and inquiries involving Sales, Fulfillment, or both.
- **Acceptance Criteria:** 1. Users can distinguish CWS from non-CWS inquiries, 2. Inquiries can be grouped by responsible department, 3. The view can identify Sales involvement, Fulfillment involvement, or both, 4. Individual users can see inquiries relevant to their own role, 5. Team leads can filter by individual employee, 6. Team leads can view the combined work of their group
- **Timestamp:** Day 2, Part 1 [01:07:40 – 01:10:45]
- **Mockups:** NO MOCKUP
- **Notes:** Role-based dashboard layouts may differ between operational users and leaders.
- **Responsible:** TBD

## CUBE-PH5-D2-017
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** Service Provider Management
- **Parent Task:** Pricing Access
- **Task Name:** Access PSP Pricing From the Service Provider Record
- **User Story:** As a Fulfillment Representative, I want PSP pricing and pricing zones available from the service-provider record so that I do not need to locate them in a separate application.
- **Description:** PSP pricing will be integrated into Cube and accessible alongside the provider's other information.
- **Acceptance Criteria:** 1. PSP pricing is available within the main Cube application, 2. A user can open pricing from the applicable service-provider record, 3. Pricing zones are visible with the provider's pricing, 4. Pricing access does not require opening the separate PSP Pricing application, 5. Pricing appears alongside related provider information such as notes and contacts, 6. The pricing shown belongs to the selected service provider
- **Timestamp:** Day 2, Part 1 [01:10:45 – 01:11:28]
- **Mockups:** NO MOCKUP
- **Notes:** This was described as planned Cube functionality.
- **Responsible:** TBD

## CUBE-PH5-D2-018
- **Group:** Accounting Dashboards
- **Category:** Functional
- **Epic:** Strategic Reporting
- **Parent Task:** Inquiry Performance
- **Task Name:** Provide Strategic Accounting Inquiry Metrics
- **User Story:** As an Accounts Payable Supervisor, I want strategic accounting-inquiry metrics so that inquiry volume, cost, and resolution performance can be reviewed over time.
- **Description:** In addition to tactical queues, the workshop identified a need for summary reporting that can be shared on a monthly or quarterly cadence.
- **Acceptance Criteria:** 1. The dashboard can show inquiries by service provider, 2. The dashboard can show actual cost year to date by service provider, 3. The dashboard can show how many inquiries are resolved each month, 4. Average inquiry age can be summarized overall, 5. Average age can be broken down by team or person, 6. Metrics can be grouped by problem type where that information is available
- **Timestamp:** Day 2, Part 1 [01:11:44 – 01:13:53]
- **Mockups:** NO MOCKUP
- **Notes:** The final set of strategic metrics and reporting cadence requires additional definition.
- **Responsible:** TBD

## CUBE-PH5-D2-019
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** Service Provider Management
- **Parent Task:** AP Data Quality
- **Task Name:** Report Missing Service-Provider AP Information
- **User Story:** As a Fulfillment Director, I want summary visibility into incomplete service-provider accounting information so that missing AP data can be identified and completed.
- **Description:** The provider AP tab contains operational payment information, and the HUB already exposes blank values while documents are processed. A summary view was requested to identify where these fields remain blank.
- **Acceptance Criteria:** 1. The report evaluates accounting fields on service-provider records, 2. Providers with blank accounting information are identified, 3. The summary distinguishes completed information from missing information, 4. A user can access the affected provider record, 5. A user can navigate to the AP tab to complete the information, 6. The report supports review across more than one service provider
- **Timestamp:** Day 2, Part 1 [01:29:48 – 01:30:40]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript did not define the complete list of required AP fields.
- **Responsible:** TBD

## CUBE-PH5-D2-020
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** PSP Workflow
- **Parent Task:** Accounting Approval
- **Task Name:** Require Accounting Approval for PSP Promotion
- **User Story:** As a Fulfillment Representative, I want Accounting included in the PSP promotion workflow so that its recommendation and approval are formally recorded instead of being handled only through Teams messages.
- **Description:** Before a service provider is promoted to PSP, Accounting needs a systematic opportunity to review the provider, provide feedback, and approve or reject the promotion.
- **Acceptance Criteria:** 1. PSP promotion includes an Accounting approval step, 2. The designated Accounting group receives a notification when approval is needed, 3. Accounting can review the provider's qualification information, 4. Accounting can record a recommendation or justification, 5. Accounting can approve or reject the promotion, 6. The approval action and user are retained in the workflow history
- **Timestamp:** Day 2, Part 1 [01:30:13 – 01:40:38]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop stated that the interdepartmental workflow concept had prior support, but detailed routing still belongs to the PSP promotion process.
- **Responsible:** TBD

## CUBE-PH5-D2-021
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** Pricing Calculations
- **Parent Task:** Credit Card Fees
- **Task Name:** Include Provider Credit Card Fees in Cost and Margin
- **User Story:** As a Fulfillment Quality Coordinator, I want a provider's credit-card fee automatically included in cost calculations when Visa is the preferred payment method so that expected margin and item receipts reflect the known fee.
- **Description:** The AP tab records preferred payment method, whether the provider charges a credit-card fee, and the percentage. The percentage is displayed today but is not included in calculations.
- **Acceptance Criteria:** 1. The provider record stores the preferred payment method, 2. Visa payment methods are recognized regardless of the specific Visa method, 3. The provider record stores whether a credit-card fee applies, 4. The credit-card fee percentage is used when Visa is the default tender, 5. The fee is included in expected provider cost and margin calculations, 6. The fee is included in the item-receipt total
- **Timestamp:** Day 2, Part 1 [01:34:43 – 01:38:59]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop preferred including a known fee even if a provider occasionally builds it into another charge.
- **Responsible:** TBD

## CUBE-PH5-D2-022
- **Group:** Service Providers
- **Category:** Functional
- **Epic:** Service Provider Management
- **Parent Task:** Billing Risk
- **Task Name:** Flag Risky Provider Billing Practices
- **User Story:** As a Fulfillment Representative, I want risky billing practices visibly flagged on service-provider records so that I can consider billing risk when selecting a provider.
- **Description:** Certain combinations of billing cycle, specific billing date, and no first- or last-month proration can cause ZTERS to be billed for two months across a very short rental period.
- **Acceptance Criteria:** 1. The system evaluates the provider's recorded billing cycle, 2. The system evaluates whether the provider bills on a specific day each month, 3. The system evaluates first-month and last-month proration practices, 4. A risky combination produces a visible billing-risk indicator, 5. The indicator is visible near the provider's other important statuses, 6. Billing practices can contribute to the provider health score
- **Timestamp:** Day 2, Part 1 [01:40:57 – 01:47:45]
- **Mockups:** NO MOCKUP
- **Notes:** The exact combinations and final status label require later definition.
- **Responsible:** TBD

## CUBE-PH5-D2-023
- **Group:** Billing Review
- **Category:** Functional
- **Epic:** Invoice Research
- **Parent Task:** Line Items
- **Task Name:** Show Service Dates in Site Line-Item Views
- **User Story:** As a Fulfillment Quality Coordinator, I want service dates visible in site line-item views so that I can match vendor charges to the correct customer billing without opening every product or ticket.
- **Description:** AP users research whether charges such as dry runs, relocations, tonnage, or miscellaneous fees were billed. Site-level line items are useful, but some entries require opening the record to see the relevant date.
- **Acceptance Criteria:** 1. Users can view line items from the site record, 2. Line items identify the type or description of the billed item, 3. The applicable service date is visible in the line-item view, 4. Users can filter the line-item list to locate a specific charge, 5. Users can still open a product or service ticket for detailed review, 6. Site-level and product-level research paths remain available
- **Timestamp:** Day 2, Part 1 [01:48:50 – 01:54:59]
- **Mockups:** NO MOCKUP
- **Notes:** The participants confirmed that both site-wide and product-specific views are used.
- **Responsible:** TBD

## CUBE-PH5-D2-024
- **Group:** Fencing
- **Category:** Functional
- **Epic:** Fencing Billing
- **Parent Task:** Secondary Rental
- **Task Name:** Display and Validate Fencing Secondary Rental Rates
- **User Story:** As an Accounts Payable Supervisor, I want fencing secondary rental rates displayed and used in recurring calculations so that I can verify billing and detect recurring low-margin services.
- **Description:** The fencing secondary rental ticket shows the rental length but not the vendor's secondary rental rate. The expected-charge display also uses primary information and does not flag recurring negative margin.
- **Acceptance Criteria:** 1. A fencing secondary rental ticket displays the customer secondary rental rate, 2. The ticket displays the provider secondary rental rate, 3. Expected customer charges use the secondary rental rate, 4. Expected provider cost uses the secondary rental rate, 5. Recurring margin is calculated from the secondary customer and provider rates, 6. Low or negative margin on secondary recurring rental is visibly identified
- **Timestamp:** Day 2, Part 1 [01:55:08 – 02:01:03]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop also noted a future desire for item receipts on recurring fencing charges.
- **Responsible:** TBD

## CUBE-PH5-D2-025
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Ticket Review
- **Parent Task:** Sort and Notes
- **Task Name:** Sort Fulfillment Tickets and Improve Note Review
- **User Story:** As an Accounts Payable Supervisor, I want to sort fulfillment tickets in either chronological direction and review their notes efficiently so that I can research an accounting inquiry from oldest activity to newest.
- **Description:** Fulfillment typically benefits from newest-first sorting, while Accounting research often requires oldest-first review. Long note columns and embedded timestamps make the current process difficult.
- **Acceptance Criteria:** 1. The ticket list can be sorted oldest to newest, 2. The ticket list can be sorted newest to oldest, 3. A user can reverse the sort with a simple control, 4. Ticket notes are displayed in a readable format rather than a very narrow column, 5. A user can move between ticket notes without repeated scrolling and extra clicks, 6. Imported QuickBase notes and newly created Cube notes remain reviewable
- **Timestamp:** Day 2, Part 1 [02:02:18 – 02:07:18]
- **Mockups:** NO MOCKUP
- **Notes:** The exact method for sorting timestamps inside legacy note text was not promised.
- **Responsible:** TBD

## CUBE-PH5-D2-026
- **Group:** Accounting Inquiries
- **Category:** Functional
- **Epic:** Hub Integration
- **Parent Task:** Status Synchronization
- **Task Name:** Send Inquiry Status Information From Cube to the HUB
- **User Story:** As an Accounts Payable Supervisor, I want Cube accounting-inquiry statuses available in the HUB so that invoice-centered AP dashboards can include the inquiry's current and final state.
- **Description:** Accounting inquiries will live in Cube, while AP dashboards are primarily being built in the HUB. The inquiry data therefore needs to bridge the two systems.
- **Acceptance Criteria:** 1. Accounting inquiries remain managed in Cube, 2. The HUB can identify invoices that have related inquiries, 3. Current inquiry status is available to HUB reporting, 4. Final inquiry status is available to HUB reporting, 5. HUB reporting can distinguish documents with open inquiries, 6. The integration supports AP reporting without duplicating the full inquiry workflow in the HUB
- **Timestamp:** Day 2, Part 1 [02:23:44 – 02:27:32]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop expected some reporting on both sides, with slightly different purposes.
- **Responsible:** TBD

## CUBE-PH5-D2-027
- **Group:** Credit Card Transactions
- **Category:** Functional
- **Epic:** Transaction Management
- **Parent Task:** Transaction Data
- **Task Name:** Standardize Credit Card Transaction Data
- **User Story:** As an Accounts Payable Supervisor, I want credit-card transactions to capture consistent details across every payment path so that payments, declines, and overpayments can be reconciled reliably.
- **Description:** Credit-card transactions currently capture different fields depending on whether payment is made up front, across multiple invoices, internally after check-by-mail, or through the customer portal.
- **Acceptance Criteria:** 1. Credit-card-up-front transactions capture the defined transaction fields, 2. Internally processed transactions capture the same defined fields, 3. Portal payments across multiple invoices capture the same defined fields, 4. Authorized.net identifiers and available batch information are retained consistently, 5. Rejected transactions remain identified as declined, 6. A separate collected-amount value shows zero for a declined transaction even when the attempted amount is displayed
- **Timestamp:** Day 2, Part 1 [02:32:57 – 02:37:26]
- **Mockups:** NO MOCKUP
- **Notes:** A separate detailed spreadsheet of required transaction fields was promised during the workshop but was not included in this transcript.
- **Responsible:** TBD

## CUBE-PH5-D2-028
- **Group:** Credits
- **Category:** Functional
- **Epic:** Credit Management
- **Parent Task:** Credit Status
- **Task Name:** Treat Credits as Negative Invoices
- **User Story:** As an Accounts Payable Supervisor, I want credits treated as negative invoices with their own usage status so that available and applied credits appear correctly in invoice and collections reporting.
- **Description:** Credits relate to an originating invoice but remain separate records. They need the same core information as invoices and a status showing whether the credit is available or used.
- **Acceptance Criteria:** 1. A credit references its originating invoice, 2. The credit exists as its own record, 3. The credit carries the same available customer and address information as an invoice, 4. The credit open balance is represented as a negative amount, 5. An unused credit is shown as available or unpaid, 6. A used credit is shown as applied or paid
- **Timestamp:** Day 2, Part 1 [02:37:26 – 02:44:17]
- **Mockups:** NO MOCKUP
- **Notes:** Credits created directly in Intacct without a Cube invoice remain outside this initial scope.
- **Responsible:** TBD

## CUBE-PH5-D2-029
- **Group:** Credits
- **Category:** Functional
- **Epic:** Credit Management
- **Parent Task:** Credit Approval
- **Task Name:** Approve Credits for Older Invoices
- **User Story:** As a Fulfillment Representative, I want older credits processed through an approval workflow so that valid credits are not blocked solely because the original invoice is old.
- **Description:** The current restriction prevents some older credits from being created in QuickBase, which causes manual Intacct entry and reporting discrepancies. The workshop preferred approval before the credit is promised to the customer.
- **Acceptance Criteria:** 1. A credit can be initiated for an older existing invoice, 2. The credit remains linked to the original invoice, 3. The request enters an approval workflow instead of being automatically blocked, 4. The designated approver can review the request, 5. Approval occurs before the credit is promised to the customer, 6. Approved credits retain the information needed for normal Cube processing
- **Timestamp:** Day 2, Part 1 [02:45:17 – 02:47:36]
- **Mockups:** NO MOCKUP
- **Notes:** The age threshold and detailed approval routing were not defined.
- **Responsible:** TBD

## CUBE-PH5-D2-030
- **Group:** Collections
- **Category:** Functional
- **Epic:** Collections Reporting
- **Parent Task:** Credits and Balances
- **Task Name:** Show Invoice and Credit Balances Separately and Net
- **User Story:** As a Fulfillment Representative, I want customer collections views to show open invoices, open credits, and the net balance so that offsetting amounts do not hide unresolved invoices or unused credits.
- **Description:** A customer's net balance can appear to be zero even when the customer owes invoices and ZTERS owes unused credits. Both the combined and separated values are needed.
- **Acceptance Criteria:** 1. The collections view includes open invoices, 2. The collections view includes open credits, 3. Used and unused credits can be distinguished, 4. The total open-invoice amount is shown, 5. The total open-credit amount is shown separately, 6. A net balance is calculated from the invoice and credit amounts
- **Timestamp:** Day 2, Part 1 [02:49:56 – 02:57:51]
- **Mockups:** NO MOCKUP
- **Notes:** Overpayments and Intacct-only credits may still create differences from the Intacct balance.
- **Responsible:** TBD

## CUBE-PH5-D2-031
- **Group:** Collections
- **Category:** Functional
- **Epic:** Collections Reporting
- **Parent Task:** Payment Terms
- **Task Name:** Base Collection Warnings on Approved Net Terms
- **User Story:** As a Fulfillment Director, I want past-due and approaching-limit warnings based on each customer's approved payment terms so that agreed Net 60 or Net 90 accounts are not repeatedly flagged as though they were Net 30.
- **Description:** Collection warnings currently include static logic that may flag accounts before their approved terms have elapsed. The warning should respond to the payment terms recorded for the customer.
- **Acceptance Criteria:** 1. The system reads the customer's approved net terms, 2. Invoice age is compared with the approved terms, 3. Past-due status begins after the applicable terms are exceeded, 4. Approaching-past-due status uses a defined threshold before the due point, 5. The warning distinguishes approaching from already past due, 6. The configured terms are used instead of applying Net 30 to every customer
- **Timestamp:** Day 2, Part 1 [02:53:14 – 02:55:59]
- **Mockups:** NO MOCKUP
- **Notes:** The exact approaching threshold was not finalized; ten days before Net 60 was discussed only as an example.
- **Responsible:** TBD

## CUBE-PH5-D2-032
- **Group:** Collections
- **Category:** Functional
- **Epic:** Strategic Reporting
- **Parent Task:** Customer Payment Behavior
- **Task Name:** Display Customer Payment Behavior Metrics
- **User Story:** As an Accounts Payable Supervisor, I want customer payment behavior metrics visible in Cube so that collections risk can be assessed beyond the current open balance.
- **Description:** The workshop identified DSO, payment frequency, recent payment dates, and typical payment amounts as useful indicators that are currently summarized outside Cube.
- **Acceptance Criteria:** 1. The dashboard can display days sales outstanding when the required data is available, 2. The dashboard can display how frequently the customer pays, 3. Recent payment dates can be shown, 4. Average payment amounts can be shown, 5. Payment behavior is available alongside open-balance information, 6. The metrics can support customer health or quality analysis
- **Timestamp:** Day 2, Part 1 [02:58:23 – 03:00:50]
- **Mockups:** NO MOCKUP
- **Notes:** Some metrics depend on additional Intacct integration and may not be available in the first phase.
- **Responsible:** TBD

## CUBE-PH5-D2-033
- **Group:** Collections
- **Category:** Functional
- **Epic:** Collections Reporting
- **Parent Task:** AR Aging
- **Task Name:** Provide a Consolidated AR Aging Report
- **User Story:** As a Fulfillment Director, I want a consolidated AR aging report in Cube so that all customers with open balances can be reviewed without exporting and combining incomplete reports.
- **Description:** The Power BI report is valued primarily for its presentation and sorting. The Cube report needs all open balances, including check-by-mail customers, with credits, credit limits, ownership, and aging details.
- **Acceptance Criteria:** 1. The report includes all customers with an open balance, 2. Credit-card and check-by-mail customers are included, 3. Invoice balances and credit values are included in the reported total, 4. Balances are separated into aging buckets, 5. Credit limit, record owner, and CSS information are available, 6. Users can filter and sort the report by the available customer and aging fields
- **Timestamp:** Day 2, Part 1 [03:01:03 – 03:18:07]
- **Mockups:** NO MOCKUP
- **Notes:** The requested report is broader than the existing credit-card-decline report.
- **Responsible:** TBD

## CUBE-PH5-D2-034
- **Group:** Collections
- **Category:** Functional
- **Epic:** Credit Management
- **Parent Task:** Credit Utilization
- **Task Name:** Track Current and Historical Credit Utilization
- **User Story:** As a Fulfillment Representative, I want current and historical credit utilization displayed so that increases or decreases to a customer's line of credit can be evaluated using more than a single-day balance.
- **Description:** Current utilization can be calculated from the open balance and approved credit limit. Historical analysis requires periodic snapshots because that data does not exist today.
- **Acceptance Criteria:** 1. Current credit utilization is calculated from the current balance and credit limit, 2. The current utilization percentage is visible in reporting, 3. Utilization snapshots can be retained over time, 4. Historical snapshots can be captured weekly or every other week, 5. The historical view can cover a two-to-three-month period, 6. The information supports review of potential credit-limit increases or decreases
- **Timestamp:** Day 2, Part 1 [03:18:26 – 03:22:35]
- **Mockups:** NO MOCKUP
- **Notes:** Weekly or every-other-week snapshots over two to three months were discussed; the final calculation still needs definition.
- **Responsible:** TBD

## CUBE-PH5-D2-035
- **Group:** Credit Card Declines
- **Category:** Functional
- **Epic:** Decline Management
- **Parent Task:** Decline Reporting
- **Task Name:** Add Operational Detail to Credit Card Decline Reports
- **User Story:** As a Fulfillment Representative, I want credit-card decline reports to show the service type, recurrence context, and relevant dates so that I can prioritize the correct operational response.
- **Description:** The existing report primarily separates recurring and non-recurring declines. The non-recurring group can contain deliveries, hauls, swaps, tonnage, rentals, storage containers, and other charges with different urgency.
- **Acceptance Criteria:** 1. Declines can be separated into recurring and non-recurring groups, 2. The report identifies the applicable product line, 3. The report identifies the service or charge type, 4. Delivery date is visible when applicable, 5. Removal date is visible when applicable, 6. Users can sort and filter declines using the added operational details
- **Timestamp:** Day 2, Part 1 [03:24:59 – 03:32:18]
- **Mockups:** NO MOCKUP
- **Notes:** Recurring in the current report specifically represents the automated overnight recurring toilet process; other recurring products may appear as non-recurring.
- **Responsible:** TBD

## CUBE-PH5-D2-036
- **Group:** Credit Card Declines
- **Category:** Functional
- **Epic:** Decline Management
- **Parent Task:** Critical Declines
- **Task Name:** Escalate Declines for Imminent Deliveries
- **User Story:** As a Fulfillment Representative, I want declines tied to imminent deliveries marked as critical and immediately communicated so that unpaid service is not delivered without an approved line of credit.
- **Description:** A non-recurring card decline for a delivery scheduled today or soon requires faster action than a charge for tonnage or a delivery scheduled weeks later.
- **Acceptance Criteria:** 1. The system evaluates whether the declined transaction is tied to a delivery, 2. The applicable delivery date is used to determine urgency, 3. Declines for imminent deliveries are marked critical, 4. The responsible sales or CSS user receives an immediate notification, 5. The critical status remains visible until payment or another valid resolution is recorded, 6. The workflow can prevent unpaid delivery from continuing according to the defined operational rule
- **Timestamp:** Day 2, Part 1 [03:27:40 – 03:31:08]
- **Mockups:** NO MOCKUP
- **Notes:** The exact time threshold and automatic cancellation behavior were not finalized.
- **Responsible:** TBD

## CUBE-PH5-D2-037
- **Group:** Credit Card Declines
- **Category:** Functional
- **Epic:** Decline Management
- **Parent Task:** Responsibility and Escalation
- **Task Name:** Route Declines by Responsibility and Escalation
- **User Story:** As a Fulfillment Representative, I want declines routed by responsibility with a manual AR escalation option so that newly declined transactions remain with Sales until collection assistance is actually needed.
- **Description:** The current AR report includes every decline immediately. The workshop requested responsibility thresholds, documented attempts, and a way for Sales to escalate a difficult collection to AR.
- **Acceptance Criteria:** 1. A newly declined transaction remains assigned to the responsible sales process, 2. The report can apply configured time or effort thresholds before routing the decline to AR, 3. Collection attempts can be documented as tasks, 4. Sales can manually escalate a decline to AR when assistance is needed, 5. The escalated state is visible to AR, 6. The record retains the history of work performed before and after escalation
- **Timestamp:** Day 2, Part 1 [03:32:18 – 03:37:16]
- **Mockups:** NO MOCKUP
- **Notes:** The number of days, attempts, calls, or tasks required before escalation was not defined.
- **Responsible:** TBD

## CUBE-PH5-D2-038
- **Group:** Credit Card Declines
- **Category:** Functional
- **Epic:** Decline Management
- **Parent Task:** Automated Retry and Aging
- **Task Name:** Show Declines After Retry and Highlight Three-to-Four-Week Cases
- **User Story:** As a Fulfillment Representative, I want recurring declines shown after the automated retry and highlighted at three to four weeks so that collection effort is focused when manual action is appropriate and removal is needed before another billing cycle.
- **Description:** Recurring cards are retried automatically after the first overnight decline. A separate report identifies declines between three and four weeks old because they need resolution or removal before the next monthly charge.
- **Acceptance Criteria:** 1. The automated recurring-card retry remains part of the process, 2. A first decline awaiting the scheduled retry can be excluded from the manual-work report, 3. The decline appears for manual work after the second failed attempt, 4. Declines between three and four weeks old are identified, 5. The three-to-four-week group is available as a dashboard count or report, 6. Users can open the affected decline to coordinate collection or removal
- **Timestamp:** Day 2, Part 1 [03:38:41 – 03:41:48]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript referred to this aging window as the recurring credit-card-decline sweet spot.
- **Responsible:** TBD

## CUBE-PH5-D2-039
- **Group:** Collections
- **Category:** Functional
- **Epic:** Collection Activities
- **Parent Task:** Collection Tasks
- **Task Name:** Record Collection Efforts as Tasks
- **User Story:** As a Fulfillment Representative, I want calls, emails, card attempts, and skip-tracing work recorded as collection tasks so that effort, timing, and outcomes can be measured without reading a long notes field.
- **Description:** The current process relies on timestamped collection notes. Tasks can capture the activity type, duration, next action, and relationships to the customer, site, product, or invoice.
- **Acceptance Criteria:** 1. Users can create a task with an AR or collections category, 2. The task can identify whether the activity was a call, email, card attempt, or skip trace, 3. Start time, end time, and time spent can be recorded, 4. A next follow-up task or date can be scheduled, 5. The task can be linked to the applicable customer, site, product, and invoice, 6. Collection activity can be reported by user, customer, product line, and time spent
- **Timestamp:** Day 2, Part 1 [03:42:25 – 03:49:22]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop proposed tasks as a replacement for future collection notes, while existing notes still need to remain reviewable.
- **Responsible:** TBD

## CUBE-PH5-D2-040
- **Group:** Invoices
- **Category:** Functional
- **Epic:** Invoice Management
- **Parent Task:** Invoice Visibility
- **Task Name:** Display Invoice Aging and Transaction User
- **User Story:** As an Accounts Payable Supervisor, I want invoice age and the user who ran each card transaction clearly displayed so that I can prioritize old balances and understand who has already attempted collection.
- **Description:** Invoice age exists in the Intacct Aging area but should be more prominent. Credit-card transaction records currently do not clearly identify the user who ran the transaction.
- **Acceptance Criteria:** 1. The invoice record displays its current age prominently, 2. Aging is based on the available invoice and Intacct aging information, 3. Aging can be presented in defined visual buckets, 4. Related credit-card transactions remain accessible from the invoice, 5. Each transaction identifies the user who ran it when that HUB user data is available, 6. The transaction user is distinct from the user who originally created the record
- **Timestamp:** Day 2, Part 1 [03:51:12 – 03:58:02]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop mentioned possible 30-day and 60-day visual buckets without finalizing the complete bucket scheme.
- **Responsible:** TBD

## CUBE-PH5-D2-041
- **Group:** Chargebacks
- **Category:** Functional
- **Epic:** Chargeback Management
- **Parent Task:** Chargeback Creation
- **Task Name:** Create Chargeback From an Invoice
- **User Story:** As an Accounts Payable Supervisor, I want to create a chargeback directly from an invoice so that existing invoice and customer information does not have to be entered again.
- **Description:** Chargebacks are currently created through a separate form with manually entered customer, invoice, account manager, credit-card, and product information. Cube should initiate the chargeback from the affected invoice and automatically establish these relationships.
- **Acceptance Criteria:** 1. A user can initiate a chargeback from an invoice, 2. The chargeback is automatically linked to the selected invoice, 3. The related customer is populated from the invoice, 4. The responsible account manager is populated from the customer record, 5. Available credit-card and transaction details are populated from the invoice, 6. Each separately received invoice chargeback can be tracked as its own chargeback record
- **Timestamp:** Day 2, Part 2 [00:00:04 – 00:03:45]
- **Mockups:** NO MOCKUP
- **Notes:** A chargeback may apply to only one invoice even when several chargebacks are received together.
- **Responsible:** TBD

## CUBE-PH5-D2-042
- **Group:** Chargebacks
- **Category:** Functional
- **Epic:** Chargeback Management
- **Parent Task:** Chargeback Details
- **Task Name:** Capture Structured Chargeback Details
- **User Story:** As a Fulfillment Representative, I want to capture the disputed amount, case information, product lines, and service type so that each chargeback accurately represents what the customer disputed.
- **Description:** Some chargebacks cover only part of an invoice. The record also needs to distinguish the chargeback provider, applicable product lines, service type, and reasons not included in the standard selections.
- **Acceptance Criteria:** 1. The disputed amount can be entered independently from the full invoice amount, 2. The chargeback provider can be selected, 3. One case identifier field is used for the selected provider, 4. One or more applicable product lines can be selected, 5. Service type options include new rental, tonnage, dry run, recurring, damage or replacement, and miscellaneous, 6. Selecting Other or Miscellaneous allows the user to enter additional details
- **Timestamp:** Day 2, Part 2 [00:03:45 – 00:08:48]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript identified Heartland and Amex as the current chargeback providers.
- **Responsible:** TBD

## CUBE-PH5-D2-043
- **Group:** Chargebacks
- **Category:** Functional
- **Epic:** Chargeback Management
- **Parent Task:** Chargeback Workflow
- **Task Name:** Manage Chargeback Status and Bank Response
- **User Story:** As a Fulfillment Representative, I want chargebacks managed through a clear status and response workflow so that open disputes remain visible and bank deadlines are documented.
- **Description:** The current Open status and Chargeback Being Processed checkbox communicate the same condition. The chargeback also requires dates for when the request was received, when a response is due, and when the response was submitted.
- **Acceptance Criteria:** 1. A newly received chargeback can be placed in Open status, 2. An open chargeback is visibly identified on the related customer record, 3. The duplicate Chargeback Being Processed checkbox is not required in addition to Open status, 4. The request-received and respond-by dates are recorded, 5. The date responded to the bank is recorded separately, 6. The chargeback can be closed after the final response and resolution are completed
- **Timestamp:** Day 2, Part 2 [00:08:54 – 00:10:35]
- **Mockups:** NO MOCKUP
- **Notes:** When a chargeback begins, the money leaves the bank account and is logged in Intacct; if ZTERS wins, the returned money is also logged.
- **Responsible:** TBD

## CUBE-PH5-D2-044
- **Group:** Chargebacks
- **Category:** Functional
- **Epic:** Chargeback Reporting
- **Parent Task:** Chargeback Dashboard
- **Task Name:** Display Chargeback Dashboard Metrics
- **User Story:** As a Fulfillment Representative, I want open chargebacks and response deadlines summarized on a dashboard so that disputes requiring attention can be identified promptly.
- **Description:** The workshop identified basic chargeback metrics such as open volume, total amount, oldest open case, and approaching response deadlines.
- **Acceptance Criteria:** 1. The dashboard displays the number of open chargebacks, 2. The dashboard displays the total disputed amount for open chargebacks, 3. The oldest open chargeback is identified, 4. Chargebacks approaching their respond-by date are identified, 5. Chargebacks without a recorded response are distinguishable, 6. A user can open the underlying chargeback from the dashboard
- **Timestamp:** Day 2, Part 2 [00:10:35 – 00:13:09]
- **Mockups:** NO MOCKUP
- **Notes:** Product-line and service-type information can support later chargeback analysis.
- **Responsible:** TBD

## CUBE-PH5-D2-045
- **Group:** Credit Limits
- **Category:** Functional
- **Epic:** Credit Limit Management
- **Parent Task:** Request Queue
- **Task Name:** Display Credit Limit Requests Needing Review
- **User Story:** As an Accounts Payable Supervisor, I want credit-limit requests requiring a response displayed on the AR dashboard so that I do not have to search for them manually every day.
- **Description:** A credit-limit request can be created while information is still being gathered. Once submitted for review, it should appear as actionable work with its submission date instead of relying on an email alone.
- **Acceptance Criteria:** 1. An incomplete credit-limit request can remain in Draft status, 2. A completed request can be submitted for review, 3. Submitted requests appear on the AR dashboard, 4. The dashboard displays the date the request was submitted, 5. The dashboard identifies requests that still need a response, 6. The reviewer can open the request directly from the dashboard
- **Timestamp:** Day 2, Part 2 [00:13:28 – 00:16:16]
- **Mockups:** NO MOCKUP
- **Notes:** The reviewer stated that a dashboard item is preferable to another email notification.
- **Responsible:** TBD

## CUBE-PH5-D2-046
- **Group:** Customers
- **Category:** Functional
- **Epic:** Customer Financial Information
- **Parent Task:** Credit Evaluation
- **Task Name:** Display Customer Credit-Evaluation Information
- **User Story:** As a Fulfillment Director, I want customer spend and operational history available during credit review so that credit-limit decisions are based on existing customer information.
- **Description:** The requested information includes monthly customer billing, three-month and six-month averages, customer tenure, site and service history, open invoices, and business-qualification information. Much of this information should live on the customer record rather than be duplicated on every credit request.
- **Acceptance Criteria:** 1. Monthly billed amounts for the previous year are available, 2. Three-month and six-month billing averages are displayed, 3. Active, removed, and historical sites and services are summarized, 4. Open invoices greater than 60 days are visible, 5. Customer tenure and credit-card-decline information are available, 6. Business-qualification information identifies how the customer came to ZTERS
- **Timestamp:** Day 2, Part 2 [00:16:25 – 00:24:12]
- **Mockups:** NO MOCKUP
- **Notes:** The spend trend was specifically identified as information that does not currently exist adequately on the customer page.
- **Responsible:** TBD

## CUBE-PH5-D2-047
- **Group:** Credit Limits
- **Category:** Functional
- **Epic:** Credit Limit Management
- **Parent Task:** Request Information
- **Task Name:** Simplify and Structure Credit Limit Requests
- **User Story:** As a Fulfillment Representative, I want credit-limit requests limited to structured request-specific information so that reviewers receive useful facts without duplicated or contextless fields.
- **Description:** General customer data should remain on the customer and related records. The request itself should contain the requested terms, recommendations, justification, and structured questions specifically needed for the credit decision.
- **Acceptance Criteria:** 1. Customer information already stored elsewhere is not manually duplicated on the request, 2. An accounting contact must exist on the customer record before the request is created, 3. Requested payment terms and requested credit amount are captured, 4. The reason for the request and supporting recommendation are captured, 5. Questionnaire fields are organized separately from factual request information, 6. Contextless fields such as Expected Quantity of Orders are not required
- **Timestamp:** Day 2, Part 2 [00:24:12 – 00:29:24]
- **Mockups:** NO MOCKUP
- **Notes:** The final questionnaire questions still need to be defined by the Accounting stakeholders.
- **Responsible:** TBD

## CUBE-PH5-D2-048
- **Group:** Credit Limits
- **Category:** Functional
- **Epic:** Credit Limit Management
- **Parent Task:** Approval Workflow
- **Task Name:** Process Credit Limit Requests Through Defined Statuses
- **User Story:** As a Fulfillment Representative, I want credit-limit requests processed through defined workflow statuses so that approval decisions and requests for additional information are traceable.
- **Description:** The administrative section currently records whether the request was approved, denied, or needs more information. Cube should manage these outcomes as part of the request workflow.
- **Acceptance Criteria:** 1. A completed request can be submitted for review, 2. The reviewer can place the request In Process, 3. The reviewer can approve the request, 4. The reviewer can deny the request, 5. The reviewer can return the request because more information is needed, 6. The approved amount and decision notes are recorded with the final action
- **Timestamp:** Day 2, Part 2 [00:29:33 – 00:30:43]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript also proposed replacing free-text review notes with defined review steps, but the step list was not provided.
- **Responsible:** TBD

## CUBE-PH5-D2-049
- **Group:** Credit Limits
- **Category:** Functional
- **Epic:** Credit Limit Management
- **Parent Task:** Secondary Approval
- **Task Name:** Require Secondary Approval Above $5,000
- **User Story:** As an Accounts Payable Supervisor, I want credit-limit requests above $5,000 routed for secondary approval so that the existing approval authority is enforced systematically.
- **Description:** The primary reviewer can approve amounts up to $5,000. Requests above that amount currently require secondary approval through an undocumented email process.
- **Acceptance Criteria:** 1. The primary reviewer can approve a credit limit of up to $5,000, 2. A requested or approved amount above $5,000 triggers secondary approval, 3. A request requiring secondary approval cannot be finalized by the primary reviewer alone, 4. The designated secondary approver can approve or reject the request, 5. Both approval actions are retained in the workflow history, 6. The secondary approval is handled within Cube instead of relying only on an email thread
- **Timestamp:** Day 2, Part 2 [00:30:50 – 00:32:32]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript did not identify the exact Cube role or group that will receive secondary approval requests.
- **Responsible:** TBD

---

# Day 3

**Stories:** 44

## CUBE-PH5-D3-001
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Ticket Information
- **Task Name:** Generate Site-Based Purchase Order Number
- **User Story:** As a Fulfillment Representative, I want each fulfillment ticket to display a purchase order number based on the related site record ID, so that invoices and hauler records can be linked at the site level.
- **Description:** The purchase order number uses the ZTERS site identifier because haulers commonly invoice ZTERS by site rather than by individual product.
- **Acceptance Criteria:** 1. The purchase order number is generated from the related site record ID, 2. The purchase order number includes the ZTERS site prefix, 3. The purchase order number identifies the site associated with the ticket, 4. The purchase order number is available for communication with the hauler, 5. The same site-based purchase order number can be used to link related invoices and services.
- **Timestamp:** Day 3, Part 1 [0:06 - 0:32]
- **Mockups:** NO MOCKUP
- **Notes:** Haulers commonly invoice by site rather than by individual product.
- **Responsible:** TBD

## CUBE-PH5-D3-002
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Product Information
- **Task Name:** Display Product Quantity and Project Length
- **User Story:** As a Fulfillment Representative, I want to view the product quantity and expected project length on the fulfillment ticket, so that I can request accurate pricing from service providers.
- **Description:** The ticket displays quantity and project length obtained from the related product record. Project length can affect the rates offered by service providers, particularly for portable toilets.
- **Acceptance Criteria:** 1. The ticket displays the quantity recorded for the related product, 2. The ticket displays the expected project length in months, 3. Quantity and project length are retrieved from the product record, 4. These fields are presented as reference information on the fulfillment ticket, 5. The values are edited from the product record rather than the fulfillment ticket, 6. The information is available while requesting provider pricing.
- **Timestamp:** Day 3, Part 1 [0:33 - 3:05]
- **Mockups:** NO MOCKUP
- **Notes:** Project length is reference information pulled from the product page and may affect provider pricing.
- **Responsible:** TBD

## CUBE-PH5-D3-003
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Ticket Classification
- **Task Name:** Select Fulfillment Ticket Type
- **User Story:** As a Fulfillment Representative, I want fulfillment tickets to be classified by ticket type, so that I can understand the service action requested.
- **Description:** The discussed ticket types include delivery, scheduled service change request, service issue, service needed, canceled scheduled order, ETA, removal, information request, quote request, and service level optimization.
- **Acceptance Criteria:** 1. A ticket type can be selected for each fulfillment ticket, 2. Delivery identifies a request to deliver a product, 3. Scheduled service change identifies a change to a booked delivery or existing service, 4. Service issue identifies a problem with an existing service, 5. Service needed identifies an additional service such as a swap or cleaning, 6. Removal identifies a request to remove a product from the site.
- **Timestamp:** Day 3, Part 1 [3:06 - 6:45]
- **Mockups:** NO MOCKUP
- **Notes:** ZSight-specific ticket types were discussed separately and are not part of the standard Fulfillment flow.
- **Responsible:** TBD

## CUBE-PH5-D3-004
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Service Scheduling
- **Task Name:** Identify Pre-Scheduled Removal Service
- **User Story:** As a Fulfillment Representative, I want a pre-scheduled service indicator on applicable tickets, so that delivery and removal can be arranged with the provider at the same time.
- **Description:** Pre-scheduled service applies when the customer schedules the removal when requesting delivery. It applies to dumpsters, storage containers, fencing, and construction portable toilets, but not event portable toilets.
- **Acceptance Criteria:** 1. The ticket includes a pre-scheduled service indicator, 2. The indicator identifies that removal is being scheduled with delivery, 3. The requested delivery date can be recorded, 4. The requested removal date can be recorded, 5. The indicator is available for dumpsters, storage containers, fencing, and construction portable toilets, 6. The indicator does not apply to event portable toilets.
- **Timestamp:** Day 3, Part 1 [9:11 - 10:29]
- **Mockups:** NO MOCKUP
- **Notes:** Pre-scheduled removal does not apply to event portable toilets because their removal is already expected.
- **Responsible:** TBD

## CUBE-PH5-D3-005
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Priority Management
- **Parent Task:** Request Prioritization
- **Task Name:** Identify Priority, Same-Day, and Bat Phone Requests
- **User Story:** As a Fulfillment Representative, I want tickets to identify different urgency levels, so that I can prioritize requests according to how quickly the customer needs service.
- **Description:** The workshop described priority requests, same-day requests, and bat phone requests as increasingly urgent indicators.
- **Acceptance Criteria:** 1. A priority request identifies service needed very soon, 2. Same-day or next-day needs can be treated as high-priority requests, 3. A same-day request identifies service that must be arranged that day, 4. A bat phone request identifies a customer waiting on the phone for immediate confirmation, 5. Urgency indicators are visible to Fulfillment, 6. The indicators can be used when prioritizing ticket work.
- **Timestamp:** Day 3, Part 1 [10:30 - 11:48]
- **Mockups:** NO MOCKUP
- **Notes:** The three urgency indicators represent increasing levels of urgency: priority, same-day, and bat phone.
- **Responsible:** TBD

## CUBE-PH5-D3-006
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Priority Management
- **Parent Task:** Bat Phone Workflow
- **Task Name:** Process Bat Phone Quote Requests
- **User Story:** As a Fulfillment Representative, I want bat phone quote requests to support rapid provider pricing and availability checks, so that Sales can respond while the customer remains on the phone.
- **Description:** A bat phone begins as an urgent quote request. If the customer accepts the pricing and availability, Sales creates the related delivery ticket.
- **Acceptance Criteria:** 1. A bat phone request begins as a quote request, 2. The customer remains on the phone while Fulfillment contacts providers, 3. Fulfillment obtains provider pricing and availability, 4. The response is communicated to the Account Manager or BDR, 5. A delivery ticket is created when the customer accepts the offer, 6. A successful bat phone sale therefore includes the quote request and delivery ticket.
- **Timestamp:** Day 3, Part 1 [11:49 - 13:38]
- **Mockups:** NO MOCKUP
- **Notes:** A successful bat phone request normally results in two tickets: a quote request and a delivery ticket.
- **Responsible:** TBD

## CUBE-PH5-D3-007
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Provider Selection
- **Parent Task:** Preferred Provider
- **Task Name:** Identify a Pre-Selected Hauler
- **User Story:** As a Fulfillment Representative, I want a quote request to identify a pre-selected hauler, so that I can contact an existing or preferred provider first.
- **Description:** This indicator is used when a provider is already servicing the site or when the requester suggests an existing provider.
- **Acceptance Criteria:** 1. The ticket includes a quote-with-pre-selected-hauler indicator, 2. The selected or preferred provider is identifiable from the ticket, 3. The indicator can be used when a provider is already servicing the site, 4. The Fulfillment Representative can use the information to determine whom to contact, 5. The provider remains subject to pricing and availability confirmation.
- **Timestamp:** Day 3, Part 1 [13:39 - 14:28]
- **Mockups:** NO MOCKUP
- **Notes:** The pre-selected hauler may already service another product at the site.
- **Responsible:** TBD

## CUBE-PH5-D3-008
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Multi-Product Fulfillment
- **Parent Task:** Ticket Coordination
- **Task Name:** Coordinate Multiple Products at One Site
- **User Story:** As a Fulfillment Representative, I want multi-product tickets for the same site to be identifiable and coordinated, so that one representative can work the site and minimize the number of providers contacted.
- **Description:** One representative should work the related product tickets to avoid duplicate calls and, when possible, locate one provider capable of servicing multiple products.
- **Acceptance Criteria:** 1. A ticket can identify that the site has multiple requested products, 2. Related product tickets remain separate tickets, 3. Related tickets identify the same site and customer, 4. One Fulfillment Representative should work the related tickets, 5. The representative can look for a provider capable of servicing multiple product types, 6. Coordination avoids multiple representatives contacting the same provider for the same site.
- **Timestamp:** Day 3, Part 1 [14:29 - 16:05]
- **Mockups:** NO MOCKUP
- **Notes:** The objective is to avoid duplicate provider calls and use fewer providers when possible.
- **Responsible:** TBD

## CUBE-PH5-D3-009
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Quote Requests
- **Parent Task:** Quote Request Classification
- **Task Name:** Capture the Quote Request Reason
- **User Story:** As a Fulfillment Representative, I want each quote request to identify why provider pricing is required, so that I understand why statistical pricing was not used directly.
- **Description:** Reasons discussed include area not covered, large order, multiple products, product not covered by the statistical model, expedited availability, specific requirements, possibly franchised market, and other.
- **Acceptance Criteria:** 1. A quote request reason is required for a quote request, 2. Only one quote request reason is selected for the same product, 3. Large order identifies a quantity requiring provider pricing, 4. Product not covered identifies a product or material outside the statistical model, 5. Expedited availability identifies an urgent availability request, 6. Other can be used when the request does not match another available reason.
- **Timestamp:** Day 3, Part 1 [16:40 - 22:50]
- **Mockups:** NO MOCKUP
- **Notes:** “Blacked out area not covered” was questioned during the workshop and explicitly skipped.
- **Responsible:** TBD

## CUBE-PH5-D3-010
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Ticket Creation
- **Task Name:** Create Fulfillment Tickets from Product Records
- **User Story:** As a Fulfillment Representative, I want fulfillment tickets to be created contextually from product records, so that the related customer, site, and product information is already known.
- **Description:** The intended operational flow is to open the relevant product and create the fulfillment ticket from that context rather than creating a ticket from the top-level module.
- **Acceptance Criteria:** 1. A fulfillment ticket can be initiated from a product record, 2. The ticket retains the related product context, 3. Related site and customer information is available through the product relationship, 4. Users are not required to select the full customer-site-product hierarchy manually, 5. The add interface is designed around the product-level workflow, 6. Each product has its own fulfillment ticket.
- **Timestamp:** Day 3, Part 1 [22:51 - 25:31]
- **Mockups:** NO MOCKUP
- **Notes:** The intended workflow starts from the product record; direct ticket creation without product context is not expected.
- **Responsible:** TBD

## CUBE-PH5-D3-011
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Multi-Product Fulfillment
- **Parent Task:** Ticket Submission
- **Task Name:** Stage and Submit Multi-Product Tickets Together
- **User Story:** As a Fulfillment Representative, I want multiple product tickets for the same site to be prepared before they are sent to Fulfillment, so that they enter the queue together and can be assigned to one representative.
- **Description:** The current process creates all product tickets first and then sends them from the site page as close together as possible.
- **Acceptance Criteria:** 1. A separate ticket is created for every product, 2. Related tickets can remain unsent while all tickets are prepared, 3. Notes and required details can be entered before submission, 4. Related tickets can be accessed from the site page, 5. The tickets are sent to Fulfillment together or as close together as possible, 6. The submitted tickets are identifiable as belonging to the same site.
- **Timestamp:** Day 3, Part 1 [25:32 - 30:15]
- **Mockups:** NO MOCKUP
- **Notes:** QuickBase currently requires users to stage the tickets and send them individually as close together as possible.
- **Responsible:** TBD

## CUBE-PH5-D3-012
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Multi-Product Fulfillment
- **Parent Task:** Ticket Grouping
- **Task Name:** Group Newly Created Multi-Product Tickets
- **User Story:** As a Fulfillment Representative, I want newly created product tickets for the same site to be grouped, so that current requests are distinguished from older products already at the site.
- **Description:** The discussed improvement was to group tickets using a defined threshold such as tickets created for the same site on the same day.
- **Acceptance Criteria:** 1. The grouping identifies tickets for the same site, 2. The grouping distinguishes newly requested products from older products, 3. Same-day creation can be used as the proposed grouping threshold, 4. Existing products from earlier requests are not automatically included in the new group, 5. Each ticket in the group displays the other relevant tickets, 6. The group shows the number and types of tickets being assigned.
- **Timestamp:** Day 3, Part 1 [30:16 - 36:34]
- **Mockups:** NO MOCKUP
- **Notes:** Improvement request; the exact grouping threshold and logic still require definition.
- **Responsible:** TBD

## CUBE-PH5-D3-013
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Queue Management
- **Parent Task:** Ticket Assignment
- **Task Name:** Assign Grouped Tickets to One Representative
- **User Story:** As a Fulfillment Quality Coordinator, I want related tickets for a multi-product request to be assigned together, so that one Fulfillment Representative can work the complete site request.
- **Description:** The workshop proposed bulk assignment or automatic assignment of related tickets when one ticket in the group is claimed.
- **Acceptance Criteria:** 1. Related tickets can be selected as a group for assignment, 2. The group can be assigned to one Fulfillment Representative, 3. The representative can see that accepting one ticket includes additional tickets, 4. The representative can view all tickets in the assigned group, 5. The representative is notified when an additional related ticket is assigned, 6. The assignment does not automatically include unrelated older tickets for the site.
- **Timestamp:** Day 3, Part 1 [27:56 - 37:15]
- **Mockups:** NO MOCKUP
- **Notes:** Automatic assignment was considered possible but complex and was not promised.
- **Responsible:** TBD

## CUBE-PH5-D3-014
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Queue Management
- **Parent Task:** Queue Vetting
- **Task Name:** Prioritize and Vet Incoming Tickets
- **User Story:** As a Fulfillment Quality Coordinator, I want to review and prioritize incoming fulfillment tickets, so that representatives receive actionable tickets with sufficient information.
- **Description:** Queue coordinators prioritize delivery and other urgent tickets and review quote requests for completeness and feasibility before assignment.
- **Acceptance Criteria:** 1. Sent but unassigned tickets appear in the Fulfillment queue, 2. Delivery and priority tickets can be identified for assignment, 3. Quote requests can be reviewed before assignment, 4. Tickets missing required information can be returned to Sales, 5. Requests that cannot be fulfilled can be returned with an explanation, 6. Workable tickets can be assigned to a Fulfillment Representative.
- **Timestamp:** Day 3, Part 1 [37:16 - 40:24]
- **Mockups:** NO MOCKUP
- **Notes:** Queue coordinators currently perform this review manually before distributing tickets.
- **Responsible:** TBD

## CUBE-PH5-D3-015
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Data Validation
- **Parent Task:** Location Information
- **Task Name:** Require a Serviceable Location
- **User Story:** As a Fulfillment Quality Coordinator, I want tickets to contain a complete location or usable location details, so that requests containing only a ZIP code do not enter the Fulfillment queue.
- **Description:** A full address is preferred, but coordinates, cross streets, a naval base, or another sufficiently specific location description may be used for job sites without conventional addresses.
- **Acceptance Criteria:** 1. A ticket cannot be submitted with only a ZIP code, 2. A complete site address satisfies the location requirement, 3. Exact coordinates can satisfy the requirement when a standard address is unavailable, 4. Cross streets or another specific location description can be provided, 5. The location information gives Fulfillment more detail than the ZIP code, 6. A ticket without sufficient location information is returned for correction.
- **Timestamp:** Day 3, Part 1 [40:25 - 41:47]
- **Mockups:** NO MOCKUP
- **Notes:** Coordinates or another specific location description may be used when a conventional address does not exist.
- **Responsible:** TBD

## CUBE-PH5-D3-016
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Data Validation
- **Parent Task:** Product Requirements
- **Task Name:** Confirm Product Accessories
- **User Story:** As a Fulfillment Representative, I want the requester to confirm required or requested accessories, so that I receive enough information to obtain a complete provider quote.
- **Description:** The workshop identified office containers and portable toilets as examples where missing accessory information causes incomplete requests.
- **Acceptance Criteria:** 1. Standard accessories can be presented for the selected product, 2. The requester confirms whether the customer needs the listed accessories, 3. The requester can indicate that none of the listed accessories are needed, 4. Product-specific accessory information is available to Fulfillment, 5. Common accessory lists do not prevent additional non-standard requests, 6. A request requiring accessory details can be returned when the information is missing.
- **Timestamp:** Day 3, Part 1 [41:48 - 43:14]
- **Mockups:** NO MOCKUP
- **Notes:** Standard accessory lists may not cover every possible office-container request.
- **Responsible:** TBD

## CUBE-PH5-D3-017
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Data Validation
- **Parent Task:** Placement Information
- **Task Name:** Capture Actionable Placement Instructions
- **User Story:** As a Fulfillment Representative, I want delivery tickets to contain actionable placement instructions or adequate on-site contacts, so that providers can place products without unnecessary delays or fees.
- **Description:** Placement may be provided through detailed text or a marked image. “Call on-site” is insufficient by itself when no reliable contact or consequence acknowledgment is provided.
- **Acceptance Criteria:** 1. Placement information is required for delivery and later-stage tickets, 2. Detailed text instructions can be provided, 3. A marked placement image can be provided, 4. Placement information is displayed prominently to Fulfillment, 5. If placement depends on an on-site contact, a secondary contact is requested when available, 6. Quote-only requests are not required to provide final placement-level detail.
- **Timestamp:** Day 3, Part 1 [43:15 - 54:26]
- **Mockups:** NO MOCKUP
- **Notes:** The system can require information but cannot guarantee that the entered placement instructions are accurate or useful.
- **Responsible:** TBD

## CUBE-PH5-D3-018
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Data Validation
- **Parent Task:** Placement Risk
- **Task Name:** Acknowledge Call-On-Site Consequences
- **User Story:** As a Fulfillment Representative, I want the ticket to document when placement depends on calling the on-site contact and whether the consequences were discussed, so that the customer understands the risk of a dry run or relocation fee.
- **Description:** The proposed systematic option was a placement method selection followed by an acknowledgment when “call on-site” is selected.
- **Acceptance Criteria:** 1. A placement method identifies whether instructions are provided as an image, detailed notes, or call on-site, 2. Selecting call-on-site prompts for two contacts when available, 3. The requester can acknowledge that the consequences were discussed with the customer, 4. The acknowledgment covers possible driver best judgment, dry run, or relocation consequences, 5. Updated placement instructions can be added when received, 6. The final operational response must follow the standardized ZTERS process.
- **Timestamp:** Day 3, Part 1 [54:27 - 1:00:28]
- **Mockups:** NO MOCKUP
- **Notes:** The standard outcome when an on-site contact cannot be reached still requires a business decision.
- **Responsible:** TBD

## CUBE-PH5-D3-019
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Quote Requests
- **Parent Task:** Expedited Requests
- **Task Name:** Process Expedited Availability Quotes
- **User Story:** As a Fulfillment Representative, I want expedited quote requests to show that the customer was pre-qualified for possible additional fees, so that I can rapidly confirm availability and pricing.
- **Description:** Expedited availability applies to same-day and potentially next-day quote requests and was described as a reverse bat chat.
- **Acceptance Criteria:** 1. Expedited availability can be selected as the quote request reason, 2. The ticket indicates whether the customer was pre-qualified, 3. Pre-qualification confirms that possible additional fees were explained, 4. Fulfillment can keep the provider on the phone while Sales contacts the customer, 5. Provider pricing and availability are communicated to Sales, 6. The provider can be booked after the customer accepts.
- **Timestamp:** Day 3, Part 1 [1:08:04 - 1:09:43]
- **Mockups:** NO MOCKUP
- **Notes:** This workflow was described as a “reverse bat chat” because Fulfillment keeps the provider on the phone while Sales contacts the customer.
- **Responsible:** TBD

## CUBE-PH5-D3-020
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Quote Requests
- **Parent Task:** Specific Requirements
- **Task Name:** Capture Delivery, Placement, and Access Requirements
- **User Story:** As a Fulfillment Representative, I want quote requests to identify specific delivery, placement, or access requirements, so that I can obtain pricing from a provider capable of meeting them.
- **Description:** Examples include restricted delivery windows, sidewalk placement, bridge access, locked gates, access codes, military base requirements, and placement permits.
- **Acceptance Criteria:** 1. A specific delivery requirement can record an allowed delivery window, 2. A specific placement requirement can describe where the product must be placed, 3. A specific access requirement can document gates, codes, permits, or identification, 4. Placement permit requirements can be recorded, 5. The selected requirement is visible while obtaining a quote, 6. The provider can confirm whether the requirement can be met.
- **Timestamp:** Day 3, Part 1 [1:09:44 - 1:10:48]
- **Mockups:** NO MOCKUP
- **Notes:** Requirements vary by site and may include delivery windows, permits, gates, access codes, or identification.
- **Responsible:** TBD

## CUBE-PH5-D3-021
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Provider Selection
- **Parent Task:** Franchise Markets
- **Task Name:** Warn About Possibly Franchised Markets
- **User Story:** As a Fulfillment Representative, I want tickets to warn me when a roll-off request may be in a franchised market, so that I can obtain accurate provider pricing and protect the expected margin.
- **Description:** Possible franchise warnings are based on ZIP-code data maintained from hauler quotes marked as franchised.
- **Acceptance Criteria:** 1. The system checks the service ZIP code for a possible franchise designation, 2. A warning is displayed when the ZIP code is marked as possibly franchised, 3. The warning applies primarily to roll-off dumpster requests, 4. A hauler quote can be marked as a franchise quote, 5. Franchise quote records provide historical information for the ZIP code, 6. Updated franchise information can be incorporated into the ZIP-code data.
- **Timestamp:** Day 3, Part 1 [1:11:04 - 1:15:31]
- **Mockups:** NO MOCKUP
- **Notes:** Franchise information is currently reviewed and added to the ZIP-code database through a monthly manual process.
- **Responsible:** TBD

## CUBE-PH5-D3-022
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Queue Management
- **Parent Task:** Ticket Rejection
- **Task Name:** Record Ticket Non-Approval Reasons
- **User Story:** As a Fulfillment Quality Coordinator, I want to select why an incoming ticket was not approved, so that Sales knows what must be corrected before resubmission.
- **Description:** Reasons discussed include missing location, missing delivery date, no-sale product status for a delivery, missing billing preference, missing placement or contacts, failure to use an available PSP, and other missing information.
- **Acceptance Criteria:** 1. A non-approval reason can be selected when a ticket is returned, 2. No address or coordinates can be selected as a reason, 3. Missing delivery date can be selected for a delivery ticket, 4. Missing customer billing preference can be selected, 5. Missing placement notes or on-site contacts can be selected, 6. Failure to select an available PSP can be selected.
- **Timestamp:** Day 3, Part 1 [1:16:13 - 1:19:38]
- **Mockups:** NO MOCKUP
- **Notes:** These non-approval reasons were identified as potential future submission validations.
- **Responsible:** TBD

## CUBE-PH5-D3-023
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Priority Management
- **Parent Task:** Priority Scoring
- **Task Name:** Calculate Ticket Priority
- **User Story:** As a Fulfillment Representative, I want ticket priority to be calculated from relevant request indicators, so that the queue can be prioritized consistently.
- **Description:** The current calculation considers indicators such as priority request, bat phone, multi-product site, large quantity, and sales temperature.
- **Acceptance Criteria:** 1. The ticket stores the selected sales temperature, 2. The priority calculation considers whether the ticket is marked as a priority request, 3. The calculation considers whether the ticket is a bat phone request, 4. The calculation considers multi-product and large-quantity indicators, 5. The calculation considers the sales temperature, 6. The resulting priority is categorized for queue use.
- **Timestamp:** Day 3, Part 1 [1:20:24 - 1:23:33]
- **Mockups:** NO MOCKUP
- **Notes:** Sales temperature is currently subjective; automation or improved scoring was requested.
- **Responsible:** TBD

## CUBE-PH5-D3-024
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Ticket Submission
- **Task Name:** Save and Send Tickets to Fulfillment
- **User Story:** As a Fulfillment Representative, I want tickets to remain in a draft state until they are explicitly sent to Fulfillment, so that all required information can be completed before the ticket becomes actionable.
- **Description:** Saving creates the record, while Send to Fulfillment moves the completed ticket into the unassigned Fulfillment queue.
- **Acceptance Criteria:** 1. The ticket is saved before it is submitted, 2. Saving creates the ticket record and record ID, 3. A saved ticket does not automatically enter the Fulfillment queue, 4. Send to Fulfillment changes the ticket from prepared to actionable, 5. Sent tickets appear in the sent-but-unassigned queue, 6. A sent ticket can be assigned by a coordinator or claimed by a Fulfillment Representative.
- **Timestamp:** Day 3, Part 1 [1:23:34 - 1:27:15]
- **Mockups:** NO MOCKUP
- **Notes:** Saving creates the record, while Send to Fulfillment makes it actionable.
- **Responsible:** TBD

## CUBE-PH5-D3-025
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Workflow Management
- **Parent Task:** Ticket Progress
- **Task Name:** Track Fulfillment Ticket Workflow and Durations
- **User Story:** As a Fulfillment Director, I want the system to track each fulfillment ticket stage, timestamp, and duration, so that ticket progress and team performance can be measured.
- **Description:** The described flow is sent, assigned, fulfilled, finished, and accepted, with additional tracking for cancellations. A one-hour work threshold was shown for the assigned representative.
- **Acceptance Criteria:** 1. The workflow displays the ticket's current stage, 2. Sent, assigned, fulfilled, finished, and accepted events are timestamped, 3. The system calculates durations between workflow events, 4. The assigned representative can see the remaining time against the one-hour threshold, 5. Cancellation time and duration are tracked when applicable, 6. The recorded durations are available for KPI reporting.
- **Timestamp:** Day 3, Part 1 [1:42:24 - 1:45:44]
- **Mockups:** NO MOCKUP
- **Notes:** The demonstrated performance threshold allowed one hour for the assigned representative to work the ticket.
- **Responsible:** TBD

## CUBE-PH5-D3-026
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Quote Fulfillment
- **Parent Task:** Ticket Review
- **Task Name:** Review Complete Ticket Context Before Quoting
- **User Story:** As a Fulfillment Representative, I want the fulfillment ticket to present the relevant customer, site, product, provider, and pricing information together, so that I can review the request without opening numerous pages and external tabs.
- **Description:** The representative currently checks the address, coordinates, site products, product details, accessories, placement, PSP, statistical pricing, prior providers, and margin information across several locations.
- **Acceptance Criteria:** 1. The ticket displays the exact address or coordinates, 2. The ticket displays the requested service and delivery information, 3. The ticket displays applicable accessories and placement instructions, 4. The ticket identifies other products and fulfillment tickets for the site, 5. The ticket displays relevant provider and pricing information, 6. The information is presented cohesively at the fulfillment ticket level.
- **Timestamp:** Day 3, Part 1 [1:46:14 - 1:54:46]
- **Mockups:** NO MOCKUP
- **Notes:** The current process requires reviewing several QuickBase pages, Google Maps, the pricing tool, and provider reports.
- **Responsible:** TBD

## CUBE-PH5-D3-027
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Provider Selection
- **Parent Task:** Pricing Tool Integration
- **Task Name:** Display Relevant Providers for the Service Location
- **User Story:** As a Fulfillment Representative, I want provider results from pricing and ZIP-code history to be available from the ticket, so that I can identify appropriate providers without performing separate searches.
- **Description:** The representative currently compares providers returned by the pricing tool with providers that previously serviced the ZIP code and excludes providers marked DNU.
- **Acceptance Criteria:** 1. Provider results use the ticket's service location, 2. Pricing-tool providers can be displayed from the ticket, 3. Providers that previously serviced the ZIP code can be displayed, 4. Recent service information can be shown for those providers, 5. PSP and statistical-pricing results are distinguishable, 6. Providers marked DNU are identifiable and are not selected for service.
- **Timestamp:** Day 3, Part 1 [1:50:47 - 1:57:27]
- **Mockups:** NO MOCKUP
- **Notes:** Providers marked DNU must not be selected even when they appear in pricing results.
- **Responsible:** TBD

## CUBE-PH5-D3-028
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Product Information
- **Parent Task:** Product Details
- **Task Name:** Display Detailed Product Requirements on the Ticket
- **User Story:** As a Fulfillment Representative, I want the ticket to display product-specific details such as debris types and accessories, so that I do not need to open the product page to verify the exact request.
- **Description:** The workshop specifically identified roll-off debris details and portable-toilet accessories as information that should be available on the ticket.
- **Acceptance Criteria:** 1. Roll-off tickets display the selected debris category, 2. Roll-off tickets display the exact debris type and restricted items, 3. Portable-toilet tickets display requested accessories, 4. Product details match the related product record, 5. The information is available before the representative contacts a provider, 6. Product-specific fields are shown only when relevant to the selected product.
- **Timestamp:** Day 3, Part 1 [1:57:29 - 2:04:19]
- **Mockups:** NO MOCKUP
- **Notes:** Fulfillment will provide a definitive list of the product, site, and customer fields needed on the ticket.
- **Responsible:** TBD

## CUBE-PH5-D3-029
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Service Scheduling
- **Parent Task:** Delivery Dates
- **Task Name:** Capture Requested, Latest Acceptable, and Confirmed Delivery Dates
- **User Story:** As a Fulfillment Representative, I want to see the customer's requested date, latest acceptable date, and provider-confirmed date, so that I can determine whether the proposed delivery is acceptable without unnecessary back-and-forth.
- **Description:** The requested date records the customer's preferred date, the proposed maximum date records how late the customer can accept delivery, and the confirmed availability date records when the selected provider can deliver.
- **Acceptance Criteria:** 1. The requested delivery date records the customer's preferred date, 2. A latest acceptable delivery date can be recorded, 3. The confirmed availability date records the provider's available date, 4. The original requested date remains unchanged for historical reference, 5. The product delivery date can reflect the accepted confirmed date, 6. The dates are visible together for comparison.
- **Timestamp:** Day 3, Part 1 [1:59:13 - 2:03:08]
- **Mockups:** NO MOCKUP
- **Notes:** The latest acceptable delivery date was proposed to reduce repeated confirmation between Fulfillment and Sales.
- **Responsible:** TBD

## CUBE-PH5-D3-030
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Hauler Quote Management
- **Parent Task:** Quote Creation
- **Task Name:** Organize Hauler Quote Questions in Call Order
- **User Story:** As a Fulfillment Representative, I want the hauler quote fields arranged in the order that questions are asked during a provider call, so that I can capture information without moving repeatedly around the form.
- **Description:** The representative stated that questions are asked in a specific order to keep the provider conversation organized.
- **Acceptance Criteria:** 1. The form begins with provider and contact information, 2. Pricing fields follow the natural order of the provider conversation, 3. Payment and billing questions appear where they are asked during the call, 4. Additional fees and service conditions are grouped with related pricing, 5. Quote-result fields are grouped together, 6. The layout reduces the need to move back and forth across the form.
- **Timestamp:** Day 3, Part 1 [2:05:37 - 2:15:54]
- **Mockups:** NO MOCKUP
- **Notes:** The field order should match the representative’s natural provider-call sequence.
- **Responsible:** TBD

## CUBE-PH5-D3-031
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Service Provider Data
- **Parent Task:** Provider Accounting Information
- **Task Name:** Display and Update Provider Accounting Details
- **User Story:** As a Fulfillment Representative, I want relevant accounting information from the service provider record displayed on the hauler quote, so that I can confirm missing details during the provider call and save them for future use.
- **Description:** Relevant information includes accepted and arranged payment methods, credit-card fees, taxes, billing cycle, proration, and other AP information.
- **Acceptance Criteria:** 1. Existing provider accounting information is displayed on the hauler quote, 2. Missing accounting fields are visually identifiable, 3. The representative can enter missing information during the provider call, 4. Newly captured information is saved to the service provider record, 5. Previously completed fields do not need to be requested again, 6. Relevant provider notes and fees are visible while entering the quote.
- **Timestamp:** Day 3, Part 1 [2:06:58 - 2:15:49]
- **Mockups:** NO MOCKUP
- **Notes:** The goal is to complete missing provider information progressively across multiple calls rather than ask a full questionnaire during one call.
- **Responsible:** TBD

## CUBE-PH5-D3-032
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Hauler Quote Management
- **Parent Task:** Rate Capture
- **Task Name:** Capture Provider Rates and Fees
- **User Story:** As a Fulfillment Representative, I want to record all rates and fees provided during the quote, so that the expected provider cost can be calculated accurately.
- **Description:** Discussed values include rental, delivery, removal, per-unit charges, fuel fees, fluctuating fuel costs, taxes, credit-card fees, payment methods, and accessory charges.
- **Acceptance Criteria:** 1. The standard rental rate can be entered, 2. Delivery and removal fees can be entered, 3. Delivery and removal can be identified as per-unit fees, 4. Fuel can be recorded as a percentage or dollar amount, 5. A fluctuating fuel-cost indicator can be selected, 6. Taxes, credit-card fees, and provider payment arrangements can be recorded.
- **Timestamp:** Day 3, Part 1 [2:15:54 - 2:18:50]
- **Mockups:** NO MOCKUP
- **Notes:** Provider billing structures may use 28-day, 30-day, weekly, per-service, or other arrangements.
- **Responsible:** TBD

## CUBE-PH5-D3-033
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Hauler Quote Management
- **Parent Task:** Special Pricing
- **Task Name:** Identify Site-Specific Pricing
- **User Story:** As a Fulfillment Representative, I want to identify pricing that applies only to the current site or request, so that it is not treated as the provider's standard pricing.
- **Description:** Special pricing includes substituted products, holiday surcharges, one-time discounts, and any other rate that deviates from the provider's normal pricing.
- **Acceptance Criteria:** 1. A quote can be marked as special pricing for the site only, 2. The indicator is used when the quoted product differs from the requested configuration, 3. The indicator is used for holiday-specific charges, 4. The indicator is used for one-time provider discounts, 5. Special pricing is excluded from normal provider pricing data, 6. The quote retains the special rates for the current request.
- **Timestamp:** Day 3, Part 1 [2:18:51 - 2:19:55]
- **Mockups:** NO MOCKUP
- **Notes:** Special pricing must not be incorporated into the provider’s normal historical pricing.
- **Responsible:** TBD

## CUBE-PH5-D3-034
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Accessory Management
- **Parent Task:** Required Accessories
- **Task Name:** Synchronize Required Accessories and Pricing
- **User Story:** As a Fulfillment Representative, I want provider-required accessories captured on a hauler quote to update the related product, so that the accessory is included in margin calculations.
- **Description:** The workshop specifically discussed containment trays that providers or municipalities require even when the customer did not initially request one.
- **Acceptance Criteria:** 1. A required accessory can be selected from the hauler quote, 2. The accessory rate can be recorded separately, 3. Selecting a required accessory updates the related product accessory selection, 4. The accessory cost is included in the product margin calculation, 5. Customer-requested accessories remain visible on the hauler quote, 6. Provider-required accessories can flow back to the product even when they were not selected originally.
- **Timestamp:** Day 3, Part 1 [2:19:56 - 2:29:29]
- **Mockups:** NO MOCKUP
- **Notes:** Containment trays were identified as the primary accessory requiring information to flow from the hauler quote back to the product.
- **Responsible:** TBD

## CUBE-PH5-D3-035
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Hauler Quote Management
- **Parent Task:** Additional Rates
- **Task Name:** Capture Additional and Conditional Service Rates
- **User Story:** As a Fulfillment Representative, I want to record additional provider charges and their frequency, so that expected costs include fees not covered by the standard rate fields.
- **Description:** Additional fields discussed include other rate, winterization, dry run, extra service, after-hours service, relocation, and weekly service days.
- **Acceptance Criteria:** 1. An additional rate can include a description, 2. An additional rate can be marked as one-time or recurring, 3. A winterization rate can be recorded, 4. Dry run and relocation rates can be recorded, 5. Additional and after-hours service rates can be recorded, 6. The provider's weekly service days can be selected.
- **Timestamp:** Day 3, Part 1 [2:29:30 - 2:36:10]
- **Mockups:** NO MOCKUP
- **Notes:** Winterization is tracked separately for accounting analysis even when it appears on the provider invoice.
- **Responsible:** TBD

## CUBE-PH5-D3-036
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Margin Management
- **Parent Task:** Quote Comparison
- **Task Name:** Compare Provider Quotes and Margins
- **User Story:** As a Fulfillment Representative, I want customer pricing, provider pricing, availability, and margin displayed for every hauler quote, so that I can compare providers without repeatedly sending rates to the product page.
- **Description:** The current process copies each quote to the product page to calculate its margin. Low-margin requests require three quotes and negative-margin requests require five.
- **Acceptance Criteria:** 1. Each hauler quote displays the applicable customer pricing, 2. Each quote displays the provider's pricing, 3. The margin is calculated for each quote independently, 4. Multiple quotes can be compared in one table, 5. Confirmed provider availability is displayed with the margin, 6. Quote values do not need to overwrite the product repeatedly for comparison.
- **Timestamp:** Day 3, Part 1 [2:36:10 - 2:40:38]
- **Mockups:** NO MOCKUP
- **Notes:** Current policy requires three quotes for low-margin requests and five for negative-margin requests.
- **Responsible:** TBD

## CUBE-PH5-D3-037
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Audit Trail
- **Parent Task:** Change History
- **Task Name:** Track Changes to Quote and Ticket Fields
- **User Story:** As a Fulfillment Representative, I want changes to fulfillment ticket and hauler quote fields logged automatically, so that I do not need to duplicate structured information in notes to preserve a historical record.
- **Description:** Representatives currently repeat dates, providers, contacts, and rates in notes because those fields can later be edited. Cube is expected to log what changed and who changed it.
- **Acceptance Criteria:** 1. Changes to tracked fields are recorded, 2. The previous and updated values are retained, 3. The user who made each change is recorded, 4. Date, provider, contact, and rate changes can be reviewed, 5. Structured values do not need to be duplicated in notes solely for historical protection, 6. Notes remain available for information that has no dedicated field.
- **Timestamp:** Day 3, Part 1 [2:40:39 - 2:43:45]
- **Mockups:** NO MOCKUP
- **Notes:** Notes should still be used for information without a dedicated field, such as a provider’s inability to guarantee an ETA.
- **Responsible:** TBD

## CUBE-PH5-D3-038
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Quote Documentation
- **Parent Task:** Supporting Documents
- **Task Name:** Attach Provider Quote Documents
- **User Story:** As a Fulfillment Representative, I want provider quote documents attached to the hauler quote, so that emailed PDFs such as fencing quotes are available with the related pricing record.
- **Description:** Fencing providers commonly send quote details as PDF files, and the team requested access to those files from the hauler quote.
- **Acceptance Criteria:** 1. A document can be uploaded to a hauler quote, 2. PDF quote documents are supported, 3. The document remains associated with the related hauler quote, 4. The document is available when reviewing the quote, 5. The document is stored through the system's document records, 6. Users do not need to search separately for the provider's emailed quote.
- **Timestamp:** Day 3, Part 1 [3:06:07 - 3:07:29]
- **Mockups:** NO MOCKUP
- **Notes:** Fencing quotes are commonly received as PDF files.
- **Responsible:** TBD

## CUBE-PH5-D3-039
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Quote Selection
- **Parent Task:** Chosen Quote
- **Task Name:** Require a Chosen Quote Before Applying Provider Pricing
- **User Story:** As a Fulfillment Representative, I want to select a chosen hauler quote before its pricing is applied to the product, so that the confirmed provider and rates are clearly identified.
- **Description:** The workshop stated that Cube should prevent pricing from being sent to the product until one quote is chosen.
- **Acceptance Criteria:** 1. Multiple hauler quotes can remain available for comparison, 2. One quote can be selected as the chosen quote, 3. Only one quote is treated as chosen for the ticket, 4. Provider pricing cannot be applied to the product until a quote is chosen, 5. The chosen quote identifies the confirmed provider and rates, 6. The required selection prevents representatives from forgetting to identify the chosen quote.
- **Timestamp:** Day 3, Part 1 [3:07:30 - 3:08:43]
- **Mockups:** NO MOCKUP
- **Notes:** Direct one-click table editing was discussed but raised concerns about accidental changes to quote values.
- **Responsible:** TBD

## CUBE-PH5-D3-040
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Accounting Integration
- **Parent Task:** Payment and Receipts
- **Task Name:** Capture Upfront Payment and Provider Receipts
- **User Story:** As an Accounts Payable Supervisor, I want upfront provider payment information and receipts captured through the fulfillment ticket and chosen quote, so that payment records and supporting documents are available for item-receipt and invoice processing.
- **Description:** The workshop stated that billing information currently captured again on service tickets should move to this process because the chosen quote already contains the relevant provider information.
- **Acceptance Criteria:** 1. The selected payment method can be recorded, 2. The amount charged to the company card can be recorded, 3. The system indicates whether a receipt was attached, not provided, or sent to Invoices, 4. A receipt can be uploaded from the fulfillment ticket, 5. The uploaded document can be related to the ticket, product, customer, site, and provider, 6. Previously captured quote information is reused rather than entered again on the service ticket.
- **Timestamp:** Day 3, Part 1 [3:17:19 - 3:21:34]
- **Mockups:** NO MOCKUP
- **Notes:** For multi-product sites, the receipt may need to be related to each applicable ticket or product to remain visible from each record.
- **Responsible:** TBD

## CUBE-PH5-D3-041
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Communication
- **Parent Task:** Notifications
- **Task Name:** Send Midstream Ticket Notifications
- **User Story:** As a Fulfillment Representative, I want to notify Sales during ticket processing and distinguish between informational updates and required actions, so that the Account Manager knows whether they need to respond.
- **Description:** Notify Sales communicates information while work continues; Sales Action Required tells Sales that they must perform an action. Ticket completion already generates its own notification.
- **Acceptance Criteria:** 1. Notify Sales sends an informational update while the ticket remains in progress, 2. Sales Action Required identifies that the Account Manager must perform an action, 3. Notes can explain the information or required action, 4. Notify Fulfillment Representative alerts the assigned representative when Sales adds requested information, 5. Submitting the completed response automatically notifies the ticket owner, 6. Completing a ticket does not require an additional Notify Sales selection.
- **Timestamp:** Day 3, Part 1 [3:23:32 - 3:30:55]
- **Mockups:** NO MOCKUP
- **Notes:** Notify Sales and Sales Action Required are intended for midstream communication, not ticket completion.
- **Responsible:** TBD

## CUBE-PH5-D3-042
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Workflow Management
- **Parent Task:** Ticket Completion
- **Task Name:** Accept or Resubmit a Fulfilled Ticket
- **User Story:** As a Fulfillment Representative, I want the completed ticket to be accepted by Sales or returned for additional work, so that the fulfillment request is not closed until the response is satisfactory.
- **Description:** After Fulfillment submits its response, the Account Manager can accept the ticket or resubmit it for further action.
- **Acceptance Criteria:** 1. The Fulfillment Representative can submit a completed response, 2. The system records when the ticket was fulfilled, 3. The system calculates the fulfillment duration, 4. Sales can review the submitted response, 5. Sales can accept the ticket when the response is satisfactory, 6. Sales can resubmit the ticket when additional action is required.
- **Timestamp:** Day 3, Part 1 [3:31:36 - 3:32:02]
- **Mockups:** NO MOCKUP
- **Notes:** Ticket completion automatically notifies Sales and records the fulfillment duration.
- **Responsible:** TBD

## CUBE-PH5-D3-043
- **Group:** Hauler Quotes
- **Category:** Functional
- **Epic:** Provider Selection
- **Parent Task:** PSP Exceptions
- **Task Name:** Document PSP Quote Outcomes and Exceptions
- **User Story:** As a Fulfillment Representative, I want to record PSP outcomes and approved exceptions, so that the system explains why an available PSP was or was not used.
- **Description:** The discussed fields include PSP chosen quote, PSP could not fulfill, pricing tool could not be used for fencing, PSP not requested, and non-PSP CSS approval.
- **Acceptance Criteria:** 1. A chosen quote can identify that a PSP was selected, 2. PSP could not fulfill can be selected when the provider lacks availability or does not service the location, 3. Pricing-tool unavailability can be identified for fencing quotes, 4. PSP not requested identifies an exception where another provider was specifically requested, 5. A non-PSP selection requires a justifiable reason, 6. The non-PSP exception requires CSS approval.
- **Timestamp:** Day 3, Part 1 [3:32:03 - 3:36:46]
- **Mockups:** NO MOCKUP
- **Notes:** Using a non-PSP when a PSP is available is an exception and requires a justified reason and CSS approval.
- **Responsible:** TBD

## CUBE-PH5-D3-044
- **Group:** Fulfillment Tickets
- **Category:** Functional
- **Epic:** Core Flow
- **Parent Task:** Ticket Creation
- **Task Name:** Determine the Initial Fulfillment Ticket Type
- **User Story:** As a Fulfillment Representative, I want the initial fulfillment ticket to be created as either a quote request or a delivery ticket based on the pricing and sale status, so that the request begins with the appropriate workflow.
- **Description:** A quote request is created when exact provider pricing is needed before the customer agrees to purchase. A delivery ticket is created when the customer has agreed to purchase and pricing is already known or expected, although some delivery tickets may still require Fulfillment to obtain provider pricing and availability.
- **Acceptance Criteria:** 1. The initial ticket is created as either a quote request or a delivery ticket, 2. A quote request is used when the customer requires exact pricing before agreeing to purchase, 3. A delivery ticket is used when the customer has agreed to purchase, 4. A delivery ticket can begin directly when PSP pricing is already known, 5. A delivery ticket can include a quote-request component when provider pricing or availability must still be confirmed, 6. A separate delivery ticket is created after a quote-request customer agrees to purchase.
- **Timestamp:** Day 3, Part 2 [0:43 - 4:22]
- **Mockups:** NO MOCKUP
- **Notes:** The remaining Part 2 discussion repeats requirements already documented from Part 1.
- **Responsible:** TBD

---

# Day 4

**Stories:** 40

## CUBE-PH5-D4-001
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Delivery Ticket Management
- **Parent Task:** Delivery Data Continuity
- **Task Name:** Carry Quote Information Into Delivery Tickets
- **User Story:** As a Fulfillment Representative, I want relevant quote and order information carried into the delivery ticket so that I can verify the details and schedule the delivery without re-entering existing information.
- **Description:** When a quote request becomes a sale, the delivery ticket should retain the applicable order details, including the requested delivery date, service address, placement instructions, onsite contact information, product details, and project length. The representative verifies this information and confirms current availability and rates with the provider before scheduling.
- **Acceptance Criteria:** 1. The delivery ticket identifies that the quote request has become a sale, 2. The requested delivery date is displayed on the delivery ticket, 3. The service address, placement instructions, and onsite contact information are available, 4. The applicable product details and project length are displayed, 5. The representative can verify whether any order information has changed, 6. The representative can confirm the provider’s current availability and rates before scheduling.
- **Timestamp:** Day 4, Part 1 [00:53 - 04:37]
- **Mockups:** NO MOCKUP
- **Notes:** Delivery details should carry forward from the quote request when available, but the Fulfillment Representative must still verify the order information and reconfirm availability and rates with the provider. The screenshot shows product pricing and vendor-rate information, not the delivery-ticket view.
- **Responsible:** TBD

## CUBE-PH5-D4-002
- **Group:** Fulfillment Operations
- **Category:** Workflow
- **Epic:** Provider Coordination
- **Parent Task:** Initial Provider Contact and Reconfirmation
- **Task Name:** Require Provider Contact Before Working New Tickets
- **User Story:** As a Fulfillment Representative, I want to contact the service provider before processing each new ticket so that I can confirm current information in real time before proceeding.
- **Description:** Fulfillment Representatives contact the service provider first when working a new ticket because calling provides immediate information and avoids waiting for an email response. If the provider is designated as email-only, the representative follows that communication requirement instead.
- **Acceptance Criteria:** 1. The ticket displays the assigned or preselected service provider, 2. The representative can access the provider information needed to initiate contact, 3. The representative contacts the provider before proceeding with the ticket, 4. Providers designated as email-only are handled through email instead of a call, 5. Current availability and applicable rates can be confirmed during the contact, 6. The contact outcome can be documented on the ticket.
- **Timestamp:** Day 4, Part 1 [05:22 - 07:15]
- **Notes:** Calling the provider first is the standard Fulfillment process because it provides information in real time. Email is used when the provider specifically requires email-only communication.
- **Responsible:** TBD

## CUBE-PH5-D4-003
- **Group:** Fulfillment Operations
- **Category:** Workflow
- **Epic:** Delivery Ticket Management
- **Parent Task:** Changed Rate Requotation
- **Task Name:** Update Hauler Quotes When Delivery Rates Change
- **User Story:** As a Fulfillment Representative, I want to create and submit an updated hauler quote when the provider confirms different rates so that the product page reflects the actual vendor costs and resulting margins.
- **Description:** If the provider confirms that a previously quoted rate has changed, the Fulfillment Representative creates a new hauler quote with the corrected vendor rates, selects it as the chosen quote, and sends it to the product page. The updated costs and resulting margins are then reviewed before proceeding.
- **Acceptance Criteria:** 1. The representative can create a new hauler quote when a confirmed provider rate differs from the existing rate, 2. The updated quote identifies the applicable provider, 3. The corrected standard, delivery, removal, or other applicable vendor rates can be entered, 4. The updated quote can be selected as the chosen quote, 5. The chosen quote can be sent to the product page, 6. The product page displays the updated vendor rates and recalculated margins.
- **Timestamp:** Day 4, Part 1 [13:56 - 15:19]
- **Notes:** The screenshot shows the Vendor Rates, Suggested Price, and Margins sections of the product page after rate information is applied. The representative must review the resulting margin before continuing with the order.
- **Responsible:** TBD

## CUBE-PH5-D4-004
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Delivery Ticket Management
- **Parent Task:** Combined Quote and Delivery Processing
- **Task Name:** Process Quote and Delivery Work in One Ticket
- **User Story:** As a Fulfillment Representative, I want to create hauler quotes and confirm scheduling within a delivery ticket when no quote already exists so that a guaranteed sale can be quoted and scheduled through one workflow.
- **Description:** When a guaranteed sale reaches Fulfillment without a completed hauler quote, the representative uses the delivery ticket to obtain provider pricing, add and select a hauler quote, send the selected pricing to the product page, and confirm the delivery schedule.
- **Acceptance Criteria:** 1. The delivery ticket displays the requested delivery date and time, 2. The representative can add a hauler quote when no quote records exist, 3. Each quote can include the provider, contact, applicable rates, and confirmed availability, 4. The representative can identify the chosen hauler quote, 5. The chosen hauler pricing can be sent to the product page, 6. The confirmed delivery date and time can be recorded before the ticket is completed.
- **Timestamp:** Day 4, Part 1 [15:24 - 17:19]
- **Notes:** This workflow applies when the customer has committed to the order but provider pricing has not yet been completed. The ticket remains a delivery ticket while supporting the quoting steps needed before scheduling.
- **Responsible:** TBD

## CUBE-PH5-D4-005
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Pricing and Margin Review
- **Parent Task:** Hauler Quote Margin Comparison
- **Task Name:** Display Margins Against Customer and Statistical Pricing
- **User Story:** As a Fulfillment Representative, I want margins displayed while comparing hauler quotes so that I can select the best available provider pricing against the applicable customer or statistical price.
- **Description:** Fulfillment works backward from the customer or statistical price and needs the margin displayed as hauler quotes are added, including cases where the statistical price and available provider price result in low or negative margin.
- **Acceptance Criteria:** 1. The applicable statistical price is visible, 2. The current customer price is available when it exists, 3. Each hauler quote displays its resulting margin, 4. Multiple hauler quotes can be compared, 5. Low or negative margin is identifiable, 6. The selected quote and its margin remain available on the ticket or product context.
- **Timestamp:** Day 4, Part 1 [17:19 - 20:38]
- **Mockups:** NO MOCKUP
- **Notes:** Fulfillment is responsible for obtaining the best provider price; later customer-price changes belong to Sales.
- **Responsible:** TBD

## CUBE-PH5-D4-006
- **Group:** Fulfillment Operations
- **Category:** Business Rule
- **Epic:** Quote Request Management
- **Parent Task:** Repeat Quote Request Prevention
- **Task Name:** Prevent Unsupported Repeat Quote Requests
- **User Story:** As a Fulfillment Quality Coordinator, I want unsupported repeat quote requests prevented after Fulfillment has already provided a quote so that representatives are not asked to repeat completed pricing work.
- **Description:** Once Fulfillment has completed a quote request and a quote has been provided, the system should prevent another quote request for the same pricing need. Legitimate quote requests must remain distinguishable through reasons such as rural location, multiple products, high quantity, or a product not covered by the pricing tool.
- **Acceptance Criteria:** 1. The system identifies when Fulfillment has completed a quote request, 2. The system identifies when a quote has already been provided, 3. Another unsupported quote request for the same pricing need cannot be submitted, 4. The existing quote remains accessible for reference, 5. Valid categorized quote-request reasons remain available when applicable, 6. A ticket non-approval Multi request reason can document that the request was rejected because a quote was already provided.
- **Timestamp:** Day 4, Part 1 [26:01 - 31:16]
- **Mockups:** NO MOCKUP
- **Notes:** The requirement addresses repeated requests caused by a customer rejecting an already-provided price. Sales training and procedures are still required because the system can prevent duplicate work but cannot fully control how pricing is communicated to customers.
- **Responsible:** TBD

## CUBE-PH5-D4-007
- **Group:** Fulfillment Operations
- **Category:** Automation
- **Epic:** Pricing and Margin Review
- **Parent Task:** Exhausted-Effort Margin Escalation
- **Task Name:** Escalate Low and Negative Margin After Required Quotes
- **User Story:** As a Fulfillment Quality Coordinator, I want low- and negative-margin tickets automatically escalated after the required number of hauler quotes is collected so that a Fulfillment lead can verify the completed effort before Sales is notified.
- **Description:** When a ticket remains at low margin after at least three hauler quotes, or at negative margin after at least five hauler quotes, it should be routed to a Fulfillment lead. After the lead confirms that the required quoting effort was completed, the system notifies Sales using the information already recorded on the ticket.
- **Acceptance Criteria:** 1. The system identifies when a ticket has low or negative margin, 2. A low-margin ticket becomes eligible for escalation after at least three hauler quotes are recorded, 3. A negative-margin ticket becomes eligible for escalation after at least five hauler quotes are recorded, 4. The eligible ticket is routed to a Fulfillment lead for review, 5. The Fulfillment lead can confirm that the required quoting effort was completed, 6. Lead confirmation triggers a notification to Sales using the existing ticket and quote information.
- **Timestamp:** Day 4, Part 1 [31:39 - 41:29]
- **Mockups:** NO MOCKUP
- **Notes:** Fulfillment is responsible for obtaining the best available provider price and completing the required quoting effort. Sales is responsible for deciding how to address the resulting customer price or margin. The automated notification would replace the manually prepared low-margin approval email.
- **Responsible:** TBD

## CUBE-PH5-D4-008
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Purchase Order Management
- **Parent Task:** PO Not-to-Exceed Capture
- **Task Name:** Capture the Purchase Order Not-to-Exceed Amount
- **User Story:** As a Fulfillment Representative, I want the purchase order’s not-to-exceed amount captured as a point-in-time value so that the maximum payment agreed with the provider is preserved.
- **Description:** When scheduling service, the Fulfillment Representative records the maximum amount ZTERS agreed to pay the provider and includes it in the purchase-order communication. The amount normally corresponds to the applicable hauler charge but may differ when a provider requires a deposit.
- **Acceptance Criteria:** 1. A PO Not to Exceed field is available in the delivery workflow, 2. The field captures the maximum amount agreed with the provider, 3. The amount can be based on the applicable hauler charge, 4. The representative can enter a different amount when a deposit changes the payment requirement, 5. The recorded amount is included in the purchase-order communication, 6. The amount is preserved historically even if the product-page rates are later updated.
- **Timestamp:** Day 4, Part 1 [43:18 - 44:21; 58:22 - 1:01:20]
- **Notes:** The not-to-exceed amount normally matches the applicable hauler charge, but it cannot always be copied automatically because provider deposits may cause the values to differ.
- **Responsible:** TBD

## CUBE-PH5-D4-009
- **Group:** Fulfillment Operations
- **Category:** Usability
- **Epic:** Delivery Ticket Management
- **Parent Task:** Delivery Availability and Cutoff Definitions
- **Task Name:** Clarify Delivery, Availability, and Cutoff Fields
- **User Story:** As a Fulfillment Representative, I want clearly differentiated delivery, availability, and cutoff fields so that I do not enter the same date repeatedly or interpret fields inconsistently.
- **Description:** The workshop identified conflicting interpretations of confirmed availability. The proposed data distinguishes the actual confirmed delivery date, the earliest date the provider is available, and a job-specific cutoff time that may differ from the provider's standard schedule.
- **Acceptance Criteria:** 1. The confirmed delivery date has a clear definition, 2. Earliest provider availability can be captured separately when it differs, 3. A job-specific cutoff time can be captured, 4. The job-specific cutoff can differ from the provider's standard cutoff, 5. Fields do not require the same value to be entered redundantly, 6. Each field includes a clear explanation of when and why it is used.
- **Timestamp:** Day 4, Part 1 [44:21 - 50:00]
- **Notes:** The exact labels were still being discussed, but separate delivery, earliest-availability, and cutoff concepts were explicitly proposed.
- **Responsible:** TBD

## CUBE-PH5-D4-010
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Ticket Data Management
- **Parent Task:** Structured Fulfillment Activity Capture
- **Task Name:** Replace Repeated Notes With Structured Ticket Data
- **User Story:** As a Fulfillment Representative, I want ticket actions and outcomes captured through structured fields and an activity history so that I do not have to repeat information already recorded on the ticket in narrative notes.
- **Description:** Fulfillment tickets should use dedicated fields, checkboxes, and activity records to capture provider details, confirmed dates, contact methods, status changes, and other standard information. Free-form notes should be used only when the information does not have an appropriate structured field.
- **Acceptance Criteria:** 1. Standard ticket information is captured through dedicated fields or checkboxes, 2. Information already displayed on the ticket does not need to be repeated in notes, 3. Changes to structured ticket fields are recorded in the activity history, 4. The history identifies what changed and when it changed, 5. The history identifies the user responsible for each change, 6. Free-form notes remain available for information that cannot be captured through an existing field.
- **Timestamp:** Day 4, Part 1 [51:00 - 55:49]
- **Mockups:** NO MOCKUP
- **Notes:** The objective is to reduce repetitive ticket notes and processing time while preserving a complete record of ticket activity. Provider names, confirmed dates, and other information already stored in structured fields should not be manually copied into notes.
- **Responsible:** TBD

## CUBE-PH5-D4-011
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Ticket Data Management
- **Parent Task:** Provider Confirmation Reference
- **Task Name:** Add Confirmation and Reference Number Fields
- **User Story:** As a Fulfillment Representative, I want a confirmation or reference number field on the ticket so that provider identifiers can be recorded without placing them in free-form notes.
- **Description:** Providers do not always issue a number, but when one is supplied the representative needs a dedicated place to capture a confirmation number, reference number, or equivalent identifier.
- **Acceptance Criteria:** 1. The ticket includes a confirmation or reference number field, 2. The field accepts a provider-supplied identifier, 3. The field is available without requiring a narrative note, 4. The field can remain empty when no number is provided, 5. The recorded number remains visible after completion, 6. The number is associated with the applicable ticket.
- **Timestamp:** Day 4, Part 1 [56:57 - 57:54]
- **Mockups:** NO MOCKUP
- **Notes:** The field list was to be finalized by the Fulfillment Quality Coordinator.
- **Responsible:** TBD

## CUBE-PH5-D4-012
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Vendor Payment Processing
- **Parent Task:** Ticket-Level Receipt and Payment Capture
- **Task Name:** Capture Vendor Payment Details and Receipt Location
- **User Story:** As a Fulfillment Representative, I want to record vendor payment information and attach receipts directly to the Fulfillment ticket so that Accounting can locate the supporting documentation.
- **Description:** The workflow records the vendor payment amount and whether the receipt is attached to the document page, attached to the ticket, not provided, or emailed to the invoices mailbox. Ticket-level drag and drop was requested.
- **Acceptance Criteria:** 1. The vendor payment amount can be entered, 2. A receipt can be attached directly to the Fulfillment ticket, 3. The receipt can be added using drag and drop, 4. The representative can indicate that the receipt is on the document page, 5. The representative can indicate that no receipt was provided, 6. The representative can indicate that the receipt was emailed to the invoices mailbox.
- **Timestamp:** Day 4, Part 1 [1:01:20 - 1:03:23]
- **Mockups:** NO MOCKUP
- **Notes:** The receipt status is intended to tell Accounting where to look during invoice review.
- **Responsible:** TBD

## CUBE-PH5-D4-013
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Scheduled Service Changes
- **Parent Task:** Service Change Date and Scope Capture
- **Task Name:** Identify the Service and Dates Being Changed
- **User Story:** As a Fulfillment Representative, I want scheduled-service-change tickets to show the original date, requested new date, confirmed date, and affected service so that I can verify the correct change with the provider.
- **Description:** A scheduled service change may apply to delivery, removal, a swap, or another pre-scheduled service. The request needs structured original and new dates plus enough information to identify which service is changing.
- **Acceptance Criteria:** 1. The original scheduled date is captured, 2. The customer's requested new date is captured, 3. The provider's confirmed date is captured separately, 4. The affected service can be identified, 5. Multiple pre-scheduled services can be distinguished, 6. The responsibility for entering requested and confirmed values is clear.
- **Timestamp:** Day 4, Part 1 [1:04:11 - 1:12:47]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript noted that notes may still identify a specific service when a clean structured selection is not available.
- **Responsible:** TBD

## CUBE-PH5-D4-014
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Scheduled Service Changes
- **Parent Task:** Reschedule Cost and PO Update
- **Task Name:** Document Additional Rescheduling Costs
- **User Story:** As a Fulfillment Representative, I want to record additional costs caused by a schedule change and issue an updated purchase order so that the provider and Sales have the corrected dates and fees.
- **Description:** When a provider charges because a driver is already en route or notice was insufficient, the representative records the additional cost, confirms the new date, and sends an updated purchase order with the corrected scheduling information.
- **Acceptance Criteria:** 1. The provider's confirmed rescheduled date is recorded, 2. An additional rescheduling cost can be entered, 3. A zero or blank cost is distinguishable from an entered fee, 4. The updated purchase order contains the corrected dates, 5. The provider contact can be recorded, 6. The completed ticket retains the confirmed date and additional cost.
- **Timestamp:** Day 4, Part 1 [1:17:02 - 1:19:15]
- **Mockups:** NO MOCKUP
- **Notes:** The example used a $50 charge when the driver was already en route.
- **Responsible:** TBD

## CUBE-PH5-D4-015
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Service Issue Management
- **Parent Task:** Service Issue Classification
- **Task Name:** Classify Provider-Side Service Issues
- **User Story:** As a Fulfillment Representative, I want to classify service issues by the type of provider-side problem so that customer complaints can be handled under the appropriate issue category.
- **Description:** The service issue ticket applies across product types and includes equipment damage, product quality, service quality, missed scheduled service, site damage, and Other for issues not covered by the predefined list.
- **Acceptance Criteria:** 1. Equipment damage is available as an issue type, 2. Product quality is available as an issue type, 3. Service quality is available as an issue type, 4. Missed scheduled service is available as an issue type, 5. Site damage is available as an issue type, 6. Other is available for uncategorized provider-side issues.
- **Timestamp:** Day 4, Part 1 [1:20:35 - 1:23:36]
- **Mockups:** NO MOCKUP
- **Notes:** The ticket was described as the catch-all for complaints about something outside the expected provider service.
- **Responsible:** TBD

## CUBE-PH5-D4-016
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Service Issue Management
- **Parent Task:** Issue Responsibility and Resolution
- **Task Name:** Assign Responsibility After the Issue Is Investigated
- **User Story:** As a Fulfillment Representative, I want to assign issue responsibility and resolution only after the investigation is complete so that the final record identifies whether the customer, provider, or ZTERS caused the issue.
- **Description:** Responsibility remains unassigned while the representative verifies information with the provider and Sales verifies it with the customer. The ticket is completed only after the cause and resolution are known.
- **Acceptance Criteria:** 1. Issue responsibility can remain blank during investigation, 2. Customer responsibility can be selected, 3. Provider responsibility can be selected, 4. ZTERS responsibility can be selected, 5. The issue-resolution status is recorded after an agreement or outcome is reached, 6. The ticket cannot be treated as fully resolved before the required information is collected.
- **Timestamp:** Day 4, Part 1 [1:23:36 - 1:31:51]
- **Mockups:** NO MOCKUP
- **Notes:** The examples included missing site hours, a locked gate, provider failure to record hours, and ZTERS failure to capture customer-provided hours.
- **Responsible:** TBD

## CUBE-PH5-D4-017
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Service Issue Management
- **Parent Task:** Issue Evidence Attachments
- **Task Name:** Attach Photos and Service Logs to Issue Tickets
- **User Story:** As a Fulfillment Representative, I want to attach issue evidence directly to the Fulfillment ticket so that photos and service logs remain with the investigation without extra product-page steps.
- **Description:** The representative may request a service log, a photo of a blocked unit, or other evidence from the provider. The workshop requested ticket-level drag-and-drop attachments for these materials.
- **Acceptance Criteria:** 1. Photos can be attached to the service issue ticket, 2. Service logs can be attached to the service issue ticket, 3. Attachments support drag and drop, 4. The attachment is associated with the applicable issue, 5. Attached evidence is available while the ticket remains open, 6. The representative does not need to add a separate note merely to identify where the ticket attachment was stored.
- **Timestamp:** Day 4, Part 1 [1:23:36 - 1:26:31]
- **Mockups:** NO MOCKUP
- **Notes:** The same general ticket-attachment capability was also requested for receipts and diversion reports.
- **Responsible:** TBD

## CUBE-PH5-D4-018
- **Group:** Fulfillment Operations
- **Category:** Workflow
- **Epic:** Service Issue Management
- **Parent Task:** Cross-Team Issue Investigation
- **Task Name:** Keep Service Issues Open Through Sales and Provider Follow-Up
- **User Story:** As a Fulfillment Representative, I want an open service-issue workflow with two-way notifications between Sales and Fulfillment so that all customer and provider facts are resolved before the ticket is closed.
- **Description:** The ticket remains open while Fulfillment communicates with the provider and Sales communicates with the customer. Updates pass back and forth through notifications and a history log until responsibility and resolution can be finalized.
- **Acceptance Criteria:** 1. The representative can notify Sales that customer action is required, 2. Sales updates can notify the assigned Fulfillment representative, 3. The ticket remains open during the exchange, 4. The update history preserves the conversation and actions, 5. Confirmed site hours or other structured data are visible to both sides, 6. Responsibility and resolution are completed before the ticket is fulfilled and closed.
- **Timestamp:** Day 4, Part 1 [1:27:21 - 1:33:15]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop characterized this as a linear sequence of provider verification, customer verification, follow-up, responsibility assignment, and closure.
- **Responsible:** TBD

## CUBE-PH5-D4-019
- **Group:** Fulfillment Operations
- **Category:** Automation
- **Epic:** Ticket Assignment
- **Parent Task:** Quote-to-Delivery Representative Continuity
- **Task Name:** Assign Delivery Tickets to the Representative Who Completed the Quote
- **User Story:** As a Fulfillment Representative, I want the delivery ticket automatically assigned to the representative who completed the related quote request so that the same person can continue the order through scheduling.
- **Description:** By process, the representative who works the quote request also schedules the corresponding delivery, regardless of whether the customer proceeds immediately or later. Reassignment remains possible for exceptions.
- **Acceptance Criteria:** 1. The system identifies the representative assigned to the related quote request, 2. A corresponding delivery ticket is assigned to that representative, 3. The assignment applies even when the delivery request arrives later, 4. The quote and delivery remain linked to the same order context, 5. An authorized user can reassign the delivery when necessary, 6. The final assignment history is retained.
- **Timestamp:** Day 4, Part 1 [1:34:08 - 1:38:09]
- **Mockups:** NO MOCKUP
- **Notes:** Out-of-office coverage was identified as the main exception to the default assignment.
- **Responsible:** TBD

## CUBE-PH5-D4-020
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Ticket Assignment
- **Parent Task:** Backup Fulfillment Representative Tracking
- **Task Name:** Identify a Backup Representative on Assigned Tickets
- **User Story:** As a Fulfillment Representative, I want a backup Fulfillment representative recorded on a ticket so that the person actually covering and working the ticket is visible alongside the primary assignee.
- **Description:** As a low-complexity first step, the workshop proposed a backup representative dropdown. Automated out-of-office rerouting was discussed separately and would require maintained coverage dates and pairings.
- **Acceptance Criteria:** 1. A backup Fulfillment representative can be selected, 2. The primary Fulfillment representative remains identified, 3. The backup representative is visible on the ticket, 4. The record shows who actually performed ticket work, 5. The backup can work the ticket without removing the primary assignment, 6. Assignment changes are retained in ticket history.
- **Timestamp:** Day 4, Part 1 [1:38:09 - 1:44:50]
- **Mockups:** NO MOCKUP
- **Notes:** This story intentionally covers the proposed backup field, not the uncommitted automated out-of-office rerouting system.
- **Responsible:** TBD

## CUBE-PH5-D4-021
- **Group:** Fulfillment Operations
- **Category:** Usability
- **Epic:** Service Needed Tickets
- **Parent Task:** Product-Specific Service Type Filtering
- **Task Name:** Filter Service Needed Options by Product
- **User Story:** As a Fulfillment Representative, I want service-needed types filtered by the selected product so that I only see relevant options instead of one combined list for every product.
- **Description:** Service-needed tickets cover additional or changed services beyond standard scheduled changes, including tip-over service, relocation, site checks, accessory changes, and partial removals. Cube can pre-filter the options based on product type.
- **Acceptance Criteria:** 1. The selected product determines the available service-needed types, 2. Portable-toilet options are limited to applicable portable-toilet services, 3. Product-inapplicable choices are hidden, 4. Additional service types such as relocation or site check remain available when applicable, 5. Partial removal remains available for supported products, 6. The selected service type is stored on the ticket.
- **Timestamp:** Day 4, Part 1 [2:08:56 - 2:11:08]
- **Mockups:** NO MOCKUP
- **Notes:** The current QuickBase form combines service-type tables because it cannot pre-filter them as proposed for Cube.
- **Responsible:** TBD

## CUBE-PH5-D4-022
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Service Needed Tickets
- **Parent Task:** Partial Removal Details
- **Task Name:** Capture Partial Removal Quantity and Related Service Details
- **User Story:** As a Fulfillment Representative, I want structured partial-removal details so that reduced quantities, accessories, service frequency, dates, and costs do not have to be explained only in notes.
- **Description:** A partial removal may reduce product quantity or remove accessories. The ticket captures the quantity change, applicable accessories or frequency, requested and confirmed dates, and the provider's extra or removal cost.
- **Acceptance Criteria:** 1. The partial-removal quantity can be entered, 2. The ticket can identify a reduction from the original quantity to the remaining quantity, 3. Applicable accessories can be identified, 4. Service frequency is available when relevant, 5. Requested and confirmed removal dates can be recorded, 6. The applicable extra or removal cost can be recorded.
- **Timestamp:** Day 4, Part 1 [2:11:08 - 2:17:55]
- **Mockups:** NO MOCKUP
- **Notes:** The Account Manager still manually updates the product quantity and creates the corresponding service record after Fulfillment completes the ticket.
- **Responsible:** TBD

## CUBE-PH5-D4-023
- **Group:** Fulfillment Operations
- **Category:** Audit
- **Epic:** Service Needed Tickets
- **Parent Task:** Product Quantity Change History
- **Task Name:** Audit Product Quantity Changes
- **User Story:** As a Fulfillment Representative, I want product quantity changes recorded in an audit log so that the prior quantity, new quantity, time, and user are traceable.
- **Description:** Cube is expected to record changes to the product quantity field automatically, improving on the indirect history currently inferred from old service tickets, line items, and invoices.
- **Acceptance Criteria:** 1. The audit log records the original quantity, 2. The audit log records the new quantity, 3. The date and time of the change are recorded, 4. The user who changed the quantity is recorded, 5. Multiple quantity changes remain available historically, 6. The history is accessible from the applicable product or record context.
- **Timestamp:** Day 4, Part 1 [2:14:22 - 2:16:32]
- **Mockups:** NO MOCKUP
- **Notes:** Automatic updating of the product quantity from the Fulfillment ticket was explicitly considered unnecessary; the audit applies when the product field is changed.
- **Responsible:** TBD

## CUBE-PH5-D4-024
- **Group:** Fulfillment Operations
- **Category:** Business Rule
- **Epic:** Cancellation Tickets
- **Parent Task:** Cancellation Reason Entry Responsibility
- **Task Name:** Require the Cancellation Reason From the Ticket Creator Only
- **User Story:** As a Fulfillment Representative, I want the cancellation reason required when the cancellation ticket is created but not when Fulfillment edits it so that I can process the ticket without rewriting the requester's explanation.
- **Description:** The cancellation reason is required from the user requesting cancellation. Fulfillment should be able to edit and complete its portion without being required to change that original reason.
- **Acceptance Criteria:** 1. A cancellation reason is required when the cancellation ticket is created, 2. The original reason remains visible to Fulfillment, 3. Fulfillment can edit its assigned ticket fields without rewriting the reason, 4. The original reason is preserved, 5. The ticket cannot be created without a cancellation reason, 6. Fulfillment completion does not make the original reason a new required entry.
- **Timestamp:** Day 4, Part 1 [2:18:07 - 2:19:39]
- **Mockups:** NO MOCKUP
- **Notes:** The reason remains a free-form text field because cancellation causes can vary.
- **Responsible:** TBD

## CUBE-PH5-D4-025
- **Group:** Fulfillment Operations
- **Category:** Business Rule
- **Epic:** Cancellation Tickets
- **Parent Task:** Required Cancellation Cost
- **Task Name:** Require Cancellation Cost Including Zero
- **User Story:** As a Fulfillment Representative, I want the cancellation cost required on my portion of the ticket so that every cancellation documents whether the provider charged a fee.
- **Description:** Fulfillment contacts the provider to determine the cancellation charge and records the amount. The field is completed even when the provider's cancellation cost is zero.
- **Acceptance Criteria:** 1. A cancellation-cost field is available to Fulfillment, 2. The field is required before Fulfillment completes the ticket, 3. A positive provider cancellation fee can be entered, 4. Zero can be entered when no fee applies, 5. The recorded cost is visible to Sales, 6. The cost remains associated with the cancellation record.
- **Timestamp:** Day 4, Part 1 [2:19:39 - 2:20:38]
- **Mockups:** NO MOCKUP
- **Notes:** The transcript example involved a provider charging after equipment had already been loaded or dispatched.
- **Responsible:** TBD

## CUBE-PH5-D4-026
- **Group:** Fulfillment Operations
- **Category:** Reporting
- **Epic:** Cancellation Tickets
- **Parent Task:** Cancellation Processing Time
- **Task Name:** Track Cancellation Time and Duration
- **User Story:** As a Fulfillment Quality Coordinator, I want cancellation submission time and processing duration tracked so that I can measure how long cancellation tickets take to complete.
- **Description:** Cancellation tickets include time tracking specific to the cancellation process: when the cancellation was submitted and how long it took to complete.
- **Acceptance Criteria:** 1. The cancellation submission time is recorded, 2. The cancellation completion time is identifiable, 3. Cancellation duration is calculated or stored, 4. The fields apply specifically to cancellation tickets, 5. The timing values remain available after completion, 6. Cancellation timing can be used in reporting.
- **Timestamp:** Day 4, Part 1 [2:20:38 - 2:21:01]
- **Mockups:** NO MOCKUP
- **Notes:** These were described as additional time fields unique to cancellation tickets.
- **Responsible:** TBD

## CUBE-PH5-D4-027
- **Group:** Fulfillment Operations
- **Category:** Reporting
- **Epic:** Cancellation Tickets
- **Parent Task:** Cancellation Cause Reporting
- **Task Name:** Log and Report Credit-Card-Decline Cancellations
- **User Story:** As a Fulfillment Quality Coordinator, I want cancellation causes such as credit-card decline logged and reportable so that ZTERS-initiated cancellations can be distinguished from customer-requested cancellations.
- **Description:** Credit-card decline can lead to a cancellation after a provider has already scheduled the order. The workshop stated that this activity should be audited and reportable, including the cancellation reason and resulting provider cost.
- **Acceptance Criteria:** 1. Credit-card decline can be recorded as the cancellation reason, 2. Customer-requested and ZTERS-initiated cancellations can be distinguished, 3. The cancellation cost is retained with the reason, 4. Cancellation records can be included in reports, 5. The applicable ticket and customer context remain linked, 6. The record remains available even when the cancellation cost cannot be recovered from the customer.
- **Timestamp:** Day 4, Part 1 [2:22:59 - 2:32:33]
- **Mockups:** NO MOCKUP
- **Notes:** A valid card pre-authorization does not guarantee that the later full transaction will succeed.
- **Responsible:** TBD

## CUBE-PH5-D4-028
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** ETA Tickets
- **Parent Task:** ETA Service Scope and Time Range
- **Task Name:** Capture ETA Type, Confirmed Date, and Time Range
- **User Story:** As a Fulfillment Representative, I want ETA tickets to identify the applicable service and capture a confirmed time range so that I can communicate when the provider expects to arrive.
- **Description:** ETA requests may concern delivery, removal, an additional service, or regular scheduled service. A single confirmed date is used, while the provider may supply a time window rather than an exact time.
- **Acceptance Criteria:** 1. Delivery is available as an ETA type, 2. Removal is available as an ETA type, 3. Additional service is available as an ETA type, 4. Regular scheduled service is available as an ETA type, 5. The confirmed service date is recorded as a single date, 6. The confirmed service time supports a start-to-end range.
- **Timestamp:** Day 4, Part 1 [2:32:40 - 2:41:40]
- **Mockups:** NO MOCKUP
- **Notes:** If the provider moves the service to another day, Fulfillment records the new confirmed date and completes the ETA ticket; Sales handles downstream billing and customer impacts.
- **Responsible:** TBD

## CUBE-PH5-D4-029
- **Group:** Fulfillment Operations
- **Category:** Usability
- **Epic:** Ticket Scheduling Fields
- **Parent Task:** Conditional Requested Service Time
- **Task Name:** Show Requested Time Fields Only When the Customer Requests a Time
- **User Story:** As a Fulfillment Representative, I want requested service-time fields shown only when the customer asks for a specific time so that routine tickets are not cluttered with unused fields.
- **Description:** Specific requested times are less common outside ETA work but are relevant for locations such as schools and military or naval bases and may result in an additional provider fee.
- **Acceptance Criteria:** 1. A control indicates whether the customer requested a specific time, 2. Requested-time fields are hidden when no time was requested, 3. Requested-time fields appear when the control is selected, 4. The requested time can be recorded, 5. The field remains available for location-specific timing requirements, 6. Any separately confirmed provider time or range remains distinguishable from the customer request.
- **Timestamp:** Day 4, Part 1 [2:35:30 - 2:38:01]
- **Mockups:** NO MOCKUP
- **Notes:** The discussion proposed a checkbox that reveals the requested-time fields.
- **Responsible:** TBD

## CUBE-PH5-D4-030
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Removal Tickets
- **Parent Task:** Removal Reason and Non-Negotiable Terms
- **Task Name:** Separate Removal Cause From Required Date and Time Terms
- **User Story:** As a Fulfillment Representative, I want removal reasons separated from non-negotiable removal terms so that I can distinguish why removal is requested from when it must occur.
- **Description:** Removal reasons include non-payment, dissatisfaction with the provider, provider change, and customer request. Non-negotiable terms specifically indicate that the requested removal date or time cannot be exceeded.
- **Acceptance Criteria:** 1. Non-payment is available as a removal reason, 2. Unsatisfied with provider is available as a removal reason, 3. Change provider is available as a removal reason, 4. Customer requested is available as a removal reason, 5. Non-negotiable removal terms are captured separately, 6. Required removal dates or latest acceptable times can be recorded when the non-negotiable control applies.
- **Timestamp:** Day 4, Part 1 [2:41:40 - 2:48:00]
- **Mockups:** NO MOCKUP
- **Notes:** Military bases, schools, and pump-out timing were given as examples of non-negotiable removal conditions.
- **Responsible:** TBD

## CUBE-PH5-D4-031
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Removal Tickets
- **Parent Task:** Off-Route Removal Cost
- **Task Name:** Capture Additional Removal Costs
- **User Story:** As a Fulfillment Representative, I want an additional removal-cost field so that off-route or date-specific pickup charges are documented without replacing the other product rates.
- **Description:** A provider may charge for removal outside its normal service day, especially when the customer requires a specific date or time. Creating a removal-only hauler quote would overwrite or blank other rates, so a dedicated field was requested.
- **Acceptance Criteria:** 1. An additional removal-cost field is available on the removal ticket, 2. Off-route pickup fees can be entered, 3. Date-specific removal fees can be entered, 4. The cost does not replace unrelated product rates, 5. The cost remains visible to Sales, 6. The cost is retained with the completed removal ticket.
- **Timestamp:** Day 4, Part 1 [2:43:06 - 2:45:37]
- **Mockups:** NO MOCKUP
- **Notes:** This was identified as a low-complexity addition to the removal workflow.
- **Responsible:** TBD

## CUBE-PH5-D4-032
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Removal Tickets
- **Parent Task:** Removal Billing Cutoff Review
- **Task Name:** Capture Provider Cycle End and Billing Stop Dates
- **User Story:** As a Fulfillment Representative, I want the provider cycle end date and billing stop date recorded separately from the confirmed removal date so that billing and proration consequences can be evaluated.
- **Description:** The provider may remove equipment after the requested date and may stop billing on a different date. The representative needs these dates to determine whether a new billing cycle starts and whether the provider will prorate.
- **Acceptance Criteria:** 1. The provider cycle end date is recorded, 2. The confirmed removal date is recorded separately, 3. The billing stop date is recorded separately, 4. Provider proration information can be considered with the dates, 5. A billing stop date that enters a new cycle is visible, 6. The captured dates remain available for later invoice and billing review.
- **Timestamp:** Day 4, Part 1 [2:48:00 - 2:54:50]
- **Mockups:** NO MOCKUP
- **Notes:** Roll-off providers may continue charging rental days until actual removal; negotiation does not always change that outcome.
- **Responsible:** TBD

## CUBE-PH5-D4-033
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Information Request Tickets
- **Parent Task:** Provider Information Request Types
- **Task Name:** Use Information Requests for Provider and Site Verification
- **User Story:** As a Fulfillment Representative, I want information-request tickets categorized by the information needed from the provider so that updates and verification work are tracked consistently.
- **Description:** Information requests can relay changed placement instructions, onsite contacts, or site hours; verify service days; investigate undocumented activity; request restricted-item information; request diversion reports; or use Other.
- **Acceptance Criteria:** 1. Updated placement instructions can be sent through an information request, 2. Updated onsite contact information can be sent, 3. Updated site hours can be sent, 4. Service days can be verified, 5. Undocumented activity can be investigated, 6. Other remains available for requests outside the listed types.
- **Timestamp:** Day 4, Part 1 [2:58:12 - 3:01:57]
- **Mockups:** NO MOCKUP
- **Notes:** Undocumented activity commonly becomes visible when an invoice contains a unit, haul, or removal that ZTERS did not record.
- **Responsible:** TBD

## CUBE-PH5-D4-034
- **Group:** Accounting and Fulfillment Integration
- **Category:** Automation
- **Epic:** Accounting Inquiry Follow-Up
- **Parent Task:** Accounting-Inquiry Fulfillment Ticket Creation
- **Task Name:** Create and Assign a Fulfillment Ticket From an Accounting Inquiry
- **User Story:** As a Fulfillment Representative, I want a Fulfillment ticket automatically created and assigned when an accounting inquiry requires Fulfillment action so that the investigation is not skipped and appears in my workload.
- **Description:** For undocumented activity or another FR action, the accounting inquiry should create a linked information-request Fulfillment ticket using the closest relevant service ticket and assign it to the Fulfillment representative responsible for the inquiry.
- **Acceptance Criteria:** 1. Marking an accounting inquiry as requiring Fulfillment action can initiate ticket creation, 2. A Fulfillment ticket is created without separate manual re-entry, 3. The new ticket is linked to the accounting inquiry, 4. The ticket is linked to the applicable product and closest relevant service ticket, 5. The ticket is assigned to the responsible Fulfillment representative, 6. Work performed on the inquiry is tracked through the Fulfillment ticket.
- **Timestamp:** Day 4, Part 1 [3:01:57 - 3:06:33]
- **Mockups:** NO MOCKUP
- **Notes:** The requested one-to-one relationship would also make accounting-inquiry workload visible to Fulfillment leads.
- **Responsible:** TBD

## CUBE-PH5-D4-035
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Information Request Tickets
- **Parent Task:** Restricted Item Cost Capture
- **Task Name:** Record Costs for Contaminated or Restricted Items
- **User Story:** As a Fulfillment Representative, I want additional restricted-item costs captured on an information-request ticket so that provider fees for changed or prohibited debris are communicated and retained.
- **Description:** When the customer asks about items such as mattresses, box springs, or air-conditioning units, Fulfillment confirms whether they are accepted and records any additional provider cost.
- **Acceptance Criteria:** 1. Contaminated or restricted items can be selected as the request type, 2. The item or changed debris information can be documented, 3. Provider acceptance can be recorded, 4. An additional restricted-item cost can be entered, 5. The cost is visible with the request outcome, 6. The completed ticket retains the item and cost information.
- **Timestamp:** Day 4, Part 1 [3:06:33 - 3:07:34]
- **Mockups:** NO MOCKUP
- **Notes:** The cost field was specifically requested because the current information-request ticket has no place for these fees.
- **Responsible:** TBD

## CUBE-PH5-D4-036
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Diversion Report Management
- **Parent Task:** Advance Diversion Report Requirement and Cost
- **Task Name:** Capture Diversion Report Requirements Before Delivery
- **User Story:** As a Fulfillment Representative, I want diversion-report requirements and provider fees captured before delivery so that reports can be requested in time and their recurring cost can be reflected.
- **Description:** Diversion reports may be required for government or other projects and must be requested from the provider before delivery. The product information should contain a required yes-or-no selection, the ticket should support report attachments, and any per-report charge must be documented.
- **Acceptance Criteria:** 1. The product record asks whether a diversion report is required, 2. The response is required before the applicable product information is saved, 3. The requirement carries into the quote or delivery context, 4. A diversion report can be requested from the provider before delivery, 5. Received reports can be attached to the ticket, 6. A per-report provider cost can be recorded.
- **Timestamp:** Day 4, Part 1 [3:07:34 - 3:14:39]
- **Mockups:** NO MOCKUP
- **Notes:** The same requirement must also be captured in the BDR call workflow because that workflow feeds the product page.
- **Responsible:** TBD

## CUBE-PH5-D4-037
- **Group:** Fulfillment Operations
- **Category:** Functional
- **Epic:** Service Level Optimization
- **Parent Task:** Front-Load Service Frequency Optimization
- **Task Name:** Process Front-Load Service Level Changes
- **User Story:** As a Fulfillment Representative, I want service-level-optimization tickets to capture front-load frequency changes so that service can be adjusted using ZSight fullness information.
- **Description:** Service level optimization is a front-load service-frequency change informed by ZSight camera statistics, including current fullness patterns, projected fullness after a change, and the risk of becoming overfull.
- **Acceptance Criteria:** 1. The ticket applies to front-load service-level changes, 2. The current service frequency is available, 3. A proposed service frequency can be recorded, 4. ZSight fullness information can support the request, 5. Projected fullness after the change can be considered, 6. Overfill risk associated with the change is available for review.
- **Timestamp:** Day 4, Part 1 [3:18:02 - 3:20:13]
- **Mockups:** NO MOCKUP
- **Notes:** The broader ZSight process was deferred for separate review because it does not follow the standard Fulfillment workflow.
- **Responsible:** TBD

## CUBE-PH5-D4-038
- **Group:** Fulfillment Operations
- **Category:** Reporting
- **Epic:** Fulfillment Queue
- **Parent Task:** Priority and Site-Based Queue Management
- **Task Name:** Prioritize and Group Unassigned Fulfillment Tickets
- **User Story:** As a Fulfillment Representative, I want the unassigned Fulfillment queue prioritized and grouped by site so that related tickets can be assigned together and the most important work is handled first.
- **Description:** The main Fulfillment queue is used by queue managers and representatives to assign unworked tickets. Priority considers factors such as next-day need and revenue, while site grouping supports assigning related tickets as a block.
- **Acceptance Criteria:** 1. Unassigned Fulfillment tickets appear in a shared queue, 2. Tickets are ordered by the calculated priority level, 3. Related tickets can be grouped by site, 4. A queue manager can assign tickets to representatives, 5. Representatives can self-assign permitted tickets, 6. Quote-request reasons such as expedited availability or product not covered remain visible.
- **Timestamp:** Day 4, Part 1 [3:21:31 - 3:23:41]
- **Mockups:** NO MOCKUP
- **Notes:** The queue was identified as a critical operational report for Fulfillment representatives and leads.
- **Responsible:** TBD

## CUBE-PH5-D4-039
- **Group:** Fulfillment Operations
- **Category:** Business Rule
- **Epic:** Fulfillment Queue
- **Parent Task:** Open Ticket Assignment Limit
- **Task Name:** Limit New Assignments When a Representative Has Too Many Open Tickets
- **User Story:** As a Fulfillment Quality Coordinator, I want a configurable maximum number of open tickets per representative so that users cannot continue taking easier work while existing assigned tickets remain unfinished.
- **Description:** The workshop selected an open-ticket count rule as the simpler control: when a representative's count reaches the defined limit, the user and queue manager cannot assign additional tickets to that representative.
- **Acceptance Criteria:** 1. The system counts each representative's open Fulfillment tickets, 2. A configurable maximum-open-ticket threshold is supported, 3. Self-assignment is blocked when the threshold is reached, 4. Queue-manager assignment is blocked when the threshold is reached, 5. Assignment becomes available again after the open count falls below the threshold, 6. The selected threshold applies consistently to the assignment workflow.
- **Timestamp:** Day 4, Part 1 [3:23:41 - 3:29:45]
- **Mockups:** NO MOCKUP
- **Notes:** The exact maximum was intentionally left for the Fulfillment team to determine offline.
- **Responsible:** TBD

## CUBE-PH5-D4-040
- **Group:** Fulfillment Operations
- **Category:** Reporting
- **Epic:** Fulfillment Performance Dashboard
- **Parent Task:** Performance and Aging Visualization
- **Task Name:** Visualize Workload, Aging, Assignment Source, and Inquiry Work
- **User Story:** As a Fulfillment Quality Coordinator, I want interactive workload dashboards with ticket-type, aging, assignment-source, and accounting-inquiry views so that I can assess productivity, identify stalled work, and drill into the underlying tickets.
- **Description:** The dashboard should distinguish open and closed work, compare ticket types with appropriate weighting, support team, user, and time filters, show whether tickets were self-assigned or assigned by a queue manager, group inactive tickets into aging buckets, allow drill-down, and display open accounting inquiries.
- **Acceptance Criteria:** 1. Open and closed ticket counts can be viewed separately by ticket type, 2. Dashboard filters support department or team, individual user, and time period, 3. Self-assigned tickets can be distinguished from queue-manager-assigned tickets, 4. Tickets are grouped into aging buckets based on time since last modification, 5. Chart segments and totals support drill-down to the underlying tickets, 6. Open accounting inquiries assigned to the current representative or relevant lead view are displayed.
- **Timestamp:** Day 4, Part 1 [3:31:06 - 3:58:46]
- **Mockups:** NO MOCKUP
- **Notes:** Ticket types were said to require different weights because an ETA and a quote request do not represent the same amount of work; the detailed weighting values were not finalized.
- **Responsible:** TBD

---

# Day 5

**Stories:** 18

## CUBE-PH5-D5-001
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Dashboard Summary
- **Task Name:** Display Open Work Counts
- **User Story:** As a Fulfillment Representative, I want to see counts of my open Fulfillment tickets, accounting inquiries, and tasks at the top of my dashboard so that I can immediately identify the work requiring my attention.
- **Description:** The Fulfillment dashboard displays summary counts for the representative’s open Fulfillment tickets, accounting inquiries, and tasks before the corresponding detailed reports.
- **Acceptance Criteria:** 1. The dashboard displays the number of open Fulfillment tickets, 2. The dashboard displays the number of open accounting inquiries, 3. The dashboard displays the number of open tasks, 4. The counts appear at the top of the dashboard before the detailed reports, 5. Each count reflects records associated with the logged-in Fulfillment Representative, 6. Each count provides one-click access to its corresponding records.
- **Timestamp:** Day 5, Part 1 [00:16 - 01:33]
- **Notes:** The detailed dashboard arrangement was not finalized during the workshop.
- **Responsible:** TBD

## CUBE-PH5-D5-002
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Performance Information
- **Task Name:** Display Year-to-Date Quality Score
- **User Story:** As a Fulfillment Representative, I want to see my year-to-date quality score on my dashboard so that I can monitor my quality performance alongside my operational work.
- **Description:** The Fulfillment dashboard displays the logged-in representative’s year-to-date quality score using the quality-review information recorded for that representative.
- **Acceptance Criteria:** 1. The dashboard displays a year-to-date quality score, 2. The score corresponds to the logged-in Fulfillment Representative, 3. The score uses quality-review information recorded for that representative, 4. The score covers the year-to-date reporting period, 5. The score is displayed alongside the representative’s operational dashboard information, 6. The representative can view the score without opening a separate report.
- **Timestamp:** Day 5, Part 1 [01:34 - 03:06]
- **Mockups:** NO MOCKUP
- **Notes:** The year-to-date quality score was requested as part of the representative's one-stop dashboard.
- **Responsible:** TBD

## CUBE-PH5-D5-003
- **Group:** Fulfillment & Accounting
- **Category:** Task Management
- **Epic:** Fulfillment Follow-Ups
- **Parent Task:** Follow-Up Creation
- **Task Name:** Create Follow-Up Tasks from Fulfillment Tickets
- **User Story:** As a Fulfillment Representative, I want to create a follow-up task directly from a Fulfillment ticket so that provider callbacks, confirmations, and other pending ticket actions are not forgotten.
- **Description:** The representative can open the follow-up task form from a Fulfillment ticket. The task is linked to the originating ticket and uses available ticket information to populate the representative, customer, site, and product details.
- **Acceptance Criteria:** 1. A Fulfillment Representative can initiate a follow-up task from a Fulfillment ticket, 2. The task type is set to Fulfillment – Follow-up, 3. The task is linked to the originating Fulfillment ticket, 4. The representative, customer, site, and available product information are populated from the ticket, 5. The representative can enter or modify the action date, status, duration, subject, and description, 6. Saving the form creates the follow-up task with its ticket relationship preserved.
- **Timestamp:** Day 5, Part 1 [04:24 - 06:57]
- **Notes:** Reuse the existing Add Task form and the Fulfillment – Follow-up task type shown in the mockup. Add an entry point from the Fulfillment ticket and preserve the relationship between the created task and that ticket.
- **Responsible:** TBD

## CUBE-PH5-D5-004
- **Group:** Fulfillment & Accounting
- **Category:** Task Management
- **Epic:** Fulfillment Follow-Ups
- **Parent Task:** Follow-Up Tracking
- **Task Name:** Track Follow-Up Completion and Duration
- **User Story:** As a Fulfillment Quality Coordinator, I want Fulfillment follow-up tasks to capture their scheduled and completed activity so that the team can report how many follow-ups were performed and how long they took.
- **Description:** The system records follow-up activity and supports reporting on the number, timing, and completion of follow-up tasks.
- **Acceptance Criteria:** 1. The follow-up stores its scheduled action date and time, 2. The follow-up records when the task was started, 3. The follow-up records when the task was completed, 4. The task can be marked as completed, 5. The system can report the number of follow-ups completed, 6. The system can report the duration of completed follow-ups.
- **Timestamp:** Day 5, Part 1 [06:58 - 08:48]
- **Mockups:** NO MOCKUP
- **Notes:** The existing follow-up process should be retained and used for confirmations and other ticket follow-ups.
- **Responsible:** TBD

## CUBE-PH5-D5-005
- **Group:** Fulfillment & Accounting
- **Category:** Notifications
- **Epic:** Fulfillment Follow-Ups
- **Parent Task:** Task Reminder Notifications
- **User Story:** As a Fulfillment Representative, I want notifications for scheduled follow-up tasks so that I am reminded to return to a ticket at the specified date and time.
- **Description:** Task notifications are generated from the action date and time recorded on a follow-up task.
- **Acceptance Criteria:** 1. A time-specific task generates a notification based on its action date and time, 2. The notification is sent before the scheduled action time, 3. A date-only task generates a notification at the beginning of the scheduled day, 4. The notification identifies the task requiring action, 5. The notification remains associated with the related follow-up task, 6. The representative can use the notification to return to the scheduled work.
- **Timestamp:** Day 5, Part 1 [08:49 - 10:22]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop referenced an Outlook-style reminder and approximately 15 minutes of advance notice, but the final notification interval was not confirmed.
- **Responsible:** TBD

## CUBE-PH5-D5-006
- **Group:** Fulfillment & Accounting
- **Category:** Task Management
- **Epic:** Fulfillment Follow-Ups
- **Parent Task:** Time-Sensitive Related Actions
- **Task Name:** Use Tasks for Time-Sensitive Inquiry and Ticket Follow-Ups
- **User Story:** As a Fulfillment Representative, I want time-sensitive actions related to accounting inquiries or Fulfillment tickets recorded as tasks so that they can receive precise reminder notifications.
- **Description:** Actions requiring date-and-time reminders are managed through tasks attached to the applicable accounting inquiry or Fulfillment ticket.
- **Acceptance Criteria:** 1. A task can be associated with an accounting inquiry, 2. A task can be associated with a Fulfillment ticket, 3. The task stores the required action date, 4. The task can store a specific action time, 5. Time-specific notifications are generated from the task rather than the related record, 6. The representative can access the related inquiry or ticket from the task.
- **Timestamp:** Day 5, Part 1 [10:25 - 13:00]
- **Mockups:** NO MOCKUP
- **Notes:** Minute-level notifications will be supported through tasks rather than continuous monitoring of every accounting inquiry or Fulfillment ticket.
- **Responsible:** TBD

## CUBE-PH5-D5-007
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Special-Project Tickets
- **Task Name:** Filter Tickets by Special-Project Classification
- **User Story:** As a Fulfillment Representative, I want to toggle between regular tickets and tickets related to special projects so that I can manage project work without losing access to the normal Fulfillment queue.
- **Description:** The dashboard uses report toggles instead of separate user-specific dashboards to distinguish CWS, Z-site, and other ticket groupings discussed in the workshop.
- **Acceptance Criteria:** 1. The ticket report includes a toggle for CWS-related tickets, 2. The report can distinguish CWS and non-CWS tickets, 3. The report includes a toggle for Z-site-related tickets when that classification remains applicable, 4. Applying a toggle does not permanently exclude the representative from the normal queue, 5. Representatives who do not use a special-project classification can leave its toggle inactive, 6. The same report structure can support both regular and special-project work.
- **Timestamp:** Day 5, Part 1 [13:06 - 18:30]
- **Mockups:** NO MOCKUP
- **Notes:** The future structure of Z-site work was not confirmed and is subject to change.
- **Responsible:** TBD

## CUBE-PH5-D5-008
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Ticket Reporting
- **Task Name:** Organize Open and Unfulfilled Tickets
- **User Story:** As a Fulfillment Representative, I want to organize open and unfulfilled tickets by operational attributes so that I can focus on the tickets relevant to my current work.
- **Description:** The dashboard ticket report supports the classifications and groupings explicitly identified during the workshop.
- **Acceptance Criteria:** 1. Tickets can be delineated by ticket type, 2. Tickets can be delineated by date, 3. Tickets can be delineated by priority, 4. Tickets can be grouped by customer, 5. Tickets can be grouped by site, 6. The report focuses on open and unfulfilled tickets.
- **Timestamp:** Day 5, Part 1 [18:31 - 19:06]
- **Mockups:** NO MOCKUP
- **Notes:** The report should focus on open and unfulfilled tickets.
- **Responsible:** TBD

## CUBE-PH5-D5-009
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Ticket Oversight
- **Task Name:** View Tickets by Representative and Lead
- **User Story:** As a Fulfillment Quality Coordinator, I want to view Fulfillment tickets across the department and narrow them by lead or representative so that I can review workloads at different levels of the team hierarchy.
- **Description:** The ticket reporting structure supports department-wide, lead-level, and representative-level views.
- **Acceptance Criteria:** 1. The coordinator can view all applicable Fulfillment tickets, 2. The coordinator can narrow the results by lead, 3. The coordinator can narrow the results by representative, 4. The selected hierarchy level updates the ticket results, 5. The displayed records remain subject to the applicable ticket filters, 6. The coordinator can move between the available hierarchy levels without opening separate spreadsheets.
- **Timestamp:** Day 5, Part 1 [19:07 - 19:50]
- **Mockups:** NO MOCKUP
- **Notes:** The hierarchy discussed during the workshop included department-wide, lead-level, and representative-level views.
- **Responsible:** TBD

## CUBE-PH5-D5-010
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Performance Metrics
- **Task Name:** Display Fulfillment Performance Metrics
- **User Story:** As a Fulfillment Representative, I want my relevant ticket-performance metrics displayed on the dashboard so that I do not have to rely on separate daily or weekly KPI reports.
- **Description:** The dashboard consolidates the representative's operational performance information currently communicated through separate reports.
- **Acceptance Criteria:** 1. The dashboard displays the representative's average ticket-completion time, 2. The dashboard displays the representative's completed-ticket count, 3. Performance metrics are calculated from Fulfillment ticket data, 4. The metrics are available without opening a separate spreadsheet, 5. The representative can view the metrics alongside current operational work, 6. The dashboard distinguishes the representative's metrics from department-level metrics.
- **Timestamp:** Day 5, Part 1 [19:51 - 20:55]
- **Mockups:** NO MOCKUP
- **Notes:** The complete list of required Fulfillment metrics will be provided after the workshop.
- **Responsible:** TBD

## CUBE-PH5-D5-011
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Productivity Points
- **Task Name:** Display Updated Productivity Points
- **User Story:** As a Fulfillment Representative, I want my productivity points to update as I close tickets so that I can see my current performance without waiting for the end-of-week report.
- **Description:** The system calculates productivity points from completed ticket activity and displays the representative's current total on the dashboard.
- **Acceptance Criteria:** 1. The system assigns productivity points using the applicable ticket data, 2. Closing a ticket causes the representative's productivity total to be recalculated, 3. The updated total is displayed on the representative's dashboard, 4. The points are calculated within CUBE rather than in a separate spreadsheet, 5. The displayed total reflects the logged-in representative's completed work, 6. The representative can view the current total before the end of the reporting week.
- **Timestamp:** Day 5, Part 1 [20:56 - 21:40]
- **Mockups:** NO MOCKUP
- **Notes:** The precise productivity-point formulas and values were not defined during the workshop.
- **Responsible:** TBD

## CUBE-PH5-D5-012
- **Group:** Fulfillment & Accounting
- **Category:** Reporting
- **Epic:** Fulfillment Performance
- **Parent Task:** Productivity Calculations
- **Task Name:** Configure Point Values by Ticket Type
- **User Story:** As a Fulfillment Director, I want point values associated with Fulfillment ticket types in CUBE so that productivity reports can be calculated by the system instead of maintained in spreadsheets.
- **Description:** The data required for the existing productivity calculations is stored in CUBE, including the point value applicable to each ticket type.
- **Acceptance Criteria:** 1. A point value can be associated with a Fulfillment ticket type, 2. The configured point value is available to productivity calculations, 3. Completed tickets use the value associated with their ticket type, 4. Productivity totals can be calculated for each representative, 5. The calculation does not depend on manually updating an external spreadsheet, 6. Changes to point-value data are reflected in subsequent productivity calculations.
- **Timestamp:** Day 5, Part 1 [21:41 - 24:23]
- **Mockups:** NO MOCKUP
- **Notes:** The current system was described as containing priority scoring but not all data required for productivity-point calculations.
- **Responsible:** TBD

## CUBE-PH5-D5-013
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Performance Comparison
- **Task Name:** Compare Individual and Department Performance
- **User Story:** As a Fulfillment Representative, I want to compare my ticket metrics and productivity points with department totals so that I can understand my performance relative to the team.
- **Description:** The dashboard presents individual metrics together with the corresponding department-level values when the metric is used for comparison.
- **Acceptance Criteria:** 1. The dashboard displays the representative's applicable metric, 2. The dashboard displays the corresponding department metric, 3. Individual and department values use the same calculation basis, 4. Ticket-completion time can be compared at both levels, 5. Productivity points can be compared at both levels, 6. The comparison is available without accessing the existing spreadsheet.
- **Timestamp:** Day 5, Part 1 [24:24 - 26:09]
- **Mockups:** NO MOCKUP
- **Notes:** Department comparisons should be provided for the performance metrics selected for the dashboard.
- **Responsible:** TBD

## CUBE-PH5-D5-014
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Performance Periods
- **Task Name:** View Performance by Time Range
- **User Story:** As a Fulfillment Representative, I want to select different reporting periods for my performance metrics so that I can review what I completed today, this week, this month, or across another available period.
- **Description:** The dashboard provides time-range controls for relevant ticket, time, and productivity metrics.
- **Acceptance Criteria:** 1. The representative can view metrics for the current day, 2. The representative can view metrics for the current week, 3. The representative can view metrics for the current month, 4. The dashboard provides a time-range selection control, 5. Changing the time range recalculates the displayed metrics, 6. Individual and corresponding department metrics use the same selected period.
- **Timestamp:** Day 5, Part 1 [25:01 - 26:51]
- **Mockups:** NO MOCKUP
- **Notes:** The workshop also mentioned all-time reporting, but the final set of available periods was not confirmed.
- **Responsible:** TBD

## CUBE-PH5-D5-015
- **Group:** Fulfillment & Accounting
- **Category:** Dashboard
- **Epic:** Fulfillment Dashboard
- **Parent Task:** Bonus Transparency
- **Task Name:** Display Projected Bonus Points
- **User Story:** As a Fulfillment Representative, I want to see my projected bonus points on my dashboard so that I can understand how many points I have earned toward the applicable monthly bonus.
- **Description:** The dashboard displays the representative's accumulated bonus-related points for the applicable bonus period.
- **Acceptance Criteria:** 1. The dashboard displays the representative's current bonus-point total, 2. The total is associated with the applicable monthly bonus period, 3. The displayed points are calculated from the representative's recorded productivity activity, 4. The total updates when qualifying activity changes, 5. The information is visible to the representative for transparency, 6. The representative does not have to wait for a separate bonus report to view the total.
- **Timestamp:** Day 5, Part 1 [26:58 - 27:36]
- **Mockups:** NO MOCKUP
- **Notes:** Bonus points are used to determine the representative's bonus, making their visibility important for transparency.
- **Responsible:** TBD

## CUBE-PH5-D5-016
- **Group:** Fulfillment & Accounting
- **Category:** Quality Control
- **Epic:** Fulfillment Quality Review
- **Parent Task:** Quality Review Records
- **Task Name:** Create Scored Quality-Control Reviews
- **User Story:** As a Fulfillment Quality Coordinator, I want each Fulfillment quality review stored as a separate scored questionnaire so that review answers and their point values can be used to calculate a quality score.
- **Description:** The existing quality-control questionnaire, form rules, layout, and point values are transferred into a separate review record associated with the Fulfillment ticket.
- **Acceptance Criteria:** 1. A quality review is stored as a separate record, 2. The review is associated with the applicable Fulfillment ticket, 3. The review contains the existing questionnaire fields, 4. Questionnaire answers use the existing point values, 5. The system calculates a score from the recorded answers, 6. The review identifies the selected reviewer.
- **Timestamp:** Day 5, Part 1 [39:39 - 42:48]
- **Mockups:** NO MOCKUP
- **Notes:** The existing questionnaire, layout, form rules, and point values should remain as-is unless later changes are provided.
- **Responsible:** TBD

## CUBE-PH5-D5-017
- **Group:** Fulfillment & Accounting
- **Category:** Quality Control
- **Epic:** Fulfillment Quality Review
- **Parent Task:** Conditional Questionnaire
- **Task Name:** Apply Conditional Rules to Quality-Review Questions
- **User Story:** As a Fulfillment Quality Coordinator, I want quality-review questions displayed according to the applicable answer and product type so that reviewers only complete questions relevant to the ticket being reviewed.
- **Description:** The quality-review questionnaire retains conditional form behavior, including answer-dependent questions and product-specific applicability.
- **Acceptance Criteria:** 1. A question can display an additional question when the specified answer is selected, 2. The dependent question remains hidden when its triggering condition is not met, 3. Questions can be excluded when they do not apply to the ticket's product type, 4. The tonnage question is not displayed for a portable-toilet ticket, 5. Conditional behavior is applied within the quality-review record, 6. Hidden non-applicable questions do not require an answer.
- **Timestamp:** Day 5, Part 1 [42:54 - 43:35]
- **Mockups:** NO MOCKUP
- **Notes:** The tonnage question for a portable-toilet ticket was provided as an example of a question that should not appear when it is not applicable.
- **Responsible:** TBD

## CUBE-PH5-D5-018
- **Group:** Fulfillment & Accounting
- **Category:** Quality Control
- **Epic:** Fulfillment Quality Review
- **Parent Task:** Review Workspace
- **Task Name:** Review the Questionnaire and Ticket Side by Side
- **User Story:** As a Fulfillment Quality Coordinator, I want the quality-review questionnaire and its Fulfillment ticket displayed side by side so that I can answer the questionnaire without duplicating ticket information in the review.
- **Description:** The review workspace presents the separate quality-review record beside the related Fulfillment ticket, which serves as the reference for ticket and margin information.
- **Acceptance Criteria:** 1. The quality-review questionnaire is displayed beside the related Fulfillment ticket, 2. The reviewer can reference ticket information while completing the questionnaire, 3. The Fulfillment ticket displays the applicable low-margin information, 4. The low-margin information includes the approver when a low margin was approved, 5. Margin fields already available on the ticket are not duplicated as manually entered review fields, 6. The review record uses standard creation and modification timestamps instead of a manually tracked review-time field.
- **Timestamp:** Day 5, Part 1 [43:59 - 47:03]
- **Mockups:** NO MOCKUP
- **Notes:** The team confirmed that manual review-duration monitoring is no longer required. Margin information can be removed from the questionnaire if the complete information is available on the Fulfillment ticket.
- **Responsible:** TBD

---
