---
layout: post
title:  "Github and Ongoing Developments"
date:   2022-09-07 11:00:00 +0200
categories: GEM development
---
First post on the GEM Open Data News website! It's hosted as part of the Github setup I'm working on and the purpose is to keep you updated on our open data initiatives, data management and systems development. I will try to post an update about once a month. 

  [Subscribe to the RSS feed](/feed.xml) to get new posts delivered to your inbox. [Here's a guide on how to subscribe to RSS in Outlook](https://support.microsoft.com/en-us/office/subscribe-to-an-rss-feed-73c6e717-7815-4594-98e5-81fa369e951c)
## Moving to Github
The idea with moving GEM on Github, is to have a better space for collaboration, shared code and documentation across participating institutions in GEM - both for GEM participants and for the public / users (documentation, open source tools and code examples for analysing data etc.).

I have started a structure of repositories on github:

- [public](https://github.com/GreenlandEcosystemMonitoring/public)
- [development-gemdataprocessing](https://github.com/GreenlandEcosystemMonitoring/development-gemdataprocessing)
- [participants-visualization](https://github.com/GreenlandEcosystemMonitoring/participants-visualization)
- [participants-docs](https://github.com/GreenlandEcosystemMonitoring/participants-docs)
- [data-and-development-docs](https://github.com/GreenlandEcosystemMonitoring/data-and-development-docs)

## Development Team / Collaborators
With aid of the significant amount of INTERACT funded hours available for development of GEM open data in 2022 + 2023, I have found two new collaborators at AU - Ecoscience. They assist me adhoc with discussing, designing and reviewing the tech infrastructure, development tools, new features and taking on smaller development tasks, and so far it's working out great! So we are now: [Jonas K. Rømer](https://github.com/orgs/GreenlandEcosystemMonitoring/people/JonasAU) with assistance of [Lars Dalby](https://github.com/orgs/GreenlandEcosystemMonitoring/people/LDalby) and [Kavi Askholm Mellerup](https://github.com/orgs/GreenlandEcosystemMonitoring/people/kaviecos)
## Visualization and aggregated data products.
We have begun exploring and designing how to visualize data better and present aggregated data products to users. [Vega-Lite](https://vega.github.io/vega-lite/) looks like a good candidate for describing visualizations at high level, and can easily be integrated in websites. Next steps will be creating example aggregations and visualizations / plot types of GEM open data, with help from the GEM participants who has deeper insight in the data. Here we can start out working with whatever language and scripts you may have already `(R, Python, Other?)`
## API 
For the visualizations and to work further with the FAIR data criteria, it is apparent that we need an API to access the GEM open data programatically. We will go for a REST based API following the [OpenAPI Specification](https://github.com/OAI/OpenAPI-Specification/). Keeping in mind that GEM users and downloads should be registered for statistics, we will implement a feature to issue API keys to registered users via the GEM open data website, so we can still control and keep track on the use of GEM open data.

We are working with an idea of two different types of API's:
1. Visualization / data exploration API (for accessing temporal subsets of data with high performance and possibility of aggregating data by a time unit - i.e. hour, day, month, and an aggregation function)
2. Bulk download API (for ordering a download of one or more datasets delivered as a zip file, similar to what you get as download on the https://data.g-e-m.dk website now).

## Central Metadata Management Tool and Data Delivery Freeze
As we notified the GEM participants on 2022-08-20, a freeze period for data delivery is in place until we have developed the new Central Metadata Management Tool.
We need the GEM database to be the only authoritative source when it comes to metadata on the datasets. The solution we are building, we will try to keep as similar to the previous as possible, aiming to only simplify the experience for participants delivering data while also standardizing everything a 100% so the automatic import processes can run without manual work and adjustments required.
