---
title: "Further Work"
weight: 1000
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Further work

I love this review and it's probably the best blueprint for real change that I've seen, although it's worth mentioning that I've seen 10+ such documents that have not led to real change, not because of deficiencies on their part but because of ignorance, apathy, and unchecked commercial interests that have pushed methodologically inferior and expensive tools and methods to senior managers who don't know what they're buying.

Clearly in a document of this size every detail will not be covered, so here is a non exhaustive list of things that I would like to see further work on now the report has been published.

## Publishing code derived from databases

I have an [open issue](https://github.com/nhsx/open-source-policy/issues/6) about this on the NHSX open code policy repo. My work involves using data that comes from off the shelf databases, and the code that we write quite naturally includes database schemata and variable names. The [guidance from gov.uk](https://www.gov.uk/government/publications/open-source-guidance/when-code-should-be-open-or-closed) is very clear:

> You should keep some data and code closed, including:
>    * keys and credentials
>    * algorithms used to detect fraud
>    * unreleased policy

[...]

> You should open all other code. This includes:
>    * configuration code
>    * database schema
>    * security-enforcing code

Nonetheless, I do not have permission to publish anything that implies the structure or even the variable names of any of the databases that we work with. This makes publishing some of our best code difficult or impossible. There are two objections given:

* Publishing table names is a security risk
* The database vendors own the "IP" of the schema and even the variable names and we are therefore not permitted to publish this information.

I have asked a vendor about this second issue and they refuse to talk to me. They will only talk to my Trust's representative; my Trust refuses to ask them for this information.

I desperately need crystal clear guidance on the legal and technical aspects of this issue from inside the NHS so I can win this argument once and for all. NHSX's open code guidance is great but as the linked issue makes clear it does not currently have anything to say on this issue. Hopefully it will in the future. 

## Software licensing

There is a section addressing "myths" about open working in the [section on open working](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis/better-broader-safer-using-health-data-for-research-and-analysis#modern-open-working-methods-for-nhs-data-analysis) and it is very welcome and sensible. There is quite a large issue lurking beneath the surface which I would like to highlight. The report reads:

> Adopting open working practices does not mean other countries or industry can exploit intellectual property created with state funds: there should be a robust and thoughtful exceptions framework to impose commercial licenses or restrictions on review and (separately) re-use of publicly funded code, where this is actively helpful; but this closed approach should be used in a planned and deliberate fashion, where it meets national strategic objectives, not as the unplanned default approach

I have heard this objection to open code many times, and have tried to address it where I can. On the face of it it seems very sensible: share the code with, say the NHS, and exploit the code commercially where it can be exploited commercially. The original text is not entirely clear but I am assuming that they are referring to dual licensing of code. I have filed [an issue on NHSX's open code guidance](https://github.com/nhsx/open-source-policy/issues/18) on this subject. I am no expert but I am dubious as to whether the benefits of dual licensing code can be realised in the NHS. It's a notoriously tricky area and my fear is that dual licensing will

a) scare off people who would otherwise have contributed, because they don't work in an organisation which can use a free licence and so would have to pay to use a project they themselves contributed to

b) will not produce anywhere near the revenue to make all the administration worthwhile- companies which can't use a free licence will either just reimplement the code themselves or just use a truly free alternative.

## Security and information governance

The "platforms" section of Barriers to RAP in *Open working* rather states "It is reasonable for local IT teams to be cautious, especially for more versatile tools such as Python, and especially when staff are working with more sensitive data", but gives no further details. 

It is unclear what the intention of this statement is. What is caution in this case? Not allowing installation at all? And what is covered other than Python? R? Julia? JavaScript? What qualifies as "sensitive data"? Any row level data at all?

Interpreted literally this statement appears to mean "Python should never be used to interact with row level patient data on a computer issued by a typical NHS organisation [such as a provider trust]". I don't think that can possibly be the intention (?) but I'm not clear.

Regardless, there is a clear need for crystal clear guidance on security and information governance, which will cover things like:

* Language (R, Python, Julia, etc.)
* Libraries (E.g. The R-based CRAN store of packages is scrutinised by a volunteer team, by contrast Python's PyPI is not and you can deploy anything you like there)
* Docker, Linux, hosting of analytic products (e.g. using Azure or RStudio) in the cloud/ behind the firewall
* Should some users be allowed access to software (like Python) that others are not? Should some users have (some) admin privileges on their machine where other users are not given the same privileges?
* Is free software intrinsically less safe or trustworthy than paid software? Clearly completely unknown software from an unknown individual or organisation is less trustworthy than R, but how do IT teams learn to make judgements like this when they are not familiar with the software from their work?

