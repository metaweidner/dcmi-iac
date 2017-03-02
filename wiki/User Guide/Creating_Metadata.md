---
layout: page
title: Creating Metadata
---

- Contributor: Stefanie Rühle 
- Contributer: Tom Baker 
- Contributor: Pete Johnston

Go to [User Guide](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide "User Guide") | [Publishing Metadata](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata "User Guide/Publishing Metadata")

| 

## Contents

- 1 About the examples
- 2 Titles
  - 2.1 Title
  - 2.2 Alternative
  - 2.3 Guidelines for the creation of title content
- 3 Relationships between Resource and Agents
  - 3.1 Using agent properties in Dublin Core
  - 3.2 Contributor
  - 3.3 Creator
  - 3.4 Publisher
  - 3.5 RightsHolder
  - 3.6 Guidelines for the creation of content for agents
- 4 Type
  - 4.1 Guidelines for the creation of type content
- 5 Format
  - 5.1 Guidelines for the creation of format content
- 6 Extent
  - 6.1 Guidelines for the creation of extent content
- 7 Medium
  - 7.1 Guidelines for the creation of medium content
- 8 Language
  - 8.1 Guidelines for the creation of language content
- 9 Identifiers
  - 9.1 Identifier
  - 9.2 BibliographicCitation
  - 9.3 Guidelines for the creation of identifier content
- 10 Descriptions
  - 10.1 Description
  - 10.2 Abstract
  - 10.3 TableOfContent
  - 10.4 Guidelines for the creation of descriptions
- 11 Subject
  - 11.1 Guidelines for describing the subject of a resource
- 12 Coverage
  - 12.1 Coverage
  - 12.2 Temporal
  - 12.3 Spatial
  - 12.4 Guidelines for describing the coverage, spatial or temporal character of a resource
- 13 Dates
  - 13.1 Date
  - 13.2 Created
  - 13.3 Issued
  - 13.4 Available
  - 13.5 Modified
  - 13.6 Valid
  - 13.7 DateCopyrighted
  - 13.8 DateSubmitted
  - 13.9 DateAccepted
  - 13.10 Guidelines for the creation of content for dates
- 14 Source and Relations
  - 14.1 Relation
  - 14.2 Source
  - 14.3 IsPartOf
  - 14.4 HasPart
  - 14.5 IsVersionOf
  - 14.6 HasVersion
  - 14.7 IsFormatOf
  - 14.8 HasFormat
  - 14.9 Replaces
  - 14.10 IsReplacedBy
  - 14.11 Requires
  - 14.12 IsRequiredBy
  - 14.13 References
  - 14.14 IsReferencedBy
  - 14.15 ConformsTo
  - 14.16 Guidelines for the creation of content for relations and source
- 15 Rights
  - 15.1 Rights
  - 15.2 AccessRights
  - 15.3 License
  - 15.4 Guidelines for the creation of rights content
- 16 Special properties for the description of education material
  - 16.1 Audience
  - 16.2 Mediator
  - 16.3 EducationLevel
  - 16.4 InsctructionalMethod
  - 16.5 Guidelines for the creation of content for properties describing education material
- 17 Special properties for the description of collections
  - 17.1 AccrualMethod
  - 17.2 AccrualPeriodicity
  - 17.3 AccrualPolicy
  - 17.4 Guidelines for the creation of content for properties describing collections
- 18 Provenance
  - 18.1 Guidelines for the creation of content for provenance
 |

**How to create content for DCMI Metadata**

# About the examples 

We are presenting the examples in tables. To interpret these tables please consider that:

- **yellow rows** are standing for statements describing a resource,
- **white rows** are standing for statements describing a resource that is the value of another statement but is not described by another record,
- **bold** strings are standing for properties,
- **italicized** strings are standing for values,
- **red strings** are standing for values linking to records.

example (see turtle explanation)

# Titles 

## [Title](http://dublincore.org/documents/dcmi-terms/#terms-title) 

Title is a property that refers to the name or names by which a resource is formally known.

## [Alternative](http://dublincore.org/documents/dcmi-terms/#terms-alternative) 

Alternative is a property that refers to a name or names of a resource used as a substitute or alternative to the formal title. These are secondary titles, abbreviations, translations of a title, etc.

## Guidelines for the creation of title content 

For the title use the name given to the resource.

| **title** | _Alvar Aalto Chair No. 66_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTit3 "User Guide/Publishing Metadata")

In most databases title is one of the main criteria to identify search results. So **if there is no formal title resp. name** you should formulate an adequate one by yourself.

| **title** | _Data from a survey about the usage of metadata_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTit6 "User Guide/Publishing Metadata")

If there is **more than one title resp. name** you should repeat the title property

| **title** | _Autumn Leaves_ |
| **title** | _The Dead Leaves_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTit4 "User Guide/Publishing Metadata")

or use the alternative property.

Typically alternative is used for **secondary titles** ,

| **title** | _Passion for Pulses_ |
| **alternative** | _A Feast of Beans, Peas and Lentils from Around the World_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exAlt1 "User Guide/Publishing Metadata")

or for **abbreviations**.

| **title** | _American Meteorological Association Newsletter_ |
| **alternative** | _AMA Newsletter_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exAlt2 "User Guide/Publishing Metadata")

If the title resp. name is expressed in **different languages** you should use language tags.

| **title** | _La Joconde_ | fre |
| **title** | _Mona Lisa_ | eng |
| **title** | _La Gioconda_ | ita |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTit5 "User Guide/Publishing Metadata")

the same is true for alternative

| **title** | _EU Stability Programm of Belgium_ | eng |
| **alternative** | _Council Opinion on the Updated Stability Programm of Belgium 2009 - 2010_ | eng |
| **alternative** | _Stellungnahme des Rates zum aktualisierten Stabilitätsprogramm Belgiens für 2009 - 2012_ | ger |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exAlt3 "User Guide/Publishing Metadata")

It is recommended to describe titles with plain text (as done in the examples above). But sometimes it is necessary to **create a relationship between the described resource and a more detailed title description**.

This should be used to refer to **a title with different transliterations** ,

| **title** | | |
| | **in greek** | _Οιδίπους Τύραννος_ |
| | **in latin** | _Oidipous Tyrannos_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTit1 "User Guide/Publishing Metadata")

