# Olam ME21N/ME22N_UOM CHANGE IN PO

Prepared: Navya S

Reviewed: Gunasekar K

Category: Article

# DOCUMENT IDENTIFICATION

|Version|Status|Date (DD-MM-YYYY)|
|---|---|---|
|1.0|Initial draft|12-12-2019|
|2.0|Final|13-12-2019|

Global SAP Support

Date (DD-MM-YYYY)

Page 1 of 7
---
# ME21N/ME22N_UOM CHANGE IN PO

# Problem description

In transaction ME21N/ME22N, when user tries to change the order unit to a different UOM, it does not get changed and it shows the same UOM

# Case 1:

# Reproducing the Issue

# PO Creation:

1. Enter transaction code ME21N
2. Choose PO Document type: Z001, Vendor, Purch. Org, Pur. Grp in PO Header Level.
3. Enter Material code “100000011486“, PO Quantity, Price and plant in PO item level.
4. The order unit picked is KG, user tries to change it to MT

# Create Purchase Order

|Document Overview Off|Hold|Messages|Personal Setting|
|---|---|---|---|
|No|ZO01|Fied Purchase|Vendor|
|2055576|1999 DESIGN AGENCY|Doc: date|12.12.2019|
|variant|Header|ShortText| |
|Matl Group|Stor. Location| | |
|Item|1 [ 1 ]|100000011486|Cashew Shelled Wholes|
|Quantity|100|Delv. Date|12.12.2019|
|Net Price|Curr: Per|Pint| |
|100QQQQ1143€|Cashew Shelled Wholes|100|12.12.2019|

# Hierarchy

Quantity
Net
28,454.00 KZX

# Pricing Elements

|CnTy Name|Amount|U.Condition value|Curr. Status|Num::|OUn|CCon:|Condition value|CdCur|
|---|---|---|---|---|---|---|---|---|
|EBXX Gross Price|284.54|28,454.00KZM| | | | | | |
|Net value incl: disc|284.54|28,454.00KZY| | | | | | |
|NAV Non-Deductible Tax|0.00|0.00KZY| | | | | | |
|Net value incl: tax|284.54|1KG|28,454.00KZY| | | | | |
|SKTC Cash Discount|0.00|0.00KZX| | | | | | |
|Actuaprice|284.54|28,454.00KZM| | | | | | |
|MOTB OTB Procurement|284.54|1KG|28,454.00KZY| | | | | |

# Condition rec_

# Analysis

# Update

Page 2 of 7
---
# ME21N/ME22N_UOM CHANGE IN PO

# Create Purchase Order

Document Overview
Off
Hold
Print Preview
Messages
Personal Setting
No
ZO01 Fied Purchase
Vendor
2055576
1999 DESIGN AGENCY
Doc. date
12.12.2019
|variant|Header| | | | | | | | | | | | |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|defined|Itm|Material|Short Text|Quantity|O0MT|Deliv. Date|Net Price|Curr:|Per|Matl Group|Plnt|Stor. Location| |
| | |10000001143|Cashew Shelled Wholes| |100| |22.12.2019|234.54|KZK| |0903|4410|KZX|

# Hierarchy

Item
1 [ 1]
100000011486
Cashew Shelled Wholes
# Material Data

|Quantities|Weights|Additional Data|Delivery Schedule|Delivery|Invoice|Conditions|Texts|Delivery Address|Confirmations|
|---|---|---|---|---|---|---|---|---|---|
|Quantity|100|Net|28,454|KZY| | | | | |

# Pricing Elements

|N: CnTy Name|Amount per U.|Condition value|Curr.|Status|Nun::.|OUn|CCon:|Condition value|CdCur|S..|
|---|---|---|---|---|---|---|---|---|---|---|
|PBXX Gross Price|284.54|28,454|KZK| | | | | | | |
|Net value incl: disc|234.54|1KG|28,454.00|KZM| | | | | | |
|NAV Non-Deductible Tax|0.00|0.00|XZK| | | | | | | |
|Net value incl|234.54|28,454.00|KZY| | | | | | | |
|SKTO Cash Discount|0.000|0.00|KZX| | | | | | | |
|Actual price|284.54|1KG|28,454.00|KZY| | | | | | |
|MOTB OTB Procurement|284.54|28,454.00|KZM| | | | | | | |

