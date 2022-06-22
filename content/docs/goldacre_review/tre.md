---
title: "Trusted Research Environments"
weight: 4
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

## What is a "Trusted Research Environment"?

> In outline, a Trusted Research Environment (TRE) is a secure environment that researchers enter in order to work on the data remotely, rather than downloading it onto their own local machine. Users can extract and download the answers from their analyses – such as results tables, or graphs – but individual patients’ data always stays within the secure environment

"good TREs can also provide a more efficient and collaborative computational environment for all data users, and an opportunity to make modern open working methods the simple default. Once again: it has been estimated that 80% of the work for data science with NHS records is spent on data preparation; this is currently delivered in a diverse, duplicative and ad hoc fashion, falling short of minimal RAP guidance, with different teams and individuals all using different methods and tools for even basic data management work, in different ways, in different organisations and settings, to do the same or very similar tasks, often on the same national NHS datasets such as GP data or HES/SUS"

"In short, TREs represent an unprecedented opportunity to modernise the data management and analysis work done across the system, allowing us to achieve the following benefits:

* replace hundreds of dispersed analytic siloes, data centres and working practices with a small number of broadly standardised environments that facilitate the use of modern, efficient approaches to data science
* reduce the number of data centres, and thereby also reduce the number of cost centres.
* reduce the number of attack surfaces for cybersecurity risk
* overcome local IT constraints that prevent analysts installing specific types of contemporary data science software by enabling analysts to conduct their analyses at a central online location rather than on multiple local bespoke machines
* create technical working environments where a smaller number of expert software developers can assist all colleagues nationally, using modern industry standard data science tools, packaging up the code for recurring tasks into adequately documented “functions” and “libraries” for easy re-use
* facilitate the collaborative development of highly effective interactive data tools for less skilled users with Graphic User Interfaces for safe and effective use of Point and Click tools (rather than these being an inappropriate default), using commercial and open data visualisation tools as appropriate
* allow (and indeed require) all data curation code to be shared with all subsequent users for review, validation, re-use, and iterative modification
* make modern, open, collaborative, computational approaches to data analysis the norm, facilitating Reproducible Analytic Pathways rather than duplicative, diverse and inefficient approaches to data management"

## What should TREs achieve?

* Preserve patients’ privacy
* Support RAP and modern, efficient, high quality, reproducible data analysis
* Provide a secure computing environment
* Provide a performant computing environment
* Earn patient trust
* Be surrounded by good governance, and support this with relevant technical features

## "Five safes" principles

* Safe projects: is this use of the data appropriate?
* Safe people: can the users be trusted to use the data in an appropriate manner?
* Safe settings: does the access facility limit unauthorised use?
* Safe data: is there a disclosure risk in the data itself?
* Safe outputs: are the statistical results non-disclosive?

## Meeting needs for expert and non-expert users

There are two broad types of users of TREs- "expert" and "non-expert" users. The methods they use to interact with TREs are quite different.

### Non experts

Non expert users will tend to use remote desktops. This is the most common method at the moment, and it is an important option because it allows analysts to use familiar tools such as Stata and Excel. Remote desktops pose some challenges for privacy and governance since

* Activity logs are difficult to parse- only keypresses, mouse movements, and videos of the screen can be stored, and these require lengthy manual review
* The data that is shared is inherently more disclosive because it is readable by standard analytical packages

> Remote desktop TREs also do not lend themselves to open working, or a network of users collaborating through shared modules of code: users are often not working in ways that meet RAP standards; and exporting code at all can be challenging, since that code has been written interactively while viewing the real data, and is therefore has a higher risk of accidentally containing some disclosive information

Expert users will benefit from a very different system, that runs in a largely script based fashion. There are skills necessary in order to be able to work in this fashion (see the chapter on [open working]({{<ref "open-working.md">}})) but they bring substantial benefits:

* RAP working with shared code is actively facilitated, and indeed is the natural way to work
* It is possible to keep informative logs of all activity, and automate a range of efficient working practices around re-used code for core common activities of data curation and analysis
* It is also much more straightforward to keep informative logs, share activity logs, and implement a range of security provisions that protect patient privacy by preventing or detecting misuse

Where there are additional privacy provisions, a full TRE can justify deeper access to more detailed and complete data while still maintaining the trust of professionals, the public, and patients

> Giving users who wish to work in this kind of environment a remote desktop would not be “easier”: in fact it would substantially obstruct their work

## The practical components of a TRE

### The service wrapper

