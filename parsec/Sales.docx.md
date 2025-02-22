# Olam

# Sales & Distribution Business Blueprint

Prepared by: Rahul Bhosale

# PROJECT IDENTIFICATION

Project Name: Brazil Soluble Coffee

Project Manager: Balaji Balaraman

Business Process Owner

# DOCUMENT IDENTIFICATION

|Version|Status|Date (DD-MMM-YYYY)|
|---|---|---|
|1.0|Version 1|01-Oct-2022|

# REVISION HISTORY

|Version|Change Made|Changed By|Date|
|---|---|---|---|
| | | | |

# SIGN OFF AND APPROVAL

|Name|Date (DD-MMM-YYYY)|
|---|---|
|Business Process Owner| |

Page 1 of 33
---
# Sales & Distribution Business Blueprint

# TABLE OF CONTENT

1. PROJECT PROFILE.........................................................................................................................6
2. KEY DATA STRUCTURE................................................................................................................6
3. SCENARIO VALIDATION.............................................................................................................. 6
4. DOMESTIC SALES (START WITH CONTRACT) – BPML ID 1.01
1. PROCESS DESCRIPTION..........................................................................................7
2. PROCESS STEP DETAILED REQUIREMENTS & SOLUTION........................................7
3. KEY POLICIES AND PROCESS CHANGES ASSOCIATED WITH THE PROCESS.............8
4. STANDARD REPORTING – REFER THE COMMON REPORT........................................8
5. MASTER DATA CONSIDERATIONS (INCLUDING ALL RELEVANT DATA
RELATIONSHIPS)........................................................................................................8
6. REPORTING ABAP & BW............................................................................................8
7. INTERFACES................................................................................................................9
8. ENHANCEMENTS.......................................................................................................9
9. FORMS.......................................................................................................................9
10. WORKFLOW................................................................................................................9
5. DOMESTIC SALES -START WITH SALES ORDER – BPML ID 1.02...........................10

Page 2 of 33
---
# Sales & Distribution Business Blueprint

# 5. PROCESS DESCRIPTION

# 5.1 PROCESS STEP DETAILED REQUIREMENTS & SOLUTION

# 5.2 KEY POLICIES AND PROCESS CHANGES ASSOCIATED WITH THE PROCESS

# 5.3 STANDARD REPORTING – REFER THE COMMON REPORT

# 5.4 MASTER DATA CONSIDERATIONS (INCLUDING ALL RELEVANT DATA RELATIONSHIPS)

# 5.5 REPORTING ABAP & BW

# 5.6 INTERFACES

# 5.7 ENHANCEMENTS

# 5.8 FORMS

# 5.9 WORKFLOW

# 6. EXPORT SALES– BPML ID 1.03

# 6.1 PROCESS DESCRIPTION

# 6.2 PROCESS STEP DETAILED REQUIREMENTS & SOLUTION

# 6.3 KEY POLICIES AND PROCESS CHANGES ASSOCIATED WITH THE PROCESS

Page 3 of 33
---
# Sales & Distribution Business Blueprint

# 6.4 STANDARD REPORTING – REFER THE COMMON REPORT

14

# 6.5 MASTER DATA CONSIDERATIONS (INCLUDING ALL RELEVANT DATA RELATIONSHIPS)

14

# 6.6 REPORTING ABAP & BW

14

# 6.7 INTERFACES

15

# 6.8 ENHANCEMENTS

15

# 6.9 FORMS

15

# 6.10 WORKFLOW

15

# 7 INTERCOMPANY SALES (TO OIL)– BPML ID 1.10

16

# 7.1 PROCESS DESCRIPTION

16

# 7.2 PROCESS STEP DETAILED REQUIREMENTS & SOLUTION

16

# 7.3 KEY POLICIES AND PROCESS CHANGES ASSOCIATED WITH THE PROCESS

17

# 7.4 STANDARD REPORTING – REFER THE COMMON REPORT

17

# 7.5 MASTER DATA CONSIDERATIONS (INCLUDING ALL RELEVANT DATA RELATIONSHIPS)

17

# 7.6 REPORTING ABAP & BW

17

Page 4 of 33
---
# Sales & Distribution Business Blueprint

# 7.7 INTERFACES

18

# 7.8 ENHANCEMENTS

18

# 7.9 FORMS

18

# 7.10 WORKFLOW

18

# 8 SAMPLE SALES PROCESS – BPML ID 1.06

19

# 8.1 PROCESS DESCRIPTION

19

# 8.2 PROCESS STEP DETAILED REQUIREMENTS & SOLUTION

