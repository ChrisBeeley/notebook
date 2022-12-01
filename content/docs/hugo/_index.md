---
title: "Hugo"
date: 2021-10-20T16:59:40+01:00
draft: false
weight: 9999
---

## Configuration

* Configure config.toml so that the baseURL points to the actual location- either online or in your file system
    * This doesn't sound like much but it won't render properly unless you do this- even if using `hugo server` does render nicely
* Install dependencies if necessary with npm install

## Themes

I'm using three different themes, I'll list them all and talk about how to set them up another time

* Terminal
* Geek docs
* Notebook (this one)

## Writing

Small point, but start with the heading `##`, not `#`. `##` is the highest level of title that shows up in the structure preview (which appears in the top right of the page when using the notebook theme, e.g.).