# Editing Authority Records Language 
## Non-Latin BCP47 & Variant Preferences

Marva has the ability to add and change certain language information related in authority records.

This is included as part of a PCC Task Group. The changes that can be made are to identify the BCP47 code
language and script of a non-Latin variant and specifying if a name is the preferred form in that language.

### Accessing
When looking up a name, a button will appear next to the "Variants" section in the record's details. If the record has no variants, there will be a button under "Extra Details."

![Name search with button to start editing](../images/image-1783452105055.png)

![Editing button for record with no variants](../images/image-1786555228523.png)

After clicking on this, Marva will check if it needs to sync with FOLIO. While it's syncing there will be a small indication to the right of the the button. This can take a second or two. 

![Record syncing with FOLIO](../images/bcp_sync.gif)

When the sync is finished the left side of the modal will change to a new interface.

![BCP47 Edit Form](../images/image-1783452250754.png)

The new screen pulls together all of the non-Latin variants for the record. 

### Adding BCP47 code to $7

Clicking on any of the inputs will populate a list of possible BCP47 codes beneath the names. A green border will appear around the name. This
will be the name that will receive changes.

![BCP47 options](../images/image-1783452358060.png)

Each option has a BCP47 code, language, and a score. The BCP47 code is the value that will populate the $7 if selected.
The score is an attempt to determine which code is most relevant to selected name.

To add a code, click on it. It will be highlighted blue and the $7 will be added to the input for that variant.

![BCP47 Code for Hebrew selected](../images/image-1783452579525.png)

A single name can have multiple code attached to it. Each will get it's own $7.

![Name with 3 BCP codes](../images/image-1783452643949.png)

To remove a name, click it again in the table and the $7 for that will be removed.

![Name after one code was removed.](../images/image-1783452771909.png)

> **NOTE**: If none of the options match the desired BCP47 code, you can click on a code and edit it, or add the entire code manually.

![Edited BCP47 code](../images/image-1783453092568.png)

### Preferred Form

To the left of each input is a grey button that reads "Pref" selecting this will mark that name as the preferred form
of the name. Doing this will flip the button to green and change the indicators. The first indicator of the 430 will change
to 1, for all other 4XX names the second indicator will change 1.

![Variant marked as preferred](../images/image-1783453426841.png)

Each language can only have 1 preferred form.

### Other Edits

Edits can be made in the input field. You can edit a subdivision, add a subdivision, or delete a subdivision.

![Variants with different edits](../images/image-1783453740744.png)

> **NOTE**: If the 1XX has a $d, there will be a button to the right of the input that will allow you to add that $d to a variant.

![Add date button](../images/image-1783453916262.png)

### Adding a Variant

There are 2 ways to add a variant. 
1) There's copy button next to each input that will create a copy of that name below the existing names.

![Copied Name](../images/image-1783454176288.png)

2) "Add Variant" button at the button of the variants.

![Add Variant Button](../images/image-1783454226229.png)

When a variant is added from either method, an input for the 670 will appear toward the bottom of the form. Deleting an added 4XX will remove the last 670 note.

![670 for variant](../images/image-1786555542354.png)

You can remove the field with the delete button to the right of the input. If the field is left with only `$a` or it is deleted, the 670 will not be added to the MARC record. 

### Deleting a Variant

If you need to remove an entire variant, delete everything from the input.

![Variant Ready to be deleted](../images/image-1783454368261.png)

### All References Evaluated

Near the bottom of the form is a checkbox to indicate if all of the non-Latin script references have been evaluated.
> Checking this does 2 things:
> 1) Sets the 008/29 to "a"
> 2) Deletes any 667 that says the non-Latin references are unevaluated

> **NOTE Partial Evaluation**
> Marva will compare the number of variants that have BCP codes with the total number of variants, if the number of total variants is greater than the number of evaluated variants a 670 will be added stating " Non-Latin script variants with (bcp47) in subfield 7 have been evaluated. Others have not yet been evaluated."

