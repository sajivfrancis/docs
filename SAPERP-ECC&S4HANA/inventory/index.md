# INVENTORY IN SAP

```
DOCS related to Inventory Valuation & Management

```

## Process Modeling:

### Core Inventory Management

[![CoreInventoryManagement](CoreInventoryManagement.png)](https://www.sap.com "SAP")

### Inventory Valuation for Year End Closing

[![YEInventoryValuation](InventoryValuationforYearEndClosing.png)](https://www.sap.com "SAP")

### Managing Material Price Changes & Inventory Values

[![CoreInventoryManagement](MatPrice&InvValues.png)](https://www.sap.com "SAP")


## SAP Best Practices Inventory Account Structure:

<iframe src="https://drive.google.com/file/d/15hgsskJjLOFgNhsDzqoqQZRC4_2Pel1s/preview" width="640" height="480"></iframe>

## Tables:

| Table | Description |
|-----------------|--------------|


## Programs, Function Modules and Exits:

| Programs | Description | Type |
|-----------------|--------------|--------------|
|-----------------|--------------|--------------|

## Role-based Fiori Apps:

### Inventory

- Material Inventory Values - Rounding Diff (Design Studio)
- Schedule Inventory Accounting Jobs

## Tables:

| Table | Name | S/4HANA - Notes |
|-------|------|-----------------|
| IKPF | Header: Physical Inventory Document | In Logical Database IMM INM IRM. |
| ISEG | Physical Inventory Document Items | In Logical Database IMM INM IRM. |
| MCHB | Batch Stocks | In Logical Database /SAPSLL/CUSMSM MSM. |
| MKOL | Special Stocks from Vendor | In Logical Database MSM. |
| MSKA | Sales Order Stock |  |
| MSKU | Special Stocks with Customer |  |
| MSLB | Special Stocks with Supplier |  |
| MSPR | Project Stock |  |
| MSSA | Total Customer Orders on Hand |  |
| MSSQ | Project Stock Total |  |
| MSTB | Stock in Transit |  |
| MSTE | Stock in Transit to Sales and Distribution Document |  |
| MSTQ | Stock in Transit for Project |  |
|-------|------|-----------------|


## Platforms:

|     ECC      |  S/4 HANA    |      U/X      |  Database     |
|--------------|--------------|---------------|---------------|
|   SAP ERP    | SAP S/4 HANA |  SAP FIORI    |  SAP HANA     |
|--------------|--------------|---------------|---------------|

Note: S/4 (cloud & on-premise) works only on Hana DB while SAP ERP is compatible with Hana DB, MS Sql, Oracle DB, IBM DB2 etc.