or to refer to a **title authority**.

| **title** | _Nibelungenlied Handschrift B_ |
| **title** | _[nibelungenlied](http://metaweidner.github.io/dcmi-iac/wiki?title=Nibelungenlied&action=edit&redlink=1 "Nibelungenlied (page does not exist)")_ |

| **title** | _Nibelungenlied Handschrift C_ |
| **title** | _[nibelungenlied](http://metaweidner.github.io/dcmi-iac/wiki?title=Nibelungenlied&action=edit&redlink=1 "Nibelungenlied (page does not exist)")_ |

| **identifier** | _[nibelungenlied](http://metaweidner.github.io/dcmi-iac/wiki?title=Nibelungenlied&action=edit&redlink=1 "Nibelungenlied (page does not exist)")_ |
| **label** | _Der Nibelunge Not_ |
| **alternative label** | _Nibelungenlied_ |
| **alternative label** | _Nibelungenklage_ |
| **alternative label** | _Nibelungensage_ |
| **description** | _The Nibelungenlied exists of 39 aventiuren created between 1180 and 1210_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTit2 "User Guide/Publishing Metadata")

# Relationships between Resource and Agents 

## Using agent properties in Dublin Core

Persons, organizations and services can relate to resources in various ways. DCMI defined only a few common properties to describe the relationship between resources and agents. So when necessary other vocabularies should be used describing these relationships more detailed. In these cases we recommend to use the [marcrelator codes](http://id.loc.gov/vocabulary/relators.html). How to use them is described in

- [MARC Relator terms and Dublin Core](http://dublincore.org/usage/documents/relators/)
- [MARC Relator properties in Dublin Core metadata](http://www.ukoln.ac.uk/metadata/dcmi/marcrel-ex/)

## [Contributor](http://dublincore.org/documents/dcmi-terms/#terms-contributor) 

The contributor property represents a relationship between the resource and a person, an organization, or a service making a contribution to a resource.

## [Creator](http://dublincore.org/documents/dcmi-terms/#terms-creator) 

The creator property represents a relationship between the resource and a person, an organization, or a service primarily responsible for making the content of a resource.

## [Publisher](http://dublincore.org/documents/dcmi-terms/#terms-publisher) 

The publisher property represents a relationship between the resource and a person, an organization, or a service responsible for making the resource available and provide access to the resource.

## [RightsHolder](http://dublincore.org/documents/dcmi-terms/#terms-rightsHolder) 

This property represents a relationship between the resource and a person or an organization owning or managing rights over this resource.

## Guidelines for the creation of content for agents 

If you know there is a **URI standing for a person or organization** you should use it. For further information you should handle the person or organization like another resource.

Example with an **organization** :

| **rights holder** | gnd | _39454-3_ |
| | **name** | _Bundesarchiv Koblenz_ |
| | **homepage** | _[http://www.bundesarchiv.de/index.html.de](http://www.bundesarchiv.de/index.html.de)_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exrih1 "User Guide/Publishing Metadata")

Example with a **person** :

| **contributor** | gnd | _135066719_ |
| | **family name** | _Elliott_ |
| | **given name** | _Missy_ |
| | **nick name** | _Missy E_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCon1 "User Guide/Publishing Metadata")

Regardless of the existence of a URI **personal names** should be grouped in family name resp. surname as one part of the name and forename resp. given name as the other part .

You should handle the person name like **another resource** ,

| **creator** | | |
| | **family name** | _Shakespeare_ |
| | **given name** | _William_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCre1 "User Guide/Publishing Metadata")

or you could devide these names **by comma**.

| **creator** | _Shakespeare, William_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCre2 "User Guide/Publishing Metadata")

When you **in doubt about family name and given name** give the name as it appears.

| **contributor** | _Snoop Dogg_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCon2 "User Guide/Publishing Metadata")

If there is **more than one contributor/creator/publisher/rightsHolder** , each should be listed separately,

like another resource,

| **publisher** | gnd | _2125990-2_ |
| | **name** | _Rossijskaja Gosudarstvennaja Biblioteka_ |
| | **homepage** | _[http://www.rsl.ru/](http://www.rsl.ru/)_ |
| **publisher** | | |
| | **name** | _Knižnaja Palata_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exPub1 "User Guide/Publishing Metadata")

or with plain text.

| **creator** | _Hubble Telescope_ |
| **publisher** | _University of Nowhere_ |
| **publisher** | _All Your Data Inc._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exPub2 "User Guide/Publishing Metadata")

# [Type](http://dublincore.org/documents/dcmi-terms/#terms-type) 

The type property refers to a description of the nature or genre of the content of a resource (e.g. a stylistic category, a function or an aggregation level). To describe the physical or digital manifestation, use format.

## Guidelines for the creation of type content 

We recommend to **select a value from a controlled vocabulary** (e. g. [DCMI Type Vocabulary](http://dublincore.org/documents/dcmi-type-vocabulary/)).

| **type** | dctype | |
| | | _Still Image_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTyp1 "User Guide/Publishing Metadata")

But you may also use **plain text**.

| **type** | _Conference_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTyp4 "User Guide/Publishing Metadata")

If **no formal controlled vocabulary** exists, you could create a domain specific one.

| **type** | _[conference](http://metaweidner.github.io/dcmi-iac/wiki?title=Conference&action=edit&redlink=1 "Conference (page does not exist)")_ |

| identifier | _[conference](http://metaweidner.github.io/dcmi-iac/wiki?title=Conference&action=edit&redlink=1 "Conference (page does not exist)")_ | |
| **label** | _Conference_ | eng |
| **label** | _Tagung_ | ger |
| **label** | _съезд_ | rus |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTyp5 "User Guide/Publishing Metadata")

Is the resource composed of **multiple components of different types** the property should be repeated.

| **type** | dctype | |
| | | _Interactive Resource_ |
| **type** | dctype | |
| | | _Text_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTyp2 "User Guide/Publishing Metadata")

Different communities use a variety of type vocabularies. To ensure interoperability you can use terms from different vocabularies side by side - e.g. a type of the DCMI Type vocabulary in addition to **a non-controlled or domain specific type term**.

| **type** | | |
| | | _PC Game_ |
| **type** | dctype | |
| | | _Software_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exTyp3 "User Guide/Publishing Metadata")