19

# 8.3 KEY POLICIES AND PROCESS CHANGES ASSOCIATED WITH THE PROCESS

19

# 8.4 STANDARD REPORTING – REFER THE COMMON REPORT

19

# 8.5 MASTER DATA CONSIDERATIONS (INCLUDING ALL RELEVANT DATA RELATIONSHIPS)

19

# 8.6 REPORTING ABAP & BW

20

# 8.7 INTERFACES

20

# 8.8 ENHANCEMENTS

20

# 8.9 FORMS

20

# 8.10 WORKFLOW

20

Page 5 of 33
---
# Sales & Distribution Business Blueprint

# 9. SALES RETURN ORDER PROCESS – BPML ID 1.17

# 9.1 PROCESS DESCRIPTION

21

# 9.2 PROCESS STEP DETAILED REQUIREMENTS & SOLUTION

21

# 9.3 KEY POLICIES AND PROCESS CHANGES ASSOCIATED WITH THE PROCESS

22

# 9.4 STANDARD REPORTING – REFER THE COMMON REPORT

22

# 9.5 MASTER DATA CONSIDERATIONS (INCLUDING ALL RELEVANT DATA RELATIONSHIPS)

22

# 9.6 REPORTING ABAP & BW

22

# 9.7 INTERFACES

22

# 9.8 ENHANCEMENTS

22

# 9.9 FORMS

23

# 9.10 WORKFLOW

23

# 10. DEBIT MEMO / CREDIT MEMO PROCESS – BPML ID 1.18

# 10.1 PROCESS DESCRIPTION

24

# 10.2 PROCESS STEP DETAILED REQUIREMENTS & SOLUTION

24

# 10.3 KEY POLICIES AND PROCESS CHANGES ASSOCIATED WITH THE PROCESS

24

# 10.4 STANDARD REPORTING – REFER THE COMMON REPORT 34

25

# 10.5 MASTER DATA CONSIDERATIONS

25

Page 6 of 33
---
# Sales & Distribution Business Blueprint

# 10.6 REPORTING ABAP & BW

# 10.7 INTERFACES

# 10.8 ENHANCEMENTS

# 10.9 FORMS

# 10.10 WORKFLOW

# 11 MASTER DATA – BPML ID 1.26

# 12 REPORTING & COMMON REPORTS – BPML ID 1.27

# 13 WRICEF

Page 7 of 33
---
# Sales & Distribution Business Blueprint

# 1. Project Profile

Brazil Soluble Coffee is green field implementation, commercial production is planned to
start around Mar’23. Soluble Coffee solution in the Olam Global Template will be rolled
out to Brazil Soluble Coffee and add incremental localization components as required for
the business operation. The targeted benefits include:

- Streamlined process across all the businesses
- Eliminate duplicate processes
- Optimize the different applications used and standardize core processes across
the Soluble Coffee Business
- Quicker period end closes
- Eliminate need for collation of information from multiple applications.

# 2. Key Data Structure

BR KDS

Docunentdoc

# 3. Scenario Validation

|BPML ID|Scenario Description|Relevance to Brazil Soluble Coffee|
|---|---|---|
|1.01|Domestic Sales (Start with Contract)|Yes|
|1.02|Domestic Sales -Start with Sales order|Yes|
|1.03|Export Sales|Yes|
|1.06|Sample sales|Yes|
|1.17|Sales Returns|Yes|
|1.18|Debit / Credit Memos|Yes|
|1.10|Intercompany sales (To OIL)|Yes|
|1.26|Master Data|Yes|
|1.27|Reporting|Yes|

Page 8 of 33
---
# Sales & Distribution Business Blueprint

# 4. Domestic Sales (Start with Contract) – BPML ID 1.01

# 4.1. Process Description

Contract is a Fixed contract and are directly created in SAP. The sales order will be created with reference to the contract. The quantity and price can be modified in the Sales Order till it be referenced to delivery. The delivery document will be created in the system if the credit check is successful. The batch will be decided by the quality team and it will be input manually in the delivery document. After delivery creation the picking process will be done and in case of warehouse managed storage location, packing would be carried out if the material is relevant for packing in delivery document. In event of weighbridge application being deployed in a Olam plant, then based on the product truck in and truck out process will capture the weight of the goods being sent to customer. Actual PGI will be done referencing delivery document & actual weight of weighbridge is not considered for billing purpose. After posting goods issue, the billing document for the customer can be generated in the system. The Accounting document and Nota Fiscal will be automatically generated as soon as the billing document be saved.

# SALES ORDER TYPE:

