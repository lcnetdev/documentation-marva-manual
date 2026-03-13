# Hubs

BIBFRAME Hubs, Work Hubs, or Hubs, are **collocation** and **aggregation** resources.

Hubs are not necessarily bibliographic entities on their own. Hubs are a means to organize resources. Hubs will not contain all the descriptive or subject metadata that you would expect to find in a bibliographic description.

The importance of Hubs as **collocation** and **aggregation** resources cannot be overstated. *Resource Description & Access*, RDA, takes an entirely different approach to work and expression access points. In RDA, disambiguation of work and expression access points is tied to identification. In RDA, work and expression access points are meant to **disambiguate**, not collocate or aggregate.

For this reason, you will notice that Hubs are very lightweight in the amount of information they contain. Hubs are intended to be lithe and flexible, serving as a means to group like things together.

There are four components in the Marva Work entity that use Hubs:

- Expression of [search for a Hub]
- Subjects --> Hub as subject
- Search series Hub (optional)
- Search related work

---

## Sources for Hubs

Hubs are created from MARC Authority and Bibliographic data, and may also be created in Marva.

From the LC/NACO Authority File (the NAF), Hubs are generated from:

- **Title NARs**
  - *130 #0 $a Experiments for the young scientist*
    (a series authority record)
  - *130 #0 $a Writing revolution*
    (title for a resource that is a compilation)
- **Name-Title NARs**
  - *100 1# $a Faulkner, William, $d 1897-1962. $t Short stories. $k Selections*
    (a collective authorized access point)
  - *100 1# $a Atwood, Margaret, $d 1939- $t Handmaid's tale. $l Chinese $s (Chen : Simplified)*
    (a fully disambiguated RDA expression authorized access point)

From the Folio bibliographic database, Hubs are generated from:

- **MARC 130**
  - *130 0# $a Annual report (Guam Agricultural Experiment Station)*
    (corporate body added to differentiate the title Annual report)
- **MARC 100/110/111 + 240**
  - *110 2# $a Food and Agriculture Organization of the United Nations*
    *240 10 $a Manual of methods for fisheries resource survey and appraisal. $l French*
    (a French translation of a resource published by the FAO)
- **MARC 600/610/611 + $t**
  - *611 2# $a Conference on Security and Cooperation in Europe $d (1972-1975 : $c Helsinki, Finland). $t Final Act*
    (a resource about the Helsinki Accords)
- **MARC 630**
  - *630 00 $a Dayton Peace Accords $d (1995)*
    (a resource about the 1995 Dayton Peace Accords)
- **MARC 700/710/711 + $t**
  - *700 12 $a Queen, Ellery. $t Roman Hat mystery*
    *(analytical added entry)*
- **MARC 730**
  - *730 02 $a Origo mundi. $l English*
    (an English translation of Origo mundi that is included in a parallel language edition)

---

## Technical Discussion of Hubs from the Network Development and MARC Standards Office

### Hubs Revisited

One can approach Bibframe Hubs from a theoretical perspective, i.e. one that references principles of library and information science theory, or from a practical perspective, perhaps by describing how they relate to current MARC practice.

### Collocation

The latter is often marginally more successful. Hubs are the functional Bibframe equivalent of MARC Title and Name-Title Authorities (1XX+$t or 130), Main Entry and/or Uniform Title combinations (1XX+240, 130) in the MARC Bibliographic format, or Access Points (6XX+$t, 630, 7XX+$t, 730, 8XX+$t, 830) in the MARC Bibliographic format. Although Name-Title and Title Authority records in MARC have some form of distinct identity, by virtue of being individually identified records in the LC/NACO file, Main Entries plus Uniform Titles and Access Points in MARC bibliographic records are handled purely as strings, even though there has been a way to record the identifier of any related Authority record since 2008. Sometimes the Main Entries, Uniform Titles, and Access Points in MARC bibliographic records correspond with an entry in the LC/NACO file, but sometimes they do not. It is possible to determine a match, or not, by taking the subfield-concatenated string in the bibliographic record and comparing it against the LC/NACO file. Easily one third of the Main Entries, Uniform Titles, and Access Points in the Library of Congress bibliographic file are not represented by a MARC Authority record in the LC/NACO file. (It may be closer to 50%.)

