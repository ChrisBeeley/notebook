---
title: "Open Working"
weight: 2
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Open working

For more information about [open source]({{< ref "docs/datascience/open-source.md" >}}) and [software licensing]({{< ref "docs/opensource/_index.md" >}}) in the NHS see elsewhere in this notebook.

## Myths about open working

This section starts with mythbusting, which is very welcome because there is a lot of rubbish spoken about open code in the NHS. To summarise:

> Adopting open working practices does not mean other countries or industry can exploit intellectual property created with state funds: there should be a robust and thoughtful exceptions framework to impose commercial licenses or restrictions on review and (separately) re-use of publicly funded code, where this is actively helpful; but this closed approach should be used in a planned and deliberate fashion, where it meets national strategic objectives, not as the unplanned default approach

* I'm not 100% clear on what is intended by this- but if it was I imagine (dual licensing) [I'm not sure about the practicalities of this one]({{< ref "further-work.md#software-licensing" >}})

> open working is fully compatible with use of commercial products: it requires only that new code and methods created for and funded by the state should be shared as default, for interoperability, quality, and efficiency. Similarly, open working does not mean that nobody is paid: simply that new code and methods are contracted from the outset as a buy-out

* An important point. I've often been told verbally that the code and working out of a contractor will be shared with me- however this rarely happens in practice. This isn't nice to have, it's essential, and a proper [open source licence](https://opensource.org/licenses) should be specified in the contract. NHS-R only funds open source work, and the licence is named on the application for funding

> open working does not mean that the results of every analysis must be shared openly, or in real time. The results of an analysis are separate to the code and methods used to create them. It may often be reasonable for NHS analysts to run data analyses to monitor and optimise the delivery of care, for example, without disclosing the results of all such analyses publicly in real time

* This red herring is trotted out at every opportunity. I only ever want the code, and never the data, but "IG" is used as an excuse to keep everything hidden

> Lastly, open sharing for code is not a philosophical, political, or ideological stance, but rather a practical one. Data curation and analysis is complex technical work across multiple teams, and it can only be done well where technical material (such as code, methods and documentation) is shared between those teams... the people working on NHS data stretch across hundreds of diverse public and private sector organisations. Creating a closed permissions-based system to carefully police limited sharing among a huge array of individuals across all these organisations would be a vast technical and bureaucratic project, of inconceivable complexity and expense. Most importantly, this expensive approach to balancing closed working and accessibility of information would bring no clear benefit, as there is no clearly articulated need for code and methods to be withheld from wider access

* Personally, I think code sharing is both philosophical/ political and practical, but the point is well taken

## Reproducible analytical pipelines (RAP)

> data scientists or analysts who had approached health data from other sectors... They repeatedly expressed how surprised they were to find that approaches regarded as standard in other parts of industry or academia – such as sharing code, or the everyday working practices of collaborative software development – were not yet the norm in teams working with health data

Reproducible analytical pipelines:

* minimise manual steps, for example copy-paste, point-click or drag-drop operations. Where it is absolutely necessary to include a manual step in the process this must be documented
* be built using open source software for data management, analysis and visualisation which is available to anyone, preferably R or python
* be open to anyone for review and re-use, with all code shared openly through open standard file and code sharing platforms such as GitHub (sharing data itself is a separate issue from sharing code, as discussed below, and should be handled very differently)
* guarantee an audit trail using version control software (such as Git, or in services such as GitHub) which systematically track exactly who has made which changes or contributions to the code, which characters and lines were modified, when, and – as appropriate – why
* follow existing good practice for quality assurance
* deepen technical and quality assurance processes with code review by peers
* contain well-commented code and have documentation embedded and version controlled within the work, rather than saved elsewhere

The key change to RAP: 

> a recognition of the need for those working with data to embrace the many norms and behaviours of the software development community when writing code

"There is undoubtedly a place for traditional and less technical approaches to collaboration and information management such as emails, meetings, phone calls, or written manuals. But these are ill-suited to managing long complex interdependent technical work with code and data"

These practices include (see the report for a description of them):

