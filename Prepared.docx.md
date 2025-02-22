# Club Coffee

# Plant Maintenance Business Blueprint Document

Prepared: Saravana raja T

Reviewed: Karthik LP

# PROJECT IDENTIFICATION

Project Name: Maple -IT Application Transition

Process Lead: Olam GT

Global Process Owner:

# DOCUMENT IDENTIFICATION

|Version|Status|Date (DD-MM-YYYY)|
|---|---|---|
|1.0|Initial Draft|26-06-2023|
|2.0|Final Draft|09-08-2023|
|2.1| | |
|2.3| | |
|2.4| | |
|3.0| | |

# REVISION HISTORY

|Version|Changes Made|
|---|---|
|1.0|Initial Draft|
| |Point 6: Safety Notification (N5) removed, 6.8 corrective notification type (N1) to be used, 6.6 capex installation is dropped handed over to finance team, 6.10 Asset disposal (N1) to be used.|
|2.0| |
|2.1| |
|2.2| |
|2.3| |
|2.4| |
|3.0| |

# SIGN OFF AND APPROVAL

|Name|Date (DD-MM-YYYY)|
|---|---|
|Global Process Owner| |

Page 1 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Contents

1. Module Overview...................................................................................................................3
2. Geographical Coverage.......................................................................................................4
3. Functional Scope...................................................................................................................4
4. Organisational Structure......................................................................................................4
5. Master Data............................................................................................................................7
6. Business Processes.............................................................................................................21
1. Preventive Maintenance – Time Based (BPML ID: 5.01)..............................................23
2. Preventive Maintenance - Performance based (BPML ID: 5.01).................................36
3. Shut Down Maintenance (BPML ID: 6.0.1)......................................................................48
4. Calibration Maintenance (BPML ID: 7.0.1)....................................................................54
5. Predictive Maintenance (BPML ID: 8.0.1)........................................................................63
6. Capex Installation process (BPML ID: 9.0.1)..................................................................66
7. Breakdown Maintenance process (BPML ID: 10.0.1).........................................................70
8. Corrective Maintenance process (BPML ID: 11.0.1)..........................................................82
9. Spares Management-Maintenance process (BPML ID: 12.0.1)...................................85
10. Asset Disposal process (BPML ID: 13.0.1)....................................................................88
11. Refurbishment process (BPML ID: 14.0.1)....................................................................91
7. Plant Maintenance Reports...............................................................................................95
8. Plant Maintenance BI / BO Reports..................................................................................97
9. GAPS......................................................................................................................................97
10. Annexure..............................................................................................................................97

Page 2 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# 1. Module Overview

SAP Plant Maintenance (henceforth shall be called as PM) module allows every maintenance
requirement to be recorded in SAP, where they are routed to the appropriate work center,
where the maintenance order is scheduled and materials are planned, work hours are
recorded, and costs are settled.

The configured SAP PM Module has capacity to manage all the routine work activities of the
Business. The maintenance group usually performs other technical activities which do not
belong to Plant Maintenance but should be performed using the same tools of maintenance
order; planning and processing can also be performed by using this SAP PM Module.

Maintenance records at the plants that are developed and maintained manually or in island
modes (legacy systems) has its own inherent limitations of not getting the information on
right time and poor and cumbersome record keeping. It is also not easy to get the desired
information like exact cost implication on any maintenance / repair activity taken place at
the time of need. Through this SAP PM Module it is expected to overcome these inherent
limitations and will maintain and deliver very high-quality real-time information and report
on all maintenance / repair activities carried out on Functional Locations & Equipments.

More stringent safety, quality assurance requirements mean there is an ever-greater
demand for regular maintenance of operating systems and equipments. Furthermore, the
status of Plant Maintenance has been significantly raised by an increase in the number of
legal and public demands for environmental protection and system safety standards.

SAP PM Module offers following business benefits:

- Uniform maintenance & reporting practice across all plants
- Real time information sharing
- On-line reporting on maintenance activities
- Integration of transactions amongst other functional departments (Finance & Accounts,
Purchase & Stores, etc.,)
- Availability of on-line maintenance history & record keeping
- Ensure & maintain visibility across all levels while conducting the best business
processes

The SAP PM module proposed to be implemented is elaborated below and in the following
sections of this document.

SAP PM Module has separate set of transactions and applications specific to each
maintenance process.

Page 3 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# 1. Current implementation scope for PM business processes are as follows:

- Preventive Maintenance-Time based
- Preventive Maintenance-Performance based
- Shutdown Maintenance
- Calibration Maintenance
- Predictive Maintenance
- Capex Installation Process
- Break-Down Maintenance
- Corrective Maintenance
- Asset Disposal
- Refurbishment

# 2. Geographical Coverage

The following entities are within the scope of PM module implementation in Club Coffee Project implementation.

|Company Code|Name|Plant Code|Name|
|---|---|---|---|
|CAF|Club Coffee|1990|55 Carrier Dr & 65 Carrier Dr|
|Club Coffee|Club Coffee|1991|101 Claireville|
|CAF|Club Coffee|1992|160 Claireville|

# 3. Functional Scope

The SAP PM module in SAP S/4 HANA addresses the various maintenance & repair activities of Functional Locations, Equipments & Sub Equipments, on a day-to-day basis.

The maintenance planning and reporting functionality of SAP PM module helps to map Plant Maintenance scenarios and capture essential information for Business. This information will assist the management to optimize their operations by closing the feedback loop.

SAP PM module components support planning, scheduling and execution at multiple levels and integrate with other functional modules (e.g., Materials Management, Financial Accounting & Controlling, Project System, Quality Management & Human Capital Management) based on the planning objectives.

# 4. Organisational Structure

Page 4 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# General Organisational Units

- Client
- Controlling Area
- Company Code
- Plant

# Location Based Organisational Units

- Maintenance Plant
- Location
- Maintenance Work Centers Org; Unit
- Business Partner
- Personnel Number
- SAP User

# Planning Based Organisational Units

- Planning Plant
- Maintenance Planner Groups

# The organisational levels are structured as follows:

# Controlling Area

From the Controlling perspective, one or more Company Codes are assigned to a Controlling Area to have a Common Controlling / Management Accounting over several subsidiaries.

# Configuration parameters as per Club Coffee requirement:

|Controlling Area|Name|
|---|---|
|OL10|Olam Controlling Area|

# Company Code

The subsidiaries with their own financial statements and balance sheets are defined as Company Codes.

# Configuration parameters as per Club Coffee requirement:

|Company Code|Name|
|---|---|
|CAF|Club Coffeee|

# Plant / Maintenance Plant

The Plant at which technical objects (equipment / functional location) of a Company are installed is called Plant / Maintenance Plant.

# Configuration parameters as per Club Coffee requirement:

Page 5 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Plant / Maintenance Plant Name (C30)

|1990|55 Carrier Dr & 65 Carrier Dr|
|---|---|
|1991|101 Claireville|
|1992|160 Claireville|

# Planning Plant

It represents the organizational unit where maintenance requirements for the operations production system are planned.

Maintenance planning plant is a plant in which maintenance tasks are planned and prepared.

In the planning plant, maintenance task lists are defined for the respective maintenance plants, spare parts planning is carried out on the basis of bill of material of the equipment, maintenance plans are managed and scheduled, maintenance notifications are created and maintenance orders are handled.

When the maintenance works are planned in the maintenance plant, then the maintenance plant is also called as maintenance planning plant (planning plant in short).

# Configuration parameters as per Club Coffee requirement:

|Planning Plant Name 1 (C30)|Name 2 (C30)|
|---|---|
|1990|Club Coffee Maintenance Planning plant|
|1991|Club Coffee Maintenance Planning plant|
|1992|Club Coffee Maintenance Planning plant|

# Assign Maintenance Planning Plant to Maintenance Plant

The maintenance plant is the plant where the technical objects are installed. The maintenance planning plant is the plant in which the maintenance tasks for the technical objects are planned and prepared. As there is no centralised planning involved the maintenance plants assumes the planning of maintenance activities of their respective plants. Both maintenance plant and planning plant will be same for one plant, planning and execution is performed in one plant for one company.

# Configuration parameters as per Club Coffee requirement:

|Maintenance Plant Name (C30)|Planning Plant Name 1 (C30)| | |
|---|---|---|---|
|1990|Club Coffee|1990|Club Coffee|
|1991|Club Coffee|1991|Club Coffee|
|1992|Club Coffee|1992|Club Coffee|

Page 6 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# 5. Master Data

PM Master data is central data in SAP System and used for processing specific business transactions. PM Master Data are the enablers for business functions such as maintenance planning, scheduling, purchasing, and performing technical analysis of any or all maintenance activities.

Following SAP PM Master Data shall be maintained in the system.

- Functional Location
- Equipment
- Maintenance Work Center
- Class & Characteristic
- Catalog Profile, Catalogs, Code Groups & Codes
- Bill of Material (Functional Location, Equipment & Material)
- Measuring Point & Counter
- Maintenance Strategy
- Task List (Functional Location, Equipment & General)
- Maintenance Plan – Time Based
- Maintenance Plan – Performance based

# Functional Location

Functional Locations are hierarchically ordered structures that represent a technical system, building, or part thereof.

Functional Locations can be structured according to spatial (for example, General Plant Area, Product Loading Area, Yard Area, etc.), technical (for example, Control Panel Unit, Air Compressor Unit, Steam Generator, etc.), or functional, that is, process oriented (for example, Chlorine Processing, Caustic Production, Utility, Tank Farm, etc.).

The aim of creating a functional location is to structure a technical system or building into units that are relevant for Plant Maintenance.

Page 7 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# For what purpose is a functional location created?

- Execution of maintenance tasks
- Recording of maintenance tasks
- Data collection over long periods of time
- Cost monitoring by area

# What affect do the usage conditions have on the likelihood of damage to the installed aggregates?

# Structure Indicator

The identification for functional locations is created using the Structure Indicator. The structure indicator consists of two input fields:

- Edit mask
- Hierarchy levels

The Edit Mask is used to control which characters may be used for identification (letters, numbers, or both) and how these characters are grouped together or split. The hierarchy levels are used to define which level ends at which character and how many hierarchy levels the structure may contain.

A Functional Location can be identified using a maximum of 30 characters (= maximum length of the edit mask).

|Edit mask|AN-ANN-N-X-X|
|---|---|
|A|Alpha|
|Numeric| |
|Hierarchy levels|1 2 3 4 5 6|
|X|Alphanumeric|

# Location number

- A1
- A1-B
- A1-B02
- A1-B02-9
- A1-B02-9-C
- A1-B02-9-C.

# Naming / Numbering Conventions

Page 8 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

A unique structure indicator shall be created based on the business requirements, to be used for structuring all technical objects (functional locations) in the company.

A typical Structure Indicator / Edit Mask for Club Coffee Plants shall look as follows:

|StrInd|StructIndText|Edit Mask|
|---|---|---|
|1990|Club Coffee|XXXX-XXXX-XXXX-XXX-XXX-XXX|
|1991|Club Coffee|XXXX-XXXX-XXXX-XXX-XXX-XXX|
|1992|Club Coffee|XXXX-XXXX-XXXX-XXX-XXX-XXX|

# Description of Improvements

This will standardize the technical structuring of maintenance objects across the Company. Vertical flow of data between the logical hierarchical levels will enable cost analysis, spares planning, job planning, maintaining technical history at different levels.

The master record for the Functional Location uses the following views:

- General - Class, Object Type, Reference Data and Manufacturer Data
- Location - Location Data & Address
- Organization - Account assignment (for example, Company Code, Cost Center), Responsibilities (for example, maintenance Planning Plant, Planner Group, etc.)
- Structure - For example, Structure Indicator, superior Functional Location & Equipment

Additional data or links in the master record for the functional location can also be activated as tab pages.

# Equipment

An equipment is an individual physical object that is to be maintained as an autonomous unit. Pieces of equipment usually represent single objects (for example, Cranes, Cutting Machines, Welding Sets, Pumps, Motors, Vehicles, Welding Sets, Compressors, etc.), for which maintenance tasks should be recorded. Equipment can be installed at Functional Locations.

Individual physical object to be maintained as an autonomous unit:

- Means of production
- Means of transport
- Test equipment
- Production resources/tools
- Customer devices
- Buildings property
- Systems, system parts
- Vehicles
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

An equipment master record is created for a technical object in order to,

- manage individual data for the object
- Record breakdown, preventive & planned maintenance tasks for an object
- Collect & evaluate technical data for an object over long periods of time
- Monitor the costs of maintenance tasks for an object
- Record the usage time of an object at Functional Locations

# For what purpose is a piece of equipment created?

- Management of individual data
- Recording of maintenance tasks
- Object-based recording of costs
- Evaluation of technical data
- Recording of usage times

The Equipment master record uses the following views in the standard system:

- General - Category, Object Type, Class, Reference data & Manufacturer data
- Location - Location data & Address
- Organization - Account Assignment (for example, Company Code, Cost Center), Responsibilities (for example, Maintenance Planning Plant, Planner Group, etc.,)
- Structure - For example, Structure Indicator, Functional Location / Superior Equipment, Technical Identification no. etc.,

Additional data or links in the master record for the equipment can also be activated as tab pages.

Equipment can be installed and dismantled at functional locations. It is also possible to monitor the installation times for a piece of equipment from both the Functional Location view and the Equipment view.

# Naming / numbering convention

All equipment numbers shall be maintained with internal number range. That is, whenever an Equipment master data is created, system would automatically assign the next available number from the number range defined.

# Maintenance Work Center

In SAP PM module, Maintenance Work Centres (Work Center in short) are used as,

- Main work center in the master record for the equipment or functional location
- Main work center in a maintenance item

Page 10 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Main work center in the task list header

# Performing work center in the operations for a task list

# Main work center in the order header

# Performing work center in the operations for an order

Work Centers belong to the master data in SAP PM module and provide the capacity required to perform a task.

# Maintenance Work Centers

For example,

- Welders
- Metalworking
- Mechanics

The basic data contains general data such as work Center category, description, responsibility, and usage.

Work Center links provide the connection between work centers and other objects within the SAP System. A work Center can be linked to the following objects:

- Cost Center
- Qualifications (linked to HR Module)
- Staffing positions (linked to HR Module)
- People (linked to HR Module)

The links are valid for certain periods of time.

# Costing

To determine the costs of an internal activity by a product unit. The aim of costing is to attribute the costs incurred to the individual cost objects. It uses the work Center to link the operation to cost accounting by maintaining cost centers and activity types. If the work Center is used in an operation, standard values can be entered for the activity types specified in the work Center.

# Scheduling

To determine the dates when the maintenance operations should be performed. For this, the time required for the operations must be calculated and compared with the time available in the work Center. The standard values and quantities in the operations are used as the basis for this calculation. During scheduling, the start and end dates for the operations are calculated from this data using formulas, which have been entered for scheduling in the work centers.

# Class & Characteristic

The classification system allows using characteristics, to describe all types of objects and to group similar objects in classes to classify objects.

Page 11 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Classes will then be used to help user to find objects more easily, using the characteristics defined in them as search criteria. This ensures that user can find objects with similar or identical characteristics as quickly as possible. The classification system allows classifying all types of object.

There are three steps to setting up a classification system:

1. Defining the Properties of Objects
Use characteristics to describe the properties of objects. Create characteristics centrally in the SAP ECC 6.0 System (e.g. Lifting capacity of a crane, power of a motor, capacity of a pump, delivery head of a pump, etc.)
2. Creating a Class
Create classes to classify objects. These classes must be set up. During set up, assign characteristics to the classes (e.g. crane, motor, pump, etc.)
3. Assigning Objects
Once the classes are created, it is required for classification, to assign objects to these classes. Characteristics of the class will be used to describe the objects that are classified. This completes the data required to use the classification system. User can then use the classification system to find objects that match the criteria required.

Once the classification system is set up, user can use it to find certain objects. To do this:

1. Find a class in which objects are classified
2. Find the object(s) the User requires in the class

When the classification is used to find objects, the characteristics as search criteria will be used and the system compares the values that are entered with the values of the classified objects.

# Catalog Profile, Catalogs, Code Groups & Codes

Catalog System is a cross-application component, used for reporting maintenance notifications.

This catalog system has a hierarchical structure. The first level of the catalog system is the Catalog Type. Each PM Catalog Type represents a certain directory.

Each Catalog Type can be further subdivided using Code Groups. For each Code Group, individual codes can be defined.

The following Catalog Types are provided as standard for Plant Maintenance:

|2|for Tasks|
|---|---|
|5|for Causes|
|A|for Activities|
|B|for Object Parts|
|C|for Damages|

Page 12 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Catalogs

|Catalog Types|Code Groups|Codes|
|---|---|---|
|Tasks|Electrical tasks|Replace cable|
|Damage causes|Mechanical tasks|Replace fuse|
|Activities| |Replace starter|
|Object parts| | |
|Damage| | |

Catalogs are assigned to each Notification Type for the predefined areas Problems, Causes, Tasks, Activities and Object parts. It is only after catalogs have been assigned to the notification type that the corresponding fields for damage cause, object part and so on, are provided in the notification item.

The Catalog Profile enables to configure particular code groups to choose from the individual PM catalogs. When maintenance tasks are performed, only the Code Groups of the PM Catalog Types that are permitted for the relevant Catalog Profile are displayed in the notification processing screen.

# Catalogs and Catalog Profile

|Catalog C: Damage|Catalog Profile|
|---|---|
|Group 1000: General damage|PM catalog type|
|Commission|Code Group|
|Damage|011000|
|Task|0025400|
|Object part|ALLG|
|Group 5400: Pumps| |

# Bill of Material (Functional Location, Equipment & Material)

The maintenance bill of material (BOM in short) differs from other BOMs; in that it only contains items relevant for Plant Maintenance.

The maintenance bill of material has three important functions:

1. Structuring of the object - The structure of an object should be displayed as clearly as possible from a maintenance viewpoint.
2. Spare parts planning in the maintenance order - If a bill of material exists for a technical object (Functional Location / Equipment), it can be used during the planning process of a maintenance order for the purpose of spare parts identification and planning.
3. Spare parts planning in the task list - Spare parts can be planned in the task list based on a bill of material.

There are three categories of maintenance bill of material:
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Functional Location BOM

There is no need to maintain elaborate maintenance history and do maintenance planning for them, but information may be required, if some maintenance jobs are planned on the functional location. These materials may be represented as Functional Location BOM.

# Naming / Numbering Conventions

Functional Location BOM’s do not have specific names / numbers but are identified by the Functional Location code to which they are attached.

# Equipment BOM

Bill of Material shall be defined for equipments to enable,

- Structuring of the equipment: Identification of material / spares including quantity requirement specific to the equipment to plan material requirement for maintenance plans (preventive and corrective)

Equipment BOM will be specific for an equipment. They can be used for spares planning as well as job planning. For spares planning, the material / spares, assemblies which form part of BOM can be stock as well as non-stock items. Material ‘Where-Used-List’ can be used to identify a common material component within a BOM, which is assigned to number of equipments.

# Naming / Numbering Conventions

For equipments, which are unique in construction, Bill of Material will be directly created for them. These will be identified in the system, by equipment number, usage (Plant maintenance BOM) combination.

# Material BOM

Material BOMs are always used in Plant Maintenance if several similarly constructed objects have to be maintained. The aim is not to create a bill of material for each technical object (i.e. Functional Location / Equipment), but to create just one bill of material and then assign this to similar technical objects, which share the same materials. This avoids the use of redundant bills of material.

A material BOM is a bill of material that is first created for a material independently of a technical object. To do this, it is required to,

- First create a material master
- Then create a material BOM for the material

Page 14 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

The material BOM can then be assigned to one or more technical objects (Equipment / Functional Location). The assignment(s) can be made in the respective technical object master record using the Structure view. The number of the corresponding material is entered in the ‘Construction Type’ field of Equipment master.

# Measuring Point & Counter

Measuring points are physical and/or logical locations at which a particular condition is described; for example, the coolant temperature or rotations per minute (rpm) of an engine. Measuring points are located at technical objects (Functional Location / Equipment).

