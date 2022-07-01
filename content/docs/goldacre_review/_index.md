---
title: "Goldacre Review"
weight: 3
bookCollapseSection: true
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookComments: false
# bookSearchExclude: false
---

# Better, Broader, Safer: Using Health Data for Research and Analysis

These are my notes from the material in the [Goldacare Review](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis). Please note that if you're not me and you're reading this I am only making notes about the bits that particularly pertain to me as a data scientist working in an NHS provider trust. For example, I think trusted research environments are a great idea, but it's not of particularly great interest to me in terms of my work, so I'm skimming over those bits. I'm interested in how we use data at the coalface from within an organisation (or ICS, IG permitting) and in particular how we use data to inform decision making and ensure that staff and patients are getting the best outcomes possible (clinical and experiential).

Note that the material is provided under the [OGL version 3](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/), and I am complying with the licence by reusing the material with proper attribution and a link to the licence. I read a lot of stuff, code and prose, that is produced with public money without an open licence so I would like to take this opportunity to thank the authors and publishers for opening the material in this way. 

## Terms of reference

[verbatim from document]

* How do we facilitate access to NHS data by researchers, commissioners, and innovators, while preserving patient privacy?
* What types of technical platforms, Trusted Research Environments (TREs), and data flows are the most efficient, and safe, for which common analytic tasks?
* How do we overcome the technical and cultural barriers to achieving this goal, and how can they be rapidly overcome?
* Where (with appropriate sensitivity) have current approaches been successful, and where have they struggled?
* How do we avoid unhelpful monopolies being asserted over data access for analysis?
* What are the right responsibilities and expectations on open and transparent sharing of data and code for arm’s length bodies, clinicians, researchers, research funders, electronic health records and other software vendors, providers of medical services, and innovators? And how do we ensure these are met?
* How can we best incentivise and resource practically useful data science by the public and private sectors? What roles must the state perform, and which are best delivered through a mixed economy? How can we ensure true delivery is rewarded?
* How significantly do the issues of data quality, completeness, and harmonisation across the system affect the range of research uses of the data available from health and social care? Given the current quality issues, what research is the UK optimally placed to support now, and what changes would be needed to optimise our position in the next 3 years?
* If data is made available for secondary research, for example to a company developing new treatments, then how can we prove to patients that privacy is preserved, beyond simple reassurance?
* How can data curation best be delivered, cost effectively, to meet these researchers’ needs? We will ensure alignment with Science Research and Evidence (SRE) research priorities and Office for Life Sciences (OLS) (including the data curation programme bid).
* What can we take from the successes and best practice in data science, commercial, and open source software development communities?
* How do we help the NHS to analyse and use data routinely to improve quality, safety and efficiency?

## Summary

### Key principles

#### Good defaults- make good practice the norm, not the exception

* "Create an ‘exceptions framework’ whereby publicly funded code can be closed [only by] by prior arrangement if this meets NHS and UKplc strategic objectives"
* "**it is crucial that** [emphasis added] the core working practices [of [RAP]({{< ref "open-working.md#reproducible-analytical-pipelines-rap" >}})], such as sharing code, are implemented as a norm throughout the system, because of the problems that closed working can create around quality, safety, usability, credibility, and review"

#### Workforce

* "Point and click tools have their place, but "[they] can only be [produced] by teams that understand the true underpinning reality of how patient data is generated, extracted, prepared and used across the system; who have RAP and computational skills... Any solution that appears to not entail this kind of process, and workforce, is simply hiding the work, by commissioning it in less effective and closed means, or similar activity"
* "there is an almost limitless array of self-directed online teaching through services such as Coursera, or some MOOCs (Massive Open Online Courses), but no clear signposting or curation of ‘journeys’ through these courses, or guidance on which to choose"


### Modernising NHS service analytics

* WIP

### Modern, open working methods for NHS data analysis