* Version control and GitHub
* Code review
* Functions
* Unit tests
* Libraries
* Documentation
* Managing the environment

### Who needs these skills

Not everyone needs these skills, there are important other roles...

"individuals with good skills around interpreting data, and communicating it effectively to clinicians or managers in the NHS in order to help them effect change. There is also an important role for individuals working as analysts, using more ‘point and click’ interactive tools developed for them by others who have deep skills in data management and analysis"

In respect of workforce:

> **It is, however, crucial** [emphasis added] that a large number of people have basic skills in this space, where they are developing and implementing analyses

In respect of culture and practice:

> **it is crucial that** [emphasis added] the core working practices, such as sharing code, are implemented as a norm throughout the system, because of the problems that closed working can create around quality, safety, usability, credibility, and review

### Point and click

> There is a legitimate and widespread ambition to have point and click tools for analytics in the NHS... However, it can only be realised by teams that understand the true underpinning reality of how patient data is generated, extracted, prepared and used across the system; who have RAP and computational skills; and who can work alongside people with clinical analytic needs to iteratively develop prototypes of interactive tools; and can then work with other tools to harden the most suitable of those prototypes into scalable interactive tools. Any solution that appears to not entail this kind of process, and workforce, is simply hiding the work, by commissioning it in less effective and closed means, or similar activity. By doing so, the system is prevented from learning about its own data, and developing the open commons of knowledge and workforce that drives high quality analytics and research in other settings and fields

### Build versus buy

> Overall, as discussed in the sections below, the best approach is: re-use existing commercial or open tools that already exist for large tasks (databases, etc) according to which is the best, with a preference for open to ensure access across hundreds of organisations in the NHS; procure open code from public and private vendors for new substantial tasks; build in-house and procure open code from public and private vendors for the vast ongoing workload of data management and analysis within those larger tools.

### Barriers to RAP

#### Skills

"there is an almost limitless array of self-directed online teaching through services such as Coursera, or some MOOCs (Massive Open Online Courses), but no clear signposting or curation of ‘journeys’ through these courses, or guidance on which to choose"

"For NHS service analysts... there is less access to formal training. The recent development of some online discussion forums aiming to drive further training was welcomed, but at present this does seem somewhat limited to links out to various YouTube videos on analysis in adjacent analytic fields, without clear curation of quality, appropriateness, priorities or journeys"

#### Recruitment

Recruitment and retention are very difficult in universities and NHS organisations because of the relatively low status and salary that these jobs have compared with equivalents in the private sector. 

"it is uncommon to find experienced software developers with industry standard skills who also have strong domain knowledge across topics such as: the nature of NHS data; how research is done with electronic health records or related research data; the clinical context for such work; the operational context of the NHS; how data is collected, manipulated, and extracted from clinical systems; and so on. This is particularly concerning given that senior individuals in the NHS and academia repeatedly expressed frustration that they wanted to recruit these staff, but that this is 'like hunting unicorns'"

"while some developers will accept a lower salary for public service, many equate this ‘public good’ with contributing to open source sharing of code, whereas in academia and the NHS code is often closed. Related to this, developers typically use evidence of prior work to get each new job, and often use their GitHub activity to help future employers see their productivity, and quality; this is not possible when code is withheld from open view; when projects are slow to deliver; or where the software contributions are low status or hidden"

#### Platforms

"those with skills in open approaches to computational data science... were actively blocked by the platforms and tools available to them in both the NHS and academia. On a small scale, at the level of individual laptops, they were often concerned to find that local IT policies actively prohibited the installation of tools – such as R, Git, Python or Docker – which they viewed as being a basic minimum necessity for the delivery of their work. Where it was possible to push through these obstructions, it took very substantial effort on the part of individuals, often requiring substantial local organisational and administrative support from senior leaders, over a very long period of time"

"these problems also seem to be prevalent in many of the large and small platforms that have been created for secure analysis of data. For example, numerous analysts expressed concern and surprise that they weren’t able to use GitHub inside Trusted Research Environments, or Data Access Environments, because communication with outside resources such as these were locked down for security reasons; and furthermore, that they were not even able to access more closed tools for code management such as GitLab, as they were either unavailable or implemented so poorly as to obstruct their normal use"

