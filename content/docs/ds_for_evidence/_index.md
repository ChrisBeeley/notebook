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

## Metaverse

[Metaverse](https://rmetaverse.github.io/) is "An R ecosystem for meta-research". It is a meta package which installs:

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

### synthsisr

This package is designed mainly to simplify download and export of bibliographic information:

* Read and assemble bibliographic files
    * synthesisr can read any BibTex or RIS formatted bibliographic data files. It detects whether files are more bib-like or ris-like and imports them accordingly
* Deduplicate bibliographic data
    * Many journals are indexed in multiple databases, so searching across databases will retrieve duplicates. After import, synthesisr can detect duplicates and retain only unique bibliographic records using a variety of methods such as string distance or fuzzy matching records
* Write bibliographic files
    * To facilitate exporting results to other platforms after assembly and deduplication, synthesisr can write bibliographic data to .ris or .bib files

### litsearchr

[Litsearchr has a GUI](https://elizagrames.shinyapps.io/litsearchr/) which is in early development

> [The litsearchr package for R is designed to partially automate search term selection and writing search strategies for systematic reviews](https://elizagrames.github.io/litsearchr/litsearchr_vignette.html)

Litsearchr identifies keywords by looking at an existing set of search results using algorithms such as Rapid Automatic Keyword Extraction (RAKE) (or a simple ngram search). The package can then group the keywords into concepts and then write a boolean search strategy. This can then be checked for precision and recall against a "Gold standard" of papers which should be returned by the search. 

### revtools

Revtools is a package which allows the user to interact with their literature search using code as well as with a GUI. It includes:

* Locating duplicates
* Screening duplicates
* Screening of titles
* Screening of abstracts
* Creation of topic models to cluster and show similarity between papers

### metaDigitise

This package can extract data points from graphics, as well as computing statistics for data extracted from a graphic. It includes GUI elements to assist with the extraction.

### robvis

The robvis package takes the summary table from risk-of-bias assessments and produces plots formatted according to the assessment tool used

## Resources for automation in systematic reviews

[A variety of point and click tools (with fairly restricted licences, on the whole)](http://eppi.ioe.ac.uk/cms/Default.aspx?tabid=3677)

## Litstudy

This is a [Python package to help with literature reviews](https://github.com/NLeSC/litstudy). It includes:

* Data import and merge
* Statistics (publication year, country of origin, number of authors etc.)
* Network analysis (co-citation network)
* Topic modelling (automatic topic discovery based on the words used in documents abstracts)

## Appendix

### Cochrane guidelines on the use of automated tools in paper selection

https://training.cochrane.org/handbook/current/chapter-04#section-4-6-6-2
