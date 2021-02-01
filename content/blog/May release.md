---
author: Wendy Zimmerman, PhD
title: May Release-It’s all about Networks!
date: 2020-05-16
description: This May, while we are stuck in social distancing, it is all about Networks!
image: "test.png"
---

We have added a new Network Status feature. Like our Nanopub Status feature, Network Status is designed to aid the curation workflow. Networks can now be set in Draft, Review, Fix, Approved, Rejected, or Finalized Status. Like Finalized Nanopubs, Finalized Networks are immutable. Finalized Networks can be copied and downloaded, but nodes and edges cannot be added or removed. By default, all new networks are created in Draft status. Status can be updated using the status dropdown menu in Edit Network Information. Status is also a Facet available for Network Searches.

For clarity, we have replaced the Draft Network tab under Knowledge Search with the TempNetwork tab. You can still generate a Temporary Network from a list of nanopubs, under TempNetwork. This Temporary Network is not searchable in the Network Store and will expire automatically after 4 hours.

We have expanded the edge search capabilities in Network Creation to include searches by collection label and Nanopub ids. For more on searching edges to add to your Network, see [http://help.biodati.com/en/articles/2414018-searching-for-network-edges](http://help.biodati.com/en/articles/2414018-searching-for-network-edges). We have also included an indicator to inform the user if the returned edges already exist in the network.

***We have added a legend to our Network Viewer. It pops open when you click legend at the upper left in Network View.***

We are still tweaking the Knowledge Creation/ Nanopub Editor. We have added the ability to export your assertions in TSV, (Tab Separated Values), format, and we have updated the appearance of the assertion filter field for better clarity.

## ChangeLog

## Studio (0.7.0)

## Added

* Added Status to Networks.

* Extending the network with edges is now indicating which edges already exist in the network.

* Edge search query filter names changed to use either singular or plural (except for metadata since it’s both). Now you can use “relation” or “relations” in each query.

* Added nanopub_id (or nanopub_ids) as a search query filter.

* Select all Edge search bug fixed — which would select all edges, not just the filtered edges.

* Added legend to Network Visualization.

## Changed

* Removed Search boxes from Table Headers (e.g. Nanopubs Assertion list and elsewhere)

* Replaced the Draft Network under Knowledge Search with the TempNetwork

* TempNetworks now expire automatically after 4 hours.

* Collections facets on nanopubs will convert ‘collection’ to ‘collections’ and change String format to List of Strings

* Improved [https://help.biodati.com](https://help.biodati.com) help articles for enhancements

## Fixed

* Collections search facet in Network creation edge search

## NetworkStore (0.6.0)

## Added

* Added Status Feature.

* “expire_at” is added to the temporary network record.

* Added Immutable to finalized Networks.