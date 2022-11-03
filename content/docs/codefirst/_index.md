---
title: "Code first!"
weight: 5
# bookFlatSection: false
# bookToc: true
# bookHidden: false
bookCollapseSection: true
# bookComments: false
# bookSearchExclude: false
---

## Background

There is a strong case for increasing the use of code first analytics in government (e.g. in the analytic function's [RAP strategy](https://analysisfunction.civilservice.gov.uk/policy-store/reproducible-analytical-pipelines-strategy/)) as well as in [the NHS](https://journals.sagepub.com/doi/full/10.1177/0141076820930666), with the recently published [Goldacre review](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis), in particular, being enthusiastically received by healthcare staff, with many of its recommendations being accepted in the recent DHSC policy [Data Saves Lives](https://www.gov.uk/government/publications/data-saves-lives-reshaping-health-and-social-care-with-data/data-saves-lives-reshaping-health-and-social-care-with-data). RAP here refers to a method of code based analytics which minimises manual steps, instead expressing all data and analytic operations in code which can be freely rerun and inspected during and after the analysis.

Another important dimension of the recommendations of the RAP strategy and the Goldacre review is the potential for the sharing of code to radically improve the transparency, accuracy, and efficiency of analytic work, even sharing within organisations but especially sharing between organisations.

There are many individuals and groups across the NHS who are carrying out excellent work using code first and RAP compliant tools, and indeed the Goldacre review names both [NHS-R](https://nhsrcommunity.com/) and [NHSPycom](https://nhs-pycom.net/) as being excellent community  projects bringing together users of these tools. However, it is clear that these practices are far from widespread- many analysts lack the skills and support to use these tools, and even some of those who do have the skills are forbidden to do so on corporate IT equipment

## Current issues in code first analytics

The are several barriers to adopting code first analytics identified in the Goldacre review and in [previous reports](https://www.health.org.uk/publications/understanding-analytical-capability-in-health-care). They are outlined briefly following.

### Tooling

Many organisations are reluctant to allow analysts to use open source tools of any kind, and in particular Python. Python is seen as a potential attack vector, both in terms of users installing packages even from official sources (which have no checks) and with respect to its being a general purpose programming language which could theoretically be used by a bad actor. The situation is not as severe in R, perhaps partly just because of there being more name recognition with R, although it is true today that analysts are not allowed to install R and/ or official packages.

### Workforce

There are several problems relating to code first analytics with respect to workforce, some of which are more general problems with the analytical workforce, but they nonetheless represent a barrier to working in this way. There is a lack of coding skills across the NHS, and many analysts will know just Excel and SQL. Those individuals who do have coding and data science experience will often leave for the private sector because of poor recognition of their skills (and therefore poor salary) in the pay structure of the NHS, *Agenda for Change*. A further problem is a lack of good structures around the profession, few heads of profession and chief analysts, a lack of community, and a lack of knowledge about code first methods in senior analytical roles across the NHS

### Openness

The recently published [*Data Saves Lives*](https://www.gov.uk/government/publications/data-saves-lives-reshaping-health-and-social-care-with-data/data-saves-lives-reshaping-health-and-social-care-with-data#working-with-partners-to-develop-innovations-that-improve-health-and-care) includes a strong message that code that is procured should be procured on the condition that it is released as open source (as a default, with clear exceptions). However, there is still very patchy sharing of code by individuals employed by the NHS, and open sourcing is rarely stipulated in procurement contracts (and therefore it is rarely done).

Some organisations fear the consequences of sharing code, either that they will prove to have made a mistake or that the code they share will somehow make it easier for people without authorisation to access confidential data. In particular, many organisations fear to share database schema, even though [government advice clearly states that it is safe](https://www.gov.uk/government/publications/open-source-guidance/when-code-should-be-open-or-closed).

## Reproducible analytical pipelines

The Goldacre review promotes that idea of Reproducible Analytical Pipelines (RAP) and they have found widespread adoption in central government who have a [clear strategy on RAP](https://analysisfunction.civilservice.gov.uk/policy-store/reproducible-analytical-pipelines-strategy/) endorsed by the head of the analysis function. Briefly, RAP is a process in which code is used to minimise manual, undocumented steps, and a clear, properly documented process is produced in code which can reliably give the same result from the same dataset.

RAP has proved itself to be of great benefit in [increasing accuracy and efficiency in central government](https://analysisfunction.civilservice.gov.uk/support/reproducible-analytical-pipelines/rap-case-studies/) and implementing RAP is one of the summary recommendations of the Goldacre review

> Embrace modern, open working methods for NHS data analysis by committing to Reproducible Analytical Pipelines (RAP) as the core working practice that must be supported by all platforms and teams; make this a core focus of NHS analyst training.

Concerted action is required to give analysts the skills and tools they need to reap the benefits of RAP and the other uses of code first analytics. This action requires a team of experts who can educate and support analysts and analytical leaders across the system, and the composition and programme of work for this team will be described following.

## Key activities

* A programme of engagement with senior managers
* A programme of work with analysts
* An open library of code for the NHS

More detail will now be given about each strand of activity.

## Programme of engagement with senior managers

Samantha Riley and the “Making Data Count” (MDC) team have produced a considerable suite of documentation and training materials which describe the reasons why switching to reporting using SPC (Statistical Process Control) can significantly raise the quality of decision making in an organisation. SPC is a highly technical topic, but the Making Data Count team has managed to make this topic approachable to all. This has significantly raised  the profile of statistical best practice across the NHS.

At the same time, the MDC team has also run a huge engagement programme, visiting boards across the country to educate them about the use of SPC, as well as doing webinars, meetings, presentations, etc. in order to bring this message to a wide audience. 

The code first/ RAP community could adopt a similar approach. The Goldacre review provides a blueprint for action around code first analytics and RAP but its penetration outside of individuals who are already interested in these methods is potentially quite weak. A team could be grown and funded to tackle the two barriers which were tackled so well by the MDC team. 
 
A properly resourced team could produce a wide range of resources for managers in the NHS, including but not limited to videos, webinars, blog posts, and training sessions. The team could also actively take this message both to trust boards and to senior IT professionals across organisations in the NHS. Sessions and materials for boards would focus on the potential benefits of adopting code first solutions to analytics, and ensuring that they understand that there is a vibrant community and dedicated teams who are able to provide advice, support, and training to teams within each organisation. The focus with IT professionals would be on understanding security practices in respect of sharing code and database schema, discussing the potential for harm from open source programming languages and packages, and ensuring that they feel that they are able to manage this risk appropriately in their organisation. Showing off the sheer number of NHS organisations who use R and Python safely every day would also be a key message, as well as organisations in other industries (for example the MoD, the Bank of England, and Google). 

## Supplemental materials

* Understanding analytical capability in health care, [Health Foundation](https://www.health.org.uk/publications/understanding-analytical-capability-in-health-care)