* Open 4. Create an ‘exceptions framework’ whereby publicly funded code can be closed by prior arrangement if this meets NHS and UKplc strategic objectives

Note that good practice around code sharing *is good practice around coding*. Good code should *never* include any personal information, whether it's being shared or not. 

### The challenge of privacy in health data
### Trusted Research Environments
### Information governance, ethics and participation
### Data curation
### Strategy

## Summary recommendations

### Platforms and security

1. Build trust by taking concrete action on privacy and transparency: trust cannot be earned through communications and public engagement alone.

2. Ensure all NHS data policies actively acknowledge the shortcomings of ‘pseudonymisation’ and ‘trust’ as techniques to manage patient privacy: these outdated techniques cannot scale to support more users (academics, NHS analysts, and innovators) using ever more comprehensive patient data to save lives.

3. Build a small number of secure analytics platforms – shared ‘Trusted Research Environments’ – then make these the norm for all analysis of NHS patient records data by academics, NHS analysts and innovators, wherever there is any privacy risk to patients, unless those patients have consented to their data flowing elsewhere. Every new TRE brings a risk of duplicated effort, duplicated information governance, duplicated privacy risks, monopolies on access or task, and obstructive divergence around data curation and similar activity: there should be as few TREs as possible, with a strong culture of openness and re-use around all code and platforms.

4. Use the enhanced privacy protections of TREs to create new, faster access rules and processes for safe users of NHS data; ensure all TREs publish logs of all activity, to build public trust.

5. Map all current bulk flows of pseudonymised NHS GP data, and then shut these down, wherever possible, as soon as TREs for GP data meet all reasonable user needs.

6. Use TREs – where all analysts work in a standard environment – as a strategic opportunity to drive modern, efficient, open, collaborative approaches to data science.

### Modern, open working methods for NHS data

7. Promote and resource ‘Reproducible Analytical Pathways’ (RAP, a set of best practices and training created in ONS) as the minimum standard for academic and NHS data analysis: this will produce high quality, shared, reviewable, re-usable, well-documented code for data curation and analysis; minimise inefficient duplication; avoid unverifiable ‘black box’ analyses; and make each new analysis faster.

8. Ensure all code for data curation and analysis paid for by the state through academic funders and NHS procurement is shared openly, with appropriate technical documentation, to all data users. Data preparation, analysis and visualisation is complex technical work, requiring collaboration by many individuals, who may never meet, in a range of organisations, across the NHS and other sectors. The only way to manage this shared complexity is by sharing information, as in other technical fields.

9. Recognise software development as a central feature of all good work with data. UKRI/NIHR should provide open, competitive, high status, standalone funding for software projects and developers working on health data. Universities should embrace research software engineering (RSE) as an intellectually and academically creative collaborative discipline, especially in health, with realistic salaries and recognition.

10. Bridge the gap between health research and software development: train academic researchers and NHS analysts in contemporary computational data science techniques, using RAP where appropriate; offer ‘onboarding’ training for software developers and data scientists who are entering health services research and epidemiology; use in-person and online training; make online resources openly available where possible.

11. Note that ‘open code’ is different to ‘open data’: it is reasonable for the NHS and government to do some analyses discreetly without sharing all results in real time.

### Data curation and knowledge management

12. Stop doing data curation differently, to variable and unseen standards, duplicatively in every team, data centre, and project: recognise NHS data curation as a complex, standalone, high status technical challenge of its own.

13. Meet this challenge with systematic curation work, devoted teams, shared working practices, shared code, shared tools, and shared documentation; driven by open competitive funding to develop new shared curation methods and tools, and to manually curate data for individual datasets and fields.

14. Use TREs as an opportunity to impose standards on how commonly used datasets are stored, and curated into analysis-ready tables.

15. Create an open online library for NHS data curation code, validity tests, and technical documentation with dedicated staff who have appropriate skills in data science, curation, and technical documentation; so that new analysts, academics and innovators can arrive to find platforms with well curated data and accessible technical documentation.