|Sales Order Type|Description EN|Description PT|
|---|---|---|
|ZC13|BR Contract|BR Contrato|
| |BR Domestic|BR Venda|
|ZO21|Sales|Domestica|

# 4.2. Process Step Detailed Requirements & Solution

|Process Step Description|Transaction Codes|Required/Optional|
|---|---|---|
|Create Sales contract – Origin|VA41|Required|
|Contract Print Out|VA43|Optional|
|Create Fixed price Sales order|VA01|Required|
|Credit release (If credit limit exceeded)|VKM3|Required|
|Create Delivery / due for delivery|VL01N|Required|
|Manual / Auto batch Determination|VL02N|Required|
|Create transfer order|LT03|Required|
|Print Pick slip|LT31|Required|
|Confirm transfer order|LT12, LM01|Required|
|Move HUs to repack area|LM01|Optional|
---
# Sales & Distribution Business Blueprint

|Transaction Process Step Description|Codes|Required/Optional|
|---|---|---|
|Repack the HU s|HU02|Optional|
|Move HU s to Picking area|LM01|Optional|
|Picking/Confirm transfer order|LT12, LM01|Optional|
|Weighbridge outbound process- Truck IN|ZWB600|Required|
|Weighbridge outbound process- Truck OUT|ZWB600|Required|
|Post goods issue|VL02N|Required|
|Delivery Printout|VL03N|Required|
|Billing due list|VF04|Optional|
|Create billing document|VF01|Required|
|Invoice printout|VF03|Required|
|Electronic Nota Fiscal Automatic creation|VF03|Required|
|Check Status of the Elect. Nota Fiscal|J1BNFE|Required|
|Print Nota Fiscal|J1B3N|Optional|

# 4.3. Key Policies and Process Changes associated with the Process

Sales order will be created with reference to the Contract

Minimum order quantity and tolerance check at order level

Delivery will be created with reference to sales order

The invoice document will be generated with reference to the delivery document.

# 4.4. Standard Reporting – Refer the Common Report

Refer common report in section 12.

# 4.5. Master Data Considerations (including all relevant data relationships)

- Customer Master
- Material master
- Batch Master
- Pricing condition master
- Tax master
- Output Master
- Credit Master

Page 10 of 33
---
# Sales & Distribution Business Blueprint

# 4.6. Reporting ABAP & BW

|Report name|Report Type (ABAP, BI, BO)|Purpose/ Remarks|
|---|---|---|
|ZSD8001|ABAP|Sales Report|
|ZWB606|ABAP|WeighBridge Report|
|ZSD206|ABAP|Contract Status Report|
|ZSD207|ABAP|Billing Report|
|ZSD412|ABAP|Credit block report|

# 4.7. Interfaces

|Interface|Data Object|Reason|Owner|
|---|---|---|---|
|WEIGHBRIGE|ZGTMMFM_WB_POST_DETAILS|BADI implementation: weight for truck in and truck out| |
| |ZGTSDBADI_WB_UPDATE|Enhancement Implementation| |

# 4.8. Enhancements

|Description|Data Object|Reason|Owner|
|---|---|---|---|
| | | | |

# 4.9. Forms

Refer section 12 for form changes

|Description|Data Object|Owner|
|---|---|---|
| | | |

# 4.10. Workflow

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

Page 11 of 33
---
# Sales & Distribution Business Blueprint

# 5. Domestic Sales -Start with Sales order – BPML ID 1.02

# 5.1. Process Description

No contract is involved in this process. Sales order will be created for local sales with required quantities and price. The price can be modified till the sale order is referenced to delivery. The delivery document will be created in the system if the credit check is successful. The batch will be decided by the quality team and it will be input manually in the delivery document. In event of weighbridge application being deployed in a Olam plant, then based on the product truck in and truck out process will capture the weight of the goods being sent to customer. Actual PGI will be done referencing delivery document & actual weight of weighbridge is not considered for billing purpose. After posting goods issue, the billing document for the customer can be generated in the system. The Accounting document and Nota Fiscal will be automatically generated as soon as the billing document be saved.

# SALES ORDER TYPE:

|Sales Order Type|Description EN|Description PT|
|---|---|---|
|ZO21|Domestic Sales|Venda Domestica|

# 5.2. Process Step Detailed Requirements & Solution

