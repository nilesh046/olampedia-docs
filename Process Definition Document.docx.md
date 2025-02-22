# Configuration Document

# Olam

# Project: Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Document Details

|Document Category|Configuration Document|
|---|---|
|Document title|PM Configuration Document|
|Team|PM|
|Project|Canada club coffee s4 Hana implementation|
|Product|Coffee|

# Document Versions

|Date|Version|Author|Status – Description|
|---|---|---|---|
|29/06/2023|V1.0|Saravana Raja T|Baseline Configuration|
|09/08/2023|V2.0|Arun Patwa|Change in config (Point 30, 31, 32, 33, 34, 35, 36, 37, 38, 39 & 40)|
|21/09/2023|V.3.0|Arun Patwa|Change in config (Point 41, 42, 43 & 44)|
|17/01/2024|v.4.0|Arun Patwa|Change in config (point 45 & 46)|
|22/01/2024|v.5.0|Arun Patwa|Change in config (point 47)|
|26/01.2024|V.6.0|Arun Patwa|Change in config (point 48)|
|29/01.2024|V.7.0|Arun Patwa|Change in config (point 49)|

TR NO: OLAM/DFM/SAP/PM/Configuration

Page 1 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

# Contents

1. MAINTENANCE PLANNING PLANT – DEFINITION.....................................3
2. ASSIGNING MAINTENANCE PLANNING PLANT TO MAINTENANCE PLANT. .4
3. DEFINE LOCATION...............................................................................5
4. PLANNER GROUP................................................................................6
5. DEFINE PLANT SECTION.......................................................................7
6. TYPES OF TECHNICAL OBJECTS............................................................8
7. STRUCTURE INDICATOR.......................................................................8
8. FUNCTIONAL LOCATION CATEGORY......................................................9
9. MAINTAIN EQUIPMENT CATEGORY......................................................10
10. MAINTENANCE PROCESSING - DEFINE NOTIFICATION TYPES................10
11. MAINTENANCE PROCESSING - ASSIGN NOTIFICATION TYPES TO ORDER TYPES......................................................................................................11
12. MAINTENANCE PROCESSING - NOTIFICATION CONTENT.......................12
13. MAINTENANCE PROCESSING - NOTIFICATION CONTENT - DEFINE CATALOG PROFILE.....................................................................................13
14. MAINTENANCE PROCESSING - NOTIFICATION CONTENT – CATALOGS FOR NOTIFICATION TYPES................................................................................14
15. MAINTENANCE PROCESSING - NOTIFICATION PROCESSING..................15
16. MAINTENANCE PROCESSING – MAINTENANCE & SERVICE ORDERS........17
17. MAINTENANCE PROCESSING – MAINTENANCE & SERVICE ORDERS........18
18. MAINTENANCE PROCESSING – MAINTENANCE & SERVICE ORDERS........19
19. MAINTENANCE PROCESSING – MAINTENANCE & SERVICE ORDERS........20
20. MAINTENANCE PROCESSING – MAINTENANCE & SERVICE ORDERS........21
21. MAINTENANCE PROCESSING – MAINTENANCE & SERVICE ORDERS........22
22. MAINTENANCE PROCESSING – MAINTENANCE & SERVICE ORDERS........23
23. MAINTENANCE PROCESSING – MAINTENANCE PLANS...........................24

OLAM/DFM/SAP/PM/Configuration           Page 2 of 64        Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Version 1.0

# 1. Maintenance Planning Plant – Definition

SAP Customizing Implementation Guide

Enterprise Structure

# Menu Path

Definition &gt; Plant Maintenance &gt; Maintain Maintenance Planning Plant

# Transaction Code

SPRO

# Transport Request

# Configuration

Define Planning Plant

# Description

|Planning plant Name|Name|
|---|---|
|1990|#55 & #65 Carrier Dr|
|1991|#101 Claireville|
|1992|#160 Claireville|

# Maintenance Plant

|Maintenance Plant|Description|
|---|---|
|1990|55 Carrier Dr & 65 Carrier Dr|
|1991|#101 Claireville|
|1992|#160 Claireville|

OLAM/DFM/SAP/PM/Configuration Page 3 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# 2. Assigning Maintenance Planning Plant to Maintenance Plant

Menu Path: SAP Customizing Implementation Guide &nbsp; Enterprise Structure &nbsp; Assignment &nbsp; Plant Maintenance &nbsp; Assign maintenance planning plant to maintenance plant

Transaction Code: SPRO

Transport Request

# Configuration

Assign Maintenance Planning Plant to Maintenance Plant

# Description

|Plnt Name|Planning Plant|Description|
|---|---|---|
|1990 #55 & #65 Carrier Dr|1990|55 Carrier Dr & 65 Carrier Dr|
|1991 #101 Claireville|1991|101 Claireville|
|1992 #160 Claireville|1992|160 Claireville|

OLAM/DFM/SAP/PM/Configuration &nbsp; Page 4 of 64 &nbsp; Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# OLAM/DFM/SAP/PM/Configuration

Page 5 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

# 3. Define Location

Menu Path: SAP Customizing Implementation Guide   Enterprise Structure   Definition Logistics General   Define Location

Transaction Code: SPRO

Transport Request: Configuration

# Define Location:

# Description: Display View "Locations"            Overview

|Plnt Location|Name| |
|---|---|---|
|1990|RST|Roasting|
|1990|ADMI|Admin block|
|1990|BAGB|Bran Bagging|
|1990|BAGF|Flur Bagging|
|h199o| |Blend After Roast|
|1990|CHILE|US-Chile Pepper|
|1990|CLEN|Cleaning|
|1990|FLV|Flavour|
|1990|GND|Grinding|
|1990|MACS|Machine shop|
|1990|MILA|Miling|
|1990|MILB|Mlling|
|1990|MILC|Milling C|
|1990|MILD|Miling D|
|1990|MILE|Miling|
|1990|PCK|Packing|

OLAM/DFM/SAP/PM/Configuration           Page 6 of 64        Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

|Location|Description|
|---|---|
|RST|Roasting|
|GND|Grinding|
|BAR|Blend After Roast|
|FLV|Flavour|
|PCK|Packing|

# 4. Planner Group

# SAP Customizing Implementation Guide

# Plant Maintenance and Customer Service

# Master Data in Plant Maintenance and Customer Service

# Technical Objects

# General Data

# Define Planner Groups

Menu Path

Transaction Code: SPRO

Transport Request

Configuration

# Description

Define Planner Groups

OLAM/DFM/SAP/PM/Configuration

Page 7 of 64

Version 4.0

Document
---
# Configuration Document

# Project: Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Display View "Maintenance planner groups Overview

|PG|Name|Telephone|
|---|---|---|
|1990 P01|Mechanical| |
|1990 P02|Utilities| |
|1990 P03|Production| |
|1990 P04|Electrical| |
|1990 P05|Packaging| |
|1990 P06|Civil| |
|1990|Mechanical Planner| |
|1990|Electrical Planner| |
|1990|Civil Planner| |
|1991 P01|Mechanical| |
|1991 P02|Utilities| |
|1991 P03|Production| |
|1991 P04|Electrical| |
|1991 P05|Packaging| |
|1991 P06|Civil| |

# Define Plant Section

SPRO SAP Reference IMG Plant maintenance and customer service Master data in plant maintenance and customer service Technical Object General Data Define Plant Section

Transaction Code: SPRO

Transport Request: Configurati Define Plant Section

OLAM/DFM/SAP/PM/Configuration Document

Page 8 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Description

Display View "Plant Sections": Overview