"in a technical environment where all the tooling, working practices and assumptions are built on a model substantially less evolved than RAP, procurement and implementation decisions are built around an assumption of people using point-and-click and copy-and-paste methods, rather than scripts, meaning that individuals with computational skills simply cannot use them"

#### Funding

"Numerous individuals complained that they were able to find no open competitive or conventional sources of funding to support them as individuals, or as a team, to focus on the software and related methodological aspects of delivering high quality outputs from NHS data, and that their salaries were therefore only covered as a component part of a grant focused on delivering a specific research paper output, adding to their sense of lower status, and obstructions in both their career and their ability to innovate, as they were only employed, conceived of, tasked, and supervised as ‘support staff’ for traditional academic epidemiology research skills. In desk research it proved extremely difficult to find open competitive sources of funding for this kind of work from any national funders, whether project-based or person-based.

More concerningly, a number of individuals described in detail situations where a substantial public investment had been made to deliver work closer to research data infrastructure, code, and methods, but that this resource had been – in their view – diverted onto delivery of traditional research outputs, and staff with only skills to deliver those outputs, either because the specific piece of funding had been administered and awarded from funders to individuals with traditional research paper skills, rather than those with computational skills, or because those in senior leadership and strategic roles in their organisations tended to be those with a traditional focus on single research paper outputs rather than code."

#### Recognition

"Researchers and analysts with strong skills in RAP and computational approaches to data science expressed a range of frustrations that clearly reflect fixable structural challenges. At an individual and organisational level, there was an impression that these skills are under-valued, or that they were viewed as ‘just programmers’. In academia examples were shared of developers and data scientists not being named as authors on publications, or grants, despite having contributed – in their view – a very substantial amount of the work, including creative and innovative methodological work to deliver the outputs. Examples were also shared of situations where individuals had left the field and moved into other industries where they could get both higher salaries and better recognition for their skills."

## Recommendations

[mostly verbatim, edits for length]

Open 1. Create a RAP and Open Code Oversight Group

Open 2. Create a public policy setting out expectations on open code

Open 3. Make open code a boilerplate feature of all public contracts

**Open code sharing should be a required feature of all standard contracts between the NHS and any external provider of code for health data management and analysis** [emphasis added]

Open 4. Create an ‘exceptions framework’ whereby publicly funded code can be closed by prior arrangement if this meets NHS and UKplc strategic objectives

Individual researchers, organisations or funders should be able to actively apply for a single project to be closed, under a carefully designed ‘exceptions’ framework, where each exceptional request is evaluated to determine whether this exception meets reasonable national, individual or organisational interests around commercialisation and collaboration, and whether the network damage inflicted by a closed license is justified by another greater public benefit. This expert group should include intellectual property specialists, software developers, researchers, key stakeholders with expertise (such as the Open Data Institute), policy experts and funders.

Open 5. Create an Open Code Ombudsman and Assistance Unit

It is possible, particularly whilst the NHS analytics workforce is in a transition period, that there will be occasions when an analyst or team of analysts in one NHS organisation needs access to code that has not yet been made open by a different NHS organisation – potentially including central government organisations. There is a need for an independent body that is tasked with dealing with these, and other, disputes. This unit should listen to complaints, and feedback common themes to the relevant policy, funding and commissioning teams so that appropriate guidance can be developed. To make this practical, the unit must have appropriate status and power over even the largest NHS organisations.

Open 6. Assert that publicly funded code is publicly owned: cautiously consider ‘Crown Copyright for code’

At present decisions about sharing and licensing code are made, at small scale, in huge numbers, across the health and research landscape, often by people who do not understand the impact and implications of these choices for themselves and/or the wider community of data users. This has very substantially blocked code sharing, which should be the norm, and is the norm in many adjacent research specialities. An expert group should be convened to formally consider a new national standard: that public funded code is publicly owned, under a formal license that covers all code produced on public funds; with an expectation that all publicly funded code should be shared under the MIT open license; and exceptions to be decided by prior arrangement with a prespecified ruleset.

