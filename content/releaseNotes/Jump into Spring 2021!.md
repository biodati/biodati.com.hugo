---
author: Wendy Zimmerman, PhD
title: Jump into Spring 2021!
date: 2021-03-08
description: Photo by Dei R. on Unsplash
image: "flowers2.jfif"
---

## **BioDati Studio 0.9.0**

Today we are celebrating our Spring release of 2021. We were very busy this winter updating Biodati Studio, both the front and back ends. We have completely replaced the authentication, and updated our login process to make it easier and more secure. Current users may need to reset their passwords — just use the Forgot Password link.

Under the hood, the API has been updated, leading to faster processing and better performance. In addition to which, BEL has been refactored, improving BEL Completion, Nanopub validation, and enhancing the Assertion to Edge pipeline.

On the front end, error messaging has been improved to provide better clarity, and the completion engine has been enhanced for better performance - it now closes parenthesis for you.

We have enhanced access to MESH terminology. This means more terms to use for annotations. For example, users can now add annotations pertaining to the age and sex of clinical trial participants. This can be particularly useful in the study of aging, heart disease, and cancer.

In addition to all these updates, we have added some **New Features**.

Under Knowledge Search, you will find three new icons when you hover your cursor over a nanopub. These new links are designed to aid in curation. The first is an edge report. This lists all the edges associated with the nanopub- not just the original assertions, but the orthologous and computed edges as well. The second allows you to copy the nanopub URL. While the third icon, which resembles a curled sheet of paper, is the nanopub by reference report. This lists all nanopubs associated with a particular reference. This report can be very helpful when you are checking to see which assertions are already in your database.

From the Project page, you can now add together and find the intersection of networks. This feature should speed your pathway building and analysis. Just click the check box to the left of the networks that you wish to work with, then click the new Union and Intersection icon (two sheets with a “+” above the Network list), and follow the prompt. Please see [http://help.biodati.com/sections/networks/Combining_Networks/ ](http://help.biodati.com/sections/networks/Combining_Networks/)for more information.

There is also a new Facet to use when Searching for Edges to add to your Networks, “updated edges”. Each time a nanopub is saved, all it’s edges are updated in the edge store. This facet will allow you to look for new edges, by limiting your search to edges that have been recently updated.

The “Copy” Network function has been added to the Network landing page to aid the network building workflow.

To those of you with custom analytics, we have also consolidated The API endpoints, this consolidated endpoint takes over for nanopubstore/networkstore/etc. It provides the same functionality just from one endpoint.

## ChangeLog

## Studio (0.9.0)

## Added

* Enhanced access to MESH terminology

* Nanopub edge report

* Nanopubs by reference report

* Link to nanopub URL on Knowledge Search page.

* Updated edges facet for Edge Searches

* Copy Network added to the Network landing page.

* Union and intersection of Networks.

## Fixed

* Validation of deg(a())

* Validation of single amino acid code used with pmod()

## Changed

* Updated to use Angular 10 for Studio

* Active Network and Active Project are now stored in the user profile.

* Logging in/registration. Refresh tokens should be active for 30 days.

* The completion engine has been enhanced.

* BEL refactored

* Subject only assertion now generates an edge

* Nested BEL Assertions may create additional edges. For more information see http://help.biodati.com/sections/overview/The%20BEL%20pipeline/

## BEL and BioDati API

## Changed

* BEL API is now hosted under the Nanopubstore API.

* Significant changes in the API’s, routes and options.

* There is now just one Biodati API that includes all of userstore, networkstore, nanopubstore, studio-common and studio_api. We've consolidated 5 git repositories into one. This simplifies deployment and development.

* We are now using a single background task queuing system across the board.

* Converted from multiple arangodb databases into two: biodati and bel - this will allow things like cross network/edge/nanopub/project queries using a single database query rather than multiple steps.

* Updated to the most recent version of arangodb which has better built in search functionality allowing us to greatly improve the edge searching.
