---
title: "Open Source"
weight: 2
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Open source

## Introduction

As discussed in an earlier chapter, section 12 of the NHS service standards compels those who follow it to "Make new source code open". Elsewhere, the NHS is being enjoined to use (as well as produce) open source software (REF). Using free software sounds like an obvious thing for a public sector body to do, and open sourcing its own code and allowing other bodies to make use of it also sounds on the surface like a sensible approach. It's important first to understand what the words "free" and "open" actually mean.

Open source software licences are not well understood within the NHS, and the important distinction between copyright and licensing even less so. This chapter will cover what free and open source software is, discuss why software licensing is so important, cover the most commonly used software licences, and explain the crucial distinction between holding the copyright for a body of code and having a licence to modify and distribute it.

## "Free" and "open"

The words *free* and *open* both have everyday meanings in English, and the word *free* is perhaps doubly confusing since it can refer to something that is either provided without cost ("free as in beer") or without restriction ("free as in speech"). Confusion often arises because much of free and open source software is both free of cost and provided without restriction. However, when organisations like the Free Software Foundation (FSF) use the word free:

>...you should think of "free" as in "free speech," not as in "free beer" (https://www.gnu.org/philosophy/free-sw.en.html)

Indeed, being able to charge money for copies of source code is part of the meaning of "free" within the definition of free software given by the Free Software Foundation (Ibid.).

The word *open* is sometimes used to mean "visible", and sometimes in a more restrictive meaning of "free and open source". Merely releasing code, for example on a website, and making it visible, gives nobody else the right to use, modify or distribute it. In order to avoid this confusion, truly free and open source software is often designated as such- Free and Open Source, often abbreviated to FOSS. The remainder of this chapter will focus on FOSS. Even the meaning of FOSS can be controversial, since there is some disagreement about how "free" different software licences are. It is standard practice to take the list of [FOSS licences maintained by the FSF](https://www.gnu.org/licenses/license-list.html) and the [Open Source Initiative](https://opensource.org/licenses/alphabetical) (OSI) as being the canonical list of free licences.

## Free and open source software

Before considering some of the common licences it is worth understanding the different perspectives of the FSF and the OSI and how they affect for what kinds of licence they typically advocate for. The FSF was founded by Richard Stallman (RMS) who became convinced of the need for software freedom through a number of incidents that occurred when he worked at MIT's AI laboratory in the 70s and 80s.

The most famous example of these incidents relates to [a modification that RMS had made to a printer in use at the lab](https://www.oreilly.com/openbook/freedom/ch01.html). He had modified the printer software so that it would email everyone waiting for print jobs when it jammed, so that they could go and unjam it and prevent a backlog of printing from forming after a jam. When the printer was replaced with a newer version RMS found that the source code was not provided (as it had been with the first printer); moreover when he requested the source from someone who had worked on the printer he was told that it was not available. RMS was therefore unable to modify the new printer software to send emails after a jam as he had done previously. This and other incidents of this kind convinced RMS of the need to protect what he went on to call the "four freedoms" of software:

- The freedom to run the program as you wish, for any purpose (freedom 0).
- The freedom to study how the program works, and change it so it does your computing as you wish (freedom 1). Access to the source code is a precondition for this.
- The freedom to redistribute copies so you can help others (freedom 2).
- The freedom to distribute copies of your modified versions to others (freedom 3). By doing this you can give the whole community a chance to benefit from your changes. Access to the source code is a precondition for this.

Non technical readers may be confused as to the designation of the first freedom as freedom 0. This is a slightly whimsical extension of the custom in most programming languages (C, for example, or Java, but not R) to begin numbering elements of an array at "0" rather than "1".

Any licence that meets these conditions is considered by the FSF to be free. However, the FSF prefers licences which are "copyleft". [Copyleft](https://en.wikipedia.org/wiki/Copyleft), which is a distorion of the word "copyright", is a form of licensing which allows a work to be reused, adapted, and distributed, but forces individuals who make use of that right to give the same rights to any derivative works they produce . Copyleft is therefore a form of licensing which protects the rights of all of the users who use derivative works. The most famous example of a copyleft licence is the GPL, more on which later.

Copyleft can be contrasted with "permissive" licences, which give similar rights to reuse, modify, and distribute, but do not mandate that individuals exercising those rights give the same rights over derivative works. There is some debate as to which of these types of licences is the most "free". The FSF argue that since permissive licences allow others to take away your rights over source code, that they are less free. Others (such as the OSI) [state no preference between copyleft and permissive licences](https://opensource.org/faq#copyleft) and recommend both approaches depending on the project. Still others argue that since permissive licences make fewer demands of individuals reusing and modifying code they are freer than copyleft licences. This debate echoes [Erich Fromm's classic distinction](https://en.wikipedia.org/wiki/Escape_from_Freedom) between "freedom from" (freedom from having your rights over source code taken away) and "freedom to" (freedom to reuse and modify code without sharing the derivative work).

It is not necessary for this argument to be settled here- for the current purpose it is enough to understand what copyleft licences (like the GPL) do and what permissive licences (such at the MIT licence) do and to make sure that data science teams in the NHS are able to choose the licence that is best for their individual project.

## Licences

### Permissive

The most famous examples of permissive licences are the MIT and BSD licences. These licences allow reuse and modification but, unlike copyleft licences, also allow the code to be incorporated into a proprietary codebase without making that codebase subject to the terms of the original licence.

#### MIT

The [MIT licence]((https://choosealicense.com/licenses/mit/#)) is one of the shortest and simplest licences, and reads as follows:

MIT License

Copyright (c) [year] [fullname]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

>THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

This licence shows all the typical features of an open source licence very clearly- it gives permission to others to use, copy, and modify the source, it ensures that the copyright and permission notice is displayed in any modified software, and it includes a notice indicating that the software is provided without warranty of any kind.

#### Apache 2.0

The Apache licence is quite a similar permissive licence. It is quite a lot longer than the MIT licence, in the main because it spells out more legal terms which are left implicit in the MIT licence. The main important difference is that it places more obligations on individuals distributing the code or modified versions to include materials from the original codebase. Specifically, it states:

>1. You must give any other recipients of the Work or Derivative Works a copy of
this License; and
> 2. You must cause any modified files to carry prominent notices stating that You
changed the files; and
> 3. You must retain, in the Source form of any Derivative Works that You distribute, all copyright, patent, trademark, and attribution notices from the Source form of the Work, excluding those notices that do not pertain to any part of the Derivative Works; and
> 4. If the Work includes a “NOTICE” text file as part of its distribution, then any
Derivative Works that You distribute must include a readable copy of the attribution notices contained within such NOTICE file, excluding those notices that do not pertain to any part of the Derivative Works, in at least one of the following places: within a NOTICE text file distributed as part of the Derivative Works; within the Source form or documentation, if provided along with the Derivative Works; or, within a display generated by the Derivative Works, if and wherever such third-party notices normally appear. The contents of the NOTICE file are for informational purposes only and do not modify the License. You may add Your own attribution notices within Derivative Works that You distribute, alongside or
as an addendum to the NOTICE text from the Work, provided that such additional attribution notices cannot be construed as modifying the License.

As can be seen, this adds to the licence conditions of the MIT licence by forcing distributors of code to state changes that have been made, as well as to include the contents of any NOTICE file from the original codebase.

#### Other licences

Although there are many other permissive licences, in the interest of brevity they will not be discussed further here. [This is a very comprehensive list of licences (with some commentary from the perspecitve of the FSF)](https://www.gnu.org/licenses/license-list.html).

### Copyleft

Copyleft licences, as described previously, are quite different to permissive licences. They:

>impose substantial limitations on those who create and distribute derivative works based on works that use these licenses. The GNU General Public License (the GPL License) explicitly requires that derivative works be distributed under the terms of the GPL License and also that derivative works may only be permitted to be distributed under the terms of the license. The Mozilla License imposes different and less restrictive terms on the licensing of derivative works.

[@understandingopensource]

Copyleft licences therefore frequently find a use when the publishers of open source code want to make sure that the code in them is not relicensed and incorporated into a proprietary system. There is no prohibition on what the code is used for, or whether the distributors charge a fee, as long as the distributor of the code is prepared to open source all of the code in the derivative work, not just the piece originally licensed under the GPL. Quite obviously it is therefore extremely unpopular companies and individuals who are in the business of selling proprietary code. It is important to note that the GPL comes into effect whenever the code is *distributed* in some way- for example on a CD or as a download from the Internet. This distinction will become important later in this section.

#### GPL

The GPL (general public licence) is the cornerstone of the philosophy of the FSF, and it enshrines the *four freedoms* described previously. Many of the key projects championed by the FSF (such as the GNU Emacs editor and the GNU C Compiler, as well as the Linux Kernel) are licensed under the GPL. [The licence begins with a nice summary of its terms](https://choosealicense.com/licenses/gpl-3.0/#):

>GNU GENERAL PUBLIC LICENSE
>
>Version 3, 29 June 2007
>
> Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
>
>Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.
>
>Preamble
  The GNU General Public License is a free, copyleft license for
software and other kinds of works.
  The licenses for most software and other practical works are designed
to take away your freedom to share and change the works.  By contrast,
the GNU General Public License is intended to guarantee your freedom to
share and change all versions of a program--to make sure it remains free
software for all its users.  We, the Free Software Foundation, use the
GNU General Public License for most of our software; it applies also to
any other work released this way by its authors.  You can apply it to
your programs, too.
  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
them if you wish), that you receive source code or can get it if you
want it, that you can change the software or use pieces of it in new
free programs, and that you know you can do these things.
  To protect your rights, we need to prevent others from denying you
these rights or asking you to surrender the rights.  Therefore, you have
certain responsibilities if you distribute copies of the software, or if
you modify it: responsibilities to respect the freedom of others.
  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must pass on to the recipients the same
freedoms that you received.  You must make sure that they, too, receive
or can get the source code.  And you must show them these terms so they
know their rights.
  Developers that use the GNU GPL protect your rights with two steps:
(1) assert copyright on the software, and (2) offer you this License
giving you legal permission to copy, distribute and/or modify it.
  For the developers' and authors' protection, the GPL clearly explains
that there is no warranty for this free software.  For both users' and
authors' sake, the GPL requires that modified versions be marked as
changed, so that their problems will not be attributed erroneously to
authors of previous versions.
  Some devices are designed to deny users access to install or run
modified versions of the software inside them, although the manufacturer
can do so.  This is fundamentally incompatible with the aim of
protecting users' freedom to change the software.  The systematic
pattern of such abuse occurs in the area of products for individuals to
use, which is precisely where it is most unacceptable.  Therefore, we
have designed this version of the GPL to prohibit the practice for those
products.  If such problems arise substantially in other domains, we
stand ready to extend this provision to those domains in future versions
of the GPL, as needed to protect the freedom of users.
  Finally, every program is threatened constantly by software patents.
States should not allow patents to restrict development and use of
software on general-purpose computers, but in those that do, we wish to
avoid the special danger that patents applied to a free program could
make it effectively proprietary. To prevent this, the GPL assures that
patents cannot be used to render the program non-free.

The GPL, as can be seen, in this introductory section, lays out three important principles of the GPL- firstly, that it is designed to protect software freedom, including of derivative works. Secondly, any type of warranty is disavowed. Lastly, an explicit condition that patents arising from this code must themselves be licensed under the GPL. The FSF has strong views on software patents which are made very clear in this section- they state their view that software patents should not be able to restrict the freedom of software, but where they are, this licence prevents them from doing so.

The GPL goes on to give clearer guidance on the exact terms of the licence. For the sake of brevity it will not be discussed further here. Interested parties are directed to the link given above or for explanation on the terms to @understandingopensource.

#### AGPL

The AGPL (Affero General Public Licence) 1is more strongly copyleft than the GPL. Its status among the free software community is somewhat controversial, with [some individuals bitterly opposed to it](https://copyleft.org/guide/comprehensive-gpl-guidech10.html#x13-970009.16). The most important difference between the GPL and the AGPL is that the AGPL defines "distribution of code" (which, it should be remembered, is the point at which the provisions of the GPL come into force) as allowing a piece of software to be transmitted over a network. It is quite common in recent time for software companies to provide what is called "Software as a Service" (SaaS). An example would be [Google Sheets](https://en.wikipedia.org/wiki/Google_Sheets) which is a spreadsheet program delivered through a web browser. The user does not have to download any extra code to use it and therefore Google does not have to distribute the code. Software licensed under the GPL can therefore be provided as SaaS without any of the provisions of the GPL applying. The AGPL, therefore, exists to allow code to be licensed so as to ensure that even if it is provided as SaaS the entity making the provision is forced to release all of the modified code under the terms of the GPL.

#### LGPL

The LGPL (lesser general public licence) is so called because it ["because it does Less to protect the user’s freedom than the ordinary General Public License. It also provides other free software developers Less of an advantage over competing non-free programs."](https://opensource.org/licenses/LGPL-2.1)

The LGPL is designed for software libraries rather than full applications. A library (for the benefit of non technical readers) is a computer program that is used in the service of another computer program. For example, a piece of software that plays music might incorporate several different libraries to decode different music formats (such as MP3, FLAC, or AAC). The FSF recommend the LGPL ([or rather, did recommend it](https://www.gnu.org/licenses/why-not-lgpl.html)) in cases where there were already proprietary libraries that can be swapped in for free ones. For example, there was a free version of the C compiler (non technical readers should just not worry what this is- suffice to say that it's pretty important to make a Linux machine work) but licensing it under the GPL would have discouraged creators of proprietary software from using it. Their response would be simply to use a proprietary compiler, which would decrease the reach of free software and would not benefit the free software community in any way. The LGPL allows a piece of software to make use of the code in a library without making all of its source code open. It therefore preserves the free software library by making it a viable choice, even if it doesn't make other software that uses it free  ([source](https://copyleft.org/guide/comprehensive-gpl-guidech11.html#x14-10000010)). 

To understand where the LGPL does and does not allow the use of LGPL code in a proprietary product the FSF distinguish "works based on the library" and "works that use the library". Works that use the library can be incorporated within a proprietary product. What this means in practice is slightly fuzzy in practice but usually this means that a body of code will communicate with the library using some sort of standardised interface (e.g. sending some sort of stream of data in a particular way) and receive back something that itself is standardised in some way (for example, music that has been decoded). The library itself is being used for its intended purpose and is not substantially modified. Works that are based on the library will usually be works that reimplement or modify the actual library itself, changing the code and making it do something different or making it work in a different way. Under the LGPL works that do this have to release all of their code exactly as though the code was licensed by the GPL (Ibid).

#### Mozilla public licence

The Mozilla public licence (MPL) is like the LGPL except more weakly copyleft. Both allow the possibility over incorporating code released under their licence conditions to be used with a proprietary codebase. As we have seen, the LGPL places fairly clear restrictions on this reuse, which effectively prevent distributors of the code from modifying the original code in any way. By contrast, the MPL allows modified code to be incorporated into a proprietary codebase as long as the modifications are themselves shared, but *not* the rest of the code which they are distributed with.

## NHS data science and software licences

The best software licence for a data science project will vary case by case, but there are some broad things to consider when choosing one. The most important decision to make is between permissive and copyleft licences. Permissive licences are useful to maximise the impact of something in situations where there is no concern about what proprietary vendors might do with code. Releasing code under, for example, an MIT licence allows everybody, including individuals using proprietary code, a chance to use the code under that licence.

Using a copyleft licence is useful when there is concern about what proprietary vendors might do with a piece of code. For example, vendors could use some functionality from an open source project to make their own product more appealing, and then use that functionality to sell their product to more customers, and then use that market leverage to help them acquire *vendor lock in*. Vendor lock in is the state in which using a company's prodcuts ensures that you find it very difficult to move to another company's products. An example might be using a proprietary statistical software package and saving data in its proprietary format, making it difficult to transfer that data to another piece of software. If proprietary software companies can use code to make the world worse in this way, then choosing a copyleft licence is an excellent way of sharing your code without allowing anybody to incorporate it into a proprietary codebase. Proprietary software companies are free to use copyleft licensed code, but are highly unlikely to do so since it means releasing all of the code that incorporates it.


