# Work type

When MARC records are converted to BIBFRAME, the software combines byte 6 and 7 of the Leader and creates multiple Work types (rdf:type) These types were included in the BIBFRAME data and used to generate the applicable Leader bytes during the BIBFRAME-to-MARC conversion.

Now, these types can be viewed and edited within Marva.

The field will be automatically populated when a record is loaded into Marva, but it can be edited if necessary:
![Portion of a work template for a book, showing that Work type Monograph is checked and the MARC preview shows a value of "a" in the Leader, byte 6](../images/image-1791575520851.png)

Available Work types will vary according to the resource being cataloged:
![Portion of a work template for a film, showing that Work type Moving Image is checked and the MARC preview shows a value of "g" in the Leader, byte 6](../images/image-1791575807487.png)
![Portion of a work template for a map, showing that Work types Cartography and Manuscript are checked and the MARC preview shows a value of "f" in the Leader, byte 6](../images/image-1791575991306.png)

