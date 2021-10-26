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