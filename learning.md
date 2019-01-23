---
layout: page
title: Learning Paths
description: Influencing by Example!
background: '/img/bg-about.jpg'
---
This is my humble attempt to influence you to keep learning... at your pace... but keep learning.

We can achive amazing things with little planning and little actions.

This is my personal list of things I want to learn, I'm learning and how I'm learning it. Also, I may share links about subjects I love, such Neuroscience, Productivity, Behaviour... and the list goes on.

Enjoy and have fun, the last is really important.

<ul class="list-unstyled">
{% for post in site.categories.learning %}

    <li>
    {% if post.status == 'done' %}
    <span class="text-success fa fa-check-circle"></span>&nbsp;
    {% endif %}
    {% if post.status == 'studying' %}
    <span class="text-primary fa fa-hand-spock-o"></span>&nbsp;
    {% endif %}
    {% if post.status == null %}
    <span class="fa fa-genderless"></span>&nbsp;
    {% endif %}

    <a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></li>

{% endfor %}
</ul>