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

## Programme of work with analysts

To be successful the programme would need to engage with a wide range of analysts for a diverse set of purposes. Fundamentally, the aims would be:

* Train a critical mass of healthcare analysts to use RAP methods ([Embrace modern, open working methods for NHS data analysis]({{< relref "#reproducible-analytical-pipelines" >}}))

A similar approach could be adopted engaging with analysts, and indeed looking at the MDC model it is clear that they have been successful at engaging at all levels, from coalface analysts to board members. Work with analysts would naturally have a practical focus, again through videos, blogs, webinars, and training sessions. Through these means the benefits of the approach could be demonstrated as well as efforts made to emphasise that, with the right training and support, these methods can be used by anyone. Specific training could be offered on a bespoke basis to particular teams or organisations who need particular help (or who wish to become outstanding) but much of the work of the team would be compiling and showing off the wide range of materials and community projects which already exist to help people to use RAP and code first methods.

## Open library of code

There are pockets of good practice all over the health and social care system and there are many great pieces of analytic work already shared in code. For example, the PHE produced [COVID dashboard](https://github.com/publichealthengland/coronavirus-dashboard) and the RCPCH [Digital Growth Charts API Server](https://github.com/rcpch/digital-growth-charts-server) . Many analysts and teams also share smaller pieces of work and useful packages for R and Python that lend themselves to reuse, for example the NHS-R community GitHub repo [demos and how to’s](https://github.com/nhs-r-community/demos-and-how-tos) which contains many snippets of code and longer scripts for a wide variety of purposes, for example common tasks reporting with RMarkdown, several scripts that interact with nationally held APIs of interest to healthcare analysts, and many other useful examples.
 
The problem in the system at the moment is not only that individuals do not share their code- many do. A fundamental problem is that there has been no concerted effort around the knowledge management processes that would be necessary to produce one of the recommendations of the Goldacre report- “a curated national open library of NHS analyst code”. There are three main areas of improvement that could be made in order to produce a useful library of code that finds wide adoption in health and care analytic teams. Firstly, existing code that is shared with an open licence needs to be found, and its content (and the authors of the content) made more prominent in a nationally visible resource. Secondly, analysts that are already sharing code (and those that are not) need to be encouraged to share code that is of high quality and sufficiently intelligible and generic to be worthy of reuse. Code of this kind is likely to be of a higher standard regardless of whether it is shared and this goal should be represented to the analysts as something that will often produce better code in the interests of the analysts themselves. Thirdly, analysts who are already in the habit of writing analytic code and reusing open code (as well as those that are not) need to be encouraged to be critical consumers of the resource, using the code, finding fault with it, filing issues, making pull requests where appropriate, and so on.
 
Producing an open library of code would produce a highly useful resource for training as well as everyday practice. There would be several components to the work to make it successful. In the first phase there would be wide engagement, firstly of individuals creating open source code and materials and secondly of individuals who do or might in the future make use of shared code (there would, of course, be overlap between these two groups). There would be an attempt to collate and summarise existing material as well as engagement with analytic teams in regard of what other resources might be useful, what languages they should be written in, the possible formats that they could be presented in, and so on. 

With the first engagement stage complete work could begin on the resource. It is likely to contain code written in at least two languages (R and Python) and may also include other languages (Julia, SQL, Bash...). It is highly likely that it would be presented as a book, with chapters, online, in a similar way to The Turing Way https://the-turing-way.netlify.app/welcome but there are other formats and standards that could be considered (for example, audio or video segments that link out to individual GitHub repos on particular subjects). The format and content of the work should be considered in detail in the engagement phase prior to this one. As the content begins to take shape, further engagement work could take place to ensure that the content is comprehensible and useful and to encourage analysts to use the work as well as to make contributions to it. A larger piece of work could also take place to find gaps in the library and to attempt to commission solutions or find existing ones. Where no solution can be found, the data scientist working on the library could write the code, or if it is too technical or difficult could attempt to induce an individual or team to produce it.
 
This piece of work would bring about a very concrete change in that it would produce a highly useful tool for learning and training as well as for day to day work. The engagement and work which occurred in order to produce a diverse library from a range of individuals working in health and care would also be likely to lead to better communication between analysts, better visibility of open work and the individuals engaged in it, and hopefully lasting cultural change. Individuals engaged in producing and using the library would be more likely to write better, more generic code, and to seek open code solutions for their day to day tasks rather than writing their own. With the right support, the library could itself help to encourage other collaborative pieces of work based on the shared interests of the users and creators of the library (who, of course, overlap). This work would, it is hoped, feed back into the library too, creating a virtuous circle of open material and collaboration leading to larger pieces of collaborative analytic work, which themselves can be written into the library.

## Funding

The project described is ambitious in scope and requires a robust team to deliver it. Naturally, the level of funding would influence the amount of work which is feasible.

### £250K per annum

This level of funding would pay for approximately one 8C, an 8A, and two 7s. The 8C would be expected to do engagement work with senior managers and IT professionals and to set the strategy and focus for the whole team. The 8A could be responsible for high level planning and supervision across the whole workstream, as well as contributing code and other materials to the training/ engagement programme and the open code library. The 7s would likely focus on a language each, ideally, one R and one Python. This team would be able to produce a suite of materials across the range of workstreams and a code library built with the analytical community that addresses many of their challenges.

### £500K per annum

TBC

## Supplemental materials

* Understanding analytical capability in health care, [Health Foundation](https://www.health.org.uk/publications/understanding-analytical-capability-in-health-care)