---
layout: post
title:  "DCMI-IAC Kickoff Call"
year: 2015
month: 11
day: "06"
categories: minutes
author:
attendees: Stuart, Tom, Kai, Adrian, Kevin, Andrew, Joachim, Konstantin, Paul
regrets: Tim
---

- (Short) Introduction by Kai: What is this all about?
- Report by Tom Baker about current DCMI infrastructure
  - Walk through: [DCMI Infrastructure Inventory][dcmi-infrastructure]
  - Tom proposes to maintain a list of purls with targets on GitHub
  - Domains: dublincore.org/net, lrmi.net, foaf-project.org, xmlns.com?
  - Stuart provides more detail to OCS, OJS, 1700 USD per year for external hosting
- Current activities, particularly within the LD4PE project regarding
  - reimplementation of the website (Joseph Chapman, Tom Baker)
- Website is main issue, horror to maintain
- Wordpress 
- RDF AP Database as an example "how things happen"
- Questions: 
  - What can we do with such systems?
  - How would we handle this in the future, if we could advise before developments starts?
- Paul: 
  - Typically a lot of such systems exist and are used actively for a time and then become archives (ideally)
  - Static site generators (Hugo?) to keep static HTML pages
  - Example: [Jekyll][jekyll], supported by GitHub
  - This is the static website generator I have adopted (prefer it to Jekyll mainly because it is is *much* faster): [Hugo][hugo]
  - JiscMail might not be reliable in the future
- Tom: 
  - DCMI website is currently semi-static, good for archiving, but hard to maintain
  - Jiscmail is very important, contains most of the history of DCMI, currently we rely on them to keep the archive
- Stuart: 
  - Is everything worth saving?
- Tom: 
  - Moinmoin Wiki pages have been archived as HTML pages
- Kai:
  - Static HTML pages plus database dump as archival record works well, but should be done in a consistent and coumented way
- Tom: 
  - DCMI Terms publishing system is also a burdon, source available, but hard to maintain
- Andrew:
   - ALA ALCTS/LITA Metadata Standards Committee blog: [Metaware][metaware]
- Paul: 
  - Core and chore, maybe we should classify accordingly
- Ideas and first insights by the participants (=you!)
  - Adrian, Research Project Manager: 
    - working on the Website
  - Kevin, researcher UNC:
    - static website generator
    - website
  - Andrew, University of Houston:
    - Generate engagement with community
    - Collaboration metaware
    - interested in purl.org
    - static site generators (jekyll)
  - Joachim, ZBW, Scientific Software Developer:
    - Drupal website
    - no experience with Wordpress or static site generators
  - Konstantin, UB Mannheim
    - consolidating workflows
    - static site generations
    - work on tools for site geration for ontologies
  - Paul, Head of Strategy, Edina:
    - static site generators
    - Core Chore thing, develop sustainable and archiving strategy
    - community profiles, lrmi    
  - Kai:
    - strategy
    - vocabulary management
    - site generators as part of stragey
  - Tom:  
    - vocabulary management
  - Stuart:
    - DCMI needs to be independent of Tom and Stuart
    - need to get past that
- Find a date for the second call
  - Doodle for a call very soon (next week)
  - Create a list of all issues and work areas
  - Then get started with most interesting or most pressing parts

[dcmi-infrastructure]: http://wiki.dublincore.org/index.php/DCMI_Technical_Board/DCMI_Infrastructure_Inventory
[jekyll]: https://jekyllrb.com/
[hugo]: https://gohugo.io
[metaware]: http://metaware.buzz/
