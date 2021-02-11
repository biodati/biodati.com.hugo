---
author: Wendy Zimmerman, PhD
title: Bulk Curation 2020
date: 2020-03-15
description: Photo by Jorge Tung on Unsplash
image: "bulk.jfif"
---

So, you have hundreds of assertions to add to your nanopub. Don’t get overwhelmed! Use our new bulk curation tool. Corral those assertions into three columns on a spreadsheet, like excel or google sheets, copy them to your clipboard and click Bulk Import. It is that easy.

This was a popular user request. We always try to develop Studio in a tight feedback loop with our users. For help with this feature see our [Bulk Assertion Loading help](http://help.biodati.com/en/articles/3793525-bulk-assertion-uploads).

## ChangeLog

## Studio (0.4.1)

## Added

* Bulk Assertion Loading in knowledge curation form

## Changed

* We have removed the curation form metadata restriction. Previously you had to add a citation and assertion before being able to add metadata

* Assertions can be added with only subject, relation OR object — validation messages will be returned for any invalid BEL assertions — previously the form would not allow adding an assertion object without a subject and relation (this was to make the Bulk Assertion loading more functional)

## NetworkStore (0.3.1)

## Changed

* API allows unlimited edges in search edge results (from previous 10k max)

* API allows turning off facets in edge searches to improve performance of search results for searches with > 100k edges returned.
