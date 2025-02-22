# Project: Key Data Structure

# Canada Club Coffee S4 Hana Implementation

# SAP GT- PM Key Data Structure

# Document details

|Document Category|Key Data Structure|
|---|---|
|Document title|PM Key Data Structure|
|Team|Plant Maintenance|
|Team Member(GT)|Saravana raja|
|Project Manager (GT)|Karthik LP|
|Project Head (GT)| |

# Document Versions

|Date|Version|Author|Status – Description|
|---|---|---|---|
|13/06/202|1.0|Sarvana raja|Initial Document|

OLAM/SAP/GT/PM/KDS Page 1 of 8 Version 1.0

# Key Data Structure
---
# Key Data Structure

# Project: Canada Club Coffee S4 Hana Implementation

# OLAM/SAP/GT/KDS/PM

# SAP GT- PM Key Data Structure

# TABLE OF CONTENTS

|1.0|INTRODUCTION|................................................................................................................3|
|---|---|---|
|2.0|KEY DATA STRUCTURES –ORGANIZATIONAL AND CONFIGURATION ELEMENTS|.......................................................................................................................................4|
|2.1|Maintenance Plant|...........................................................................................................4|
|2.1.1|Location|..................................................................................................................4|
|2.1.2|Maintenance Work centers|.................................................................................4|
|2.2|Maintenance Planing Plant|..............................................................................................5|
|2.2.1|Planner group|.....................................................................................................5|
|3.0|MASTER DATA RELATED SETTINGS|........................................................................6|
|3.1|Types of Technical objects|............................................................................................6|
|3.2|Plant Section|....................................................................................................................6|
|3.3|Equipment category|.........................................................................................................7|
|4.0|PROCESS RELATED SETTINGS|...................................................................................7|
|4.1|Sort field for maintenance plan|.......................................................................................7|
|4.2|Person responsible for work center|.................................................................................7|
|4.3|Notification types|.............................................................................................................7|
|4.4|Order types|.....................................................................................................................8|

OLAM/SAP/GT/PM/KDS Page 2 of 8 Version 1.0

# Key Data Structure
---
# Key Data Structure

# Project: Canada Club Coffee S4 Hana Implementation

# OLAM/SAP/GT/KDS/PM

# 1.0 Introduction

# Purpose of this Document

This document describes all Key Data Structures necessary for enabling various business processes and making them operational with requisite controls and business rules. This document will serve as reference document for system settings and configuration in Realization. This document lists out all KDS whether required to be defined newly or the SAP Standard ones which are identified for use in any of the process for Olam Global template. The list however excludes those SAP Standard KDS that are not identified for a specific use but may not be deleted from production client for technical or other pragmatic reasons.

# Intended Audience

This document is for internal project distribution. It is to be used to communicate to all team members the value list of Key Data Structures for Olam GT. It is the responsibility of all project team members to read the document and seek clarification from the respective Team Leads if they have any queries.

# Related Documents

This document should be read in conjunction with the following documents:

- Business Blue Print Documents for Olam GT

OLAM/SAP/GT/PM/KDS Page 3 of 8 Version 1.0
---
# Key Data Structure

# Project: Canada Club Coffee S4 Hana Implementation

# OLAM/SAP/GT/KDS/PM

# 2.0 Key Data Structures – Organizational and Configuration elements

# 2.1 Maintenance Plant

The maintenance plant of a technical object is the plant at which it is installed. The following Maintenance plants are to be defined:

|Maintenance Plant|Description|
|---|---|
|1990|55 Carrier Dr & 65 Carrier Dr|
|1991|101 Claireville|
|1992|160 Claireville|

# 2.1.1 Location

A place in a maintenance plant at which a technical object is physically located. The following Locations are to be defined:

|Location|Description|
|---|---|
|0010/ RST|Roasting|
|0020/GND|Grinding|
|0030/BAR|Blend After Roast|
|0040/FLV|Flavour|
|0050/PCK|Packing|

# 2.1.2 Maintenance Work centers

The main workcenter usually represents one person or a department, responsible for ensuring that the maintenance Work in order is executed by the work center performing the individual operations. The following maintenance work centers are to be defined:

|Maintenance Work centers|Description|
|---|---|
|Mech|Mechanical|
|INS|Instrument|
|Elec|Electrical|
|UTL|Utility|

# OLAM/SAP/GT/PM/KDS

Page 4 of 8

Version 1.0
---
# Key Data Structure

Project: Canada Club Coffee S4 Hana Implementation

# 2.2 Maintenance Planning Plant

