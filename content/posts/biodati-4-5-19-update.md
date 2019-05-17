---
title: "BioDati Studio: 4/5/19 Update"
date: 2019-05-04T00:00:00Z
author: "Ally Rose"
tags: ["random"]
thumbnail: "/img/thumbnails/ladybug.jpeg"
tagline: "Spring is finally here and the plants aren’t the only things growing this season. Here are some ways BioDati is blossoming:"
---

Spring is finally here and the plants aren’t the only things growing this season. Here are some ways BioDati is blossoming:

Added:

You now have the ability to export, edit, and then re-import nanopubs! Everyone here at BioDati is really excited about this one.
There is selectable text in edge search results table.
There’s officially a Create Draft Network from NanoPub Assertions. We’ve been having lots of fun with this one.
We’ve launched Validation Search Facets for Knowledge/Nanopub searches.
Changed:

The Finalized status is now recorded as finalized in the gd_status metadata field instead of published. (for semantic congruency, consistency is key!)
BEL API /nanopubs/validate now returns the entire nanopub by default with nanopub[‘nanopub’][‘metadata’][‘gd_validation’] = [<validation_results>]
“gd:” metadata tags are now presented as “gd_”, e.g. gd_status, etc. in the NanoPub metadata to make it easier to use in search and other types of queries.
Fixed:

With spring comes bugs: We had a bug with the shortest path query in Edge search, but we called our exterminators. (Thanks, Grant!)

This is Grant!
Bugs with protein: Network visualization — p(X, var()) was showing up as an RNA instead of a protein. Regex has been updated for BEL functions.