# [Format](http://dublincore.org/documents/dcmi-terms/#terms-format) 

The property format refers to the file format, the physical medium (e.g. the data storage medium), or the dimension (the size or duration) of a resource. The information can be relevant to determine the equipment needed to display or operate a resource (e.g. if the described resource has format pdf you need a pdf reader to use it). To specify the different categories of format you should use extent and/or medium. To reference to the nature or genre of the content use type.

## Guidelines for the creation of format content 

For the description of the **file format** we recommend to use a controlled vocabulary - e.g. the list of [Internet Media Types](http://purl.org/NET/mediatypes/)(MIME).

| **format** | mime | _jpeg_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exFor1 "User Guide/Publishing Metadata")

You should repeat the properties when **more than one type of value exists**.

| **format** | mime | _jpeg_ |
| **format** | | _40 x 512 pixels_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exFor2 "User Guide/Publishing Metadata")

# [Extent](http://dublincore.org/documents/dcmi-terms/#terms-extent) 

This property refers to the size (e.g. bytes, pages, inches, etc.) or duration (e.g. hours, minutes, days, etc.) of a resource.

## Guidelines for the creation of extent content 

Typically the value used for the description of the extent consists of a **numeric value and a caption** to specify it. You may use a text string to present it

| **extent** | |
| | _21 minutes_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exExt1 "User Guide/Publishing Metadata")

or use controlled values for the caption.

| **extent** | | |
| | minutes | _21_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exExt2 "User Guide/Publishing Metadata")

# [Medium](http://dublincore.org/documents/dcmi-terms/#terms-medium) 

This property refers to the physical carrier of the resource and may only be used if the resource is of physical nature (e.g. a painting, a sculpture, etc.)

## Guidelines for the creation of medium content 

Note that the **media types must not be used with the property medium** because medium describes only physical objects.

We recommend to **use a controlled vocabulary**. If no formal controlled vocabulary exist you should nonetheless handle the media type like another resource.

| **medium** | |
| | _oil on wood_ |
| | _oil_ |
| | _wood_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exMed1 "User Guide/Publishing Metadata")

# [Language](http://dublincore.org/documents/dcmi-terms/#terms-language) 

This properties refers to the language of the intellectual content of the resource.

## Guidelines for the creation of language content 

For the identification of languages please follow [RFC 4646](http://www.ietf.org/rfc/rfc4646.txt). Best practice would be to **select a value from the three letter language tags of ISO 639** (e.g. [http://www.sil.org/iso639-3/codes.asp](http://www.sil.org/iso639-3/codes.asp)).

| **title** | _A great deliverance_ | |
| **language** | ISO 639-3 | _eng_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exLan7 "User Guide/Publishing Metadata")

or

| **title** | _A great deliverance_ | |
| **language** | | |
| | [RFC 4646](http://tools.ietf.org/html/rfc4646) | _eng_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exLan1 "User Guide/Publishing Metadata")

If the content is in **more than one language** , the property should be repeated.

| **title** | _Charlie Wilson's War_ | |
| **language** | ISO 639-3 | _eng_ |
| **language** | ISO 639-3 | _hun_ |
| **language** | ISO 639-3 | _tur_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exLan2 "User Guide/Publishing Metadata")

But if **every language version has it's own identifier** , they have to be treated like single resources.

Video1

| **title** | _Medieval helpdesk with English subtitles_ | |
| **identifier** | _[http://www.youtube.com/watch?v=pQHX-SjgQvQ&feature=player\_embedded](http://www.youtube.com/watch?v=pQHX-SjgQvQ&feature=player_embedded)_ | |
| **isVersionOf** | _Video2_ | |
| **language** | ISO 639-3 | _nor_ |
| **language** | ISO 639-3 | _eng_ |

Video2

| **title** | _Book help (better verson)_ | |
| **identifier** | _[http://www.youtube.com/watch?v=UOorZQLsmuA&feature=related](http://www.youtube.com/watch?v=UOorZQLsmuA&feature=related)_ | |
| **isVersionOf** | _Video1_ | |
| **language** | ISO 639-3 | _nor_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exLan3 "User Guide/Publishing Metadata")

You could also use plain text

| **title** | _The Power of Orange Knickers_ |
| **language** | _English_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exLan5 "User Guide/Publishing Metadata")

or create your own language vocabulary.