|Plnt|Plant ction|PersResponsible|Phone|
|---|---|---|---|
|1990|010|Frau X|123|
|1991|010|Frau X|123|
|1992|010|Frau X|123|
|1990|010|Frau X| |
|1991|010|Frau X| |
|1992|010|Frau X| |

# 6. Types of Technical Objects

Plant Maintenance & CS &gt; Master Data in Plant Maintenance & CS &gt;

Menu Path Technical Objects &gt; General Data &gt; Define Types of Technical Objects

Transaction SPRO

Code

Transport Request

Configuration

Description

OLAM/DFM/SAP/PM/Configuration Page 9 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Display View 'Types of Technical Objects' Overview

|Object Type|Description|
|---|---|
|PACKAGING|PACKAGING EQUIPMENT|
|PACKING|Packing machine|
|PACKING MC|Packing Machines|
|PACKING MC|PACKING MACHINE|
|PACKLINE|Packing Line|
|PADDY DRYR|Paddy Dryers|
|PADDY SEPR|Paddy Seperator|
|PALETISEUR|PALETISEUR|
|PALETROLY|Pallet Trolley|
|PALETTRUCK|PALETTE TRUCK|
|PANEL|PANEL|
|PANEL CONT|Panel Controller|
|PANELS|Panels|
|PANEL CTRL|CONTROL PANEL|
|PANEL ELEC|ELECTRICAL PANELS|
|PANEL INST|INSTRUMENT PANEL|
|ROASTER|ROASTER|
|GRINDER|GRINDER|
|EXTRACTION|EXTRACTION|
|PACKAGING|PACKAGING|
|SILOS|SILOS|
|GRADING|GRADING|
|CLEANING|CLEANING EQUIPMENT|
|DRYING|DRYING EQUIPMENT|
|HULLING|HULLING|
|POLISH|POLISHING MACHINES|
|PULPERS|PULPERS|

OLAM/DFM/SAP/PM/Configuration Page 10 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# BLEND MIX

# BLEND MIXERS

# POWDER

# FILL

# POWDER FILLING MACHINE

# COOL EQUIP

# COOL EQUIPMENT

# SEAL

# SEALING MACHINE

# 7. Structure Indicator

Plant Maintenance & CS &gt; Master Data in Plant Maintenance & CS &gt; Technical Objects &gt; Functional Locations &gt; Create Structure Indicator for Reference Locations/Functional Locations

Transaction SPRO

Code

Transport Request

Configuration Description

Change View "Functional Location Structure Indicators Details

|StrIndicator|9901|
|---|---|
|StructIndText|Structure Indicator for 55 &amp; 65 Carrier|
|Structure Edit mask|XXXX-XXXX-XXX-XXXX|
|HierLevels| |

# 8. Functional location Category

Menu Path Plant Maintenance & CS &gt; Master Data in Plant Maintenance & CS &gt; Technical Objects &gt; Functional Locations &gt; Define Category of Functional Location

OLAM/DFM/SAP/PM/Configuration Page 11 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Transaction Code

SPRO

# Transport Request

# Configuration

Description

No Change

# Change View "Functional Location Category": Overview

# New Entries

|Categ|Description|
|---|---|
|Block|Technical system standard|
|Production zone|Meteorological station|

# Change View "Functional Location Category

# New Entries

|FunctLocCat:|Functional Location Category|Description|
|---|---|---|
|Technical system standard|ChangeDocuments|CustObject|
|Other data|Status Profile|PartnDet Proc:|
|Object info|MeasPtCategory|Viewprofile|
|SIANDARD|SIANDARD|SIANDARD|
|Change Docs During Creation|Change Docs During Creation|Change Docs During Creation|

# OLAM/DFM/SAP/PM/Configuration

Page 12 of 64

Version 4.0

Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

# 9. Maintain Equipment Category

Plant Maintenance & CS &gt; Master Data in Plant Maintenance & CS &gt; Technical Objects &gt; Equipment &gt; Equipment Categories &gt; Maintain Equipment Category

Transaction Code: SPRO

Transport Request:

Configuration Description: No Change

# Change View "EquipCategories" : Overview

|EquipCategories|Equipment CatDesc:|
|---|---|
|B|Machines|
|C R|Admin Equipments|
| |Customer equipment|
|F Machines|External Equipment|
|M Machines|Fleet|
| |Machines|
| |Production resources/tools|
| |Test/measurement equipment|
|Customer -pment|Customer equipment|
|Z Machines|Chemical Application Tanks|

# 10. Maintenance Processing - Define Notification Types

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt; Notification Creation &gt; Notification Types &gt; Define Notification Types

Transaction Code: SPRO

Transport Request:

Configuration: OLAM/DFM/SAP/PM/Configuration

Page 13 of 64

Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Description

No Change

# Change View "Notification Types": Overview

|Typ|Notification Type|Notif. Category|
|---|---|---|
|N1|'JT-Maintenance Reqst|Maint; Notification|
|N2|GT-Malfunction Rept:|Maint; Notification|
|N3|GT-Activity Report|Maint; Notification|
|N4|GT-Predictive Maint:|Maint; Notification|

# Display View "Notification Types" Details

|Notification type|GT-Malfunction Rept.|
|---|---|
|Notif.cat|Maint: Notification|
|Parameters| |
|Notification origin|02 Malfunction eport|
|Reference time|Malfunction start|
|Catalog profile|OLAKEKOOI Olam PM Catalog Profile|
|Update group (stats)|PMIS: Genera|
|Process| |
|Earky no alloc:|Number rnge|

# Display View "Catalog profiles'" Overview

|Catalog profiles|Cat Prof.|Catalog profile|
|---|---|---|
|Catalogs code grou|OLAKEXOOI|Olam PM Catalog Profile|

OLAM/DFM/SAP/PM/Configuration Page 14 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# 11. Maintenance Processing - Assign Notification Types to Order Types

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt; Menu Path Notification Creation &gt; Notification types &gt; Assign Notification Type to Order type

Transaction Code: SPRO

Transport Request: Configuration

Description: No Change

# Display View "Order Type by Notification Type Overview

|Typ|Notification type|Type Order type|text|
|---|---|---|---|
|GT-Maintenance Reqst|ZO1|Preventive Maintenence Order| |
|GT-Malfunction Rept:|Zx02|Breakdown Maintenance order| |
|GT-Activity Report|ZvO1|Preventive Maintenence Order| |
|GT-Predictive Maint:|Zv02|Breakdown Maintenance order| |

# 12. Maintenance Processing - Notification Content

Menu Path: Plant Maintenance & CS &gt; Maintenance and Service Processing &gt; Notification Creation &gt; Notification Content &gt; Maintain Catalog

Transaction Code: SPRO

Transport Request: Configuration

Description: No change

OLAM/DFM/SAP/PM/Configuration Page 15 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Change View "Catalog types" Overview

# New Entries

|Catalog|Short text for the catalog|Keyword|
|---|---|---|
|Action Reasons|Action| |
|Characteristic Attributes|Attribute| |
|Tasks|Task| |
|Usage Decisions|Decision| |
|Events|Event| |
|Causes|Cause| |
|Results of Defects|Results(Def)| |
|Hold Codes|Hold| |
|Activities (QM)|Activity QM| |
|Defect Types|Defect Type| |
|Activities (PM)|Activity PM| |
|Object Parts|Object Part| |
|Overview of Damage|Damage| |

# Maintenance Processing - Notification Content - Define Catalog Profile

Plant Maintenance & CS > Maintenance and Service Processing > Notification Creation > Notification Content > define Catalog Profile