|Process Step Description|Transaction Codes|Required/Optional|
|---|---|---|
|Create Price change order|VA01|Required|
|Credit release (If credit limit exceeds)|VKM3|Required|
|Create Delivery/due for delivery|VL01N|Required|
|Manual & Auto batch Determine|VL02N|Required|
|Create transfer order|LT03|Required|
|Print Pick slip|LT31|Required|
|Picking/Confirm transfer order|LT12, LM01|Required|
|Move HUs to repack area|LM01|Optional|
|Repack the HUs|HU02|Optional|
|Move HUs to Picking area|LM01|Optional|
|Picking/Confirm transfer order|LT12, LM01|Optional|
|Weighbridge outbound process- Truck IN|ZWB600|Required|
|Weighbridge outbound process- Truck OUT|ZWB600|Required|
|Post goods issue|VL02N|Required|
---
# Sales & Distribution Business Blueprint

|Transaction Process Step Description|Required/ Optional Codes|
|---|---|
|Delivery Printout|VL03N Required|
|Billing due list|VF04 Required|
|Create billing document|VF01 Required|
|Invoice printout|VF03 Required|
|Electronic Nota Fiscal Automatic creation|VF03 Required|
|Electronic Nota Fiscal creation and approval|J1BNFE Required|
|Print Nota Fiscal|J1B3N Optional|

# 5.3. Key Policies and Process Changes associated with the Process

Minimum order quantity and tolerance check at order level

Delivery will be created with reference from sales order

The invoice document will be generated with reference to the delivery document.

# 5.4. Standard Reporting – Refer the Common Report

Refer common report in section 12.

# 5.5. Master Data Considerations (including all relevant data relationships)

- Customer Master
- Material master
- Pricing condition master
- Tax master
- Output Master
- Credit Master
- Batch Master

# 5.6. Reporting ABAP & BW

|Report name|Report Type (ABAP, BI, BO)|Purpose/ Remarks|
|---|---|---|
|ZSD8001|ABAP|Sales Report|
|ZWB606|ABAP|Weighbridge Report|
|ZSD207|ABAP|Billing Report|
|ZSD412|ABAP|Credit block report|
---
# Sales & Distribution Business Blueprint

# 5.7. Interfaces

|Interface|Data Object|Reason|Owner|
|---|---|---|---|
|WEIGHBRIGE|ZGTMMFM_WB_POST_DETAILS|BADI implementation: Weigh bridge weight for truck in and truck out|ZGTSDBADI_WB_UPDATE|
| |ZGTSDBADI_WB_UPDATE|Enhancement Implementation| |

# 5.8. Enhancements

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 5.9. Forms

Refer section 12 for form changes

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

# 5.10. Workflow

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

Page 14 of 33
---
# Sales & Distribution Business Blueprint

# 6. Export Sales– BPML ID 1.03

# 6.1. Process Description

Contract is a Fixed contract and are directly created in SAP. The sales order will be created with reference to the contract. The quantity and price can be modified in the Sales Order till it be referenced to delivery. The delivery document will be created in the system if the credit check is successful. The batch will be decided by the quality team and it will be input manually in the delivery document. After delivery creation the picking process will be done and in case of warehouse managed storage location, packing would be carried out if the material is relevant for packing in delivery document. In event of weighbridge application being deployed in a Olam plant, then based on the product truck in and truck out process will capture the weight of the goods being sent to customer. Actual PGI will be done referencing delivery document & actual weight of weighbridge is not considered for billing purpose. After posting goods issue, the billing document for the customer can be generated in the system. The Accounting document and Nota Fiscal will be automatically generated as soon as the billing document be saved.

# SALES ORDER TYPE:

|Sales Order Type|Sales Order Description EN|
|---|---|
|ZC13|BR Contract|
|ZO22|BR Export Sales|

# 6.2. Process Step Detailed Requirements & Solution

|Transaction|Process Step Description|Required/Optional|
|---|---|---|
|VA41|Create Sales contract|Required|
|VA43|Contract Print Out|Optional|
|VA01|Create Fixed price Sales order|Required|
|VKM3|Credit release (If credit limit exceeds)|Required|
|VL01N|Create Delivery/due for delivery|Required|
|VL02N|Manual & Auto batch Determine|Required|
|LT03|Create transfer order|Required|
|LT31|Print Pick slip|Required|
|LT12, LM01|Picking/Confirm transfer order|Required|
|LM01|Move HUs to repack area|Optional|
|HU02|Repack the HUs|Optional|
---
# Sales & Distribution Business Blueprint