| **title** | _The Power of Orange Knickers_ |
| **language** | _[english](http://metaweidner.github.io/dcmi-iac/wiki?title=English&action=edit&redlink=1 "English (page does not exist)")_ |

| **identifier** | _[english](http://metaweidner.github.io/dcmi-iac/wiki?title=English&action=edit&redlink=1 "English (page does not exist)")_ |
| **label** | _English_ |
| **ISO 639-1** | _en_ |
| **ISO 639-3** | _eng_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exLan4 "User Guide/Publishing Metadata")

# Identifiers 

## [Identifier](http://dublincore.org/documents/dcmi-terms/#terms-identifier) 

An identifier is an unambiguous reference to a resource. Examples of formal identification systems include the Uniform Resource Identifier (URI) - including the Uniform Resource Locator (URL), the Digital Object Identifier (DOI) or the International Standard Book Number (ISBN).

## [BibliographicCitation](http://dublincore.org/documents/dcmi-terms/#terms-bibliographicCitation) 

- dcterms:bibliographicCitation

BibliographicCitation is a bibliographic reference to a resource identifying the resource by bibliographic details. Typically the described resource is the child in a parent/child relationship where the bibliographicCitation is not describing the relationship but the location of the described resource within the parent resource (e.g. the bibliographic citation of an article consists of the name of a journal as well as the number of volume, issues and even page references). For the description of parent/child relations see hasPart or isPartOf. BibliographicCitation may only be used to describe bibliographic resources like books, articles or other documentary resource.

## Guidelines for the creation of identifier content 

Best practice is to **declare the identification system** from which an identifier is selected.

| **title** | _What's a URI and why does it matter?_ | |
| **identifier** | _[http://www.ltg.ed.ac.uk/~ht/WhatAreURIs/](http://www.ltg.ed.ac.uk/~ht/WhatAreURIs/)_ | URI |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exIde1 "User Guide/Publishing Metadata")

Identifiers should be selected from formal identification systems as above but can also be **local identifiers** as long as there is a proper declaration of these.

| **title** | _Small and medium sized companies in Kathmandu_ | |
| **identifier** | _03KTM147_ | local ID |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exIde2 "User Guide/Publishing Metadata")

Note that the identifier of the description of a resource (e. g. of the metadata record) is not the same as the identifier of the resource itself.

| metadata record | | |
| **created** | _2010_ | W3CDTF |
| **identifier** | _013234098_ | database ID |
| my Video | | |
| **title** | _Medieval helpdesk with English subtitles_ | |
| **created** | _2007_ | W3CDTF |
| **identifier** | _[http://www.youtube.com/watch?v=pQHX-SjgQvQ&feature=player\_embedded](http://www.youtube.com/watch?v=pQHX-SjgQvQ&feature=player_embedded)_ | URI |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exIde3 "User Guide/Publishing Metadata")

If no identifier from a formal identification system exist, the identifier can be generated by a **bibliographic citation**. The bibliographic citation can be created as **text citation** ,

| **title** | _Prototyping Digital Library Technologies in zetoc_ |
| **bibliographicCitation** | _Lecture Notes in Computer Science 2458, 309-323 (2002)_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exBib1 "User Guide/Publishing Metadata")

or as **machine readable citations**.

| **title** | _Prototyping Digital Library Technologies in zetoc_ |
| **bibliographicCitation** | _&ctx\_ver=Z39.88-2004&rft\_val\_fmt=info:ofi/fmt:kev:mtx:journal&rft.jtitle=Lecture Notes in Computer Science&rft.volume=2458&rft.spage=309"^^info:ofi/fmt:kev:mtx:ctx_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exBib2 "User Guide/Publishing Metadata")

You can also **structure the bibliographic information**.

| **title** | _My first article about metadata_ | |
| **identifier** | | |
| | **journal title** | _My Favorite Journal_ |
| | **volume** | _3_ |
| | **issue** | _2_ |
| | **start page** | _14_ |
| | **date** | _2010_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exIde4 "User Guide/Publishing Metadata")

For additional information on bibliographicCitation see ["Guidelines for Encoding Bibliographic Citation Information in Dublin Core Metadata"](http://dublincore.org/documents/dc-citation-guidelines/index.shtml).

# Descriptions 

## [Description](http://dublincore.org/documents/dcmi-terms/#terms-description) 

This property refers to the description of the content of a resource. The description is a potentially rich source of indexable terms and assist the users in their selection of an appropriate resource. To refine the character of a description use abstract or tableOfContent.

## [Abstract](http://dublincore.org/documents/dcmi-terms/#terms-abstract) 

This property is used when the description of a resource is a formal abstract.

## [TableOfContent](http://dublincore.org/documents/dcmi-terms/#terms-tableOfContent) 

This property is used when the description of a resource is a structured list of the contents of a resource.

## Guidelines for the creation of descriptions 

A description may be **a free text account** ,

| **title** | _Bugs from New Zealand_ |
| **description** | _A box of ten bugs collected in New Zealand between 1845 and 1846_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDes2 "User Guide/Publishing Metadata")

an **abstract** ,

| **title** | _The Foundations of Programm Verification_ |
| **abstract** | _This revised edition provides a precise mathematical background to several program verification techniques. It concentrates on those verification methods that have now become classic, such as the inductive assertions method of Floyd, the axiomatic method of Hoare, and Scott's fixpoint induction. The aim of the book is to present these different verification methods in a simple setting and to explain their mathematical background. In particular the problems of correctness and completeness of the different methods are discussed in some detail and many helpful examples are included._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exAbs1 "User Guide/Publishing Metadata")

a **table of contents** ,

| **title** | _Remains of Claire Klawitter_ |
| **table of content** | _Diary 1822 - 1824 -- 20 pictures of Indian farmers -- 5 letters to Rudi Ratlos -- 1 map of North India_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exToc1 "User Guide/Publishing Metadata")

or a **reference to a description**.

| **title** | _Thriller_ |
| **description** | _[http://en.wikipedia.org/wiki/Thriller\_(album)](http://en.wikipedia.org/wiki/Thriller_(album))_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDes1 "User Guide/Publishing Metadata")

You can give some **information about the description you refer to**.

| **title** | _Coriandrum sativum_ | |
| **description** | _[http://en.wikipedia.org/wiki/Coriander](http://en.wikipedia.org/wiki/Coriander)_ | |
| | **title** | _Coriander_ |
| | **contributor** | _Wikipedia_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDes3 "User Guide/Publishing Metadata")

If **descriptions in different languages** exist, the property should be repeated with language tags.

| **title** | _Delvig and Kjuchelbeker_ | |
| **abstract** | _The book is a collection of works of two poets - contemporaries and friends of Pushkin - A. A. Delvig and V. K. Kjuchelbeker. It includes poems and prosa by Kjuchelbeker, parts of his diary, the poem Jurij and Xenia and reviews by Delvig. The attachment presents some retrospections to Delvig and Kjuchelbeker. A detailed biographic description tells us something about the life of the poets._ | eng |
| **abstract** | _Сборник впервые обединяет произведения двух поетов - современиков и друзей Пушкина - А. А. Дельвига и В. К. Кюхельбекера. Наряду со стихотворениями в книгу вклучены проза Кюхельбекера, фрагменты из его дневника, поема "Юрий и Ксения", а также рецензии Дельвига. В "Приложении" печатаются воспоминания о Дельвиге и Кюхельбекерею. Подробные биографические очерки рассказывают о жизненном пути поэтов._ | rus |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exAbs2 "User Guide/Publishing Metadata")

# [Subject](http://dublincore.org/documents/dcmi-terms/#terms-subject) 

The property subject represents a relationship between a resource and another resource which is a topic of the first resource rsp. describes the intellectual content of the first resource. If the topic of the resource has a spatial or temporal character, use coverage, spatial or temporal.

## Guidelines for describing the subject of a resource 

To express the topic of a resource we recommend to **use a URI representing another resource describing this topic** ,