Transaction Code: SPRO

Transport Request:

Configuration Description: No Change

OLAM/DFM/SAP/PM/Configuration

Page 16 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Display View "Catalogs / code groups Overview

# @ B

# Dialog Structure

# Catalog profiles

# Catalog profile OLAKEXOOI Olam PM Catalog

# Catalogs code grou

# Ca . Code group

# 14. Maintenance Processing - Notification Content – Catalogs for Notification types.

Menu Path Plant Maintenance & CS > Maintenance and Service Processing >

# OLAM/DFM/SAP/PM/Configuration

Page 17 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Notification Creation > Notification Content > Change Catalogs and Catalog Profile for Notification Type

# Transaction Code

SPRO

# Transport Request

No Change.

# Configuration Description

# Change View "Catalogs for notification types" Overview

|Notification Type|Notif, Category|
|---|---|
|NL|GT-Maintenance Reqst|
|N2|GT-Malfunction Rept:|
|N3|GT-Activity Report|
|N4|GT-Predictive Maint.|

# Change View "Catalogs for notification types' Details

|Notification Type|Notification type|Catalog profile|
|---|---|---|
|N2|GT-Malfunction Rept.|01|
| |Maint; Notification|OLAMPMOO1|

# Catalogs for Coding

|Coding|Overview of Damage Causes|Tasks|Activities|Object Parts|Class active|
|---|---|---|---|---|---|
| | | |(PM)| | |

OLAM/DFM/SAP/PM/Configuration Page 18 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# 15. Maintenance Processing - Notification Processing

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Notification Processing &gt; User Status for Notifications &gt; Define User Status &gt;

Transaction Code: SPRO

Transport Request Configuration: Define User Status Profile for Notifications

# Description

Change Status Profile: Overview

|Status Profile|Text|
|---|---|
|EvoOOOOl|Plant Maintenance Operations|

Display Status Profile: User Status

# Object Types

|Status Profile|Maintenance Language|User Status|
|---|---|---|
|PMOOOO01|EN English|Status|

|Status Short Text|Long Text|Init|Lowest Position|Highest Position|Priority|Auth. code|
|---|---|---|---|---|---|---|
|SFEM|Employee Safety| | | | | |
|SFFS|Food Safety| | | | | |

Assign User Status to Notification Types

OLAM/DFM/SAP/PM/Configuration Page 19 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Display View "Status profile of notifications" : Overview

|Typ|Notification type|Notif.cat|
|---|---|---|
|Nl|GT-Maintenance Reqst|Maint, Notification|
|N2|GT-Malfunction Rept:|Maint, Notification|
|N3|GT-Activity Report|Maint, Notification|
|N4|GT-Predictive Maint|Maint, Notification|

# Display View "Status profile of notifications' Details

Notifictn type
N2
Notif.cat
01
Maint; Notification

# Status profile for notifications

Status Profile
PMOOOO01
Plant Maintenance Operations

# Status profile for tasks

Status Profile
ZPMTASK
PM Task Status

OLAM/DFM/SAP/PM/Configuration Page 20 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

# 16. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Maintenance and Service Orders &gt; Functions and Settings for Order Types &gt; Configure Order Types

Transaction SPRO

|Code|Transport Request|Configuration Description|
|---|---|---|
|Display View "Maintenance Order Types'| |Overview|

|Order Type|Text|
|---|---|
|ZMO1|Preventive Maintenance Order|
|ZMO2|Breakdown Maintenance Order|
|ZMO3|Shutdown Maintenance Order|
|ZMO4|Refurbishment Maintenance Order|
|IzMo5|Calibration Maintenance Order|

OLAM/DFM/SAP/PM/Configuration Page 21 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# 17. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Maintenance and Service Orders &gt; Functions and Settings for Order Types &gt; Assign Order Types to Maintenance Plants

Transaction SPRO

Code

Transport Request

Configuration

# Display View "Valid Order Types by Planning Plant = Overview

|E @ B|PIPI Name|Type|Order type text|
|---|---|---|---|
|1990 #55 &amp; #65 Carrier Dr|ZMO1|Preventive Maintenance Order| |
|1990 #55 &amp; #65 Carrier Dr|ZMO2|Breakdown Maintenance order| |
|1990 #55 &amp; #65 Carrier Dr|ZMO3|Shutdown Maintenance order| |
|1990 #55 &amp; #65 Carrier Dr|ZMO4|Refurbishment Maintenance Order| |
|1990 #55 &amp; #65 Carrier Dr|ZMO5|Calibration Maintenance Order| |

OLAM/DFM/SAP/PM/Configuration Page 22 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# 18. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Maintenance and Service Orders &gt; Functions and Settings for Order Types &gt; Availability Check for Material, PRTs, and Capacities &gt; Define Inspection Control

Transaction SPRO

Code

Transport Request

# Configuration Display View "Order control Overview

