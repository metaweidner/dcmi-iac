---
layout: page
title: DCMI Metadata Terms
---

## DCMI Metadata Terms 

The RDF Properties, Classes, Vocabulary Encoding Schemes, and Datatypes declared and maintained by the Dublin Core Metadata Initiative are collectively referred to as [DCMI Metadata Terms](http://dublincore.org/documents/dcmi-terms/)<sup id="cite_ref-0" class="reference"><a href="#cite_note-0">[1]</a></sup>. Of the four types of terms, Properties, Classes, and Datatypes (Syntax Encoding Scheme) are defined exactly as in [RDF](http://metaweidner.github.io/dcmi-iac/wiki/Glossary/RDF "Glossary/RDF"). The notion of a Vocabulary Encoding Scheme is unique to DCMI, though it is similar to -- arguably, formally indistinguishable from -- the notion of a [Concept Scheme](http://www.w3.org/TR/skos-reference/#schemes)<sup id="cite_ref-1" class="reference"><a href="#cite_note-1">[2]</a></sup> in Simple Knowledge Organization System (SKOS).

It hasn't always been this way. When Elements were introduced in a 1995 workshop, and Qualifiers in 1997, the W3C specification for RDF did not yet exist. The path from "native Dublin Core" term types to RDF only really ended with the publication of a revised DCMI Abstract Model in 2007<sup id="cite_ref-2" class="reference"><a href="#cite_note-2">[3]</a></sup>. Starting with the Canberra Qualifiers of 1997<sup id="cite_ref-3" class="reference"><a href="#cite_note-3">[4]</a></sup> -- Language, Scheme, and Type (Sub-Element) -- and continuing with the transitional Types A and B of 1998 <sup id="cite_ref-4" class="reference"><a href="#cite_note-4">[5]</a></sup>, the path to RDF took the following turns:

- The Dublin Core Qualifiers published in 2000 were of two types -- Element Refinements and Encoding Schemes.<sup id="cite_ref-5" class="reference"><a href="#cite_note-5">[6]</a></sup>

- By 2003, Elements began to be called Properties. The type Encoding Scheme was differentiated into Vocabulary Encoding Schemes and Syntax Encoding Schemes.<sup id="cite_ref-6" class="reference"><a href="#cite_note-6">[7]</a></sup>

- In the meantime, 2004 saw the publication of a major revision of RDF and laying the groundwork for modern Semantic Web implementations.<sup id="cite_ref-7" class="reference"><a href="#cite_note-7">[8]</a></sup>

- In the revised DCMI Abstract Model of 2007, Property replaced Element as the designation of choice and was explicitly equated with RDF Property. The term Element Refinement was dropped with the explanation that an Element Refinement was no more than a Property which happened to be a sub-property of another. Syntax Encoding Schemes were declared to be RDF Datatypes.

### Equivalences 

| The Dublin Core (1995) | DCMI Grammatical Principles (2000-2001) | DCMI Abstract Model (2007) | RDF and SKOS (today) |
| _element_ | _element_ | _property_ or _element_ | [_rdf:Property_](http://www.w3.org/1999/02/22-rdf-syntax-ns#Property) |
| | _qualifier_ | _element refinement_ | _property_ with sub-property-of relation | [_rdf:Property_](http://www.w3.org/1999/02/22-rdf-syntax-ns#Property) with [_rdfs:subPropertyOf_](http://www.w3.org/2000/01/rdf-schema#subPropertyOf) relationship |
| _encoding scheme_ | _syntax encoding scheme_ | [_rdfs:Datatype_](http://www.w3.org/2000/01/rdf-schema#Datatype) |
| _vocabulary encoding scheme_ | [_skos:ConceptScheme_](http://www.w3.org/TR/skos-reference/#schemes), though the equivalence is debatable and has not been formally declared |

### References 

1. ↑ [http://dublincore.org/documents/dcmi-terms/](http://dublincore.org/documents/dcmi-terms/)
2. ↑ [http://www.w3.org/TR/skos-reference/#schemes](http://www.w3.org/TR/skos-reference/#schemes)
3. ↑ [http://dublincore.org/documents/2007/06/04/abstract-model/#sect-5](http://dublincore.org/documents/2007/06/04/abstract-model/#sect-5)
4. ↑ [http://www.dlib.org/dlib/june97/metadata/06weibel.html](http://www.dlib.org/dlib/june97/metadata/06weibel.html)
5. ↑ [http://dublincore.org/documents/1998/10/07/datamodel/index.shtml](http://dublincore.org/documents/1998/10/07/datamodel/index.shtml)
6. ↑ [http://dublincore.org/documents/2000/07/11/dcmes-qualifiers/](http://dublincore.org/documents/2000/07/11/dcmes-qualifiers/)
7. ↑ [http://dublincore.org/usage/documents/2003/02/07/principles/](http://dublincore.org/usage/documents/2003/02/07/principles/)
8. ↑ [http://www.w3.org/TR/2004/REC-rdf-concepts-20040210/](http://www.w3.org/TR/2004/REC-rdf-concepts-20040210/)