The carefully constructed strings in MARC Title and Name-Title authorities -- indeed, the reason behind developing an authority file more generally - and Main Entries plus Uniform Titles and Access Points in MARC bibliographic records have traditionally been used for collocation. In physical card catalogs and later online systems, these strings made it possible to cluster information items. Current Library of Congress cataloging policies and use of these headings facilitate collocation.

### Identifiers as Strings

The focus, thus far, has been on how these carefully constructed lexical strings, composed, minimally, of a normalized form of a name (if appropriate) and a normalized form of the title, function in MARC, where much of the functionality these headings enable is based on string matching or viewing browse lists of these strings. The strings are the identifiers.

### Strings to URI Identifiers

But Bibframe is a data format that uses pure identifiers (URIs, ...), not lexical strings, to identify resources. The string is secondary. In the simplest of explanations, the strings used in MARC were wrapped in a resource called a Hub and then the Hub given an identifier, an HTTP URI.

An example, in RDF/XML, of one these resources:

```xml
<bf:Hub rdf:about="http://id.loc.gov/resources/hubs/4978c720-ca4f-ca86-2d7e-a15f8245ade9">

  <bflc:aap>Homer. Odyssey. English</bflc:aap>

  <bf:title>
    <bf:Title>
      <bf:mainTitle>Odyssey. English</bf:mainTitle>
    </bf:Title>
  </bf:title>

  <bf:contribution>
    <bf:Contribution>
      <rdf:type rdf:resource="http://id.loc.gov/ontologies/bibframe/PrimaryContribution"/>
      <bf:agent rdf:resource="http://id.loc.gov/rwo/agents/n78095639"/>
      <bf:role rdf:resource="http://id.loc.gov/vocabulary/relators/ctb"/>
    </bf:Contribution>
  </bf:contribution>

  <bf:language rdf:resource="http://id.loc.gov/vocabulary/languages/eng"/>

</bf:Hub>
```

Although the creator (Homer), title (Odyssey), and language (English) have been broken into distinct elements and identifiers, URIs, added for creator and language, the AAP (short for Authorized Access Point) near the top retains the carefully constructed string used in MARC cataloging. Although this example has been pruned of a few variant titles and a few notes for the sake of succinctness, Hubs are designed to be fairly lightweight. They are an essential component of the ecosystem, but not the main focus of the cataloger's attention, nor of the user.

In Bibframe, since this Hub has an identifier, it is possible to link to the Hub (and it is also possible to link the Hub to other resources). With all of the potential incoming and outgoing links, the Hub functions very much as its name implies -- it is a Hub with many spokes connected to other resources. And it is therefore also possible to aggregate all the versions of Homer's Odyssey in English in precisely the way the controlled string functions in MARC. This is why Hubs have always been described as aggregators and why they functionally serve the same collocation purpose of the Title and NameTitle Authorities, Main Entries plus Uniform Titles, and Access Points in MARC.

### Hub as Collocator

The act of taking what is commonly conceived of as a string in MARC and making it into a 'resource,' or 'entity,' with a new identity and name seems to be a common stumbling point. In MARC cataloging culture, a name/title access point found in a 700 is a string created using specific rules and designed to collocate resources in a browse display or via searching. But looking more deeply, that carefully crafted string represents an abstract bibliographic resource/entity, regardless of whether the string relates to an authority record in the LC/NACO file or whether it was merely added in a bibliographic description based on cataloger judgment. "Homer's Odyssey in English" is a concept, a bibliographic one, and it is abstracted from any known, specific expression or manifestation. It does not matter if, in MARC, the cataloger enters "Homer. Odyssey. English" in a 700 or if, in Bibframe, a cataloger creates a relationship to the Hub presenting Homer's Odyssey in English, in both situations the cataloger is making a reference to an abstracted bibliographic concept with the intent that this Thing being cataloged should in some way collocate, with other similar resources, under the abstract idea thought of as "Homer's Odyssey in English."