Measuring point counters are resources that enable to represent the wear and tear of an object or the consumption or reduction in its useful life, for example, the mileage indicator of a truck or the electricity consumption meter of an electrically powered system. Counters are also located at technical objects (Functional Location / Equipment).

Measurement or counter readings can be entered for each object if it is required to document the condition of an object based on measurement readings or if the regular maintenance of an object depends on its meter readings.

Each measuring point or counter refers to a characteristic (for example, pressure, temperature, kilometer, litre, operating hours, and so on).

The characteristic of a measuring point or counter determines the characteristic unit in which measurement and counter readings are entered:

- The characteristic ‘Ratio’ for example, can have the characteristic unit ‘Percent’.
- The characteristic ‘Temperature’ for example, can have the characteristic unit ‘Degrees Celsius’ or ‘Degrees Fahrenheit’.

Before maintaining the measuring points for a Functional Location or Equipment, all the relevant characteristics should have been created in the classification system.

|Temperature|Flow (liters)|Class|
|---|---|---|
|Kilometers|Operating hours| |
|Measuring point/Counter|Characteristics of the class system| |

Following customizing inputs have been defined for creation of Measuring Points & Counters:

Page 15 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Measuring Point Category: M - Measuring Point (General)

# Measuring Point Object: IEQ - Equipment & IFL - Functional Location

# Numbering Convention:

The number range defined for measuring points & counters will be internal.

# Maintenance Strategy

A Maintenance Strategy consists of several maintenance packages and represents the scheduling rule for preventive maintenance. Task lists can be assigned to maintenance strategies.

# The Maintenance Strategy uses the following parameters:

- Scheduling indicator (time: calendar-based, time: using key date, time: using factory calendar)
- Call horizon
- Shift factors and tolerances
- Factory calendar
- Package sequence and ‘where used’ list

A Maintenance Strategy can consist of Maintenance Package(s). Maintenance packages are part of a Maintenance Strategy.

# Maintenance Package(s)

Maintenance packages define the frequency at which specific operations are executed. They are assigned to the operations in a task list.

# Important parameters for a maintenance package are:

- Maintenance package number
- Description
- Cycle length
- Unit of measurement
- Hierarchy

If two maintenance packages are due at the same time, the hierarchy defines which maintenance package is performed.

# Offset:

The offset determines the first due date of a maintenance package.

# Preliminary / Follow-up buffer:

The preliminary or follow-up buffer is specified in days with reference to the planned date and sets the basic start and end dates for a maintenance order.

# Scheduling indicator

# Package definition

|Time using key date|Strategy| | |
|---|---|---|---|
| |months|months|months|

Page 16 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Maintenance packages can be assigned to a maintenance strategy. Note that the maintenance packages for a strategy should not have different cycle units (for example, month & year). A strategy consisting of one month and one year should be defined as one month and twelve months.

|Package number|Description|Cycle length|Unit of measurement|Preliminary / Offset|Hierarchy|
|---|---|---|---|---|---|
|3 months| | | | | |

The hierarchy of maintenance packages defines whether all maintenance packages that coincide should be executed, or whether certain maintenance packages should be ignored. For this reason, a hierarchy level is assigned to each maintenance package. If maintenance packages with the same hierarchy level coincide, these maintenance packages are executed. In the case of maintenance packages with different hierarchy levels, the maintenance package with the lower level is not executed.

Example: For the maintenance of a vehicle, the spark plugs should be cleaned every three months and changed every six months. In order that cleaning and exchanging are not both performed after six months ("first clean, then throw away"), the 6-month package (exchange spark plugs) is assigned a higher hierarchy than the 3-month package (clean spark plugs), whereby the latter is deactivated.

# Same hierarchy levels

H1 months) Strategy months _ months months

# Different hierarchy levels

H1 months) months) Strategy months months months

H2

Maintenance Strategies shall be created manually, based on the business requirement.

# Task List (Functional Location, Equipment & General)

In Plant Maintenance, there are 03 types of task lists. They are distinguished by an indicator:

Page 17 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# E - Equipment Task List

# T - Functional Location Task List

# A - General Task List

Equipment task lists are always object based and created for a specific, individual piece of equipment (example: steps for calibrating measuring device M-105).

Task lists for functional locations are also object-related and created for a specific functional location (example: steps for inspecting hydraulic press HP-200).

General task lists are without object reference (example: general steps for pump maintenance).

All three task list types can be used for routine and preventive maintenance.

The maintenance task lists in the Plant Maintenance are combined into task list groups. A task list group contains all the maintenance task lists with the same or similar maintenance steps. The maintenance task lists within a task list group are identified by the group counter, which numbers the task lists within the group sequentially.

Depending on the task list type, task list groups are either object-based (equipment task lists, task lists for functional locations) or object-independent (general maintenance task lists).

# Example 1:

Task list group 1 for measuring device M-105

- Task list no. 1 - Steps for inspecting measuring devices
- Task list no. 2 - Steps for calibration

# Example 2:

Task list group PUMP_WTG for pump maintenance

- Task list no. 1 - Steps for pump inspection
- Task list no. 2 - Steps for exchange of gears
- Task list no. 3 - Steps for maintaining pump motor

In the Plant Maintenance, all maintenance task lists within a group are handled as one unit. Therefore, it is advisable to divide your maintenance task lists into several small groups to facilitate processing. The data volume that the system has to process when accessing a task list group will thereby be reduced and system response times will be shorter.

Page 18 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Task list groups

# Task list header

# Pump_Wtg

# Pumps

TLGC: Group counter = 3

Operation list Group counter = 0.2

0010 Switch off

Group counter =

# Number assignment for Equipment Task Lists & Functional Location task Lists

The numbers for equipment task lists and task lists for functional locations are assigned internally. This means that the system assigns the number when a task list is created. The first task list that is created for a particular piece of equipment or functional location is identified by a task list group number and group counter. Further task lists for the same piece of equipment are identified by the task list group counter within the group.

# Number assignment for General Task Lists

System generated internal number will be assigned for each General Task List.

|K1-MO1|Task list group Counter| |
|---|---|---|
|Functional location|742|01|
| | |02|
| | |03|

# Internal number assignment

|Internal number assignment|Pump_Wtg|Task list group Counter|
|---|---|---|
| |Pump_Wtg|01|
|200125|Task list group Counter| |
|Equipment|395|01|
| | |02|
| | |03|
| | |04|

# Internal and external Number assignment

The following assignments are made in the task list header:

- Plant
- Maintenance Work Center
- Planner Group
- Maintenance Strategy
- Inspection Point
- Status
- Condition of Technical System

Page 19 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Planning plant

|Task list header|Usage|
|---|---|
|Pump Wtg|Maintenancestrategy|
|TLGC:|Status|
|Operation list|Work center|
|Components|Service packages|
| |Maintenance packages|

# Maintenance Plan

A maintenance plan is used to generate a call object automatically for a particular date. A call object can be a maintenance order or maintenance notification or service entry sheet. The order and notification can also be generated at the same time.

|Orders|Service Notifications|Maintenance plan|
|---|---|---|
|Ordec 9017.60|Notificat|Single cycle plan|
| | |Strategy plan|
| | |Multiple counter plan|

# Scheduling data

Maintenance item Call date

|Time-based|Performance-based|
|---|---|
|Cycle start|Cycle|

The maintenance item contains the following data areas:

- Planning Data: Planning Plant, Planner Group, Order Type, Maintenance Activity Type, Maintenance Work Center, Business Area, etc.
- Reference object (i.e. Functional Location or Equipment)
- Task List

The maintenance interval (cycle) is assigned at the level of the maintenance plan: Interval: Cycle, Offset, Cycle Text.

A maintenance plan can consist of several maintenance items. In this case, an order (or notification or service entry sheet) is created for each maintenance item.

Example: In a maintenance plan, different components of a water pump should be maintained. For example, a maintenance item for the pump itself, another item for the electric motor, and a third for the pump gears. Each maintenance item has its own task list. All the items are part of the same maintenance plan and thereby have the same times (that is, the same scheduling data).

Page 20 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Interval (cycle)

|Maintenance plan|months|
|---|---|
|Scheduling data| |
|Maintenance item| |
|Maintenance item| |
|Reference object| |
|Task list| |
|Responsibilities| |
|Planning data| |

Description of Improvements: The system can schedule the planned maintenance job and generate maintenance notifications / orders. Also, tracking of backlog jobs will be easy within SAP. Various logics can be defined for scheduling the job, (e.g. time period, performance, or combination of both).

Time Based Maintenance Plan (Single Cycle / Strategy): Many technical objects require a maintenance job based on exactly one time based or performance-based maintenance cycle, in which the interval at which the maintenance plan should be executed is specified. Under such circumstances Time based plan (Single Cycle / Strategy) can be deployed.

Performance Based Maintenance Plan (Single Cycle / Strategy): Some of the equipment’s are maintained based on a maintenance strategy (i.e. rules for the sequence of planned maintenance work). Some jobs are done on the equipment after certain time intervals, while other jobs are done at some other time intervals (e.g. it may so happen that different maintenance tasks for a diesel generator are due in different cycles: oil checks every 500 run-hours, various filter changes & oil change every 5000 run-hours). Under such circumstances a Performance based Plan (Single Cycle / Strategy) can be deployed.

Naming / Numbering Conventions: System generated internal number will be assigned for each maintenance plan. No separate logic needs to be maintained for identifying maintenance plans.

# 6. Business Processes

BPML Of Plant Maintenance:

Page 21 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Process Id|Business Process(LO)|Subprocess Id|Subprocess (LI)|Subprocess (L2)|
|---|---|---|---|---|
|PTM_4.0|Plant Maintenance|PTM_4.0.1|Master Data Management|Equipment master|
|PTM_4.0|Plant Maintenance|PTM_4.0.2|Master Data Management|Functional location masters|
|PTM_4.0|Plant Maintenance|PTM_4.0.3|Master Data Management|Task list|
|PTM_4.0|Plant Maintenance|PTM_4.0.4|Master Data Management|Maintenance plan|
|PTM_4.0|Plant Maintenance|PTM_4.0.5|Master Data Management|Work centre master|
|PTM_4.0|Plant Maintenance|PTM_4.0.6|Master Data Management|Measuring Point|
|PTM_5.0|Plant Maintenance|PTM_5.0.1|Maintance planning|Preventive Maintenance|
|PTM_6.0|Plant Maintenance|PTM_6.0.1|Maintance planning|Shutdown Maintenance|
|PTM_7.0|Plant Maintenance|PTM_7.0.1|Maintance planning|Calibration Maintenance|
|PTM_8.0|Plant Maintenance|PTM_8.0.1|Maintance planning|Predictive Maintenance|
|PTM_9.0|Plant Maintenance|PTM_9.0.1|Unplanned Maintenanace|Breakdown Maintenance|
|PTM_10|Plant Maintenance|PTM_I0.0.1|Unplanned Maintenanace|Corrective Maintenance|
|PTM_IE.O|Plant Maintenance|PTM_I.O.1|Capex Process|Equipent installation process|
|PTM_12.0|Plant Maintenance|PTM_12.0.1|Spare parts Magement|Issue of Spares|
|PTM_13.0|Plant Maintenance|PTM_13.0.1|SparepartsMagement|Purchase of spares|
|PTM_14.0|Plant Maintenance|PTM_14.0.1|Asset Management|Refurbishment Process|
|PTM-15.0|Plant Maintenance|PTM_15.0.|Asset Management|Asset Disposal|

# Club Coffee Maintenance-Division

There are 2 Parts of Plant maintenance adopted in Club Coffee viz.

1. Maintenance
2. Operational

# Maintenance

Maintenance Team take care of Equipment maintenance inside the Plant to maintain smooth flow of production.

Planner Generates work order on daily basis and allocates to Mechanical and Electrical Team lead, which further Task execution carried out by Maintenance technical allotted by Team leads.

Any uncompleted task can be shifted to weekend for completion.

Electrical task like substation work carried out as per frequency defined in the task list.

# Operation

Operation Team take care of equipment cleaning activities through which they maintain clean environment in the production line.

Operation team take care of Equipment cleaning through 7i software in which task is issued to shift Manager and team Leaders and then assigned to Operators of the machine to ensure completion of task operations.

Operation team after completion of task gives back to planner and Planner completes the job in the system.

Page 22 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Sanitation Group carries out of PM task as per their PM schedule due for the day through Sanitation management software.

# Maintenance Notification

Maintenance Notifications is a mode of communication between Operations & maintenance department and internally between different maintenance departments. System malfunction and maintenance requests are created as Notifications.

Maintenance dept. can also generate notifications for recording the activities performed by the dept. / requesting maintenance from other dept. and also records different parameters like break down indicator, down time Etc.

# Considerations w.r.t Club Coffee

|Process|Notification type|Number Range|
|---|---|---|
|Maintenance Request (No prod.loss)|N1|Internal number range|
|Break down Notification (with loss)|N2|--do--|
|Activity report (preventive maint)|N3|--do--|
|Predictive maint.Notification|N4|-do-|

# Notification process

Notification creation in SAP – The concerned maintenance personnel has to create the notification in the system based on the log details/oral information given by the reporting person. Notification will capture the equipment number (with all master data information automatically coming into it), timing of breakdown, reporting person’s name etc.

Breakdown Analysis – The concerned maintenance personnel will analyse the nature of breakdown whether any material or manpower is required for its correction or not. If no cost is involved, the correction will be done and notification will be closed with time confirmation and comments. If the notification involves cost, it will be converted to maintenance order.

# The steps for maintenance order cycle is given below:

1. Creation – Maintenance Order will be created with reference to the notification. This keeps a track on which notification has cost implications to it.
2. Planning – Plan for material and manpower required for correction of the breakdown. List of operation involved to clear the breakdown can be noted in the order itself. Material availability check can be performed if the equipment BoM is present.
3. Release – Release the order in the system for its further processing.
4. Printout – Print out of the order can be taken, if required.
5. Execution – Execute the maintenance activity based on planned activities captured earlier.
6. Confirmation – Confirmation of the end of maintenance job with timing and comments.
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Technical Completion

The order is technically completed in the system once all the activities have been done for it.

# Settlement

After technical completion, the cost of maintenance order could either be settled to cost center (if it is to be expensed out) or can be capitalized.

# Business Completion

In case a work order is available against a notification, then an additional activity has to be carried out termed ‘Business Completion’. This signals completion of all transactions pertaining to that work orders have been completed.

In Club Coffee, Maintenance Orders would be used for all the reasons, which discussed above. The following Order types are identified for Club Coffee:

|Order Type|Description|Notification Type|Description|
|---|---|---|---|
|ZM01|Preventive Maintenance|N1|GT-Maintenance Request|
|ZM02|Breakdown Maintenance|N2|GT-Malfunction Report|
|ZM03|Shutdown Maintenance|N3|Activity Report|
|ZM05|Calibration Maintenance|N4|Predictive Maintenance|

# 6.1 Preventive Maintenance – Time Based (BPML ID: 5.01)

# Business Process Description:

# Process Characteristics

Process Trigger: Pre-defined Preventive Maintenance Schedule

Process Input: Equipment / Functional Location, Maintenance Strategy, Task List, Maintenance Plan & Background Scheduling

Process Output: Preventive Maintenance Order

Process Owner: Maintenance Department

Process Volumes: Approx. 50 Per Day

Process Frequencies: For example, Weekly / Fortnightly / Monthly / Quarterly / Half Yearly / Yearly

# Business process flow:

As is:

Planning: Maintenance planner create or finalised annual schedule for either daily, weekly and yearly for all the activities to be carried out for the production plant which includes preventive and general Inspection plan.

Page 24 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Based on the production planning, downtimes for various equipment, planner prepares the weekly maintenance activity and circulates to various departments for execution.

# Execution:

Execution will be carried out by various departments under maintenance-by-Maintenance technician. Most of the maintenance activity is carried out by mech and electrical dept.

Every week beginning Maintenance person chooses to carry out the task for pm, with respect to the production schedule of the day.

Once pm task is completed, Next step is go to 7i online and close the work order with comments with recorded hours spent. One more technician will validate the work order executed and confirm the same.

Consumption of spares is not being tracked online in 7i.

If spares and consumables are required for the maintenance activities, it will be issued from stores by maintenance dept itself for the work order. If stock is not available in store, then it will be procured from outside and issued to the maintenance team.

Spare parts list not maintained fully and consumption is not maintained or tracked inside the system.

# As is Process flow diagram:

|1|Start|PM-Task list|PM Schedule|
|---|---|---|---|
|1|Work|Manual Assignment|Copy Spare Taken|
|1|Mechanical|Electrical Tech|Reference|
|7|PM task Execution|PM task Assignment of|Name|
|7|Work order close|Spares consumed|(ne Equipment)|
|8|Adherence| | |

Page 25 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# To Be:

- Annual plan for Preventive maintenance is drawn up for machines and equipment’s.
- Maintenance strategy and packages (Monthly, half yearly, yearly) are created to capture the frequency of preventive maintenance.
- Task lists are created to capture the preventive maintenance activity/operation.
- Enter operations, time and manpower required for the operation and components with item category.
- Maintenance Plans are created for equipment with reference to task lists.
- For time-based maintenance, through strategy parameters, scheduling parameters and deadline monitoring, auto generation of maintenance orders will be carried out.

# Schedule Maintenance Plan

We can schedule a maintenance plan with which the system generates maintenance call objects for the defined cycles.

Maintenance order type ZM02 is created from the system as per plan.

For each scheduling the system calculates the due dates for a maintenance call object on the scheduling parameters and the maintenance cycles.

Maintenance planner will schedule the maintenance plan such as orders will get generated some days before actual planned dates.

This reminder interval can be set using Deadline Monitoring.

# Change Order and Release:

After scheduling the maintenance plan the maintenance call object is created automatically.

Then we can proceed with the same cycle after releasing your maintenance order.

# Time confirmation:

Enter time completion confirmations for operations.

# Technical confirmation:

Complete the order technically once the maintenance work has been completed.

# Order settlement:

The cost collected in the PM order should be settled at Maintenance Cost center.

# Business Complete:

Business completion of an order is performed when no further costs are expected to be posted to the order.

Preventive maintenance completion of task can be opened up in mobile application (Field tekpro), confirmation can be given for each task with final TECO to complete the order.

# FieldTekPro - Intelligent Mobile Asset Maintenance:

FieldTekPro for Plant & Asset Maintenance is an SAP Certified Mobile Application available in Android, iOS & Windows mobile platforms to perform all plant & asset maintenance related operations like Real-Time Notification/Work Order Processing, Permit-To-Work [PTW] & Isolation, Job Risk Assessment, Time Confirmation, Equipment Inspection, Measurement Readings, Calibration, Material Reservations, Bill of Material & Stock & MIS Analytics.

The mobile application works both in online & offline mode with many advanced functions.

Page 26 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Additional capabilities include Offline Features, Document Integration, Extended security, Near Field Communication (NFC) & Push Notification, Geo-Tagging, Built-in Bar code/QR Code/RFID readers, IoT plug-in and ready to use PM analytics dashboard. Annual plan for Preventive maintenance is drawn up for machines and equipment’s.

# Real-Time Notification / Work Order Management

Technicians & Supervisors can create & process Maintenance Notification/Work Orders based on asset condition or asset history with capability to scan & attach images. View pending list of Maintenance Notification/Work Orders. Assign Work Orders to Mobile Users. Access complete information of Notifications/Work Orders with Items, Documents, Operations, Reservations & Asset History.

# Some of the Tiles of FieldTekpro shown below:

Dashboard
Notifications
Orders
Equipment
Calibration
Inspection
Unplanned Goods
Utilities
MIS
Maintenance Plan
AlertLog
User Log

# Preventive Maintenance

Preventive maintenance refers to all the tasks for determining the actual condition (inspection) and maintaining the target condition (maintenance) of assets. Every technical asset has a certain service life. If the service life is exhausted, then maintenance measures must be taken to renew it. As a rule, these measures are carried out periodically. The maintenance tasks are planned and performed depending on the time-dependent intervals determined.

Page 27 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

There are many benefits in using planned maintenance within OLAM. It is the generic term inclusive of inspections, preventive maintenance, and planned repairs, for which the time and scope of the work can be planned in advance.

