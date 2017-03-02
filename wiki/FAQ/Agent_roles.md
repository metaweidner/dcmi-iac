---
layout: page
title: Agent roles
---

## How are agent "roles" expressed in Dublin Core metadata (e.g., a "contributor" who is, more specifically, a "translator")? 

From [https://www.jiscmail.ac.uk/cgi-bin/webadmin?A2=ind1110&L=DC-GENERAL&P=3741](https://www.jiscmail.ac.uk/cgi-bin/webadmin?A2=ind1110&L=DC-GENERAL&P=3741)

    I need to record at least two specific contributor roles in a way consistent
    with Dublin Core, unfortunately I haven't found the solution as to how to
    call them nor how to input the credits.
    
    First, the person responsible for implementing the DC structure within the
    system and therefore responsible for the DC-oriented metadata architecture
    being right or wrong (Maybe I would call this role "Metadata programmer").
    
    Second, the person responsible for inputting the metadata for each digital
    object. I could call this "Metadata creator".
    
    Now, how do I this?
    
    <dc:contributor role="Metadata programmer">Momme, Sondra</dc:contributor>
    <dc:contributor role="Metadata creator">Smith, John</dc:contributor>
    
    ...?
    
    Same for the person who scanned a physical photograph...
    
    <dc:contributor role="Scanner">Mills, Joe</dc:contributor>
    
    Should that form be correct, had I better use natural language as in the
    examples or established codes such as
    
    Data manager [dtm] or Programmer [prg] (which?) for the first one
    Markup editor [mrk] for the second one
    from
    http://www.loc.gov/marc/relators/relaterm.html
    ?

