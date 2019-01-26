---
layout: page
title: Learning Paths
description: Influencing by Example!
background: '/img/bg-about.jpg'
---
This is my humble attempt to influence you to keep learning. We can achieve amazing things with little planning and little actions.

Here is my personal list of things I want to learn and I'm interest of. You will find Learning Paths for certifications and other subjects, collection of links, books etc... Wherever I find interest and adds value to myself.

<ul class="list-unstyled">
{% for post in site.categories.learning %}

    <li>
    {% if post.status == 'done' %}
    {{ site.icons_done }}
    {% endif %}
    {% if post.status == 'studying' %}
    {{ site.icons_doing }}
    {% endif %}
    {% if post.status == null %}
    {{ site.icons_done }}
    {% endif %}

    <a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></li>

{% endfor %}
</ul>