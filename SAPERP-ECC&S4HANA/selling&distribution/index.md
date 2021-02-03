# SAP SD MODULE

```
DOCS related to SAP Selling & Distribution

```

## Process Modeling:

### Order to cash process overview:

[![OTC](OTC.png)](https://docs.sajivfrancis.com "DOCS")

### Selling & Distribution process overview:

[![SDOVERVIEW](sdoverview.png)](https://docs.sajivfrancis.com "DOCS")

## Tables:

| Table | Name | S/4HANA - Notes |
|-------|------|-----------------|
| LIKP | SD Document: Delivery Header Data | In Logical Database ALV PSJ VLV. |
| LIKPUK | View: Delivery Header + Status Data |  |
| VBAK | Sales Document: Header Data | In Logical Database AAV CKS CKS_WAO PSJ SD_ORDER SD_SALES_DOCUMENT VAV VC1. |
| VBAKUK | Generated Table for View | VBAK & VBUK. |
| VBAP | Sales Document: Item Data | In Logical Database AAV CKS CKS_WAO PSJ SD_ORDER SD_SALES_DOCUMENT VAV VC2. |
| VBBE | Sales Requirements: Individual Records |  |
| VBDKA | Document Header View for Inquiry,Quotation,Order |  |
| VBDPA | Document Item View for Inquiries,Quotation,Order |  |
| VBEP | Sales Document: Schedule Line Data | In Logical Database AAV SD_ORDER SD_SALES_DOCUMENT VAV. |
| VBFA | Sales Document Flow | In Logical Database AAV AKV ALV ARV SD_ORDER SD_SALES_DOCUMENT VAV VC1 VFV VLV. |
| VBKA | Sales Activities | In Logical Database AKV VC1 VC2. |
| VBKD | Sales Document: Business Data | In Logical Database AAV PSJ SD_ORDER SD_SALES_DOCUMENT VAV. |
| VBPA | Sales Document: Partner | In Logical Database AAV AKV ALV ARV SD_ORDER SD_SALES_DOCUMENT VAV VC1 VFV VLV. |
| VBUK | Sales Document: Header Status and Administrative Data | In Logical Database AAV AKV ALV ARV PSJ SD_ORDER 

| SD_SALES_DOCUMENT VAV VFV VLV. | | |
|-------|------|-----------------|
| VBUV | Sales Document: Incompletion Log | In Logical Database AAV AKV SD_ORDER SD_SALES_DOCUMENT VAV. |
| VEDA | Contract Data | In Logical Database SD_ORDER SD_SALES_DOCUMENT. |

| Billing and Pricing     |  |  |
|-------|------|-----------------|
| A005 | Customer/Material | For items get the value in Condition record number (KNUMH) and go to table KONP. |
| FPLA | Billing Plan | In Logical Database ERM PSJ SD_SALES_DOCUMENT. Category (FPTYP)=0 for Billing plan in SD |
| KOMK | Communication Header for Pricing |  |
| KOMP | Communication Item for Pricing |  |
| KONP | Conditions (Item) | In Logical Database ERM ILM V12L. |
| VBRK | Billing Document: Header Data | In Logical Database ARV VFV VXV. |
| VBRKUK | Billing Document Header and Status Data |  |
| VBRP | Billing Document: Item Data | In Logical Database ARV VC2 VFV VXV. |
| VRPMA | SD Index: Billing Items per Material |  |

| Billing Documents Copy Control     |  |  |
|-------|------|-----------------|
| TVCPF | Billing: Copying Control |  |
| TVFSP | Billing: Blocking Reasons |  |

| Customer for Sales and Distribution     |  |  |
|-------|------|-----------------|
| BUT000 | Business Partner: General data I | In Logical Database REBP UKM_BUPA. |
| BUT020 | Business Partner: Addresses | In Logical Database REBP. |
| BUT100 | Business Partner: Roles | In Logical Database REBP. |
| CVI_CUST_LINK | Assignment Between Customer and Business Partner |  |
| KLPA | Customer/Vendor Linking |  |
| KNA1 | General Data in Customer Master | In Logical Database BRF DDF SD_KUSTA VC1 VC2 VDF WTY. |
| KNB1 | Customer Master (Company Code) | In Logical Database BRF DDF VDF. |
| KNB4 | Customer Payment History | In Logical Database BRF DDF. |
| KNB5 | Customer master (dunning data) | In Logical Database BRF DDF. |
| KNBK | Customer Master (Bank Details) | In Logical Database BRF DDF. |
| KNKA | Customer master credit management: Central data | In Logical Database DDF. |
| KNKK | Customer master credit management: Control area data | In Logical Database BRF DDF. |
| KNVA | Customer Master Unloading Points |  |
| KNVD | Customer master record sales request form |  |
| KNVH | Customer Hierarchies |  |
| KNVI | Customer Master Tax Indicator |  |
| KNVK | Customer Master Contact Partner | In Logical Database SD_KUSTA VC1 VC2. |
| KNVL | Customer Master Licenses |  |
| KNVP | Customer Master Partner Functions | In Logical Database SD_KUSTA VC2. |
| KNVS | Customer Master Shipping Data |  |
| KNVV | Customer Master Sales Data | In Logical Database SD_KUSTA VC1 VC2. |

| Finance Links for Sales and Distribution     |  |  |
|-------|------|-----------------|
| COES | CO Object: Sales Order Value Line Items |  |
| KNA1 | General Data in Customer Master | In Logical Database BRF DDF SD_KUSTA VC1 VC2 VDF WTY. |
| KNB1 | Customer Master (Company Code) | In Logical Database BRF DDF VDF. |
| KNB5 | Customer master (dunning data) | In Logical Database BRF DDF. |
| KNVD | Customer master record sales request form |  |
| KNVP | Customer Master Partner Functions | In Logical Database SD_KUSTA VC2. |
| KNVV | Customer Master Sales Data | In Logical Database SD_KUSTA VC1 VC2. |

| Material Management-Link for Sales and Distribution      |  |  |
|-------|------|-----------------|
| MAKT | Material Descriptions | Field ‘Mat. desc MAKTG' for search. Logical Database MMIMRKPFRESB S1L S2L. |
| MARA | General Material Data | In Logical Database /SAPSLL/CUSMSM BAM BKM BMM CKM EBM ECM ENM ESM IFM S1L WTY. |
| MARC | Plant Data for Material | S/4: Master data without stock aggregates. In Logical Database /SAPSLL/CUSMSM S1L. |
| MARD | Storage Location Data for Material | S/4: Master data without stock aggregates. In Logical Database /SAPSLL/CUSMSM MSM. |
| MARM | Units of Measure for Material | In Logical Database MSM. |
| MBEW | Material Valuation | In Logical Database /SAPSLL/CUSMSM BMM CKA. |
| MLAN | Tax Classification for Material |  |
| MVKE | Sales Data for Material | In Logical Database MSM. |
| T179 | Materials: Product Hierarchies |  |

| Sales Documents Copy Control     |  |  |
|-------|------|-----------------|
| TVAK | Sales Document Types |  |
| TVASP | Sales Documents: Blocking Reasons |  |
| TVCPA | Sales Documents: Copying Control |  |
| TVCPF | Billing: Copying Control |  |
| TVCPL | Deliveries: Copying Control |  |

| Sales Document Item Categories Copy Control     |  |  |
|-------|------|-----------------|
| T184 | Sales Documents: Item Category Determination |  |
| TVAPT | Sales document item categories: Texts |  |
| TVCPA | Sales Documents: Copying Control |  |
| TVCPF | Billing: Copying Control |  |
| TVCPL | Deliveries: Copying Control |  |
| TVEPZ | Sales Document: Schedule Line Category Determination |  |
| TVLP | Deliveries: Item Categories |  |
| TVPT | Sales documents: Item categories |  |

| Delivery Documents Copy Control     |  |  |
|-------|------|-----------------|
| T184L | Sales Documents: Item Category Determination |  |
| TVCPF | Billing: Copying Control |  |
| TVCPL | Deliveries: Copying Control |  |
| TVLSP | Delivery Blocks |  |

| More Sales and Distribution Tables     |  |  |
|-------|------|-----------------|
| NAST | Message Status | In Logical Database AAV AKV ALV ARV ERM. |
| SADR | Address Management: Company Data | In Logical Database AAV AKV ALV ARV. |
| T049E | Control Data for Swiss ISR Procedure |  |
| TNAPR | Processing programs for output |  |

| Enterprise Structure    Part of the Customizing |  |  |
|-------|------|-----------------|
| Table | Table - Name | S/4HANA -Table and general Notes |
| T001K | Valuation area |  |
| T001L | Storage Locations |  |
| T001W | Plants/Branches |  |
| T499S | Location |  |
| TSPA | Organizational Unit: Sales Divisions |  |
| TVBUR | Organizational Unit: Sales Offices |  |
| TVBVK | Organizational Unit: Sales Groups per Sales Office |  |
| TVKBZ | Org.Unit: Sales Office: Assignment to Organizational Unit |  |
| TVKGR | Organizational Unit: Sales Groups |  |
| TVKO | Organizational Unit: Sales Organizations |  |
| TVKWZ | Org.Unit: Allowed Plants per Sales Organization |  |
| TVTA | Organizational Unit: Sales Area(s) |  |
| TVTW | Organizational Unit: Distribution Channels |  |

| Customizing     |  |  |
|-------|------|-----------------|
| Table | Table - Name | S/4HANA -Table and general Notes |
| C001 | Cust.Grp/MaterialGrp/AcctKey | FI-Accounting determination in SD for invoices. |
| NRIV | Number Range Intervals | Edit with transaction SNUM. |
|-----------------|--------------|


## Programs, Function Modules and Exits:

| Programs | Description | Type |
|-----------------|--------------|--------------|
| RVSCD100  | Display Document Changes | SD |
| RFDKLI20  |  SD, FI: Recreation of Credit Data after Organizational Changes  | SD |
|-----------------|--------------|--------------|

## Role-based Fiori Apps:

### Sales

- Event based Revenue Recognition
- Market Segments
- P&L
- Project WIP Details
- Projects
- Realignment Results (Profitability Analysis)
- Revenue Recognition for Projects
- Sales Orders

## Platforms:

|     ECC      |  S/4 HANA    |      U/X      |  Database     |
|--------------|--------------|---------------|---------------|
|   SAP ERP    | SAP S/4 HANA |  SAP FIORI    |  SAP HANA     |
|--------------|--------------|---------------|---------------|

Note: S/4 (cloud & on-premise) works only on Hana DB while SAP ERP is compatible with Hana DB, MS Sql, Oracle DB, IBM DB2 etc.