# Condition rec

Analysis
Update
No messages issued during check

SAP

SAPLMEGUI

olameccgrq INS

When he changes it to MT and clicks on enter, it shows KG itself

Page 3 of 7
---
# ME21N/ME22N_UOM CHANGE IN PO

# Cause

The order unit whichever user is trying to change is not maintained in Inforecord - General data view or In Material master Purchasing view.

# Resolution

User has to contact MDM TEAM to maintain the order unit in Inforecord and in Material master data.

Page 4 of 7
---
# ME21N/ME22N_UOM CHANGE IN PO

# Display Info Record: General Data

|Purch: Org:|Data|Conditions|Texts|
|---|---|---|---|
|Info Record|5300345057|Vendor|2055578|
| | |1999 DESIGN AGENCY LDA| |
|Material|10000001148d|Cashew Shelled Wholes| |
|Material Group|0903|Cashew Pieces| |

# Vendor Data

|1st Rem: Exped_|Daya|
|---|---|
|Znd RemExped_|Day3|
|3rd Rem /Exped_|Daya|
|Vendor Mat: No_| |
|Vendor Subrange| |
|VSR Sort No_| |
|Vendor Mat: Grp| |
|Manufacturer| |
|Points|0.00Q|
|Salesperson| |
|Telephone| |
|Return Agmt| |
|Prior Vendor| |
|Regular Vendor| |

# Purchase Order Unit of Measure

|Order Unit|Conversion|Var. Order Unit|
|---|---|---|
| |00o|Not active|
---
# ME21N/ME22N_UOM CHANGE IN PO

Once maintained, user will be able to save the PO with MT as the order unit

Page 6 of 7
---
# ME21N/ME22N_UOM CHANGE IN PO

Fixed Purchase 5900012435 Created by Navya $

Document Overview Off Print Preview Messages Personal Setting

|No|ZO01 Fied Purchase|900012435|Vendor|2055576|999 DESIGN AGENCY|Doc. date|12.12.2019| |
|---|---|---|---|---|---|---|---|---|
|variant|Header|Short Text|Deliv. Date|Net Price|Per|Matl Group|Plnt| |
|defined|Itm|Material|PO Quantity|Curr:| |Stor:|LoqL| |
| | |100QQQQ1148|Cashew Shelled Wholes|100.000MT|12.12.2019|28454KZY|0903|4410|

# Hierarchy

Item
1 [ 1 ]
100000011486
Cashew Shelled Wholes
# Material Data

|Quantities|Weights|Additional Data|Delivery Schedule|Delivery|Invoice|Conditions|Texts|Delivery Address|Confirmations|
|---|---|---|---|---|---|---|---|---|---|
|Quantity|100|Net|28,454.00|KZY| | | | | |

# Pricing Elements

|CnTy Name|Amount per|Condition value|Curr.|Status|Num::.|OUn|CCon:|Condition value|CdCur S..|
|---|---|---|---|---|---|---|---|---|---|
|EBXX Gross Price|284.54|28,454.00|KZK| |MT| | |0.00| |
|Net value incl: disc|234.54|23,454.00|KZM| |MT| | |0.00| |
|NAVK Non-Deductible Tax|0.00|0.00|KZX| | | | |0.00| |
|Net value incl: tax|284.54|28,454.00|KZM| |MT| | |0.00| |
|SKTO Cash Discount|0.00|0.00|XZX| | | | |0.00| |
|Actual price|284.54|28,454.00|KZM| |MT| | |0.00| |
|WOTB OTB Procurement|284.54|28,454.00|KZY|1|MT|1KG|0.00| | |

# Condition Rec:

Analysis Update

Fied Purchase 5900012435 changed

SAP SAPLMEGUI olameccgrq INS

Page 7 of 7