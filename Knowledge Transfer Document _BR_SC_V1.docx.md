# Global SAP SUPPORT

# Olam

# Olam Information Services Pvt Ltd - Global SAP Support Team

# Knowledge Transfer Document

Country: Brazil_SC

Product: Coffee

Legal Entity: BR25

Module: Sales and Distribution

|NAME|DATE|Origin|JOB TITLE|
|---|---|---|---|
|Prepared By|05-04-2023|Brazil_SC|Functional/Senior Consultant|
|Reviewed By|05-04-2023|Brazil_SC|Lead Consultant|
|Approved By|05-04-2023|Brazil_SC|Project Manager|

# VERSION HISTORY

|Version No.|Date|Changed By|Changes Made After Go live|
|---|---|---|---|
|1|05-04-2023|Rahul Bhosale|Initial Document|
---
# Global SAP SUPPORT

# Olam

# Knowledge Transfer Document

# Table of Contents

# OBJECTIVE

# 1.1 PROJECT INTENT

# 1.2 PRODUCT BRIEF DESCRIPTION-

# 1.3 EXISTING TOOLS BEING USED

# 1.4 USER DETAILS

# END USER DETAILS

# TOTAL USERS

# BUSINESS PROCESS OWNERS

# 2.0 BUSINESS PROCESS / FUNCTIONAL KNOWLEDGE

# 2.1 KNOWLEDGE TRANSFER SESSIONS DETAILS

# 3.0 TECHNICAL DETAILS

# 3.1 CONFIGURATION DOCUMENT

# 3.2 BBP /FS ATTACHMENT

# 3.3 Z TRANSACTION DETAILS

# 3.4 Z TABLE DETAILS

# 3.5 Z REPORT DETAILS

# 3.6 MOBILITY SOLUTIONS

# 3.7 END USER DOCUMENTATION

# 3.8 TEST SCRIPTS

# 3.9 DETAILS OF ISSUES/CHANGES HANDLED DURING HYPER CARE

# 3.10 JOB SCHEDULING

# 4.SPECIAL MASTER DATA REQUIREMENTS

# 4.0 RELEVANT MANDATORY FIELDS OF MASTERS

# 4.1 PARAM TABLE ENTRIES

# 5.0 KNOWLEDGE TRANSFER PROCESS

# 6.SPECIFIC INFORMATION

# 6.1 ALL ISSUES FACED AFTER GO LIVE

# 6.2 PENDING DEVELOPMENTS POST GO LIVE

# 6.3 LESSONS LEARNED DURING PROJECT

# 6.4 DETAILS OF OPEN ISSUES

# 6.5 OTHER DETAILS/INTEGRATED POINTS

# 6.6 THIRD PARTY CONTACT DETAILS

# 6.7 LOCAL REGULATORY REQUIREMENTS

# 6.8 AUTHORIZATION MATRIX

# 7.APPROVAL MAILS

# 8. EXCEPTION/NOTES/GAP NON - GT SOLUTIONS
---
# Global SAP SUPPORT

# OBJECTIVE

This document is intended to capture the understanding of the application gained by support team during the Knowledge Acquisition phase. The objective is for Practice / Application support group Owners to assess the understanding, comfort level and effectiveness of the Knowledge acquisition phase and decide the readiness of proceeding to subsequent phases in the Knowledge acquisition phase gate review.

# Timelines & Process of Handover to Support

Essentially the Project team decides on the duration of hyper care support to Origins depending upon the system/ user’s stability and usage. During Hypercare, support team members shall be involved, and they would travel to the origin and understand the business process, user comfort etc. Project teams shall inform support team 2-3 month in advance for hypercare support. During this phase the process KT shall start to the support team member and support team member would be shadowing the project consultant.

On completion of knowledge transfer and complete documentation, project consultant would shadow the support consultant for a duration where user comfort levels could be determined. Few Indicators for Stabilization- Outstanding Issues proportion, completion of major program changes, Absence of backend table updates. The formal transition happens after the joint call with the business is done and the support process is intimated to origins.
---
# Global SAP SUPPORT

# 1.1 Project Intent

(Business expectation and IT delivery)

Previously, there wasn’t any system to record the quantity sold and revenue in the system. In Olam Coffee, sales and Distribution model is implemented to track the quantity of goods sold and to record the revenue in SAP system.

