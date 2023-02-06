---
title: "Data science for Evidence"
weight: 50
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

The SU data science team are currently looking at how we can use DS tools to help with evidence review. I know nothing whatsoever about this so I'm going to do some reading on it and I may as well write it here in case it helps anyone else. So far I have a list of links, I will flesh this document out with these and more in due course.

## Metaverse

Metaverse is "An R ecosystem for meta-research". It is a meta package which installs:

* synthsisr
    * Import, assemble and de-duplicate bibliographic data 
* litsearchr
    * Quasi-automatic search strategy development for systematic reviews
* revtools
    * Article screening for evidence synthesis using manual or visual methods
* metaDigitise
    * High-throughput, reproducible extraction of data from figures 
* robvis
    * Publication quality risk-of-bias figures 

## synthsisr

This package is designed mainly to simplify download and export of bibliographic information:

* Read and assemble bibliographic files
    * synthesisr can read any BibTex or RIS formatted bibliographic data files. It detects whether files are more bib-like or ris-like and imports them accordingly
* Deduplicate bibliographic data
    * Many journals are indexed in multiple databases, so searching across databases will retrieve duplicates. After import, synthesisr can detect duplicates and retain only unique bibliographic records using a variety of methods such as string distance or fuzzy matching records
* Write bibliographic files
    * To facilitate exporting results to other platforms after assembly and deduplication, synthesisr can write bibliographic data to .ris or .bib files

## litsearchr

[Litsearchr has a GUI](https://elizagrames.shinyapps.io/litsearchr/) which is in early development

> [The litsearchr package for R is designed to partially automate search term selection and writing search strategies for systematic reviews](https://elizagrames.github.io/litsearchr/litsearchr_vignette.html)

Litsearchr identifies keywords

## Appendix

https://rmetaverse.github.io/

http://eppi.ioe.ac.uk/cms/Default.aspx?tabid=3677

https://elizagrames.github.io/litsearchr/

https://www.sciencedirect.com/science/article/pii/S235271102200125X

https://training.cochrane.org/handbook/current/chapter-04#section-4-6-6-2