|Transaction Process Step Description|Codes|Required/Optional|
|---|---|---|
|Move HU s to Picking area|LM01|Optional|
|Picking/Confirm transfer order|LT12, LM01|Optional|
|Weighbridge outbound process- Truck IN|ZWB600|Required|
|Weighbridge outbound process- Truck OUT|ZWB600|Required|
|Post goods issue|VL02N|Required|
|Delivery Printout|VL03N|Required|
|Billing Due list|VF04|Required|
|Create billing document|VF01|Required|
|Invoice printout|VF03|Required|
|Electronic Nota Fiscal Automatic creation|VF03|Required|
|Electronic Nota Fiscal creation and approval|J1BNFE|Required|
|Print Nota Fiscal|J1B3N|Optional|

# 6.3. Key Policies and Process Changes associated with the Process

Sales order will be created with reference to Contract

Minimum order quantity and tolerance check at order level

Delivery will be created with reference from sales order

The invoice document will be generated with reference to the delivery document

# 6.4. Standard Reporting – Refer the Common Report

Refer common report in section 12.

# 6.5. Master Data Considerations (including all relevant data relationships)

- Customer Master
- Material master
- Batch Master
- Pricing condition master
- Output master
- Material Determination
- Credit Master

Page 16 of 33
---
# Sales & Distribution Business Blueprint

# 6.6. Reporting ABAP & BW

|Report name|Report Type (ABAP, BI, BO)|Purpose/ Remarks|
|---|---|---|
|ZSD8001|ABAP|Sales Report|
|ZWB606|ABAP|Weighbridge Report|
|ZSD206|ABAP|Contract Status Report|
|ZSD207|ABAP|Billing Report|
|ZSD412|ABAP|Credit block report|

# 6.7. Interfaces

|Interface|Data Object|Reason|Owner|
|---|---|---|---|
|WEIGHBRIGE|ZGTMMFM_WB_POST_DETAILS|BADI implementation: weight for truck in and truck out|GT|
| |ZGTSDBADI_WB_UPDATE| | |

# 6.8. Enhancements

|Description|Data Object|Reason|Owner|
|---|---|---|---|
| | | | |

# 6.9. Forms

Refer section 12 for form changes

|Description|Data Object|Owner|
|---|---|---|
| | | |

Page 17 of 33
---
# Sales & Distribution Business Blueprint

# 6.10. Workflow

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

Page 18 of 33
---
# Sales & Distribution Business Blueprint

# 7. Intercompany Sales (To OIL)– BPML ID 1.10

# 7.1. Process Description

Contract is a Fixed contract and it is interfaced through CTRM. The sales order will be interfaced through CTRM with reference to Shipping Order. The delivery document will be created in the system if the credit check is successful. OPS details will be entered delivery document. The batch will be decided by the quality team and it will be input manually in the delivery document. After delivery creation the picking process will be done and in case of warehouse managed storage location, packing would be carried out if the material is relevant for packing in delivery document. In event of weighbridge application being deployed in a Olam plant, then based on the product truck in and truck out process will capture the weight of the goods being sent to customer. Actual PGI will be done referencing delivery document & actual weight of weighbridge is not considered for billing purpose. After posting goods issue, the billing document for the customer can be generated in the system. The Accounting document and Nota Fiscal will be automatically generated as soon as the billing document be saved.

# SALES ORDER TYPE:

|Sales Order Type|Sales Order Description EN|
|---|---|
|ZC13|BR Contract|
|ZO22|BR Export Sales|

# 7.2. Process Step Detailed Requirements & Solution

|Transaction|Process Step Description|Required/Optional|
|---|---|---|
|CTRM|Create Sales contract|Required|
|VA43|Contract Print Out|Optional|
|CTRM|Create Fixed price Sales order|Required|
|VKM3|Credit release (If credit limit exceeds)|Required|
|VL01N|Create Delivery/due for delivery|Required|
|VL02N|Manual & Auto batch Determine|Required|
|LT03|Create transfer order|Required|
|LT31|Print Pick slip|Required|
|LT12, LM01|Picking/Confirm transfer order|Required|
|LM01|Move HUs to repack area|Optional|
|HU02|Repack the HUs|Optional|
|LM01|Move HUs to Picking area|Optional|
---
# Sales & Distribution Business Blueprint

|Transaction Process Step Description|Codes|Required/Optional|
|---|---|---|
|Picking/Confirm transfer order|LT12, LM01|Optional|
|Weighbridge outbound process- Truck IN|ZWB600|Required|
|Weighbridge outbound process- Truck OUT|ZWB600|Required|
|Post goods issue|VL02N|Required|
|Delivery Printout|VL03N|Required|
|Billing Due list|VF04|Required|
|Create billing document|VF01|Required|
|Invoice printout|VF03|Required|
|Electronic Nota Fiscal Automatic creation|VF03|Required|
|Electronic Nota Fiscal creation and approval|J1BNFE|Required|
|Print Nota Fiscal|J1B3N|Optional|