### Identifier as Collocator

Having introduced the notion that Hubs, like access points, represent an abstract bibliographic concept/resource/entity, it is not clear how much deeper into information theory one must delve to sufficiently describe Hubs and their relationship to traditional cataloging, but it is worth viewing the above in light of Elaine Svenonius's 2000 publication The Intellectual Foundation of Information Organization. Quoting Svenonius at length about what she describes as "Work Identifiers (Work IDs)" is illuminating:

> From the point of view of collocation the most important metadata used in bibliographic description are work identifiers. How to construct work IDs is a problem that has claimed the attention of some of the best minds in cataloging and one that has been misunderstood by many. Normally, the AACR author-title language identifies authored works using expressions consisting of the normalized name of the author followed by the normalized title of the work. Where a work has no obvious author, its ID is its normalized title. Work identifiers were introduced in the nineteenth century in the form of main entries... (95)

She is, of course, describing the name/title pair found in Title and Name/Title authority records, main entries plus uniform titles, and access points. Notably, lest we apply today's concept of 'identifier,' it is worth underscoring how it is the resulting string from the normalized name/title combination that is the identifier. And she opens with the notion of collocation and notes the importance of these work identifiers. All of this perfectly aligns with how these strings have been used in bibliographic description in a MARC environment.

### Sets as Organizing Tool

Earlier in Intellectual Foundation, Svenonius introduces the notion of 'sets,' with sections about 'work sets' and 'author sets' and 'subject sets,' etc. She also introduces the idea of a 'superworks set' ("A superwork may contain any number of works as subsets, the members of which while not sharing essentially the same information content are nevertheless similar by virtue of emanating from the same ur-work" (38)) and ended with a section for "other entities." In short, she introduced the concept of "set theory," which has its roots in mathematics, to bibliographic description. From Stanford's Encyclopedia of Philosophy: "Set theory is the mathematical theory of well-determined collections, called sets, of objects that are called members, or elements, of the set." Svenonius explored how taking attributes of documents, for example, such as author and title to determine work sets or whether something is a revision or abridgement of a work to determine edition sets. Although Hubs do not relate in any specific way to any of the sets Svenonius identified, they certainly have commonalities with 'work sets' and 'superwork sets' and the 'entity sets.' But her description of a work set, in light of Hubs, is worth quoting in full:

> The forming of work sets constitutes the prototypical act of information organization. It is the act that collects in one place all documents that contain the same information, that systematically integrates each new documented into a database, and that transforms the database from a simple finding tool to a sophisticated bibliographic tool. In structuring a database, work sets are used to perform two essential functions: to organize displays and to provide nodes for linking related bibliographic entities. (36)

To suggest this is about Hubs is anachronistic and wrong, and it is immaterial whether Hubs better align with Svenonius's notion of work or superwork or simply entity, but it is nigh impossible to take her description of a 'work set' and not view our Hubs as being a set of collected, related bibliographic resources ("nodes for linking related bibliographic entities") that can be used to organize displays/information.

Ultimately, Svenonius is not talking about RDF and RDF Resources and triples -- her notions are largely grounded in the practice of using strings for identity -- but it is hard not to see how in Bibframe we are not conforming to her ideas for information organization.

### Hubs as Work Aggregators

Hubs as aggregators have become essential in the system, mostly as nodes between related bibliographic entities. They perform the historical function of collocation that are the rationale behind the traditional Title and NameTitle Authorities, Main Entries plus Uniform Titles, and Access Points in MARC.

### Expression Noise

But performing the functions of effective aggregation and collocation have been increasingly challenged in the last five years because of the introduction of, and growth in number of, ever more expression-specific headings. These expression-specific headings are permitted by RDA cataloging rules and some in the community exercise this option vigorously. A few examples of these expression specific headings:

```text
100 1# $a Bronte, Charlotte, $d 1816-1855. $t Jane Eyre. $l Spanish $s (Gomez Aquino)
100 0# $a Euripides. $t Medea. $l English $s (Way). $f 1894
100 0# $a Euripides. $t Medea. $l English $s (Way). $f 1912
100 0# $a Euripides. $t Medea. $l Greek $s (Paley). $f 1872
100 0# $a Homer. $t Odyssey. $l English $s (Rieu, Rieu, and Jones). Spoken word (Blagden)
100 0#  $a Homer. $t Odyssey (Findaway World, LLC). $l English. $h Spoken word $s (Findaway World, LLC)
```

The names seen in these authorized access points are somewhat ambiguous; they may reflect the editor, translator, narrator or producer. Regardless, they are added, as are the dates, to disambiguate the RDA expression from anything else in the file and to ensure the resulting string, mainly to be used in MARC bibliographic descriptions, is unique. This is the very opposite of facilitating collocation. Indeed, some headings are so unique that it is hard to see how, for example, "Euripides. Medea. English (Way). 1912" they will collocate anything other than the 1912 Way-translated version of Euripides's Medea. Compare the headings Library of Congress catalogers would use:

```text
100 1# $a Bronte, Charlotte, $d 1816-1855. $t Jane Eyre. $l Spanish
100 0# $a Euripides. $t Medea. $l English
100 0# $a Euripides. $t Medea. $l Greek
100 0# $a Homer. $t Odyssey. $l English
100 0# $a Homer. $t Odyssey. $l English. $h Spoken word
```

Stripped of the most expression specificity, it is readily clear how any of the above headings will group similar resources together. Want to find all the resources of Bronte's Jane Eyre in Spanish? Check. All the audio versions of Homer's Odyssey in English? Check.

From a practical perspective, these exceedingly expression-specific authorized access points create noise in the system. We have had tens of thousands of Hubs, maybe hundreds of thousands, that do not link to anything in LC's collection. This is to be expected, of course, since the Library does not hold a copy of every title represented in the LC/NACO file, but current policy is not to use these expression-specific forms in bibliographic description. For example, if an LC cataloger had to create a 700 reference for Euripides's Medea in Greek, the cataloger would enter "700 0  $aEuripides.$tMedea.$lGreek," and no additional version or date information. Since these expression-specific Hubs appear in the typeaheads and suggest services in Marva, catalogers must sift through this noise to identify the appropriate Hub to use. This increasing noise comes with a cost, and a lack of purpose.

### Hubs as Aggregators Now

Recent changes to the Hub file at ID have been made to better streamline the Hub file with an eye to emphasizing its purpose as a work aggregator for end users:

1. No longer are all LC/NACO Title or Name-Title authorities converted automatically to Hubs.
   - a. If the Authority 1XX contains a $f (date of work), the NAR is not converted.
   - b. If the Authority 1XX contains a $k and there is something in parentheses in the $k, the NAR is not converted.
2. If the Authority 1XX has a $s (version), the $s subfields are stripped and the NAR is converted.
3. The same logic applies when bibliographic records are processed (Main Entry and/or Uniform Title combinations (1xx+240, 130) or Access Points (6XX+$t, 630, 7XX+$t, 730, 8XX+$t, 830)).
4. We have not modified the conversion, but we strip the $f and $s subfields and then look for a Hub match. If one is found, that Hub is used.
5. We have deleted most of the Hubs that were originally derived from MARC records with $f and $s subfields.
   - a. We have only deleted Hubs that match this criteria and \*do not\* link to anything in the system.

These changes have collectively made aggregation/collocation the focus of Hubs by eliminating the overly expression-specific Hubs from the system. Prior to this change, the blind conversion of Title and Name/Title authorities to Hubs created undo confusion and noise, not only in our system but also amongst catalogers.

---

[Back to Table of Contents](../index.md)
