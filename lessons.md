---
title: Lesson Material
layout: splash
---

# Workshops

Here are past topics and workshops from BioData Club, sorted by Date they were given. If you want us to do another workshop, [please let us know](https://biodata-club.github.io/teaching/)!

{% assign sorted_events = site.events | sort: 'date' | reverse %}
{% capture now_moment %}{{ "today" | date: '%s' | plus: 0 }}{% endcapture %}

{% for event in sorted_events %}
    {% capture date %}{{ event.date | date: '%s' | plus: 0 }}{% endcapture %}
     {% if date < now_moment and event.event_type == "workshop" %}
      {% include past_events.html %}
      {% endif %}
{% endfor %}

## [ The Magic of Markdown](https://github.com/laderast/magic-of-markdown)

This workshop introduces you to Markdown, an easy to learn format to save written documents in. Once you have a document in Markdown, you can transform it into all sort of outputs: from webpages, slides, PDF documents, and even Reproducible Analysis. 

## [ Setting up a GitHub Page](https://github.com/BioData-Club/githubPagesTutorial)

Once you know Markdown, you can now setup your own personal GitHub Page, with your academic CV and other accomplishments! We cover how to personalize it and add posts in Markdown. 

## [ Git for Collaboration](https://github.com/probinso/introduction-git)

This is a workshop introducing you to Git and GitHub. Learn the basics of Git by sorting panels from Edward Gorey's *Gashlycrumb Tinies*. In order to host the talk, please refer to these [setup/management scripts](https://github.com/probinso/ABC).

# Educational Resources

## [R-Bootcamp](https://r-bootcamp.netlify.com)

This was a four part course that is free that introduces everyone to visualizing, data wrangling, and simple statistics with `tidyverse` packages.

# Discussion Topics

This is a list of discussion topics and talks hosted by BioData Club that we think have been successful and of interest to other BioData Club Groups

+ [Good Enough Practices For Scientific Computing](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) 
  
This is a paper by Greg Wilson that outlines how to improve your scientific software.

+ [How to Be a Modern Scientist](https://www.scribd.com/document/325829082/Modern-Scientist) 

We had a discussion about Jeff Leek's book *How to be a Modern Scientist* and what it means for students and postdocs today. 

+ [Take a Sad Plot and Make it Better: A Case Study with R and ggplot2](https://apreshill.github.io/ohsu-biodatavis/slides.html) 
  
Alison Presmanes Hill gave a talk for our visualization hacky hour about how she slowly revised and improved a figure. Very funny and very informative.

+ [Ten Simple rules for a Successful Cross-Disciplinary Collaboration](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004214)

We at BioData Club are cross-disciplinary by nature. What does it take to be a good cross-disciplinary collaborator?

# Events/Workshops by Date