Open 7. Data Controllers should require RAP and open code sharing from data users

Data controllers and especially the NHS should require all those accessing patients’ data to share all analysis code, or openly argue for exceptions in single cases. Where the system is in a period of transition, this should be strongly considered in all data access requests, and where there is no plan to share code immediately there should be a credible plan to ensure that this is done later. As with other mandates around open code this should have a clear pre-specified exceptions framework.

Open 8. Amend the Code of Practice for the Research Powers of the Digital Economy Act

The Department of Health and Social Care and the UK Health Security Agency should work with the Department of Digital, Culture, Media and Sport to make a minor amendment to the Code of Practice for the Research Powers of the Digital Economy Act (the primary legal gateway for accessing non-health data) requiring data analysts to make their code available, with a robust exceptions framework as discussed elsewhere.

Open 9. Make it ‘okay to ask’ about access to publicly funded code

The team heard from several interviewees that at present it is commonly regarded as provocative to ask for access to the code used to implement an analysis, especially in some parts of the academic community, despite general positive statements on open working. Culture change will only be possible if it is deemed socially acceptable to question when deviations from the ‘new norm’ of open working are identified. This should be made clear in all relevant policies, and codes of conduct, across academic and NHS organisations.

Open 10. Health and Care Information Governance Panel guidance should facilitate open code

It is important that all NHS organisations are given clear direction that code sharing is not the same as data sharing and that it is entirely possible to share code routinely and safely without the organisation incurring significant costs or reputation risks. To make this clear, the Health and Care Information Governance Panel should create guidance on the importance (and permissibility) of code sharing, to go on the Information Governance Portal, emphasising that transparency is a crucial means to build public trust and clinical safety.

Open 11. The Information Commissioner’s Office should produce guidance to facilitate code sharing

The Information Commissioner’s Office (ICO) is currently working to produce new and updated guidance on anonymisation. Alongside this, the ICO should also produce guidance regarding code sharing. This should make clear that sharing code is not a disclosure risk, and that those writing code have a clear responsibility to ensure that their analytic code is not disclosive of any personal information. Ideally this guidance should also make clear that code sharing and the practices associated with Reproducible Analytical Pipelines are an important aspect of good citizenship around data usage. There is also a need for better guidance and training on ensuring that analytic code is not disclosive of any personal information.

Open 12. The Medicines and Healthcare products Regulatory Agency should address code sharing and device regulation

Open 13. Negotiate co-ownership of claimed commercial innovations from NHS data

Open 14. Write an ‘open analytics policy for the NHS’

Bring together DHSC and the NHS Transformation Directorate to write a policy that makes it clear to all analyst teams across the NHS, and all general managers, that sharing code is not the same as sharing data and that open is the preferred and default method for all analysis conducted using public data and public funding

This policy should set out best practice for using open working methods, for openly sharing code and for writing documentation. It should also cover more complex areas such as licensing and the protection of IP where applicable. It should be kept under regular review to ensure it remains up-to-date and should signpost to further sources of help and advice where necessary. All external procurement of data science services, whether data management or analysis, should require that all code and codelists produced to deliver the work are shared openly by default. Exceptions to this should be rare and explicitly pre-arranged, with clear justification under pre-specified criteria set by the NHS Transformation Directorate and DHSC

Open 15. Make open a standard contractual requirement

Government departments should require all those conducting data analysis on their behalf, in-house and as contractors, to share all code, consistent with RAP and the computational methods above, with adequate technical documentation as per RAP criteria. To aid with this Intellectual Property assignment and publication requirements should be laid out in template and framework contracts so that all organisations commissioning or contributing analysis and code to the public sector are held to the same standards. These contractual requirements should be developed in collaboration with members of the research software engineering community to ensure that they are fit for purpose. It should also be borne in mind that all such requirements, policies, and guidance documents are likely to be ‘living’ and regularly iterated best on the evolving nature of best practice in this field

Open 16. Commission intermittent open code audits to drive improvement

