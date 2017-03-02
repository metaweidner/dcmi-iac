---
layout: page
title: Linking data on dates
---

## Because a date doesn't have an URI, is it not possible to link in a semantic way based on date? 

A date can be represented in RDF by a typed literal -- that is, a string value identified as being of a specific type to distinguish it from other types. So the string "1984" can be labeled as following, for example, a W3C Date and Time Format which specifies that a string consisting of four numbers is to be interpreted as a "year". In RDF terminology, this designation is called an RDF Datatype and is equivalent, in DCMI terminology, to the Syntax Encoding Scheme. When used as the title of a resource, the string "1984" would not normally be identified as a year. When used as a value for the publication date, however, the string "1984" -- identified as a year -- could be matched against other typed-literal values of the same, or comparable, type, and therefore "linked". Note that the matching takes place on triple objects only, as the date string cannot be the subject of a triple because it has no URI -- for example, "get the URIs of resources published in the year 1984". In principle, one might assign a URI to a date, but assigning URIs would require time, effort, and a maintenance commitment; it is more appropriate to assign a URI to an event (something occurring at a specific time and place).

2011-10-26: [Gordon Dunsire](http://metaweidner.github.io/dcmi-iac/wiki?title=User:GordonDunsire&action=edit&redlink=1 "User:GordonDunsire (page does not exist)") and [Tom Baker](http://metaweidner.github.io/dcmi-iac/wiki/User:TomBaker "User:TomBaker")

