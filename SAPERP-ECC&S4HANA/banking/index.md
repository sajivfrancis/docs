# SAP BANKING

```
DOCS FOR SAP Banking

```

Commands:

```
SAP BANKING

```

## Process Modeling:

### LockBox

[![LockBox](Lockbox.png)](https://www.sap.com "SAP Banking")

### EBS

[![EBS](EBS.png)](https://www.sap.com "SAP Banking")

## SAP Best Practices Banking Account Structure:

<iframe src="https://drive.google.com/file/d/1uq93Nx6a44LNf8cn4C0kKrI9BtzVm8ty/preview" width="640" height="480"></iframe>

## Tables:

| Table | Name | S/4HANA - Notes |
|-------|------|-----------------|
| BNKA | Bank master record | In Logical Database BANK. |
| KNBK | Customer Master (Bank Details) | In Logical Database BRF DDF. |
| LFBK | Vendor Master (Bank Details) | In Logical Database BRF KDF. |
| TCURF | Conversion Factors |  |
| TCURR | Exchange Rates |  |
| TIBAN | IBAN | In Logical Database IBAN. |
| T001B | Permitted Posting Periods |  |
| T012 | House Banks |  |
| T012K | House Bank Accounts |  |
| T012C | Terms for bank transactions |
| T012D | Parameter for DME's and foreign PM |
| T012E | EDI-compatible house banks/PM |
| T012K | House Bank Accounts |
| T012T | House Bank Account Names |
| T012O | ORBIAN Detail: Bank Accounts |
| BANK_PACK_PARAMS | Application-Specific Parameters for Package Templates |
| BANK_PP_PARAMS | Application-Specific Global Parameters |
| BANK_PP_PAR_PCR | Parameters for Package Generation |
| BANK_PP_RUNPARM | Global Parameters for Mass Run |
|-----------------|--------------------------------|

## Programs, Function Modules and Exits:

| Programs | Description | Type |
|-----------------|--------------|--------------|
| SAPFPAYM  |  Payment Medium: Creation  | Banking |
| RFCHKE00  |  Check Extract Creation  | Banking |
| SAPFPAYM_SCHEDULE  |  Payment Medium: Scheduling of Creation  | Banking |
| RFBLBC00  |  Bank Chains for House Banks  | Banking |
| RFBLBC01  |  Bank chains for bank account carry forwards  | Banking |
| RFBLBC02  |  Bank chains for creditors/debtors  | Banking |
| SAPFPAYM_MERGE  |  Creation of Cross-Payment Run Payment Media  | Banking |
| RFCCSSTT  |  Payment Cards: Execute Settlement  | Banking |
| RFCHKL00  |  List of Checks for Company Code &0..  | Banking |
| RFCHKN10  |  Check Register  | Banking |
| RFCHKD30  |  Reset Check Information Data  | Banking |
| RFMPAY00  |  Status of Payments for Cross-Payment Run Payment Media  | Banking |
| OFX_MSG_SELECT_DISPLAY  |  Display Internet Messages  | Banking |
| RFCHKD00  |  Delete Check Information on Payment Run  | Banking |
| RFCHKD10  |  Delete Check Information on Voided Checks  | Banking |
| RFFOD__L | Payment Medium Workbench | PMW |
| RFFOD__S | Payment Medium Workbench | PMW |
| RFFOUS_T | Payment Medium Workbench | PMW |
| RFFOM200 | Payment Medium Workbench | PMW |
| RFFOM202 | Payment Medium Workbench | PMW |
| RFFOM210 | Payment Medium Workbench | PMW |
|----------|--------------------------|-----|

## Platforms:

|     ECC      |  S/4 HANA    |      U/X      |  Database     |
|--------------|--------------|---------------|---------------|
|   SAP ERP    | SAP S/4 HANA |  SAP FIORI    |  SAP HANA     |
|--------------|--------------|---------------|---------------|

Note: S/4 (cloud & on-premise) works only on Hana DB while SAP ERP is compatible with Hana DB, MS Sql, Oracle DB, IBM DB2 etc.


## EBS PROCESS:
<iframe src="https://drive.google.com/file/d/1p7NXjlpvlglWnm4-rur00JCASCL-AJNk/preview" width="640" height="480"></iframe>

## BAI2 FILE FORMAT:
<iframe src="https://drive.google.com/file/d/0B-TzAlgXPGrTSFRHT0hLd2dIVlk/preview" width="640" height="480"></iframe>

## APP PAYMENT PROGRAM:
<iframe src="https://drive.google.com/file/d/1zHXwuSIEOo400o-bjqqlxVwffOUGMatt/preview" width="640" height="480"></iframe>
