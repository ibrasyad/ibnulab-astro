---
title: Comment System in Static Website Like Hugo
published: 2025-07-04
updated: 2025-10-06
draft: false
description: My effort of adding comment section into my static website. It was a long and confusing journey, but thankfully with Cloudflare D1 database it can be done.
image: /assets/images/cover comment.png
tags:
  - Project
  - Comment
  - Cloudflare
  - D1
  - Hugo
category: Project
lang: ''
pinned: false
author: M. Ibnu Rasyad
sourceLink: ''
licenseName: CC BY 4.0
licenseUrl: https://creativecommons.org/licenses/by/4.0/
encrypted: false
password: ''
---
# Why do I do it?

The reason why I was trying to make this was to enable interaction, engagement with the audience (well, one can dream to have some interaction right??). But trying to implement a comment system in here wasn't easy, maybe not solely because it's a complicated thing, but mostly of how inexperienced I am at this. You see, there are a lot of alternative ready to be implemented, like discus, giscus, gitalk, and remark 42 (and many more), but I'm not particularly fond of not having control over my own data/content. That's also exactly why I build my website using Hugo and host it myself through cloudflare pages. "What if the website builder like wix or squarespace goes out of business?", "What would happen to my website?", those questions were in my head.

So I set out my research on this, since I started making this in December 2024. But since it's a hassle to host my own database for my comment section, I abandoned the project, UNTIL I heard about cloudflare D1 database recently. In short, I can have a simple table to store the comments in D1, and use cloudflare Workers to fetch and submit comments. Obviously I don't work "alone", with the help of ChatGPT, I managed to make this project finally a reality.

You can try it out in the comment section of this post, please try it!

Disclaimer though: I am not in any way proficient in any of this. I'm just a data analyst, I might know a bit about SQL and ETL process, but HTML and CSS is way out of my expertise. So while I have an idea, I mostly ask ChatGPT on how to do it and struggle through it. It might not be following best practices or anything like that, but I'm happy and proud of it, so I'll be sharing about it.

# What Made This Possible?

As mestioned, I used cloudlflare D1 and Workers to build this comment system. Let's talk about each one.

## What is Cloudflare D1 and Workers?

At least to my knowledge, most SQL database needs to be hosted somewhere and/or managed by someone to be accessed. But just hosting it alone is a hassle and to make it not a hassle you need to pay some subscription like supabase or very limited by the free plan. I mean, it can work, but still, as I said, I don't like not having control over my data. So this is where cloudflare D1 comes in.

Cloudflare D1 is a lightweight SQL database that runs close to the users — perfect for small projects or dynamic data on static sites. Think of it like SQLite, but hosted and managed by Cloudflare. And the free plan IMO is really generous. Check out their pricing here: [Cloudflare D1 Pricing](https://developers.cloudflare.com/d1/platform/pricing/).

But _someone_ still have to push and fetch the comment from my website to the database, that's where Cloudflare Workers comes in. Most of the time, if you want to run some backend code — like handling form submissions or reading from a database — you’d need a server. That usually means spinning up something like Node.js, hosting it somewhere like Vercel, Railway, or DigitalOcean, and managing deployments or scaling.

But for small projects (like mine), that’s **_a lot of work_** just to handle a few HTTP requests.

Cloudflare Workers let you write JavaScript (or TypeScript) that runs on the edge — super fast and globally distributed. Together with D1, you can make a powerful dynamic backend _without_ needing a traditional server or hosting setup. You can write a function to handle POST requests (like comment submissions), or GET requests (to show existing comments), without needing a full backend or server. Plus, the free tier is pretty generous. It’s perfect for personal sites, blogs, and tiny apps. [Cloudflare Workers Pricing](https://developers.cloudflare.com/workers/platform/pricing/)

In short, here's the summary:

- **D1** store comments in a table
- **Workers** handle requests for posting and fetching comments in table inside D1

## How they work together

Basically the flow is like this:

1. A visitor writes a comment on my site.
2. The comment is then sent to a Cloudflare Worker (a simple JS endpoint).
3. That Worker writes the comment to the D1 database.
4. Another Worker endpoint fetches comments from D1 and renders them on the page.

There are other things they do of course, like parsing, checking for bots or malicious intent. But that's the gist of it.

# Final thoughts

This was one of those projects that started just from curiosity like "can I even do this?" and ended up being a real learning experience. I had no idea how Cloudflare Workers or D1 worked before this, but just by asking questions, reading docs, and experimenting (with help from ChatGPT), I got something working. Is it perfect? No. But it's mine, my own, **_~~my precious~~_**, and it works! **_~~GOLLUM GOLLUM~~_**

If you're like me, someone without a traditional web dev background, I hope this shows that you can build useful things with the right tools and support. You don’t need to know everything from day one.

If you’re curious to try this setup yourself, feel free to comment and include your email so I can reach you out! Or simply email me through my email (ibnura96@gmail.com) or my [LinkedIn](https://www.linkedin.com/in/ibnu-rasyad/). I’d love to see more people building lightweight, fast, and self-owned web tools like this.

Thanks for reading! Let me kow what you think on the comment section below!

> Update: Since I'm moving to Astro, this might not be needed anymore. The learning process was fun, but I'll try to use existing open-source projects, what I have in mind is using Twikoo.
