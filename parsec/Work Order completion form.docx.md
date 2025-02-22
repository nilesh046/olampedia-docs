# Club Coffee – Preventive Maintenance Work Order Completion Form

# Work Order Completion Form - Functional Specification

|Module|PM|
|---|---|
|Conversion|Forms|
|Version|1.0|

1 | P a g e
---
# Business Blueprint

# Project Maple – IT Applications Transformation at CLUB

# Club Coffee LP Canada (S/4HANA)

# COFFEE

Woke i rea

EST: 1906

OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

# Document Details

| |Role|Individuals Name|
|---|---|---|
|Author|Functional Designer|Arun Patwa|
|Reviewer|Document Review|Ramesh AVS|
|Approval|GT Approval| |

# Change Control

|Version|Version Details|Individuals Name|Date|
|---|---|---|---|
|1.0|Initial Draft|Arun Patwa|28/08/2023|

# Club Coffee MES to SAP Interface Implementation
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

# Content

1. Functional Specification................................................................................................. 4
2. General Information...............................................................................................................................4
3. Overview.......................................................................................................................... 5
4. 1. Overview & Scope.................................................................................................................................5
2. Assumptions..........................................................................................................................................5
3. Key Report Characteristics.................................................................................................................... 5
4. Dependencies / Constraints................................................................................................................... 5

Detailed Functional Requirements................................................................................6
5. 1. Functional Detail / Process Flow............................................................................................................ 6
2. Existing / Sample Reports..................................................................................................................... 9
3. Selection................................................................................................................................................9
4. 1. Selection Screen Layout/Fields/Logic & Validation.......................................................................9

Conversion Layout.................................................................................................................................9
5. Error Handling....................................................................................................................................... 9
6. Performance Consideration(s).............................................................................................................10
7. Non-Functional Requirements.............................................................................................................10

Testing Requirements..................................................................................................11
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

# 1 Functional Specification

# 1.1 General Information

General description

FRICEW reference number Forms (ZETA ID)

Process description¹ Once the Maintenance order confirmation has done by the user, System has to Print the planned and confirmed activities carried out.

Report Usage Origin Specific

GT Development

Origin Requested Yes

Impact on Solution

Areas of impact

1 Short description of the process context of the report

Club Coffee MES to SAP Interface Implementation
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

# 2 Overview

# 2.1 Overview & Scope

Club Coffee has been a leader in private label and co-manufactured coffee solutions for over 100 years. As a part of S/4 HANA implementation, logistics modules will be implemented. With respect to Plant maintenance module, Club Coffee carry out Preventive maintenance activities with respect to equipment and Operational activities from production side.

Once the PM order is generated based on the scheduled date, the order will be assigned to the technician to carry out the task. PM order will be released, and the task will be confirmed against the planned operation. After confirmation, a printout will be taken by the user to verify the planned task with respect to the actual task.

# 2.2 Assumptions

The input will be based on the selection parameters only.

# 2.3 Key Report Characteristics

|Report Characteristics|Description|
|---|---|
|Trigger|Document the trigger for the report|
| |User initiated on-line|
| |Scheduled job|
| |System trigger (e.g. output of transaction execution)|
|Frequency/Timing of Execution|Indicate the frequency of the report execution|
| |Ad-hoc|
| |Hourly|
| |Daily|
| |Weekly|
| |Monthly|
|Processing Type|Indicate how the report will be processed once triggered|
| |Batch|
| |Real time|
|Output Type|Indicate the expected output method(s) for the report (e.g. On-screen response, send to print, send to email account)|
| |On-screen response|
| |Send to print|
| |Send to email|

# Club Coffee MES to SAP Interface Implementation
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

# Expected Number of Records (Transaction Volume)

Provide an indication of the expected number of records that will need to be read and/or displayed (maximum count)

# 2.4 Dependencies / Constraints

# 2.5 Detailed Functional Requirements

# 2.6 Functional Detail / Process Flow

Order will be appeared in the list of PM order due for completion both in SAP GUI System and Mobile application.

Release of order by authorized person/Planner in the mobile application.

Planner will assign Internal Technician to execute the task at site.

During the execution of the task if materials are required then the same can be raised in the mobile application to generate the reservation number automatically.

Based on the order number Maintenance team will use barcode Scanner to scan the material and will be issued against the same.

Technician will use the materials and carry out the PM task as planned.

Individual or bulk operation will be carried out through confirmation tab in mobile and record the observation against the planned and actual execution of task.

During confirmation duration and user id will be captured and detail assessment can be captured through long text option available in mobile.

PM -Completion report will be generated to check the planned operation vs actual operation executed after completion of all PM tasks in the SAP system.

Technical completion of the order will be executed to finish the process through mobile application.

# Detail Steps for development:

Logic for order Number:

1. User Enters table AUFK-AUFNR value AUART=ZM01,ZM02,ZM03,ZM04,ZM05
2. Pass OBJNR value into JEST table
3. IF JEST-STAT= I0045(TECO), I0046 (CLSD),I0002 (REL) JEST-ACT TO “ ”)
4. ‘Continue with Next step

Now fetch the records

- Order number=In table AUFK and fetch AUFNR
- Order Type: In table and fetch AUART
- Order Status: In table AUFK-OBJNR pass OBJNR to JEST table to get the status
- Description: In table AUFK and fetch KTEXT
- ABC Indicator (Criticality): In table VIAUFKS pass AUFNR and retrieve ABCKZ value
- Location: In table AUFK and fetch STROT
- Last changed by (Assigned by): In table AUFK and fetch AENAM
- Main work center (Assigned to): In table AUFK and fetch VAPLZ
- Plant =In AUKF table pass the AUFNR to get WERKS.
- Equipment No: In table AFIH and fetch EQUNR

