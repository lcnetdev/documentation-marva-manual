# AutoDewey

AutoDewey will attempt to generate a DDC classification number from an LCC.

## Access

There are 2 ways to get to AutoDewey.
1) You can find it under "Tools" in the Nav bar. This will open an empty AutoDewey.
2) From the "Action Button" of the classification component. This will open AutoDewey with the LCC number added to the form.

![AutoDewey option under "Tools"](../images/image-1794948235702.png)

![AutoDewey option from "Action Button"](../images/image-1794948384449.png)

## Using AutoDewey

Once AutoDewey is open it needs to be provided with an LC Class Number. If you opened it from the action button, the LCC from that field will be added to the input.

![AutoDewey modal with LCC provided](../images/image-1794948588737.png)

With the LCC entered, select the genre that best matches the item you are trying to classify and then click "Create DDC."

![Suggested DDC numbers for LCC](../images/image-1794949182903.png)

If there's more than 1 possible match, you'll be presented with a list. After selecting one of the options, the right side will populate with details about the selection.

!["Textile arts" selected](../images/image-1794949308683.png)

The results shows:
1) LCC: Value used to match
2) LCC Range: possible range for this LCC
3) LCC Caption: label for the LCC
4) DDC: Generated DDC value
5) DDC Caption: Label for the DDC value

Clicking `Add to record` will generate a new classification component in Marva, populate it with the DDC value, and add the default values for DDC.

![Added DDC Value](../images/image-1794949444792.png)

## Periods

In some cases, more information is needed when creating the DDC. This can happen with literature class numbers where a time period is required.

![Period selection for literature number](../images/image-1794949881421.png)

The results shows:
1) mode: always 'autoDewey'
2) dewey: generated DDC
3) genre: selected genre
4) country: country for LCC
5) periods: possible periods for DDC

Select the period that matches the resource to change `dewey` into a real DDC value.

![Period selected and DDC provided](../images/image-1794950006254.png)

Click `Add to record` to add the DDC to the Marva record.