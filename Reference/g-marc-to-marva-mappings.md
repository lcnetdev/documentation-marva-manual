# MARC to Marva Mappings

This appendix provides a comprehensive mapping between MARC fields and their corresponding Marva components. Use this reference to understand how traditional MARC cataloging data translates into the BIBFRAME-based Marva editor.

## Marva Component Colors

In the original PDF, table cells are color-coded by Marva component type. Since Markdown cannot render cell background colors, the following legend indicates which color corresponds to each component area:

| Color | Component Area |
|-------|---------------|
| Blue tint | **Work** |
| Peach/salmon tint | **Instance** |
| Green tint | **Item** |
| Yellow tint | **Admin Metadata** |

In the tables below, the **Marva Component** column indicates which area each mapping belongs to (Work, Instance, Item, or Admin).

---

## Leader Values

| MARC Value | MARC Definition | Marva Component | Comments |
|------------|----------------|-----------------|----------|
| Ldr/05 | Record status | Admin: Status (new/changed/deleted) | This value should be pre-populated when a MARC bibliographic record from Folio is imported into Marva |
| Ldr/06 | Type of record | none | Determined by profile used in Marva |
| Ldr/07 | Bibliographic level | Instance: Mode of issuance | This is a drop-down list in Marva |
| Ldr/08 | Type of control | none | |
| Ldr/17 | Encoding level | Admin: Encoding level | This value should be pre-populated when a MARC bibliographic from Folio is imported into Marva |
| Ldr/18 | Descriptive cataloging form | Admin: Description conventions | This value should be pre-populated when a MARC bibliographic from Folio is imported into Marva |
| Ldr/19 | Multipart resource record level | none | |

---

## 008

| MARC Value | MARC Definition | Marva Component | Comments |
|------------|----------------|-----------------|----------|
| 008/06 | Type of date | none | Inferred from Instance: Provision activity: EDTF date (to/from 008) |
| 008/07-10 | Date 1 | Instance: Provision activity: EDTF date (to/from 008) | Enter single dates in Marva as in the 008/07-10 |
| 008/11-14 | Date 2 | Instance: Provision activity: EDTF date (to/from 008) | Enter multiple dates in Marva following the EDTF specification. EDTF date coding: YYYY for simple years (Example: 1925). YYYX to indicate unknown (currently 'u' is used; Example: 192X for 192u). YYYY/YYYY to indicate to/from ranges (Example: 1925/1935). YYYY/.. to indicate a range with a defined start date but no current end date (Example: 1925/.. for 1925- in the 264 or 19259999 in the 008). Note, EDTF syntax is two dots. Using the EDTF standard for recording dates will generate the correct 008/06 Type of date value |
| 008/15-17 | Place of publication | Instance: Provision activity: Search place of publication (to/from 008) | This is a long drop-down list in Marva just like the drop-down list in Folio for the MARC 008/15-17 |
| 008/18, 19, 20, 21 | Illustrations | Work: Illustrative content | This is a drop-down list in Marva just like the drop-down list in Folio for the MARC 008/18,19,20,21 |
| 008/22 | Target audience | Work: Intended audience | This is a drop-down list in Marva just like the drop-down list in Folio for the MARC 008/22 |
| 008/23 | Form of item | Instance: Media type | This is a drop-down list in Marva |
| 008/24,25,26,27 | Nature of contents | Work: Supplementary content; Work: Genre/Form | This is a drop-down list in Marva just like the drop-down list in Folio for the MARC 008/24,25,26,27, but the Marva drop-down list has more options. |
| 008/24,25,26,27 | Nature of contents: Bibliography | Work: Supplementary content | When a bibliography is present in a resource, **bibliography** is selected in Work: Supplementary content. This will populate the value "b" in one of the MARC 008/24,25,26,27 bytes in the Modern MARC record. When a 504 note would be recorded indicating the presence of a bibliography, with or without specific pagination, record this information as a textual note in the Instance description, Notes about the Instance, and select bibliography as the Note type. This will populate the 504 field in the Modern MARC record. |
| 008/28 | Government publication | Work: Government publication | This is a drop-down list in Marva just like the drop-down list in Folio for the MARC 008/28 |
| 008/29 | Conference publication | Work: Genre/Form | Use: Conference papers and proceedings |
| 008/30 | Festschrift | Work: Genre/Form | Use: Festschriften |
| 008/31 | Index | Work: Supplementary content | This is a drop-down list in Marva, not the option in Folio to select only the presence or the absence of an index. Select index from the drop-down list in Marva |
| 008/33 | Literary form | Work: Genre/Form | Use the appropriate heading from LCGFT |
| 008/34 | Biographical material | Work: Genre/Form | For 008/34 "a": Use: Autobiographies. For 008/34 "b" or "c": Use: Biographies. For 008/34 "d": Do not use an LCGFT heading. Add a Work: Notes about the Work: "Includes biographical information" and Note type biographical data |
| 008/35-37 | Language | Work: Language (008 [1st], 041 $a [others]) | This is a drop-down list in Marva just like the drop-down list in Folio for the MARC 008/35-37 |
| 008/38 | Modified record | none | |
| 008/39 | Cataloging source | none | |