![Note for partial evaluation.](../images/image-1786043076712.png)

### All References Justified

There's also a checkbox to say whether or not all the references have justification. There's a note in some records `667   $a Machine-derived non-Latin script reference project.` Which says that some variant was created for this project and indicate that a variant might not have justification. 

Checking the box, will remove the note from the NAR. In cases where the NAR has been edited to provide justification for all names.

![All References Justified](../images/image-1786994451411.png)

## Submitting the Edit

Once all edits have been made, click the "Preview" button at the bottom of the form. This will perform validation and present a MARC preview of the edits.

>**Record should have the following changes:**
>- Leader/05 = `c`
>- Add 670 note for the test
>- `$7` added to appropriate 4XXs
>- 4XX indicators show when one is preferred
>- 008/29 = `a`, **if** "All References Evaluated" is checked
>- Remove 667 note: "Non-Latin scripts references not evaluated."
>- Add 667 note: " Non-Latin script variants with (bcp47) in subfield 7 have been evaluated. Others have not yet been evaluated.." **If** "all" is not checked and Marva detects that there are some 4XXs without `$7`

![Finished record with "Preview" highlighted](../images/image-1783454745657.png)

![Preview of finished record with changes highlighted and annotated](../images/image-1784642529147.png)

### Validation
There's general validation that matches the NAR creation validation in Marva. In addition to that, the 
validation will fail if there are multiple preferred forms for a single language. Or, if something is marked 
preferred without have a BCP47 code.

![Validation error: Multiple preferred](../images/image-1783455207639.png)

![Validation error: Preferred form without BCP](../images/image-1784642617073.png)

If there are no validation errors, there will be a "Submit" button at the bottom.

![Submit Button](../images/image-1784642713905.png)

---

## BCP Status

When searching for a name in Marva, variants will have BCP47 information represented by an icon (🗣️) to the right of the variant.

The color of the icon represents it's status:
- Green: Preferred Form with BCP code
- Gray: there's a BCP code, not marked preferred. *[BCP code is likely system generated.]*
- Red: There's a BCP code with an undefined language `und-` *[BCP code is system generated.]*

**If there is no green icon, there has been no BCP work on the name.**

Hovering over the icon will show the BCP information.

![Gray and Red icons](../images/image-1787677794678.png)

![Green icon with hover information](../images/image-1787677928358.png)

> **NOTE**: The information isn't a perfect 1-to-1. If there are multiple forms of the name in the same script, only 1 will be shown. For example if there's a preferred name in `hani` and an unpreferred form in `hani`, only the preferred form of the name will have the information. As in the image above with the middle column.
> Additionally, the hover information may not match exactly. The information being displayed is based on what's in ID and there might be differences to what's in the MARC. For example, if a BCP code would only be the language because the script is implied, the ID information may add the script. So `ko` would display as `ko-hang`. This is a cosmetic difference.

---

# PCC Testing a& Feedback

There are some pieces of this workflow that are related to the PCC's testing and feedback collection for preferred variants & BCP codes.

## Testing Note
Every record that goes through this process will have a 667 note added to it. That note is 
> Non-Latin script variants with (bcp47) in subfield 7 are for PCC testing. Please do not remove or edit 4XX fields that contain subfield 7.

There may be references in this documentation to older forms of that note. The note has gone through many revisions

## Feedback

There is an opportunity to provide feedback about difficulties in determining which form should be preferred or which BCP code to use with a variant.

If everything went smoothly and there are no question or issues, there is no need to provide feedback.

Feedback can be given by pressing the button next to preview. It will take you to a Microsoft Forms survey. We try to populate the form with as much information as we can.

![Feedback Button](../images/image-1786042527364.png)

## PCC Flagged NARs

There are a number of NARs that the PCC Task Group has identified as wanting feedback on. If you are working on one of these records Marva will present a message and hide the "Submit" button until the feedback form has been opened.

![image](../images/image-1786042751979.png)

---