In collaboration with academics and key organisations such as AphA and the NHS-R community, the NHS Transformation Directorate should commission regular code audits of all organisations that have received public funding for health data research or analysis, including funding for the development of intermediate knowledge objects (for example, datasets, or TREs). These audits should evaluate adherence to RAP and open computational methods; follow a set methodology; be published openly; and be used for the explicit purpose of improving performance on code sharing, rather than penalising poor performance. 

Specific criteria should be developed in collaboration with the community but include: all code shared on GitHub or similar; adequate technical documentation embedded within code as per RAP criteria; use of version control and appropriate methods; sharing of non-disclosive open data where possible; support for continuing professional development in work time; whether staff meet job descriptons with training, continuing professional development, or other proof. 

Open 17. Establish a technical writing and documentation team for the NHS

Open 18. Create a ‘Code For Health’ training programme for NHS service analysts and academic researchers

This should include advanced computational data science covering RAP, software carpentry, version control, functions, code documentation, and similar. This should be at a range of levels including MOOCs, short courses, and long courses, with strong practical elements. The principles and working practices set out in the box below are strongly recommended.

* Combine NHS and academia
  * Although historically NHS service analysts and academic analysts are considered separately, this is a strong strategic opportunity to begin building robust technical bridges between the two: both work on similar data, often with similar methods or tools; and both should ideally work in similar data analysis environments, as discussed in the Trusted and Shared Research Environments chapter.

* MOOCs and practical work
    * Traditional teaching and training has a role. However, for scope and access, a priority should be placed on delivering training as a combination of Massive Open Online Courses (MOOCs) and in-person teaching, both developed specifically for this purpose. MOOCs can cover factual content, and with practical code development exercises can be procured outright: they should be made openly available to all. In-person supervision is necessary for a subset of attenders, especially those seeking certification, to supervise practical work, and for marking work to evaluate competences. This will necessitate a per-person fee, which will create a revenue stream for providers, but necessitate a system for unit payment from the NHS which may obstruct NHS analyst attenders given current lower status of this group in some organisations (see NHS Analysts chapter): thought should be given to block purchase or training budgets as seen in other parts of the NHS.

* Build on prior work but maintain focus on RAP
    * This training should build appropriately on various existing resources and expertise including: the work by existing RAP teams; the work by the NHS-R Community; and other work specifically on RAP and computational methods. It should focus specifically on RAP and computational data science techniques as directly applied to working with NHS data. Caution should be taken that resource is not diverted into training on other issues such as general research methods, specific statistical methods (except as specifically embodied of RAP training), or newer methods such as Machine Learning which are useful but different subjects. Similarly this training cannot be delivered by universities rebadging existing training on other topics such as bioinformatics; or by simply linking out to generic data science training resources from other suppliers; albeit that these may be fertile starting points for modification into bespoke training on RAP and computational methods in NHS data.

* Open competitive procurement
    * Training should be procured by an open competitive process, amenable to the best of either public or private providers. All training can be commissioned by either UKRI, the NHS, or both. A rapid technical review should be conducted of recent very welcome UKRI investment in this space to evaluate whether it addresses RAP and computational methods as above, and whether outputs are open. There is currently a rich diverse ecosystem of training in many other aspects of analytics, with no concern about overlap between offers, and similarly a diverse range of providers with different focuses should be acceptable here. An emphasis should be placed on finding providers with strong previous track record of using RAP or open computational methods.

Open 19. Create a ‘Data for NHS leaders’ training programme

For senior leaders and those in adjacent skill groups training should be accessible on the basics of data analysis, RAP and computational methods so that this group can understand the principles and purpose of the work done by those in their team. This should be MOOCs and short courses. Some of the excellent recent work at the Number 10 Data Science Unit (10ds) ‘data for leaders’ programme may be adaptable.

Open 20. Create an ‘NHS data for developers and data scientists’ training programme

Very senior leaders in the system repeatedly expressed to us the view that individuals with deep developer skills and NHS domain knowledge are extremely hard to recruit, if not impossible. Strong software development and data science skills are developed over many years and often require a specific disposition: it is not realistic to expect that current NHS analysts (with a deep but very different knowledge base) can be trained in such skills to the standard required by the NHS and wider community. New knowledge for generalist Software Developers and Data Scientists should be addressed with health data ‘Transfer Training’ so that individuals with strong technical skills can develop deep NHS domain knowledge. 

