---
title: Signing Day 2015
description: Official live updates for the UCLA Bruins’ Football Signing Day
order: 8
involvement: creator
skills: Django, PostgreSQL, AngularJS, caching, Amazon S3, web development
link: http://uclabruins.com/signingday
num_images: 5
---

Every year, UCLA Athletics hosts a central page for National Football Signing Day where it officially announces players as they sign with UCLA.

Previous years' pages involved a cumbersome process of manually editing HTML and re-saving the page after each recruit's announcement. This method was was both time consuming and error prone.

For the UCLA's 2015 National Signing Day page, I proposed and implemented a more elegant system: an admin interface where information about players who were likely to sign could be pre-filled by the Athletic Communications department accessible via an API. A player could be announced as signed simply by checking a checkbox, and the signing day page itself, which used an AngularJS app, pulled from the API in real time.

Anticipating a huge volume of traffic, I chose to deploy the backend application on a scalable Heroku dyno, implemented caching with Memcached, and did load testing with Load Impact. The API server held up to the high demand of hundreds of requests per second throughout the day.

After Signing Day, I "flattened" the page and spun down the API server to remove the page's external dependencies, making it more maintainable for the future.