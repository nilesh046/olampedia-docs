# Olam ME55 – VN_COV_PR_RELEASE_TAB_MISSING

Prepared: Sharmila J

Reviewed: Sathish S

Category: Article

# DOCUMENT IDENTIFICATION

|Version|Status|Date (DD-MM-YYYY)|
|---|---|---|
|1.0|Initial draft|11-12-2019|
|2.0| | |

Page 1 of 4
---
# ME55 – VN_COV_PR_RELEASE_TAB_MISSING

# Global SAP Support

# Date (DD-MM-YYYY)

# Problem description

COV business User try to release Purchase Requisition collectively using the transaction ME55. User face difficulty can’t able to release. When user check a single PR, identifies that Release Strategy Tab is not in PR Item level.

# Reproducing the Issue

# PR Creation Via MRP:

1. Use transaction MD02 to run MRP for Spares material in COV.
2. Run the transaction MD04 for material “400000224925“ and plant “9331“.
3. You will get PR details.
4. Check PR in ME53N transaction.

# ME53N:

1. Enter Transaction code: ME53N
2. Check the PR release strategy tab at PR item level.
3. Notice that PR Document type is created with NB Purchase Requisition -> Standard PR document type.

Page 2 of 4
---
# ME55 – VN_COV_PR_RELEASE_TAB_MISSING

Display PurchaseReq: 1001755813

# Document Overview

On ersonal Setting

# NB Purchase Requisiti_ 1001755313

# Texts

# Additional Data

# Header note

# Continuous-t_

# Default Values

|Item|Material|Short Text|Quantity|Unit|Delivery Date|Crcy|Matl Group|Plant|Stor: Loc_|PGr Requisnr.|Val: Price|Tracking Vendor|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1400000224,_|RAPID 5000/080 30|7703,|100|000|01.08.2018|VND|7024|9331|V04 Spares|100,000| | |
|Item|1 [ 10|400000224925|RAPID 5000/080 30| | | | | | | | | |

# Release Strategy Tab?

# Material Data

# Quantities

# Dates

# Valuation

# Source of Suppl

# Status

# Contact

# erson

# Texts

# Delivery Address

# Customer Data

Created by Spares

Changed on 20.09.2018

CreaInd_ Material requirements plann.

Requisitioner Spares

Tracking Number

Purch. Group V04 COV Engineering

Telephone 72 3655999

# Cause

As per our GT process, PR document type – ZR01 Fixed Purchase Req.

MRP Group is not maintained with Z000 - Default PR Doc. Type ZR01 in MRP1 View for Material master will trigger NB Purchase Req.

Page 3 of 4
---
# ME55 – VN_COV_PR_RELEASE_TAB_MISSING

# Display Material 400000224925 (Spare Parts)

# Additional Data Org. Levels

| | | | | |MRP Group (3)|3 Entries found|
|---|---|---|---|---|---|---|
|Purchase order text|MRP|MRP|MRP|Plant data|Restrictions| |
|Material|400000224925|RAPID 5000/080|30|77035754| | |
|Plant|9331|CafeOutspan Vietnam Ltd Planti| |Plant: 9331| | |

# General Data

|Base Unit of Measure|each|
|---|---|
|MRP group|Zooo|
|Purchasing Group|V04|
|ABC Indicator|ZO0i|
|Prod Issu SLOc based on Prodn Version|Z002|
|Prod SLoc -Material Prodn Version| |

# Plant-sp.matl status

Valid from
# Resolution

1. Kindly request MDM team (mdm@olamnet.com) to change Z000 - Default PR Doc. Type ZR01 from blank in MRP group field in MRP1 View.

# Key Notes

This article is origin specific, it will applicable only to Cafe outspan Vietnam.

Page 4 of 4