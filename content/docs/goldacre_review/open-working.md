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

## Reproducible analytical pipelines

> data scientists or analysts who had approached health data from other sectors... They repeatedly expressed how surprised they were to find that approaches regarded as standard in other parts of industry or academia – such as sharing code, or the everyday working practices of collaborative software development – were not yet the norm in teams working with health data


