---
title: "Privacy"
weight: 3
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# The challenge of privacy in health data

High quality analysis requires very detailed information about individuals, which means that a group of analysts have "access to every recorded detail, of every medical event, for almost every citizen, all the way back to birth" (I'm a little dubious of this claim myself. I'm not sure anyone could give you this even for the patients in my Trust, limiting themselves only to events within the Trust). 

> Managing this problem – widening access to records, while also preserving patients’ privacy – is the fundamental challenge for use of NHS data in service improvement, academic research, and the life sciences sector

* The NHS must maintain trust and active enthusiasm from patients and the public
* Researchers and analysts, conversely, are deeply frustrated by inaccessibility of data, and missed opportunities to improve patient care, when slow information governance processes obstruct data access

## Current practice

Privacy is currently maintained in two ways: pseudonymisation and trust in individuals and organisations. 

Pseudonymisation refers to removing individual identifiers such as DOB and postcode. In practice with a large dataset it is very vulnerable to the reidentification of individuals. 

> Knowing the approximate date range in which someone had a medical intervention, their approximate age, and their approximate location is often enough to re-identify someone in a pseudonymised dataset, and then – illegally – to see everything else in their record

Mothers are particularly vulnerable since their approximate age and when they gave birth can be inferred by many individuals known to them. The more individuals in the dataset, and the more detailed the dataset, the greater the risk of reidentification. 

Because pseudonymisation is imperfect in practice the system relies also on putting trust in a limited number of individuals and organisations. This creates a large bureaucratic overhead and will intrinsically not scale. 

It is worth noting finally that the current systems have failed in their attempt to reassure the public about the use of their data.

NHS data is not confined to the national datasets (e.g. at NHS Digital) that tend to be the focus of discussions. Because of a lack of clear guidance and secure analytics platforms, every GP practice and NHS Trust is an independent data controller. This leads to a large, confusing patchwork of data flows which are often not consistent even regionally, and certainly are ill defined at a national level. 

> National GP data flowing into a Trusted Research Environment (TRE- see below and the [section on TRE]({{<ref "tre.md">}})) is therefore an important privacy safeguard for patients, a substantial net improvement in protections for patients, and a reduction in burden around data flows for GPs

## The consequences of lack of trust in privacy

Because of a lack of trust in large data collection programmes such as [care.data](https://en.wikipedia.org/wiki/Care.data) and [GPDPR](https://digital.nhs.uk/data-and-information/data-collections-and-data-sets/data-collections/general-practice-data-for-planning-and-research) there are now many individuals opting out of the programme, "at a scale that will compromise the usefulness of the data"

## Trusted research environments

> ...there is a clear path forwards. In many other sectors – such as census work at ONS for 2 decades – data is not disseminated out to users. Instead the analysts go to the data, and work inside a secure platform called a Trusted Research Environment (TRE). This working style **must** [emphasis added] be adopted in the NHS

There should be no expansion of the use of pseudonymised data until TREs are in place- worth noting that the GPDPR dataset will only be available within a TRE.

## Other methods

"There are other forms of risk mitigation including: removal of ‘sensitive codes’ (which obstructs research on key areas of medicine); data minimisation (which has uses but is under-researched); sub-sampling (which has limits when aiming to detect subtle statistical signals); data perturbation (which has a role but requires a substantial research programme, and is complex to implement); and emergent methods such as ‘homomorphic encryption’ (which has seen no substantial working health implementation to date). Overall they show that this an important area of work which has been relatively neglected. Wider access to NHS patient records requires that the system as a whole takes the challenge of practical approaches to secure analytics, developing and evaluating robust methods for protecting patients privacy at scale. 

There is a clear role for UKRI/NIHR in providing open, competitive resource for applied methods research into privacy preservation, to earn public trust, in collaboration across the NHS, epidemiology and security engineering communities"

[note that there is a substantial amount of discussion in the paper about different privacy protecting methods as well as reidentification risks, these have been omitted in the interests of brevity, but if you're interested they are very much worth reading]

## Conflict between the views of the public and researchers

The reviewers heard from two groups:

* campaigners, patients, policymakers, and professionals about the need for patients’ privacy to be respected, about the need for medical records to be handled confidentially, and the substantial shortcomings in current ways of working with health data, such as disseminating detailed data out to multiple locations where subsequent activity is less clearly monitored
* researchers, funders, NHS analysts and senior leaders in the health service and government, [who said that] that the administrative, regulatory, practical and legal aspects of information governance (IG) are obstructive, duplicative, expensive, slow, inefficient, confusing, inconsistent and disproportionate to the risks presented by their work

It was been widely argued that these two views are inherently opposed and lead to a simple trade off between the two. The report authors argue that in fact it is possible to achieve both aims at the same time using the methods detailed in the report.

> The set-up of siloed, and slightly out-of-date data was fine for 25 years ago. This is no longer a viable model. We can have multiple eyes on the data in near real-time

"...all pseudonymised national detailed health datasets should be treated as if they have name and address in the clear, both practically and in our governance, regulatory, and legislative frameworks"

## Better research into privacy

> ...teams managing data access requests in organisations such as NHS Digital and elsewhere are commonly applying rules of thumb, or intuition, to inform their proportionate responses. It would be better for the whole community – patients, researchers, and those serving their needs – if this were addressed with a modest programme of applied health research from a national funder

## Recommendations

* There is no new emergency, but TREs should be used, and data dissemination should not expand
* UKRI/NIHR should resource applied methods research into privacy preservation
* Revise the definitions of ‘anonymous’, ‘identifiable’ and ‘linked’ data; add a new category of ‘pseudonymised but re-identifiable’