# 1.2 Product Brief Description

(Description of the BU / Product business in brief)

Olam instant Coffee has estate in Brazil (Brazil_SC), which was spread around 10,870 Ha. From the Estate, they harvest the wet cup lump, which they called as “Tapping”. After the drying process, they sell the Dry cup lump to the customer.

# 1.3 Existing Tools Being Used

|Type|Concept|Version|Identified in Application|
|---|---|---|---|
|NA|I Olam|1.0|Yes|
|Legacy System (If Any)|NA|1.0|Yes|
|SAP|NA| |Yes|
|Interface (If Any)| | |Yes|

# 1.4 User Details

End User Details

Total users

Business Process Owners
---
# Global SAP SUPPORT

# 2.0 Business Process / Functional Knowledge

# Business functionality

|BBP reference|BR Soluble|
|---|---|
|1|Coffee_SD_BBPVIZ|
|Brazil soluble|2 coffee BPML SD.Xsx|

# Business Process

|1|NA|
|---|---|
|Included During|2|
|Hyper Care(Which is not part of BBP)|Product Process|
|2|NA|

# 2.1 Knowledge transfer Sessions details

Date Held
Project Consultants
Support Consultants
---
# Global SAP SUPPORT

# 3.0 Technical details

# 3.1 Configuration Document

|Version|Configuration Description|Configuration Documents|Configuration document link|
|---|---|---|---|
|1.0|COFFEE Configuration|SD|SD|

# 3.2 BBP /FS Attachment

|Version|Process Description|Attachments or Links|
|---|---|---|
|1.0|ORG Olam Coffee Brazil_SC|SD|

# 3.3 Z Transaction Details

|Z Transaction Code|Description|Purpose|FS details|Accounting Impact|
|---|---|---|---|---|
|ZSD955|Trigger SAP invoice to CTRM|Triggering the SAP invoice to CTRM|NA|NA|

# 3.4 Z Table Details

|Z Table Name|Description|Purpose|Associated Transaction/Report|Maintenance Required|
|---|---|---|---|---|
|ZBRMMTR_INT_DA TA|Data Interface|For Dummy sales interface with Easy Export.|ZBRSDFM_WB_CMS_SAP_DELIVERY ZBRSD_DELIVERY_AUTOMATION1|No|
|ZGTCATR_PARAM|PARAM table for customizing|HSN code maintain|ZBRSDCL_ADD_DATA_UTRIB|No|
---
# Global SAP SUPPORT

|entries|Local Paramfor|HSN number|
|---|---|---|
|ZGT_OTIF_EXCEPT|Field|For|
|I|validatio|exceptio|
| |n|of the|
| |Exception XLSX|No|
|ZGTSDTR_CTRMM|Field|For|
|AND|validatio|exceptio|
| |n|of the|
| |ExceptionlXLSX|No|
| |exceptio|mandatory data|
| |in|Delivery|

# 3.5 Z Report Details

|Transaction Code|Description|Purpose|Details|
|---|---|---|---|
|ZSD8001|Sales Report|Sales report|Details of sales report|
|ZWB606|Weighbridge Report|Weighbridge Report|Details of Weighbridge Report|
|ZSD206|Contract Status Report|Contract Status Report|Details of Contract Status Report|
|ZSD207|Billing Report|Billing Report|Details of Billing Report|
|ZSD412|Credit block report|Credit block report|Details of Credit block report|

# 3.6 Mobility Solutions

|Description|Process|Master Data|Usage Frequency|Business Owner|Transaction Code|
|---|---|---|---|---|---|
|NA|NA|NA|NA|NA|NA|

# 3.7 End User Documentation

|Document Name|Description|Scenario Name|Link|Reversal Procedure Included|Yes/No|
|---|---|---|---|---|---|
|NA|NA|NA|NA|NA|NA|

# 3.8 Test Scripts

|Document Name|Description|Scenario Name|Link|Reversal Procedure|
|---|---|---|---|---|
|NA|NA|NA|NA|NA|
---
# Global SAP SUPPORT

|Included|Yes/No|
|---|---|
|Coffee SD Test|Sales process|
|Test scripts-|No|
|Script|of Coffee Sales|
| |BR_SC_SD.xls|
---
# Global SAP SUPPORT

