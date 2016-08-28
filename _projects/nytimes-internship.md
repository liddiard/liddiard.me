---
title: The New York Times CMS dashboard search
description: Implementing faster, more accurate resource location with Elasticsearch
order: 13
involvement: developer
skills: Backbone, Marionette, Elasticsearch, React, Java 
num_images: 4
---

During my summer 2016 internship at The New York Times, I worked as a developer on the CMS team. I reimplemented the CMS's main dashboard search, a feature used hundreds of times per day by journalists to find specific pieces of content like articles, images, and videos.

The existing search was slow. Returning results could take several seconds, and results were not very accurate. The search form required a user to fill out several inputs to explicity filter by fields like content type, section, and source to obtain relavent results.

The source of the slowness was a complex SQL query that joined several tables to search and produce a result. The solution was to index searchable parts of the database in a denormalized document data structure stored in Elasticsearch, which is optimized for full-text search using an [inverted index](https://www.elastic.co/guide/en/elasticsearch/guide/current/inverted-index.html), and to keep it up to date with the database by hooking into The Times's internal ActiveMQ-brokered event system. A Gaussian decay function weights content publishing closer to the current time more highly. 

The new implementation sped up search performance 10x.

In addition to this backend work I implemented with another intern, I designed and coded a new search frontend in Backbone, Marionette, and LESS. The old search displayed results in a table that was difficult to scan quickly because key information for identifying an asset was spread across the screen, and a result item lacked visual heirarchy even though some data were more important than others.

For the new search, I formatted results in a familiar Google-style layout emphasizing a matching item's slug, a human-readable, quasi-unique identifier for a piece of content that a journalist would recognize. I got rid of the several form elements in favor of a single search box. The new UI displays example searches indicating how to search for specific content types, sections, etc., just by typing them in the query. Search results update as one types for instant feedback.

In addition to the search project, I worked with the frontend team to use the Elasticsearch infastructure we set up to create the beginnings of a live updating, React-based editing console, a place where reporters, story editors, and copy editors will be able to keep tabs on the status of stories they are watching.