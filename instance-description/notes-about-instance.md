# Notes about the Instance

## Scope

**Notes in Marva are in flux. Most Notes will be recorded in the Instance description, not in the Work description. In Folio / MARC, each 5XX note has a specific definition. Being aware of the definition will help determine where the note goes, with the [Work description](../work-description/), or with the Instance description.**

For now (February 2025), only record Notes relating to the **language** of the Work in this component in Marva. All other notes are recorded in the Instance description.

## Folio / MARC

- 5XX fields, Note Fields

## Note

Notes related to the RDA Manifestation are recorded here. In addition, notes about supplementary content of a resource such as the presence of bibliographical references and/or indexes are recorded here, even though in RDA, supplementary content is an Expression attribute (RDA 7.16). A controlled value for the presence of bibliographical references and/or indexes is recorded in the Work entity, in the Supplementary content component.

Note is a literal field. Notes are keyed in. Ending punctuation is optional.

![Note field with value "illustrations"](../images/page090_img01.png)

![Note field with value "Includes bibliographical references and index."](../images/page090_img02.png)

**Controlled values for the presence of bibliographical references and index are recorded in the BIBFRAME Work:

![Supplementary content component with value "bibliography" and another Supplementary content component with value "index"](../images/page091_img01.png)

![Note examples: "The research on which this paper was based was commissioned by the Consortium for Research on Educational Access, Transitions & Equity--T.p. verso.", "Copyright: University of Sussex.", and "Includes statistical tables."](../images/page091_img02.png)

## Note Type

Because MARC 5XX fields define the type of note being recorded, and Marva does not use MARC, Notes are categorized by selecting a value from the drop-down list. If the note is a General Note (General Notes are recorded in the MARC 500 field), do not select a value from the drop-down list. For all other notes, select a value.

![Notes about the Instance with Note "Includes bibliographical references (pages 91-93)" and Note type "bibliography"](../images/page091_img03.png)

![Note "color illustrations" with Note type "physical details"](../images/page092_img01.png)

![Notes about the Instance with Note "illustrations (some color)" and Note type "physical details"](../images/page092_img02.png)

![Note with issuing body information and Note type "issuing body (issuing)"](../images/page092_img03.png)

Notes that are all related to one of the Note type values may be recorded in the same component but in different fields.

![Notes about the Instance component with multiple notes sharing the same Note type, containing Note fields for research commissioning information, copyright, and statistical tables, with no Note type selected (General Note)](../images/page092_img04.png)

Notes that have a unique Note type value must appear in separate components.

![Example showing separate Notes about the Instance components: one with Note type "physical details" for "ill. (chiefly col.)", and another with multiple general notes and no Note type, plus a separate component with Note type "bibliography" for bibliographical references](../images/page092_img05.png)

![Notes about the Instance with Add Another Component action button highlighted, showing how to create additional note components](../images/page092_img06.png)

---

[Back to Table of Contents](../index.md)
