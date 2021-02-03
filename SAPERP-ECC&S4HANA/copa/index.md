# SAP COPA

```
SAP COPA

```

## Process Modeling:

### Profitability and Cost Analysis:

[![profitability&cost](Profitability&CostAnalysis.png)](https://www.sap.com "SAP")

### Types of COPA 

- Costing-based CO-PA groups costs and revenues according to value fields and Costing-based valuation approaches in a
separate persistence. This solution is already available for long period and is widely used by customers. Costing-based CO-PA
is available in SAP ERP Financials and SAP S/4HANA Finance (in maintenance mode).

- Account-based CO-PA profitability analysis is using an account-based valuation approach. Also, this solution is available for
a long period. Account-based is available only in SAP ERP Financials (in maintenance mode).

- Combined CO-PA (fka “profitability subledger”) is designed as “Best of both worlds”. Technically this is an enhancement of Costing-based CO-PA with additional persistence consisting of 4 new tables CE9xxxx_xx. It eliminates shortcomings
of the legacy versions 1. and 2. of CO-PA regarding reconciliation with GL, currencies and quantities. Combined CO-PA can be
run in addition to CB and/ or AB CO-PA and is currently available with S/4HANA.

- Simplified Profitability Analysis (fka “Profitability Analysis in the Universal Journal”) offers a new form of profitability analysis, which is part of the new product SAP S/4HANA Finance and is technically based on the former Account-based CO-PA. 

## Configuration

### Costing based COPA:

- Define Characteristics (Transaction: KEA5)
- Define Value Fields (Transaction: KEA6)
- Create Operating Concern (Transaction: KEA0)
- Assign Company Code to Controlling Area (Transaction: OX19)
- Assign Controlling Area to Operating Concern (Transaction: KEKK)
- Activate COPA (Transaction: KEKE)
- COPA: Additional Functionalities (Transaction: KECP)
- COPA: Transport (Dev, Quality system to Prod - KE3I)
- Master Data: Maintain Characteristic Values (Transaction: KES1)
- Master Data: Define Characteristic Hierarchy (Transaction: KES3)
- Master Data: Derivation Rule (Transaction: KEDR)
- Master Data: Valuation (Transaction: KE21S)
    - Valuation using Material Cost Estimate.
    - Valautio using Condition.
- Planning: (Level, Package, Parameter Set)  (Transaction: KEPM)
- Planning Methods: (Display, Copy PM) (Transaction: KEPM)
- Planning Methods: (Forecast PM) (Transaction: KE1T)
    - Top down Distribution
- Planning Methods: Ratio (Transaction: KE1I, KE16)
- Planning Methods: Valuation (Transaction: KE1I, KE16)
    - Define access to Standard Cost Estimates 
    ```
    (SPRO --> Controlling --> P.A --> Master Data --> Valuation --> Set Up Valuation using Material Cost Estimate
    --> Define access to Standard Cost Estimates)

    ```
    - Define access to actual costing/material ledger
        ```
    (SPRO --> Controlling --> P.A --> Master Data --> Valuation --> Set Up Valuation using Material Cost Estimate
    --> Define access to actual costing/material ledger)

    ```
    - Assign Costing Key to Product (Transaction: KE4H)
    - Assign costing key to material type (Transaction: KE4J)
    - Assign costing keys to any characteristics (Transaction: KEPC)
    - Assign value fields (Transaction: KE4R)
    - Create parameter (Transaction: KEPM)
    - Execute method (Transaction: KEPM)
    - Valuation Simulation (Transaction: KE21S)
        - Valaution using Material Cost Estimate
        - Valaution using Condition & Costing Sheet

- Planning Methods: Condition Table - Profitability Analysis
    - Define Condition Table (Transaction: KE4A)
    - Define Access Sequences (Transaction: KE48)
    - Create condition type & costing sheet (Transaction: 8KEV)
    - Display condition type (Transaction: KE41)
    - Assign Value Field (Transaction: KE45)
    - Define & Assign Valuation Strategy (Transaction: KE4U)
    - Valuation using condition & costing sheet (Transaction: KE4A)

- Planning Methods: Revaluation
- Planning Methods: Event (Transaction: KEPM)
- Planning Methods: Period Distribution (Transaction: KEPM)
- Planning Methods: Planning Sequence (Transaction: KEPM)

- Assessment Cycle: Create - (Transaction: KEU1)
- Assessment Cycle: Plan - (Transaction: KEU7)
- Assessment Cycle: Execute - Actual (Transaction: KEU5)
- Assessment Cycle: Execute - Plan (Transaction: KEUB)


### Costing versus Account based COPA:

| Description | Costing based | Account based |
| Postings | Sales Order is Created | Accounting Document is posted to Financial Accounting |
| COPA Data Transfer | Data is transferred with Value Fields to Costing based COPA Tables | Data is transferred with Revenue/Cost elements to ACDOCA tables. |
| COGS Postings | With Billing Document Posting | With Post Goods Issue (PGI) |
| Reconciliation with GL | Pain point | Reconciled |
| Currencies | Operating Concern Currency; Company Code Currency | Controlling Area Currency, Company Code Currency, Transaction Currency |
| Settlement | Costs are settled from the original cost elements to the valuefields to which they are assigned in the PA transfer structure | Costs are settled to the settlement cost element specified in the settlement structure |
| Parallel Valuation | Costing based COPA provides 6 parallel valuations forcalculating the cost of goods sold (COGS). This enables youcompare the standard cost for sales processes with differentproduction opportunities in different plants. | N/A |
| Sales Order Analysis | Can transfer the sales order data to Profitability Analysis =>an early analysis of profit forecast can be carried out. | N/A |
| COPA Tables | Costing based COPA Stores Data in CE1XXXX to CE1XXXX tables. CE1XXXX is actuals data CE2XXXX is Plan data. CE3XXXX & CE4XXXX contain aggregated and segment level data within the Operating Concern | Account based COPA Stores data in general CO tables. Line item actual data in ACDOCA. Line item plan data in ACDOCP. Actual line item in COEP value type not equal to 4 and not equal to 11. Plan line item in COSP & COEJ specific value types |


## SAP Best Practices COPA Account Structure:

<iframe src="https://drive.google.com/file/d/1h0I7oaphfTzy_mSqYfOyIUuBoxkvHy-q/preview" width="640" height="480"></iframe>

## Tables:

| COPA | Description |
|-----------------|--------------|
| CE1XXXX | Costing Based: Actual Line-items |
| CE2XXXX | Costing Based: Plan Line-items |
| CE3XXXX | Costing Based: Totals records per profitability segment |
| CE4XXXX | Costing & Account Based: Profitability Segment Definitions |
| COEJ | Account Based: Actual Line-items |
| COEP | Account Based: Plan Line-items (value type ≠ 4 and ≠ 11) |
| COSP | Account Based: Primary Costs - Totals records per profitability segment |
| COSS | Account Based: Secondary Costs - Totals records per profitability segment |
| ACDOCA | Account Based: Actual Line-items |
| ACDOCP | Account Based: Plan Line-items |
|-----------------|--------------|

## Transactions:

| ECC Tr. | S4 Tr. | Description |
|-------------------|-------------------|-------------|
| KA01 | FS00 | Create Primary Cost Element |
| KA02 | FS00 | Change Cost Element |
| KA03 | FS00 | Display Cost Element |
| KA06 | FS00 | Create Secondary Cost Element |
| KE21 | KE21N | Create CO-PA line item |
| KE23 | KE24 | Display CO-PA line item |
| N/A | FAGLCOFIFLUP | Transfer CO documents from worklist to FI (Realtime – integration) |
|-------------------|-------------------|-------------|

## Programs, Function Modules and Exits:



## Platforms:

|     ECC      |  S/4 HANA    |      U/X      |  Database     |
|--------------|--------------|---------------|---------------|
|   SAP ERP    | SAP S/4 HANA |  SAP FIORI    |  SAP HANA     |
|--------------|--------------|---------------|---------------|

Note: S/4 (cloud & on-premise) works only on Hana DB while SAP ERP is compatible with Hana DB, MS Sql, Oracle DB, IBM DB2 etc.

## SAP Profitability Analysis

<iframe src="https://drive.google.com/file/d/1ZlIzUY5lQ_qZxb7nJrMfonhGt1iH0xFz/preview" width="640" height="480"></iframe>