Open 21. Modify the Research Excellence Framework (REF) to reflect computational work

Open 23. Pay realistic salaries to software developers

Software developers are among the highest paid staff globally, but university pay scales typically do not recognise the skillsets required to be a research software engineer, and often attempt to hire engineers and developers on pay-grades similar to those of IT support staff. This makes it hard to recruit people with outstanding software skills and serves to further undermine the value of software development, data management, data curation, and code development. It is commonplace for universities to pay those with technical skills, such as clinicians or accountants, something closer to their realistic market salaries, Universities should develop pay scales for developers in the same way that they have done for clinical academics, recognising the specialist skills and outside options of those they are seeing to recruit.

Open 24. Create a working group to develop an attribution model for code and data

Open 25. Clarify the need for authorship for software developers and data scientists as equal core contributors

...Overall, having discussed this issue extensively, it is clear that there should be a presumption to include software developers and data scientists who have contributed to the delivery of [papers] in authorship, not least because this work commonly entails a wide range of creative input to deliver the work informed by deep technical knowledge of the analysis, but also in very many cases the clinical domain, and the statistical context, and similar issues. Where this is argued to conflict with other current documentation on principles such as guidance from the International Committee of Medical Journal Editors – which is itself commonly breached across a range of other topics – this should be robustly addressed and discussed...

Open 26. Proactively address sharing during the pandemic

Academic researchers have played an essential role in the response to the global COVID-19 pandemic. Yet, despite the global nature of the emergency, not all research, code, and other outputs have been made openly available for others to re-use or learn from. In some instances there may be good reasons for this, but in others it may simply be that the barriers to sharing have proved too high for some research groups – for example, paying for GitHub or for open-access publication. University administration teams and innovation offices should discuss with researchers providing research outputs on COVID-19 whether they can share code, methods, documentation, libraries, or more, for recent and future outputs.

Open 27. Academic journals should be encouraged to make code-sharing a requirement

Open 28. Embrace research software engineering with 3 data pioneer groups leading by example

Open 31. Provide guidance and training on RAP and code sharing

The training above covers broader issues around RAP and code sharing. Some researchers currently funded by for example NIHR and UKRI may be willing to share code but require bespoke training and support to do so. To help these individuals with this transition, funders should provide guidance and funding to attend training on ‘good enough’ code sharing, alongside guidance and examples of ‘perfect world’ code sharing. This should include supporting existing work, such as the Turing Way, RAP, and other similar projects.

Open 32. Fund a fellowship programme around Code for Health Data.

There is currently a need for more teams and individuals who combine skills in computational methods, alongside domain knowledge around epidemiology, NHS analytics, and EHR data. This can be addressed by applying the normal mechanisms for capacity building, especially fellowships which bring independent status within the university sector for individuals and a field; support career progression; and support individuals to make their own choices about where they can best contribute and innovate collaboratively alongside pure research colleagues, to get away from a paradigm of developers being seen as ‘instructed by’ researchers. 

Open 33. Open funding calls for projects and programmes around Code for Health Data.

Work related to technical infrastructure, data management, and TREs is not universally regarded as legitimate academic or methodological activity. There are multiple sources of funding for Individuals and teams to address specific single clinical research questions, but almost no open competitive funding for the development of code, infrastructure, or innovative methods in this space. It is crucial that great code and data infrastructure is developed in close collaboration with the delivery of strong single academic research paper outputs. However strong code is not produced when this aspect of the work is left to fend for itself as a junior party to single topic research projects, especially during a period of transition towards more computational approaches. UKRI and/or NIHR should launch an open funding call specifically for open code projects in health data science, and consult closely with the Wellcome Data for Science group on the best means to achieve this. 

Open 34. Treat ‘data Infrastructure’ as open code