|Plant Description|Type|Busin. Text|
|---|---|---|
|990 #55 &amp; #65 Carrier Dr|ZIO1|Check availabilty during orde|
|1990 #55 &amp; #65 Carrier Dr|ZIO1 2|Check availabiity during orde|
|1990 #55 &amp; #65 Carrier Dr|ZI02|Check availabilty during orde|
|1990 #55 &amp; #65 Carrier Dr|ZIO2 2|Check availability during orde|
|1990 #55 &amp; #65 Carrier Dr|ZMOI|Check availability during orde|
|1990 #55 &amp; #65 Carrier Dr|ZMO1 2|Check availabilty during orde|
|990 #55 &amp; #65 Carrier Dr|ZMO2|Check availability during orde|
|1990 #55 &amp; #65 Carrier Dr|ZMO2|Check availability during orde|
|990 #55 &amp; #65 Carrier Dr|ZMO3|Check availability during orde|
|1990 #55 &amp; #65 Carrier Dr|ZM03|Check availabilty during orde|
|990 #55 &amp; #65 Carrier Dr|ZMOS|Check availabilty during orde|
|hs9o [75 &amp; #65 Carrier Dr|ZMO5 2|Check availabilty during orde|

# 19. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Maintenance and Service Orders &gt; Functions and Settings for Order Types &gt; Control Key &gt; Maintain Default Values for Control Keys for Order Types

Transaction SPRO

Code

Transport Request

OLAM/DFM/SAP/PM/Configuration Page 23 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Display View "Control Key Default": Overview

|Planning plant|Order Type|Text|
|---|---|---|
|1990|ZMO1|Preventive Maintenence Order|
|1990|ZMO2|Breakdown Maintenance order|
|1990|ZM03|Shutdown Maintenance order|
|1990|ZM04|Refurbishment Maintenance Order|
|1990|ZMOS|Calibration Maintenance Order|

# 20. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS > Maintenance and Service Processing > Menu Path Maintenance and Service Orders > General Data > User Status for Orders > Define Status Profile

Transaction Code: SPRO

Transport Request:

# Configuration

Define User Status Profile for Orders

OLAM/DFM/SAP/PM/Configuration Document

Page 24 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Change Status Profile: User Status

# Object Types

Status Profile: ZEMWRECR PM Work Order status

Maintenance Language: English

# User Status

|Stat|Status Short Text|Lon:|Init:|Lowes:|Highes:|Posi:|Prio:|
|---|---|---|---|---|---|---|---|
|PERK|Permanent Repairs| | | | | | |
|TEXP|Temporary Repairs| | | | | | |
|NISI|No Status| | | | | | |
|INER|Work In Progress| | | | | | |
|HYAT|Waiting for Material| | | | | | |
|WECO|Waiting for Plant Condition| | | | | | |
|WINS|Waiting For Inspection| | | | | | |
|RIC|Ready to be Closed| | | | | | |
|CANC|Order Canceled| | | | | | |

# Assign User Status to Order Types

# Change View "Status Profile f. MaintOrders Overview

|Type Name|Stat Prof:|Description|pStatProf Description|
|---|---|---|---|
|ZMO1|Preventive Maintenance Order|ZPMRRORZ|PM Work Order status testl|
|ZMO2|Breakdown Maintenance order|ZPMWRKOR|PM Work Order status|
|ZMO3|Shutdown Maintenance order|ZPMWRKOR|PM Work Order status|
|ZMO4|Refurbishment Maintenance|ZPMWRKOR|PM Work Order status|
|ZMO5|Calibration Maintenance Order|ZPMWRKOR|PM Work Order status|

OLAM/DFM/SAP/PM/Configuration Page 25 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# 21. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Maintenance and Service Orders &gt; Scheduling &gt; Set Scheduling Parameters

Transaction SPRO

Code

Transport Request

# Configuration Display View "Specify scheduling parameters Overview

|Plant Ord.|PrSch|Prod. Scheduler|
|---|---|---|
|h99o|1990|ZMO2|
| |1990|ZM03|
| |1990|ZMO4|
| |1990|ZMOS|

For Order Types - ZM01, ZM02, ZM03, ZM04 &amp; ZM05

For Order Type – ZM01:

OLAM/DFM/SAP/PM/Configuration Page 26 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Display View "Specify scheduling parameters

|Plant|Tp1990 /3;5 & #65 Carrier Dr|
|---|---|
|Order type|ZMO1|
|Preventive Maintenance Order| |
|Prodn Superv.| |
|Adjust scheduling| |
|Adjust Dates|Do not adjust basic dates dep regmts to order start|
|Scheduling control for detailed scheduling| |
|Scheduling Type|Forwards in time|
|Automatic Scheduling| |
|Start in the Past|30|
|Automatic log| |
|Scheduling with breaks| |
|Shift Order| |
|Latest Staging Date| |

# 22. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS > Maintenance and Service Processing >

Menu Path Completion Confirmations> Define Control Parameters for Completion Confirmations

Transaction SPRO

Code

Transport Request

Configuration Description

OLAM/DFM/SAP/PM/Configuration

Page 27 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Display View "Confirmation Parameters Overview

|Order category|Plant/Order Type|Plant Name|Type|Description of Order Type|
|---|---|---|---|---|
|30|SMO1|1990 #55 & #65 Carrier Dr|Service order| |
|30|SMO2|1990 #55 & #65 Carrier Dr|Service order (with revenues)| |
|30|SMO3|1990 #55 & #65 Carrier Dr|Repair service| |
|30|ZMO1|1990 #55 & #65 Carrier Dr|Preventive Maintenance Order| |
|30|ZMO2|1990 #55 & #65 Carrier Dr|Breakdown Maintenance order| |
|30|ZMO3|1990 #55 & #65 Carrier Dr|Shutdown Maintenance order| |
|30|ZMO4|1990 #55 & #65 Carrier Dr|Refurbishment Maintenance Order| |
|30|ZMO5|1/990 15 & #65 Carrier Dr|Calibration Maintenance Order| |

# Maintenance Processing – Maintenance plans

Plant Maintenance & CS > Maintenance Plans, Work Centers, Task Lists and PRTs > Maintenance Plans > Define Sort Fields for Maintenance Plan

Transaction Code: SPRO

Transport Request:

Configuration Description: OLAM/DFM/SAP/PM/Configuration

Page 28 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Change View "Maintenance Plan Sort Field" Overview

|MaintPlan sort field|Description maintenance plan sort field|
|---|---|
|1990|65 Carrier Dr & 65 Carrier Dr|
|1991|101 Claireville|
|1992|160 Claireville|

# Work Center – Responsible Person

Plant Maintenance & CS > Maintenance Plans, Work Centers, Task Lists and PRTs > Work Centers > General Data> Define Employee Groups Responsible for Work Centers

Menu Path: Transaction SPRO

Code: Transport Request

# Change View "Person Responsible for Work Center" Overview

|Plnt|Pers respons|Person responsible for work center|
|---|---|---|
|1990|001|Department Head-Production line|
|1990|002|Department Head ~Labelling line|
|1990|BaG|Building & Grounds|
|1990|EsI|Electrical & Instrumentation|
|1990|MEC|Mechanic|
|1990|PRO|Projects|

OLAM/DFM/SAP/PM/Configuration Page 29 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# 25. Maintenance Processing – Maintenance & Service Orders

Menu Path: Plant Maintenance & CS &gt; Maintenance and Service Orders &gt; General Data &gt; Activate Default Value for Current Date as Basic Date

Transaction: SPRO

Code

Transport Request

Configuration

|Description|B|D|E|
|---|---|---|---|
|Planning plant Default current date|1990|1991|1992|

# 26. Maintenance Processing – Maintenance & Service Orders

Menu Path: Plant Maintenance & CS &gt; Maintenance and Service Orders &gt; General Data &gt; Define Default Values for Units for Operation

Transaction: SPRO

Code

Transport Request

Configuration

Description

OLAM/DFM/SAP/PM/Configuration Page 30 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Display View "Operation units for duration/work" Overview

|Planning plant|Norm.duratn un_|Unit text|Unit for work|Unit text|
|---|---|---|---|---|
|h199o|Hours|HR|Hours| |
|1991|HR|Hours|HR|Hours|
|1992|HR|Hours|HR|Hours|

# 27. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS > Maintenance and Service Orders>

Menu Path Functions and Settings for Order Types> Default Values for Task List

Data and Profile Assignments

Transaction SPRO

Code

Transport Request

# Configurati Display View "Screen Ref: Object; General Profiles, Task List Presetti

|Plant Ord.|Short Text|
|---|---|
|1990|ZMOI Preventive Maintenence Order|
|1990|ZMO2 Breakdown Maintenance order|
|990|zMok3 Itdown Maintenance order|
|1990|ZM04Refurbishment Maintenance Order|
|1990|ZMOS Calbration Maintenance Order|

# 28. Maintenance Processing – Planner group in Task list

Menu Path Plant Maintenance & CS > Maintenance Plans, Work Centers, Task Lists and PRTs> Task Lists> General Data > Configure Planner Group

OLAM/DFM/SAP/PM/Configuration Page 31 of 64 Version 4.0 Document
---
# Configuration Document

# Project: Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Transaction SPRO

# Code

# Transport Request

# Configuration

# Display View "Maintenance planner group Overview"

|Description|Plnt|PIGrp|Planner Group Description|
|---|---|---|---|
| |1990|CHI|Planner Chile Pepper|
| |1990| |Mechanical|
| |1990| |Electrical|
| |1990|P3|Civil|
| |1990|P4|Civil planner|

# 29. Quality Inspection – Inspection lot Completion

# Menu Path

Quality Management > Quality Inspection > Inspection lot Completion > Define Follow up actions

# Transaction SPRO

# Code

# Transport Request

# Configuration

OLAM/DFM/SAP/PM/Configuration

Page 32 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Change View "Function modules Overview

# New Entries EK

# Dialog Structure

# Follow-up actn QM PM

# Update Maintenance Data

# Follow-up actions

# Function modules

|Cntr|Function Module|AftrPst|SyncUpdt|BTran|Short text for function module|
|---|---|---|---|---|---|
|pFOA|QMCHAR|To PM POINTS| | |Follow-Up Action: Transfer of|
|QFOA_|OBJECT STATUS SET| | | |Follow-Up Action: Set Equipmer|
|QFOA_|ORDER TECHNICAL COMPLETE| | | |Follow-Up Action: Technically|

# Version 2.0

# 30. Define Location

# Menu Path

SAP Customizing Implementation Guide &gt; Enterprise Structure &gt; Definition &gt; Logistics General &gt; Define Location

# Transaction Code

SPRO

# Transport Request

Configuratio Define Location:

OLAM/DFM/SAP/PM/Configuration

Page 33 of 64

# Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

# Change View "Locations": Overview

# New Entries

|Plnt|Location|Name|
|---|---|---|
|1990|BDG|Building|
|1990|CHILE|US-Chile Pepper|
|1990|CLEN|Cleaning|
|1990|FIL|Filling|
|1990|FLV|Flavour|
|1990|GBN|Green bean|
|990|GRD|Grinding|
|1990|MACS|Machine shop|
|1990|MILA|Milling A|
|1990|MILB|Milling|
|1990|MILC|Milling C|
|1990|MILD|Milling D|
|1990|MILE|Milling E|
|1990|PCK|Packing|
|1990|PRD|Production|
|1990|RST|Roasting|
|990|WHO|Warehouse|
|1990|WORK|Work shop|
|1991|PRD|Production|
|1991|QCO|Quality Control|
|1991|UTL|Utility|

OLAM/DFM/SAP/PM/Configuration           Page 34 of 64        Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

|OLAM/US/SAP/PM|PM – Configuration Document| | |
|---|---|---|---|
| |1991|QCO|Quality Control|
| |1992|PRD|Production|
| |1992|UTL|Utility|
| |1992|WHO|Warehouse|
| |1992|QCO|Quality Control|
| |1990|PRD|Production|
| |1990|WHO|Warehouse|
| |1990|RST|Roasting|
| |1990|GRD|Grinding|
| |1990|GBN|Green bean|
| |1990|CMN|Common|
| |1990|BDG|Building|
| |1990|FIL|Filling|

# 31. Planner Group

SAP Customizing Implementation Guide Plant Maintenance and Customer Service Master Data in Plant Maintenance and Customer Service Technical Objects General Data Define Planner Groups

Transaction Code: SPRO

Transport Request

Configuration

Description: Define Planner Groups

OLAM/DFM/SAP/PM/Configuration Page 35 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Change View "Maintenance planner groups" Overview

|New Entries|EX|Ex|Name|Telephone|
|---|---|---|---|---|
|PIPI|PG|1990|ELE|Electrical|
|1990|MEC|Mechanical| | |
|1990|P1|Mechanical Planner| | |
|1990|P2|Electrical Planner| | |
|1990|P3|Civvil Planner| | |
|1990|TCL|Technical Cell Lead| | |
|991|ELE|Electrical| | |
|991| |Mechanical| | |
|1991|PO1|Mechanical| | |
|1991|PO2|Utilities| | |
|1991|P03|Production| | |
|1991|P04|Electrical| | |
|1991|P05|Packaging| | |
|1991|P06|Civvil| | |
|1991|P1|Mechanical Planner| | |
|1991|P2|Electrical Planner| | |
|1991|P3|Civil Planner| | |

|Plant|Planner Group|Description|
|---|---|---|
|1991|MEC|Mechanical|
|1991|ELE|Electrical|
|1991|TCL|Technical Cell lead|
|1990|MEC|Mechanical|
|1990|ELE|Electrical|
|1990|TCL|Technical Cell lead|
|1992|MEC|Mechanical|
|1992|ELE|Electrical|
|1992|TCL|Technical Cell lead|
|1990|MPL|Maintenance Planner|

OLAM/DFM/SAP/PM/Configuration Page 36 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM  PM – Configuration Document

# 32. Define Plant Section

SPRO   SAP Reference IMG   Plant maintenance and customer service

Menu Path: Master data in plant maintenance and customer service Technical Object General Data Define Plant Section

Transaction Code: SPRO

Transport Request:

# Configuration

Define Plant Section

# Description

Display View "Plant Sections": Overview

|Plant section|Pers Responsible|Phone|
|---|---|---|
|1990 010|Frau X|123|
|1990 106|Head Maint|123|
|1990 107|Head Engg|123|
|1991 010|Frau X|123|
|1991 106|Head Maint|123|
|1991 107|Head Engg|123|
|1992 010|Frau X|123|
|1992 106|Head Maint|123|
|1992 107|Head Engg|123|
|1993 010|Frau X|123|
|1994 010|Frau X|123|
|1995 010|Frau X|123|

|Plant|Plant section|Person Responsible|
|---|---|---|
|1991|106|Head Maint|
|1991|107|Head Engg|
|1992|106|Head Maint|
|1992|107|Head Engg|
|1990|106|Head Maint|

OLAM/DFM/SAP/PM/Configuration Page 37 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# 1990 107 Head Engg

# 33. Structure Indicator

Plant Maintenance & CS &gt; Master Data in Plant Maintenance & CS &gt; Menu Path Technical Objects &gt; Functional Locations &gt; Create Structure Indicator for Reference Locations/Functional Locations

Transaction: SPRO

Code

Transport Request

# Configuration Description

Change View "Functional Location Structure Indicators": Details

|New Entries|[63|
|---|---|
|StrIndicator|1990|
|StructIndText|[55 Carrier Dr &amp; 65 Carrier Dr|
|Structure Edit mask|XXXX-XXX|
|HierLevels| |
|Identifying Lvl|Ident: Label|
|Znd Ident: Lvl|Znd Iden: Label|

OLAM/DFM/SAP/PM/Configuration Page 38 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Change View "Functional Location Structure Indicators" Details

# New Entries

|StrIndicator|1991|
|---|---|
|StructIndText|Iho1 Claireville|
|Structure| |
|Edit mask|XXXX-XXXX-XXX-XXXX|
|HierLevels|2|
|Identifying Lvl|Ident: Label|
|Znd Ident; Lvl|Znd Iden: Label|

# Change View "Functional Location Structure Indicators" Details

# New Entries

|StrIndicator|1992|
|---|---|
|StructIndText|0160 Claireville|
|Structure| |
|Edit mask|XXXX-XXXX-XXX-XXXX|
|HierLevels| |
|Identifying Lvl|Ident; Label|
|Znd Ident; Lvl|Znd Iden: Label|

# 34. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS > Maintenance and Service Processing >

Menu Path Maintenance and Service Orders > Functions and Settings for Order Types > Assign Order Types to Maintenance Plants

# OLAM/DFM/SAP/PM/Configuration

Page 39 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Transaction Code

SPRO

# Transport Request

Configuration

# Display View "Valid Order Types by Planning Plant"

|PIPI Name|Type|Order type text|
|---|---|---|
|41991 01 Claireville|ZMO1|Preventive Maintenence Order|
|1991 #101 Claireville|ZMO2|Breakdown Maintenance order|
|1991 #101 Claireville|ZMO3|Shutdown Maintenance order|
|1991 #101 Claireville|ZM0 4|Refurbishment Maintenance Order|
|1991 #101 Claireville|ZMO 5|Calibration Maintenance Order|
|1992 160 Claireville|ZMO1|Preventive Maintenence Order|
|1992 160 Claireville|ZMO2|Breakdown Maintenance order|
|1992 160 Claireville|ZMO 3|Shutdown Maintenance order|
|1992 #160 Claireville|ZM0 4|Refurbishment Maintenance Order|
|1992 #160 Claireville|ZMO 5|Calibration Maintenance Order|

# 35. Maintenance Processing – Maintenance & Service Orders

Menu Path: Plant Maintenance & CS > Maintenance and Service Processing >

OLAM/DFM/SAP/PM/Configuration

Page 40 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Maintenance and Service Orders > Functions and Settings for Order Types > Availability Check for Material, PRTs, and Capacities > Define Inspection Control

|Transaction Code|Transport Request|Configuration Description|
|---|---|---|
|SPRO| |New Entries: Overview of Added Entries|

|Plant Description|Type|Business Text|
|---|---|---|
|11991 01 Claireville|ZMO1|Check availability during order|
|1991 #101 Claireville|ZMO1|Check availability during order|
|1991 #101 Claireville|ZMO2|Check availability during order|
|1991 #101 Claireville|ZMO2|Check availability during order|
|1991 #101 Claireville|ZMO3|Check availability during order|
|1991 #101 Claireville|ZMO3|Check availability during order|
|1991 #101 Claireville|ZMO4|Check availability during order|
|1991 #101 Claireville|ZMO4|Check availability during order|
|1991 #101 Claireville|ZMO5|Check availability during order|
|1991 #101 Claireville|ZMO5|Check availability during order|

|Plant Description|Type|Business Text|
|---|---|---|
|11992 60 Claireville|ZMO1|Check availability during order|
|11992 #160 Claireville|ZMO1|Check availability during order|
|1992 #160 Claireville|ZMO2|Check availability during order|
|1992 #160 Claireville|ZMO2|Check availability during order|
|1992 #160 Claireville|ZMO3|Check availability during order|
|1992 #160 Claireville|ZMO3|Check availability during order|
|1992 #160 Claireville|ZMO4|Check availability during order|
|1992 #160 Claireville|ZMO4|Check availability during order|
|1992 #160 Claireville|ZMO5|Check availability during order|
|1992 #160 Claireville|ZMO5|Check availability during order|

OLAM/DFM/SAP/PM/Configuration Document

Page 41 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

# 36. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Maintenance and Service Orders &gt; Functions and Settings for Order Types &gt; Control Key &gt; Maintain Default Values for Control Keys for Order Types

Transaction SPRO

|Code|Transport Request|Configuration|Change View "Control Key Default Overview|Description|
|---|---|---|---|---|
|5 E B|[63| | | |
|1990|ZMO2|Breakdown Maintenance order| | |
|1990|ZMO3|Shutdown Maintenance order| | |
|1990|ZMO4|Refurbishment Maintenance Order| | |
|1990|ZMO5|Calibration Maintenance Order| | |
|1991|ZMO1|Preventive Maintenence Order| | |
|1991|ZMO2|Breakdown Maintenance order| | |
|1991|ZMO3|Shutdown Maintenance order| | |
|1991|ZMO4|Refurbishment Maintenance Order| | |
|1991|ZMO5|Calibration Maintenance Order| | |
|1992|ZMO1|Preventive Maintenence Order| | |
|1992|ZMO2|Breakdown Maintenance order| | |
|1992|ZMO3|Shutdown Maintenance order| | |
|1992|ZMO4|Refurbishment Maintenance Order| | |
|1992|[05|Calibration Maintenance Order| | |

# 37. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Processing &gt;

Menu Path Maintenance and Service Orders &gt; Scheduling &gt; Set Scheduling Parameters

Transaction SPRO

Code

Transport

OLAM/DFM/SAP/PM/Configuration

Page 42 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document Request

# Configuration Change View "Specify scheduling parameters": Overview

|Plant|Order|Prod. Supervisor|
|---|---|---|
|41991|991 ZMO2| |
| |1991 ZM03| |
| |991 ZMO4| |
| |991 ZMO5| |
| |992 ZMO1| |
| |992 ZMO2| |
| |992 ZM03| |
| |1992 ZMO4| |
| |992 ZMO5| |

# For Order Types - ZM01, ZM02, ZM03, ZM04 & ZM05

# For Order Type – ZM01:

# Change View "Specify scheduling parameters": Details

|Plant|Order type|Prodn Supervisor|
|---|---|---|
|1991|ZM01|Preventive Maintenance Order|

# Adjust scheduling

# Adjust Dates

Adjust basic dates, adjust dep. reqmts to operation date

# Scheduling control for detailed scheduling

|Scheduling Type|Forwards in time|Automatic Scheduling|
|---|---|---|
|Start in the Past|30|Automatic log|
|Scheduling with breaks|Shift Order|Latest Staging Date|

# OLAM/DFM/SAP/PM/Configuration

Page 43 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Change View "Specify scheduling parameters"

# Details

|Plant|1992|#160 Claireville|
|---|---|---|
|Order type|ZMO1|Preventive Maintenance Order|
|Prodn Superviso| | |
|Adjust scheduling| | |
|Adjust Dates|IAdjust basic dates, adjust dep. reqmts to operation date|IAdjust basic dates, adjust dep. reqmts to operation date|
|Scheduling control for detailed scheduling| | |
|Scheduling Type|Forwards in time|Automatic Scheduling|
|Start in the Past|30|Automatic log|
|IScheduling with breaks|IScheduling with breaks|IScheduling with breaks|
|Shift Order|Shift Order|Shift Order|
|Latest Staging Date|Latest Staging Date|Latest Staging Date|

# Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS > Maintenance and Service Processing >

Menu Path Completion Confirmations> Define Control Parameters for Completion Confirmations

Transaction SPRO

Code

Transport Request

Configuration Description

OLAM/DFM/SAP/PM/Configuration

Page 44 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Display View "Confirmation Parameters": Overview

|Order category|Plant|Name|Type|Description of Order Type|
|---|---|---|---|---|
|30 Maintenance order|1991|#101 Claireville|ZMO1|Preventive Maintenance Order|
| |1991|#101 Claireville|ZMO2|Breakdown Maintenance order|
| |1991|#101 Claireville|ZMO3|Shutdown Maintenance order|
| |1991|#101 Claireville|ZMO4|Refurbishment Maintenance Order|
| |1991|#101 Claireville|ZMO5|Calibration Maintenance Order|
| |1992|#160 Claireville|ZMO1|Preventive Maintenance Order|
| |1992|#160 Claireville|ZMO2|Breakdown Maintenance order|
| |1992|#160 Claireville|ZMO3|Shutdown Maintenance order|
| |1992|60 Claireville|ZMO4|Refurbishment Maintenance Order|
| |11992|#160 Claireville|ZMO5|Calibration Maintenance Order|

OLAM/DFM/SAP/PM/Configuration Page 45 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Display View "Confirmation Parameters": Details

|Order category| |30 Maintenance order|
|---|---|---|
|Plant|1991|L01 Claireville|
|Order Type| |ZMO1 Preventive Maintenence Order|

# Default Values

|IFinal Confirmation|OAII Components|
|---|---|
|Clear Open Reservs:| |
|Propose Dates|Selection|
|Propose Activities|Iconfirmable|
|Calc: performance|Confirmed Ops|

# Checks

|WrkDev. active|Work Deviation|
|---|---|
|DurtnDev active|Duration Deviatn|
|Dates in Future|Confirmation (QM)|

# Logs/Error Handling

|Actual Costs|No HR Update|
|---|---|
|Termination for Incorrect ActCosts| |
|Goods Movement|Control Data|
|Termination for Incorrect Goods Movt|Process Control|

# Mass Confirmation

|Rough Reversal| |
|---|---|
|Rough Reversal frm Counter Stats| |

OLAM/DFM/SAP/PM/Configuration Page 46 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Display View "Confirmation Parameters

|Order category|30 Maintenance order|
|---|---|
|Plant|1992 L60 Claireville|
|Order Type|ZMO1 Preventive Maintenance Order|

# Default Values

|IFinal Confirmation|OAII Components|
|---|---|
|Clear Open Reservs:| |
|Propose Dates| |
|Propose Activities| |
|Icalc: performance|Confirmed Ops|

# Checks

|WrkDev, active|Work Deviation|
|---|---|
|DurtnDev active|Duration Deviatn|
|Dates in Future|Confirmation (QM)|

# Logs/Error Handling

|IActual Costs|INo HR Update|
|---|---|
|Termination for Incorrect ActCosts| |
|Goods Movement|Control Data|
|Termination for Incorrect Goods Movt|Process Control|

# Mass Confirmation

IRough Reversal
Rough Reversal frm Counter Stats
# Work Center – Responsible Person

# Menu Path

Plant Maintenance & CS > Maintenance Plans, Work Centers, Task Lists and PRTs > Work Centers > General Data> Define

# OLAM/DFM/SAP/PM/Configuration

Page 47 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

# Employee Groups Responsible for Work Centers

# Transaction Code     SPRO

# Transport Request

# Configuration

# Description

# Change View "Person Responsible for Work Center": Overview

# New Entries

|Plnt|Responsible|Person responsible for work center|
|---|---|---|
|1990|001|Department Head 55 & 65|
|1990|B&G|Building & Grounds|
|1990|EcI|Electrical & Instrumentation|
|1990|HDE|HOD-Electrical|
|1990|HDM|HOD -Mechanical|
|1990|MEC|Mechanic|
|1990|PRO|Projects|
|1990|SUP|Supervisor|
|1991|001|Department Head 101|
|1991|HDE|HOD-Mechanical|
|1991|HDM|HOD-Mechanical|
|1992|001|Department Head 160|
|11992|HDE|HOD-Electrical|
|1992| |HOD-Mechanical|
|2010|001|Department Head|
|2011|001|Department Head|

# Plant       Person          Description

1990
HDM
HOD -Mechanical
OLAM/DFM/SAP/PM/Configuration              Page 48 of 64          Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

|1990|HDE|HOD-Electrical|
|---|---|---|
|1991|HDM|HOD-Mechanical|
|1991|HDE|HOD-Electrical|
|1992|HDM|HOD-Mechanical|
|1992|HDE|HOD-Electrical|

# 40. Maintenance Processing – Maintenance & Service Orders

Plant Maintenance & CS &gt; Maintenance and Service Orders&gt; Menu Path Functions and Settings for Order Types&gt; Default Values for Task List Data and Profile Assignments

Transaction SPRO

Code

Transport Request

# Configuration Change View "Screen Ref: Object; General Profiles, Task List Presetting

# Description

# New Entries

|Plant Order Short Text| | |
|---|---|---|
|1991|ZMoJ|Preventive Maintenance Order|
|1991|ZMO2|Breakdown Maintenance Order|
|1991|ZMO3|Shutdown Maintenance Order|
|1991|ZMO4|Refurbishment Maintenance Order|
|1991|ZMO5|Calibration Maintenance Order|
|1992|ZMO1|Preventive Maintenance Order|
|1992|ZMO2|Breakdown Maintenance Order|
|1992|ZMO3|Shutdown Maintenance Order|
|1992|ZMO4|Refurbishment Maintenance Order|
|1992|ZMO5|Calibration Maintenance Order|

VERSION 3.0

OLAM/DFM/SAP/PM/Configuration Page 49 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# 41. Planner Group

# SAP Customizing Implementation Guide

# Plant Maintenance and Customer Service

# Master Data in Plant Maintenance and Customer Service

# Technical Objects

# General Data

# Define Planner Groups

Menu Path

Transaction Code: SPRO

Transport Request

Configuration

# Description

Define Planner Groups

# Change View "Maintenance planner groups Overview

|New Entries|Name|Telephone|
|---|---|---|
|1199o|Maintenance Assist| |
|1990 MPL|Maintenance Planner| |
|1990 PO1|Mechanical| |
|1990 P02|Utilities| |
|1990 P03|Production| |
|1990 P04|Electrical| |
|1990 PO5|Packaging| |
|1990 PlO|Building Planner| |
|1990 Pll|Service Planner| |

|Plant|Planner Group|Description|
|---|---|---|
|1990|MNA|Maintenance Assistant|
|1992|MPL|Maintenance Planner|
|1991|MPL|Maintenance Planner|

OLAM/DFM/SAP/PM/Configuration

Page 50 of 64

Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# 42. Work Center – Responsible Person

Plant Maintenance & CS &gt; Maintenance Plans, Work Centers, Task Lists and PRTs &gt; Work Centers &gt; General Data &gt; Define Employee Groups Responsible for Work Centers

Menu Path

Transaction Code SPRO

Transport Request

Configuration Description

# Change View "Person Responsible for Work Center" Overview

|Plnt Responsible|Person responsible for work center| |
|---|---|---|
|1992|HDE|HOD-Electrical|
|1992|HDM|HOD-Mechanical|
|1992| |HOD-Technical Cell Lead|
|2010|001|Department Head|
|2011|001|Department Head|
|2012|001|Department Head|
|0|0|1 ?|

# New Entries: Overview of Added Entries

|Plnt Responsible|Person responsible for work center| |
|---|---|---|
|1990|HDC|HOD Contractor|
|1990|HAD|HOD maintenance Assist|
|1990|HMM|HOD management|
|1990|HOB|HOD Operator|
|1990|HTC|HOD Technical Cell Leads|
|1990|THE|Engineering|
|1991|HOE|Engineering|
|1992|HOE|Engineering|

OLAM/DFM/SAP/PM/Configuration Page 51 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM    PM – Configuration Document

|Plant|Person responsible|Description|
|---|---|---|
|1990|HDT|HOD-Technical Cell Lead|
|1991|HDT|HOD-Technical Cell Lead|
|1992|HDT|HOD-Technical Cell Lead|
|1990|HDC|HOD Contractor|
|1990|HAD|HOD maintenance Assist|
|1990|HMM|HOD management|
|1990|HOB|HOD Operator|
|1990|HTC|HOD Technical Cell Leads|
|1990|HOE|Engineering|
|1991|HOE|Engineering|
|1992|HOE|Engineering|

# 43. Structure Indicator

Plant Maintenance & CS > Master Data in Plant Maintenance & CS >

Menu Path Technical Objects > Functional Locations > Create Structure Indicator for Reference Locations/Functional Locations

Transaction Code SPRO

Transport Request

Configuration Description

OLAM/DFM/SAP/PM/Configuration Document

Page 52 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# Change View "Functional Location Structure Indicators": Details

|StrIndicator|StructIndText|Structure|Edit mask|HierLevels|Identifying Lvl|Ident; Label|Znd Ident; Lvl|Znd Iden. Label|
|---|---|---|---|---|---|---|---|---|
|1990|55 Carrier Dr & 65 Carrier Dr| |XXXX-XXXX-XXXX-XXXX-XXXXX| | | | | |

# New Entries: Details of Added Entries

|StrIndicator|StructIndText|Structure|Edit mask|HierLevels|Identifying Lvl|Ident; Label|Znd Ident; Lvl|Znd Iden. Label|
|---|---|---|---|---|---|---|---|---|
|1991|0101 Claireville| |XXXX-XXXX-XXXX-XXXX-XXXXX| | | | | |

OLAM/DFM/SAP/PM/Configuration Page 53 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# New Entries: Details of Added Entries

|StrIndicator|14992|
|---|---|
|StructIndText|160 Claireville|
|Structure| |
|Edit mask|XXXX-XXXX-XXXX-XXXX|
|HierLevels| |
|Identifying Lvl|Ident; Label|
|Znd Ident; Lvl|Znd Iden. Label|

# Technical Object Type

Plant Maintenance & CS > Maintenance Data in plant

# Menu Path

maintenance & Customer services Technical Objects > General Data> Define type of technical Objects.

# Transaction Code

SPRO

# Transport Request

Configuration

Description

OLAM/DFM/SAP/PM/Configuration

Page 54 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# New Entries: Overview of Added Entries

|ObjectType|Description|
|---|---|
|GBND|Green Been Dumping|
|GRD|Grinders|
|RST|Roasters|
|FIL|Filling & Packaging|
|AROMA|Aroma Pack|
|CHN|Chainvey|
|FLV|Flavor System|
|PLT|Palletizer|
|RLT|Roll Lifter|
|CONVR|Conveyors|
|BE|Bucket Elevators|
|SAUG|Screw Augers|
|PNG|Pneumatic Gates|
|DOMINO|Domino|
|MARKEM|Markem|
|WBRS|WB Recovery System|

OLAM/DFM/SAP/PM/Configuration Page 55 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM  PM – Configuration Document

# New Entries: Overview of Added Entries

|ObjectType|Description|
|---|---|
|DUMP STAT|Dump Station|
|SCANNER|Scanner|
|CHAINWAY|Chain way|
|FLV SYST|Flavour System|
|POD MACH|Pod Machine|
|SARG MACH|Sarg Machine|
|VISN SYST|Vision System|
|BAGGER|Bagger|
|AUTO CATN|Auto cartoner|
|ROBOT|Robot|
|PALLETIZER|Palletizer|
|CASE PACK|Case Packer|
|ROLL LIFT|Roll Lifter|
|LASER|Laser Printer|
|OVER WRAP|Overwrapped|
|TRAYFORMER|Trayformer|

OLAM/DFM/SAP/PM/Configuration  Page 56 of 64  Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM   PM – Configuration Document

# Equipment

|Object Types|Description|
|---|---|
|Green Been|GBND - Dumping|
| |GRD - Grinders|
| |RST - Roasters|
|Filling & Packaging|FIL - Lines|
| |AROMA - Aroma Pack|
| |CHN - Chainvey|
| |FLV - Flavor System|
| |PLT - Palletizer|
| |RLT - Roll Lifter|
| |CONVR - Conveyors|
| |BE - Bucket Elevators|
| |SAUG - Screw Augers|
| |PNG - Pneumatic Gates|
| |DOMINO - Domino|
| |MARKEM - Markem|
|WB Recovery|WBRS - System|
|WB & Grnd Coffee|WBGB - Str Bins|
|Auxiliary|AUX - Equipments|

# Facility

|Object Types|Description|
|---|---|
|DUMP_STAT|Dump Station|
|SCANNER|Scanner|
|CHAINWAY|Chain way|
|FLV_SYST|Flavour System|
|POD_MACH|Pod Machine|
|SARG_MACH|Sarg Machine|
|VISN_SYST|Vision System|
|BAGGER|Bagger|
|AUTO_CATN|Auto cartoner|
|ROBOT|Robot|
|PALLETIZER|Palletizer|
|CASE_PACK|Case Packer|
|ROLL_LIFT|Roll Lifter|
|LASER|Laser Printer|
|OVER_WRAP|Overwrapped|

OLAM/DFM/SAP/PM/Configuration          Page 57 of 64       Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

- TRAYFORMER: Trayformer
- PRESTO: Presto
- CARTON:
- CLOSURE: Carton closure
- LAB_EQUIP: LAB EQUIPMENT
- LABELLER: Labeller
- INKJET: Inkjet printer
- NORDSON: Nordson Glue Pot

# Version 4.0

# 45. Define Location

Menu Path: SAP Customizing Implementation Guide &nbsp; Enterprise Structure &nbsp; Definition &nbsp; Logistics General &nbsp; Define Location

Transaction Code: SPRO

Transport Request:

# Configuration

Define Location:

OLAM/DFM/SAP/PM/Configuration &nbsp; Page 58 of 64 &nbsp; Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

|Plant|Location|Description|
|---|---|---|
|1990|QCO|Quality Control|

OLAM/DFM/SAP/PM/Configuration

Page 59 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

# 46. Define main activity type

Menu Path: Plant Maintenance and Customer Service -> Maintenance and Service Processing -> Functions and Settings for Order Types -> Maintenance Activity Type -> Define Maintenance Activity Types

Transaction Code: SPRO

Transport Request:

# Configuration

Define main activity type

# Description

Display View "Maintenance activity types' Overview

|MAT|MAT Description|
|---|---|
|1zo1|ne based inspection|
|202|Time based exchange|
|203|PDM technologies|
|204|Process conditions|
|205|Repair|
|206|Compliance|
|207|Overhaul|
|208|Pre-Engineering|
|209|Commissioning|
|Z34|Safety EHS|

OLAM/DFM/SAP/PM/Configuration Page 60 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document

# Version 5.0

# 47. Assign Valid Maintenance Activity Types to Maintenance Order Types

Plant Maintenance and Customer Service -> Maintenance and Service Processing -> Functions

Menu Path and Settings for Order Types -> Maintenance Activity Type -> Assign Valid Maintenance Activity Types to Maintenance Order Types

Transaction SPRO

|Code|Transport Request|
|---|---|
|Configurati|Assign Valid Maintenance Activity Types to Maintenance Order Types|

# Description

New Entries: Overview of Added Entries

|Type|Order type text|MAT|MAT Description|
|---|---|---|---|
|PMO1|Maintenance order|234|Safety EHS|
|ZM01| |Z34|Safety EHS|

# Version 6.0

# 48. Types of Technical Objects

Plant Maintenance & CS > Master Data in Plant Maintenance & CS > Technical Objects > General Data > Define Types of Technical Objects

Transaction SPRO

Code

Transport

# OLAM/DFM/SAP/PM/Configuration

Page 61 of 64 Version 4.0 Document
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM PM – Configuration Document Request

# Configuration Description

|Object Type|Description|
|---|---|
|UTL|UTILITIES|
|GBN|GREEN BEAN SYSTEM|
|CMN|COMMON SERVICE|
|NUSPARK|Nuspark Espresso|
|CHECKWEIGH H|Checkweigher|
|RPW|RAW AND PACKIGING WAREHOUSE|

OLAM/DFM/SAP/PM/Configuration Page 62 of 64 Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

Version 7.0

# 49. Types of Technical Objects

Plant Maintenance & CS &gt; Master Data in Plant Maintenance & CS &gt;

Menu Path Technical Objects &gt; General Data &gt; Define Types of Technical Objects

Transaction SPRO

Code

Transport Request

Configuration Description

OLAM/DFM/SAP/PM/Configuration

Page 63 of 64

Version 4.0
---
# Configuration Document

# Project : Club Coffee Plant Maintenance

# OLAM/US/SAP/PM

# PM – Configuration Document

|Object|Type|Description|
|---|---|---|
|General|General| |
|CART_CLOSE|CART_CLOSE| |

OLAM/DFM/SAP/PM/Configuration

Page 64 of 64

Version 4.0