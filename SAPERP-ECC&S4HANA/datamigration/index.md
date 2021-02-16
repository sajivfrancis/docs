# DATA MIGRATION IN S4HANA:

1. Migrate using files
2. Migrate using staging Tables
3. Migrate directly from SAP System

[![DataMigration](datamigration.png)](https://www.sap.com/ "DataMigration")

## S4HANA - Migration Cockpit

<iframe src="https://drive.google.com/file/d/1OVSFp00m7xyZl7xYMRd8u-ybw7eOy8Jo/preview" width="640" height="480"></iframe>

## ECC - LSMW 

<iframe src="https://drive.google.com/file/d/1ZxSxLDjQhFWUdzwUEwicOgod1yYK1w1G/preview" width="640" height="480"></iframe>

## IDOCS

### IDOC Structure

- Control Record: The administration part which has the type of idoc, message type, the current status, the sender, receiver etc.

    - All control record data is stored in EDIDC table. The key to this table is the IDOC Number
    - It contains information like IDOC number, the direction(inbound/outbound),  sender, recipient information, channel it is using, which port it is using etc.
    - Direction '1' indicates outbound, '2' indicates inbound.

- Data Record: The application data record which contains the data, these are called the data records/segments.

    - Data record contains application data like employee header info, weekly details, client details etc
    - All data record data is stored in EDID2 to EDID4 tables and EDIDD is a structure where you can see its components.
    - It contains data like the idoc number, name and number of the segment in the idoc, the hierarchy and the data
    - The actual data is stored as a string in a field called SDATA, which is a 1000 char long field.

- Status Record: Gives you information about the various stages the idoc has passed through.
    - Status record is attached to an I-DOC at every milestone or when it encounter errors.
    - All status record data is stored in EDIDS table.
    - Statuses 1-42 are for outbound while 50-75 for inbound.

### IDOCS - Outbound Process

- Create segments(WE31)
- Create an idoc type(WE30)
- Create a message type (WE81)
- Associate a message type to idoc type(WE82)
- Create a port(WE21)
- If you are going to use the message control method to trigger idocs then create the function module for creating the idoc and associate the function module to an outbound process code
- If not, create the function module or stand-alone program which will create the idoc
- Create a partner profile(WE20) with the necessary information in the outbound parameters for the partner you want to exchange the idoc with to trigger the idoc.

### IDOCS - Inbound Process

- Creation of basic Idoc type (Transaction WE30)
- Creating message type (Transaction WE81)
- Associating the Message type to basic Idoc type (Transaction WE82)
- Create the function module for processing the idoc
- Define the function module characteristics (BD51)
- Allocate the inbound function module to the message type(WE57)
- Defining process code (Transaction WE42)
- Creation of partner profile (Transaction WE20)

### IDOC Configuration Guide

<iframe src="https://drive.google.com/file/d/1O-Uh_wjZBnCd_7jR963xP8SQrnmNO1fn/preview" width="640" height="480"></iframe>

## BAPI's

BAPIs are defined in the  BOR(Business object repository) as methods of SAP business object types that carry out specific business functions.They  are implemented as RFC-enabled function modules and are created in the Function Builder of the ABAP Workbench - SW01.



### List of Standardized BAPIs:

- BAPIs for Reading Data - GetList() , GetDetail() , GetStatus() , ExistenceCheck().
- BAPIs for Creating or Changing Data- Create() ,Change(),Delete() and Undelete().
- BAPIs for Mass Processing -ChangeMultiple(), CreateMultiple(), DeleteMultiple().