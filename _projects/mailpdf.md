---
title: Mail a PDF Online
description: Mail a document to anywhere in the U.S. under 60 seconds
order: 14
link: https://mailpdf.online
involvement: creator
skills: Node.js, Express, React, ES6, Sass
num_videos: 1
---

Mailing a PDF document is not a quick task for anyone who doesn't have easy access to a post office or a printer. And of course you'll also need an envelope and stamps, or else you'll need to stand in line at the post office to pay. All this even if you're trying to get an ultimately electronic document from point A to B.

Mail a PDF Online lets you do exactly what is says with a simple one-page interface, leveraging the [Lob](https://lob.com/) and [Stripe](https://stripe.com/) APIs for shipment and payment. Upload a PDF – we resize it to letter dimensions if necessary – and enter your "from" and "to" addresses – we validate them in case you make a mistake. Choose shipping options and pay, all under 60 seconds. Take a look at the accompanying video.

The interface is designed to be fast, self explanatory, and error tolerant. It provides concise information, instant feedback when appropriate, and upfront pricing.

This React and Node.js + Express application is deployed in a Docker container on [DigitalOcean](https://digitalocean.com/). All assets are compressed and distributed through [Cloudflare](https://cloudflare.com/) for quick access with any connection speed. [Let's Encrypt](https://letsencrypt.org/) and Cloudflare provide SSL.
