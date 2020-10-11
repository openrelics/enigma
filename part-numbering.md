# Part Numbering

This document is a part of the OpenRelics Enigma project. It defines the convention for part numbering.

## Scope and terms

This numbering system applies to all parts and assemblies in the project. It is intended to be simple but extensible.

While the word *number* is used for the identifiers assigned under this system, they may contain non-numeric symbols in some fields.

## Number format

All part numbers should:

1. Begin with the project code EGM.
2. Be unique within the Enigma project.
3. Be treated as case-insensitive.
4. Follow the format **EGM(-TYPE)-XXXX(-DASH)** where:
   * **TYPE** is an optional type code, as defined in this document.
   * **XXXX** is a numeric code which is at least four digits long.
   * **DASH** is an optional [dash number](https://en.wikipedia.org/wiki/Part_number#Dash_numbers) whose format depends on the document.

### Type codes

Documents should bear one of the following type codes:

* **No type code** for parts - 2D or 3D models and drawings describing physical objects in Fusion 360, FreeCAD, etc.
* **ASM** for assemblies - 2D or 3D models and drawings containing multiple parts.

### Numeric codes

There is no requirement that numeric codes carry meaning; they may be sequential or even random. It is preferred, however, that numeric codes be reserved in blocks for similar items and, where possible, selected for memorable quality.

### Dash numbers

The dash number suffix is an optional suffix of arbitrary length, with a format defined at component level. The typical use of dash numbers is to designate variations on a common item. For example, a whole family of screws may be designated:

EGM-PRT-0000-[A]X[B] where **[A]**=thread M2, M3, etc and **[B]**=length in mm

If a part uses dash numbers, its associated BOM should include a column defining the dash number format.

## Bill of Materials

Parts and assemblies shall be listed in a project-wide mechanical Bill of Materials (BOM) document. Note that part numbers refer to designs as a whole, which typically comprise both 3D model files and drawings. When a part or assembly has a single drawing (regardless of the number of sheets in the drawing) the model and drawing files may share a single part number. Dash numbers should be used to distinguish between drawings if a single part or assembly has multiple associated drawings. This situation should be avoided where possible.

## Examples

Example BOM listings for several parts are provided here. As this is not an official BOM listing, the Enigma project EGM- prefix has been replaced by PREFIX-.
| Part Number         | Description                           | Dash number rules |
|---------------------|---------------------------------------|-------------------|
| PREFIX-0003         | Bearing Block Right                   | None              |
| PREFIX-0026-[A]     | Letter insert, button head, glyph [A] | [A] = letter A-Z  |
| PREFIX-ASM-0101     | Assembly, letter                      | None              |
| PREFIX-ASM-0102-[A] | Assembly, button short, glyph [A]     | [A] = letter A-Z  |
