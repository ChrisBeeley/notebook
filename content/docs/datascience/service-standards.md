---
title: "Service Standards"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Data science and the service standards

Although all of these standards are relevant to data science teams I will now outline those that are most relevant within data science and briefly talk about their importance

## Make the service simple to use

// TODO

## Team with multidisciplinary skills and perspectives

[The digital, data, and technology](https://www.gov.uk/government/collections/digital-data-and-technology-profession-capability-framework) provides an outline of the types of roles present within an effective digital/ data/ technology team, which comprise:

  * Data job family
  * IT operations job family
  * Product and delivery job family
  * Quality assurance testing (QAT) job family
  * Technical job family
  * User-centred design job family

All of these roles are relevant to an effective data science offering in the NHS, although depending on the size of the team and the project it may be that they interact with other teams to access some of these skills (for example, in the technical job family, which includes DevOps, or in the IT job family, which includes service desk operatives).

Following is an outline of the types of skills one would expect to find within a data science team. From the data job family data engineer and data scientist are the key roles. An effective data science team would ordinarily be expected to include individuals with skills in these areas. The other skillsets in this family are data analyst and performance analyst.

Data analysts and analysts are an important adjunct to an effective data science team but will not necessarily be part of the team itself.

Data analysts:

  * "apply tools and techniques for data analysis and data visualisation (including the use of business information tools)
  * identify, collect and migrate data to and from a range of systems
  * manage, clean, abstract and aggregate data alongside a range of analytical studies on that data
  * manipulate and link different data sets
  * summarise and present data and conclusions in the most appropriate format for users"

Performance analysts:
>...develop performance measurement frameworks - key performance indicators (KPIs), goals, user needs and benefits - and analyse the performance of a service or product against these, adapting your approach and framework appropriately and in line with any changes

The synergy with these roles and those of an effective data science team should be clear. Data and performance analysts take metrics and methodologies that have been developed and productionised by the data science team (as well as preexisting data reports) and deliver them across the organisation

They make use of dashboards, regular and ad hoc reports and ensure that these measures are used and understood throughout the organisation. For the purposes of this discussion it is enough to say that the difference between the two roles is one of emphasis- with data analysts focused on bringing stakeholders new information and insight from across the organisation and performance analysts on ensuring that performance targets are met and liaising with teams and senior managers when they find that performance is not being met in a particular area. For a fuller discussion of these roles see [this discussion of the data job family](https://www.gov.uk/government/collections/digital-data-and-technology-profession-capability-framework#data-job-family).

It should be clear, therefore, that the work of data scientists can only be brought effectively to bear on an organisation when used in conjunction with data and performance analyst skills. Effective data science teams which do not include these skills, therefore, (which some will), should have a close and mutually supportive relationship with a team which does.

It is worth noting that all of these skills do not have to be within one individual in the data science team, and nor does each skill have to be found in only one member of the team. Effective teams can have individuals who have a broad skillset fulfilling several of these roles and/ or "specialists" who are highly experienced within a narrow domain and fulfil this role only in the team.

## Agile

Agile methods are widely used in data science and they are extremely helpful in making sure that the analyses and data products that are used meet user specifications as well as ensure that they are thoroughly tested in a live context before deployment. The key message from agile methods is that:

>iterative, user-centred ways of working will help you get your service in front of real users as soon as possible. Then observing and analysing data on how they use it, and iterating the service based on what you've learned. Because you're not specifying everything up front before you've developed an understanding of what users need, you will reduce the risk of delivering the wrong thing

Following on from the points made previously about multidisciplinary working it is worth noting that [Agile Data Science](https://www.oreilly.com/library/view/agile-data-science/9781491960103/ch01.html) states that agile data science teams favour:

  * Choosing generalists over specialists
  * Preferring small teams over large teams

There are eleven different job roles listed within Agile Data Science, and the author argues that having these roles fulfilled by individuals whose skill spans two or three of these roles can contribute to the agility of a team and reduce the overheads that large, specialised teams can suffer from, such as the need for each role to effectively communicate with other similar roles (e.g experience designer, interaction designer, and web developer).

NHS service standard number 6 (multidisciplinary teams) explicitly states that teams must "includes people with expertise in how services are delivered across all the relevant channels, and the back end systems the service will need to integrate with". To make such a team small and agile, it is often preferable for individuals to span several roles, some spanning front end activities (data scientists with experience in UX and web design) and some back end activities (data scientists who can do some or all of their own data engineering).

Agile methods are covered in more detail in /TODO.

## Respect and protect users’ confidentiality and privacy

This point is clearly highly germane in healthcare, and it's worth noting that the rapid prototyping and lack of career specialisation inherent in much of data science do increase the risks that mistakes will be made with user data. This part of the service standard lists many obligations, including:

  * actively identify security and privacy threats to the service and have a robust, proportionate approach to securing information and managing fraud risks
  * have a plan and budget that lets you manage security during the life of the service (for example, by responding to new threats, putting controls in place and applying security patches to software)
  * work with business and information risk teams (for example, senior information risk owners and information asset owners) to make sure the service meets security requirements and regulations without putting delivery at risk
  * carry out appropriate vulnerability and penetration testing

Early data science work (for example dashboards which do not contain identifiable data, delivered within an organisation's firewall) may not require strict adherence to these guidelines, but the danger is that as the scope of a programme of work widens these issues become relevant and the data science team do not take the appropriate steps to ensure that they bring on board security and governance specialists who can ensure that data is processed and delivered to endusers securely.

## Make new source code open

Although the advantages of using open source technologies and of open sourcing new technologies have been known for decades (see, e.g. [The Cathedral and the Bazaar](https://en.wikipedia.org/wiki/The_Cathedral_and_the_Bazaar)), and government policy has encouraged the production and use of open source within the public sector for ten years or more there has been surprisingly little progress in this area. The NHS is still overwhelmingly dependent on expensive, proprietary software, giving rise to vendor lock in as well as wasting public money. Anecdotal reports suggest even that many IT departments are reluctant to install the statistical programming language [R](https://cran.r-project.org/), an absurd situation given its widespread adoption and use across industry and academia.

At the same time, NHS organisations are still very reluctant to open source any code produced by their staff or by agencies subcontracted by NHS organisations. Open sourcing new code is important enough to warrant its own chapter (see [open source]({{< ref "open-source.md" >}}), for the present time it will suffice to quote from the NHS service standard:

>"Public services are built with public money. So unless there's a good reason not to, the code they're based should be made available for other people to reuse and build on.
Open source code can save teams duplicating effort and help them build better services faster. And publishing source code under an open licence means that you're less likely to get locked in to working with a single supplier"
