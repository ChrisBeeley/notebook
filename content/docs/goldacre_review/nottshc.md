---
title: "Nottinghamshire Healthcare NHS Trust"
weight: 99
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

A considerable amount of policy and guidance relating to data and analytics in the NHS has been published in recent times, with the publication of the  Goldacre Review (commissioned by the DHSC) and the  Data Saves Lives policy from DHSC. The papers are closely aligned and Data Saves Lives accepts in whole or in part all of the  summary recommendations from the Goldcare Review. The recommendations cover modernising NHS service analytics, open working methods, privacy, Trusted Research Environments, information governance, ethics, and data curation. This paper will focus on modernising  service analytics, open working methods, and data curation. The other recommendations are relevant to the Trust insofar as it shares data with ICB colleagues and with national bodies, but much of this work will be planned and coordinated at the ICB/ national  level.

# What should Nottinghamshire Healthcare NHS Trust do

Nottinghamshire Healthcare NHS Trust (NHC) is part of an [analytically able ICS](https://healthandcarenotts.co.uk/) and employs three analytical teams with good working relationships: Applied Information, Performance, and CDU data science. The teams combine expertise in data curation and management, performance and quality surveillance, and data science methods and analytical pipelines. 

NHC could become one of the "data pioneer" trusts (or form part of a "data pioneer" ICS) that the report recommends in [NHSA 7](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis/better-broader-safer-using-health-data-for-research-and-analysis#modernising-nhs-service-analytics) by building on the work already happening at the trust.

## Reproducible analytical pipelines

> Reproducibility is the cornerstone of analysis. Analysts should get the same results as each other when using the same data and methods. Since 2017, analysts in the UK public sector have made their analysis more efficient and reproducible using a methodology called Reproducible Analytical Pipelines (RAP). They advocate writing analysis as code and using open-source tools, version control software, and dependency management... Analysis can be higher quality through automated data validation and testing, more impactful through interactive data presentation, more prompt and less costly by removing manual steps, and more powerful by using advanced analytics.

(source: [Government Reproducible Analytical Pipelines strategy](https://analysisfunction.civilservice.gov.uk/policy-store/reproducible-analytical-pipelines-strategy/))

> [summary recommendation 17]: Embrace modern, open working methods for NHS data analysis by committing to Reproducible Analytical Pipelines (RAP) as the core working practice that must be supported by all platforms and teams; make this a core focus of NHS analyst training.

(source: [Goldacre review](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis/better-broader-safer-using-health-data-for-research-and-analysis#summary-recommendations))

Reproducible analytic pipelines are analytical tasks that are entirely expressed in code (often, but not always, R or Python). At a minimum they will:

* minimise manual steps, for example copy-paste, point-click or drag-drop operations. Where it is absolutely necessary to include a manual step in the process this must be documented
* be built using open source software for data management, analysis and visualisation which is available to anyone, preferably R or python
* be open to anyone for review and re-use, with all code shared openly through open standard file and code sharing platforms such as GitHub (sharing data itself is a separate issue from sharing code, as discussed below, and should be handled very differently)
* guarantee an audit trail using version control software (such as Git, or in services such as GitHub) which systematically track exactly who has made which changes or contributions to the code, which characters and lines were modified, when, and – as appropriate – why
* follow existing good practice for quality assurance
* deepen technical and quality assurance processes with code review by peers
* contain well-commented code and have documentation embedded and version controlled within the work, rather than saved elsewhere

(source: [Goldacre review](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis/better-broader-safer-using-health-data-for-research-and-analysis#modernising-nhs-service-analytics))

They offer a number of advantages over typical workflows such as Excel such as:

* Efficiency- the pipeline can be re-run with new data with very little effort
* Accuracy- because all data manipulation is performed within code, the data and analysis can be checked easily after the analysis is complete
* Sharing and collaboration- RAPs can be shared and collaborated on between teams and organisations simply using tools like git and GitHub
* Transparency- analysis can be shared as code without the sharing of data, which allows external stakeholders to satisfy themselves that the analysis was performed correctly, even if the data is withheld.

Using RAPs as suggested by government and by the Goldcare review will take a considerable amount of changes in working practice and training, but it can be begun slowly. The ultimate prize is considerable time saved from repetitive tasks and analysts being able to carry out more meaningful and strategic analyses.

### Recommendation

The internal data science team in CDU is already looking to produce a RAP of a monthly analytic task. To begin to mainstream the methodology the Trust should identify a business critical analytic task which is suitable to be processed in a RAP compliant way (not all processes are amenable to this process with the current data architecture). The CDU data science team could offer assistance and training in this regard, with the ultimate aim being that this process would sit within the Trust's mainstream analytic functions.

## Open code

> We will: begin to make new source code that we produce or commission open and reusable by default (with clear exceptions) and publish it under appropriate licences to encourage further innovation (such as MIT and OGLv3, alongside suitable open data sets or dummy data). Subject to consultation, the relevant policies will also aim to be open and reusable...)

(source: [Data Saves Lives](https://www.gov.uk/government/publications/data-saves-lives-reshaping-health-and-social-care-with-data/data-saves-lives-reshaping-health-and-social-care-with-data#working-with-partners-to-develop-innovations-that-improve-health-and-care))

> it is crucial that the core working practices, such as sharing code, are implemented as a norm throughout  the system [i.e. of analytical teams], because of the problems that closed working can create around quality, safety, usability, credibility, and review

(source: [Goldacre review](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis/better-broader-safer-using-health-data-for-research-and-analysis#modernising-nhs-service-analytics))

### Recommendations

NHC should actively seek permission to open source code that refers to database schema from proprietary databases. [OpenSAFELY](https://www.opensafely.org/) publishes code from databases produced by [TPP](https://tpp-uk.com/) ([with their permission](https://github.com/nhsx/open-source-policy/issues/6#issuecomment-1138403404)), and NHC should do the same, as well as approaching the other main EHR database vendor the trust has engaged, [Servelec](https://www.servelec.co.uk/) (regarding the [Rio database](https://www.servelec.co.uk/product-range/rio-epr-system/))

<!-- Open 
- Open code
- Stop doing data curation differently, to variable and unseen standards, duplicatively  in every team, data centre, and project
- Meet this challenge with systematic curation work, devoted teams, shared working  practices, shared code, shared tools, and shared documentation -->

