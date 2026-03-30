# Additional Instances and Secondary Instances

In Marva, you can add additional instances and create secondary instances for a record under the "Menu" option.
![Instance Creation Options](../images/image-1772122488622.png)

Additional Instances in Marva enable the cataloger to provide more detailed information about the Instance. For example: a book and an ebook. The same access information appears in the Work. One Instance describes the print book, and another Instance describes the ebook. An Additional Instance also has a unique LCCN.

Secondary Instances were created to solve a problem in MARC where a single MARC record contains information
about multiple resources. For example: a book with an accompanying DVD, a DVD with a CD, or a map with a link to a digitized image of the map. Secondary Instances in Marva provide minimal information that focuses on the technical
details of that Instance.

When should a cataloger create an Additional Instance or a Secondary Instance? It depends on the desired output
in MARC.

An Additional Instance will create two MARC records, or one for each LCCN. 

Using a Secondary Instance will create a single MARC record that uses $3 labels, along with multiple 007 and 3XX fields,  to differentiate between the resources.

---

[Back to Table of Contents](../index.md)