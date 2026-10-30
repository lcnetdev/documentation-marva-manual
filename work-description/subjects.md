# Subjects

## Scope

This component is used for recording controlled access to subject content of the Work.

## Folio / MARC

- 600, 610, 611, 630, 650, and 651 fields, Subject Access Fields

## Subject Components

There are four values for this field. **Subject components** is the default value.

![Subjects drop-down showing Subject components, Geographic subjects, CYAC subject, Work as subject options](../images/page026_img02.png)

## Search LCSH/LCNAF

Assigning subjects can be a complex cataloging process in Marva since linking to authority records occurs in several ways. A complex LCSH string with a heading and one or more subdivisions might be linked to one authority record, if there is a corresponding LCSH authority record for the heading plus the subdivision(s). But because LCSH follows a free-floating subdivision practice, sometimes there is not an authority record for a complex string. In cases like this, each component of the string needs to be controlled as a separate component.

There are two ways to use Marva to input LCSH strings: **Build Mode** and **Link Mode**.

---

## Build Mode

### Search Options

There are a few options at the top of the search screen for different types of searches:
- LCSH/NAF - Any subject, name, or _non-geographic_ subdivision [`ctrl+alt+1`]
- Children's Subjects - Subjects and Children's subjects [`ctrl+alt+2`]
- Geo. Subdiv. - Only geographic subdivisions: hierarchical or not [`ctrl+alt+3`]
- Hubs - Search for hubs [`ctrl+alt+4`]

**Note:** You can use shortcuts to jump between search types. Shortcuts are in square brackets above.

**Note:** Appending a `?` at the end of the search will flip it to a keyword search. The search will be left anchored

### Search LCSH/LCNAF: Blackburn, Elizabeth H. (Elizabeth Helen), 1948-

Key in Blackburn, Elizabeth H. (Elizabeth Helen), 1948-.

![Subject Builder in Build Mode showing search for Blackburn with authority record preview](../images/image-1772569469371.png)

Marva will look up this name in both LCSH and in the LCNAF. Because this is a personal name, only the LCNAF values should be reviewed. If there is an authorized access point in the LCNAF for Blackburn, Elizabeth H. (Elizabeth Helen), 1948-, it will display in the search results in Marva. A view screen on the right-hand side of the screen can be used to view the complete authority record before assigning it.

Select the correct value and click on **Add [SHIFT+Enter]**. The authorized access point will be added as a Subject Added Entry - Personal Name in Marva. The thesaurus will be: Library of Congress subject headings.

![Subject component showing Blackburn linked with thesaurus "Library of Congress subject headings"](../images/page027_img02.png)

### Search LCSH/LCNAF: Biochemists--United States--Biography

Add a new Subject component.

![Lightning bolt menu showing Add Another Component option for Subjects](../images/page027_img03.png)

Key in **Biochemists--United States--Biography**. A pop-up box to the Subject Builder appears, with Biochemists and United States and Biography appearing in the search box, separated with double dashes (`--`). If the lookup can find a comprehensive URI for the string, it will display above the search box with (Auth Hd) at the end of the string. Click on the Auth Hd string, and the search box will show green highlighting, meaning that the entire string can be represented with a URI in the Subject component. Click on **Add [SHIFT+Enter]** to add the controlled string to the subject component. The thesaurus will be: Library of Congress subject headings.

In the case of **Biochemists--United States--Biography**, there is not a comprehensive URI for the entire string. The individual components of the string will need to be controlled as separate URIs.

![Subject Builder showing individual components of Biochemists--United States--Biography](../images/image-1772569672165.png)

1. Click in the box with the heading **Biochemists**. Marva will search for the URI for this individual component. Click on Biochemists (Auth Hd), then click on **Topic / Heading ($a $x)** beneath the search box.

2. Next click in the box with **United States**. Marva will search for the URI for this individual component. Because LCSH uses indirect geographic subdivision for most geographic entities, the search will look for the value that would appear in the MARC Authority File 781 field. In this case, because United States cannot be used indirectly as a geographic subdivision, the value United States is used both as the authorized access point, and the geographic subdivision form. Click on United States [LCNAF] (GeoSubDiv), then click on **Geographic ($z)** beneath the search box.

3. Do the same for **Biography** (GnFrm).

4. Click on **Add [SHIFT+Enter]**. The LCSH string will be added as a Subject Added Entry - Topical Term in Marva. The thesaurus will be: Library of Congress subject headings.

![Subject Builder showing Biography subdivision with Build Mode and Link Mode tabs](../images/image-1772569772681.png)

### Search Geo. Subdiv.: Social History--California

When building a heading with a geographic subdivision, you should search under `Geo. Subdiv.` All geographic subdivisions will appear under this option.

![Geographic search without Geo. Subdiv. selected](../images/image-1772569944620.png)

![Geographic search with Geo. Subdiv. selected](../images/image-1772569996879.png)

### Search LCSH/LCNAF: Telomere--History

Add a new Subject component.

Key in **Telomere--History**. A pop-up box to the Subject Builder appears, with Telomere and History appearing in the search box, separated with double dashes (`--`).

