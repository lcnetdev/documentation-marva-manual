# Editing Authority Records Language 
## Non-Latin BCP47 & Variant Preferences

Marva has the ability to add and change certain language information related in authority records.

This is included as part of a PCC Task Group. The changes that can be made are to identify the BCP47 code
language and script of a non-Latin variant and specifying if a name is the preferred form in that language.

### Accessing
When looking up a name, if it has any non-Latin variants a button will appear next to the "Variants" section
in the record's details. 

![Name search with button to start editing](../images/image-1783452105055.png)

After clicking on this, the left side of the modal will change to a new interface.

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

### Deleting a Variant

If you need to remove an entire variant, delete everything from the input.

![Variant Ready to be deleted](../images/image-1783454368261.png)

### References Evaluatd

Near the bottom of the form is a checkbox to indicate if all of the non-Latin script references have been evaluated.
Checking this does 2 things:
1) Sets the 008/29 to a
2) Deletes any 667 that says the non-Latin references are unevaluated

## Submitting the Edit

Once all edits have been made, click the "Preview" button at the bottom of the form. This will perform validation and 
present a MARC preview of the edits.

![Finished record with "Preview" highlighted](../images/image-1783454745657.png)

![Preview of finished record with changes highlighted](../images/image-1783455077906.png)

### Validation
There's general validation that matches the NAR creation validation in Marva. In addition to that, the 
validation will fail if there are multiple preferred forms for a single language. Or, if something is marked 
preferred without have a BCP47 code.

![Validation error: Multiple preferred](../images/image-1783455207639.png)

![Validation error: Preferred form without BCP](../images/image-1783455408333.png)

If there are no validation errors, there will be a "Submit" button at the bottom.

![Submit Button](../images/image-1783455555755.png)