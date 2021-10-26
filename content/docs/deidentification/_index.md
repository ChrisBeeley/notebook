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

## Deidentification of data

The team and I do a [lot](https://github.com/CDU-data-science-team/pxtextmining) of [stuff](https://github.com/CDU-data-science-team/experiencesdashboard) with [patient experience data ](https://github.com/nhs-r-community/pxtextmineR) and it can be tricky to reuse it without thoroughly redacting it because people put personal information in there- sometimes asking for a response, by email or telephone. It's a bit of an unusual case because the data _should_ be anonymous- there's no need to identify patients in it at all, I just want the text of their experience, but in practice it _isn't_. 

Having some way of automatically redacting patient experience data to a high enough standard to reuse the data would be very useful, and to that end I made a [pull request](https://github.com/nhsx/nhsx-internship-projects/pull/4) on the NHSX internship site to see if they could look at it with a PhD student.

Jonny Pearson very helpfully gave me some links to some resources to improve it and I need to digest the contents of a bit, may as well do it here in case it helps anyone else (or future me, for that matter :smile:). We have:

* [Introduction to anonymisation](https://go.privitar.com/rs/588-MYA-374/images/2021-07-Privitar-Bristows-Intro_to_Anonymisation.pdf)
* [Anonymisation: managing data protection risk code of practice](https://ico.org.uk/media/1061/anonymisation-code.pdf)
* [A Review of Anonymization for Healthcare Data](https://arxiv.org/pdf/2104.06523.pdf)

You may just want the links and ignore my witterings below of course :wink:.

### Introduction to anonymisation

At a simple level, organisations who are trying to anonymise data will mask _direct identifiers_. Some data, like diagnosis or medication is not identifiable. Some data, like name or phone number is identifiable, and these variables are known as direct identifiers. Masking the direct identifiers should in theory make it impossible to identify individuals, but [Sweeny](https://dataprivacylab.org/projects/identifiability/index.html) showed that combining _quasi identifiers_ could lead individuals to be identified.