If the lookup can find a comprehensive URI for the string, it will display above the search box with (Auth Hd) at the end of the string. In the case of Telomere--History, there is not a comprehensive URI for the entire string. The individual components of the string will need to be controlled as separate URIs.

![Subject Builder showing History subdivision lookup with authority record detail](../images/image-1772570396197.png)

1. Click in the box with the heading **Telomere**. Marva will search for the URI for this individual component. Click on Telomere (Auth Hd), then click on **Topic / Heading ($a $x)** beneath the search box.

2. Next click in the box with **History**. Marva will search for the URI for this topical subdivision.

The components do not need to be controlled in order.

Click on History (SubDiv), then click on **Topic / Heading ($a $x)** beneath the search box.

Click on **Add [SHIFT+Enter]**. The LCSH string will be added as a Subject Added Entry - Topical Term in Marva. The thesaurus will be: Library of Congress subject headings.

![Three Subject components showing all completed subjects with thesaurus values](../images/page030_img02.png)

When searching a subject, adding `?` at the end of the word will perform a keyword search

![Adding ? at the end of the word will perform a keyword search](../images/Picture13.png)

### Symbols

There are a few symbols that can appear when adding a subject heading.


<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" height="24px" width="24px" fill="#000000"><path d="M12,17q0.43,0 0.71-0.29Q13,16.43 13,16t-0.29-0.71T12,15t-0.71,0.29T11,16t0.29,0.71T12,17Zm-1-4h2V7H11v6ZM8.25,21L3,15.75V8.25L8.25,3h7.5L21,8.25v7.5L15.75,21H8.25ZM9.1,19h5.8L19,14.9V9.1L14.9,5H9.1L5,9.1v5.8L9.1,19ZM12,12Z"/></svg> There heading doesn't have a link
![Stop sign with !: No links](../images/image-1793378787772.png)

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" height="24px" width="24px" fill="#000000"><path d="M8.6,22.5L6.7,19.3L3.1,18.5l0.35-3.7L1,12L3.45,9.2L3.1,5.5L6.7,4.7L8.6,1.5L12,2.95L15.4,1.5l1.9,3.2l3.6,0.8L20.55,9.2L23,12l-2.45,2.8l0.35,3.7l-3.6,0.8l-1.9,3.2L12,21.05L8.6,22.5Zm0.85-2.55L12,18.85l2.6,1.1l1.4-2.4l2.75-0.65L18.5,14.1L20.35,12L18.5,9.85l0.25-2.8L16,6.45l-1.45-2.4L12,5.15L9.4,4.05L8,6.45L5.25,7.05L5.5,9.85L3.65,12L5.5,14.1L5.25,16.95L8,17.55l1.45,2.4ZM12,12Zm-1.05,3.55L16.6,9.9L15.2,8.45L10.95,12.7L8.8,10.6L7.4,12l3.55,3.55Z"/></svg> there is one link for the entire heading
![Circle with chechmark: One link for everything](../images/image-1793378882926.png)

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" height="24px" width="24px" fill="#000000"><path d="M6.7,18L1.05,12.35l1.43-1.4L6.73,15.2l1.4,1.4L6.7,18Zm5.65,0L6.7,12.35l1.4-1.43l4.25,4.25l9.2-9.2l1.4,1.43L12.35,18Zm0-5.65l-1.43-1.4L15.88,6L17.3,7.4l-4.95,4.95Z"/></svg> there are multiple parts to the heading, each has a link
![Multiple checkmarks: Multiple parts everything has a link](../images/image-1793378897978.png)

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" height="24px" width="24px" fill="#000000"><path d="M1,21L12,2L23,21H1Zm3.45-2h15.1L12,6L4.45,19Zm8.26-1.29Q13,17.43 13,17t-0.29-0.71T12,16t-0.71,0.29T11,17t0.29,0.71T12,18t0.71-0.29ZM11,15h2V10H11v5Zm1-2.5Z"/></svg> there are multiple parts to the heading, not everything is linked. 
This can happen when the heading has a complex heading and a subdivision. If some part of the complex heading, doesn't have a URI, it will not be possible to link to it. The result is this symbol.
![Triangle with !: Multiple parts, some have links and some don't](../images/image-1793378921480.png)

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" height="24px" width="24px" fill="#000000"><path d="M12.84,17.64q0.36-0.36 0.36-0.89t-0.36-0.89T11.95,15.5t-0.89,0.36q-0.36,0.36-0.36,0.89t0.36,0.89T11.95,18t0.89-0.36Zm-1.79-3.49H12.9q0-0.82 0.19-1.3t1.06-1.3q0.65-0.65 1.03-1.24T15.55,8.9q0-1.4-1.03-2.15T12.1,6Q10.68,6 9.79,6.75T8.55,8.55L10.2,9.2q0.13-0.45 0.56-0.97T12.1,7.7q0.8,0 1.2,0.44T13.7,9.1q0,0.5-0.3,0.94t-0.75,0.81q-1.1,0.97-1.35,1.47t-0.25,1.82ZM12,22q-2.07,0-3.9-0.79q-1.82-0.79-3.17-2.14Q3.58,17.73 2.79,15.9T2,12Q2,9.92 2.79,8.1Q3.58,6.27 4.93,4.93Q6.28,3.57 8.1,2.79Q9.93,2 12,2t3.9,0.79t3.17,2.14q1.35,1.35 2.14,3.17Q22,9.92 22,12t-0.79,3.9t-2.14,3.17q-1.35,1.35-3.17,2.14T12,22Zm0-2q3.35,0 5.68-2.32T20,12T17.68,6.32T12,4T6.33,6.32T4,12t2.33,5.68T12,20Zm0-8Z"/></svg> there are multiple parts none have links
![Circle with ?: Multiple pieces no linls](../images/image-1793378941325.png)

---

## Link Mode

If you know MARC LCSH coding, you can use the Link Mode to assign LCSH strings in Marva.

Using the example Biochemists--United States--Biography, the MARC string is `$a Biochemists $z United States $v Biography`.

In a Subject component in Marva, key in `Biochemists $z United States $v Biography`. Include the subfield values and the dollar sign as the delimiter for the subdivisions, but not for the main heading (do not use subfield $a).

![Link Mode showing subject string with green check marks for each resolved component](../images/page031_img01.png)

Marva will search for the URIs for the individual components and identify them with green checks directly in the Subject component box. Using Link Mode, there is no need to search directly in Build Mode.

![Link Mode subject with all components verified with green checks](../images/page031_img02.png)

To change or edit information in the subject component, best practice is to delete the component that is not correct, and add a new component to search for the correct subject string.

---

## Using Literal Values as LCSH Subjects

There are some situations where you will need to select a literal value for an authorized LCSH subject heading. The first situation arises when you are dealing with what is called a "multiple" subdivision record.

A "multiple" subdivision is a subdivision in the subject authority file that incorporates bracketed terms, generally followed by the word *etc.* This device is used to suggest the creation of similar subdivisions under the heading in question. The presence of a multiple subdivision under a heading in the subject authority file automatically gives free-floating status to analogous subdivisions under the same heading, and, if the heading is a pattern heading, under those headings that it controls.

For example, **--Dictionaries--French, [Italian, etc.]** is a multiple subdivision record that can be used as a form subdivision under subjects. Any appropriate language can be used with --Dictionaries on a free-floating basis.

When using a multiple subdivision record as the basis for an LCSH subdivision in Marva, use the **Literal Value** to capture the correct subdivision.

![Subject Builder showing Romanian as a Literal value selection](../images/image-1772570623287.png)

Literal values are indicated with yellow backgrounds. It is also necessary to select at `type` before you will be able to add the heading. `Types` appear below the search bar.

![Subject component showing Biology--Dictionaries--Romanian as Partially Linked with MARC output](../images/page032_img02.png)

A second situation arises when you wish to insert a subject heading that is has not been published on an approved LCSH list yet. These headings can be added to the description by clicking the "Provisional" checkbox, and this setting also ensures that the MARC output will assign this heading a second indicator of "0".

![Subject search for American baseball with the provisional box checked and Topic/Heading highlighted](../images/image-1786473773069.png)

![Subject template showing American baseball as a provisional subject heading in Marva](../images/image-1786473419959.png)

---

## Hub as Subject

Works may be used as subject access points in bibliographic descriptions, following the instructions in the Subject Headings Manual (SHM):

| SHM Instruction | Topic |
|-----------------|-------|
| H1155_6 | Literary Works Entered Under Author |
| H1155_8 | Literary Works Entered Under Title |
| H1295 | Bible: Special Topics |
| H1300 | Bible and Other Sacred Works |
| H1435 | Commentaries on Individual Works |

Works will be represented by Hubs in BIBFRAME and in Marva. Always use the option **Hub as subject** when selecting a work as a subject access point.

![Subjects component with "Hub as subject" option selected and Search Hubs field](../images/page033_img01.png)

If you do not find the Hub that is needed:

1. If you would create a title or name-title authority record in the LC/NACO Authority File for the work, create a NAR in Folio and wait for the record to migrate to the Marva view of the LC/NACO Authority File. This should take 5 minutes. This option is generally followed when a work is needed for a subject entry and the work is not represented by a bibliographic record in the LC database (see DCM Z1, Introduction).

2. If you would not create a title or a name-title authority record in the LC/NACO Authority File for the expression, create a Hub in Marva.

![Lightning bolt menu showing Create Hub option for Hub as subject](../images/page033_img02.png)

See [Hubs](../Reference/e-hubs.md) for more information.

---

## LCSH Subject Proposals

If you need to submit an LCSH subject proposal, there will not be a link to use in Marva until the subject proposal is approved. Just as in MARC cataloging, you can add an access point in Marva for an LCSH heading that is being proposed. "Claim" the heading as a literal value and select **Library of Congress Subject Headings** as the Thesaurus.

![Subject Builder showing literal value for proposed heading "Regulatory arbitrage (Economics)"](../images/page033_img03.png)

---

## Classification Numbers

It is possible to add classification numbers from the subject search. See [Classification Numbers](work-description/classification-numbers.md) for details.

---

[Back to Table of Contents](../index.md)