In addition to internal company aspects for planned maintenance, external factors should also be considered. An increasing number of conditions set by legislative bodies demand more stringent requirements on planned monitoring and maintenance of objects.

# External requirements can be as follows:

- Manufacturer recommendations: The manufacturer of your technical objects may recommend certain procedures to ensure that the objects always function optimally.
- Legal requirements: There may be labour protection laws or laws concerning the safety of objects which require you to maintain your technical system on a regular basis.
- Environmental requirements: Effective planned maintenance can also help to prevent breakdowns which could lead to environmental hazards.

Another reason for planned maintenance is the need for quality assurance, since, for example, the quality of products manufactured at a technical system is substantially affected by the operating condition of the production plant.

It is also often more cost-effective to maintain objects regularly, and therefore prevent a much more expensive breakdown. You can determine the data required for this using past data supplied by the system.

# Business Process Steps in Detail

# Create Maintenance Item (Transaction Code: IP04)

A maintenance item describes which preventive maintenance tasks should take place regularly at a technical object or a group of technical objects.

A maintenance item can be assigned to reference objects (for example, equipment or functional locations) to align a maintenance item where you want to perform the maintenance task.

We can assign one or more maintenance items to a maintenance plan. A maintenance plan always automatically contains at least one maintenance item.

We can assign maintenance items to a maintenance plan in the following ways:

- Create a maintenance plan and create a maintenance item directly in the maintenance plan by entering the required data on the Item tab.
- Create additional maintenance items in a maintenance plan.
- Create a maintenance item without assignment and subsequently assign it to a maintenance plan.

A maintenance item can only be assigned to one maintenance plan. We must have created the maintenance item we want to assign to a single cycle plan without reference to a.

Page 28 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Maintenance strategy. The maintenance item assigned to a strategy plan must have the same maintenance strategy as the Maintenance plan. The maintenance item assigned to a strategy plan must have the same maintenance plan category as the Maintenance plan. We can assign an equipment / functional location to a maintenance item at which we want to perform the maintenance task. The easiest way is to create maintenance items directly in the maintenance plan.

# Selection of PM task List in the Maintenance Item

Maintenance task lists are used to process planned and unplanned maintenance tasks. Maintenance task lists are key reference data in the planning, execution steps and gathering actual information for a maintenance order, as would a routing/recipe for production and process orders. Maintenance task lists describe the individual steps which must be executed for inspections, repairs, and preventive maintenance. In addition, they list the spare parts and tools required for the job and specify the necessary completion time.

# Preventive Maintenance Task List

There are three types:

- Equipment Task List
- Functional Location Task List
- General Task List

A Maintenance Item can use any task list as required for maintenance plan. We include this information, if necessary, in a maintenance item by assigning a task list to it. If we work with strategy plans, enter a maintenance strategy in the task list. This means that we can assign the maintenance packages of the assigned maintenance strategy to individual operations in the task list.

In time based preventive maintenance, Equipment task list, Functional Location task list and General task list will be prepared with details of activities and with the details of resources required to execute the maintenance task.

For time-based maintenance plans with a strategy, the task list and the maintenance item must have the same strategy. The status Released must be set for the task list.

# Create Maintenance Plan (Transaction code: IP41/IP42/IP43)

Maintenance plan will be prepared with the details of the equipment / functional location and scheduling parameters. Based on the scheduling parameters a maintenance order will be generated by the system. Scheduling can be done manually and automatically.

# Single Cycle Plan

Single cycle plan is the simplest form of maintenance plan. In this process, single cycle plan is created with one-time based maintenance cycle (it contains the details of time when maintenance must be performed). It might be used, for example, for the annual maintenance of a DG Set or for the repair of Bucket elevator at every 6 months.

# Strategy Plan

The maintenance plan with use of strategy is useful when different operations of a task list are to be performed at different interval of time. The strategy in task list should be the same as that in the maintenance plan(s). The maintenance strategy defines the rules for

Page 29 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

The sequence of planned maintenance operations. It includes general scheduling information and can be assigned to as many maintenance task lists and maintenance plans as required. Maintenance Packages contain the details of time when maintenance must be performed.

We use the maintenance plan category to determine which maintenance call object the system generates for a maintenance plan when a maintenance call is due (for example, maintenance order, notification, etc.), which in turn generated automatically.

For example, a Maintenance Strategy (Time Based) is shown below:

|Name|01|
|---|---|
|Description|PM by Schedule time|
|Scheduling indicator|Time|
|Pack: seq_| |

|Package No.|Cycl length|Unit|Maintenance cycle text|Cycle ShortText|Hierarchy|Hierarchy ShortText|
|---|---|---|---|---|---|---|
|7 DAY|Weekly|1W|HI| | | |
|30DAY|Monthly|IM|H2| | | |
|91DAY|Quarterly|3M|H3| | | |
|175DAY|Half-Yearly|6M|H4| | | |
|365DAY|Yearly|1Y|H5| | | |
|730DAY|Two yearly|2y|H6| | | |

# Assign scheduling Parameters

We can use the scheduling parameters to adapt the scheduling process to meet our individual requirements. The scheduling parameters are as follows:

- Scheduling Period
- Completion Requirement
- Call Horizon
- Shift Factor
- Cycle Modification Factor
- Scheduling Indicators
- Cycle Start

# Scheduling Parameters in detail

Scheduling Period: Determines the period of time, for which the system generates planned or call dates during scheduling, i.e. time for which maintenance jobs should be scheduled (365 days).

Completion Requirement: By setting the indicator, the system only generates the next maintenance call object once the previous call object has been completed.

Call Horizon: Determines when a maintenance order should be generated for a maintenance call, i.e. how early from the planned date of job, the order should be generated in the system as a % of the cycle time.

Shift Factors: The shift factors for early/delayed confirmation of a maintenance task define what % of the shift should be considered for the next date. i.e. in case if the maintenance.

Page 30 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Task is confirmed early/delayed by 2 days then the next maintenance call will be preponed or postponed based on this input.

# Cycle Modification Factor

By entering a cycle modification factor, we can lengthen or shorten the cycle specified in the maintenance strategy. A cycle modification factor greater than 1 lengthens the cycle, whereas a factor less than 1 shortens the cycle. For example, a maintenance strategy with total cycle duration of 60 days is assigned to the maintenance plan and we want to change that for this plan. Therefore, when we enter the cycle modification factor as 1.5 the result would be 60 x 1.5 = 90 days.

# Scheduling Indicator

There are three scheduling indicators in the Maintenance Planning component. They are used for the following scheduling options:

- Time-based scheduling
- Scheduling based on a key date
- Scheduling by factory calendar

# Cycle Start

Date on which the cycle should start. It is required for calculating planned and call dates. From this date, the system starts to calculate the planned and call dates based on the cycle.

# Schedule Time based Plan (Transaction code: IP10)

We schedule a maintenance plan which the system generates maintenance call objects (for example, maintenance order or notification) for the defined cycles.

You create several maintenance plans. Each maintenance plan contains a maintenance item that describes the object to be maintained. The system generates a separate order with reference to notification for each object on a due date.

For each order in scheduling, the system calculates the due date (planned date) for a maintenance call object based on the scheduling parameters and the maintenance cycles or packages and generates maintenance calls.

When the maintenance call is due, the system generates a maintenance call object for each maintenance item due, which object the system generates is determined by the maintenance plan category.

If notifications and orders are generated through a maintenance plan, the date of the notification or order completion is used for the further scheduling of the maintenance plan.

We can use this function to simplify the generation of maintenance call objects for maintenance plans. Start the deadline monitoring at regular intervals using an internally programmed report (for example, weekly or for a weekly cycle). The system then generates the maintenance call objects according to the cycles defined.

A start date must have been entered in the scheduling parameters for the maintenance plan, or we must have already scheduled the maintenance plan.

When we run the deadline monitoring function, the system converts all the maintenance calls, for which the call horizon has been reached, into maintenance call objects.
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

System also performs a complete rescheduling of the maintenance plan and ensures that maintenance calls are always available for the period which you have defined as the scheduling period.

# Process Preventive Maintenance Order (Transaction code: IW31 / IW32 / IW38)

The order for Preventive Maintenance will be generated automatically as per the frequency defined in the Maintenance Plan. Maintenance Planner checks the order and starts the Time-based preventive maintenance work as per order. If required, we change the status of system condition as 0, which means the equipment / functional location is not in operation.

# Material and Resource Planning (Material Reservation, Issue and Procurement process)

# Material Planning

Material planning is the process through which all the materials and spares are planned as required to carry out a maintenance task. All the materials required for carrying out maintenance work are planned based upon the task list creation. In the task list, the preventive maintenance activities to be performed are divided into operations and for each operation the material required is assigned. The required quantity, the item category i.e. whether stock item or non-stock item will be mentioned in the order.

The results of material planning, material availability is checked for Stock item or Non-Stock Items. If material is available (in Stock), then item Category is Set to be L and a Reservation No. is generated to reserve and issue the material from Stores. If material is not available in Stock, then Item Category N is Set for which a Purchase Requisition No. is Generated after saving the Order which will be used by Procurement Department to generate the necessary Purchase Order.

# Resource (Manpower) Planning

Resource Management is part of the Planning process in a Work Order. When an order is planned, all the resources required for the successful completion of the job is planned. When operations are planned, manpower required for the job in terms of their skills, time required for performing particular operation, total time required to complete the job etc. are all planned and calculated.

Maintenance engineer will assign the resources to the order based on various factors like:

- Internal Resource – if available for a job. In this case the operation control key will remain as PM01, i.e., internal manpower will be used.
- External Resource – if a job is to be carried out by external Service Providers (Vendors). In this case the operation control key is to be changed to PM03, which indicates that the operation is to be performed by external agencies. By doing so, a Service Purchase Requisition can be generated from the maintenance order. The Purchase Requisition can further be processed until Purchase Order.

# Material Availability Check

Materials planned for the executing order operations can be viewed, or displayed for the operation if they are available on time and in sufficient quantity.

Page 32 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

The system can only determine and display the necessary information once an availability check has been performed for the required material. We can either perform this check before the order is released, or the system can do it automatically when the order is released. Additionally, Transaction Code MMBE can be used for Material Availability Check any time up to release of the order.

At any stage during the maintenance order processing, the stock availability of spares reserved for the order can be checked. When the order is released, the system does the availability check and alerts the user if the stock doesn't exist. The alert message can still be ignored, and the work order can be released to execute the work.

# Scheduling

Planning an order with all its operations and components is performed by the scheduling function to determine the following data:

- The actual execution dates based on the dates specified in the order and the time specifications in the operations
- The capacity requirement needed to execute the order, based on the data in the operations
- The date at which a particular material should be available

This date is entered based on the start date for the operation in which the material is required.

# Order Release (Transaction Code: IW32 / IW38)

After planning, the release of the order can be performed. The following activities are the result from the release of an order:

- Printing shop papers
- Withdrawing material
- Posting goods receipts
- Entering time completion confirmations
- Completing a task

When we release an order, it has the status REL. This status is a prerequisite for executing the dependent functions outlined above.

When we release an order, the system checks the availability of materials. At the latest when the order is released, the material reservations are relevant for materials planning and can be withdrawn, and the purchase requisitions generated.

# Settlement Rule

The Settlement Rule defines what proportion of the costs are allocated to where (mostly a Cost Center). Entering the correct settlement rule into the system ensures that the costs incurred in the execution of the maintenance work can be settled correctly. The settlement rule must have been specified when the order is released.

The system determines the settlement rule for an order automatically from the reference object, i.e., functional location / equipment.

Page 33 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

If no object has been entered in the order, or if we do not want the order to be settled in the way proposed by the system, the settlement rule can be manually changed. In Club Coffee, the settlement receiver will be the respective cost Center of the functional location/equipment.

If the settlement receiver is present in the master data of the reference object, at the time of order release system automatically creates settlement rule. If no settlement receiver is present in reference object (i.e., no cost Center assigned) at the time of order release, we have to maintain it manually.

# Goods Issue

When the order is generated by the system based on the schedule, material reservation number is also created against the maintenance order. During the execution of work, materials are withdrawn against this reservation. When the material is withdrawn, the system automatically creates a goods issue document.

Goods Issue is made against the reservation to facilitate:

- Control of issue and check that the correct material is being issued
- Accurate and real time records of all material issues and receipts for maintenance work

Since, the material is issued against the order, it makes data entry quicker, accurate and with relevant reference. The quantity withdrawn is updated in the order as well as in the reservation. This reduces the reserved quantity.

For Unplanned materials, goods are issued against the order to capture the material and cost details in equipment history. After completion of work, excess or unused materials can be returned back to inventory.

The material issue transaction being handled through Transaction Code MIGO by Engineering Stores against material reservation/maintenance order.

# Pre-Closing Activities

# Actual Time Confirmation (Transaction Code: IW41 / IW42 / IW45)

This process will be used to record the actual activity and interval in the maintenance order. It will be used to identify:

- Who processed the operations specified in the order
- The time required for completing the operation, or if not completed, the remaining time required
- If all the materials specified in the order has been used, and if used, whether reservations have been cleared

After completion of work, the actual status is to be updated in the maintenance order to understand the difference between the plan and actual data in terms of manpower and material. Material issued will be automatically updated by the system, manpower detail is updated as in time required to complete the operation through the time confirmation.

The following information is documented:

- Time and date on which the operations were completed

Page 34 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# The activity performed

# Remaining work

# Time utilized of the total time required for an operation

# Recording the Observation

In case, a notification is generated along with the maintenance order, following activities shall be performed in the notification.

1. Open the Notification (Transaction Code: IW22 / IW28)
2. Select the item code for failed part
3. Select the damage code
4. Select the cause code of the damage
5. Select the Task to be carried out to prevent such failure in future (if any)
6. Select the activities performed

The notification may further be completed after completing the outstanding tasks within the notification, if any.

# Technical Completion of Order (Transaction Code: IW32 / IW38)

After completion of maintenance order, the maintenance engineer or authorized person sets the status of the order to technically completed. Technical Completion will be used to ensure that further processing of the work order does not take place and all the unutilized resources which have been planned or reserved for the order are released.

After all the maintenance work is completed the Complete Technically button is clicked. After this the PM Order Status is changed from REL (Released) to TECO (Technically Complete) & Notification Status is set to be NOCO (Notification Completed). While this status is set, no further work can be carried out on the particular Notification / Order.

Once an Order is technically completed, outstanding purchase requisitions or material reservations are deleted or cleared. Notifications for the order is also completed. Only the following changes are allowed on an order:

- Lock and unlock the order
- Set the deletion flag

# Plan v/s Actual Cost in an Order

Cost is the value of consumption of stock / non-stock materials, actual work hours and so on, which are required to execute maintenance tasks. Costs are distinguished according to planned and actual costs.

Planned costs are calculated automatically by the system during order planning while actual costs for goods issues and goods receipts are calculated automatically by the system whilst the order is being executed. The actual costs for the work performed can only be calculated once the work has been confirmed.

We can display the costs resulting from an order from the Plant Maintenance perspectives in the system, this display is called the cost overview. The cost overview lists the individual value categories. A value category is a grouping of cost elements.

# Order Settlement (Transaction Code: KO88)

Page 35 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Order settlement is used to control costs and to identify where maximum costs are being incurred for maintenance. Costs associated with the maintenance work are assigned to Cost centers / internal order. Costs arising out of executing an order are initially collected in the order. These costs are then transferred to a receiver, for e.g., Cost Center. The receiver of costs is specified in the order and settlement carried out at regular intervals by finance / accounting department.

# Business Completion of Order (Transaction Code: IW32 / IW38)

Business completion of an order means ‘final completion of an order’. When an order has been fully executed and all the costs incurred in it are settled, then the status of the order can be changed to Business Completion (CLSD) and no further processing can be done on it. This ensures that no further postings of any kind are carried out on it. Business Completion of orders is performed when after all the work has been completed and all the costs settled.

Business Completion of an order is done after it has been:

- Technically completed
- Costs have been fully settled and the order balance is zero
- There are no open purchase orders for that specific maintenance order

When an order is given the status completed, then the system checks that settlement has been done and the order balance is zero and no outstanding purchase orders exist. No more postings can be done on it against the order. If for any reason the work has not been performed and the order is given the status CLSD then the system generates error message depending upon the error. For example, if the order is not settled (i.e., balance of cost is not zero) then the system gives error message ‘Order balance is not zero’ and the status of the order cannot be changed.

# Business Process Flow Diagram

Page 36 of 110
---
# Project Maple Club Coffee

# Plant Maintenance Business Blueprint Document

|Order Types|Hotification Type|
|---|---|
|Mainenance|For Iil|
|NI-FTE ErILive|ZNJI-Pieventne|
|Buildirio|NZ-Bieakdor|
|2Mo2-Breakdown|N3-Acuvity-Report|
|ZMO3-ShutDown|Na-Precidive|
|ZMM4-Refurbishment|Zi-Calibrtion|

Page 37 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Preventive Maintenance (Time based Strategy)

|Maintenance|Plant Maintenance|Purchase Material|Finance/Costing|
|---|---|---|---|
|Create Maintenance Strategy|Create Task List|Create Maintenance Schedule|Maintenance|
|Maintenance|Print Maintenance Order|Release Purchase Requisition|Fxema|
|Services Required|Create Service PC|Create Service Entry Sheet|Create Purchase Requisition (PR)|
|Stock Available|Yes|Create Reservation|Create Purchase Order from PR|
|Goods Receipt|Invoice Verification?|against PO|Goods Order|
|Confirmation|Technical Order|Payment to Vendor|Order Cost Settlement|

# Business Process Transactional Steps

|Transactional Step Description|Transaction Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Maintenance Strategy|IP11|Maintenance Strategies (IP11)|
|Create Task List (General / Functional Location / Equipment)|IA05 / IA11 / IA01|Create Task List - (W0021)|
|Create Maintenance Plan (Single Cycle / Strategy / Multiple Counter)|IP41 / IP42 / IP43|Create Maintenance Plan (W0009)|
|Schedule Maintenance Plan (Individual / Deadline Monitoring)|IP10 / IP30H|Schedule Maintenance Plan (IP10)|
|Mass Schedule Maintenance Plans| |(F2774)|
|Maintenance Scheduling Overview & Simulation|IP19|Maintenance Scheduling Overview (IP19)|
|Scheduling Overview List Form|IP24|Scheduling Overview List Form (IP24)|
|Change PM Orders: Selection of Orders|IW38|Manage Orders and Notifications in Information Center (W0019)|
|Goods Issue (Stock Material)|MIGO|Post Goods Movement (MIGO)|
|PM Order Operation Confirmation|IW41 / IW42|Find Maintenance Order and Operation (F2173)|

Page 38 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Transactional Step Description|Code(s)|GUI|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|---|
|PM Order Technical Completion|IW32 / IW38|Confirm Jobs (W0020)|Manage Orders and Notifications in Information Center (W0019)|

# Key Policies and Process Changes associated with the Process

- Use of Fiori Apps like Maintenance Scheduling Board, Resource Scheduling Maintenance Planners & Maintenance Planning Overview
- Automated background scheduling of Maintenance Plans results in timely trigger of Preventive Maintenance Orders

# Standard Reporting

