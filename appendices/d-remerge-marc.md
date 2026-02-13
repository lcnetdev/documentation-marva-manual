# Appendix D: Instructions for Determining When to Re-Merge a Modern MARC Record Due to Missing or Modified Information

Modern MARC records contain URIs for a significant portion of the data, with most of these URIs generated at the Work level. The exceptions to this are the 334 field (Mode of Issuance), 337 field (Media Type) and 338 field (Carrier Type), which are at the Instance level and generate URIs.

If a cataloger identifies that a field was overlooked or requires modification after a record has been merged, it is essential to determine whether the change should be made in Marva Editor or Folio.

Below are the guidelines for when to edit the record in Marva Editor and when edits can be made directly in Folio.

## General Guidelines

If the field contains a URI (Uniform Resource Identifier) and needs modification or has been missed:

- Go back to Marva Editor to retrieve the record and make the necessary changes, as URIs must be generated at the Work and/or Instance levels.
- After editing in Marva Editor, save, validate, and post the record, and then merge it into Folio.

**Important Fields to Retain:**

- **985** (Local Notes)
  - When a merge occurs, a duplicate of the 985 field will be created. Retain the earlier 985 field as it serves as a history marker.
- **040** (Cataloging Source)
  - When a merge occurs, the 040 field will add extra subfield $d DLC-MRC $d DLC. These subfields must be retained and not deleted.

If the field does NOT contain a URI, the cataloger can modify the field directly in Folio, without needing to return to Marva Editor. Please add $d DLC and boat it. The Modern Marc is the record of truth. If you update this Modern Marc record, it should reflect the changes in Marva.

## Fields That Contain URIs (Must Be Edited in Marva Editor)

The following fields, if modified or missed, require editing in Marva Editor to regenerate the appropriate URIs.

| Field | BIBFRAME |
|-------|----------|
| **043** (Geographic Area Code) | **Work Level** -- URI is assigned to the Geographic Area. |
| **100** (Main Entry--Personal Name) | **Work Level** |
| **110** (Main Entry--Corporate Name) | A URI for the relator code 'author' is added. Also, two URIs are assigned for the Real World Object (RWO) and for an identifier for the agent. Both points to the name authority record for the agent. |
| **111** (Main Entry--Meeting Name) | |
| **130** (Uniform Title) | **Work Level** -- URI is linked to the BIBFRAME Hub |
| **240** (Uniform Title--Alternative Title) | **Work Level** -- URI is linked to the BIBFRAME Hub |
| **334** (Mode of Issuance) | **Instance Level** -- New usage in MARC record, with URI generated |
| **336** (Content Type) | **Work Level** -- URI is generated |
| **337** (Media Type) | **Instance Level** -- URI is generated |
| **338** (Carrier Type) | **Instance Level** -- URI is generated |
| **340** (Physical Medium) | **Work Level** -- A new usage in the MARC record, with the URI added. This data is recorded in other controlled areas, such as the 008 byte. |

**340 Examples:**

```text
$p Illustrations $0
http://id.loc.gov/vocabulary/millus/ill
$p maps $0 http://id.loc.gov/vocabulary/millus/map
$p Facsimiles $0
http://id.loc.gov/vocabulary/millus/fac
$g color (mul) $0
http://id.loc.gov/vocabulary/mcolor/mul
```

| Field | BIBFRAME |
|-------|----------|
| **353** (Supplementary Content Characteristics) | A new usage in the MARC record, with the URI added. This data is recorded in other controlled areas, such as the 008 byte. |

**353 Examples:**

```text
$a bibliography $b bibliography $0
http://id.loc.gov/vocabulary/msupplcont/bibliography
$a index $b index $0
http://id.loc.gov/vocabulary/msupplcont/index
```

| Field | BIBFRAME |
|-------|----------|
| **6XX** (Authorized Subject Headings Strings) | **Work Level** -- URIs are generated for LCSH strings under authority control. If the string uses a free-floating subdivision array not under authority control, no URI will be generated. |
| All **LCGFT** (Library of Congress Genre/Form Terms) headings | **Work Level** -- have URIs, as LCGFT does not use free-floating subdivisions. |
| **700, 710, 711, 730** | **Work Level** -- URIs are generated for 7XX |

## Additional Notes

Please be aware that if the cataloger has missed including **color illustrations, maps** this information must be added at the Work level (mapping 008 fixed) as well as "color" to generate the appropriate URI in the 340 field. Additionally, the cataloger should include **color illustrations, maps** at the Instance level in the "Notes about the Instance" with Note Type: Physical details.

For another example, if a bibliographical reference is missing, the cataloger must add it at the Work level (mapping 008 fixed), which will generate the URI in the 353 field and include it at the Instance level in the 'Notes about the Instance' as 'Includes bibliographical references' with the 'Note type': bibliography.

---

[Back to Table of Contents](../index.md)