Recent work from UKRI increasingly recognises that modern infrastructure is less about computers and buildings, and more about code and teams. It is crucial that data infrastructure is handled in this way, with delivery of open code at its core, accompanied by detailed technical documentation alongside it, consistent with RAP and the computational approaches outlined above. It is equally crucial to recognise that this approach can and should viewed as modular (with different re-usable elements for different tasks produced by different teams) and methodological (with approaches to specific data management, data analysis, and privacy preservation tasks developed iteratively through innovation and delivery). Most importantly, the system must steer carefully away from procuring infrastructure such as TREs as ‘black box services’ where only comms material and finished academic manuscripts can be seen from the outside; this is covered more in the chapter on Trusted Research Environments

Open 35. Use open competitive funding for code projects

It is vital to support an open collaborative ecosystem where those with the best ideas and delivery can compete to propose the best approaches to diverse challenges in data management, analysis, analytic platform components, and so on. An approach where one organisation, or a small number of organisations, is viewed as the sole supplier will not lead to excellence. Open competitive funding, where all can propose projects, is a key route to ensuring we identify and resource the best ideas and teams.

Open 36. Review prior delivery of open code by applicants

During a period of transition to new ways of working it is important that those leading by example are enabled to drive change; and prior delivery in this comparatively new space will likely be a strong predictor of future delivery. Particular caution should be used around teams with prior substantial resources for health data research projects that have not delivered, or cannot retrospectively showcase, a commensurate set of documented code.

Open 37. Ensure experts on code select and oversee code projects

Individuals with direct technical expertise in software projects, data infrastructure, RSE, RAP and related work should lead or very strongly guide all funding for projects in this space, just as conventional academics guide awards and oversight for projects delivering single academic paper outputs.

Open 38. Ensure the objectives and outputs of all investments are open

All funding for code projects, especially those around infrastructure, should be openly and publicly disclosed, with a brief description of the amount, the recipient, the expected work and timelines, and a link to the repositories where development and documentation is anticipated to reside.

Open 39. Ensure funding for code and platforms does not get diverted

When providing bespoke funding for developing open code and appropriate technical platforms it is necessary to ensure resource is not diverted to fund single research paper outputs for which there is extensive funding through other routes. This will require oversight at a number of different levels. When applications are being reviewed, funders should make sure that they have relevant technical experts on the panel reviewing the applications – for example, research software engineers and data scientists – evaluating proof of skills such as GitHub profiles and repositories in addition to CVs.

Open 40. Avoid ‘regressive funding models’ built around short-term bursts of funding

There is a concerning tendency for code projects to be resourced with short-term urgent bursts (for the avoidance of doubt, outside of COVID-19) with funding arrangements that require successful applicants in extremis to spend a large amount of money very suddenly, over less than a year, starting with only a few weeks’ notice. This strongly suggests a lack of strategic thinking in the organisations offering funding, and will tend to preferentially resource large incumbents who can rapidly absorb such costs, but who may not have the best prospects of delivering for the wider community. More specifically this last-minute funding strategy actively mitigates against new entrants to the market, field, and creative academic pool, while favouring incumbents; and disadvantages those in more junior roles, or without large existing teams, who may have the strongest ideas, newest skills, and best delivery prospects. The preferred funding approach should operate on 2 to 5 year cycles to build capacity and open delivery, with the conventional option of 6 months from award to commencement to facilitate inward recruitment of staff.

Open 41. Focus on sustainability for software projects: set aside a third of resource for this task

Funding should work hard to identify teams and projects with broad user bases and impact, then support them to continue their work with 2 to 5 year funding. This should not entail unrealistic proposals for commercialisation of data management and analysis code used solely for research and health data analytics unless there are clear grounds for a standalone commercial spinout; and it should not necessarily entail extensive commitments to specific new features simply to justify sustaining a project. Iterative improvement and sustained delivery are sufficient goals in themselves, build capacity in the system, and build a broader ecosystem of productive outputs. A third of any budget should be set aside for sustainability.

Open 42. All Trusted Research Environments for NHS data must facilitate and require code sharing

Open 43. TREs themselves should be built on principles of RAP and open code

Open 44. Produce clear guidance on disclosure risk and open code