Refer (Standard – GUI & FIORI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Master Data Considerations (including all relevant data relationships)

- Maintenance Work Center
- Functional Location
- Equipment
- Material - Spare Parts
- Maintenance Strategy (Optional)
- Maintenance Task List (General / Equipment / Functional Location)
- Maintenance Plan
- Business Partner – Person Responsible

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

Page 39 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|PM-Completion report|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.2 Preventive Maintenance - Performance based (BPML ID: 5.01)

# Business Process Description:

# Process Characteristics

Process Trigger: Pre-defined Preventive Maintenance Schedule

Process Input: Equipment / Functional Location, Maintenance Strategy, Task List, Maintenance Plan & Background Scheduling

Process Output: Preventive Maintenance Order

Process Owner: Maintenance Department

Process Volumes: Approx. 10 Per Day

Process Frequencies: For example, every 500 / 1000 / 2000 / 4000 / 5000 / 6000 / 7000 Hours

# As is:

Equipment based on running hours, counters falls under this category for preventive maintenance like compressors.

If spares and consumables are required for the maintenance activities, it will be issued from stores by maintenance dept itself for the work order. If stock is not available in store, then it will be procured from outside and issued to the maintenance team.

Spare parts list not maintained fully and consumption is not maintained or tracked inside the system.

# As is Process flow diagram:

Page 40 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# To Be:

With performance-based maintenance plans, we can plan regular maintenance based on counter readings maintained for measuring points at pieces of equipment and functional locations.

To represent simple maintenance cycles, we can create a single cycle plan. To represent complex maintenance cycles, we can create a strategy plan based on a performance-based maintenance strategy.

We create a strategy plan and assign a maintenance strategy in which we have defined the maintenance cycles (in the strategy maintenance package).

A maintenance strategy contains general scheduling information and can therefore be assigned to as many maintenance plans and maintenance task lists as required.

For Example: A maintenance task is performed on a reference object after every 1000, 2000 & 5000 operating hours.

For each scheduling the system calculates the due dates for a maintenance call object on the scheduling parameters and the maintenance cycles.

Maintenance planner will schedule the maintenance plan such as orders will get generated some days before actual planned dates.

This reminder interval can be set using Deadline Monitoring.

# Change Order and Release:

After scheduling the maintenance plan the maintenance call object is created automatically.

Then we can proceed with the same cycle after releasing your maintenance order.

Page 41 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Time confirmation:

Enter time completion confirmations for operations.

# Technical confirmation:

Complete the order technically once the maintenance work has been completed.

# Order settlement:

The cost collected in the PM order should be settled at Maintenance Cost center.

# Business Complete:

Business completion of an order is performed when no further costs are expected to be posted to the order.

Preventive maintenance completion of task can be opened up in mobile application (Field tekpro), confirmation can be given for each task with final TECO to complete the order.

With performance-based maintenance plans, regular maintenance is planned based on counter readings maintained for measuring points at pieces of equipment and functional locations. To represent simple maintenance cycles, we can create a single cycle plan. To represent complex maintenance cycles, we can create a strategy plan based on a performance-based maintenance strategy.

# Business Process Steps in Detail

# Measuring Point Counter

Business can use this component in Plant Maintenance to enter counter readings for technical objects. Using the measuring point counter, we can document the latest status (like running hours, kilometres, etc.) of a technical object at a particular point in time. Documenting the latest status of a particular object is of great importance in cases where detailed records regarding the latest status have to be kept for legal reasons. This could involve critical values recorded for environmental protection purposes, hazardous working areas that are monitored for health and safety reasons.

# Counter based maintenance

Counter based maintenance tasks are another type of preventive maintenance. Generally, these tasks should reduce the number of breakdowns for the objects. In case of a counter-based maintenance, maintenance activities are always performed when the counter of the technical object has reached a particular counter reading, for example, every 1000 operating hours.

The data transferred to the system after a measurement has been taken for a measuring point counter is described in the SAP system as a measurement document. This data transfer can be performed automatically or manually. The measurement document is therefore the result of a measurement or counter reading being entered in the system.

# Create Measurement document (Transaction Code: IK11)

The measurement document shall be created against the measuring point counter.

# Create Maintenance Item (Transaction Code: IP04)
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

A maintenance item describes which preventive maintenance tasks should take place regularly at a technical object or a group of technical objects.

A maintenance item can be assigned to reference objects (for example, equipment or functional locations) to align a maintenance item where you want to perform the maintenance task.

We can assign one or more maintenance items to a maintenance plan. A maintenance plan always automatically contains at least one maintenance item.

We can assign maintenance items to a maintenance plan in the following ways:

- Create a maintenance plan and create a maintenance item directly in the maintenance plan by entering the required data on the Item tab.
- Create additional maintenance items in a maintenance plan.
- Create a maintenance item without assignment and subsequently assign it to a maintenance plan.

A maintenance item can only be assigned to one maintenance plan. We must have created the maintenance item we want to assign to a single cycle plan without reference to a Maintenance strategy. The maintenance item assigned to a strategy plan must have the same maintenance strategy as the Maintenance plan. The maintenance item assigned to a strategy plan must have the same maintenance plan category as the Maintenance plan. We can assign an equipment / functional location to a maintenance item at which we want to perform the maintenance task. The easiest way is to create maintenance items directly in the maintenance plan.

# Selection of PM task List in the Maintenance Item

Maintenance task lists are used to process planned and unplanned maintenance tasks. Maintenance task lists are key reference data in the planning, execution steps and gathering actual information for a maintenance order, as would a routing/recipe for production and process orders. Maintenance task lists describe the individual steps which must be executed for inspections, repairs, and preventive maintenance. In addition, they list the spare parts and tools required for the job and specify the necessary completion time.

Preventive Maintenance Task List are three types. They are:

- Equipment Task List
- Functional Location Task List
- General Task List

A Maintenance Item can use any task list as required for maintenance plan. We include this information, if necessary, in a maintenance item by assigning a task list to it. If we work with strategy plans, enter a maintenance strategy in the task list. This means that we can assign the maintenance packages of the assigned maintenance strategy to individual operations in the task list.

In time based preventive maintenance, Equipment task list, Functional Location task list and General task list will be prepared with details of activities and with the details of resources required to execute the maintenance task.

For time-based maintenance plans with a strategy, the task list and the maintenance item must have the same strategy. The status Released must be set for the task list.

Page 43 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Create Maintenance Plan (Transaction code: IP41/IP42/IP43)

Maintenance plan will be prepared with the details of the equipment / functional location and scheduling parameters. Based on the scheduling parameters a maintenance order will be generated by the system. Scheduling can be done manually and automatically.

# Single Cycle Plan

Single cycle plan is the simplest form of maintenance plan. In this process, single cycle plan is created with one-time based maintenance cycle (it contains the details of time when maintenance must be performed). It might be used, for example, for the annual maintenance of a DG Set at every 500, 1500 and 4500 hours.

# Strategy Plan

The maintenance plan with use of strategy is useful when different operations of a task list are to be performed at different interval of time. The strategy in task list should be the same as that in the maintenance plan(s). The maintenance strategy defines the rules for the sequence of planned maintenance operations. It includes general scheduling information and can be assigned to as many maintenances task lists, and maintenance plans as required. Maintenance Packages contain the details of time when maintenance must be performed.

We use the maintenance plan category to determine which maintenance call object the system generates for a maintenance plan when a maintenance call is due (for example, maintenance order, notification, etc.,), which in turn generated automatically. For example, every 1000 hours, 2000 hours, 3000 hours and so on.

We use the maintenance plan category to determine which maintenance call object the system generates for a maintenance plan when a maintenance call is due (for example, maintenance order, notification, etc.,), which in turn generated automatically.

# For example, a Maintenance Strategy (Performance Based) is shown below:

|Name|02| | | | | |
|---|---|---|---|---|---|---|
|Description|Performance based maintenance| | | | | |
|Scheduling indicator|Activity| |Pack: seq:| | | |
|Package No:|Cycl length|Unit|Maintenance cycle text|Cycle ShortText|Hierarchy|Hierarchy ShortText|
|1000HR every|10|HL| | | | |
|2000HR every|20|H2| | | | |
|3000HR every|30|H3| | | | |
|4000HR every|40|H4| | | | |
|5000HR every|50|H5| | | | |
|6000HR every|60|H6| | | | |
|000HR every|70|H7| | | | |

# Assign Scheduling Parameters

Page 44 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

We can use the scheduling parameters to adapt the scheduling process to meet our individual requirements. The scheduling parameters are as follows:

- Scheduling Period
- Completion Requirement
- Call Horizon
- Shift Factor
- Cycle Modification Factor
- Scheduling Indicators
- Cycle Start

# Scheduling Parameters in detail

# Scheduling Period:

Determines the period of time, for which the system generates planned or call dates during scheduling, i.e. time for which maintenance jobs should be scheduled (365 days).

# Completion Requirement:

By setting the indicator, the system only generates the next maintenance call object once the previous call object has been completed.

# Call Horizon:

Determines when a maintenance order should be generated for a maintenance call, i.e. how early from the planned date of job, the order should be generated in the system as a % of the cycle time.

# Shift Factors:

The shift factors for early/delayed confirmation of a maintenance task define what % of the shift should be considered for the next date. i.e. in case if the maintenance task is confirmed early/delayed by 2 days then the next maintenance call will be preponed or postponed based on this input.

# Cycle Modification Factor:

By entering a cycle modification factor, we can lengthen or shorten the cycle specified in the maintenance strategy. A cycle modification factor greater than 1 lengthens the cycle, whereas a factor less than 1 shortens the cycle. For example, a maintenance strategy with total cycle duration of 60 days is assigned to the maintenance plan and we want to change that for this plan. Therefore, when we enter the cycle modification factor as 1.5 the result would be 60 x 1.5 = 90 days.

# Scheduling Indicator:

There are three scheduling indicators in the Maintenance Planning component. They are used for the following scheduling options:

- Time-based scheduling
- Scheduling based on a key date
- Scheduling by factory calendar

# Cycle Start:

Date on which the cycle should start. It is required for calculating planned and call dates. From this date, system starts to calculate the planned and call dates based on the cycle.

# Schedule Time based Plan (Transaction code: IP10)

We schedule a maintenance plan which the system generates maintenance call objects (for example, maintenance order or notification) for the defined cycles.

Page 45 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

You create several maintenance plans. Each maintenance plan contains a maintenance item that describes the object to be maintained. The system generates a separate order with reference to notification for each object on a due date.

For each order in scheduling, the system calculates the due date (planned date) for a maintenance call object based on the scheduling parameters and the maintenance cycles or packages and generates maintenance calls.

When the maintenance call is due, the system generates a maintenance call object for each maintenance item due, which object the system generates is determined by the maintenance plan category.

If notifications and orders are generated through a maintenance plan, the date of the notification or order completion is used for the further scheduling of the maintenance plan.

We can use this function to simplify the generation of maintenance call objects for maintenance plans. Start the deadline monitoring at regular intervals using an internally programmed report (for example, weekly or for a weekly cycle). The system then generates the maintenance call objects according to the cycles defined.

A start date must have been entered in the scheduling parameters for the maintenance plan, or we must have already scheduled the maintenance plan.

When we run the deadline monitoring function, the system converts all the maintenance calls, for which the call horizon has been reached, into maintenance call objects. The system also performs a complete rescheduling of the maintenance plan and ensures that maintenance calls are always available for the period which you have defined as the scheduling period.

# Process Preventive Maintenance Order (Transaction code: IW31 / IW32 / IW38)

The order for Preventive Maintenance will be generated automatically as per the frequency defined in the Maintenance Plan. Maintenance Planner checks the order and starts the Time-based preventive maintenance work as per order. If required, we change the status of system condition as 0, which means the equipment / functional location is not in operation.

# Material and Resource Planning (Material Reservation, Issue and Procurement process)

# Material Planning

Material planning is the process through which all the materials and spares are planned as required to carry out a maintenance task. All the materials required for carrying out maintenance work are planned based upon the task list creation. In the task list, the preventive maintenance activities to be performed are divided into operations and for each operation the material required is assigned. The required quantity, the item category i.e. whether stock item or non-stock item will be mentioned in the order.

The results of material planning, material availability is checked for Stock item or Non-Stock Items. If material is available (in Stock), then item Category is Set to be L and a Reservation No. is generated to reserve and issue the material from Stores. If material is not available in Stock, then Item Category N is Set for which a Purchase Requisition No. is Generated after saving the Order which will be used by Procurement Department to generate the necessary Purchase Order.

# Resource (Manpower) Planning
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Resource Management is part of the Planning process in a Work Order. When an order is planned, all the resources required for the successful completion of the job is planned. When operations are planned, manpower required for the job in terms of their skills, time required for performing particular operation, total time required to complete the job etc. are all planned and calculated.

Maintenance engineer will assign the resources to the order based on various factors like:

- Internal Resource – if available for a job. In this case the operation control key will remain as PM01, i.e., internal manpower will be used.
- External Resource – if a job is to be carried out by external Service Providers (Vendors). In this case the operation control key is to be changed to PM03, which indicates that the operation is to be performed by external agencies. By doing so, a Service Purchase Requisition can be generated from the maintenance order. The Purchase Requisition can further be processed until Purchase Order.

# Material Availability Check

Materials planned for the execution of order operations can be viewed, or displayed for the operation if they are available on time and in sufficient quantity. The system can only determine and display the necessary information once an availability check has been performed for the required material. We can either perform this check before the order is released, or the system can do it automatically when the order is released. Additionally, Transaction Code MMBE can be used for Material Availability Check any time up to the release of the order.

At any stage during the maintenance order processing, the stock availability of spares reserved for the order can be checked. When the order is released, the system does the availability check and alerts the user if the stock doesn't exist. The alert message can still be ignored, and the work order can be released to execute the work.

# Scheduling

Planning an order with all its operations and components is performed by the scheduling function to determine the following data:

- The actual execution dates based on the dates specified in the order and the time specifications in the operations
- The capacity requirement needed to execute the order, based on the data in the operations
- The date at which a particular material should be available. This date is entered based on the start date for the operation, in which the material is required.

# Order Release (Transaction Code: IW32 / IW38)

After planning, the release of the order can be performed. The following activities are the result from the release of an order:

Page 47 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

- Printing shop papers
- Withdrawing material
- Posting goods receipts
- Entering time completion confirmations
- Completing a task

When we release an order, it has the status REL. This status is a prerequisite for executing the dependent functions outlined above.

When we release an order, the system checks the availability of materials. At the latest when the order is released, the material reservations are relevant for materials planning and can be withdrawn, and the purchase requisitions generated.

# Settlement Rule

The Settlement Rule defines what proportion of the costs are allocated to where (mostly a Cost Center). Entering the correct settlement rule into the system ensures that the costs incurred in the execution of the maintenance work can be settled correctly. The settlement rule must have been specified when the order is released.

The system determines the settlement rule for an order automatically from the reference object, i.e., functional location / equipment.

If no object has been entered in the order, or if we do not want the order settled in the way proposed by the system, the settlement rule can be manually changed. In Club Coffee, the settlement receiver will be the respective cost center of the functional location / equipment.

If the settlement receiver is present in the master data of the reference object, at the time of order release the system automatically creates the settlement rule.

If no settlement receiver is present in the reference object (i.e., no cost center assigned), at the time of release we have to maintain it manually.

# Goods Issue

When the order is generated by the system based on the schedule, a material reservation number is also created against the maintenance order. During the execution of work, materials are withdrawn against this reservation. When the material is withdrawn, the system automatically creates a goods issue document.

Goods Issue is made against the reservation to facilitate:

- Control of issue and check that the correct material is being issued
- Accurate and real time records of all material issues and receipts for maintenance work

Since the material is issued against the order, it makes data entry quicker, accurate and with relevant reference.

The quantity withdrawn is updated in the order as well as in the reservation. This reduces the reserved quantity.

For unplanned materials, goods are issued against the order to capture the material and cost details in equipment history. After completion of work, excess or unused materials can be returned back to inventory.
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

The material issue transaction being handled through Transaction Code MIGO by Engineering Stores against material reservation / maintenance order.

# Pre-Closing Activities

# Actual Time Confirmation (Transaction Code: IW41 / IW42 / IW45)

This process will be used to record the actual activity and interval in the maintenance order. It will be used to identify:

- Who processed the operations specified in the order
- The time required for completing the operation, or if not completed, the remaining time required
- If all the materials specified in the order has been used, and if used, whether reservations have been cleared

After completion of work, the actual status is to be updated in the maintenance order to understand the difference between the plan and actual data in terms of manpower and material. Material issued will be automatically updated by the system, manpower detail is updated as in time required to complete the operation through the time confirmation.

The following information is documented:

- Time and date on which the operations were completed
- The activity performed
- Remaining work
- Time utilized of the total time required for an operation

# Recording the Observation

In case, a notification is generated along with the maintenance order, following activities shall be performed in the notification.

1. Open the Notification (Transaction Code: IW22 / IW28)
2. Select the item code for failed part
3. Select the damage code
4. Select the cause code of the damage
5. Select the Task to be carried out to prevent such failure in future (if any)
6. Select the activities performed

The notification may further be completed after completing the outstanding tasks within the notification, if any.

# Technical Completion of Order (Transaction Code: IW32 / IW38)

After completion of maintenance order, the maintenance engineer or authorized person sets the status of the order to technically completed. Technical Completion will be used to ensure that further processing of the work order does not take place and all the unutilized resources which have been planned or reserved for the order are released.

Page 49 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

After all the maintenance work is completed the Complete Technically button is clicked. After this the PM Order Status is changed from REL (Released) to TECO (Technically Complete) & Notification Status is set to be NOCO (Notification Completed). While this status is set, no further work can be carried out on the particular Notification / Order. Once an Order is technically completed, outstanding purchase requisitions or material reservations are deleted or cleared. Notifications for the order is also completed. Only the following changes are allowed on an order.

- Lock and unlock the order
- Set the deletion flag

# Plan v/s Actual Cost in an Order

Cost is the value of consumption of stock / non-stock materials, actual work hours and so on, which are required to execute maintenance tasks. Costs are distinguished according to planned and actual costs. Planned costs are calculated automatically by the system during order planning while actual costs for goods issues and goods receipts are calculated automatically by the system whilst the order is being executed. The actual costs for the work performed can only be calculated once the work has been confirmed.

We can display the costs resulting from an order from the Plant Maintenance perspectives in the system, this display is called the cost overview. The cost overview lists the individual value categories. A value category is a grouping of cost elements.

# Order Settlement (Transaction Code: KO88)

Order settlement is used to control costs and to identify where maximum costs are being incurred for maintenance. Costs associated with the maintenance work are assigned to Cost centers / internal order. Costs arising out of executing an order are initially collected in the order. These costs are then transferred to a receiver, for e.g., Cost Center. The receiver of costs is specified in the order and settlement carried out at regular intervals by finance / accounting department.

# Business Completion of Order (Transaction Code: IW32 / IW38)

Business completion of an order means ‘final completion of an order’. When an order has been fully executed and all the costs incurred in it are settled, then the status of the order can be changed to Business Completion (CLSD) and no further processing can be done on it. This ensures that no further postings of any kind are carried out on it. Business Completion of orders is performed when after all the work has been completed and all the costs settled.

Business Completion of an order is done after it has been:

- Technically completed
- Costs have been fully settled and the order balance is zero
- There are no open purchase orders for that specific maintenance order

When an order is given the status completed, then the system checks that settlement has been done and the order balance is zero and no outstanding purchase orders exist.

Page 50 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

No more postings can be done on it against the order. If for any reason the work has not been performed and the order is given the status CLSD then the system generates error message depending upon the error. For example, if the order is not settled (i.e., balance of cost is not zero) then the system gives error message ‘Order balance is not zero’ and the status of the order cannot be changed.

# Business Process Flow Diagram

|Preventive Maintenance (Performance Based)|Maintenance|Plant Maintenance Purchase Material|Finance/Costing|
|---|---|---|---|
|CIEZ Meusurinu|Crale Mrasinno|Documanl| |
|Schcnua|Vbintenance Fian|Orcor crozicg|Mainlenel|
|Creare Servico|Purc" 931|Rcmisior| |
|Exterriz|Scnc?|Requite| |
|Creale Seivice PO|SpSas|Requlit?| |
|Stact Availabl|Cieal Puchise|Remuis -ion FRI| |
|Creale|Resonaton|Cicatc Pucnc|Ordar from PR|
|Jood3 Rece %|#quinst PC|Involca Vanhoniog|Cruds Iut|
|Nnnsl|Orcer|PayManllo|Veljal|
|Teclinkal|Camelchan|Cosl|Sotic Men|

# Business Process Transactional Steps

|Transactional Step Description|Transactional Step Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Measuring Point|IK01|Create Measuring Point (IK01)|
|Create Measurement Document -|IK11|Create Measurement Document for|
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Transactional Step Description|Code(s)|GUI / SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Initial| |Technical Object (W0014)|
|Create Task List (General / Functional Location / Equipment)|IA05 / IA11 / IA01|Create Task List - (W0021)|
|Create Maintenance Plan (Single Cycle / Strategy / Multiple Counter)|IP41 / IP42 / IP43|Create Maintenance Plan (W0009)|
|Schedule Maintenance Plan (Individual / Deadline Monitoring)|IP10 / IP30|Schedule Maintenance Plan (IP10)|
| | |Mass Schedule Maintenance Plans (F2774)|
|Maintenance Scheduling Overview & Simulation|IP19|Maintenance Scheduling Overview (IP19)|
|Scheduling Overview List Form|IP24|Scheduling Overview List Form (IP24)|
|Change PM Orders: Selection of Orders|IW38|Manage Orders and Notifications in Information Center (W0019)|
|Goods Issue (Stock Material)|MIGO|Post Goods Movement (MIGO)|
|PM Order Operation Confirmation|IW41 / IW42|Find Maintenance Order and Operation (F2173)|
| | |Confirm Jobs (W0020)|
|PM Order Technical Completion|IW32 / IW38|Manage Orders and Notifications in Information Center (W0019)|
|Create Measuring Point|IK01|Create Measuring Point (IK01)|

# Key Policies and Process Changes associated with the Process

Use of Fiori Apps like Maintenance Scheduling Board, Resource Scheduling Maintenance Planners & Maintenance Planning Overview.
Automated background scheduling of Maintenance Plans results in timely trigger of Preventive Maintenance Orders.

# Standard Reporting

Refer (Standard – GUI & FIORI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Master Data Considerations (including all relevant data relationships)

- Maintenance Work Center
- Functional Location
- Equipment
- Catalog
- Measuring Point / Counter
- Material - Spare Parts
- Maintenance Strategy (Optional)
- Maintenance Task List (General / Equipment / Functional Location)
- Maintenance Plan
- Business Partner – Person Responsible

# Reporting (ABAP & BI / BO)

Refer (Customised – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

Page 52 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Interfaces

|Description|Interface|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.3 Shut Down Maintenance (BPML ID: 6.0.1)

# Business Process Description:

# Process Characteristics

Process Trigger: All maintenance activities due during Plant off-season / annual shutdown period

Process Input: Pre-defined annual shutdown activities

Process Output: Shutdown orders and all open notifications & orders earmarked for closure during shutdown period

Process Owner: Maintenance Department

# Process Volumes

Process Frequencies: During Plant off-season / annual shutdown period (once or more than once per year)

# Business process flow:

As is:

In 65 Plant We have shut down maintenance Business team performing maintenance activities with a frequency of one year.

Page 53 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

In 101 Plant shutdown maintenance is there captured from spreadsheet as well as from the system for yearly maintenance task schedule.

Identifying the list of equipment’s on which maintenance has to be performed.

Perform list of check list/activities against each equipment wise as per annual schedule.

No of hours spent on captured in the system.

If spares and consumables are required for the maintenance activities, it will be issued from stores by maintenance dept itself for the work order. If stock is not available in store, then it will be procured from outside and issued to the maintenance team.

Spare parts list not maintained fully and consumption is not maintained or tracked inside the system.

# As is Process flow diagram:

# Club Coffee Shutdown Maintenance Process Flow

|1|Shutdown Schedule|
|---|---|
|1|General Order Work|
|1|Annual Physical Spare Task|
|1|Shutdown Task Execution|
|1|Verification of Work Order|
|7|Spares consumed|
| |Work Order analysis for difference|

Page 54 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# To Be:

- Planned maintenance order is created with separate order type for annual shutdown maintenance.
- Based on maintenance history reports and pending points, scope of work is defined by list of operations.
- Maintenance spares are planned and listed in maintenance order.
- Services planned and maintained.
- Manpower requirement is planned and assigned to the operations.
- If spares are not available, then spares will be procured through PR.
- If spares available, Reservation will be raised and materials will be withdrawn from stores.
- For external services, service PR will be generated and processed.
- After job completion, time confirmations will be done for all operations.
- Service entry sheet will be created.
- Maintenance order will be completed technically.
- Cost settlement will be done.
- Maintenance order business completion will be done.
- Shut Down maintenance completion of task can be opened up in mobile application (Field Tek pro where confirmation can be carried out with final tech completion to close the process).

# Business Process Steps in Detail

The various steps involved in a shutdown maintenance process is described in detail as below:

# Create Maintenance Revision (Transaction Code: OIOB)

Maintenance revision is used to group / collect multiple service or maintenance tasks under one number, which need to be performed in a specific period (e.g., Plant off-season period). These services / maintenance tasks are generally planned long term. You enter a revision number in notifications or in orders and use it to summarize several notifications or orders. You can only assign a revision to a notification or an order if it has the status opened or released. You can then only close it if the assigned notifications or orders are closed. If a revision has the status opened, you can only directly close or delete it if no notifications or orders are assigned to it.

Create a revision by entering data such as the plant, revision name, start date, start time, end date and end time information.

# Create Shutdown Maintenance Order (Transaction Code: IW31)

A Shutdown Order shall be created with reference to an equipment or functional location. The shutdown order would have further details like planner group, work center, maintenance activity type, maintenance revision, etc. In addition, operations and materials shall be assigned within the shutdown order. In case of vendor involved services, necessary service requirement details shall be maintained in the operation tab by changing the operation control key from PM01 to PM03. This would facilitate creation of service PR at the time of order release. In case of similar operations need to be performed for many equipments which are of same construction type, then a general task list shall be created beforehand, so that the general task list shall be assigned to those order operations.

Page 55 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Assign Maintenance Revision (Transaction Code: IW21 / IW22 / IW28 / IW31 / IW32 / IW38)

A maintenance revision denotes period of time during which a plant or a part of a plant is temporarily shut down for off-season / turnaround events, so that service or maintenance work can be performed and retrieved for reporting purposes. For a given period, only one revision can be valid for an order / notification.

When a revision is assigned to an order / notification, the basic start & end dates are changed automatically based on the dates defined in the revision master. In other words, the basic start & end dates which were originally picked by the system based on notification / order priority is overridden.

For reasons, if dates in revision master have been revised after the assignment of revision in a notification / order, the new revised dates will not be populated in notification / order.

A revision master is Work Center / Plant specific in nature. However, by maintaining different nomenclature / codification, revisions can be created and maintained for production line wise, location wise, system wise shutdown operations, within a Plant.

# Assignment of Maintenance Revision in open / deferred Notifications & Orders

For reasons, any open / deferred Notifications & Orders which could not be processed as per the schedule but are planned to be attended and completed during the shutdown period can be assigned with Maintenance Revision. This facilitates the Maintenance Department to easily segregate and identify those open Notifications & Orders marked with Maintenance Revision to be attended during the shutdown period.

# Processing Shutdown Orders (Transaction Code: IW21 / IW22 / IW28 / IW31 / IW32 / IW38)

# Non-Stock Material Procurement (Transaction Code: IW31 / IW32 / IW38)

Any materials that are required to attend the shutdown maintenance but are not available in stock or which is a new material, shall be procured through Purchase Order which would have reference to the Purchase Requisition.

Purchase Requisition for procurement of such materials can be created against each operation within the order. In this case, the PR will have a direct reference to the shutdown maintenance order. Such material procurement shall be consumed directly against the shutdown maintenance order and will not go through the inventory.

To create a Purchase Requisition for a non-stock material, ensure to change / maintain the ‘Item Category’ as N (Non-Stock) in addition entering the material code and quantity required.

# External Services Processing (Transaction Code: IW31 / IW32 / IW38)

For any services that are required to be performed by an external agency to attend the shutdown maintenance, shall be procured through Purchase Order which would have reference to the Purchase Requisition which was created against operation within the order.

To create a Purchase Requisition for external services, ensure to change / maintain the operation control key as ‘PM03’, in the operation of order. In addition, maintain the material group, purchase group/organisation, vendor (if known) and the external service details (i.e.
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

service master number, if available, service description, quantity, unit of measurement, approximate value of the external service and cost element).

# Goods Issue & Return of Stock Items (Transaction Code: MIGO)

Materials which are available in stock that are required for maintenance work will be issued from stores, against the material reservation slip number for the maintenance order. The material reservation slip can be printed if required, by the maintenance dept. Any unused materials shall be returned back to the stores. In such cases, the material document number which was generated at the time of Goods Issue should be used as a reference during goods return.

# Actual Work Execution

Once all the resources are made available to perform the work, the shutdown maintenance is attended physically and completed. During the course of shutdown maintenance work (i.e. order processing), maintenance person responsible shall update additional activities or spares required to perform the work, as part of order planning process.

# Operation Confirmation (Transaction Code: IW41 / IW42)

For activities performed, maintenance person responsible shall carryout actual time confirmation for each of the operations performed against the planned time.

# Creation & Acceptance of Service Entry Sheet (Transaction Code: ML81N)

After the vendor completes the work based on the Purchase Order (with reference to the Purchase Requisition No. & Order No.), the maintenance person responsible shall acknowledge / certify the quantity of the work done by the vendor, through creation & acceptance of ‘Service Entry Sheet’. Partial acceptance of ‘Service Entry Sheet’ is also allowed. However, acceptance of a quantity which is more than the quantity defined within the Purchase Order is not accepted. In such cases, a fresh Purchase Order shall be created and issued to the vendor.

# Technical Completion (Transaction Code: IW32 / IW38 / IW22 / IW28)

Maintenance person responsible shall update the technical findings / observations and work completed date & time in the Maintenance Order after the reasonable observation time to monitor the performance of the equipment, if required. Maintenance person responsible will technically complete the Maintenance Order upon completion of the actual work.

# Order Settlement (Transaction Code: KO88 / KO8G)

Once the order is technically completed, all the costs booked to the order would be transferred to the relevant cost center, which was maintained in the ‘settlement rule’ within the order. For this, order settlement is done. Order settlement is done periodically or once fully.

# Business Completion (Transaction Code: IW32 / IW38)

Page 57 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Once the order is fully settled, then the order shall be business completed, which means, cost booking of any sort to the order is no longer possible.

# Closure of Maintenance Revision (Transaction Code: OIOB)

Once all the notifications & orders have assigned with the revision have been technically completed, then the revision can be closed by activating the check box provided in the revision. This means that the revision is no longer valid and hence cannot be assigned in notifications or orders.

# Business Process Flow Diagram

# Shutdown Maintenance Process

|Maintenance Planning|Plant Maintenance Management|PurchaselMaterial|Finance/Costing|
|---|---|---|---|
|Cruille Revisoin|Cre3-€ Orcar|Periding|UNanuaMram|
|Nohjicatoni|Atign mevzin Io|Ordor| |
|Mainenari|Onder|Orier Rclarcd|Craata Samacn|
| |Purchase|Rruisiion|Senvica|
|Raquirao|Crebie Senica Ko|Scars|Requleo|
| |Enir Shaat|Ceatt Purcast|Requisitin (PR)|
|Create Purcnart|CndarFrom PR|Gocjs Racaipt|auainstpo|
|Guuds Ig2Je|Regenraton|Crjor|Payrienl lo|
|Callurna lol|Tochnica|Order Casl|3ult ement|

# Business Process Transactional Steps

Page 58 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Transactional Step Description|Code(s)|GUI SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Maintenance Revision (before start of shutdown period)|OIOB|Not Available|
|Create PM Order and assign Maintenance Revision in PM Order|IW31|Process Maintenance Order (W0017)|
|PM Order Release|IW32 / IW38|Manage Orders and Notifications in Information Center (W0019)|
|Create Purchase Order w.r.t Purchase Requisition|ME21N|Manage Purchase Orders (F0842A)|
|Goods Receipt (Non-Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Goods Issue (Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Create & Accept Service Entry Sheet w.r.t Purchase Order|ML81N|Manage Service Entry Sheets - Lean Services (F2027)|
|PM Order Operation Confirmation|IW41 / IW42|Find Maintenance Order and Operation (F2173) Confirm Jobs (W0020)|
|PM Order Technical Completion|IW32 / IW38|Manage Orders and Notifications in Information Center (W0019)|
|Completion of Maintenance Revision (after end of shutdown period)|OIOB|Not Available|

# Key Policies and Process Changes associated with the Process

Assignment of Maintenance Revision functionality in open Notifications & Orders (having system status created, in process & released) as a differentiator to be processed during the planned shutdown period.

Use of Fiori Apps like Process Maintenance Order (create, change & display), Manage Orders and Notifications in Information Center, Find Maintenance Order and Operation & Manage Orders and Notifications in Information Center.

# Standard Reporting

Refer (Standard – GUI & FIORI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Master Data Considerations (including all relevant data relationships)

- Maintenance Revision
- Maintenance Work Center
- Functional Location
- Equipment
- Catalogs
- Material - Spare Parts
- Business Partner - Person Responsible

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

Page 59 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Interfaces

|Description|Interface|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.4 Calibration Maintenance (BPML ID: 7.0.1)

# Calibration Maintenance Process

# As is:

Internal calibration of equipment’s is being identified for calibration of equipment’s from the master list is part of Preventive maintenance category, where Calibration due compliance is checked as per calibration Schedule.

External Calibration is carried out for set of equipment’s by external vendor, where they will give the complete report on the calibration and Calibration certificate will be issued to the equipment’s whichever is under for calibration.

# As is Process flow diagram:

Page 60 of 110
---
# Plant Maintenance Business Blueprint Document

# Club Coffee

# As Callbialon Maintenance Process Flow

|Start|Cal-Task list|Schedule|GenErrderWork|
|---|---|---|---|
|Manual Assignment|Physical Tool|Spare Requirement|Reference|
|Cal Task|Calibration Task|Assignment Name|Work Order Closure|
|Spares consumed|The Equipment|Work Order Analysis for Calibration|Adherence|

# To-Be

Annual plan for Calibration maintenance is drawn up for equipment’s like temperature and pressure gauges.

Maintenance strategy and packages (Monthly, half yearly, yearly) are created to capture the frequency of calibration.

Task lists are created to capture the calibration activity/operation.

Enter operations, time and manpower required for the operation and components with item category.

Maintenance Plans are created for equipment with reference to task lists.

For time-based maintenance, through strategy parameters, scheduling parameters and deadline monitoring, auto generation of maintenance orders will be carried out.

# Schedule Maintenance Plan

We can schedule a maintenance plan with which the system generates maintenance call objects for the defined cycles.

Maintenance order type ZM05 is created from the system as per plan.

For each scheduling the system calculates the due dates for a maintenance call object on the scheduling parameters and the maintenance cycles.

Page 61 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Maintenance planner will schedule the maintenance plan such as orders will get generated some days before actual planned dates. This reminder interval can be set using Deadline Monitoring.

# Change Order and Release:

After scheduling the maintenance plan the maintenance call object is created automatically. Then we can proceed with the same cycle after releasing your maintenance order.

# Time confirmation:

Enter time completion confirmations for operations.

# Technical confirmation:

Complete the order technically once the maintenance work has been completed.

# Order settlement:

The cost collected in the PM order should be settled at Maintenance Cost center.

# Business Complete:

Business completion of an order is performed when no further costs are expected to be posted to the order. Calibration maintenance completion of task can be opened in mobile application (Field tekpro), confirmation can be given for each task with final TECO to complete the order.

The objective of a calibration inspection is to determine whether each piece of equipment specified in the maintenance order meets the predefined performance specifications. Based on results, a decision can be taken whether the equipment/instrument can be put in operation or to be rectified.

Calibration order is used to check the accuracy of a measuring instrument or equipment. If calibration or inspection is to be done on regular basis (planned), maintenance plan will be used to generate calibration order. In this process, Calibration order is generated automatically by the system. Calibration order can be created directly, if calibration or inspection is to be done spontaneously (on need basis). For example, if a Pressure gauge is not measuring exactly and if it has to be inspected or calibrated immediately, a calibration order can be created directly.

The measuring instruments/equipment’s which are all to be calibrated are to be identified by individual departments. The measuring instrument/equipment number, parameters which are to be inspected and with their acceptable values, frequency of inspection, etc. are to be prepared by them and to be forwarded to Master data Maintenance team. Once the master data is created in the system, the user departments can do inspection/calibration as per the frequency of inspection. After the inspection, the actual values will be recorded. Based on actual values, Usage Decision can be entered by Authorized person.

# The process involved in Calibration Order is as follows:

1. Creating the Maintenance Plan
2. Assigning and Displaying the Task List
3. Scheduling the Maintenance Plan
4. Displaying the Calibration Order and the Inspection Lot
5. Entering Characteristic Values
6. Entering the Usage Decision
7. Confirming the Order
8. Settling the Order
9. Closing the Order

# Creating the Maintenance Plan (Transaction code: IP41)

Page 62 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Maintenance plan is used to generate a calibration order for the inspection of the measuring instrument / equipment. Maintenance plan will be prepared with the details of activities to be performed, characteristics to be inspected and values of the characteristics. It will be done by assigning Task list with the Maintenance Plan. It also consists of details of equipment / measuring instrument and scheduling parameters. Based on the scheduling parameters, Calibration Order will be generated by the system. Automatic release of calibration order enables the immediate creation of an inspection lot.

# Assigning and Displaying the Task List (Transaction code: IP01)

The Task Lists used for Calibration / Inspection are created with the details of activities to be performed, parameters to be inspected (MIC) and its acceptable limit (Lower limit, Upper limit or Acceptable limit), Sampling type, etc. The Master Inspection Characteristics are of two types, one is Qualitative and another one is Quantitative. The MIC’s are created and assigned with the task lists. The task lists are assigned with the Maintenance Plan by displaying and selecting the suitable task lists.

# Scheduling the Maintenance Plan (Transaction code: IP10)

The Maintenance Plan can be scheduled automatically or manually. Maintenance Plan can be scheduled automatically by defining the scheduling parameters (Immediate, Date/Time, After Job, After Event, etc.) in Background Job. Maintenance Plan can be scheduled manually by calling the suitable maintenance plan at regular intervals. Based on the scheduling parameters, the calibration order is generated with the inspection lot number.

- We schedule a maintenance plan with which the system generates maintenance call objects (for example, maintenance orders or Notification) for the defined cycles.
- You create several maintenance plans.
- Each maintenance plan contains a maintenance item that describes the object to be maintained.
- The system generates a separate order with reference to Notification for each object on a due date.

# Displaying the Calibration Order and the Inspection Lot (Transaction Code: IP24,IW32)

When the Maintenance Plan is scheduled at regular intervals, the system generates a Calibration order with an Inspection Lot. The inspection lot number can be viewed from calibration order process itself. The person in-charge will check the system for outstanding orders and select the desired equipment’s calibration order. In particular, if he wants to select the outstanding calibration orders only, he can select by entering the Order type for Calibration. The system automatically copies the information about the procedure for the inspection and inspection characteristics from the assigned task list in the order.

# Entering Characteristics Value in result recording (Transaction Code: QA32)

After the inspection / calibration of the measuring instrument / equipment, the inspection results for each characteristic in each operation is to be recorded to determine whether the recorded values are within the predefined inspection specifications. On the basis of the inspection results, each characteristic is to be evaluated and closed. The valuation specifies whether the equipment can be put in operation (accept) or to be rectified (reject). Valuation of equipment can be done manually or the system can evaluate the equipment automatically. If the recorded results are not within specified range, a N2 notification will be raised in the system to proceed with further action on this.

Page 63 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Entering the Usage Decision (Transaction code: QA32/QA11)

The Usage Decision (UD) for an Inspection lot confirms that an inspection has been completed. Usage Decision can be made manually or automatically for one or more inspection lots by means of pre-planned, periodically executed jobs. Usage decision can be controlled by authorization; the UD can be made only by authorized persons, if required.

When the Usage Decision is made for an inspection lot, the system calculates the Quality score automatically.

If the Conditions for acceptance are met, then the Equipment status will be updated manually.

If the conditions for acceptance are not met, then Usage Decision will be entered as Rejected and the equipment status will be automatically set as NPRT-PRT not ready for Use. The notification which is raised during result recording will be set as complete when user decision is made as Rejected.

# Processing the Calibration Order (Transaction code: IW32/IW33)

The user has to take the list of operations along with the material requirement and execute the job. If any more operations/materials are required then those are to be added. If the BOM is available for the technical objects, we can select the component from the list.

System will copy the selected components along with the quantity and create the reservation. Against this reservation the material will be issued from the stores. If any permit is required it has to be assigned.

For external services PR (Purchase Requisition) is created through order and processed. After execution, for external services we have to create the service entry sheet for the services rendered by the external agency.

# Material Availability Check

When materials are planned for executing order operations, they can be displayed as to their availability, on time and in sufficient quantity. Use MMBE Transaction code for Material Availability.

The system can only determine and display the necessary information once an availability check has been performed for the required material. We can either perform this check before the order is released, or the system can do it automatically when the order is released.

At any stage in work order, the stock of spares reserved for the work can be checked. While work order release, system will do availability check and alert the user if the stock doesn't exist. The alert message can still be ignored, and work order can be released to execute the work.

# Scheduling

After an order has been planned with all its operations and components, the scheduling function will determine the following data:

- The actual execution dates based on the dates specified in the order and the time specifications in the operations.
- The capacity requirement needed to execute the order, based on the data in the operations.
- The date in which particular material should be available. This date is entered based on the start date for the operation, in which the material is required.

# Order Release

Finished planning with all the necessary specifications, triggers the next step for release of the order. The release allows the start of activities described. We can only perform the following activities after we have released the order:
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Printing shop papers

# Withdrawing material

# Posting goods receipts

# Entering time completion confirmations

# Completing a task.

When we release an order, it has the status REL. This status is a prerequisite for executing the dependent functions outlined above.

When we release an order, the system checks the availability of materials and the necessary permits. Obtain the necessary permits from the concerned authorities through Hardcopy. At the latest when the order is released, the material reservations are relevant for materials planning and can be withdrawn, and the purchase requisitions generated.

# Settlement Rule

Settlement Rule defines what proportion of the costs on a sender should be settled to which receiver(s). For this, one or more distribution rules are assigned to each settlement sender.

We have to enter the correct settlement rule into the system to ensure that the costs incurred in the execution of the maintenance work can be settled correctly.

In OLAM the settlement rule must have been specified when the order is released. The system determines the settlement rule for an order automatically from the object data (Reference object i.e. Functional Location/Equipment).

If no object has been entered in the order, or if we do not want the order settled in the way proposed by the system, we must enter the settlement rule manually.

In OLAM the settlement receiver will be the respective cost center of the equipment. If the settlement receiver is present in the master data of the reference object, at the time of order release system automatically creates settlement rule. If no settlement receiver is present in reference object, at the time of release we have to maintain it manually.

# Goods issue processing

When the order is generated by the system based on the schedule, material reservation number is also created against the maintenance order. During the execution of work, materials are withdrawn against this reservation. When the material is withdrawn, the system automatically creates a goods issue document.

Goods Issue is made against the reservation to facilitate:

- Control of issue and check that the correct material is being issued.
- Accurate and real time records of all material issues and receipts for maintenance work.
- Since, the material is issued against the order, it makes data entry quicker, accurate and with relevant reference.
- The quantity withdrawn is updated in the order as well as in the reservation. This reduces the reserved quantity.

For Unplanned materials, goods are issued against the order to capture the material and cost details in equipment history. After completion of work, excess or un-used material can be return back to stores.

Page 65 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Pre-Closing Activities

Time confirmation for internal activities (Transaction code: IW41/IW43/IW45) This process will be used to get the current status of a maintenance order. It will be used to identify:

- Who processed the operations specified in the order?
- The time required for completing the operation, or if not completed, the remaining time required.
- If all the materials specified in the order has been used, and if used, whether reservations have been cleared.

After completion of work, the actual status is to be updated in the maintenance order to understand the difference between the plan and actual data in terms of manpower and material. Material issues will be automatically updated by the system, whereas manpower detail is to be updated like time required to complete the operation, manpower used, etc. The following information is documented:

- Time and date on which the operations were completed.
- The activity performed.
- Remaining work.
- Time utilized of the total time required for an operation.

# Recording the Observation

Open the notification T. Code IW22

- Select the item code for failed part.
- Select the damage code.
- Select the cause code of the damage.
- Select the Task to be carried out to prevent such failure in future (if any).
- Select the activities performed.

# Completing the Notification

Complete the notification after completing all the outstanding tasks T. Code IW22.

# Service entry of contractor’s work (Transaction code ML81N)

Service Entry of contractor’s work is to document the work done by contractors for payments to be made per the contract. A purchase requisition is generated for an external service when a maintenance order is generated. This PR is converted to a PO by the purchase department. The PO contains the following details:

- The specifications of work,
- The expected time of delivery, price etc.

Purchase orders are issued to the contractor specifying the nature of the work, time, cost etc. The contractor performs the work. A service entry sheet is created based on the purchase order and in which the service performed is entered. The values from the PO get defaulted into the service entry sheet. The work done by the contractor is checked and accepted by the maintenance engineer or by authorized person. Invoice is sent by the vendor for the work done. Along with service acceptance, invoice verification is also done. The invoice is verified by the FI against the service entry sheet and payment made if the values are correct.

# Work Completion
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Technical Order Completion (Transaction: IW32)

After completion of all work against an order, maintenance engineer or authorized person changes the status of the order to “Technically complete”. Technical Completion will be used to ensure that further processing of the work order does not take place and all the unutilized resources which have been planned or reserved for the order are released. It is very important to fill all the data correctly in order to analyze the causes for Breakdowns. An order is technically completed when all the operations in the order has been fully completed. Once an order is technically completed,

- Outstanding Purchase requisitions or reservations are deleted or cleared
- All notifications for the order are also completed.

Only the following changes are allowed on an order:

- Lock and unlock the order.
- Set the deletion flag.

# Plan v/s Actual Cost in an Order

Cost is based upon the value of usage of materials, work hours and so on, required to execute maintenance tasks. Costs are distinguished according to planned and actual costs. Planned costs are calculated automatically by the system during order planning. Actual costs for goods issues and goods receipts are calculated automatically by the system during order execution. The actual costs for the work performed can only be calculated once the work has been Confirmed. We can display the costs resulting from an order from the Plant Maintenance perspectives. In the system, this display is called the cost overview. The cost overview lists the individual value categories. A value Category is a grouping of cost elements.

# Settling the Order (Transaction code: KO88)

Order settlement is used to control costs and to identify where maximum costs are being incurred for maintenance. Costs associated with the maintenance work are assigned to cost centers / internal order. Costs arising out of executing an order are initially collected on the order. These costs are then transferred to a receiver, for e.g. cost center / internal order. The receiver of costs are specified in the order and settlement carried out at regular intervals by FI.

# Closing the Order (Transaction code: IW32)

Business completion of an order means “Final Completion of an order”. When an order has been fully executed and all the costs incurred on it been settled, then the status of the order can be changed to “Business Completion” and no further processing can be done on it. This ensures that no further postings of any kind are carried out on it.

Page 67 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Completion of orders is performed when after all the work has been completed and all the costs settled.

# Calibration Maintenance Process

|Ji|Create Equipment Master (IEO1)|Create MIC (OS21)|Create Task List (IAOS)|Assign MIC in Task List|Create Strategy Plan|Schedule Maintenance Plan|Order Confirmation|Technical Completion|
|---|---|---|---|---|---|---|---|---|
|Inspection lot Created|Result recording and User decision|Result Notification got Equipment status changed|Maintenance Order created|Order Released|External Service Required|Spares Required|Yes|Create Stock Available Reservation|
| |Create Service Purchase Requisition|Create Service PO|Create Service Entry Sheet|Create Purchase Requisition (PR)|Create Purchase Order (PO)|Goods Receipt against PO|Goods Issue against Reservation|Order Cost Settlement|

# Process Flow, Step Detailed Requirements and Solution

|Process Step Description|Transaction Codes|SAP Dynpro / Classic|APP & APP ID|
|---|---|---|---|
|Create Task List|IA01|Create Maintenance Plan|W0009|
|Add single plan|IP41|Schedule Maintenance Plan|IP10|
|Mass Schedule Maintenance Plans|F2774|Manage Orders and Notifications in Information Center|W0019|
|Result Recording in Inspection Lot|QA32|Record inspection results|F1685A|
|Entering Usage Decision|QA32|Manage Usage decisions|F2345|
|Goods Issue|MIGO|Post Goods Movement|MIGO|
|Create Purchase Order|ME21N|Manage Purchase Orders|F0842A|

Page 68 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Manage Service Entry Sheets - Lean

# Service Entry Sheet

ML81N Services (F2027)

# Order settlement

KO88 Run actual settlement- order (KO88)

# Key Policies and Process Changes associated with the Process

Use of Fiori Apps like Process Maintenance Order (create, change & display), Manage Orders and Notifications in Information Center, Find Maintenance Order and Operation & Manage Orders and Notifications in Information Center.

# Standard Reporting

Refer (Standard – GUI & FIORI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Master Data Considerations (including all relevant data relationships)

- Equipment task List
- Equipment
- Inspection Plan
- Calibration planning parameters
- Master inspection Characteristics (MIC)

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface|Application|Owner|Method|
|---|---|---|---|---|
|NA|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

Page 69 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.5 Predictive Maintenance (BPML ID: 8.0.1)

# Business Process Description:

# Process Characteristics

|Process Trigger|All maintenance activities planned or Predictive maintenance|
|---|---|
|Process Input|Pre-defined Production requirements|
|Process Output|Predictive equipment operations carried out|
|Process Owner|Maintenance Department|
|Process Volumes|Approx. 10 Predictive order will be cf|
|Process Frequencies| |

# Business process flow:

As is:

Most of the predictive maintenance covered under electrical components like measuring temperature of electric motors, measuring voltage, pressure, vibration. When there is an abnormality in measured values, maintenance will be performed by stopping the equipment. Rotating machine vibration status is being monitored and temperature is recorded for the equipment for PM analysis and later on the specific part ex. bearing will be replaced as part of the data analysis. Predictive maintenance is not captured in 7i system and it's done manually.

As is Process flow diagram:

Page 70 of 110
---
# Plant Maintenance Business Blueprint Document

# Club Coffee As Plant Maintenance Process Overview

This Process deals with the Automatic creation of predictive notifications. Measuring points shall be created for the same, where parameters have to be measured. The Parameters will be recorded by Measurement documents. Any abnormality will be notified by Notification to the concerned Maintenance Department for rectifying the same. The notification will be converted to a Maintenance Order. Manpower and material will be planned for the job & the job will be executed.

# Create Measurement Document Against Measuring Point

Measurement Document creation, T-Code IK11. The measurement document will be created against the measurement point. Parameters noted against the Measuring points are to be recorded in an Excel sheet and to be uploaded in the system or can be entered manually.

Page 71 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

If the measured value is deviating from the limits, a notification gets generated automatically.

# Business process flow diagram:

|Create Measuring point (IK01)| | |
|---|---|---|
|Setting upper and lower limits for the measuring point| | |
|Create Measuring Document (IK11)| | |
|If Value Lies Out of the limit|Automatic Trigger of Predictive Notification (N4)|Processing of Notification and further Maintenance processing|

# Process Step Detailed Requirements & Solution

|Process Step Description|Transaction Codes|
|---|---|
|Create Measurement Document|IK11/IK14/IK16/IK22/IK34|
|Change Notifications|IW28|
|Change PM Orders|IW38|
|Goods Movement|MIGO|
|Enter PM Order Confirmation|IW41/IW42|
|Order Closure|IW32|
|Actual Settlement: Order|KO88|

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

Page 72 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Interfaces

|Description|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.6 Capex Installation process (BPML ID: 9.0.1)

# Process Characteristics

Process Trigger: All maintenance activities planned during New equipment installation and existing asset change

Process Input: Pre-defined Production requirements

Process Output: Capital Order for capex process

Process Owner: Maintenance Department

Process Volumes: Approx. 30 capex order will happen.

Process Frequencies:

# Buisness process flow:

As is:

Replacement of new machine or replacement of any obsolete item or any Formation of New line is addressed through Rebuild process in which is having a separate GL account

Page 73 of 110
---
# Plant Maintenance Business Blueprint Document

Entire cost spent for Material and services will hit the specific GL account created by finance in order track the expenses.

New line formation will be initiated as part of production expansion, then it will go through finance for approval for AFE creation. Procurement will be start as part of AFE code created.

New line formation or Modification of existing line will be carried out throughout the year as per the requirement arises.

# As is Process flow diagram:

# Club Coffee As Capex Installation- process

|1|Start|New Line|Production|modification|
|---|---|---|---|---|
|Create New:|Approve|AFE code|Procurement|creation|
|Assignment| | | | |

# To Be:

Assets under construction (AUC) are a special form of tangible assets. They are usually displayed as a separate balance sheet item and therefore require a separate account determination and their own asset classes.

During the construction phase of an asset, all actual postings are assigned to the AUC. Once the asset is completed, a transfer is made to the final fixed asset.

In SAP Plant Maintenance, we can create a project order or investment order to capture the costs of the asset under construction.

During the period and month-end processing will settle the costs from the project order/investment order to the asset under construction. This is done so that budget information can be entered for the AUC and tracking of the actual-to-budget can be performed.

Once the project is completed, the final asset is created in the appropriate asset class, and the project order is set to technical completion (TECO) so that the next settlement will transfer the AUC asset value to the completed asset.

Page 74 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

With the work order cycle in Plant Maintenance, we can define a process wherein we can create a project order with asset under construction, then we can create a budget for the new asset. Release the project order; post the invoice(s) and materials to project order; monitor project order execution; If the Project is already done, we technically complete the project order; come month end, we will settle all charges to the asset and then we can close the project order.

As discussed this can we covered through by finance team for capex installation.

Updated-To be clubcofee pdf Project Maple Club Coffee Trar Updated-To be clubcofee pdf Decision Points_Club Coffee_vZ.C Updated-To be clubcofee pdf

File CJUsers/saravanaraja.t/OneDrive/Updated-To%2Obe%2Oclubcofee pdf

# Business Process Flow

# Business Process Flow Steps in Detail:

External Services Processing (Transaction Code: IW31 / IW32 / IW38)

For any services that are required to be performed by an external agency to attend the Capex maintenance, shall be procured through Purchase Order which would have reference to the Purchase Requisition which was created against operation within the order.

Page 75 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

To create a Purchase Requisition for external services, ensure to change / maintain the operation control key as ‘PM03’, in the operation of order. In addition, maintain the material group, purchase group/organisation, vendor (if known) and the external service details (i.e. service master number, if available, service description, quantity, unit of measurement, approximate value of the external service and cost element).

# Goods Issue & Return of Stock Items (Transaction Code: MIGO)

Materials which are available in stock that are required for maintenance work will be issued from stores, against the material reservation slip number for the maintenance order. The material reservation slip can be printed if required, by the maintenance dept. Any unused materials shall be returned back to the stores. In such cases, the material document number which was generated at the time of Goods Issue should be used as a reference during goods return.

# Actual Work Execution

Once all the resources are made available to perform the work, maintenance person responsible shall update additional activities or spares required to perform the work, as part of order planning process.

# Operation Confirmation (Transaction Code: IW41 / IW42)

For activities performed, maintenance person responsible shall carryout actual time confirmation for each of the operations performed against the planned time.

# Creation & Acceptance of Service Entry Sheet (Transaction Code: ML81N)

After the vendor completes the work based on the Purchase Order (with reference to the Purchase Requisition No. & Order No.), the maintenance person responsible shall acknowledge / certify the quantity of the work done by the vendor, through creation & acceptance of ‘Service Entry Sheet’. Partial acceptance of ‘Service Entry Sheet’ is also allowed. However, acceptance of a quantity which is more than the quantity defined within the Purchase Order is not accepted. In such cases, a fresh Purchase Order shall be created and issued to the vendor.

# Technical Completion (Transaction Code: IW32 / IW38 / IW22 / IW28)

Maintenance person responsible shall update the technical findings / observations and work completed date & time in the Maintenance Order after the reasonable observation time to monitor the performance of the equipment, if required. Maintenance person responsible will technically complete the Maintenance Order upon completion of the actual work.

# Order Settlement (Transaction Code: KO88 / KO8G)

Once the order is technically completed, all the costs booked to the order would be transferred to the relevant cost center, which was maintained in the ‘settlement rule’ within the order. For this, order settlement is done. Order settlement is done periodically or once fully.

# Business Completion (Transaction Code: IW32 / IW38)
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Once the order is fully settled, then the order shall be business completed, which means, cost booking of any sort to the order is no longer possible.

# Business Process Transactional Steps

|Transactional Step Description|GUI Transaction Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Capex order|IW31|Create Maintenance order|
|PM Order Release|IW32|Release Maintenance order|
|Create Purchase Order w.r.t Purchase Requisition|MIGO|Manage Purchase Orders (F0842A)|
|Goods Receipt (Non-Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Goods Issue (Stock Material)|ML81N|Post Goods Movement (MIGO)|
|Create & Accept Service Entry Sheet w.r.t Purchase Order|IW41 / IW42|Manage Service Entry Sheets - Lean Services (F2027)|
|PM Order Operation Confirmation|IW41 / IW42|Find Maintenance Order and Operation (F2173)|
|PM Order Technical Completion|IW32 / IW38|Manage Orders and Notifications in Information Center (W0019)|
|Settle capex order to Asset|KO88|Settlement of order|

# Key Policies and Process Changes associated with the Process

Assignment of Maintenance Revision functionality in open Notifications & Orders (having system status created, in process & released) as a differentiator to be processed during the planned shutdown period.

Use of Fiori Apps like Process Maintenance Order (create, change & display), Manage Orders and Notifications in Information Center, Find Maintenance Order and Operation & Manage Orders and Notifications in Information Center.

# Standard Reporting

Refer (Standard – GUI & FIORI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Master Data Considerations (including all relevant data relationships)

- Maintenance Revision
- Maintenance Work Center
- Functional Location
- Equipment
- Catalogs
- Material - Spare Parts
- Business Partner - Person Responsible

# Reporting (ABAP & BI / BO)

Page 77 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Refer (Customised – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.7 Breakdown Down Maintenance process (BPML ID: 10.0.1)

# Business Process Description:

# Process Characteristics

Process Trigger: Abnormal Condition or Poor Performance of a machine or a system, which results in stoppage, which needs immediate attention.

Process Input: Functional Location / Equipment & Breakdown details

Process Output: Breakdown Maintenance Notification & Order

Process Owner: Production / Maintenance Department

Process Volumes: Approx. 5 Per Day

Process Frequencies: Daily

Page 78 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# As is:

Un-planned maintenance includes any activity that is carried out based on work request or receipt of failure/breakdown from either production team or any other teams. Break down some times its reported by operations and Maintenance team attend the break physically and capture the information in the log book, later they capture in the system. Consumption of spares, consumables are entered in system without any relation to the work order.

Based on the Production information, the equipment breakdown is reported for remedial action. Equipment is attended by technician and cleared. After clearing the breakdown only, Information will be captured in 7i system with the detail info. about the classification of the breakdown and other details.

# Breakdown Details captured in HxGn EAM software:

|HxGn EAM|SAP|
|---|---|
|Line Number|will be captured as a part of Functional Location Structure. Reports can be drawn on the basis of Line Number (functional location structure) in SAP.|
|Name of Supervision|would need to be given during Notification Entry|
|Area Code|will be captured as a part of Functional Location Structure.|
|Equipment|Equipment Number in SAP|
|Sub Equipment Code| |
|Stoppage Reason|will be mapped in Reason Catalog feature of SAP. This can be captured during Notification Entry|
|Down Time (From… To…)|The user entering the Notification will need to enter the down time start and end|
|Total Break Down Time|Automatically Calculated by the SAP system from down time|
|Product Details|Material no|
|Remarks|Standard Notification feature|

# HxGn System:

|Date:|Line|Machine:|Problem description:|
|---|---|---|---|
|Product code:|Problem:|Functional location|Equipment code/desc.|
|Shift:|Solution:|Basic start date|Page 79 of 110|
|Issue:|Empcode:|Basic end date|Time|
|Total Down Time:|Emp name|Job desk:|Remarks:|
|Instances|Status:|Work centre| |
---
# Plant Maintenance Business Blueprint Document

# HxgN Eam 7i system field comparison

This Process deals with the creation and processing of malfunction / breakdown notifications. Malfunction / breakdown notifications will be used to report a Breakdown to Maintenance Department describing a malfunction of an object.

# As is Process flow diagram:

|Club Coffee|As|Breakdown-Maint|
|---|---|---|
|1|Start Equipment Masters| |
|L|Report for Mech/Elec Breakdown assigned for the Task|Spare Requirements assigned for the Fault|
| |Work order close completion| |
|1|Spares consumed to the Equipment| |
|8|1. Breakdown Analysis|2. MTTR / MTBF Reports|

# To Be:

The user informs the Maintenance department about an equipment malfunction or any technical objects by creating a Notification.

The user will input or select the functional location or equipment.

A checkbox provision is made available in the notification to indicate if the notification is a breakdown. This has to be activated whenever it is required that breakdown hours has to be calculated.

Maintenance work centre will be selected to notify the problem. Problem description and remarks will be entered.

Based on the nature of the problem, the user will select the notification type as breakdown notification.

User will save the notification after all necessary input details have been given. Notification number will be generated automatically.

Page 80 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Break-down maintenance completion of task can be opened up in mobile application (Field tekpro), confirmation can be given for each task with final TECO to complete the order.

Mobile Asset Maintenance via Notification creation to TECO

# Screenshots for Reference:

|14.54|15.28|
|---|---|
|Notifications|Cause Code|

|Header|Cause Code|Activity|Task|Object Part|
|---|---|---|---|---|
|Notification Type|NI GT-Maintenance Reqst|Object Part Code|0002|Pulley|
|Notification Short Text|Damage|AIRLOCK|Airlock| |
|Function Location|2080-PRO-LIQ|Damage Code|0002|Abnormal Noise|
|Function Location Name|Liquor production|Damage Description|testing| |
|Equipment Number|10003954|Cause|APH|APH & Economiser|
|Equipment Name|Air Conditioner -(child)|Cause Code| | |

CANCEL
SAVE
CANCEL
ADD

Page 81 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Notifications|10004243|
|---|---|
|Cause Code (1|Activity|
|Notification Type|Notification Type|
|NI GT-Maintenance Reqst|NI GT-Maintenance Reqst|
|Notification Short Text|Notification Short Text|
|Notification 10004243 has been created|Notification 10004243 is changed successfully|
|OK|OK|

|Equipment Number|Function Location Name|
|---|---|
|10003877|Liquor grinding refining B|
|Equipment Name|Equipment Number|
|Pre-Grinder-GMO17|10003877|

CANCEL
SAVE
CANCEL
SAVE

Page 82 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Notifications (32)

12.06.2019

OSNO 10004243

HSC

30.05.2019

Notification 10004221 is completed successfully

OK

if

29.05.2019 4-Low

OSNO 10004217

ios offline change

28.05.2019

OSNO 10004213

chocolate

28.05.2019 4-LOw

In the Breakdown Report Notification, the malfunction start and end time along with the break down check box is activated. Use of Catalogs can assist to assign the object part, damage, and cause codes for a notification. Tasks can be assigned to a notification and the tracking of the tasks are possible.

Each Malfunction / Breakdown Report can be created with a Priority along with details like:

- Affected Functional Location / Equipment
- Created by
- Date & Time
- Short description of Breakdown Incident

# Notification Creation (Transaction Code: IW21)

Malfunctions which occur in any technical system will be reported by Operations / Production Department to the Maintenance Department of that specific location. Based on that information and the investigation, there will be Breakdown report, in which will have assigned the affected functional location / equipment, priority, malfunction start date, malfunction start time and will flag the condition of the equipment to indicate whether it is

Page 83 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

breakdown or working and inform the maintenance department. When the notification is created and saved, the notification attains the System Status OSNO (Outstanding Notification).

The maintenance department will process the breakdown notification by assigning responsible work centre and by putting the notification in ‘in process’. When the notification is put in process, the notification attains the System Status NOPR (Notification in Process).

Note: It is very important that the notification is created as soon as the breakdown is reported or observed.

# Details in Notification

- Each Notification will be given a priority (not mandatory).
- Affected equipment details to be chosen from Equipment Master.
- Coding - Coding will be used to categorize the type of Breakdown. In Club Coffee, the coding will be Electrical Breakdown, Mechanical Breakdown, Utility Breakdown, Electronic Breakdown and Operational Error.
- Reported by - the person who reports the malfunction or break down, a site engineer, supervisor, or officer in-charge of the section. The reporting person is expected to create the notification in system directly. In exigencies, the breakdown may be reported over telephone to the maintenance officer, who may create the notification in system, if system access is not available to the site engineer at that moment in time.
- Date & Time - System proposes current date & time; changes can be made if required. However, system maintains a log of the date and time of notification creation automatically internally.
- Short Description of Job Request - Enter the details in ‘Description’ field.
- Object Part / Damage / Cause Codes can be captured in system in a codified form besides entering it in a text form. Operations / Production department can enter their original first-hand observation of the problem in notification. Later it can be modified by maintenance department to capture exact details.

System Status of notifications can be used to monitor the status of the breakdown work (i.e., Outstanding, In Process & Completed).

The System will be configured to generate a message at the time of creation of notification if equipment is under warranty.

Notifications created for the objects will update the object history automatically.

# Processing of Notification (Transaction Code: IW22 / IW28)

After the maintenance work has been carried out on functional location / equipment, all the pertinent relevant details can be entered as follows:

- Malfunction end date & time
- Damage & Cause of breakdown
- Malfunction attended by

Page 84 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

This helps in the calculation of breakdown duration and analysis of the causes for breakdowns / abnormal occurrences in the equipment and decision / prevention in the future.

# Notification Completion (Transaction Code: IW22 / IW28)

In case of no resources (materials & services) required and upon completion of the actual maintenance work the notification can be completed.

When the notification is completed and saved, the notification attains the System Status NOCO (Notification Completed). It is very important to fill all the data correctly in order to carry out the analysis of the breakdown causes. Technical findings about the maintenance work on equipment are stored in notifications.

# Create Maintenance Order (Transaction Code: IW21 / IW22 / IW31)

In case of resources (materials & services) required to complete the actual maintenance work Maintenance Order shall be created from the Notification screen itself. Maintenance Orders form an important part of the detailed planning of tasks and their accompanying documentation in Plant Maintenance. A technician on site must execute tasks for a technical object. For this, materials, utilities, and staff must be planned and costs estimated. The order supports these tasks, since it primarily contains data for planning and executing tasks, which must be performed at the technical object in question.

The order type is a classification characteristic for orders. It consists of control information that is important for managing orders.

The order type is client based. This means that each order type can be used in all controlling areas.

In Club Coffee, for functional location / equipment maintenance a Maintenance Order shall be created. Orders can be created with or without reference to the notification. It is possible to assign the order subsequently to one or more notifications.

To create a Breakdown maintenance order, go into change mode of notification screen to create an order directly.

While creating an order, following entries would be entered in the order header screen:

- Priority
- Maintenance Activity Type
- System Condition

The order covers the following details:

- Order number – Automatically generated by system upon saving the order
- Functional location / Equipment number for which maintenance work is to be done
- List of operations to be performed – Operations lists out the requirements in terms of number of people, time required, spares, flow of work through relationship between operations and special tools required.
- Whether work should be done in-house or by an external agency or both together is controlled by means of Control keys which are assigned to the operations in an Order.

Page 85 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Materials/Spares

Reservations are created for materials held in stock and for non-stock materials/external services. Purchase requisitions are created automatically when an Order is released.

# Costs

The system calculates the planned costs for an order during the planning stage itself. The actual costs incurred, however, are calculated only after the actual completion of work.

# Settlement

The maintenance order captures the cost through consumption of materials or services (external contractor jobs). This cost remains in the order until it is settled to a cost center. At the month end, a finance department settles the cost-to-cost centre depending upon the status of the order.

# Material and Resource Planning (Material Reservation, Issue and Procurement process)

# Material Planning

Material planning is the process through which all the materials and spares are planned as required to carry out a maintenance task. All the materials required for carrying out maintenance work are planned based upon the task list creation. In the task list, the preventive maintenance activities to be performed are divided into operations and for each operation the material required is assigned. The required quantity, the item category i.e. whether stock item or non-stock item will be mentioned in the order.

The results of material planning, material availability is checked for Stock item or Non-Stock Items. If material is available (in Stock), then item Category is Set to be L and a Reservation No. is generated to reserve and issue the material from Stores. If material is not available in Stock, then Item Category N is Set for which a Purchase Requisition No. is Generated after saving the Order which will be used by Procurement Department to generate the necessary Purchase Order.

# Resource (Manpower) Planning

Resource Management is part of the Planning process in a Work Order. When an order is planned, all the resources required for the successful completion of the job is planned. When operations are planned, manpower required for the job in terms of their skills, time required for performing particular operation, total time required to complete the job etc. are all planned and calculated.

The maintenance engineer will assign the resources to the order based on various factors like:

- Internal Resource – if available for a job. In this case the operation control key will remain as PM01, i.e., internal manpower will be used.
- External Resource – if a job is to be carried out by external Service Providers (Vendors). In this case the operation control key is to be changed to PM03, which indicates that the operation is to be performed by external agencies. By doing so, a Service Purchase Requisition can be generated from the maintenance order. The Purchase Requisition can further be processed until Purchase Order.

# Material Availability Check

Materials planned for executing order operations can be viewed, or displayed for the operation if they are available on time and in sufficient quantity.

Page 86 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

The system can only determine and display the necessary information once an availability check has been performed for the required material. We can either perform this check before the order is released, or the system can do it automatically when the order is released. Additionally, Transaction Code MMBE can be used for Material Availability Check any time up to release of the order.

At any stage during the maintenance order processing, the stock availability of spares reserved for the order can be checked. When the order is released, the system does the availability check and alerts the user if the stock doesn't exist. The alert message can still be ignored, and the work order can be released to execute the work.

# Scheduling

Planning an order with all its operations and components is performed by the scheduling function to determine the following data:

- The actual execution dates based on the dates specified in the order and the time specifications in the operations
- The capacity requirement needed to execute the order, based on the data in the operations
- The date at which a particular material should be available

This date is entered based on the start date for the operation in which the material is required.

# Order Release (Transaction Code: IW32 / IW38)

After planning, the release of the order can be performed. The following activities are the result from the release of an order:

- Printing shop papers
- Withdrawing material
- Posting goods receipts
- Entering time completion confirmations
- Completing a task

When we release an order, it has the status REL. This status is a prerequisite for executing the dependent functions outlined above.

When we release an order, the system checks the availability of materials. At the latest when the order is released, the material reservations are relevant for materials planning and can be withdrawn, and the purchase requisitions generated.

# Settlement Rule

The Settlement Rule defines what proportion of the costs are allocated to where (mostly a Cost Center). Entering the correct settlement rule into the system ensures that the costs incurred in the execution of the maintenance work can be settled correctly. The settlement rule must have been specified when the order is released.

Page 87 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

The system determines the settlement rule for an order automatically from the reference object, i.e., functional location / equipment.

If no object has been entered in the order, or if we do not want the order settled in the way proposed by the system, the settlement rule can be manually changed. In Club Coffee, the settlement receiver will be the respective cost center of the functional location / equipment.

If the settlement receiver is present in the master data of the reference object, at the time of order release system automatically creates settlement rule.

If no settlement receiver is present in reference object (i.e., no cost center assigned), at the time of release we have to maintain it manually.

# Goods Issue

When the order is generated by the system based on the schedule, material reservation number is also created against the maintenance order. During the execution of work, materials are withdrawn against this reservation. When the material is withdrawn, the system automatically creates a goods issue document.

Goods Issue is made against the reservation to facilitate:

- Control of issue and check that the correct material is being issued
- Accurate and real time records of all material issues and receipts for maintenance work

Since, the material is issued against the order, it makes data entry quicker, accurate and with relevant reference.

The quantity withdrawn is updated in the order as well as in the reservation. This reduces the reserved quantity.

For Unplanned materials, goods are issued against the order to capture the material and cost details in equipment history. After completion of work, excess or unused materials can be returned back to inventory.

The material issue transaction being handled through Transaction Code MIGO by Engineering Stores against material reservation / maintenance order.

# Pre-Closing Activities

# Actual Time Confirmation (Transaction Code: IW41 / IW42 / IW45)

This process will be used to record the actual activity and interval in the maintenance order. It will be used to identify:

- Who processed the operations specified in the order
- The time required for completing the operation, or if not completed, the remaining time required
- If all the materials specified in the order has been used, and if used, whether reservations have been cleared

After completion of work, the actual status is to be updated in the maintenance order to understand the difference between the plan and actual data in terms of manpower and material. Material issued will be automatically updated by the system, manpower detail is updated as in time required to complete the operation through the time confirmation.

The following information is documented:

- Time and date on which the operations were completed
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# The activity performed

# Remaining work

# Time utilized of the total time required for an operation

# Recording the Observation

In case, a notification is generated along with the maintenance order, following activities shall be performed in the notification.

1. Open the Notification (Transaction Code: IW22 / IW28)
2. Select the item code for failed part
3. Select the damage code
4. Select the cause code of the damage
5. Select the Task to be carried out to prevent such failure in future (if any)
6. Select the activities performed

The notification may further be completed after completing the outstanding tasks within the notification, if any.

# Create & Accept Service Entry Sheet (Transaction Code: ML81N)

Acceptance of external services is essential to document the work done by external Service Providers / Vendors so that payments can be made to them as per the Purchase Order.

A purchase requisition is generated for an external service when a maintenance order is generated that requires external services. This PR is converted to a PO by the purchase department. The PO contains the following details.

- The service specifications & quantity
- The expected time of delivery, price, etc.,

Purchase orders are issued to the external service providers / vendors specifying the nature of the work, time, cost etc. The contractor performs the work. A service entry sheet is created with reference to the purchase order and in which the service performed is entered. The values from the PO get defaulted into the service entry sheet. The work done by the contractor is checked and accepted by the maintenance engineer or by an authorized person. Invoice is sent by the vendor for the work done. Along with service acceptance, invoice verification is also done. The invoice is verified by the finance / accounting department against the service entry sheet and payment made if the values are correct.

# Technical Completion of Order (Transaction Code: IW32 / IW38)

After completion of maintenance order, the maintenance engineer or authorized person sets the status of the order to technically completed. Technical Completion will be used to ensure that further processing of the work order does not take place and all the unutilized resources which have been planned or reserved for the order are released.

After all the maintenance work is completed the Complete Technically button is clicked. After this the PM Order Status is changed from REL (Released) to TECO (Technically Complete) & Notification Status is set to be NOCO (Notification Completed). While this status is set, no further work can be carried out on the particular Notification / Order.

Page 89 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Once an Order is technically completed, outstanding purchase requisitions or material reservations are deleted or cleared. Notifications for the order is also completed. Only the following changes are allowed on an order:

- Lock and unlock the order
- Set the deletion flag

# Plan v/s Actual Cost in an Order

Cost is the value of consumption of stock / non-stock materials, actual work hours and so on, which are required to execute maintenance tasks. Costs are distinguished according to planned and actual costs.

Planned costs are calculated automatically by the system during order planning while actual costs for goods issues and goods receipts are calculated automatically by the system whilst the order is being executed. The actual costs for the work performed can only be calculated once the work has been confirmed.

We can display the costs resulting from an order from the Plant Maintenance perspectives in the system, this display is called the cost overview. The cost overview lists the individual value categories. A value category is a grouping of cost elements.

# Order Settlement (Transaction Code: KO88)

Order settlement is used to control costs and to identify where maximum costs are being incurred for maintenance. Costs associated with the maintenance work are assigned to Cost centers / internal order. Costs arising out of executing an order are initially collected in the order. These costs are then transferred to a receiver, for e.g., Cost Center. The receiver of costs is specified in the order and settlement carried out at regular intervals by finance / accounting department.

# Business Completion of Order (Transaction Code: IW32 / IW38)

Business completion of an order means ‘final completion of an order’. When an order has been fully executed and all the costs incurred in it are settled, then the status of the order can be changed to Business Completion (CLSD) and no further processing can be done on it. This ensures that no further postings of any kind are carried out on it. Business Completion of orders is performed when after all the work has been completed and all the costs settled.

Business Completion of an order is done after it has been:

- Technically completed
- Costs have been fully settled and the order balance is zero
- There are no open purchase orders for that specific maintenance order

When an order is given the status completed, then the system checks that settlement has been done and the order balance is zero and no outstanding purchase orders exist. No more postings can be done on it against the order. If for any reason the work has not been performed and the order is given the status CLSD then the system generates error message depending upon the error. For example, if the order is not settled (i.e., balance of cost is not zero) then the system gives error message ‘Order balance is not zero’ and the status of the order cannot be changed.
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Business Process Flow Diagram:

# Breakdown Maintenance

|Plant Maintenance|Plant Maintenance Materials Management|Finance|
|---|---|---|
|Create|Order Created|Notification|
|Manually|Release|Maintenance:|
|Costs Involved|Order Print|Purchase|
|Maintenance|Service|Request|
|Stock Available|Order to Room Print|Rejection|
|Order Closure| | |

# Business Process Transactional Steps

|Transactional Step Description|GUI Transaction Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Breakdown Notification|IW21|Report and Repair Malfunction (F2023)|
|Selection of Notification: Change / Put In Process|IW22 / IW28|Report and Repair Malfunction (F2023)|
|Create PM Order & Plan for Resources|IW31 / IW34|Report and Repair Malfunction|

Page 91 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Transactional Step Description|Code(s)|GUI & SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|PM Order Release|IW32 / IW38|Report and Repair Malfunction (F2023)|
|Create Purchase Order w.r.t Purchase Requisition|ME21N|Manage Purchase Orders (F0842A)|
|Goods Receipt (Non-Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Goods Issue (Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Create & Accept Service Entry Sheet w.r.t Purchase Order|ML81N|Manage Service Entry Sheets - Lean Services (F2027)|
|PM Order Operation Confirmation|IW41 / IW42|Report and Repair Malfunction (F2023)|
|PM Notification & Order Technical Completion|IW22 / IW32 / IW28 / IW38|Report and Repair Malfunction (F2023)|

# Key Policies and Process Changes associated with the Process

Use of Fiori Apps like Report Malfunction, Manage Malfunction Reports & Repair Malfunctions, facilitates User to easily report that a technical object has a malfunction, plan the required repair work, as well as document and confirm the maintenance work when it's done, in one single App.

Auto calculation of Breakdown duration based on the Malfunction Start Date / Time & Malfunction End Date / Time and thereby MTTR & MTBR calculation for each Equipment / Functional Location.

# Standard Reporting

Refer (Standard – GUI & FIORI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Master Data Considerations (including all relevant data relationships)

- Maintenance Work Center
- Functional Location
- Equipment
- Catalogs
- Material - Spare Parts
- Business Partner - Person Responsible

# Reporting (ABAP & BI / BO)

Refer (Customised – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

Page 92 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.8 Corrective-Maintenance process (BPML ID: 11.0.1)

# Business Process Description:

# Process Characteristics

Process Trigger: Abnormal Condition or Poor Performance of a machine or a system, which results in stoppage, which needs corrective attention.

Process Input: Functional Location / Equipment & Breakdown details

Process Output: Corrective -Maintenance Notification & Order

Process Owner: Production / Maintenance Department

Process Volumes: Approx. 5 Per Day

Process Frequencies: Daily

# As is:

Corrective maintenance comes under planned/unplanned maintenance where any breakdown immediately corrected by Maintenance and later on corrected for corrective actions on the scheduled weekends.

Corrective maintenance sometimes is reported by operations and Maintenance team attend the breakdown physically and capture the information in the log book, later they capture in the system.

Consumption of spares, consumables are entered in system without any relation to the work order.

Based on the Production information, the equipment breakdown is reported for remedial action. Equipment is attended by technician and cleared.
---
# Plant Maintenance Business Blueprint Document

After clearing the Corrective action down only, Information will be captured in 7i system with the detail info. about the classification of the breakdown and other details.

# As is Process flow diagram:

# Club Coffee As Connective Maint

|1|Stant Equipment Masters|Report for Mech/Elec|Spare|Perton|Preventive Work Order|
|---|---|---|---|---|---|
|1|Corrective assigned for action|Task Requirement|Action carried|Close completion| |
|1|Spares consumed|the Equipment| | | |

# To be Corrective Maintenance Process:

Corrective maintenance process flow will be same as the breakdown notification. Only difference here we will not put breakdown tick mark to capture the information.

# Execution process

Details explanation can be followed under BPML id:10.0.1 of this document. We can proceed with Maintenance activity type to map this process and reports can be reviewed against the same using N1 notification type.

# Business Process Flow Diagram:

Page 94 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Un-Planned Maintenance - BreakDown Corrective Order Typua

# Business Process Transactional Steps

|Transactional Step Description|Transactional Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Corrective Notification|IW21|Report and Repair Malfunction (F2023)|
|Selection of Notification: Change / Put In Process|IW22 / IW28|Report and Repair Malfunction (F2023)|
|Create PM Order & Plan for Resources|IW31 / IW34|Report and Repair Malfunction (F2023)|
|PM Order Release|IW32 / IW38|Report and Repair Malfunction (F2023)|
|Create Purchase Order w.r.t Purchase Requisition|ME21N|Manage Purchase Orders (F0842A)|
|Goods Receipt (Non-Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Goods Issue (Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Create & Accept Service Entry Sheet w.r.t Purchase Order|ML81N|Manage Service Entry Sheets - Lean Services (F2027)|
|PM Order Operation Confirmation|IW41 / IW42|Report and Repair Malfunction (F2023)|

Page 95 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Transactional Step Description|GUI Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|PM Notification & Order Technical Completion|IW22 / IW32 / IW28 / IW38|Report and Repair Malfunction (F2023)|

# Key Policies and Process Changes associated with the Process

Use of Fiori Apps like Report Malfunction, Manage Malfunction Reports & Repair Malfunctions, facilitates User to easily report that a technical object has a malfunction, plan the required repair work, as well as document and confirm the maintenance work when it's done, in one single App.

Auto calculation of Breakdown duration based on the Malfunction Start Date / Time & Malfunction End Date / Time and thereby MTTR & MTBR calculation for each Equipment / Functional Location.

# Standard Reporting

Refer (Standard – GUI & FIORI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Master Data Considerations (including all relevant data relationships)

- Maintenance Work Center
- Functional Location
- Equipment
- Catalogs
- Material - Spare Parts
- Business Partner - Person Responsible

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

Page 96 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.9 Spares Management-Maintenance process (BPML ID: 12.0.1)

# Business Process Description:

|Process Characteristics| |
|---|---|
|Process Trigger|Planned/unplanned maintenance, calibration, shutdown, Predictive|
|Process Input|Functional Location / Equipment & Breakdown details|
|Process Output|Reservation and Purchase requisition|
|Process Owner|Production / Maintenance Department|
|Process Volumes|Approx. 5 Per Day|
|Process Frequencies|Daily|

# As is:

Procurement of spares and consumables are categorized in terms of stock and non-stock item and any services can be placed to Contractor under Service Category. Whenever there is a critical component, we have 2 or 3 spares for machine maintenance. They have a threshold limit whenever it goes below, Procurement has to be initiated with approval for processing those critical items. PO will be created in 7i HxGN EAM for procurement, and maintenance dept will receive the spares from suppliers. Invoice sent by the supplier will have a reference of PO number and maintenance dept will confirm the receipt of the spares, post confirmation Finance will process for further payment. Maintenance manager, Planner and IT manager can raise Purchase order. List of spares needed will be circulate through PR and RFQ will be floated to different vendors. Based on commercials and other aspects PO will be placed to vendor for Procurement. Only approved vendors only will be required to supply spares for the maintenance. Procurement will happen for Breakdown maintenance for forklifts or for any machine maintenance. For Annual maintenance contract Separate PO will be issued to vendor say for ex. Chillers/Fork-lifts.

Page 97 of 110
---
# Plant Maintenance Business Blueprint Document

# As is Process flow diagram:

# Club Coffee

|1|Stan|PM Schedule|shut-schedule|
|---|---|---|---|
|1|CeneraterWark|Manual-|Nanma|
|1|Mech/|Elec Tech|Rejerence|
|1|Ptask|PM task|'ssienment|
|1|Physk1|'Vesificatony|Ciosure|
|1|PRYPO|Spares CCMumec|Diocuremeni|
|piccess|piccess|piccess|piccess|
|Anaisis|Anaisis|Anaisis|Anaisis|
|adherence|adherence|adherence|adherence|

# To be process flow

Spare parts management covers both BPML viz

1. Internal spares generation - BPMl 12.0.1
2. External Purchase requisition - BPML - 12.0.1

# Warranty of spares:

Warranty of equipment comes into picture when new equipment are brought. Most part of line expansion.

Mostly equipment which are new to the line will have a contract signed in the PO in which machine may be warranted for unwearable parts, say an example equipment which has the PLC card will be replaced in the same location as per the warranty terms.

Based on the PO, warranty will be tracked with the vendor for any replacement of spares manually.

Going forward in SAP Auto Message (Pop up) will appear for any item which is under warranty during breakdown.

# Consumption based planning:

Critical items will be identified as part of classification of Items in MM module. Based on consumption certain items will go through consumption-based planning.

Page 98 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

Consumption-based MRP procedures use past consumption data (historical data) to calculate future requirements using the material forecast or static MRP procedures.

Net requirements calculation is triggered when a stock level falls below a reorder point or by forecast requirements calculated from consumption data from the past.

In MRP under consumption based planning we have Auto reorder point plan, so that based on historical data, System will generate Automatic Purchase requisitions for the given Items.

Business can take action for those Purchase requisitions and convert into Purchase Order for Procurement.

# Business Process Flow Diagram:

To Be Material issue and transfer

|1|MzCTt Order|Azian AJFcres|mcquircd ncm Avlalc?|IZvc :ojrcs|
|---|---|---|---|---|
|1|Acccip: Dispjnz|7|Drwmhjut {Dje Pio-uncmcnt|YRF PRPC|
|1|Fost SeNicc Entn|1|Vcndcr Invo ccPotrg| |

# Business Process Transactional Steps

|Transactional Step Description|GUI Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Corrective Notification|IW21|Report and Repair Malfunction (F2023)|
|Selection of Notification: Change / Put In Process|IW22 / IW28|Report and Repair Malfunction (F2023)|
|Create PM Order & Plan for Resources|IW31 / IW34|Report and Repair Malfunction (F2023)|
|PM Order Release|IW32 / IW38|Report and Repair Malfunction (F2023)|
|Reservation no generation|IW32|Post release|
|Purchase Requisition|IW32|Purchase requisition generation|
|Create Purchase Order w.r.t Purchase Requisition|ME21N|Manage Purchase Orders (F0842A)|

Page 99 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Transactional Step Description|Transaction Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Goods Receipt (Non-Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Goods Issue (Stock Material)|MIGO|Post Goods Movement (MIGO)|
|Create & Accept Service Entry Sheet w.r.t Purchase Order|ML81N|Manage Service Entry Sheets - Lean Services (F2027)|
|PM Order Operation Confirmation|IW41 / IW42|Report and Repair Malfunction (F2023)|
|PM Notification & Order Technical Completion|IW22 / IW32 / IW28 / IW38|Report and Repair Malfunction (F2023)|

# Key Policies and Process Changes associated with the Process

NA

# Standard Reporting

NA

# Master Data Considerations (including all relevant data relationships)

- Maintenance Work Center
- Functional Location
- Equipment
- Catalogs
- Material - Spare Parts
- Business Partner - Person Responsible

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

Page 100 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|Workflow Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|
|6.10 Asset Disposal process (BPML ID: 13.0.1)|6.10 Asset Disposal process (BPML ID: 13.0.1)|6.10 Asset Disposal process (BPML ID: 13.0.1)|6.10 Asset Disposal process (BPML ID: 13.0.1)|
|Business Process Description:|Business Process Description:|Business Process Description:|Business Process Description:|
|Process Characteristics|Process Trigger|Process Input|Process Output|
|Process Owner|Process Volumes|Process Frequencies| |
|Production / Maintenance Department|1 per Quarterly|Daily| |
|As is:|As is:|As is:|As is:|
|Equipment served for the company, and it has to be disposed off considering the unhealthy condition of the equipment.|Equipment served for the company, and it has to be disposed off considering the unhealthy condition of the equipment.|Equipment served for the company, and it has to be disposed off considering the unhealthy condition of the equipment.|Equipment served for the company, and it has to be disposed off considering the unhealthy condition of the equipment.|
|We have 2 scenarios of equipment disposal where, equipment which has zero book value will be processed for sale by the company or through any 3rd party.|We have 2 scenarios of equipment disposal where, equipment which has zero book value will be processed for sale by the company or through any 3rd party.|We have 2 scenarios of equipment disposal where, equipment which has zero book value will be processed for sale by the company or through any 3rd party.|We have 2 scenarios of equipment disposal where, equipment which has zero book value will be processed for sale by the company or through any 3rd party.|
|Sale value will be captured through finance, and it will be tracked.|Sale value will be captured through finance, and it will be tracked.|Sale value will be captured through finance, and it will be tracked.|Sale value will be captured through finance, and it will be tracked.|
|Equipment which has some book value will also undergo same process like zero book value and will go the sale process as above.|Equipment which has some book value will also undergo same process like zero book value and will go the sale process as above.|Equipment which has some book value will also undergo same process like zero book value and will go the sale process as above.|Equipment which has some book value will also undergo same process like zero book value and will go the sale process as above.|
|In some cases, without capex, machineries will be dismantled within Maintenance Budget and put in Warehouse.|In some cases, without capex, machineries will be dismantled within Maintenance Budget and put in Warehouse.|In some cases, without capex, machineries will be dismantled within Maintenance Budget and put in Warehouse.|In some cases, without capex, machineries will be dismantled within Maintenance Budget and put in Warehouse.|
|As is Process flow diagram:|As is Process flow diagram:|As is Process flow diagram:|As is Process flow diagram:|
|Club Coffee Asset-Disposal process|Club Coffee Asset-Disposal process|Club Coffee Asset-Disposal process|Club Coffee Asset-Disposal process|
|1|Aset-Disposal|Book Value: 0|Initiate Scrap|
|Perform Sale|Aset Disposed Revenue|Finance| |
|Page 101 of 110|Page 101 of 110|Page 101 of 110|Page 101 of 110|
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# To be process flow:

In SAP Plant Maintenance, we can create a Separate Notification type to track the entire tracking of Asset disposal process. Asset identified and it will be process through multiple approvals and will created as equipment to be disposed through a notification. Once notified, Notification will be released for approval. Notification multiple user status will be set based on the requirement one level or 2 level. Once approved for disposal and user acceptance, Mail will be triggered to the respective department as a process. Equipment once disposed will go through sale or scrap process as per business decision. Asset will be finally removed from the system as a process. All Maintenance plan for the disposed asset will be removed completely and Deactivated.

Same N1 notification type used for asset disposal based on maintenance activity type reports can be generated.

# Business Process Flow Diagram:

|1|Start| | | |
|---|---|---|---|---|
|2|Receive|Equipment list|Notification| |
|3|Request|Sale Process|Disposal Triggered| |
|1|Prepare|Approval Request|Communicate| |
|1|Write off|Notification completed|Revenue|Asset Removal|
|3|Scrapping Process|Disposed|Equipment Asset report update| |

Page 102 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Business Process Transactional Steps:

|Transactional Step Description|Transactional Code(s)|GUI / SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Disposal Notification|IW21|Report and Repair Malfunction (F2023)|
|Selection of Notification: Change / Put In Process|IW22 / IW28|Report and Repair Malfunction (F2023)|
|Notification - Release|IW32 / IW38|Report and Repair Malfunction (F2023)|
|Notification-status -APP1|IW22|User status approval 1|
|Notification status -APP2|IW22|User status approval 2|
|Notification status -closure|IW22|Post Goods Movement (MIGO)|
|PM Notification Technical Completion|IW22 / IW28|Report and Repair Malfunction (F2023)|
|Equipment deactivation|IE02|Post notification closure.|

# Key Policies and Process Changes associated with the Process

NA

# Standard Reporting

NA

# Master Data Considerations (including all relevant data relationships)

- Maintenance Work Center
- Functional Location
- Equipment
- Catalogs

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

Page 103 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 6.11 Refurbishment process (BPML ID: 14.0.1)

# Business Process Description:

|Process Characteristics| |
|---|---|
|Process Trigger|Breakdown /Obsolete - spare for repair|
|Process Input|Functional Location / Equipment & Breakdown details|
|Process Output|Order / Purchase requisition.|
|Process Owner|Production / Maintenance Department|
|Process Volumes|2 per Monthly|
|Process Frequencies|Daily|

# As is:

Repairing of high value faulty spares of an equipment is of economic importance for companies and is a core process in Maintenance Processing. Refurbishment is much more cost effective than a new purchase. Equipment served for the company, and it has to be disposed of considering the unhealthy condition of the equipment. Club Coffee processes both internal and external refurbishment processes for processing the repair item. Repair items are handled by internal labour or external labour through Purchase order as a process. Tracking of these items is manual as per the existing system.

# As is Process flow diagram:

Page 104 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Process Flow

This scenario is of particular interest to scenarios where spares is vital, and availability plays a crucial role.

Refurbishment orders are created for defective repairable spares. These refer to:

- Individual repairable spares (pieces of equipment)
- Non-individual repairable spares (material)

The refurbishment order can be used to plan and execute the transition of the repairable spare from its initial defective condition to a new target condition.

Each of these orders can refer to one or more repairable spares that have to be refurbished from the same initial condition to the same final condition.

Spare part has different valuation types to represent different values. Because it is also a high value spare part or critical part, this spare part is serial-number managed.

Serial numbers can be assigned to the procured material.

While receiving the material with serial number, equipment will be created automatically in back end for the respective material with serial number.

These repairable spare parts can be identified with different cost assignments & valuation types like:

- New (C1)
- Repaired or Refurbished (C2)
- Damaged (C3)

# Business Process Flow Diagram:

Page 105 of 110
---
# Club Coffee

# Business Process Transactional Steps:

|Transactional Step Description|Transactional Code(s)|SAP APP Name (Fiori / Web Dynpro / Classic) & APP ID|
|---|---|---|
|Create Refurbhishment Order|IW81|Order Generation|
|Goods Movement|MIGO|Goods issue|
|Maintenance order confirmation|IW41|Order confirmation|
|Goods-Receipt|MIGO|Goods Receipt|
|Maintenance order-closure|IW32|Order close|
|Order-Settlement|IW32|Order closure|

# Key Policies and Process Changes associated with the Process

NA

# Standard Reporting

Page 106 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Master Data Considerations (including all relevant data relationships)

- Maintenance Work Center
- Functional Location
- Equipment
- Catalogs

# Reporting (ABAP & BI / BO)

Refer (Customized – GUI) Reports in Section 7 – Plant Maintenance Reports, of this document.

# Interfaces

|Description|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Enhancements (Including Mobile)

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Forms

|Description|Data Object|Object ID|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# Workflow

|Description|Data Object|Engaged Parties|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 7. Plant Maintenance Reports

Following Standard & Customised Reports would be available in S/4 Hana Plant Maintenance Module:

Page 107 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# SAP GUI Transaction   Description of Report

# Code / App ID

|Management of Technical Objects:| |
|---|---|
|IH08|Display Equipment|
|IE07|Equipment List (Multilevel)|
|IH04|Equipment Structural Display|
|IN19|Display Equipment Object Network|
|IH06|Display Functional Location|
|IL07|Functional Location List (Multilevel)|
|IH01|Functional Location Structural Display|
|IH09|Display Material|
|IK07|Display Measuring Points|
|IK17|Display Measurement Documents|
|S_ALR_87013421|Display Measurement Reading Entry List|
|IK51|Measurement Reading Transfer: Structural Display|
|IK52|Display Measurement Reading Transfer (History)|
|CR05|Work Center List Display|
|Maintenance Processing:| |
|IW29|Display Notifications|
|IW30|Notification List (Multilevel)|
|IW67|Display Tasks|
|IW69|Display Notification Items|
|IW68|Change Notification Items|
|IW65|Display Activities|
|IW39|Display Orders|
|IW40|Display Orders (Multilevel)|
|IW49|Display Operations|
|S_ALR_87013431|Confirmation Using Operation List|
|S_ALR_87013432|Display Confirmations|
|S_ALR_87013434|Material Where-Used List|
|IW13|Material Where Used List|
|IWBK|Material Availability|
|IP16|Display Maintenance Plan|
|IP18|Display Maintenance Item|
|IP30|Deadline Monitoring for Maintenance Plan|
|IP19|Graphical Scheduling Overview|
|IP24|Maintenance Scheduling Overview|
|S_ALR_87013426|Maintenance Plan Costing|
|IP14|Where-Used List by Strategy|
|S_ALR_87013428|Package Sequence Strategy|
|S_ALR_87013429|Display Document Flow|
|F2603|Maintenance Scheduling Board|
|F2227|Resource Scheduling for Maintenance Planners|
|F2828|Maintenance Planning Overview|
|F3326|Manage Schedules|

# Maintenance Task Lists:

|Report Type|(Standard - GUI / Customised - GUI / Standard - FIORI)|
|---|---|
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - GUI| |
|Standard - Fiori| |
|Standard - Fiori| |
|Standard - Fiori| |
|Standard - Fiori| |

Page 108 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

|SAP GUI Transaction Code / App ID|Description of Report|Report Type|
|---|---|---|
|IA09|Display Task Lists|Standard - GUI|
|IA10|Display Task Lists (Multilevel)|Standard - GUI|
|IA16|Cost Maintenance Task Lists|Standard - GUI|
|IA17|Print Maintenance Task Lists|Standard - GUI|
|IP62|Where-Used List for Material|Standard - GUI|
|IA21|Evaluate Change Documents for Maintenance Task Lists|Standard - GUI|

# Plant Maintenance Information System (PMIS):

|SAP GUI Transaction Code / App ID|Description of Report|Report Type|
|---|---|---|
|MCI1|PMIS: Object Class Analysis|Standard - GUI|
|MCI2|PMIS: Manufacturer Analysis|Standard - GUI|
|MCI3|PMIS: Location Analysis|Standard - GUI|
|MCI4|PMIS: Planner Group Analysis|Standard - GUI|
|MCI5|PMIS: Single Object - Damage Analysis|Standard - GUI|
|MCI6|PMIS: Object Statistics|Standard - GUI|
|MCI7|PMIS: Breakdown Analysis|Standard - GUI|
|MCI8|PMIS: Cost Analysis|Standard - GUI|
|MCJB|MTTR/MTBR Equipment|Standard - GUI|
|MCJC|MTTR/MTBR Functional Location|Standard - GUI|
|MMBE|Stock Overview|Standard - GUI|
|ZPM406|PM Dashboard|Customized - GUI|
|ZPM407|PM Breakdown Dashboard|Customized - GUI|
|ZPM500|PM Costing Report|Customized - GUI|
|ZPM002|Work Order Progress Report|Customized - GUI|
|F2222|Manage Work Center Utilization|Standard - Fiori|
|F3567|Actual Maintenance Cost Analysis|Standard - Fiori|
|F2812|Technical Object Breakdown Analysis|Standard - Fiori|
|F3075|Technical Object Damages|Standard - Fiori|

# 8. Plant Maintenance BI / BO Reports

Following BI / BO Reports would be available in S/4 Hana Plant Maintenance Module:

|Report|Description|
|---|---|
|Daily Maintenance Summary|Provides the breakdown hours, instances and cost incurred for the day, month and year across functional locations and equipments|
|Maintenance Overall Summary|Provides all the details regarding individual notifications such as equipment affected, type of problem, items affected, breakdown hours and cost.|

Page 109 of 110
---
# Club Coffee

# Plant Maintenance Business Blueprint Document

# Preventive Maintenance Summary

Provides the summary of maintenance tasks. It provides details as to the scheduled time for tasks and how many are completed / pending.

# 9. GAPS

Process
Scenario
Proposed Solution
# 10. Annexure

PM-completion formpdf KDS SAHANA Club Coffee_PM_vL.O_DRAF spare

Page 110 of 110