---
title: "BioDati Studio: 10/27/2018 Update"
date: 2018-10-27T00:00:00Z
author: "Ally Rose"
tags: ["random"]
thumbnail: "/img/thumbnails/deer.jpeg"
tagline: "BioDati always has something brewing, it’s no surprise that in only a month we’ve updated so much."
---

BioDati always has something brewing, it’s no surprise that in only a month we’ve updated so much.

Product Updates
High points:
The Network workflows are improved, we just love making your life easier!
Updated the BEL Pipeline, now it prioritizes manually updated NanoPubs and reduces the resource consumption.
All traffic is redirected to https now to get ready for groups/permissions!
What we’ve changed
Studio:
Help added to the top level menu. You no longer need help trying to find help!
Some of the menu item sub-selections have been reorganized to make accessing them easier.
You can now click on the Network name in the header and it will take you right to the network. Easy Peasy.
API- Path for Swagger documentation is now /swaggerui (was /swagger/ui)
Networks:
Edges/Nodes:

You can now click on the grid label and it will sort the column. Give it a shot. This includes selected edges.
Toggle selected nodes/edges allow you to work with only the items you have selected. All of the other scorned items will be hidden from view.
You can now delete selected items from the network.
The left menu now allows for you to Edit Network Information (Or ENI if you are in the know.)
Create Network:

Lots of changes. Please check out the help documentation for complete details. (Network Help Documentation)
Dashboard:
Networks are now first-class citizens; as such, they now have their own section.
The Network area is now above the workspace area. It just makes sense.

Search
Network:

Each row is highlighted for better visibility when the cursor is over it.
Clicking on a network will now directly open it.
The menu was removed from the rows and all of the selections for the network are visible on hover.
You can still see the network details by clicking on the preview icon.
Import:

If you import a single network, it will be made “active” and then opened.
If you import multiple networks, you will be redirected upon completion to the network search page
We fixed importing a network without edges/nodes properties
BELAPI
Updated:

We’ve improved the computed edges from Nanopub.
Fixed:

NanoPub validation bug for BEL 2.1.0-alpha is resolved! Hooray!
Added:

Warnings for BEL entities that are not in the terminology store (e.g. HGNC:TTTTTT) will throw a warning. WARNING: BioDati is heating up!
NetworkStore
Added:

Updated Swagger doc for Post method will include the list of reserved metadata keys that are used during the import process.
Post method now has 128M max request size limit. Let’s face it, no one wants a friend that doesn’t know their limit.
API- Path for Swagger documentation is now /swaggerui (was /swagger/ui)
Changed:

Delete Networks will return the count of deleted (Logically) documents.
Purge Networks will return the count of deleted (Physically) documents.
PUT API (Replace Network) executes an import when network id is not found in the Database.
The Method name is changed for TraversaltJGF to LineagetoJGF.
Fixed:

Immutable tag changed to be consistent: ‘gd:immutable’ instead of ‘gd:Immutable’
If Network JGF is imported without nodes, edges or metadata properties, these are initialized to empty objects.