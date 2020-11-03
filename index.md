---
layout: default
title: "Strona główna"
---
## {{page.title}}

#### Zadania domowe:

{% for post in site.pages %}
    {% if post.url contains "assets" or post.title contains "Index" %}  
    {% else %}
        {% raw %}
            <div>
              <a href="{{post.url | absolute_url}}">{{ post.title }}</a>
            </div>
        {% endraw %}
    {% endif %}
{% endfor %}
