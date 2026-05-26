# Notes about the Instance

## Scope

**Notes in Marva are in flux. Most Notes will be recorded in the Instance description, not in the Work description. In Folio / MARC, each 5XX note has a specific definition. Being aware of the definition will help determine where the note goes, with the [Work description](../work-description/), or with the Instance description.**

Record Notes relating to the **language** of the Work in this component in Marva. All other notes are recorded in the Instance description.

## Folio / MARC

- 5XX fields, Note Fields
- 300 field, subfield $e, Accompanying material

## Note

Notes related to the RDA Manifestation are recorded here. In addition, notes about supplementary content of a resource such as the presence of bibliographical references and/or indexes are recorded here, even though in RDA, supplementary content is an Expression attribute (RDA 7.16). A controlled value for the presence of bibliographical references and/or indexes is recorded in the Work entity, in the Supplementary content component.

Note is a literal field. Notes are keyed in. Ending punctuation is optional.


![Note field with value "illustrations"](../images/image-1772568380061.png)

![Note field with value "Includes bibliographical references and index."](../images/image-1772568394947.png)

**Controlled values for the presence of bibliographical references and index are recorded in the BIBFRAME Work:

![Supplementary content component with value "bibliography" and another Supplementary content component with value "index"](../images/page092_img01.png)

![Note examples: "The research on which this paper was based was commissioned by the Consortium for Research on Educational Access, Transitions & Equity--T.p. verso.", "Copyright: University of Sussex.", and "Includes statistical tables."](../images/page092_img02.png)

## Note Type

Because MARC 5XX fields define the type of note being recorded, and Marva does not use MARC, Notes are categorized by selecting a value from the drop-down list. If the note is a General Note (General Notes are recorded in the MARC 500 field), do not select a value from the drop-down list. For all other notes, select a value.

![Notes about the Instance with Note "Includes bibliographical references (pages 91-93)" and Note type "bibliography"](../images/page092_img05.png)

![Note "color illustrations" with Note type "physical details"](../images/page092_img06.png)

![Notes about the Instance with Note "illustrations (some color)" and Note type "physical details"](../images/page092_img07.png)

![Note with issuing body information and Note type "issuing body (issuing)"](../images/page092_img08.png)

Notes that are all related to one of the Note type values may be recorded in the same component but in different fields.

![Notes about the Instance component with multiple notes sharing the same Note type, containing Note fields for research commissioning information, copyright, and statistical tables, with no Note type selected (General Note)](../images/page093_img01.png)

Notes that have a unique Note type value must appear in separate components.

![Notes about the Instance with Add Another Component action button highlighted, showing how to create additional note components](../images/page093_img02.png)

Accompanying material that is placed in the MARC 300 $e field is treated as a note on the Instance in Marva.

![Notes about the Instance component showing "1 audio disc (4 3/4 in.)" as the note text and "accompanying material" as the Note type.](../images/image-1779810365581.png)

---

[Back to Table of Contents](../index.md)
