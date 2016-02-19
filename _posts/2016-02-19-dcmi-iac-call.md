---
layout: post
year: "2016"
month: "02"
day: "12"
category: minutes
author: ""
attendees: "Stuart, Andrew, Jon, Joachim, Kai"
regrets: Tom
published: true
title: "DCMI-IAC Call"
---

### Static Site Generators vs. Wordpress, continued...

#### Kai: experimented with Jekyll and Hugo
- Can Hugo be extended?
- Hugo provides short codes for easier development
- Hugo is a simple system: single cross-platform executable
- Jekyll may be more difficult to set up
- Concerned with Ruby dependencies over the long term

#### Jon: building documentation site in Hugo
- Hugo is simple
- Is the new Jekyll system supported better?
- Lector Python static site generator
- has single executable
- administrative interface in browser

#### Andrew: experimented with Jekyll
- Jekyll is difficult to manage on local machines
- easy to deploy a site with Github pages

#### Discussion
- Need to be able to sync pages across multiple local systems
- Work on shared repository, probably on Github
- [prose.io](http://prose.io) makes it easy to publish Markdown files to Github
- Not many people will need edit access, most pages will stay static
- How stable is the content, how much is there, and how often will it be updated?
- There is a time limit to design and implement a new architecture: May 2017
- Wordpress is easy to use, not necessarily the most important consideration for long term
- Wordpress is the most accessible to a non-technical user
- Possibility for a hybrid architecture?
- static content over the long term in shared repository
- dynamic content in Wordpress
- Difficult to publish specifications in Wordpress
- Versioning is a big advantage for static site generators hosted remotely
- Technical debt may be resolved over the long term with good documentation
- LRMI Wordpress is a front end for a triple store
- Split makes it difficult to create a cohesive web presence
- Need to develop a methodology for analyzing content and then choose a direction
- Possible to integrate Github managed static sites through Wordpress
- Systems must be managed by a staff position
- montly stipend for infrastructure manager in discussion
- volunteers can contribute as they will
- Local systems require long term maintenance commitment and pose security issues
- DCMI should downsize to reflect the current state of activity
- Static site generators are a technical moving target
- dependencies change and can break a site
- best to choose a system with an active support community
- single executable options (Hugo, Lector) are less likely to break
- Documentation is a good fit for static pages and technically proficient personnel
- Front page, newsy content is more dynamic and more likely to be maintained by less technically proficient personnel

#### Recommendations
- Jon: static site generator needs to be very stable, Jekyll provides stability but ease of use is an issue, Lector might be a good system
- Joachim: avoid Wordpress, has set up Drupal with all content local to avoid security issues, update migrations are a burden
- Andrew: static site generators are great for a number of reasons, but they require a substantial technical investment in the system
- Kai: Wordpress updates are generally painless and reliable, use Wordpress for daily activities for now and investigate ways to integrate static sites

#### Action Items
- investigate how to incorporate static pages in Wordpress
- experiment with shared git repository  [DCMI IAC Demo Site](https://github.com/metaweidner/dcmi-iac/tree/gh-pages)
- continue looking into new systems

