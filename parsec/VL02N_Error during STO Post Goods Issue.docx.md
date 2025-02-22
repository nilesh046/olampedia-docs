# Olam VL02N – Error during STO Delivery

# Picking

Prepared: Karthik R

Reviewed: Sathish S

Category: Article

# DOCUMENT IDENTIFICATION

|Version|Status|Date (DD-MM-YYYY)|
|---|---|---|
|1.0|Initial draft|12-12-2019|

Global SAP Support

Date (DD-MM-YYYY)

Page 1 of 4
---
# VL02N – Error during STO Delivery

# Picking

# Problem description

In transaction VL02N, if error displays as “Only 0 CAR of material 1XXXXXXXXXXX available“ users cannot able to post the goods issue and create a material document.

# Case 1:

# Reproducing the Issue

Delivery – Post goods issue:

1. Enter Transaction code: VL02N
2. When we click on Post Goods Issue tab, System will throw this Only 0 CAR of material 100000031368 available error and not allow you to post this document.

|Outbound delN.|8130218695|
|---|---|
|Document Date|11.12.2019|
|Ship-to party|GH2997|
| |GH2997 Ghana|

# Item Overview

|Picking|Loading|Trnspom|Status Overview|Goods Movement Data|
|---|---|---|---|---|
|Planned GI|11.12.2019|0O:0|Total Weight|522 573|
|Accual GI date|0o:00|No.of packages| | |

# All Items

|ICM|Material|Delv. Qty|Description|ICa|Batch|
|---|---|---|---|---|---|
|100000Q1EZ| |CAR TP TT 70g*50 SACHET|MLN| | |
|100000031368| |CAR TP TT 1.1KG x 12 Enriched SUP|MLAT| | |
|100000019283| |CAR TP TL 2106*24 EQENRICHED|MIN| | |
|100|Performance Assistant| |MIN| | |
|100| | |NLN| | |

Only 0 CAR of material 100000031368 available

Page 2 of 4
---
# VL02N – Error during STO Delivery

# Picking

# Cause

The above error message is due to stock reserved for any open delivery/reservation/sales order.

# Resolution

Go to MD04 transaction and check whether any open delivery or order available for this material and plant as shown below. Close the open delivery or sales order available and proceed with the Post goods issue for the STO delivery.

# Stock/Requirements List as of 20:16hrs

|Materia|Plant|MRP type|Material Type|FERI|Unit|CAR|
|---|---|---|---|---|---|---|
|100000031363|2997| | | | | |

|Date|MRP|MRP element data|Rescheduling|Receipt Regmt|Available Qty|Stc .. Pr.. Su:. Iss ..St ..| |
|---|---|---|---|---|---|---|---|
|12.12.2019|Stock| | | |14,014.140| | |
|31.07.2019|CusOrd|2430137627/000030/0_| | | |Fe02| |
|26.09.2019|CusOrd|2430141243/000010/0_| | |730-|FE02| |
|26.09.2019|CusOrd|2430141243/000020/0_| | | |Fe02| |
|25.10.2019|CusOrd|2430143250/00oo50/0_| | | |FE02| |
|13.11.2019|CusOrd|2430144459/000020/0_| | | | | |
|18.11.2019|CusOrd|2430144737/00oo2o/0_| | |15 _|Fe02| |
|27.11.2019|CusOrd|2430145430/000020/0_| | |15 _-| | |
|11.2019|CusOrd|2430145513/00oo60/0_| | |45 -|FC02| |
|01.12.2019|PldOrd|0000701354/SICK| |758|23,772.140|Q001| |
|12.2019|IndReq|VSF| |51,200-|27,427.860-| | |
|04.12.2019|PrcOrd|001000455403/ZiOi/Bd|01.12.2019|10|20,691|6,736.860-|Q001|
|10.12.2019|POitem|1400029811/00003|01.12.2019|10|300|5,936.860_|2997 FG02 FGsS|
|10.12.2019|CusOrd|2430146247/0000s0/0_| | | |FG04| |
|10.12.2019|CusOrd|2430146296/000030/0_| | | |VO15| |

# Key Notes

Page 3 of 4
---
# VL02N – Error during STO Delivery

# Picking

This article is not origin specific, it will applicable to all global origins in Olam.

Page 4 of 4