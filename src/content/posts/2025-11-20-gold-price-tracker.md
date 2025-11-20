---
title: Gold Price Tracker
published: 2025-11-21T08:00:00.000+07:00
draft: true
description: A project which mainly to help gain insight in gold prices for
  personal investment. Data is scrapped from Galeri24, which I understand is not
  the exact price, but should be enough as an overall picture.
image: /assets/images/screenshot-2025-11-20-145215.png
tags:
  - Portfolio
  - Project
  - Data-Scraping
  - Automation
  - ETL
category: Project
lang: ""
pinned: false
author: M. Ibnu Rasyad
sourceLink: ""
licenseName: CC BY 4.0
licenseUrl: https://creativecommons.org/licenses/by/4.0/
encrypted: false
password: ""
---
# What is this? And Why?

This is a data scrapping project to get the price of gold (some brands and weights) everyday. The data is collected from [Galeri24 website](https://galeri24.co.id/harga-emas). In short, it will automatically extract the data, transform it, and load into our "database". I know, I know, it's a terrible joke that I mention "database" but it's stored on Google Sheets. But it was easy to test, and I wanted to see how long until I see some errors. But yeah, next plan is to store this into BigQuery maybe, but that will be for much later.

Well, this was started from my wife. We were wondering when would be the best time to buy gold. While I could easily look up what other people have built to track price of gold, I just thought "I could just do it myself, couldn't I?". 

Well, so here we are, a dataset that will continuously track the price of gold daily. This is not perfect, nor this is accurate. The simplest I could do for now is to scrap the [Galeri24 website](https://galeri24.co.id/harga-emas) and get the price from there. I'm not quite sure when they change the price on their website, but I just take a guess and choose 12 PM.
You can check the [Result Data Here](https://docs.google.com/spreadsheets/d/1BCR_IbhFWSIR1faz9UJXItLHSOicaSWofymvDCSuq_E/edit?usp=sharing). It's shared publicly, and you can use it if you want. I'd be happy if you give credits, but eh, it's nothing much, I just need reason to do fun projects like this.

# What's next?

For the data collection part, this should be it for now. But I do have some plan for what I might do next:

1. As mentioned, when Google Sheets can't handle it anymore, I'll need to move it to BigQuery, cause it's free there and I can easily connect it to Looker Studio.
2. And as I *just* mentioned, I want to make a dashboard for it, making it easier to access and get insight to for other people, and I'm 90% sure I'll go with Looker Studio. The reason is very simple, it's cheap, easy to use, and anyone can access it.

# Thanks to

Thanks to Galeri24 for making their pricing data publicly available. Based on their robots.txt, this scraping activity is permitted. However, if this project causes any issues or violates any policy, please contact me.