# 7.3. Key Policies and Process Changes associated with the Process

Sales order will be created with reference to Contract

Minimum order quantity and tolerance check at order level

Delivery will be created with reference from sales order

The invoice document will be generated with reference to the delivery document

# 7.4. Standard Reporting – Refer the Common Report

Refer common report in section 12.

# 7.5. Master Data Considerations (including all relevant data relationships)

- Customer Master
- Material master
- Batch Master
- Pricing condition master
- Output master
- Material Determination
- Credit Master

# 7.6. Reporting ABAP & BW

|Report name|Report Type (ABAP, BI, BO)|Purpose/ Remarks|
|---|---|---|
|ZSD8001|ABAP|Sales Report|
|ZWB606|ABAP|Weighbridge Report|
|ZSD206|ABAP|Contract Status Report|
---
# Sales & Distribution Business Blueprint

|Report name|Report Type (ABAP, BI, BO)|Purpose/ Remarks|
|---|---|---|
|ZSD207|ABAP|Billing Report|
|ZSD412|ABAP|Credit block report|

# 7.7. Interfaces

|Interface|Data Object|Reason|Owner|
|---|---|---|---|
|WEIGHBRIGE|ZGTMMFM_WB_POST_DETAILS|BADI implementation: Weigh bridge weight|GT|
| |ZGTSDBADI_WB_UPDATE|Enhancement Implementation| |
|CTRM to SAP|RFC|CTRM purchase contract to SAP Sales Contract|GT|
|CTRM to SAP|RFC|CTRM Shipping Instructions to SAP Sales Order|GT|
|SAP to CTRM|RFC|SAP delivery to CTRM shipment|GT|
|SAP to CTRM|RFC|SAP sales invoice to CTRM purchase invoice|GT|

# 7.8. Enhancements

|Description|Data Object|Reason|Owner|
|---|---|---|---|
| | | | |

# 7.9. Forms

Refer section 12 for form changes

|Description|Data Object|Owner|
|---|---|---|
| | | |

Page 21 of 33
---
# Sales & Distribution Business Blueprint

# 7.10. Workflow

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

Page 22 of 33
---
# Sales & Distribution Business Blueprint

# 8. Sample sales process – BPML ID 1.06

# 8.1. Process Description

Sample sales order is created whenever a request for sample is received from customer or marketing team decides to send a sample to customer. Since this is a sample sale, no price needs to be recorded in the order/invoice. The delivery document will be created with reference to sales order. After posting goods issue, the billing document for the customer can be generated in the system viz, a zero value invoice will be generated.

# SALES ORDER TYPE:

|Sales Order Type|Description EN|
|---|---|
|ZO24|BR Sample Order|

# 8.2. Process Step Detailed Requirements & Solution

|Process step Description|Transaction Codes|Required/Optional|
|---|---|---|
|Create sales order|VA01|Required|
|Create Delivery/due for delivery|VL01N|Required|
|Manual & Auto batch Determine|VL02N|Required|
|Post goods issue|VL02N|Required|
|Delivery Printout|VL03N|Required|
|Billing Due list|VF04|Required|
|Create sample sales invoice|VF01|Required|
|Electronic Nota Fiscal Automatic creation|VF03|Required|
|Electronic Nota Fiscal creation and approval|J1BNFE|Required|
|Print Nota Fiscal|J1B3N|Optional|

# 8.3. Key Policies and Process Changes associated with the Process

During Goods Issue the consumption is posted to the Sample COGS Account. Invoice will be generated with zero prices for unpriced sample sales.

# 8.4. Standard Reporting – Refer the Common Report

Refer common report in section 12.

# 8.5. Master Data Considerations (including all relevant data relationships)

Customer Master

Page 23 of 33
---
# Sales & Distribution Business Blueprint

# 8.6. Reporting ABAP & BW

|Report name|Report Type (ABAP, BI, BO)|Purpose/ Remarks|
|---|---|---|
|ZSD8001|ABAP|Sales Report|
|ZSD207|ABAP|Billing Report|

# 8.7. Interfaces

|Desc|Interface Method|Application|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 8.8. Enhancements

|Description|Data Object|Reason|Owner|
|---|---|---|---|
|NA|NA|NA|NA|

# 8.9. Forms

Refer section 12 for form changes

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

# 8.10. Workflow

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

Page 24 of 33
---
Sales & Distribution Business Blueprint
                  Page 25 of 33
---
# Sales & Distribution Business Blueprint

