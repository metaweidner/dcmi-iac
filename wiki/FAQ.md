---
layout: page
title: FAQ
---

## Frequently Asked Questions (FAQ) 

| 

**Note** : This "work in progress" is meant to replace the [legacy DCMI FAQ](http://dublincore.org/resources/faq/), which was last updated in 2003.<sup id="cite_ref-0" class="reference"><a href="#cite_note-0">[1]</a></sup> Many of the concepts and issues covered in the 2003 FAQ are now covered in a draft [DCMI Glossary](http://metaweidner.github.io/dcmi-iac/wiki/Glossary "Glossary"), which is likewise a work in progress. Good questions are posted here as they are asked, so not all questions have answers. Work typically begins with a "long answer", and when the long answer is complete (or at least stable), it will be summarized on this page as a "short answer". Readers interested in discussing answers are cordially invited to do so on the [dc-glossary mailing list](http://www.jiscmail.ac.uk/lists/dc-glossary.html), which is open to any interested member of the public.

 |

<dl>
<dt>How should <a href="http://metaweidner.github.io/dcmi-iac/wiki/Glossary/Encoding_Scheme" title="Glossary/Encoding Scheme">syntax encoding schemes</a> be encoded in HTML5 given that the &lt;scheme&gt; element of the &lt;meta&gt; tag has been deprecated?
</dt>
<dd>Short answer needed (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/HTML5_Scheme" title="FAQ/HTML5 Scheme">long answer</a>).
</dd>
</dl><dl>
<dt>What is the difference between dc:creator and dcterms:creator, and why have the fifteen elements of the Dublin Core been declared using two separate namespaces?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/DC_and_DCTERMS_Namespaces" title="FAQ/DC and DCTERMS Namespaces">long answer</a>): The <a href="http://purl.org/dc/elements/1.1/" class="external free" rel="nofollow">http://purl.org/dc/elements/1.1/</a> namespace, coined in 2000 and commonly used with the prefix "dc:", was used for the fifteen properties of "the Dublin Core" unconstrained with formal domains and ranges. As a result, dc:creator was used either with the name of a creator, or with a URI (or blank node) representing the creator. In response to evolving notions of best practice for RDF vocabularies, the DCMI Usage Board assigned formal domains and ranges to the fifteen elements. Not wishing to "invalidate" existing data by constraining the meaning of existing properties, the Usage Board created fifteen new properties as sub-properties of the fifteen "dc:" properties and assigned them URIs under the <a href="http://purl.org/dc/terms/" class="external free" rel="nofollow">http://purl.org/dc/terms/</a> namespace. DCMI encourages users to use the /terms/ properties because their semantics are more precise, but the /elements/1.1/ properties have not been deprecated and remain popular as an alternative.  
</dd>
</dl><dl><dt>Why have DCMI Metadata Terms been declaring using the W3C RDF Vocabulary Description Language ("RDF Schema") and not the W3C Web Ontology Language (OWL)?
</dt></dl><dl>
<dt>What is the DCMI Abstract Model, and what is its current status?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/DCMI_Abstract_Model" title="FAQ/DCMI Abstract Model">long answer</a>):
</dd>
</dl><dl>
<dt>How are agent "roles" expressed in Dublin Core metadata (e.g., a "contributor" who is, more specifically, a "translator")?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/Agent_roles" title="FAQ/Agent roles">long answer</a>)
</dd>
</dl><dl>
<dt>What does "Dublin Core Application Profile" mean today?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/Application_Profile" title="FAQ/Application Profile">long answer</a>):
</dd>
</dl><dl>
<dt>Because a date doesn't have an URI, is it not possible to link in a semantic way based on date?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/Linking_data_on_dates" title="FAQ/Linking data on dates">long answer</a>):
</dd>
</dl><dl>
<dt>If libraries move away from catalogs in the old sense, would they move towards something like a search interface? What would this new interface look like?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/Beyond_library_catalogs" title="FAQ/Beyond library catalogs">long answer</a>):
</dd>
</dl><dl>
<dt>As a production cataloger of original material, I am not seeing Linked Data as saving labor for me and my colleagues, only as providing opportunities for others to leverage our work. What's the business model for supporting the work of a national bibliography, i.e., for verifying and controlling data?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/Linked_Data_ROI_for_catalogers" title="FAQ/Linked Data ROI for catalogers">long answer</a>):
</dd>
</dl><dl>
<dt>How are the persistence and reliability of metadata required for the operation and management of a given library, museum, etc. assured if records are "everywhere and nowhere"?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/Metadata_persistence_and_reliability" title="FAQ/Metadata persistence and reliability">long answer</a>):
</dd>
</dl><dl>
<dt>What do you do when you disagree with triples assigned to your item (i.e., statements made by others about your own resources)?
</dt>
<dd>Short answer (see also <a href="http://metaweidner.github.io/dcmi-iac/wiki/FAQ/Dubious_triples" title="FAQ/Dubious triples">long answer</a>):
</dd>
</dl>
### References 

1. ↑ [http://dublincore.org/resources/faq/](http://dublincore.org/resources/faq/)

