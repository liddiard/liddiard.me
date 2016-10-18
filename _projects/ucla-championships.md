---
title: UCLA Bruins championships showcase
description: "Explore the Bruins’ history as the #1 winner of NCAA championships"
order: 13
link: http://uclabruins.com/championships
involvement: creator
skills: React, ES6, Sass, UI design
num_videos: 1
---

The UCLA Bruins have a rich history as the #1 winner of NCAA championships, holding the most NCAA titles of any university. Working as a web developer at UCLA Athletics, I set out to design an interactive page for exploring these over 100 titles that accommodates several use cases while remaining intuitive to navigate.

The use cases I identified, in order of priority, are:

1. Browsing championships in a specific sport
2. Browsing all championships chronologically
4. Locating information about a specific championship
3. Browsing championships in a specific year

In order to accommodate all of these use cases cleanly, I came up with a two-part radio button navigation that offers a year filter and a sport filter. Both filters are initially set to "All Years" and "All Sports," respectively, so that all championships are displayed by default. I decided to display championships in reverse chronological order because people are more likely to be interested in a championship that happened last year than say, one that happened in 1950.

Take a look at the accompanying video to see how the navigation filtering makes it easy to filter either by year or by sport, or to quickly locate a specific championship.

I built the web page with React because it offers a nice minimal framework for a small page like this while handling the manipulation of potentially hundreds of DOM elements with ease. Championship data is pulled from a Google Sheet for easy updating by non-technical internal users.