# Club Coffee MES to SAP Interface Implementation
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

Equipment Description: In table EQUI and fetch EQKTU

Manufacturer: In table EQUI pass the EQNR and fetch the HERST

Serial no: In table EQUI pass the EQNR and fetch the TYBPZ

Model no: In table EQUI pass the EQNR and fetch the SERGE

Priority: In table AFIH get the PRIOK

Function Location= In table VIAUFKS pass AUFNR and retrieve TPLNR value

PM date: In table MHIO pass AUFNR and get WARPL& ABNUM and pass WARPL & ABNUM in MHIS to get NPLDA.

Next due date: In table MHIO pass and WARPL and get GSTRP

Actual start date: In table AFKO get the GSTRI

End date: In table AFKO get the GETRI

# Work carried out:

Task list Description: In AFKO table pass AUFNR and take AUFPL number and pass it in AFVC table AUFPL field and get LTXA1, LTXA2 and VORNR for all the fields.

Confirmation Text: Pass AUFNR in AFRU table and retrieve LTXA1.

Task List Instruction: The data maintained in under task list instruction remains’ same.

# 2.7 Existing / Sample Reports

NA

# 2.8 Selection

# 2.8.1 Selection Screen Layout/Fields/Logic & Validation

[Provide a sample layout for the selection screen. The selection screen gives the user the capability to refine the search criteria prior to executing the report. Please provide the fields and their descriptions in the report layout. Document any additional rules and validations required in the selection screen. Do not include processing logic in this section. Also include any variants that need to be created.]

# General Data:

|Plant|Description| |
|---|---|---|
|Order Number|Order type|Order status|
|Assigned by|Assigned to| |
|Equipment No|Equipment|Model No.|
|Description|Manufacturer|Serial No.|
|Function Location|Criticality|Location|
|PM Date|Next Due Date| |

Club Coffee MES to SAP Interface Implementation
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

|Actual Start Date|End date|Operation|
|---|---|---|
| | | |

|Slno|Work Center|Operation description|Confirmation Text|
|---|---|---|---|
|1|mechh|Inspection| |

# Task List Instructions:

Follow all Lock Out Tag Out (LOTO) procedures and be sure that you have read the Health and Safety manual for this procedure.

Line Equipment Clearance Protocol.

1. Reconciliation of all tools and parts:.......................................... Yes__No__Not applicable__
2. Day#1______Day#2_______Day#3_____Day#4____
3. Sanitation and wiped down completed after maintenance work Yes__ No__ Not applicable__
4. Food grade/Nonfood grade lubricant used:.............................. Yes__No__ Not applicable__
5. Product contamination hazard removed from line/equipment:. Yes__ No __Not applicable__
6. Any temporary repairs made:.................................................... Yes__ No __ Not applicable__ If yes, please describe it_____________________________________________________
7. ____________________________________________________________________________

DONE BY:

Sign & Date:

Name:

APPROVED BY:

Sign & Date:

Name:

PM-completion form

Clubcoffee form

form pdf

test_pdf

# Conversion Layout

[Attach excel for conversion fields]

Club Coffee MES to SAP Interface Implementation
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

# Conversions

|Zeta ID|Conversion Object|Source|Conversion Activities|Conversion Method|T Code|
|---|---|---|---|---|---|
|1|MAPPING SAP FIELDS TO SOURCE / TARGET|[Please provide details of the expected mapping between the Source / Target system and SAP fields. This can either be done within a table in this document or as an attached Mapping Document.]|[Please provide details of the expected mapping between the Source / Target system and SAP fields. This can either be done within a table in this document or as an attached Mapping Document.]|[Please provide details of the expected mapping between the Source / Target system and SAP fields. This can either be done within a table in this document or as an attached Mapping Document.]|[Please provide details of the expected mapping between the Source / Target system and SAP fields. This can either be done within a table in this document or as an attached Mapping Document.]|

# 2.10 Error Handling

Field Label
SAP Table
SAP Field Name
Mandatory, Optional (M / O)
Rules/Notes

# 2.11 Performance Consideration(s)

# 2.12 Non-Functional Requirements

# 2.12.1 Security

Data security classification:

- INTERNAL USE – Low-risk information generally available to internal employees, but not the public
- RESTRICTED – Should be restricted to be available to only nominated internal employees.

# 2.12.2 Authority/Authorization object

Club Coffee MES to SAP Interface Implementation
---
# Business Blueprint

# Project Maple – IT Applications Transformation at Club Coffee LP Canada (S/4HANA)

# OLAM/SAP/GT/BBP/PP

# Process Order Goods Issue and Goods Receipt (MES to SAP)

# Functional Specification

# 3 Testing Requirements

# 3.1 Key Business Test Conditions

[Document the business-level test conditions that should be used to verify successful operations of the report. These should be tested by the developer to ensure compliance with the expectations of the functional designer and also used by the functional designer as a means to validate the development and functionally acceptance test the component. Note: The table below should not include detailed technical testing requirements – these will be documented by the technical designer / developer in the technical design document.]

|Report No.|Reference|Test Condition|Expected Results|
|---|---|---|---|
|Club Coffee MES to SAP Interface Implementation| | | |