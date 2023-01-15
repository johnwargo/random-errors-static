---
layout: page
title: Category List
permalink: /catlist/
---

Access all of the articles for a particular category by picking an item from the list below:

{% assign categories = site.categories | sort %}
<ul>
    {% for category in categories %}
        <li>
           <a href="/category/{{ category | first | slugify }}">{{ category[0] | replace:'-', ' ' }} ({{ category | last | size }})</a>
        </li>
    {% endfor %}
</ul>
