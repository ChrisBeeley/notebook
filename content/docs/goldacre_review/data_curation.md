---
title: "Data Curation"
weight: 6
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

> The Association of the British Pharmaceutical Industry (ABPI) have said that they estimate 80% of all work on an analysis project using NHS data is spent on this data preparation, and they have previously recommended that 80% of the national resource deployed on data science in the NHS should therefore be spent on optimising data curation

## The problem

Even for something as simple as hypertension there are hundreds of definitions and SNOMED codes that some individuals may think do (or don't) constitute hypertension. 

"Creating these lists is therefore complex and difficult work. To do it, the team need a number of skills which may not all be embodied in one individual. They will need domain knowledge about clinical medicine, to spot the need to include a code such as “arteriolar nephritis”. They will also need domain knowledge about how health data works: they will need to know what SNOMED-CT codes are, how they can be searched, how codes are nested within a poly-hierarchy (and then challenging details such as how parent-child relationships in the poly-hierarchy can create overlapping conflicts, which can in turn change when individual codes move between nodes in different releases); they also need knowledge of how clinicians use clinical systems, what is recorded, how it is coded, and what the strengths and weaknesses of the data are (collectively this is often called “clinical informatics”)"

* It is not possible to produce a single "hypertension" codelist
* Codelists are often imperfect, but secret, either because nobody thinks to share them or because the team who produced them wants to use them for a competitive advantage
* Many patients don't have a diagnosis at all, but it must be inferred instead from their clinical information (systolic BP, for example)
* Diagnoses may change and go out of date- is a 15 year old diagnosis of hypertension still valid?

## How data management is currently implemented

> It is clear that this work is typically done in siloes, with minimal formal open sharing, to the frustration of many analysts. However, it is also clear that there is a vast amount of deep expertise currently left untapped and mostly undocumented, in individuals and teams across the system with domain knowledge around clinical relevance, the structure and meaning of individual data elements, the strengths and weaknesses of different national and local datasets, their provenance, and so on. This is **captured in local documents at best, but often resides in the tacit knowledge of individuals and teams** [emphasis added], and shared through informal personal relationships, because of an absence of any expectation or technical facility for wider sharing.

## The problems

### Data inconsistencies

Data is held with diverse schemata (which are not shared) which means that SQL code is not at all portable between organisations, even when it's the same data

### Requesting datasets in code