| **title** | _Inviato alla Biennale&nbsp;: Venezia, 1949 - 2009_ | |
| **subject** | _[http://www.labiennale.org/en/Home.html](http://www.labiennale.org/en/Home.html)_ | |
| | **title** | _La Biennale di Venezia_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exSub1 "User Guide/Publishing Metadata")

or a URI representing the value of a controlled vocabulary,

- like **entries from authority file systems** (e.g. [the Library of Congress Subject Headings](http://id.loc.gov/authorities) or the [authority files of the German National Library](http://d-nb.info/gnd/), etc.), 

| **title** | _My Winter Wonderland_ | |
| **subject** | _[http://id.loc.gov/authorities/sh88004323#concept](http://id.loc.gov/authorities/sh88004323#concept)_ | |
| | **label** | _Cross-country skiing--Skating_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exSub2 "User Guide/Publishing Metadata")

- like **entries from classification systems** ((e.g. the [Dewey Decimal Classification](http://www.oclc.org/dewey/), or Linnaean taxonomy, etc.).

| **title** | _Transports in Kazakhstan 2000 - 2010_ |
| **subject** | _[W03\_7](http://metaweidner.github.io/dcmi-iac/wiki?title=W03_7&action=edit&redlink=1 "W03 7 (page does not exist)")_ |
| **subject** | _[G06\_3](http://metaweidner.github.io/dcmi-iac/wiki?title=G06_3&action=edit&redlink=1 "G06 3 (page does not exist)")_ |

| **label** | _W03.7_ |
| **name** | _Freight Transport_ |
| **broader** | _W03_ |
| **narrower** | _W03.72_ |
| **narrower** | _W03.75_ |

| **label** | _G06\_3_ |
| **name** | _Kazakhstan_ |
| **broader** | _G06_ |
| **narrower** | _G06\_31_ |
| **narrower** | _G06\_35_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exSub3 "User Guide/Publishing Metadata")

You may also use plain text. But if you need **more than one entry to describe the content** you should repeat the property.

| **title** | _How to get an aircraft_ |
| **subject** | _aircraft_ |
| **subject** | _leasing_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exSub6 "User Guide/Publishing Metadata")

If you want to use a keyword or keyphrase in **different languages** , you should use language tags.

| **title** | _KONSTYTUCJA RZECZYPOSPOLITEJ POLSKIEJ_ | |
| **subject** | | |
| | _Rzeczpospolita Polska_ | pol |
| | _Republic of Poland_ | eng |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exSub4 "User Guide/Publishing Metadata")

If the **subject is a person or organization** you should use names from formal name authorities (e.g. from the Library of Congress Name Authority Headings [[1]](http://id.loc.gov/authorities), or from the Virtuell International Authority File [[2]](http://www.viaf.org/)).

| **title** | _Candle in the wind_ | |
| **subject** | gnd | _118583549_ |
| | **family name** | _Monroe_ |
| | **given name** | _Marilyn_ |
| | **born** | _1926_ |
| | **died** | _1962_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exSub5 "User Guide/Publishing Metadata")

# Coverage 

## [Coverage](http://dublincore.org/documents/dcmi-terms/#terms-coverage) 

The property coverage describes a relationship between a resource and another resource which represents the extent or scope of the content of the first resource. This includes the spatial locations (a place name or geographic co-ordinates), temporal periods (a period label, a date or a date range), or jurisdictions (states, counties, or other administrative entities). If you want to make a destinction between the temporal or spatial character of the content use temporal or spatial.

## [Temporal](http://dublincore.org/documents/dcmi-terms/#terms-temporal) 

This property describes the relationship between a resource and another resource which represent the temporal characteristics of the intellectual content of the first resource expressed by period labels or date encoding. If you want to describe date of the lifecycle of a resource use the date properties.

## [Spatial](http://dublincore.org/documents/dcmi-terms/#terms-spatial) 

This property describes the relationship between a resource and another resource which represents spatial characteristics of the intellectual content of the first resource expressed by by geographic names, latitude/longitude, or other established georeferencing.

## Guidelines for describing the coverage, spatial or temporal character of a resource 

To describe the **temporal** characteristic of a resource

you may use plain text,

| **title** | _Transports in Kazakhstan 2000 - 2010_ |
| **coverage** | _2000 - 2010_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCov5 "User Guide/Publishing Metadata")

or **structure your entry** using dates,

| **title** | _Transports in Kazakhstan 2000 - 2010_ | | |
| **temporal** | | | |
| | **start** | _2000_ | W3CDTF |
| | **end** | _2010_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCov3 "User Guide/Publishing Metadata")

or **period labels**.

| **title** | _Analysis of rocks collected in Perth_ | |
| **temporal** | | |
| | **start** | _Cambrian period_ |
| | **scheme** | _Geological timescale_ |
| | **name** | _Phanerozoic Eon_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCov4 "User Guide/Publishing Metadata")

Further information on encoding temporal characteristics you will find in the [DCMI Period Encoding Scheme](http://dublincore.org/documents/dcmi-period/).

To describe the **spatial** character of a resource, you could use plain text,

| **title** | _Analysis of rocks collected in Perth_ |
| **coverage** | _Perth, W. A._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCov6 "User Guide/Publishing Metadata")

or express it by **georeferencing** ,

| **title** | _Analysis of rocks collected in Perth_ | |
| **spatial** | | |
| | **east** | _115.85717_ |
| | **north** | _-31.95301_ |
| | **name** | _Perth, W. A._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCov1 "User Guide/Publishing Metadata")

or **reference to a formal encoding**.

| **title** | _The growth of trees in the suptropical highlands_ | |
| **spatial** | | |
| | **label** | _Cwb_ |
| | **source** | _Köppen-Geiger Climate Classification_ |
| | **main Climates** | _warm temperate_ |
| | **precipitation** | _winter dry_ |
| | **temperature** | _warmest month averaging below 22°C_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCov2 "User Guide/Publishing Metadata")

