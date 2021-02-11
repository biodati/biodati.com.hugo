---
author: Wendy Zimmerman, PhD
title: New for July!
date: 2020-07-11
description: We just released our new Project Feature.
image: "projects.jfif"
---

We just released our new Project Feature. “Projects” is designed to help you organize your work by providing a space for you and your team to group together knowledge (Nanopublications or nanopubs) and networks.

Projects are accessible from the BioDati Studio dashboard. For a walkthrough of the new Projects feature, see [look here](https://app.intercom.com/a/apps/q01vyayo/articles/articles/4169327/show).

July is not just about Projects! The Knowledge Search page has a new look and feel. It’s more streamlined with a bunch of added usability features; we are sure you will notice them as soon as you start looking for some Knowledge. Things like:

* Clicking on a nanopub allows you to directly review it

* Hovering over a nanopub and icons to export, copy, edit, delete or pin the nanopub now appear

* You can easily add nanopubs to a Project, Export them, or build a Temporary Network

* There is a new Project Facet available for filtering your knowledge, as well as a new earmark that highlights the nanopubs that have already been added to the active project

* Nanopubs can be individually added or removed from projects using the tabs under Nanopub Review

* Nanopubs can also be added to an active project as you curate them, under Knowledge Creation.

BioDati Studio now saves your Active Project and Active Network with your user profile. Finally! We are as happy as you are to have this feature.

The Dashboard banner displays the active project and the active network. You can go directly to the Project or Network page by clicking its name in the banner and inactivate a Project or Network by clicking the adjacent x in the banner.

The Knowledge Creation page has also been given some attention. Here are the details…

## ChangeLog

## Studio (0.8.0)

## Added

* Projects Feature

* Earmarks on search pages to show which Networks and nanotubes have already been added to an active Project

* Banner functions. Load or inactivate a Project or Network directly from the Banner

* Process a list of nanotubes (limited to the first 50) in Knowledge Search all at once

* Add them **All** to a Project, Export them, or build a Temporary Network

* All tables now have a sorting feature. (nodes, edges, assertions)

## Fixed

* Edges in nanopubs with Fix or Rejected Status cannot be used to build Networks

* Edit / Delete is disabled from Nanopub Review if the nanopub status is finalized

* Creating a new nanopub properly clears nanopub editing form.

* Network Search bugs

* Corrected Network creation bug that prevented multiple rounds of edge addition without reloading the Network.

* BEL API — PubMed mesh terms listing bug. Now API only returns the first namespace for any terms — e.g. Cell; CellLine

## Changed

* Active Network and Active Project are now stored in the user profile.

* Nanopub Review on the Nanopub search page is no longer a separate icon. Click a nanopub to go straight to review.

* Hover over a nanopub to reveal icons to export, copy, edit, delete, or pin the individual nanopub.

* In Knowledge Search, the hover icon for Edit will take you to Nanopub Preview if the nanopub is in Finalized status.