# 3.9 Details of Issues/Changes handled during Hyper Care

|Issues Description|Root Cause|Corrective Action|Proposed Solution (Accounting Entry)|Financial Impact Yes/No|
|---|---|---|---|---|
|NA|NA|NA|NA|NA|

# 3.10 Job Scheduling

|Program Name|Plant|Variant Name|Reason|Frequency|
|---|---|---|---|---|
|NA|NA|NA|NA|NA|

# 4. Special Master Data Requirements

# 4.0 Relevant Mandatory Fields of Masters

|Masters Name|Mandatory Field|Related Report Impact|Related T. Code|Reasons|
|---|---|---|---|---|
|NA|NA|NA|NA|NA|

# 4.1 Param Table entries

|Module|Description|Program Name|Parameter Values|Related Transactions Impacted|
|---|---|---|---|---|
|ZGTCATR_PARAM|Parameter Table for Customizing Entries to integrate with CTRM|NA|NA|CTRM PARAM.Msx|
---
# Global SAP SUPPORT

# 5.0 Knowledge Transfer process

|Document|Available| | |Received|
|---|---|---|---|---|
|Business Requirements|Yes|No|Yes|No|
|Functional Specifications|Yes|No|Yes|No|
|Product Flow Diagrams|Yes|No|Yes|No|
|Data Flow Diagrams|Yes|No|Yes|No|
|Product Specific Report (Origin Specific)|Yes|No|Yes|No|
|Business Process Master List (BPML)|Yes|No|Yes|No|
|Reversal Documents (Mandatory)|Yes|No|Yes|No|
|Opening balance confirmation with business|Yes|No|Yes|No|
|BBP sign off|Yes|No|Yes|No|
|Data In GRQ|Yes|No|Yes|No|
|User Manuals|Yes|No|Yes|No|
|Training Material|Yes|No|Yes|No|
|Test Scripts (Must be Aligned with BPML)|Yes|No|Yes|No|

# Process

|Scenario’s Demo|Start Date|End Date|Attendees|Status|
|---|---|---|---|---|
| | | | | |
---
# Global SAP SUPPORT

# 6. SPECIFIC INFORMATION

# 6.1 All Issues Faced After Go Live

|Module|Error Screen Shot|Dependency|Expected Result|Actual Result|Status|
|---|---|---|---|---|---|
|SD|NA|NA|NA|NA|NA|

# 6.2 Pending Developments Post Go Live

|Description|Business Requirement|Proposed Requirement (Process Flow)|Financial Impact|Charm ID|
|---|---|---|---|---|
|NA|NA|NA|NA|NA|

# 6.3 Lessons Learned During Project

|Date|Module|Situation|Impact|Solution|Follow Up Needed ??|
|---|---|---|---|---|---|
|NA|NA|NA|NA|NA|NA|

# 6.4 Details of Open Issues

|Issue|Description|Priority|Reported By|Assigned to|Status|
|---|---|---|---|---|---|
|NA|NA|NA|NA|NA|NA|

# 6.5 Other Details/Integrated Points

|Description|Documents|Details|Link|Remarks|
|---|---|---|---|---|
|BBP Sign Off|BBP Signoff|SD Coffee BBP Sign off| |Approved by Mr. Pedro Guimaraes|
|Opening Balance|NA|NA|NA|Confirmation from Business|

# 6.6 Third Party Contact Details

|Name|Email ID|Contact|
|---|---|---|
|NA|NA|NA|
---
# 6.7 Local Regulatory Requirements

|Description|Purpose|Process Flow|
|---|---|---|
|NA|NA|NA|

# 6.8 Authorization Matrix

|Legal Entity|Profit Center|Primary Business Approver|Secondary Business Approver (Back Up)|
|---|---|---|---|
|BR25|BR1127|Mr. Pedro Guimaraes| |
---
# Global SAP SUPPORT

# 7. Approval Mails

|Description|Attachment/Mail|
|---|---|
|Quality Gate Approval Mail|NA|
|UAT sign off Mail| |
---
# Global SAP SUPPORT

# 8. Exception/Notes/GAP Non - GT solutions

|Description|Details|
|---|---|
|NA|NA|

Project Consultant: Rahul Bhosale

Support Consultant:

Date: 05/04/2023