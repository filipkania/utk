---
layout: default
title: "Strona główna"
---
## {{page.title}}

#### Zadania domowe:

{% for post in site.pages %}
    {% if post.url contains "assets" or post.title contains "Strona główna" %}  
    {% else %}
        {% include renderPost.html date=post.date title=post.title url=post.url}
    {% endif %}
{% endfor %}