# 9. Sales Return Order Process – BPML ID 1.17

# 9.1. Process Description

Customer returns could occur due to number of business reasons like wrong products shipped, or customer complaints. Customer complaints regarding quality are noted and reasons analysed.

In case it is determined that the party at fault is OLAM, then customer might ask for a sales return. It can also be settled through quality claims by debit/credit memo but in case if the goods are sent back it should be taken back in our stock. In this case, the goods will go the quality stock for further inspection.

The delivery document will be created in the system with reference to sales order. The batch will be automatically determined in the delivery document.

In event of weighbridge application being deployed in a Olam plant, then based on the product truck in and truck out process will capture the weight of the goods being received from customer.

Actual PGR will be done referencing delivery document & actual weight of weighbridge is not considered for billing purpose.

The billing block gets activated in the sales returns document which should be removed by authorised person to create credit memo.

# SALES ORDER TYPE:

|Sales Order Type|Description EN|
|---|---|
|ZO35|Return Order Cust.NF|
|ZO36|Return Order Own.NF|
|ZO37|BR Return w/o Deliv|

# 9.2. Process Step Detailed Requirements & Solution

|Process step Description|Transaction Codes|Required/Optional|
|---|---|---|
|Create Return sales order with reference to billing document|VA01|Required|
|Enter the Order reasons|VA01|Required|
|Create Returns Delivery|VL01N|Required|
|weighbridge outbound process- Truck IN|ZWB600|Optional|
|weighbridge outbound process- Truck OUT|ZWB600|Optional|
|Post goods Receipt to Return stock|VL02N|Required|
|Create Invoice/Credit Memo|VF01|Required|

Page 26 of 33
---
# Sales & Distribution Business Blueprint

|Process step|Transaction Codes|Required/ Optional|
|---|---|---|
|Release to accounting|VF02|Required|
|Electronic Nota Fiscal| |Required|
|Automatic creation|VF03| |
|Check Status of the Elect. Nota Fiscal|J1BNFE|Required|
|Print Nota Fiscal|J1B3N|Optional|

# 9.3 Key Policies and Process Changes associated with the Process

The returned stock will go for quality check.

The billing block should be removed by authorized person to create return invoice document (Credit memo).

Return order quantity should not be more than that of invoice quantity.

Material documents will be posted in the month of the material document period which is open and the goods are physically moved in.

# 9.4 Standard Reporting – Refer the Common Report

Refer common report in section 12.

# 9.5 Master Data Considerations (including all relevant data relationships)

- Customer Master
- Material master
- Batch Master
- Pricing condition master
- Output Master

# 9.6 Reporting ABAP & BW

|Report name|Report Type (ABAP, BI, BO)|Purpose/ Remarks|
|---|---|---|
|ZSD8001|ABAP|Sales Report|
|ZWB606|ABAP|Weighbridge Report|
|ZSD207|ABAP|Billing Report|

Page 27 of 33
---
# Sales & Distribution Business Blueprint

# 9.7 Interfaces

|Interface|Data Object|Reason|Owner|
|---|---|---|---|
|ZGTMMFM_WB_POST_DETAILS|WEIGHBRIGE|BADI implementation: bridge weight for truck in and truck out|GT|
| |ZGTSDBADI_WB_UPDATE|Enhancement Implementation| |
| |ZGTSDBADI_WB_UPDATE| | |

# 9.8 Enhancements

|Description|Data Object|Reason|Owner|
|---|---|---|---|
| | | | |

# 9.9 Forms

Refer section 12 for form changes

# 9.10 Workflow

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

Page 28 of 33
---
# Sales & Distribution Business Blueprint

# 10. Debit Memo / Credit Memo Process – BPML ID 1.18

# 10.1 Process Description

When the customer is claiming for quality issues in the delivered products, negotiation happens through exchange of mails & the price will be agreed to issue the credit memo.

In other cases, if the invoice value is less than actual, a debit memo can be issued to collect the balance amount.

Debit /credit memo also arise in case of missing bags or when business circumstances necessitate usage of debit/credit memo.

During the quality claims, it will be decided whether the customer returns the goods or agrees for a credit memo. If the customer sends the goods, we have to follow the process of goods returns (Sales return). If it is agreed for credit memo then the credit memo requests will be created in the system with reference to the original billing document.

The credit memo will be created corresponding to the credit memo request after the billing block is removed by the authorised person.

# SALES ORDER TYPE:

|Sales Order Type|Sales Order Description|EN Type|
|---|---|---|
|ZO33|BR Credit Memo Req| |
|ZO34|BR Debit Note Req| |

