## Adding Your Own Events to The BioData Site

Adding your events is a matter of doing the following:

1. Create a new markdown file in the `_events` with the following format:

`YYYY-MM-DD-My_Event.md`

2. Add your event information by filling out the YAML front matter:

Here's an example of filling out the info for the event. Note the `---` before and after all the information fields is required.

```
---
title: "The Magic of Markdown"
date: 2018-10-05
time: "4:00 - 5:30 PM"
event_type: # either "workshop", "discussion", "hacky hour"
presenters: ["Blah Blah", "Blah 2"]
keyworkds: ["Visualization", "Data"]
location: "Choose a location that facilitates discussion and co-learning.  This means thinking about not only the technology a space provides, but also the face-to-face interaction it will allow"
location_url: "If you have a link to an interactive map, please add it here"
description: "Create a welcoming description of your event.  Include a description of the learning outcomes and any prework (such as software downloads) attendees should accomplish."
link: "post a link to the RSVP survey"
# The following should be filled out post workshop - please uncomment them
#slides: #url for presenter slides
#code: #url for code repository
#recording: #recording if available
#app: #Code environment (such as rstudio.cloud or mybinder.org) or web app
---
```
