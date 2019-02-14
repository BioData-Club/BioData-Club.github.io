## Adding Your Own Events to The BioData Site

Adding your events is a matter of doing the following:

1. Create a new markdown file in the `_events` with the following format:

`YYYY-MM-DD-My_Event.md`

2. Add your event information by filling out the YAML front matter:

Here's an example of filling out the info for the event. Note the `---` before and after all the information fields is required.

```
---
title: "First Event"
date: 2020-01-01
time: "2 PM"
location: "123 Fake Street"
description: "Here's an example of an event that can go on your calendar. When in doubt, put things in quotes."
link: "http://github.com/"
---
```