Further information on encoding spatial characteristics you will find in the [DCMI Box Encoding Scheme](http://dublincore.org/documents/dcmi-box/) and the [DCMI Point Encoding Scheme](http://dublincore.org/documents/dcmi-point/).

# Dates 

## [Date](http://dublincore.org/documents/dcmi-terms/#terms-date) 

The property date refers to a description of any dates or ranges in the lifecycle of a resource and is typically associated with the creation or availability. If the destinction between different sorts of date is necessary, the following subproperties should be used. If a date is describing the content of a resource the properties coverage or temporal have to be used.

## [Created](http://dublincore.org/documents/dcmi-terms/#terms-created) 

This property refers to a description of the date or range of the creation of a resource. According to the one-to-one principle this has to be the creation date of the resource being described and not the creation date of any other resource from which the described resource derives (e.g. a former version or a superior resource). So a resource is created only once, every other date of creation belongs to another resource that has to be described on its own.

## [Issued](http://dublincore.org/documents/dcmi-terms/#terms-issued) 

This property refers to a description of the date of the formal issuance resp. publication of a resource. A resource is issued only once, every other issuance belongs to another resource that has to be described on its own. If the issuance of a resource is not formal the property "available" should be used.

## [Available](http://dublincore.org/documents/dcmi-terms/#terms-available) 

This property refers to a description of the date a resource did become or will become available. A resource becomes available only once, every other availability belongs to another resource that has to be described on its own. If the availability of a resource starts with the formal issuance resp. publication use "issued".

## [Modified](http://dublincore.org/documents/dcmi-terms/#terms-modified) 

This property refers to a description of the date a resource was changed. You may record every date a resource was modified by repeating this property or record only one date (this should be the last one).

## [Valid](http://dublincore.org/documents/dcmi-terms/#terms-valid) 

This property refers to a description of the date or range a resource is, was or will be valid. This property should be used if a resource is only valid resp. relevant until a particular date.

## [DateCopyrighted](http://dublincore.org/documents/dcmi-terms/#terms-dateCopyrighted) 

This property refers to a description of the date or range of the copyright of the resource.

## [DateSubmitted](http://dublincore.org/documents/dcmi-terms/#terms-dateSubmitted) 

This property refers to a description of the date a resource was submitted (e.g. a thesis at a university department, an article at the editorial board of a journal, etc.).

## [DateAccepted](http://dublincore.org/documents/dcmi-terms/#terms-dateAccepted) 

This property refers to a description of the date a resource was accepted (e.g. a thesis by a university department, an article by the editorial board of a journal, etc.)

## Guidelines for the creation of content for dates 

For the structure of date properties we recommend the usage of the **W3CDTF profile of ISO 8601** [W3CDTF]. It allows to sort search results by date and facilitates the merging of metadata of different applications.

You should use this encoding for **a point in time**

| **created** | _2003-04-10_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat2 "User Guide/Publishing Metadata")

but must not use it with **a range** ,

| **valid** | _2007-05-06/2007-07-15_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat9 "User Guide/Publishing Metadata")

or when the date is located **before the common area**.

| **created** | _-500_ | gYear |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat3 "User Guide/Publishing Metadata")

If you need to **structure range data** , make a distinction of start and end date.

| **date** | | | |
| | **start** | _2007-05-06"_ | W3CDTF |
| | **end** | _2007-07-15_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat10 "User Guide/Publishing Metadata")

If the **complete date is unknown** you should use

month and year

| **available** | _2006-07_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat1 "User Guide/Publishing Metadata")

or only the year

| **issued** | _2009_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat7 "User Guide/Publishing Metadata")

If **more than one date of the same type** (e.g. modified) is recorded, the property must be repeated.

| **modified** | _2009-12-22_ | W3CDTF |
| **modified** | _2010-01-08_ | W3CDTF |
| **modified** | _2010-02-15_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat8 "User Guide/Publishing Metadata")

Since a resource has only one date of creation, issuance, availability and/or copyright you may repeat the properties created, issued, available and dateCopyrighted only if you want to **provide the same date in another structure**.

| **created** | _1752_ | W3CDTF |
| **created** | _probably after 1752_ | |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat4 "User Guide/Publishing Metadata")

If the described date is **only approximately known** , you may use plain text,

| **created** | _aprox. 500 B.C._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat5 "User Guide/Publishing Metadata")

or describe it.

| **date** | | |
| | **year** | _500_ |
| | **qualifier** | _approx._ |
| | **epoch** | _B.C._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat11 "User Guide/Publishing Metadata")

**Another date of creation, issuance, availability and/or copyright** however belongs to another resource that has to be described on its own. The relation of both resources may be described by one of the relation properties or by source.

| **title** | _Population estimates in Scandinavia_ | | |
| **created** | _2004_ | W3CDTF | |
| **source** | | | |
| | **title** | _World health report 2002 statistical annex_ | |
| | **created** | _2002_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exDat6 "User Guide/Publishing Metadata")

# Source and Relations 

## [Relation](http://dublincore.org/documents/dcmi-terms/#terms-relation) 

Relation represents the relationship between the described resource and another resource, that is related to the described resource in some way. Such relationship may be expressed reciprocally but this is not required and depends on the sort of relation. If the relation shall be specified more precicely use one of the following properties.

## [Source](http://dublincore.org/documents/dcmi-terms/#terms-source) 

Source describes the relationship between the described resource and another resource, from which the described resource is derived in whole or in part (e.g. data of a climate centre are the source of a forecast, a book or journal is the source of a scan, etc.)

## [IsPartOf](http://dublincore.org/documents/dcmi-terms/#terms-isPartOf) 

This property describes the relationship between the described resource and another resource of which the described resource is a physical or logical part (e.g. a painting as part of a collection, an article as part of a journal, etc.). The described resource is like a "child" in a hierarchical or "parent/child" relationship. For the reciprocal statement use hasPart.

## [HasPart](http://dublincore.org/documents/dcmi-terms/#terms-hasPart) 

This property describes the relationship between the desribed resource and another resource which is a physical or logical part of the described resource (e.g. the described resource is a collection of paintings, or a journal with different articles, etc.). The described resource is like the "parent" in a hierarchical or "parent/child" relationship. For the reciprocal statement use isPartOf.

## [IsVersionOf](http://dublincore.org/documents/dcmi-terms/#terms-isVersionOf) 

This property describes the relationship between the described resource and another resource, that is a former version, edition or adaptation of the described resource (e.g. the described resource is the revision of a book, or another recording of a song, etc.). Another version implies changes in the content of a resource. For resources with different formats use isFormatOf. For the reciprocal statement use hasVersion.

