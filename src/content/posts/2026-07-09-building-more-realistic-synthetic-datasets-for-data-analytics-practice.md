---
title: Building More Realistic Synthetic Datasets for Data Analytics Practice
published: 2026-07-09T08:00
updated: 2026-07-09T10:40
draft: true
description: Framework to create a realistic synthetic dataset
image: /assets/images/pasted-image-1783568863550.png
tags:
  - Project
  - Portfolio
  - Python
  - Kaggle
category: Project
lang: English
pinned: false
author: M. Ibnu Rasyad
sourceLink: https://github.com/ibrasyad/creanu-labs
licenseName: CC BY 4.0
licenseUrl: https://creativecommons.org/licenses/by/4.0/
encrypted: false
password: ''
---

# Building More Realistic Synthetic Datasets for Data Analytics Practice

One thing I've learned after several years working in data analytics education is that finding a good dataset is surprisingly difficult.

Students are often asked to complete an analytics project: choose a business problem, analyze the data, build dashboards, and present actionable insights. It's a fantastic exercise because it closely resembles what analysts do in real organizations.

The challenge is finding data that supports that experience.

Many students end up using the same well-known public datasets from platforms like Kaggle or Maven Analytics. Those datasets are excellent learning resources, but after seeing hundreds of student projects, it's common to encounter the same analyses repeatedly.

Another option is using generated datasets. These are useful for practicing SQL, data cleaning, or dashboard creation, but many generators simply produce statistically random values. While technically valid, they often lack the underlying business behaviors that make analysis meaningful.

Real businesses aren't random.

Sales fluctuate with seasons. Customers return at different intervals. Promotions influence purchasing decisions. Some products naturally sell together, while others rarely appear in the same basket. New customers join over time, while existing ones become loyal or stop purchasing altogether.

These patterns are where many interesting analytical questions come from.

## The Idea

Rather than creating a single dataset, I decided to build a dataset generation framework.

The goal is to generate synthetic business datasets that follow configurable business rules instead of relying solely on random number generation.

Instead of asking, "What should this value be?", the framework asks questions like:

- How often should customers return?
- Which products are frequently purchased together?
- How much should weekends affect sales?
- What happens during promotional periods?
- How does customer acquisition change over time?

By combining configurable business rules with controlled randomness, each generated dataset can be different while still exhibiting realistic business behavior.

## The First Dataset

The first dataset generated using this framework is a simulated grocery store.

It currently includes multiple related tables covering different aspects of a retail business:

- Product catalog
- Customer data
- Transactions
- Transaction line items
- Customer funnel and activity data

The intention is to provide enough complexity for learners to practice:

- SQL
- Dashboard development
- Exploratory data analysis
- Customer segmentation
- Basket analysis
- ETL pipelines
- Business intelligence projects

Because every record is synthetic, there are no privacy concerns while still maintaining realistic relationships between the tables.

## Still a Work in Progress

This project is far from finished.

There are many aspects I'd like to improve, including:

- More sophisticated customer behavior models
- Better seasonality and promotional effects
- Additional retail scenarios
- Improved code structure and configuration

Ultimately, I'd like the framework to support multiple business domains, not just grocery stores, but restaurants, e-commerce, healthcare, finance, and other industries.

## Why I'm Sharing It Now

I believe projects improve much faster when they're shared early.

The grocery dataset is already useful for learning and portfolio projects, but I'm equally interested in feedback on the framework itself. If you've worked with synthetic datasets, teach analytics, or have ideas for making the generated data more realistic, I'd love to hear your thoughts.

This is only the beginning, and I hope to continue expanding both the framework and the datasets it can generate over time.
