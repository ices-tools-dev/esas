---
title: Format
description: >
  Description of the file format to submit data.
permalink: /format/
---

To [submit data to ESAS](https://esas.ices.dk/manage/ScreenFile), data need to be provided in a specific file format.

## Description

The file format consists of concatenating records from the [5 tables]({{ '/tables/' | relative_url }}) of the data model into a single txt file. This enables data validation for a unit of related data.

- Rows should start with a `recordType` (`FI`, `EC`, `ES`, `EP`, `EO`) indicating the type of record. The example below is a file (`FI`) with one campaign (`EC`) and sample (`ES`), containing 2 positions (`EP`) and 17 observations (`EO`).
- The file should only have one `FI` record, limiting a file to data associated with the same data rights holder(s).
- Data in a row should be tab-delimited and have all columns in the correct order for that recordType.
- All records should be related. E.g. observation `1100031833` is related to position `110004709`, which in turn is part of sample `110000153` and campaign `110000153`.

## Example

```
FI	202	BE															
EC	110000153	Public	1996-02-28	1996-02-28													
ES	110000153	110000153	1996-02-28	11BE	30			300	1	TRUE	1	0|50|100|200|300	3		Platform: Belgica		
EP	110000153	110004708	07:05:00	51.1367	2.5267	0.70	0.21	4	C					0			
EP	110000153	110004709	07:09:00	51.1467	2.5333	2.14	0.64	4	C					0						
EO	110004708	1100031820		FALSE	ESAS	5920	  1	F	3								
EO	110004708	1100031821		FALSE	ESAS	5920	  2	F	A		B						
EO	110004708	1100031822		FALSE	ESAS	5920	  1	F	2								
EO	110004708	1100031823		FALSE	ESAS	5920	  1	F	2								
EO	110004709	1100031824	 1	FALSE	ESAS	2130	  2	A				F					
EO	110004709	1100031825	 1	FALSE	ESAS	2130	  5	A				M					
EO	110004709	1100031826		FALSE	ESAS	6340	  1	A			W						
EO	110004709	1100031827		FALSE	ESAS	6000	  1	F	2								
EO	110004709	1100031828		FALSE	ESAS	5900	  1	F	A		T						
EO	110004709	1100031829		FALSE	ESAS	  90	  1	A			W						
EO	110004709	1100031830		FALSE	ESAS	5920	  1	F	A		B						
EO	110004709	1100031831		FALSE	ESAS	5900	  1	F	A		T						
EO	110004709	1100031832		TRUE	ESAS	5920	  1	F	2								
EO	110004709	1100031833		FALSE	ESAS	5900	  1	F	A		W						
EO	110004709	1100031834		FALSE	ESAS	 710	  1	F	A								
EO	110004709	1100031835		FALSE	ESAS	2130	  8	F									
EO	110004709	1100031836		FALSE	ESAS	5900	  1	F	A		T						
```