## [HasVersion](http://dublincore.org/documents/dcmi-terms/#terms-hasVersion) 

This property describes the relationship between the desribed property and another property, that is a later version, edition or adaptation of the described resource (e.g. the described resource is the older version of a revised book, or of a song, etc.). Another version implies changes in the content of a resource. For resources with different formats use hasFormat. For the reciprocal statement use isVersionOf.

## [IsFormatOf](http://dublincore.org/documents/dcmi-terms/#terms-isFormatOf) 

This property describes the relationship between the described resource and another resource, that is a former version of the described resource with the same intellectual content but presented in another format (e.g. the described resource is the microfilm version of a printed book, or the pdf version of a doc document). For intellectual changes between resources use isVersonOf. For the reciprocal statement use hasFormat.

## [HasFormat](http://dublincore.org/documents/dcmi-terms/#terms-hasFormat) 

This property describes the relationship between the described resource and another resource, that is a later version of the described resource with the same intellectual content but presented in another format (e.g. the desribed resource is a printed book that is also availabel as a microfilm, or a doc document that is also available as pdf). For intellectual changes between resources use hasVersion. For the reciprocal statement use isFormatOf.

## [Replaces](http://dublincore.org/documents/dcmi-terms/#terms-replaces) 

This property describes the relationship between the described resource and another resource, that has been supplanted, displaced or superseeded by the described resource. It is used for the valid version in chain of versions (e.g. the described resource is the the last draft of a contract, or the current version of guidelines). For the reciprocal statement use isReplacedBy.

## [IsReplacedBy](http://dublincore.org/documents/dcmi-terms/#terms-isReplacedBy) 

This property describes the relationship between the described resource and another resource, that supplants, displaces or superseedes the described resource. It is used, when in chain of versions only one version is valid (e.g. the described resource is one of the former drafts of a contract, or a former version of guidelines). For the reciprocal statement use replaces.

## [Requires](http://dublincore.org/documents/dcmi-terms/#terms-requires) 

This property describes the relationship between the described resource and another resource supporting the function, delivery or coherence of the content of the described resource (e.g. the described resource is an application that can be used only with a particular software, or hardware). For the reciprocal statement use isRequiredBy.

## [IsRequiredBy](http://dublincore.org/documents/dcmi-terms/#terms-isRequiredBy) 

The described resource is necesssary for the function, delivery or coherence of the content of the resource the property references to (e.g. the described resource is a software or hardware necesssary to use a particular application). For the reciprocal statement use requires.

## [References](http://dublincore.org/documents/dcmi-terms/#terms-references) 

This property describes the relationship between the described resource and another resource that is cited, referenced, or otherwise pointed to by the described resource (e.g. the described resource is an article citing a book, or an interview pointing to a play). For the reciprocal statement use isReferencedBy.

## [IsReferencedBy](http://dublincore.org/documents/dcmi-terms/#terms-isReferencedBy) 

This property describes the relationship between a resource and another resource that points to the described resource by citation, acknowledgement, etc (e.g. the described resource is a book cited in an article, or a play pointed to in an interview, etc.). For the reciprocal statement use references.

## [ConformsTo](http://dublincore.org/documents/dcmi-terms/#terms-conformsTo)

This property describes the relationship between a resource and an established standard, to which the described resource conforms (e.g. a metadata record that conforms to the RDA standard, or a pipe that conforms to ISO 3183, etc.)

## Guidelines for the creation of content for relations and source 

You may refer to the related resource by plain text or by a URI representing the related resource. If you use plain text, you should **use a formal citation**.

| **issued** | _2009_ | W3CDTF |
| **isFormatOf** | | |
| | _Eike von Repgow: Sachsenspiegel, Auffs newe vbersehen mit Summarijs vnd Additionen ...; Leipzig 1561/1563_ | |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRel1 "User Guide/Publishing Metadata")

However recommended best practice is to **use an identifier instead of text** ,

| **conformsTo** | _[http://www.w3.org/2001/XMLSchema](http://www.w3.org/2001/XMLSchema)_ | - |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRel2 "User Guide/Publishing Metadata")

or to **describe the related resources like another resource**.

| **references** | | | |
| | **creator** | _Black, Carl_ |
| | **contributor** | _White, Stuart_ |
| | **title** | _Black and White_ |
| | **date** | _1988_ | W3CDTF |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRel3 "User Guide/Publishing Metadata")

If there is **more than one relation of the same sort** you have to repeat the property:

| **requires** | |
| | _audio_ |
| | _video_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRel4 "User Guide/Publishing Metadata")

If **both resources of a relationship are described** the relation could be expressed reciprocally whereupon reciprocality could be generated automatically

