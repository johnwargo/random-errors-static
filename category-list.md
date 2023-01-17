---
layout: page
title: Categories
permalink: /category-list/
---

Access all of the articles for a particular category by selecting an item from the list below:

<ul>
    {% for cat in site.data.categories %}
        <li>
           <h4><a href="/categories/{{ cat.category | slugify }}">{{ cat.category | replace:'-', ' ' }} ({{cat.count}} Posts)</a></h4>
        </li>
    {% endfor %}
</ul>


<!-- {% assign categories = site.categories | sort %}
<ul>
    {% for category in categories %}
        <li>
           <a href="/categories/{{ category | first | slugify }}">{{ category[0] | replace:'-', ' ' }} ({{ category | last | size }})</a>
        </li>
    {% endfor %}
</ul> -->