### NHS data analysts

16. Create an NHS Analyst Service modelled on the Government Economic Service and Statistical Service, with: a head of profession; clear job descriptions tied to technical skills; progression opportunities to become a senior analyst rather than a manager; and realistic salaries where expensive specific skills are needed.

17. Embrace modern, open working methods for NHS data analysis by committing to Reproducible Analytical Pipelines (RAP) as the core working practice that must be supported by all platforms and teams; make this a core focus of NHS analyst training.

18. Create an Open College for NHS Analysts: this should devise (and coordinate delivery of) a curriculum for initial training and ‘continuing professional development’, tied to job descriptions; all training content should be shared openly online to all; and cover a range of skills and roles from deep data science to data communication.

19. Recognise the value of knowledge management: create and maintain a curated national open library of NHS analyst code and methods, with adequate technical documentation, for common and rare analytic tasks, to help spread knowledge and examples of best practice across the community; use this in training.

20. Seek expert help from academia and industry, but ensure all code and technical documentation is openly available to all, procuring newly created ‘intellectual property’ on a ‘buy out’ basis. Commission best practice guidance on outsourcing data analytics to cover: where external collaborations can be most helpful; the role of skilled analysts in guiding procurement; common red flags for delivery; and why RAP builds capacity, quality, and continuity of service.

21. Train senior non-analysts and leaders in how to be good customers of data teams.

### Governance

22. Rationalise approvals: create one map of all approval processes; require all relevant organisations to amend it until all agree it is accurate; de-duplicate work by creating a single common application form (or standard components) for all ethics, information governance, and other access permissions; coordinate shared meetings when approval requires multiple organisations; have researchers available to address misunderstandings of their project; build institutions to help users who are blocked; recognise and address the risk of data controllers asserting access monopolies to obstruct competitors; publish data on delays annually; ensure high quality patient and public involvement and engagement (PPIE) is done.

23. Have a frank public conversation about commercial use of NHS data for innovation, but only after privacy issues have been addressed through adoption of TREs; ensure the NHS gets appropriate financial return where marketable innovations are driven by NHS data, which has been collected at great cost over many decades; avoid exclusive commercial arrangements.

24. Develop clear rules around the use of NHS patient records in performance management of NHS organisations, aiming to: ensure reasonable use in improving services; avoid distracting NHS organisations with unhelpful performance measures.

25. Address the problem of 160 trusts and 6,500 GPs all acting as separate data controllers. Do this either through one national organisation acting as Data Controller for a copy of all NHS patients’ records in a TRE, or an ‘approvals pool’ where trusts and GPs can nominate a single entity to review and approve requests on their behalf.

### Approaches and strategy

26. Use people with technical skills to manage complex technical problems – create very senior strategic leadership roles for developers, data architects and data scientists; offer leadership training to those in existing technical roles. (Also train senior leaders in the basics of data analysis, software development, and clinical informatics; but recognise the limitations of that approach).

27. Build impatiently, but incrementally, accepting that new ways of working are overdue, but cannot replace old methods overnight. We must build skills, and prove the value of modern approaches to data in parallel to maintaining old services and teams.

28. Identify a range of ‘data pioneer’ groups from each key sector: 3 ICS analyst teams; 3 national quality improvement registry or audit teams; 3 academic birth cohort or electronic health record analysis teams; and 1 to 3 national NHS analytic teams.

29. Build TRE capacity by taking a hands-on approach to the components of work common to all TREs. Avoid commissioning multiple closed, black box data projects from which little can be learned, or framing these as ‘experiments’. Experimentation is only powerful where it delivers openly shared working methods, code, outputs and technical documentation from which all can learn.

30. Focus on platforms by resourcing teams, services and institutions who are focused solely on facilitating great analytic work by other people, working closely with users. Data curation, secure analytics, TREs, libraries, RAP training, and platforms are the key missing link: they will only be delivered if they become high status, independent activities.