| **identifier** | _[mySong1](http://metaweidner.github.io/dcmi-iac/wiki?title=MySong1&action=edit&redlink=1 "MySong1 (page does not exist)")_ | |
| **title** | _Candle in the wind_ | |
| **issued** | _1973_ | W3CDTF |
| **description** | _Portayal of the life of Marilyn Monroe_ | |
| **hasVersion** | _[mySong2](http://metaweidner.github.io/dcmi-iac/wiki?title=MySong2&action=edit&redlink=1 "MySong2 (page does not exist)")_ | |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRel5 "User Guide/Publishing Metadata")

| **identifier** | _[mySong2](http://metaweidner.github.io/dcmi-iac/wiki?title=MySong2&action=edit&redlink=1 "MySong2 (page does not exist)")_ | |
| **title** | _Candle in the wind_ | |
| **alternative** | _Goodbye England's Rose_ | |
| **issued** | _1997_ | W3CDTF |
| **description** | _Tribut to the dead princess of Wales_ | |
| **isVersionOf** | _[mySong1](http://metaweidner.github.io/dcmi-iac/wiki?title=MySong1&action=edit&redlink=1 "MySong1 (page does not exist)")_ | |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRel6 "User Guide/Publishing Metadata")

# Rights 

## [Rights](http://dublincore.org/documents/dcmi-terms/#terms-rights) 

The rights property represents the relationship between a resource and information about rights held in and over this resource. This includes information like access rights, Intellectual Property Rights (IPR), copyrights, references to legal documents describing how to use a resource, etc. To specify rights more precicely use accessRights or license.

## [AccessRights](http://dublincore.org/documents/dcmi-terms/#terms-accessRights) 

This property represents the relationship between a resource and information about who can access a resource or an indication of its security status. Access rights provides information about restrictions to view, search or use a resource based on attributes of the resource itself or the category of user.

## [License](http://dublincore.org/documents/dcmi-terms/#terms-license) 

This property represents the relationship between a resource and a legal document giving official permission to do something with the resource (e.g. an otherwise free resource may not be used for reproduction within commercial applications). Examples of such licenses you will find at [http://creativecommons.org/](http://creativecommons.org/).

## Guidelines for the creation of rights content 

A rights statement may be **a text** ,

| **title** | _Data from my last evaluation_ |
| **accessRights** | |
| | _My colleagues only_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRig1 "User Guide/Publishing Metadata")

or **a URI** referencing to formal rights information,

| **title** | _You and me_ |
| **rights** | _[http://creativecommons.org/licenses/by/3.0/legalcode](http://creativecommons.org/licenses/by/3.0/legalcode)_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRig3 "User Guide/Publishing Metadata")

or a **combination of both**.

| **title** | _GeoNetwork - Geographic Metadata Catalog_ |
| **license** | _[http://www.gnu.org/licenses/gpl.html](http://www.gnu.org/licenses/gpl.html)_ |
| | _GNU General Public License_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRig2 "User Guide/Publishing Metadata")

If there are no formal rights statements to use you may also **create your own rights statement**.

| **title** | _Diaries of Juanita Ramirez_ |
| **rights** | _[accessConditions](http://metaweidner.github.io/dcmi-iac/wiki?title=AccessConditions&action=edit&redlink=1 "AccessConditions (page does not exist)")_ |

| **identifier** | _[accessConditions](http://metaweidner.github.io/dcmi-iac/wiki?title=AccessConditions&action=edit&redlink=1 "AccessConditions (page does not exist)")_ |
| **title** | _Access to my stuff_ |
| **description** | _Resources under this right can only be read, searched and used by members of the myProject_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exRig4 "User Guide/Publishing Metadata")

# Special properties for the description of education material 

## [Audience](http://dublincore.org/documents/dcmi-terms/#terms-audience) 

The property audience represents the relationship between a resource and the class of persons for whom the resource is intended or useful (e.g. the resource is a textbook for psychologists, etc.). To specify an audience more precisely use mediator or educationLevel.

## [Mediator](http://dublincore.org/documents/dcmi-terms/#terms-mediator) 

This property represents the relationship between a resource and the class of persons who mediate access to the resource and for whom it is intended or useful. This might be teachers, parents etc. (e.g. teachers are mediators for a resource intended to be used in elementary school lessons)

## [EducationLevel](http://dublincore.org/documents/dcmi-terms/#terms-educationLevel) 

This property refers to information about the progress of an audience through the educational or training context, for which the described resource is intended (e.g. the resource is an English workbook for students of the 4th - 5th grade).

## [InsctructionalMethod](http://dublincore.org/documents/dcmi-terms/#terms-instructionalMethod) 

This property refers to the process used to engender knowledge, attitudes and skills, that the described resource is designed to support. Typically it includes ways of presenting instructional materials or conducting instructional activities, patterns of learner-to-learner and learner-to-instructor interactions, and mechanisms by which group and individual levels of learning are measured. Instructional methods include all aspects of the instruction and learning processes from planning and implementation through evaluation and feedback.

## Guidelines for the creation of content for properties describing education material 

You should use formal or informal **controlled vocabularies**. Though none are registered by DCMI, implementors are encouraged to develop local lists of values, and to use them consistently.

| **title** | _Advances Physics_ |
| **audience** | |
| | _elementary school pupils_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exEdu1 "User Guide/Publishing Metadata")

| **mediator** | |
| | _schoolteacher_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exEdu4 "User Guide/Publishing Metadata")

| **educationLevel** | |
| | _3rd - 4th grade_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exEdu2 "User Guide/Publishing Metadata")

| **InstructionalMethod** | |
| | _experimental learning_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exEdu3 "User Guide/Publishing Metadata")

# Special properties for the description of collections 

## [AccrualMethod](http://dublincore.org/documents/dcmi-terms/#terms-accrualMethod) 

This property refers to the method by which items are added to a collection.

## [AccrualPeriodicity](http://dublincore.org/documents/dcmi-terms/#terms-accrualPeriodicity) 

This property refers to the frequency with wich items are added to a collection.

## [AccrualPolicy](http://dublincore.org/documents/dcmi-terms/#terms-accrualPolicy) 

This property refers to the policy governing the addition of items to a collection.

## Guidelines for the creation of content for properties describing collections 

Resources described by these properties **have to be collections**. We recommend to use values of formal or informal **controlled vocabularies**.

| **title** | _Pottery in Scandinavia in the second half of 19th century_ |
| **accrualMethod** | |
| | _purchase_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCol1 "User Guide/Publishing Metadata")

| **accrualPeriodicity** | |
| | _irregular_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCol2 "User Guide/Publishing Metadata")

| **accrualPolicy** | |
| | _Objects of this collection have to be Scandinavian ceramics from 1940s to 1999s._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exCol3 "User Guide/Publishing Metadata")

# [Provenance](http://dublincore.org/documents/dcmi-terms/#terms-provenance) 

This property refers to a description of changes in ownership and custody. The statement should include any changes of the resource that are significant for its authenticity, integrity and interpretation.

## Guidelines for the creation of content for provenance 

The description of the provenance of a resource includes all changes made to a resource.

The provenance can be **described by text** ,

| **title** | _Luxor Obelisk_ |
| **provenance** | |
| | _Originally located at the entrance to the Luxor temple the obelisk came to Paris in 1836 as a gift by Muhammad Ali Pasha._ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exPro1 "User Guide/Publishing Metadata")

or **desribed like another resource**.

| **title** | _The flea circus_ | |
| **provenance** | | |
| | **ownedBy** | _1829 - 1833; Jim Button_ |
| | **ownedBy** | _1833 - 1915; My Library_ |
| | **ownedBy** | _since 1915; Flea Academy_ |

[as linked data](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Publishing_Metadata#exPro2 "User Guide/Publishing Metadata")

