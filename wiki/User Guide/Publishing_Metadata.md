---
layout: page
title: Publishing Metadata
---

- Contributor: Stefanie Rühle 
- Contributer: Tom Baker 
- Contributor: Pete Johnston

Go to [User Guide](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide "User Guide") | [Creating Metadata](http://metaweidner.github.io/dcmi-iac/wiki/User_Guide/Creating_Metadata "User Guide/Creating Metadata")

**How to use DCMI Metadata as linked data**

| 

## Contents

- 1 About the linked data examples
- 2 Properties of the terms namespace
  - 2.1 Properties of the terms namespace used only with literal values
    - 2.1.1 dcterms:alternative
    - 2.1.2 dcterms:available
    - 2.1.3 dcterms:bibliographicCitation
    - 2.1.4 dcterms:created
    - 2.1.5 dcterms:date
    - 2.1.6 dcterms:dateAccepted
    - 2.1.7 dcterms:dateCopyrighted
    - 2.1.8 dcterms:dateSubmitted
    - 2.1.9 dcterms:identifier
    - 2.1.10 dcterms:issued
    - 2.1.11 dcterms:modified
    - 2.1.12 dcterms:title
    - 2.1.13 dcterms:valid
  - 2.2 Properties of the terms namespace used only with non-literal values
    - 2.2.1 dcterms:accrualMethod
    - 2.2.2 dcterms:accrualPeriodicity
    - 2.2.3 dcterms:accrualPolicy
    - 2.2.4 dcterms:accessRights
    - 2.2.5 dcterms:audience
    - 2.2.6 dcterms:conformsTo
    - 2.2.7 dcterms:contributor
    - 2.2.8 dcterms:coverage
    - 2.2.9 dcterms:creator
    - 2.2.10 dcterms:educationLevel
    - 2.2.11 dcterms:extent
    - 2.2.12 dcterms:format
    - 2.2.13 dcterms:hasFormat
    - 2.2.14 dcterms:hasPart
    - 2.2.15 dcterms:hasVersion
    - 2.2.16 dcterms:instructionalMethod
    - 2.2.17 dcterms:isFormatOf
    - 2.2.18 dcterms:isPartOf
    - 2.2.19 dcterms:isReferencedBy
    - 2.2.20 dcterms:isReplacedBy
    - 2.2.21 dcterms:isRequiredBy
    - 2.2.22 dcterms:isVersionOf
    - 2.2.23 dcterms:language
    - 2.2.24 dcterms:license
    - 2.2.25 dcterms:mediator
    - 2.2.26 dcterms:medium
    - 2.2.27 dcterms:provenance
    - 2.2.28 dcterms:publisher
    - 2.2.29 dcterms:references
    - 2.2.30 dcterms:relation
    - 2.2.31 dcterms:replaces
    - 2.2.32 dcterms:requires
    - 2.2.33 dcterms:rights
    - 2.2.34 dcterms:rightsHolder
    - 2.2.35 dcterms:source
    - 2.2.36 dcterms:spatial
    - 2.2.37 dcterms:subject
    - 2.2.38 dcterms:temporal
    - 2.2.39 dcterms:type
  - 2.3 Properties of the terms namespace, that may be used with literal and non-literal values
    - 2.3.1 dcterms:abstract
    - 2.3.2 dcterms:description
    - 2.3.3 dcterms:tableOfContents
- 3 Legacy namespace
  - 3.1 Properties of the legacy namespace
    - 3.1.1 dc:contributor
    - 3.1.2 dc:coverage
    - 3.1.3 dc:creator
    - 3.1.4 dc:date
    - 3.1.5 dc:description
    - 3.1.6 dc:format
    - 3.1.7 dc:identifier
    - 3.1.8 dc:language
    - 3.1.9 dc:publisher
    - 3.1.10 dc:relation
    - 3.1.11 dc:rights
    - 3.1.12 dc:subject
    - 3.1.13 dc:title
    - 3.1.14 dc:type
 |

# About the linked data examples 

To present these examples in a concise form we use the [Turtle syntax for RDF](http://www.w3.org/TeamSubmission/2008/SUBM-turtle-20080114/). The examples therefore appear in code lines such as:

    @prefix ex: <http://www.example.com/>.
     ex:aResource ex:aProperty "An RDF Literal" .

or

    @prefix ex: <http://www.example.com/>.
     ex:aResource ex:aProperty ex:anotherResource . 
     ex:anotherProperty "An RDF Literal"@en .

Within the examples we use different namespaces. The following prefixes are used to specify the namespaces we use for our examples:

For the **Dublin Core namespaces** we use:

    @prefix dc: <http://purl.org/dc/elements/1.1/> (DCMI legacy namespace used for the 15 core properties)
     @prefix dcterms: <http://purl.org/dc/terms/> (DCMI terms namespace of the DCMI terms - properties, classes and datatypes)
     @prefix dctype: <http://purl.org/dc/dcmitype/> (DCMI type namespace of the DCMI classes of types)

**Further namespaces** used are:

    @prefix ex: http://www.example.org/ (an exemplary namespace)
     @prefix xsd: http://www.w3.org/2001/XMLSchema# (namespace of the XML Schema language)
     @prefix rdf: http://www.w3.org/1999/02/22-rdf-syntax-ns# (namespace of the rdf vocabulary)
     @prefix rdfs: http://www.w3schools.com/RDF/rdf-schema.xml (namespace of the rdf schema vocabulary)
     @prefix foaf: http://xmlns.com/foaf/0.1/ (namespace of the "Friend of a Friend" vocabulary)
     @prefix gnd: http://d-nb.info/gnd/ (namespace of the authority files of the German National Library)
     @prefix mime: http://purl.org/NET/mediatypes/ (namespace for MIME media types vocabulary)
     @prefix skos: http://www.w3.org/2004/02/skos/core# (namespace of the SKOS vocabulary)

# Properties of the terms namespace 

The main difference between the legacy namespace and the terms namespace is the definition of ranges for most terms of the last and the definition of a domain for some of them. The definition of a domain governs the entities for which a property may be used. The definition of a range governs the usage of literal and non-literal values in context with a property.

## Properties of the terms namespace used only with literal values 

### [dcterms:alternative](http://dublincore.org/documents/dcmi-terms/#terms-alternative) 

The range for dcterms:alternative is rdfs:Literal. So you can use dcterms:alternative only with literal values

    ex:myBook dcterms:title "Passion for Pulses" ;
              dcterms:alternative "A Feast of Beans, Peas and Lentils from Around the World" .

    ex:myStuff dcterms:title "American Meteorological Association Newsletter" ;
               dcterms:alternative "AMA Newsletter" .

    ex:myDocument dcterms:title "EU Stability Programm of Belgium"@eng ;
                  dcterms:alternative "Council Opinion on the Updated 
                                       Stability Programm of Belgium 2009 - 
                                       2010 "@eng ,
                                      "Stellungnahme des Rates zum 
                                       aktualisierten Stabilitätsprogramm 
                                       Belgiens für 2009 - 2012"@ger .

### [dcterms:available](http://dublincore.org/documents/dcmi-terms/#terms-available) 

The range defined for dcterms:available is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myMusic dcterms:available "2006-07"^^dcterms:W3CDTF .

### [dcterms:bibliographicCitation](http://dublincore.org/documents/dcmi-terms/#terms-bibliographicCitation) 

The range defined for dcterms:bibliographicCitation is the class of rdfs:Literal. Values used with dcterms:bibliographicCitation have to be instances of this class. Therefore this property can only be used with literal values.

Moreover a domain of the class dcterms:BibliographicResource is declard for dcterms:bibliographicCitation. Thus dcterms:bibliographicCitation may only be used describing bibliographic resources.

    ex:myArticle dcterms:title "Prototyping Digital Library Technologies in zetoc" ;
                 dcterms:bibliographicCitation "Lecture Notes in Computer Science 2458, 309-323 (2002)" .

    ex:myArticle dcterms:title "Prototyping Digital Library Technologies in zetoc" ;
                 dcterms:bibliographicCitation "&ctx_ver=Z39.88-2004&rft_val_fmt=info:ofi/fmt:kev:mtx:journal
                 &rft.jtitle=Lecture Notes in Computer Science&rft.volume=2458&rft.spage=309"^^info:ofi/fmt:kev:mtx:ctx .

### [dcterms:created](http://dublincore.org/documents/dcmi-terms/#terms-created) 

The range defined for dcterms:created is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myPicture dcterms:created "2003-04-10"^^dcterms:W3CDTF .

    ex:mySculpture dcterms:created "-500"^^xsd:gYear

    ex:myScript dcterms:created "1752"^^dcterms:W3CDTF ,
                                 "probably after 1752" .

    ex:mySculpture dcterms:created "approx. 500 B.C."

    ex:myData dcterms:title "Population estimates in Scandinavia" ;
              dcterms:created "2004-07-19"^^dcterms:W3CDTF ;
              dcterms:source ex:oldData .
    
    ex:oldData dcterms:title "World health report 2002 statistical annex" ;
               dcterms:created "2002-09-28"^^dcterms:W3CDTF .

### [dcterms:date](http://dublincore.org/documents/dcmi-terms/#terms-date) 

The range defined for dcterms:date is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myManuscript dcterms:date "1633"^^dcterms:W3CDTF .

### [dcterms:dateAccepted](http://dublincore.org/documents/dcmi-terms/#terms-dateAccepted) 

The range defined for dcterms:dateAccepted is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myThesis dcterms:dateAccepted "2010-05-07"^^dcterms:W3CDTF .

### [dcterms:dateCopyrighted](http://dublincore.org/documents/dcmi-terms/#terms-dateCopyrighted) 

The range defined for dcterms:dateCopyrighted is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myFoto dcterms:dateCopyrightes "2009-04-03"^^dcterms:W3CDTF .

### [dcterms:dateSubmitted](http://dublincore.org/documents/dcmi-terms/#terms-dateSubmitted) 

The range defined for dcterms:dateSubmitted is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myArticle dcterms:dateSubmitted "2011-07-09"^^dcterms:W3CDTF .

### [dcterms:identifier](http://dublincore.org/documents/dcmi-terms/#terms-identifier) 

The range defined for dcterms:identifier is the class of rdfs:Literal. Values used with dcterms:identifier have to be instances of this class. Therefore this property can only be used with literal values.

    ex:myWebsite dcterms:title "What's a URI and why does it matter?" ;
                 dcterms:identifier "http://www.ltg.ed.ac.uk/~ht/WhatAreURIs/"^^dcterms:URI .

    ex:myFile dcterms:title "Small and medium sized companies in Kathmandu" ;
              dcterms:identifier "03KTM147"^^ex:mylocalID .

    ex:myVideo dcterms:title "Medieval helpdesk with English subtitles" ;
               dcterms:created "2007"^^dcterms:W3CDTF ;
               dcterms:identifier "http://www.youtube.com/watch?v=pQHX-SjgQvQ&feature=player_embedded"^^dcterms:URI .
    
    ex:myMetadata dcterms:created "2010"^^dcterms:W3CDTF ;
                  dcterms:identifier "013234098"^^ex:myDatabaseIdentifier .

### [dcterms:issued](http://dublincore.org/documents/dcmi-terms/#terms-issued) 

The range defined for dcterms:issued is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myBook dcterms:issued "2009"^^dcterms:W3CDTF .

### [dcterms:modified](http://dublincore.org/documents/dcmi-terms/#terms-modified) 

The range defined for dcterms:modified is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:mySoftware dcterms:modified "2009-12-22"^^dcterms:W3CDTF ,
                                    "2010-01-08"^^dcterms:W3CDTF ,
                                    "2010-02-15"^^dcterms:W3CDTF .

### [dcterms:title](http://dublincore.org/documents/dcmi-terms/#terms-title) 

The range for dcterms:title is rdfs:Literal. So you can use dcterms:title only with literal values.

    ex:myFurniture dcterms:title "Alvar Aalto Chair No. 66" .

    ex:mySong dcterms:title "Autumn Leaves",
                            "The Dead Leaves" .

    ex:myPainting dcterms:title "La Joconde"@fre ,
                                "Mona Lisa"@eng ,
                                "La Gioconda"@ita .

    ex:myData dcterms:title "Data from a survey about the usage of metadata" .

### [dcterms:valid](http://dublincore.org/documents/dcmi-terms/#terms-valid) 

The range defined for dcterms:valid is the class of rdfs:Literal. Values used with this property therefore have to be literal values.

    ex:myDraft dcterms:valid "2007-05-06/2007-07-15" .

## Properties of the terms namespace used only with non-literal values 

### [dcterms:accrualMethod](http://dublincore.org/documents/dcmi-terms/#terms-accrualMethod) 

The range of dcterms:accrualMethod is the class dcterms:MethodOfAccrual. All values used with dcterms:accrualMethod have to be instances of this class. Therefore the property may only be used with non-literal values.

The domain of dcterms:accrualMethod is the class dcmitype:Collection. So dcterms:accrualMethod may be used only for the description of collections.

    ex:myCollection dcterms:title "Pottery in Scandinavia in the second half of 19th century" ;
                    dcterms:accrualMethod [rdfs:label "purchase"] .

### [dcterms:accrualPeriodicity](http://dublincore.org/documents/dcmi-terms/#terms-accrualPeriodicity) 

The range of dcterms:accrualMethod is the class dcterms:Frequency. All values used with dcterms:accrualPeriodicity have to be instances of this class. Therefore the property may only be used with non-literal values.

The domain of dcterms:accrualPeriodicity is the class dcmitype:Collection. So dcterms:accrualPolicy may be used only for the description of collections.

    ex:myCollection dcterms:title "Pottery in Scandinavia in the second half of 19th century" ;
                    dcterms:accrualPeriodicity [rdfs:label "irregular"] .

### [dcterms:accrualPolicy](http://dublincore.org/documents/dcmi-terms/#terms-accrualPolicy) 

The range of dcterms:accrualPolicy is the class dcterms:Policy. All values used with dcterms:accrualPolicy have to be instances of this class. Therefore the property may only be used with non-literal values.

The domain of dcterms:accrualPolicy is the class dcmitype:Collection. So dcterms:accrualPolicy may be used only for the description of collections.

    ex:myCollection dcterms:title "Pottery in Scandinavia in the second half of 19th century" ;
                    dcterms:accrualPolicy [ rdfs:label "Objects of this collection have to be 
                                           Scandinavian ceramics from 1940s to 1999s." ] .

### [dcterms:accessRights](http://dublincore.org/documents/dcmi-terms/#terms-accessRights) 

The range of dcterms:accessRights is the class dcterms:RightsStatement. Values used with this property have to be instances of the class RightsStatement and therefore non-literal values.

    ex:myDatabase dcterms:title "Data from my last evaluation" ;
                  dcterms:accessRights [rdfs:label "My colleagues only"] .

### [dcterms:audience](http://dublincore.org/documents/dcmi-terms/#terms-audience) 

dcterms:audience has a range of the class dcterms:AgentClass. Values used with this property therefore have to be non-literal values.

    ex:myTutorial dcterms:title "Advanced physic" ;
                  dcterms:audience [rdfs:label "elementary school pupils"] .

### [dcterms:conformsTo](http://dublincore.org/documents/dcmi-terms/#terms-conformsTo) 

dcterms:conformsTo has a range of the class dcterms:Standard. Values used with this property therefore have to be non-literal values.

    ex:myData dcterms:conformsTo <http://www.w3.org/2001/XMLSchema> .

### [dcterms:contributor](http://dublincore.org/documents/dcmi-terms/#terms-contributor) 

The range for dcterms:contributor is dcterms:Agent. All values used with this property have to be instances of the class [dcterms:Agent] . **dcterms:contributor must not be used with literal values**.

You may use dcterms:contributor only with non-literal values.

    ex:myMusic dcterms:contributor gnd:135066719 .
    
    gnd:135066719 foaf:familyName "Elliott" ;
                  foaf:givenName "Missy" ;
                  foaf:nick "Missy E" .

### [dcterms:coverage](http://dublincore.org/documents/dcmi-terms/#terms-coverage) 

dcterms:coverage has a range of the class dcterms:LocationPeriodJurisdication. All values used with dcterms:coverage have to be instances of this class. Therefore the property must only be used with non-literal values.

    ex:myYearbook dcterms:title "Demographic Development in Australia" ;
                  dcterms:coverage tgn:7000490 .
    
    tgn:7000490 ex:lat "25 00 00 S degrees minutes" ;
                ex:long "135 00 00 E degrees minutes" ;
                ex:name "Australia" .

### [dcterms:creator](http://dublincore.org/documents/dcmi-terms/#terms-creator) 

The range for dcterms:creator is dcterms:Agent. All values used with this property have to be instances of the class [dcterms:Agent] . **dcterms:creator must not be used with literal values**. You may use it only with non-literal values.

    ex:myBook dcterms:creator _shakespearesName .
    
    _:shakespearesName foaf:familyName "Shakespeare" ;
                       foaf:givenName "William" .

### [dcterms:educationLevel](http://dublincore.org/documents/dcmi-terms/#terms-educationLevel) 

dcterms:educationLevel has a range of the class dcterms:AgentClass. Values used with this property therefore have to be non-literal values.

    ex:myTutorial dcterms:title "Advanced physic" ;
                  dcterms:educationLevel [rdfs:label "3rd - 4th grade"] ;

### [dcterms:extent](http://dublincore.org/documents/dcmi-terms/#terms-extent) 

The range of dcterms:extent is the class dcterms:SizeOrDuration. All values used with dcterms:extent have to be instances of this class. Therefore the property may only be used with non-literal values.

    ex:myVideo dcterms:extent [rdf:value "21 minutes"] .

    ex:myVideo dcterms:extent [rdf:value "PT21M"^^xsd:duration] .

### [dcterms:format](http://dublincore.org/documents/dcmi-terms/#terms-format) 

The range of dcterms:format is the class dcterms:MediaTypeOrExtent. All values used with dcterms:format have to be instances of this class. Therefore the property may only be used with non-literal values.

    ex:myPicture dcterms:format mime:jpeg .

### [dcterms:hasFormat](http://dublincore.org/documents/dcmi-terms/#terms-hasFormat) 

This property is intended to be used with non-literal values.

    ex:myBook dcterms:creator gnd:118529501 ;
               dcterms:title "Sachsenspiegel, Auffs newe vbersehen mit Summarijs vnd Additionen" ;
               dcterms:date "1563"^^dcterms:W3CDTF ;
               dcterms:hasFormat ex:myScan .

### [dcterms:hasPart](http://dublincore.org/documents/dcmi-terms/#terms-hasPart) 

This property is intended to be used with non-literal values.

    <http://www.rijksmuseum.nl/meesterwerken> dcterms:title "The Masterpieces special" ;
                                              dc:contributor "Rijksmuseum Amsterdam" ;
                                              dcterms:hasPart ex:myPainting .

### [dcterms:hasVersion](http://dublincore.org/documents/dcmi-terms/#terms-hasVersion) 

This property is intended to be used with non-literal values.

    ex:mySong1 dcterms:identifier "mySong1"
               dcterms:title "Candle in the wind" ;
               dcterms:issued "1973"^^dcterms:W3CDTF;
               dcterms:description "Portayal of the life of Marilyn Monroe" ;
               dcterms:hasVersion ex:mySong2

### [dcterms:instructionalMethod](http://dublincore.org/documents/dcmi-terms/#terms-instructionalMethod) 

dcterms:instructionalMethod has a range of the class dcterms:MethodOfInstruction. Values used with this property therefore have to be non-literal values.

    ex:myTutorial dcterms:title "Advanced physic" ;
                  dcterms:InstructionalMethod [rdfs:label "experimental learning"] .

### [dcterms:isFormatOf](http://dublincore.org/documents/dcmi-terms/#terms-isFormatOf) 

This property is intended to be used with non-literal values.

    ex:myScan dcterms:issued "2009"^^dcterms:W3CDTF ;
              dcterms:isFormatOf [ rdfs:label "Eike von Repgow: Sachsenspiegel, Auffs newe vbersehen mit 
                                 Summarijs vnd Additionen ...; Leipzig 1561/1563" ] .

### [dcterms:isPartOf](http://dublincore.org/documents/dcmi-terms/#terms-isPartOf) 

This property is intended to be used with non-literal values.

    ex:myPainting dcterms:title "Still Life" ;
                  dc:creator "Mignon, Abraham" ;
                  dcterms:isPartOf <http://www.rijksmuseum.nl/meesterwerken> .

### [dcterms:isReferencedBy](http://dublincore.org/documents/dcmi-terms/#terms-isReferencedBy) 

This property is intended to be used with non-literal values.

    ex:myData dc:creator "Black, Carl" ;
              dc:contributor "White, Stuart" ;
              dcterms:title "Black and White" ;
              dcterms:date "1988"^^dcterms:W3CDTF ;
              dcterms:isReferencedBy ex:myArticle .

### [dcterms:isReplacedBy](http://dublincore.org/documents/dcmi-terms/#terms-isReplacedBy) 

This property is intended to be used with non-literal values.

    ex:myBestPractice dcterms:title "How to catch a fish" ;
                       dc:creator "Fishermans Union, Pensicola" ;
                       dcterms:issued "2009"^^dcterms:W3CDTF ;
                       dcterms:isReplacedBy ex:myNewBestPractice .

### [dcterms:isRequiredBy](http://dublincore.org/documents/dcmi-terms/#terms-isRequiredBy) 

This property is intended to be used with non-literal values.

    ex:mySoftware dcterms:title "Dia Diagram Editor" ;
                   dcterms:isRequiredBy ex:myDiagram .
     
     ex:myDiagram dcterms:title "Libraries Metadata Model" ;
                  dcterms:requires ex:mySoftware .

### [dcterms:isVersionOf](http://dublincore.org/documents/dcmi-terms/#terms-isVersionOf) 

This property is intended to be used with non-literal values.

    ex:mySong2 dcterms:identifier "mySong2"
               dcterms:title "Candle in the wind" ;
               dcterms:alternative "Goodbye England's Rose" ;
               dcterms:issued "1997"^^dcterms:W3CDTF ;
               dcterms:description "Tribut to the dead princess of Wales" ;
               dcterms:isVersionOf ex:mySong1 .

### [dcterms:language](http://dublincore.org/documents/dcmi-terms/#terms-language) 

The range of dcterms:language it the class dcterms:LinguisticSystem. All values used with dcterms:language have to be instances of this class. Therefore the property may only be used with non-literal values.

    ex:myBook dcterms:title "A great deliverance" ;
              dcterms:language [rdf:value "eng"^^dcterms:RFC4646] .

or

    ex:myBook dcterms:title "A great deliverance" ;
              dcterms:language <http://lexvo.org/id/iso639-3/eng>

    ex:myVideo dcterms:title "Charlie Wilson's War" ;
               dcterms:language <http://lexvo.org/id/iso639-3/eng> ,
                                <http://lexvo.org/id/iso639-3/hun> ,
                                <http://lexvo.org/id/iso639-3/tur> .

    ex:myVideo1 dcterms:title "Medieval helpdesk with English subtitles" ;
                dcterms:identifier "http://www.youtube.com/watch?v=pQHX-SjgQvQ&feature=player_embedded"^^dcterms:URI .
                dcterms:isVersionOf ex:myVideo2 ;
                dcterms:language <http://lexvo.org/id/iso639-3/nor> ,
                                 <http://lexvo.org/id/iso639-3/eng> .
     
    ex:myVideo2 dcterms:title "Book help (better verson)" ;
                dcterms:identifier "http://www.youtube.com/watch?v=UOorZQLsmuA&feature=related"^^dcterms:URI .
                dcterms:hasVersion ex:myVideo1 ;
                dcterms:language <http://lexvo.org/id/iso639-3/nor> .

    ex:mySong dcterms:title "The Power of Orange Knickers"
              dcterms:language _:eng
    
    _:eng rdfs:Label "English"
          ex:639-1 "en"
          ex:639-2 "eng"

### [dcterms:license](http://dublincore.org/documents/dcmi-terms/#terms-license) 

The range of dcterms:license is the class dcterms:LicenseDocument. Values used with this property have to be instances of the class LicenseDocument and therefore non-literal values.

    ex:mySoftware dcterms:title "GeoNetwork - Geographic Metadata Catalog" ;
                  dcterms:license <http://www.gnu.org/licenses/gpl.html> .
    
    <http://www.gnu.org/licenses/gpl.html> rdfs:label "GNU General Public License" .

### [dcterms:mediator](http://dublincore.org/documents/dcmi-terms/#terms-mediator) 

dcterms:mediator has a range of the class dcterms:AgentClass. Values used with this property therefore have to be non-literal values.

    ex:myTutorial dcterms:title "Advanced physic" ;
                  dcterms:mediator [rdfs:label "schoolteacher"] ;

### [dcterms:medium](http://dublincore.org/documents/dcmi-terms/#terms-medium) 

The range of dcterms:medium is the class dcterms:PhysicalMedium. All values used with dcterms:medium have to be instances of this class. Therefore the property may only be used with non-literal values.

The domain of dcterms:medium is the class dcterms:PhysicalResource. So dcterms:medium may be used only for the description of physical resources.

    ex:myPainting dcterms:medium _:oilOnWood
    
    _:oilOnWood rdfs:label "oil on wood"
                rdfs:label "oil"
                rdfs:label "wood"

### [dcterms:provenance](http://dublincore.org/documents/dcmi-terms/#terms-provenance) 

The range of the provenance property is the class dcterms:ProvenanceStatement. So you may use this property only with non-literal values.

    ex:myResource dcterms:title "Luxor Obelisk"
                  dctems:provenance [ rdfs:label "Originally located at the entrance to the Luxor temple the 
                                     obelisk came to Paris in 1836 as a gift by Muhammad Ali Pasha." ] .

    ex:myBook dcterms:title "The flea circus" ;
              dcterms:provenance _:thisProvenance
    
    _:thisProvenance ex:ownedBy "1829 - 1833; Jim Button" ,
                                "1833 - 1915; My Library" ,
                                "since 1915; Flea Academy" .

### [dcterms:publisher](http://dublincore.org/documents/dcmi-terms/#terms-publisher) 

The range for dcterms:publisher is dcterms:Agent. All values used with this property have to be instances of the class [dcterms:Agent] . **dcterms:publisher must not be used with literal values**. You may use it only with non-literal values.

    ex:myBook dcterms:publisher gnd: 2125990-2 ,
                               _:kniznajaPalata
    
    gnd:2125990-2 foaf:name "Rossijskaja Gosudarstvennaja Biblioteka ;
                  foaf:homepage "http://www.rsl.ru/" .
                  
    _:kniznajaPalata foaf:name "Knižnaja Palata"

### [dcterms:references](http://dublincore.org/documents/dcmi-terms/#terms-references) 

This property is intended to be used with non-literal values.

    ex:myArticle dcterms:references _:articlesReference .
    _:articlesReference dc:creator "Black, Carl" ;
                        dc:contributor "White, Stuart" ;
                        dc:title "Black and White"
                        dc:date "1988"^^dcterms:W3CDTF

### [dcterms:relation](http://dublincore.org/documents/dcmi-terms/#terms-relation) 

This property is intended to be used with non-literal values.

    ex:myArticle dcterms:title "Computational Surface and Roundness Metrology" ;
                  dc:creator "Muralikrishnan, Balasubramanian" , 
                             "Raja, Jayaraman" ;  
                  dcterms:relation <http://d-nb.info/1008973041> .

### [dcterms:replaces](http://dublincore.org/documents/dcmi-terms/#terms-replaces) 

This property is intended to be used with non-literal values.

    ex:myNewBestPractice dcterms:title "How to catch a fish" ;
                          dc:creator "Fishermans Union, Pensicola" ;
                          dcterms:issued "2011"^^dcterms:W3CDTF ;
                          dcterms:replaces ex:myBestPractice .

### [dcterms:requires](http://dublincore.org/documents/dcmi-terms/#terms-requires) 

This property is intended to be used with non-literal values.

    ex:myGame dcterms:requires [rdfs:label "audio"] ,
                               [rdfs:label "video"].

### [dcterms:rights](http://dublincore.org/documents/dcmi-terms/#terms-rights) 

The range of dcterms:rights is the class dcterms:RightsStatement. Values used with this property have to be instances of the class RightsStatement and therefore non-literal values.

    ex:myPicture dcterms:title "You and me" ;
                  dcterms:rights <http://creativecommons.org/licenses/by/3.0/legalcode> .

    ex:myDocuments dcterms:title "Diaries of Juanita Ramirez"
                   dcterms:rights _:accessConditions
    
    _:accessConditions dcterms:title "Access to my stuff"
                       dcterms:description "Resources under this right can only be read, searched and 
                       used by members of the myProject" .

### [dcterms:rightsHolder](http://dublincore.org/documents/dcmi-terms/#terms-rightsHolder) 

The range for dcterms:rightsHolder is dcterms:Agent. All values used with this property have to be instances of the class [dcterms:Agent] . **dcterms:rightsHolder must not be used with literal values**. You may use it only with non-literal values.

    ex:myFilm dcterms:rightsHolder gnd:39454-3 .
    
    gnd:39454-3 foaf:name "Bundesarchiv Koblenz" ;
                foaf:homepage "http://www.bundesarchiv.de/index.html.de" .

### [dcterms:source](http://dublincore.org/documents/dcmi-terms/#terms-source) 

This property is intended to be used with non-literal values.

    ex:myData dcterms:title "Australian Birth Rates 2000 - 2010" ;
              dcterms:source [rdfs:label "Yearbooks of Demographic Development in Australia"] .

### [dcterms:spatial](http://dublincore.org/documents/dcmi-terms/#terms-spatial) 

dcterms:spatial has a range of the class dcterms:Location. All values used with dcterms:spatial have to be instances of this class. Therefore the property must only be used with non-literal values.

    ex:myData dcterms:title "Analysis of rocks collected in Perth" ;
              dcterms:spatial _:thisPlace .
    
    _:thisPlace ex:east "115.85717" ;
                ex:north "-31.95301" ;
                ex:name "Perth, W. A." .

    ex:myData dcterms:title "The growth of trees in the suptropical highlands" ;
              dcterms:spatial _:Cwb .
    
    _:Cwb rdfs:label "Cwb"
          dc:source "Köppen-Geiger Climate Classification" ;
          ex:mainClimates "warm temperate" ;
          ex:precipitation "winter dry" ;
          ex:temperature "warmest month averaging below 22°C" .

### [dcterms:subject](http://dublincore.org/documents/dcmi-terms/#terms-subject) 

This property is intended to be used with non-literal values.

    ex:myBook dcterms:title "Inviato alla Biennale : Venezia, 1949 - 2009" ;
              dcterms:subject <http://www.labiennale.org/en/Home.html> .
    
    <http://www.labiennale.org/en/Home.html> dcterms:title "La Biennale di Venezia"

    ex:myVideo dcterms:title "My Winter Wonderland" ;
               dcterms:subject <http://id.loc.gov/authorities/sh88004323#concept> .
    
    <http://id.loc.gov/authorities/sh88004323#concept> rdfs:label "Cross-country skiing--Skating" .

    ex:myData dcterms:title: "Transports in Kazakhstan 2000 - 2010"
              dcterms:subject ex:W03_7 ,
              dcterms:subject ex:G06_3
                                             
    ex:W03_7 rdf:type skos:Concept ;
             prefLabel "W03.7" ;
             skos:altLabel "Freight Transport" ;
             skos:broader ex:W03 ;
             skos:narrower ex:W03_72 ,
                           ex:W03_75 .
    
    ex:G06_3 rdf:type skos:Concept ; 
             prefLabel "G06_3 ;
             skos:altLabel "Kazakhstan" ;
             skos:broader ex:G06 ;
             skos:narrower ex:G06_31 ,
                           ex:G06_35 .

    ex:myLaw dcterms:title "KONSTYTUCJA RZECZYPOSPOLITEJ POLSKIEJ"
             dcterms:subject _:polska
    
    _:polska rdfs:label "Rzeczpospolita Polska"@pol ,
                         "Republic of Poland"@eng .

    ex:mySong dcterms:title "Candle in the wind" ;
              dcterms:subject gnd:118583549 .
    gnd:118583549 foaf:_familyName "Monroe" ;
                  foaf:_givenName "Marilyn" ;
                  <http://rdvocab.info/ElementsGr2/dateOfBirth> "1926"^^dcterms:W3CDTF ;
                  <http://rdvocab.info/ElementsGr2/dateOfDeath> "1962"^^dcterms:W3CDTF .

### [dcterms:temporal](http://dublincore.org/documents/dcmi-terms/#terms-temporal) 

dcterms:temporal has a range of the class dcterms:PeriodOfTime. All values used with dcterms:temporal have to be instances of this class. Therefore the property must only be used with non-literal values.

    ex:myData dcterms:title "Transports in Kazakhstan 2000 - 2010"
              dcterms:temporal _:thisPeriod .
    
    _:thisPeriod ex:start "2000"^^dcterms:W3CDTF ;
                 ex:end "2010"^^dcterms:W3cDTF .

    ex:myData dcterms:title "Analysis of rocks collected in Perth" ;
              dcterms:temporal _:thisPeriod .
    
    _:thisPeriod ex:start "Cambrian period" ;
                 ex:scheme "Geological timescale" ;
                 ex:name "Phanerozoic Eon" .

### [dcterms:type](http://dublincore.org/documents/dcmi-terms/#terms-type) 

The range of dcterms:type is rdfs:Class. Values used with dcterms:type may only be non-literal values.

    ex:myPainting dcterms:type dctype:StillImage .
    
    dctype:StillImage rdfs:label "Still Image" .

    ex:myStuff dcterms:type dctype:InteractiveResource , 
                            dctype:Text .
    
    dctype:InteractiveResource rdfs:label "Interactive Resource" .
    
    dctype:Text rdfs:label "Text" .

    ex:myStuff dcterms:type _:PCGameType ,
                            dctype:Software .
    
    _:PCGameType rdfs:label "PC Game" .
    
    dctype:Software rdfs:label "Software" .

    ex:myEvent dcterms:type _:conference .
    
    _:conference rdfs:label "Conference"@eng ,
                            "Konferenz"@ger ,
                            "съезд"@rus .

## Properties of the terms namespace, that may be used with literal and non-literal values 

### [dcterms:abstract](http://dublincore.org/documents/dcmi-terms/#terms-abstract) 

There is no range defined for dcterms:abstract. Therefore you can use it with literal values

    ex:myBook dcterms:title "The Foundations of Programm Verification" ;
              dcterms:abstract "This revised edition provides a precise mathematical background to 
                               several program verification techniques. It concentrates on those 
                               verification methods that have now become classic, such as the 
                               inductive assertions method of Floyd, the axiomatic method of Hoare, 
                               and Scott's fixpoint induction. The aim of the book is to present these 
                               different verification methods in a simple setting and to explain their 
                               mathematical background. In particular the problems of correctness and 
                               completeness of the different methods are discussed in some detail and 
                               many helpful examples are included." .

    ex:myBook dcterms:title "Delvig and Kjuchelbeker"
              dcterms:abstract "The book is a collection of works of two poets - contemporaries 
                               and friends of Pushkin - A. A. Delvig and V. K. Kjuchelbeker. It 
                               includes poems and prosa by Kjuchelbeker, parts of his diary, the 
                               poem Jurij and Xenia and reviews by Delvig. The attachment presents 
                               some retrospections to Delvig and Kjuchelbeker. A detailed biographic 
                               description tells us something about the life of the poets"@eng ,
                               "Сборник впервые обединяет произведения двух поетов - современиков 
                               и друзей Пушкина - А. А. Дельвига и В. К. Кюхельбекера. Наряду со 
                               стихотворениями в книгу вклучены проза Кюхельбекера, фрагменты из его 
                               дневника, поема Юрий и Ксения, а также рецензии Дельвига. В Приложении 
                               печатаются воспоминания о Дельвиге и Кюхельбекерею. Подробные 
                               биографические очерки рассказывают о жизненном пути поэтов."@rus

and with non-literal values.

    ex:myBook dcterms:title "Computational Surface and Roundness Metrology" ;
               dcterms:abstract <http://www.springerlink.com/content/M7V5444582756209/primary> .

### [dcterms:description](http://dublincore.org/documents/dcmi-terms/#terms-description) 

There is no range defined for dcterms:description. Therefore you can use it with literal values

    ex:myObjects dcterms:title "Bugs from New Zealand" ;
                 dcterms:description "A box of ten bugs collected in New Zealand between 1845 and 1846" .

and with non-literal values.

    ex:myMusic dcterms:title "Thriller" ;
               dcterms:description <http://en.wikipedia.org/wiki/Thriller_(album)> .

### [dcterms:tableOfContents](http://dublincore.org/documents/dcmi-terms/#terms-tableOfContents) 

There is no range defined for dcterms:tableOfContents. Therefore you can use it with literal values.

    ex:myFile dcterms:title "Remains of Claire Klawitter" ;
              dcterms:tableOfContents "Diary 1822 - 1824 -- 20 pictures of Indian farmers 
              -- 5 letters to Rudi Ratlos -- 1 map of North India" .

and with non-literal values

    ex:myJournal dcterms:title "Cäcilia ; eine Zeitschrift für die musikalische Welt" ;
                  dcterms:tableOfContents <http://www.digizeitschriften.de/content/PPN472885294_0020/800/0/00000003.jpg> ,
                                          <http://www.digizeitschriften.de/content/PPN472885294_0020/800/0/00000004.jpg> ,
                                          <http://www.digizeitschriften.de/content/PPN472885294_0020/800/0/00000005.jpg> .

# Legacy namespace 

For properties of the legacy namespace neither domain nor range is defined. So all properties of the legacy namespace can be used either with literal values or with non-literal values.

## Properties of the legacy namespace 

### [dc:contributor](http://dublincore.org/documents/dcmi-terms/#elements-contributor) 

You may use dc:contributor with literal values

    ex:myMusic dc:contributor "Snoop Dogg" .

and with non-literal values.

    ex:myMusic dc:contributor gnd:135066719 .
    
    gnd:135066719 foaf:familyName "Elliott" ;
                  foaf:givenName "Missy" ;
                  foaf:nick "Missy E" .

### [dc:coverage](http://dublincore.org/documents/dcmi-terms/#elements-coverage) 

You may use dc:coverage with literal values

    ex:myData dc:title "Transports in Kazakhstan 2000 - 2010"
              dc:coverage "2000 - 2010" ,
                          "Kazakhstan" .

    ex:myData dc:title "Analysis of rocks collected in Perth" ;
              dc:coverage "Perth, W. A." .

and with non-literal values.

    ex:myYearbook dc:title "Demographic Development in Australia" ;
                   dc:coverage tgn:7000490 .
     
     tgn:7000490 ex:lat "25 00 00 S degrees minutes" ;
                 ex:long "135 00 00 E degrees minutes" ;
                 ex:name "Australia" .

### [dc:creator](http://dublincore.org/documents/dcmi-terms/#elements-creator) 

You may use dc:creator with literal values

    ex:myBook dc:creator "Shakespeare, William" .

and with non-literal values.

    ex:myBook dc:creator _shakespearesName .
     
     _:shakespearesName foaf:familyName "Shakespeare" ;
                        foaf:givenName "William" .

### [dc:date](http://dublincore.org/documents/dcmi-terms/#elements-date) 

You may use dc:date with literal values

    ex:myManuscript dc:date "1633"^^dcterms:W3CDTF .

and with non-literal values.

    ex:myDraft dc:date _:thisValidity .
    
    _:thisValidity ex:start "2007-05-06"^^dcterms:W3CDTF ;
                   ex:end "2007-07-15"^^dcterms:W3CDTF .

    ex:mySculpture dc:date _:mySculptureDate .
     _mySculptureDate ex:year "500" ;
                      ex:qualifer "approx." ;
                      ex:epoch "B.C." .

### [dc:description](http://dublincore.org/documents/dcmi-terms/#elements-description) 

You may use dc:description with literal values,

    ex:myHerbs dc:title "Coriandrum sativum" ;
               dc:description "Coriandrum sativum or Coriander is a herb used in Europe, North Africa 
               and Asia. It belongs to the familiy of Apiaceae and ist growing to 20 inch." .

and with non-literal values.

    ex:myHerbs dc:title "Coriandrum sativum" ;
               dc:description <http://en.wikipedia.org/wiki/Coriander> .
    
    <http://en.wikipedia.org/wiki/Coriander> dc:title "Coriander" ;
                                             dc:contributor "Wikipedia" .

### [dc:format](http://dublincore.org/documents/dcmi-terms/#elements-format) 

You may use dc:format with literal values

    ex:myPicture dc:format "40 x 512 pixels" .

and with non-literal values.

    ex:myPicture dc:format mime:jpeg .

### [dc:identifier](http://dublincore.org/documents/dcmi-terms/#elements-identifier) 

You may use dc:identifier with literal values

    ex:myVideo dc:title "My first article about metadata"
                dc:identifier "My Favorite Journal 3 (2), 14-25 (2010)" .

and with non-literal values

    ex:myVideo dc:title "My first article about metadata"
               dc:identifier _:myCitation .
    
    _:myCitation ex:jtitle "My Favorite Journal"
                 ex:volume "3"
                 ex:issue "2"
                 ex:spage "14"
                 ex:date "2010" .

### [dc:language](http://dublincore.org/documents/dcmi-terms/#elements-language) 

You may use dc:language with literal values

    ex:mySong dc:title "The Power of Orange Knickers"
              dc:language "English"

    ex:mySong dc:title "The Power of Orange Knickers"
              dc:language "eng"^^dcterms:RFC4646 .

and with non-literal values.

    ex:myBook dc:title "A great deliverance" ;
               dc:language <http://lexvo.org/id/iso639-3/eng> .

### [dc:publisher](http://dublincore.org/documents/dcmi-terms/#elements-publisher) 

You may use dc:publisher with literal values

    ex:myData dc:creator "Hubble Telescope";
               dc:publisher "University of Nowhere" ,
                            "All Your Data Inc. .

and with non-literal values.

    ex:myBook dc:publisher gnd: 2125990-2 ,
                                 _:kniznajaPalata
     
     gnd:2125990-2 foaf:name "Rossijskaja Gosudarstvennaja Biblioteka ;
                   foaf:homepage "http://www.rsl.ru/" .
                   
     _:kniznajaPalata foaf:name "Knižnaja Palata"

### [dc:relation](http://dublincore.org/documents/dcmi-terms/#elements-relation) 

You may use dc:relation with literal values

    ex:myArticle dc:title "Introduction to Fitting Substitute Geometry" ;
                  dc:relation "Muralikrishnan, Balasubramanian and Raja, Jayaraman: Computational Surface and Roundness 
                              Metrology III, 2009" .

and with non-literal values

    ex:myBook dc:title "Computational Surface and Roundness Metrology" ;
               dc:creator "Muralikrishnan, Balasubramanian" , 
                          "Raja, Jayaraman" ;  
               dc:relation <http://d-nb.info/1008973041> .

### [dc:rights](http://dublincore.org/documents/dcmi-terms/#elements-rights) 

You may use dc:rights with literal values

    ex:myVideo dc:rights "May be used only by members of the myProject" .

    ex:myBook dc:title "News from the South" ;
              dc:rights "http://creativecommons.org/licenses/by-nd/3.0/legalcode"^^dcterms:URI .
              dc:rights "Attribution-NoDerivs 3.0 Unported" .

and with non-literal values.

    ex:myPicture dc:title "You and me" ;
                  dc:rights <http://creativecommons.org/licenses/by/3.0/legalcode> .

### [dc:subject](http://dublincore.org/documents/dcmi-terms/#elements-subject) 

There is no range defined for dc:subject. Therefore you can use it with literal values

    ex:myManual dc:title "How to get an aircraft"
                dc:subject "aircraft" ;
                           "leasing" .

and with non-literal values.

    ex:myVideo dc:title "My Winter Wonderland" ;
                dc:subject <http://id.loc.gov/authorities/sh88004323#concept> .
     
     <http://id.loc.gov/authorities/sh88004323#concept> rdfs:label "Cross-country skiing--Skating" .

### [dc:title](http://dublincore.org/documents/dcmi-terms/#elements-title) 

It is recommended to use for titles literal values. But there are important **uses with non-literal values** as well. To do so you have to use dc:title, because dc:title may be used with literal values

    ex:myPainting dc:title "La Joconde"@fre ,
                            "Mona Lisa"@eng ,
                            "La Gioconda"@ita .

and with non-literal values.

    ex:myBook dc:title _:thisTitle .
    
    _:thisTitle ex:greekAlphabet "Οιδίπους Τύραννος" ;
                ex:latinAlphabet "Oidipous Tyrannos" .

    ex:myScript1 dcterms:title "Nibelungenlied Handschrift B" ;
                 dc:title _:nibelungenlied .
                 
    ex:myScript2 dcterms:title "Nibelungenlied Handschrift C" ;
                 dc:title _:nibelungenlied
    
    _:nibelungenlied skos:prefLabel "Der Nibelunge Not" ;
                     skos:altLabel "Nibelungenlied" ,
                                   "Nibelungenklage" ,
                                   "Nibelungensage" ;
                     dcterms:description "The Nibelungenlied exists of 39 aventiuren created between 1180 and 1210" .

### [dc:type](http://dublincore.org/documents/dcmi-terms/#elements-type) 

You may use dc:type with literal values

    ex:myEvent dc:type "Conference" .

and with non-literal values.

    ex:myEvent dcterms:type _:conference .
     
     _:conference rdfs:label "Conference"@eng ,
                             "Konferenz"@ger ,
                             "съезд"@rus .

