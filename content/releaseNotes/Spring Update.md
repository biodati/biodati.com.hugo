---
author: Wendy Zimmerman, PhD
title: The Spring update is Here!
date: 2020-04-06
description: Photo by Dei R. on Unsplash
image: "flowers.jfif"
---

It’s Spring, the daffodils are blooming, and we made a few changes to the curation interface to speed the workflow for those using our Bulk Loading feature.

We reformulated the form to enhance nanopub validation so it’s less intrusive to the workflow. Assertion validation now occurs in the background, so you can continue to edit while waiting for your long list, (of hundreds ****or thousands of assertions in your nanopub), to complete validation. A new status icon will let you know if validation for an assertion is incomplete. The validation status will update whenever the nanopub is saved or refreshed. The validation status is also displayed on the Knowledge Search page.

Reviewing nanopubs with hundreds of assertions is also challenging. We have updated nanopub Review and nanopub Edit to make this easier, by adding a scroll bar and filter search capability. This is the same filter search that we have for searching Edges in Networks. You can now filter assertions in a nanopub by Subject, Object, or Relation.

## ChangeLog

## Studio

### Added

* Scroll and Search capability for assertions in nanopub Review and nanopub Edit.

* Assertion validation status displayed in Knowledge Search, nanopub Edit and Add Knowledge.

### Changed

* Flow for validation — 1) Save nanopub 2) nanopub saved to database 3) nanopub retrieved from database with any cached validations 4) batch process kicked off to validate any assertions/annotations that are not already cached 5) nanopub retrieved at this point will have all assertions/annotation validations available from cache.
