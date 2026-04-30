# Title Information

## Scope

Title information is used to transcribe title information from the Instance. All the values in this component are literals.

## Folio / MARC

- 245 field, Title Statement
- 246 field, Varying Form of Title

## Title Information

There are three values for this component.

![Title information dropdown showing Instance title, Variant title, and Parallel title options](../images/page071_img01.png)

Instance title is the default value.

### Non-sort character count

This numerical value indicates initial words and marks of punctuation that are not to be considered in title searching. The Non-sort character count is identical to the MARC 245 Indicator 2 value.

![Instance title with Non-sort character count set to 4 and title "The Best of California"](../images/page071_img02.png)

![Instance title with Non-sort character count set to 5 and title 'The "winter mind"'](../images/page071_img03.png)

### Title

Transcribe the Title proper of the Instance in this field. Include initial articles and set the Non-sort character count to disregard the initial article in searching. This is a literal field. Do not use ISBD punctuation.

![Instance title with Non-sort character count 4 and title "The establishment and consolidation of imperial government in southern Nigeria, 1891-1904"](../images/page072_img01.png)

### Part number

If there is a part designation in the title, transcribe it here. Do not use ISBD punctuation.

![Instance title showing title "The digital photography book" with Part number "Part 5"](../images/page072_img02.png)

### Part name

If there is a part name in the title, transcribe it here. Do not use ISBD punctuation.

![Instance title showing title "The digital photography book", Part number "Part 5", and Part name "Photo recipes"](../images/page072_img03.png)

### Other title information

If there is other title information for the title, transcribe it here. Do not use ISBD punctuation.

![Instance title showing title "The digital photography book", Part number "Part 5", Part name "Photo recipes", and Other title information "the step-by-step secrets for how to make your photos look like the pros'!"](../images/page072_img04.png)

When there is Other title information in the instance title there will be a second option, "Send Subtitle to Work Variant" that will create a variant title in the work with the information

!["Send Subtitle to Work Variant" that will create a variant title in the work with the information](../images/image-1777565663355.png)

There can only be one Instance title. If you need to record a Parallel title or a Variant title, add a new Title component in the [Work description](../work-description/) and select the appropriate value. Parallel titles and Variant titles are recorded in the Work description. Titles that are dependent on a location, such as a Spine title or a Caption title, are recorded in the Instance description.

![Title information component with Add Another Component, Delete Component, and Send to Work action buttons](../images/page073_img01.png)

![Full example showing Instance title with Parallel title "Digitale Fotobuch" including Other title information, Part number "Teil 5", and Part name "Fotorezepte" in German](../images/page073_img02.png)

### Send Subtitle to Work Variant 

This feature allows you to send the subtitle from the Instance to the Work forcing it to copy over as a Variant Title.

Found in the action button:

![action button with Send Subtitle to Work Variant highlighted](../images/image-1772223551023.png)

Clicking this will copy any value in the Instance Subtitle, often labeled "Other title information" to the Work as a new component.

You can highlight a portion of Subtitle and this function will only send the highlighted portion to the work

![Animated image of using the Send Subtitle to Work Variant button](../images/weppysnap_4.webp)


### Date

Leave this field blank.

### Note

This is a literal field to show information about the title.

![Note field with value "Title from colophon"](../images/page073_img03.png)

To delete a component, select Delete Component.

![Title information component showing Additional Literal, Set Language, Russian S2R, Russian R2S, Debug, Add To Library, and View Documentation action button options](../images/page074_img01.png)

> **See also:** [Title Information: Best Practice for Non-Latin Titles](title-non-latin.md) for guidance on recording non-Latin script titles.

---

[Back to Table of Contents](../index.md)