# 10.2 Process Step Detailed Requirements & Solution

|Process step Description|Transaction Codes|Required/Optional|
|---|---|---|
|Create Credit/Debit memo request|VA01|Required|
|Remove billing block|VA02|Required|
|Create Credit/Debit memo|VF01|Required|
|Release to accounting|VF02|Required|
|Electronic Nota Fiscal Automatic creation (Only For Debit Memo)|VF03|Required|
|Check Status of the Elect. Nota Fiscal (Only For Debit Memo)|J1BNFE|Optional|
|Print Nota Fiscal (Only For Debit Memo)|J1B3N|Optional|

Page 29 of 33
---
# Sales & Distribution Business Blueprint

# 10.3 Key Policies and Process Changes associated with the Process

The credit / debit memo request should be created with reference to invoice.

The price on the document can be the negotiated amount on quality issues.

The billing block should be removed by authorized person to create credit memo document.

The credit memo request should always be created with reference to invoice, to keep the document relationships.

# 10.4 Standard Reporting – Refer the Common Report 34

Refer common report in section 12.

# 10.5 Master Data Considerations

- Customer Master
- Material master
- Pricing condition master
- Output Master

# 10.6 Reporting ABAP & BW

Report name
Report Type (ABAP, BI, BO)
Purpose/ Remarks

# 10.7 Interfaces

Interface
Data Object
Reason
Owner

# 10.8 Enhancements

Description
Data Object
Reason
Owner

# 10.9 Forms

Description
Data Object
Owner

Page 30 of 33
---
# Sales & Distribution Business Blueprint

# 10.10 Workflow

|Description|Data Object|Owner|
|---|---|---|
|NA|NA|NA|

# 11 Master Data – BPML ID 1.26

Conversion Design Document will contain details of the Master Data. General Master Data where Customers master, Sales organisation, Plant, Material etc are involved for the interface to Pluto from SAP. Other SAP master data are also there which are maintained for the purpose of the process flow.

|Process step|Description|Transaction Codes|Required/Optional|
|---|---|---|---|
|Customer Master|Create Customer Master|XD01|Required|
| |Change Customer Master|XD02|Required|
| |Update Credit Master Record for Customer|FD32|Required|
| |Block Customer - By Sales Area|VD05|Optional|
| |Block Customer - By Company Code|XD05| |
| |Flag for Deletion - By Sales Area|VD06|Optional|
| |Flag for Deletion - By Company Code|XD06|Optional|
| |Change Account Group|XD07|Optional|
| |Display Changes to Customer|OV51|Optional|
| |Display Customer Master|XD03| |

# Outputs

|Description|Transaction Codes|Required/Optional|
|---|---|---|
|Create Sales Output|VV11|Required|
|Change Sales Output|VV12|Required|
|Display Sales Output|VV13|Required|
|Create Delivery Output - (Outbound Delivery, Pick List, Pack List)|VV21|Required|
|Change Delivery Output|VV22|Required|
|Display Delivery Output|VV23|Required|
|Create Invoice Output|VV31|Required|
|Change Invoice Output|VV32|Required|
|Display Invoice Output|VV33|Required|

Page 31 of 33
---
# Sales & Distribution Business Blueprint

# 12 Reporting & Common Reports – BPML ID 1.27

|Transaction Code|Description|
|---|---|
|VA05N|List of Sales Orders|
|VA45|List of Contracts|
|VA14L|Sales Documents Blocked for|
| |Delivery|
|V.23|Sales Documents Blocked for|
| |Billing|
|VL06O|Outbound Delivery Monitor|
|VF04|Deliveries due for Billing|
|VF05N|List of Billing Documents|
|F.31|Credit Management Overview|
|VCUST|Customer List|
|MMBE|Material Stock Overview|
|MM60|Material list|

Page 32 of 33
---
# Sales & Distribution Business Blueprint

# WRICEF

|S. No.|WRICEF Type|RICEF Name|Remarks|Delivery Time|
|---|---|---|---|---|
|1|Form|Sales Contract| |In Progress|
|2|Form|Sales Order Confirmation| |In Progress|
|3|Form|Delivery Order| |In Progress|
|4|Form|Picking list| |In Progress|
|5|Form|Packing List| |In Progress|
|6|Form|Invoice| |In Progress|
|7|Interface|CTRM for Sales Contract| |In Progress|
|8|Interface|CTRM for Sales Order| |In Progress|
|9|Interface|CTRM for OPS| |In Progress|
|10|Interface|CTRM for Invoice| |In Progress|

Page 33 of 33