---
title: The New York Times CMS dashboard search
description: Fast and accurate resource location with Elasticsearch
order: 15
involvement: developer
skills: Backbone, Marionette, Elasticsearch, React, Java
media:
  - type: image
    filename: 1.png
    caption: Immediately after clicking on the search bar, example searches appear below – one every few seconds.
  - type: image
    filename: 2.png
  - type: image
    filename: 3.png
  - type: image
    filename: 4.png
---

I worked as a developer on the CMS team in my summer 2016 internship at The New York Times. I reimplemented the CMS's main dashboard search, a feature used hundreds of times per day by journalists to find specific pieces of content like articles, images, and videos.

The existing search was slow and poorly formatted. Returning results could take several seconds, and the results were not very accurate. The search form required a user to fill out several inputs, explicity filtering by multiple fields to get relavent results. Results were shown in a table that was difficult to scan quickly because information to identify an asset was spread across the screen without any visual heirarchy.

The slowness was caused by a complex SQL query that joined several tables to search and produce a result. Our solution was to index searchable parts of the database in a denormalized document data structure with Elasticsearch and keep it up to date with the database by hooking into The Times's internal ActiveMQ-brokered event system.

The new implementation sped up search performance 10x.

In addition to this backend work I implemented with another intern, I designed and coded a new search frontend using Backbone, Marionette, and LESS. 

I formatted results in a familiar Google-style layout which emphasized a matching item's slug – a unique, human-readable identifier that a journalist would quickly recognize. I got rid of the several form elements in favor of a single search box. The UI displays example searches that demonstrate how to narrow a search easily by adding e.g. a relevant section or author to the query. Search results update as one types for instant feedback.

I also worked with the frontend team to use our new Elasticsearch infastructure create the beginnings of a React based, live-updating story status console, a place where reporters and editors will be able to monitor the progress of stories throughout the writing and editing process.