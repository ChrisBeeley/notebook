---
title: "Copyright"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Copyright

## Intellectual property

Intellectual property is an umbrella term which principally refers to copyright, trademarking, design rights, and patents. Trademarks and design rights, although they can sometimes be relevant in the world of software development ([for example, in the story of the Debian linux distribution rebranding Firefox to Iceweasel](https://en.wikipedia.org/wiki/Mozilla_software_rebranded_by_Debian)) are only obliquely related to the present matters of discussion and will not be explored any further here.

Under the [Berne convention](https://en.wikipedia.org/wiki/Copyright), copyright is assigned automatically to any expression (such as a piece of music, a book, an artwork, or a set of computer code). It is not necessary to apply for copyright. Where a literary, dramatic, musical or artistic work, or a film, is made by an employee in the course of her employment ("work for hire"), [her employer is the first owner of any copyright in the work](https://en.wikipedia.org/wiki/Copyright#Ownership) (unless they agree otherwise). The expression "in the course of employment" is not well defined but the crucial difference is between "contract of service" (eg as an employee) and "contract for services" (eg as a freelancer). Individuals working under a contract of service will usually maintain copyright (unless they agree otherwise).

Patents are a very different thing, and give intellectual property over an idea. Some argue that software patents [should not exist at all](https://www.gnu.org/philosophy/software-patents.en.html) and there is much debate about where the boundaries should be between ideas in software that can and cannot be patented (for example in the case of [non-obviousness](https://webarchive.nationalarchives.gov.uk/20140603152456/http://www.ipo.gov.uk/response-inventive.pdf)). The ideas and debates in this area are very important and interesting in the world of software but given the reservations many free software proponents have about software patents (and the complexity and expense of acquiring and defending software patents) they are clearly not a suitable thing for NHS data science teams to acquire and will not be discussed further here.

Copyright, on the other hand, cannot be avoided since, as discussed above, it is automatically attributed at the moment of creation to the individual creator(s) or their employing organisation. Failing to discuss this issue at the beginning of a project could lead to confusion and disagreement once a project has begun or been completed. In a sense the holder of copyright for a piece of software licensed as FOSS (whether permissively or as copyleft) is unimportant, since the software licence ensures that anybody can use the code for any purpose (subject to the restrictions of copyleft where this is applied). However, one important power that a copyright holder has on a piece of open source software is the ability to *relicense*. Relicensing takes place when copyright holders wish to take existing code and place it under another licence. There is a great deal of confusion about exactly how to ensure that code can be relicensed legally, but there are examples of where this has been done successfully [here](https://dolphin-emu.org/blog/2015/05/25/relicensing-dolphin/), [here](https://blogs.fsfe.org/ciaran/?p=58), and [here](https://www-archive.mozilla.org/mpl/relicensing-faq). In short, it is widely believed that in order to relicense computer code it is necessary to get the approval of all, or nearly all, of the contributors. Some projects, such as the Linux kernel, have thousands of contributors and are therefore widely seen as impossible to relicense. Where only one individual or organisation holds the copyright relicensing is simple. The FSF ensures that the [copyright of all of their software projects is explicitly granted to them by all contributors](https://www.gnu.org/licenses/why-assign.en.html) so they can responsibly exercise the powers that being a copyright holder grants.

## Crown copyright

The data scientists at the Government Digital Service have no need to concern themselves with copyright in their day to day work since

>All code produced by civil servants is automatically covered by Crown Copyright

[Source](https://www.gov.uk/service-manual/technology/making-source-code-open-and-reusable#licensing-your-code).

The NHS, by contrast, because is a patchwork of national and local bodies (NHS England, Nottingham City CCG, Nottinghamshire Healthcare NHS Trust...), can potentially produce code that is copyright to any one of hundreds of different organisations. When these bodies cooperate they could produce code licensed to a confusing patchwork of different organisations. Individuals working for the NHS should be able to cooperate on open source projects without engaging in lengthy negotiations about which organisations will hold copyright and, furthermore, it is desirable that individuals in other NHS organisations can freely contribute without worrying about whether their employer expects to see their "share" of the intellectual property. A solution to this problem would be for there to be a presumption that NHS staff releasing open source code do so under a Crown copyright licence, unless there is a reason why an exception to this rule should be made. There is [precedent for assigning copyright to the crown](https://en.wikipedia.org/wiki/Crown_copyright#United_Kingdom) but assigning it routinely to open source code produced by NHS staff has not been tried previously.



