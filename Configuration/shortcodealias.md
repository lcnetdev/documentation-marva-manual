# Shortcode Aliases

In simple lookup fields (like contributor role, or identifier status) you are able to set a value that will map to one of the list items.

For example in the Identifier ISBN component there is the invalid/canceled field that lets you set a status:
![image](../images/image-1787692072047.png)

But say you want to only have to enter the text "inv" or even just "i" into the field and press enter and it will add the "canceled or invalid (cancinv)" value.

To do this open the "Set Shortcode Alias" window from the action button in that field (Invalid/canceled?)

![image](../images/image-1787692228798.png)

It will open this pop-up:

![image](../images/image-1787692287937.png)

The Shortcode is the value you want to type in and hit enter, Map to is the value it will populate with. 

To setup my "i" -> "canceled or invalid (cancinv)" mapping it would look like this:

![image](../images/image-1787692409610.png)

Click Save it it will return to the editor, now when you "i" into the Invalid/canceled? field and hit enter it will populate "canceled or invalid (cancinv)"

![image](../images/shortcode-1787692918450.webp)

Open the shortcode alias pop-up again to remove mappings you don't want anymore.

The mappings are lookup specific and are saved in your preferences and will persist if you save/restore your preferences from file or DB.

  