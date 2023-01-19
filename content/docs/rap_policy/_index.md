---
title: "RAP policy in government and the NHS"
weight: 15
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

## Introduction

Note that much of the material on this page is reproduced verbatim from sources that are licensed under OGL and MIT, therefore links are provided to the source material in all cases.

RAP is becoming a widely known term, but for the sake of clarity it can be simply described as

> [a process in which code is used to minimise manual, undocumented steps, and a clear, properly documented process is produced in code which can reliably give the same result from the same dataset]({{< relref "docs/codefirst/_index.md#reproducible-analytical-pipelines" >}}).

The [Goldacre review's](https://www.gov.uk/government/publications/better-broader-safer-using-health-data-for-research-and-analysis) summary recommendation 17 states that RAPs should be

> the core working practice that must be supported by all platforms and teams; make this a core focus of NHS analyst training.

## Levels of RAP

Within the [NHS Digital RAP community of practice](https://nhsdigital.github.io/rap-community-of-practice/introduction_to_RAP/levels_of_RAP/) there are three levels of RAP given:

> * Baseline - RAP fundamentals offering resilience against future change
> * Silver - Implementing best practice by following good analytical and software engineering standards
> * Gold - Analysis as a product to further elevate your analytical work and enhance its reusability to the public

These are summarised following.

### Baseline RAP

* Data produced by code in an open-source language (e.g., Python, R, SQL).
* Code is version controlled (see [Git basics][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/git/intro-to-git.md] and [using Git collaboratively][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/git/using-git-collaboratively.md] guides).
* Repository includes a README.md file (or equivalent) that clearly details steps a user must follow to reproduce the code (use [NHS Open Source Policy section on Readmes](https://github.com/nhsx/open-source-policy/blob/main/open-source-policy.md#b-readmes) as a guide.
* Code has been [peer reviewed][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/implementing_RAP/code-review.md].
* Code is [published in the open][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/implementing_RAP/how-to-publish-your-code-in-the-open.md] and linked to & from accompanying publication (if relevant).

### Silver RAP

* Outputs are produced by code with minimal manual intervention.
* Code is well-documented including user guidance, explanation of code structure & methodology and [docstrings][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/python/python-functions.md#documentation] for functions.
* Code is well-organised following [standard directory format][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/python/project-structure-and-packaging.md].
* [Reusable functions][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/python/python-functions.md] and/or classes are used where appropriate.
* Code adheres to agreed coding standards (e.g PEP8, [style guide for Pyspark][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/pyspark/pyspark-style-guide.md]).
* Pipeline includes a testing framework ([unit tests][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/python/unit-testing.md], [back tests][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/python/backtesting.md]).
* Repository includes dependency information (e.g. [requirements.txt](https://pip.pypa.io/en/stable/user_guide/#requirements-files), [PipFile](https://github.com/pypa/pipfile/blob/main/README.rst), [environment.yml][https://pip.pypa.io/en/stable/user_guide/#requirements-files]).
* [Logs][https://github.com/NHSDigital/rap-community-of-practice/blob/main/docs/training_resources/python/logging-and-error-handling.md] are automatically recorded by the pipeline to ensure outputs are as expected.
* Data is handled and output in a [Tidy data format](https://medium.com/@kimrodrikwa/untidy-data-a90b6e3ebe4c).

### Gold RAP

* Code is fully [packaged](https://packaging.python.org/en/latest/).
* Repository automatically runs tests etc. via [CI](https://github.com/skills/continuous-integration)/CD or a different integration/deployment tool e.g. [GitHub Actions](https://docs.github.com/en/actions).
* Process runs based on event-based triggers (e.g., new data in database) or on a schedule.
* Changes to the RAP are clearly signposted. E.g. a changelog in the package, releases etc. (See gov.uk info on [Semantic Versioning](https://github.com/alphagov/govuk-frontend/blob/main/docs/contributing/versioning.md))

## Appendix: Source materials

* [Government analysis function RAP strategy](https://analysisfunction.civilservice.gov.uk/policy-store/reproducible-analytical-pipelines-strategy/)
* [Analysis Function RAP Strategy 2023 implementation plan](https://www.ons.gov.uk/aboutus/whatwedo/programmesandprojects/analysisfunctionrapstrategy2023implementationplan)
* [Public Health Scotland RAP](https://www.isdscotland.org/About-ISD/Methodologies/_docs/Reproducible_Analytical_Pipelines_paper_v1.4.pdf)
* [NHS Digital community of practice](https://nhsdigital.github.io/rap-community-of-practice/)