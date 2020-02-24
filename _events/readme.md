## Adding Your Own Events to The BioData Site

Adding your events is a matter of doing the following:

1. Create a new markdown file in the `_events` folder with the following format:

`YYYY-MM-DD-My_Event_Name.md`

2. Add your event information by filling out the YAML front matter:

Here's an example of filling out the info for the event. Note the `---` before and after all the information fields is required.

```
---
title: "The Magic of Markdown"
date: 2018-10-05 # Make sure the date is in this format
time: "4:00 - 5:30 PM" #Time is Human readable
event_type: "" # either "workshop", "discussion", or "social" 
presenters: ["Blah Blah", "Blah 2"] # put multiple presenters in brackets, separated by comma
keywords: ["Visualization", "Data"] #These should come from taxonomy
location: "Choose a location that facilitates discussion and co-learning.  This means thinking about not only the technology a space provides, but also the face-to-face interaction it will allow" #Try to keep this entry on a single line
location_url: "If you have a link to an interactive map, please add it here"
description: "Create a welcoming description of your event.  Include a description of the learning outcomes and any prework (such as software downloads) attendees should accomplish." 
link: "post a link to the RSVP survey"
# The following should be filled out post workshop - please uncomment them when you do
#slides: ""  #url for presenter slides
#code: "" #url for code repository
#recording: "" #recording if available
#app: "" #Code environment (such as rstudio.cloud or mybinder.org) or web app
---
```

3. After the workshop and the recordings are available, fill out the `slides`,`code`, `recording`, and `app` fields as necessary. The links and event info will then appear on the [materials](http://biodata-club.github.io/materiasl/) page.

## Some tips

Be careful that you keep the space between the field name and the field value. That is, make sure you've typed `code: http://github.com/` instead of `code:http://github.com`.

If you have double quotes (`"`) in your entry, make sure to escape them `\"` because the parser will get confused.