"This is the set of rules, regulations, governance and customer service that surrounds a TRE. There will be a range of rules around who can access the data, the skills or certificates they may need; there will be a similar range of rules around permissioning for projects; there will be processes to evaluate compliance with these rules; there will be forms to collect the data, and administrative processes to manage them; and so on. There will be governance for the TRE as a project in itself, and a range of permissions, contracts, relationships and governance arrangements around the patient data that is being ingested. There will be public-facing material to be managed, describing activity in the TRE to a greater or lesser extent. There will also usually be an “output checking service”: when an analysis is complete, and the analysts are ready to release their tables and graphs from the secure environment, this is a final manual check to ensure that no disclosive information is being accidentally sent out. This output checking work is done by staff with skills in data management and analysis: it is a rapidly growing field of work that is long overdue for methodological innovation embodied in re-usable code"

### Generic compute and database

"A TRE is a truly multidisciplinary project: it requires strong knowledge of governance, but also deep knowledge of technical infrastructure. However, much of this technical work presents broadly similar requirements to that in other non-health sectors around tasks such as provisioning large databases, ensuring that they are secure, ensuring they are performant, managing access permissions, and providing a computational environment where users through some sensible means can call up processor power, memory and disk storage to execute their code.

There is some overlap, inevitably, with domain knowledge: the team ingesting and transforming the data will need some knowledge of the specific qualities of the data they are working with, and the end-users’ needs; the implementation of processes around users will entail some knowledge of the service wrapper processes. But overall, the key practical issue is as follows: the compute, database, and service design aspects of a TRE are largely generic tasks that can be largely delivered by staff who have strong generalist software and data science skills, and who are easily recruited from other sectors."

### Subject-specific code

"This is best understood by analogy with other fields. The data science team at the music-streaming service Spotify do innovative work with data that helps drive the usability and popularity of their subscription service. For example, they extract patterns in the listening behaviour across all their users, and then use this to provide individual users with tailored recommendations for other music they might enjoy. The Spotify data science team couldn’t buy, off the shelf, a data science environment specifically built to service the needs of “a global music streaming service”. They implemented standard off-the-shelf tools for a general purpose data science environment. Then, within that raw environment, they needed to build their own tools, analytic approaches, workflows, data preparation work, and so on. A new arrival in the Spotify data science team today will find modules of code, libraries and packages – some even with nice interactive interfaces – to help them find interesting new patterns in Spotify user data. Many of these tools will feel like part of the furniture, but they were all built by their predecessors in the Spotify data science environment. Furthermore, many of these tools will not have been built to a pre-determined specification, by software developers hired to do that work to order; rather, they will emerge from a team. A single analyst might painstakingly implement a one-off analysis; if it looks like the approach will have broader use, then a more experienced developer might offer to help package it up into a function or library, with good documentation; if it becomes a commonly used approach, they might work with other analysts to create an interactive tool."

## Recommendations

TREs are not really a focus for me, so this will be a very brief summary, but there are some interesting points here:

* TRE 10. All TREs must support code sharing and RAP 
* TRE 14. Establish a standard scheme to accredit NHS TRE users
* TRE 18. Switch off data disseminations, without undue panic
* TRE 21. The National TRE should be open to all legitimate users
* TRE 24. Create a local NHS TRE programme
* TRE 25. Work to rapidly standardise local TRE and DAE provision, starting with ICSs:
    * Create a standard service wrapper model for local NHS TREs.
    * Ensure all ICSs use a standard TRE approach.
    * Encourage other local NHS data centres to use the same standard TRE.
    * Manage diverse local datasets by creating and sharing standard data curation tools and methods.
    * Ensure all local implementations of national or commonly used datasets such as SUS/HES conform to a single standard.
    * Ensure all datasets extracted from national datasets in NHS Digital are requested using standard data management code.
    * Ensure local analysts use a national TRE wherever possible.
    * Work towards federated analytics with standard local TREs.
    * Listen carefully to local NHS analysts and TRE managers who describe shortcomings in standard approaches; and address these wherever possible
* TRE 26. Create a single service wrapper model for local NHS TREs 
* TRE 29. Manage diverse local datasets by creating and sharing standard data curation tools and methods
* TRE 33. Ensure local analysts use a national TRE wherever possible
* TRE 34. NHS Trusts and Data Access Environments
    * "Many NHS trusts have arrangements for academic and service analysts to use their internal data for a range of projects involving research and service improvement. These projects should be encouraged to adopt the standard NHS TRE service wrapper, and standard NHS TRE technical approaches"
* TRE 40. Academics should use NHS data infrastructure to access NHS patient records
* TRE 44. All academic TREs must support, and should require, RAP and open working
* TRE 57. Address TREs for Artificial Intelligence, but as a separate workstream, funded by existing AI resource
    * "challenges primarily relate to compute power; the use of specific tools such as GPUs; and export controls, because exported random forest models can ( in ways that are hard to detect) sometimes contain disclosive patient data"