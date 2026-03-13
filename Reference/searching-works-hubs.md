## Searching Related Works and Hubs

In MARC cataloging, we never really had to think about the difference between a Work that was represented by an authority record in the LC/NACO Authority File, and a Work that was added as a Related Work access point in a bibliographic record. Works were works in the MARC world. There were situations where you knew you were required to create an authority record for a Work -- for example, if you had a translation, and there was a creator involved with the original Work, you would create a name-title authority record for the translation so you could trace a variant access point from the translated title. Only an authority record could express that relationship in a structured way.

Or you might create a title or name-title authority record to assist with collocation, to provide structure to areas in the catalog that had a lot of resources. Entries like Shakespeare's works or Beethoven's symphonies. A title or name-title authority record would help organize the catalog in these dense areas.

When the Library traced series, you would create a series authority record (a SAR) for the series. A series is a Work. For SARs, there are not often creators associated with the series, so the SAR would represent only a title.

Many times, you would want to give a 7XX Related work access point, and as long as the Library has that related work in its collections, you would not create an authority record for the Work.

In a past practice, a date of publication was added to analytical access points in subfield $f. Still, an authority record for the title or name-title might not exist, since the Library held the work in its catalog. Other things might be added to analytical access points for Works in the catalog, too, such as content type, version, etc.

This strange world of having some Works represented by authority records, and some Works represented only by access points in the bibliographic catalog, was something we were used to and we could work with it.

Then BIBFRAME and Marva came along.

What we had been used to in the past now was thrown into a new light.

BIBFRAME likes having actionable URIs for data. You could argue that an authority record for a Work can have an actionable URI, or an Work access point in a bibliographic description could have an actionable URI, but in order to bring some organization to Marva, there needed to be a new way to identify titles and name-titles: **Hubs** and **Works**.

In general terms, you might want to think about the difference between a **Hub** and a **Work** this way:

A **Hub** is most likely derived from a title or name-title NAR or SAR in the LC/NACO Authority File. That means that translations, controlled series titles, titles or name titles that are used to provide order in dense areas of the catalog, are all going to be represented as BIBFRAME Hubs.

A **Work** is most likely derived from an access point for a title or name-title in the catalog. There probably will not be an authority record in the LC/NACO Authority File for these Works. But these Works will include all the additional elements that have been added based on older cataloging practices -- dates, content type, editor surnames, publisher names, etc.

That is why there are two categories of searches in the Related works component in Marva: Hubs and Works. Using MARC tagging helps to understand the difference between Hubs and Works. In the Search related work component in Marva:

- if you are linking to a Work that would appear in a MARC 700, 710, 711, or 730 field (an **Added Entry**), use the **Hub** lookup
- if you are linking to a Work *and an Instance* that would appear in a MARC 76X-78X field (a **Linking Entry**), use the **Work** lookup