The maintenance planning plant of a technical object is the plant in which the maintenance tasks for the object are planned and prepared. Maintenance planner groups work at the maintenance planning plant to plan and prepare the maintenance tasks for the plants that are assigned to the maintenance planning plant. The following activities are performed at the maintenance planning plant:

- Definition of task lists
- Material planning based on bills of material in task lists and orders
- Management and scheduling of maintenance plans
- Creation of maintenance notifications

# Manufacturing Facilities

|Plan|Planning Plant|SAP Description|Company Code|
|---|---|---|---|
|1990|1990|55 Carrier Dr & 65 Carrier Dr|CA13|
|1991|1991|101 Claireville|CA13|
|1992|1992|160 Claireville|CA13|

# 2.2.1 Planner group

A group of employees responsible for planning and processing maintenance tasks in a plant

|Maintenance Planner group|Description|
|---|---|
|P1|Mechanical Planner|
|P2|Electrical Planner|
|P3|Civil Planner|

OLAM/SAP/GT/PM/KDS Page 5 of 8 Version 1.0
---
# Key Data Structure

# Project: Canada Club Coffee S4 Hana Implementation

# OLAM/SAP/GT/KDS/PM

# 3.0 Master data Related Settings

# 3.1 Types of Technical objects

A division of a technical object for precise description

Example

Category of technical object: "Fleet objects"

Type of technical object: "Heavy goods vehicle," "Automobile," "Fork-lift truck"

|Technical Object|Description|
|---|---|
|AHU|Air Handling Unit|
|AC|AIR CONDITIONER|
|BATTERY|BATTERY|
|BEARING|Bearings|
|BLENDER|Blender|
|CB|CIRCUIT BREAKER|

# 3.2 Plant Section

A division of maintenance plants into production areas.

Machines or sets of machines that are represented in the system as pieces of equipment or functional locations are installed in plant sections.

|Plant section|Person responsible|
|---|---|
|P01|Plant Sect1|
|P02|Plant Sec 2|
|P03|Plant Sec-3|

OLAM/SAP/GT/PM/KDS Page 6 of 8 Version 1.0

# Key Data Structure
---
# Key Data Structure

# Project: Canada Club Coffee S4 Hana Implementation

# SAP GT- PM Key Data Structure

# 3.3 Equipment category

An indicator used to differentiate pieces of equipment according to usage

|Category|Reference|Description|
|---|---|---|
|E|Electrical|Machines|
|M|Machines|Machines|
|F|Machines|Fleet|
|Q|Machines|Test/measurement equipment|
|U|Machines|Utility|

# 4.0 Process related settings

# 4.1 Sort field for maintenance plan

The sort field in the maintenance plan, which facilitates the selection and grouping of maintenance plans.

|Maintenance plan sort field|Description|
|---|---|
|CP|Calibration|
|PM|Plant Maintenance|

# 4.2 Person responsible for work center

The person or the group of people responsible for maintaining the master data of a particular work center.

|Plant|Person responsible|Description|
|---|---|---|
|1990|HDM|HOD -Mechanical|
|1990|HDE|HOD-Electrical|
|1991|HDM|HOD-Mechanical|
|1991|HDE|HOD-Mechanical|
|1992|HDM|HOD_Mechanical|
|1992|HDE|HOD-Electrical|

OLAM/SAP/GT/PM/KDS Page 7 of 8 Version 1.0 Key Data Structure
---
# Key Data Structure

# Project: Canada Club Coffee S4 Hana Implementation

# OLAM/SAP/GT/PM

# 4.3 Notification types

Notification type references a notification category and an origin. Notifications have the category predefined on the basis of the origin.

|Notification type|Description|
|---|---|
|N1|GT-Maintenance Reqst|
|N2|GT-Malfunction Rept.|
|N3|GT-Activity Report|
|N4|GT-Predictive Maint.|
|N5|Safety Notiifcation|

# 4.4 Order types

Orders form part of the detailed planning of tasks and their accompanying documentation in Plant Maintenance. A technician on site must execute tasks at a technical object. For this, materials, utilities and staff must be planned and costs estimated. The order supports you with these tasks, since it primarily contains data for planning and executing tasks, which must be performed at the technical object.

|Order type|Description|
|---|---|
|ZM01|Preventive-Maintenance|
|ZM02|Breakdown Maintenance|
|ZM03|Shutdown Maintenance|
|ZM04|Refurbishment Maintenance|
|ZM05|Calibration Maintenance|

OLAM/SAP/GT/PM/KDS Page 8 of 8 Version 1.0