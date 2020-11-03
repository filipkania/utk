---
layout: default
title: "Index page"
---
## {{page.title}}

#### Zadania domowe:

{% for post in site.pages %}
    {% if post.url contains "assets" or post.title contains "Index" %}  
    {% else %}
        <div>
          <a href="{{post.url | absolute_url}}">{{ post.title }}</a>
        </div>
    {% endif %}
{% endfor %}
