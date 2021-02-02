---
author: Ally Rose
title: Product Update 10/6/19
date: 2019-10-06
description: This release is all about small enhancements that you can see and major ones that you cannot see that make it easier for us to deliver faster and with better quality.
image: "fox.jpeg"
---

### This release is all about small enhancements that you can see and major ones that you cannot see that make it easier for us to deliver faster and with better quality.

## Added

### User:

* Added ‘Fix’ status to the set of Nanopub statuses. You can also leave internal comments on nanopubs for curators during the review process. Check out the details [here](http://help.biodati.com/en/articles/3136693-using-the-fix-status)!

* AND/OR search facet features added. So you can filter on multiple facets at the same time. We’re using Boolean logic to fetch you the best results. Need [help](http://help.biodati.com/en/articles/3362814-facets)?

* Restricted nanopub updates to follow workflow restrictions for Finalized nanopubs, admins vs non-admins. (This is a temporary workflow until Groups/Permissions is deployed)

* Search facets are customizable per customer for nanopubs and networks

### API:

* Automated swagger documentation, so the endpoints are automatically kept in sync with the codebase

* All API endpoints are secured (except for the belapi). You must add a valid token to the header to access the API. Customer installations may be run with API endpoint security turned off if desired.

* Nanopubstore has a new API endpoint to view nanopubs by Pubmed ID, you’re able to obtain a report on all nanopubs/assertions/annotations (not exposed by the Studio UI yet)

* Studio_api endpoint handles all Studio related API endpoints that are not specific to nanopubstore/networkstore/userstore/belapi endpoints.

## Changed

### User:

* We changed the name of “Workspaces” to “Projects.” Projects just sounds better, right? A future planned change will be changing the project metadata tag in nanopubs to ‘collection’ to avoid any confusion.

![](https://cdn-images-1.medium.com/max/5096/1*FDMSBd13WrC1g7MS9HKOTA.png)

### API:

* Login/logout endpoints for API documentation access. Must be logged in to view API docs and even high-level database stats. No snoopers allowed!

* Separated the deprecated /nanopubs/importmany from the /nanopubs/import endpoint

* Adding nanopub status metadata “gd_status” = “draft” if no gd_status is set when saving nanopub

*  API Documentation is now at /docs instead of /swagger/ui/index.html, simplicity is key. Going to the service endpoint (e.g. nanopubstore.<server>.biodati.com) will open the service landing page with some basic stats on the service (if you are logged in) links to the API docs, and login/logout links

* Studio search facets code has been unified, simplified and is dynamic responding to the service (nanopubstore, networkstore) search results

## Fixed

### User:

* Nanopub file import now validates the imported nanopubs. They are also checked to make sure the status changes are in accordance to the permissions associated with normal and admin users (temporary — will be reworked soon with the Groups/Permissions feature being developed)

* Network edge search enhancement: option to clear the edge search form. We’re all about the small time saving improvements, they really add up! Now that I’m thinking about it… I could have saved time by not writing any of that.

## Removed

### API:

* The bservices API endpoint has been merged with studio_api endpoint and has been removed, edge search queries and edge node completions are now handled by new studio_api endpoint.

![Search requested above is human + mouse](https://cdn-images-1.medium.com/max/2000/1*HWF4V0VrP2iiHY92qesVvg.png)
