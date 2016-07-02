---
title: kikl.co
description: Tiny, short-lived, memorable URLs
order: 5
involvement: creator
skills: Django, PostgreSQL, advanced SQL, rate limiting, user accounts, web development
link: http://kikl.co
github: liddiard/kikl
num_images: 4
---

Sometimes you just need to get a link from one place to another, and the most convenient method of transport is your memory. Links like `http://bit.ly/1loNbfX/` are short, but they're very impractical to remember.

Instead of random number/letter links, kikl.co gives you fun and easy-to-remember URLs like `kikl.co/fat-walrus`, perfect for remembering, sharing by word of mouth, and typing easily.

Links are automatically generated and last for an hour (though you can add more time if you log in). This way, kikl.co can keep reusing really short and memorable URLs without tying `fat-walrus` to your page for eternity.

The app contains some fun SQL queries [like this one](https://github.com/liddiard/kikl/blob/36b6215b6813fcebe070c1f1e952c4a570950354/shortener/views.py#L183) to efficiently select random words while maintaining unique adjective-noun combinations for active links.