---

## MARC Bibliographic Fields

| MARC Field | MARC Definition | Marva Component | Comments |
|------------|----------------|-----------------|----------|
| 906 | Local Processing Data | none | Recorded in Modern MARC record only |
| 925 | Local Selection Decision | none | Recorded in Modern MARC record only |
| 955 | Local Functional Identifying Information | none | Recorded in Modern MARC record only |
| 010 | Library of Congress Control Number | Instance: Identifiers: LCCN | Record the LCCN if not present. Remember leading spaces! The Invalid/canceled? field is a drop-down list |
| 020 | International Standard Book Number | Instance: Identifiers: ISBN | Record the ISBN. The qualifier is a literal value. Do not include parentheses. The Invalid/canceled? field is a drop-down list |
| 024 | Other Standard Identifier | Instance: Identifiers: Other identifier | Record Other identifier if appropriate. The qualifier is a literal value. Do not include parentheses. |
| 037 | Source of Acquisition | Instance: Identifiers: Acquisitions identifiers: Source of acquisition | This is a literal value in Marva just like in Folio. For example: Library of Congress -- Islamabad Overseas Office |
| 040 | Cataloging Source | Admin: Note | This is a recorded value that includes delimiter values to facilitate Modern MARC 040 field generation in Folio: `040  $aDLC$beng$cDLC$erda` |
| 041 | Language Code | Work: Language (008 [1st], 041 $a [others]) | This is a drop-down list to the MARC Language Code List. Use the appropriate value that you would select for the MARC 008/35-37 (see above MARC 008/35-37). If there is more than one primary language, repeat this component and add the other language values from the drop-down list |
| 042 | Authentication Code | Admin: Description authentication | This value should be pre-populated when a MARC bibliographic from Folio is imported into Marva |
| 043 | Geographic Area Code | Work: Geographic coverage | In Marva, this component uses the name of the place, not the Geographic Area Code (GAC). For example, Illinois, not n-us-il. But you can search by GAC as well as by name of the place. Searching by name of the place is a little easier because if you search using GAC, you will get all the place names that have that GAC in the 043 field of the authority record |
| 046 | Special Coded Dates | Work: Date of Work | This is a literal field. Use EDTF dates (just like in Folio). |
| 050 | Library of Congress Call Number | Work: Classification numbers: Library of Congress classification | |
| 051 | Library of Congress Copy, Issue, Offprint Statement | Item: Classification number | Used in Rare Materials profile |
| 082 | Dewey Decimal Classification Number | Work: Classification: Dewey Decimal classification | |
| 1XX | Main Entry Fields | Work: Creator of Work | Relationship designator required. Use the drop-down list. It is a MARC list, not an RDA list, but the MARC list is acceptable for RDA cataloging. |
| 240 | Uniform Title | Work: Expression of [search for a Hub] | All title and name-title NARs have been created as BIBFRAME Hubs. You should be able to find the expression authorized access point that is needed, using the Hub created from the title or name-title NAR. If there is not a Hub, you can create one directly in Marva. |
| 245 $a,$n,$p | Title Statement | Work: Title information: Work title | Work: Title information: Work title = RDA Preferred Title for Work, which does not include other title information, but does include Part name and/or Part title |
| 245 $a,$b,$n,$p,$c | Title Statement | Instance: Title information: Instance title | Instance: Title information: Instance title includes title proper and other title information |
| 246 | Varying Form of Title | Work: Title information: Variant title; Work: Title information: Parallel title | In Marva, variant titles and parallel titles are recorded in the Work description. |
| 250 | Edition Statement | Instance: Edition statement | |
| 260 | Publication, Distribution, etc. (Imprint) | Instance: Provision activity: Publication; Instance: Provision activity: Production; Instance: Provision activity: Distribution; Instance: Provision activity: Manufacture | Only found in older MARC records. Modern MARC records will only use 264 fields. MARC records with 260 fields will be converted to 264 fields when a Modern MARC record is generated |
| 264 | Production, Publication, Distribution, Manufacture, and Copyright Notice | Instance: Provision activity: Publication; Instance: Provision activity: Production; Instance: Provision activity: Distribution; Instance: Provision activity: Manufacture | If a resource has more than one element (Production, Publication, Distribution, Manufacture), repeat the Provision activity component to record the information. |
| 300 $a | Physical Description: Extent | Instance: Extent | |
| 300 $b | Physical Description: Other physical details | Work: Illustrative content | |
| 300 $c | Physical Description: Dimensions | Instance: Dimensions | |
| 336 | Content Type | Work: Content type | Added to all bibliographic records, including AACR2. |
| 337 | Media Type | Instance: Media type | Added to all bibliographic records, including AACR2. |
| 338 | Carrier Type | Instance: Carrier type | Added to all bibliographic records, including AACR2. |
| 490 | Series Statement | Work: Input transcribed series | |
| 500 | General Note | Instance: Notes about the Instance | |
| 504 | Bibliography, etc. Note | Instance: Notes about the Instance | When a 504 note would be recorded indicating the presence of a bibliography, with or without specific pagination, record this information as a textual note in the Instance description, Notes about the Instance, and select bibliography as the Note type. This will populate the 504 field in the Modern MARC record. When a bibliography is present in a resource, **bibliography** is selected in Work: Supplementary content. This will populate the value "b" in one of the MARC 008/24,25,26,27 bytes in the Modern MARC record. |
| 505 | Formatted Contents Note | Work: Contents | |
| 506 | Restrictions on Access Note | Instance: Access policy | Record as a literal value |
| 520 | Summary, etc. | Work: Summary | |
| 521 | Target Audience Note | Work: Intended audience | Record as uncontrolled term |
| 540 | Terms Governing Use and Reproduction Note | Instance: Access policy | Record as a literal value |
| 546 | Language Note | Work: Notes about the Work; Work: Script | Select note type **language** |
| 600,610,611,630,650,651 | Subject Access Fields | Work: Subjects | |
| 653 | Index Term-Uncontrolled | Work: Subjects | Uncontrolled index terms may be used in Marva as literal values. These terms will appear in Modern MARC records in the 653 field. Do not select a source in Marva when recording an uncontrolled index term. |
| 655 | Index Term - Genre/Form | Work: Genre/Form | |
| 700,710,711,730 | Added Entry Fields | Work: Contributors; Work: Search related work | |
| 720 | Added Entry-Uncontrolled Name | Work: Creator of Work; Work: Contributors | If there is not enough information available to create a name authority record for the agent, even a Provisional name authority record, the Literal value for the agent can be selected in the search modal. Do not create a NAR. The literal value will appear in the Modern MARC record in the 720 field. |
| 800,810,811,830 | Series Added Entry Fields | Work: Search series Hub (optional) | |
| 856 | Electronic Location and Access | Instance: Supplementary content URL | |
| 880 | Alternate Graphic Representation | Work: various | |
| 880 | Alternate Graphic Representation | Instance: various | |

---

[Back to Table of Contents](../index.md)
