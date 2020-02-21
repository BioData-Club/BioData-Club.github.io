---
title: Lesson Material
layout: splash
---

# Events/Workshops by Date

{% assign sorted_events = site.events | sort: 'date' | reverse %}
{% capture now_moment %}{{ "today" | date: '%s' | plus: 0 }}{% endcapture %}

{% for event in sorted_events %}
    {% capture date %}{{ event.date | date: '%s' | plus: 0 }}{% endcapture %}
     {% if date < now_moment and event.event_type == "workshop" %}
      {% include past_events.html %}
      {% endif %}
{% endfor %}

