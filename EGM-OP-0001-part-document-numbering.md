# EGM-OP-0001 Part and Document Numbering
This document is an Operating Procedure (OP) for the OpenRelics Enigma project. It defines a standard for document and part numbering.

# Scope and terms
This numbering system applies to all documents in the project.

While the word *number* is used for the identifiers assigned under this system, they may contain non-numeric symbols in some fields.

The phrase *document number* is a general name for the identifiers assigned under this system. The phrases *part number*, *reference number*, etc. may be used when referring to different types of documents, for clarity.

# Number format
These rules apply to all document numbers.
1. Numbers shall begin with the project code EGM.
2. Numbers shall be unique within the Enigma project.
3. Numbers are case insensitive.
4. Numbers shall follow the format **EGM-TYPE-XXXX-DASH** where:
	* **TYPE** is one of the type codes defined in this document.
	* **XXXX** is a numeric code which is at least four digits long.
	* **DASH** is an optional [dash number](https://en.wikipedia.org/wiki/Part_number#Dash_numbers) whose format depends on the document.

## Type codes
Documents shall bear one of the following type codes:
* **PRT** for parts - 2D or 3D models and prints describing physical objects in Fusion 360, FreeCAD, etc.
* **ASM** for assemblies - 2D or 3D models and prints containing multiple parts.
* **SCH** for electrical schematics - Encompasses both traditional electrical schematics and wiring diagrams.
* **BRD** for circuit boards - Circuit board layout documents in KiCAD, EAGLE, etc.
* **BOM** for bill of materials documents - Lists of parts, assemblies, schematics and boards
* **REF** for references - All non-part and non-assembly documents containing knowledge. Includes original historical documents, documents containing interpretations of history, and 
* **OP** for operating procedures - Documents that define the way the project is run.

Example: this document is an OP. It has document number EGM-**OP**-0001.

## Numeric codes
There is no requirement that numeric codes carry meaning; they may be sequential or even random. It is recommended, however, that numeric codes be reserved in blocks for similar documents and, where possible, selected for memorable quality. Furthermore, when two documents with different type codes are closely related, they should share numeric codes if possible (e.g. a part and its associated drawing). 

## Dash numbers
The dash number suffix is an optional suffix of arbitrary length, with a format defined at component level. The typical use of dash numbers is to designate variations on a common item. For example, a whole family of screws may be designated:

EGM-PRT-0000-[A]X[B] where **[A]**=thread M2, M3, etc and **[B]**=length in mm

Where dash numbers are used, a document must exist which specifies the dash number format. Documents bearing dash numbers shall refer back to the associated specification if possible. The most common example of this is a part family and its associated BOM listing; if a part uses dash numbers, its associated BOM should include a column defining the dash number format.

# Type-specific rules
Certain document types are subject to special rules and requirements.

**PRT** and **ASM** documents shall be listed in a project-wide mechanical Bill of Materials (BOM) document. Note that PRT and ASM documents refer to designs as a whole, which typically comprise both 3D model files and print files. When a part or assembly has a single print (regardless of the number of sheets in the print) the model and print files may share a single document number. Dash numbers should be used for prints if a single part or assembly has multiple associated prints.

**SCH** and **BRD** documents shall be listed in a project-wide electrical Bill of Materials (BOM) document.

**BOM** documents shall be formatted as comma-separated tables whenever possible, for portability.

**REF** documents shall be listed in a project-wide reference list (itself considered a reference document). References may be internal or external; external references such as books and websites should still be assigned document numbers.
