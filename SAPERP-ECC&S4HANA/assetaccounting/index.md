# SAP ASSET ACCOUNTING

```
DOCS FOR SAP AA

```

Commands:

```
SAP ASSET ACCOUNTING

```

## Process Modeling:

### Asset Procurement from PO:

[![AssetProcurementfromPO](AssetProcurementfromPO.png)](https://www.sap.com "SAP")

### Asset Valuation:

[![AAValuation](AAValuation.png)](https://www.sap.com "SAP")

### Asset Retirement:

[![AARetirement](AARetirement.png)](https://www.sap.com "SAP")

### Asset Month End Close:

[![AAMonthEndClose](AAMonthEndClose.png)](https://www.sap.com "SAP")

### Asset Year End Close:

[![AAYearEndClose](AAYearEndClose.png)](https://www.sap.com "SAP")

## SAP Best Practices Assets Account Structure:

<iframe src="https://drive.google.com/file/d/1UoPi7b4V4DZ8Q2PszBaGwZfN9D5MuHFx/preview" width="640" height="480"></iframe>

## Tables:

| Table | Name | S/4HANA - Notes |
|-------|------|-----------------|
| ANLA | Asset Master Record Segment |  |
| ANLB | Depreciation terms | In Logical Database ADA. |
| ANLI | Link table for investment measure -> AuC |  |
| ANLT | Asset Texts |  |
| ANLU | Asset Master Record: User Fields |  |
| ANLZ | Asset Allocations | Acc. Assign. for DEP, Gain/Loss from asset sales - Logical Database ADA |
| T087 | Evaluation groups |  |
| ANEA | Asset Line Items for Proportional Values |  |
| ANEK | Document Header Asset Posting | In Logical Database ADA. |
| ANEP | Asset Line Items |  |
| ANLC | Asset Value Fields |  |
| ANLH | Main asset number |  |
| ANLP | Asset Periodic Values | In Logical Database ADA. |
| ANLW | Insurable values (year dependent) |  |
| ANLX | Asset Master Record Segment |  |
| BKPF | Accounting Document Header | In Logical Database BMM BRF BRM DDF KDF SDF. |
| BSEG | Accounting Document Segment | In Logical Database BMM BRF BRM DDF KDF SDF. |
| TABA | Depreciation posting documents | Current status of depreciation and amortization. |
| VBKPF | Document Header for Document Parking |  |
| VBSEGA | Document Segment for Document Parking - Asset Database |  |
| BSEG_ADD | Entry View of Accounting Document | When the document is not relevant for the leading ledger. |
| FAGLFLEXA | General Ledger: Items |  |
| FAGLFLEXP | General Ledger: Plan Line Items |  |
| FAGLFLEXT | General Ledger: Totals |  |
| ACDOCA | Universal Journal Entry Line Items |  |
| ACDOCC | Consolidation Journal |  |
| ACDOCP | Plan Data Line Items |  |
| FAAT_DOC_IT | Statistical Line Item in Asset Accounting |  |
| FAAT_PLAN_VALUES | Planned Depreciations and Revaluations |  |
| FAAT_YDDA | Year-Dependent Attributes for Depreciation |  |
| T001B | Permitted Posting Periods |  |
| T093 | Real and derived depreciation areas |  |
| T093A | Real depreciation area |  |
| T093B | Company code-related depreciation area specifications | Closed Asset-fiscal year. S/4:Edit with transaction FAA_CMP. |
| T093C | Company codes in Asset Accounting | Fiscal year change. |
| T093D | Control dep. posting | Depriciation. |
| T096 | Chart of depreciation |  |
| ANKA | Asset classes: general data |  |
| ANKB | Asset class: depreciation area |  |
| ANKT | Asset classes: Description |  |
| NRIV | Number Range Intervals | Edit with transaction SNUM. Object=ANLANR for assets |
| T003 | Document Types | Document Types AA, AP und AF for Asset Accounting. |
| T082A | Field string asset master record maintenance |  |
| T082B | Field groups assets definition |  |
| T082G | Field strings for screen selection asset master data |  |
| T082L | Summary of logical field groups |  |
| T082T | Names For Field Groups |  |
| T087 | Evaluation groups |  |
| T090NA | Depreciation Keys |  |
| T090NAZ | Depreciation Keys - Method Assignment |  |
| T090NP | Period Control Method |  |
| T090NR | Base Method |  |
| T095 | Balance sheet accounts for depreciation areas |  |
| T095B | G/L accounts value adjustment |  |
| T095P | Reconcil.accts. derived dep. areas |  |
| TABW | Asset transaction types |  |
| TABWA | Transaction types/dep. areas |  |
| TABWT | Asset transaction types texts |  |
|-------|------|-----------------|

## Transactions:

| ECC Tr. | S4 Tr. | Description |
|-------------------|-------------------|-------------|
| ABST | ABSTL | Asset reconciliation
| AB01 | AB01L | Create asset transaction |
| ABAA | ABAAL | Unplanned depreciation |
| ABAKN | ABAKNL | Last Retirement on Group Asset |
| ABAO | ABAOL | Asset Sale Without Customer |
| ABAV | ABAVL | Asset Retirement by Scrapping |
| ABAW | ABAWL | Balance sheet revaluation |
| ABCO | ABCOL | Adjustment Posting to Areas |
| ABGF | ABGFL | Credit Memo in Year after Invoice |
| ABGL | ABGLL | Enter Credit Memo in Year of Invoice |
| ABIF | ABIFL | Investment support |
| ABMA | ABMAL | Manual depreciation |
| ABMR | ABMRL | Manual transfer of reserves |
| ABNA | ABNAL | Post-capitalization |
| ABNE | ABNEL | Subsequent Revenue |
| ABNK | ABNKL | Subsequent Costs |
| ABSO | ABSOL | Miscellaneous Transactions |
| ABUM | ABUML | Transfer From |
| ABZE | ABZEL | Acquisition from in-house production |
| ABZO | ABZOL | Asset acquis. autom. offset. posting |
| ABZP | ABZPL | Acquistion from affiliated company |
| ABZU | ABZUL | Write-up |
|-----------------|--------------|--------------|

## Programs, Function Modules and Exits:

| Programs | Description | Type |
|-----------------|--------------|--------------|
| AW01N  |  Asset Explorer  | AA |
| RAPOST2000  |  Depreciation Posting Run  | AA |
| RAALTD01  |  Legacy Data Transfer Program   Asset Accounting | AA |
| SAPMA01B  |  ?…  | AA |
| RACSTABL  |  Asset Customizing: Calling Up Different Views  | AA |
| RAVCLUST  |  FI-AA: Call of view clusters  | AA |
| RAFABNEW  |  Automatic Opening of a New Depreciation Area  | AA |
| RABEST_ALV01  |  Asset Balances  | AA |
| RAUMFE20  |  Analysis of an asset and its environment: Data collect. and analysis  | AA |
| RAALTD11  |  Direct Data Import   Asset Accounting | AA |
| RAAFAR00  |  Recalculate Depreciation  | AA |
| RASIMU02  |  Depreciation Simulation  | AA |
| RAPERB2000  |  Periodic Asset Postings  | AA |
| RAGITT_ALV01  |  Asset History Sheet  | AA |
| RAGITT01 | Asset History Sheet | S_ALR_87011990 |
| RAUNVA00  |  Incomplete Assets   Detail List | AA |
|-----------------|--------------|--------------|

## Role-based Fiori Apps:

- Asset Balances (Design Studio)
- Asset History Sheet (Design Studio)
- Asset Transactions
- Depreciation Lists
- Manage Fixed Assets

## Platforms:

|     ECC      |  S/4 HANA    |      U/X      |  Database     |
|--------------|--------------|---------------|---------------|
|   SAP ERP    | SAP S/4 HANA |  SAP FIORI    |  SAP HANA     |
|--------------|--------------|---------------|---------------|

Note: S/4 (cloud & on-premise) works only on Hana DB while SAP ERP is compatible with Hana DB, MS Sql, Oracle DB, IBM DB2 etc.


## Asset Accounting Doc:

<iframe src="https://drive.google.com/file/d/1rtlNXu7i9L31XH0JMgmO5brxa6SrrQ9J/preview" width="640" height="480"></iframe>
