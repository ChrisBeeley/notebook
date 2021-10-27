---
title: "Deidentification"
weight: 700
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Deidentification of data

The team and I do a [lot](https://github.com/CDU-data-science-team/pxtextmining) of [stuff](https://github.com/CDU-data-science-team/experiencesdashboard) with [patient experience data ](https://github.com/nhs-r-community/pxtextmineR) and it can be tricky to reuse it without thoroughly redacting it because people put personal information in there- sometimes asking for a response, by email or telephone. It's a bit of an unusual case because the data _should_ be anonymous- there's no need to identify patients in it at all, I just want the text of their experience, but in practice it _isn't_. 

Having some way of automatically redacting patient experience data to a high enough standard to reuse the data would be very useful, and to that end I made a [pull request](https://github.com/nhsx/nhsx-internship-projects/pull/4) on the NHSX internship site to see if they could look at it with a PhD student.

Jonny Pearson very helpfully gave me some links to some resources to improve it and I need to digest the contents of a bit, may as well do it here in case it helps anyone else (or future me, for that matter :smile:). We have:

* [Introduction to anonymisation](https://go.privitar.com/rs/588-MYA-374/images/2021-07-Privitar-Bristows-Intro_to_Anonymisation.pdf)
* [Anonymisation: managing data protection risk code of practice](https://ico.org.uk/media/1061/anonymisation-code.pdf)
* [A Review of Anonymization for Healthcare Data](https://arxiv.org/pdf/2104.06523.pdf)

You may just want the links and ignore my witterings below of course :wink:.

## Introduction to anonymisation

At a simple level, organisations who are trying to anonymise data will mask _direct identifiers_. Some data, like diagnosis or medication is not identifiable. Some data, like name or phone number is identifiable, and these variables are known as direct identifiers. Masking the direct identifiers should in theory make it impossible to identify individuals, but [Sweeney](https://dataprivacylab.org/projects/identifiability/index.html) showed that combining _quasi identifiers_ could lead individuals to be identified. Quasi identifiers are values that are not directly identifying on their own, but may be identifying in combination. Sweeney suggested that this kind of _linkage attack_ can be prevented by generalising some of the data. For example, using year and month of birth rather than exact birth date. 

Sweeney codified these ideas within a concept called [k-identity](https://dataprivacylab.org/dataprivacy/projects/kanonymity/kanonymity.html). The k variable gives the minimum number of people who are indistinguishable from each other in the dataset. A k-anonymous dataset means that each row is indistinguishable from k-1 other rows. For example, when k is 5 each individual is indistinguishable from 5 other individuals. 

### The modern big data landscape

In more recent times the data available about each individual has proliferated and additional controls are often required in order to thoroughly anonymise data. Controlling the environment can help with this, for example by having data accessed in a secure area where data access is monitored, or providing data in a secure way that doesn't allow it to be recombined with other data, like a [trusted research environment](https://www.hdruk.ac.uk/wp-content/uploads/2021/04/Goldacre-Review-TRE-Response.pdf). 

Environmental controls do not generally affect the utility of data for analysis, but have an associated in cost, control of use, etc. 

### Summary

* Deidentification comes at a cost- either in terms of the usefulness of the data or the cost of managing environmental access to data
* Deidentification can be very difficult when there is high dimensional or high frequency data
* It is not always obvious what will and what won't lead to reidentification, and there are many high profile failure of deidentified data (e.g. [Netflix](https://www.wired.com/2007/12/why-anonymous-data-sometimes-isnt/))

## Aggregation

