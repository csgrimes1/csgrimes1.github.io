---
layout: default
title: Home
---
This is where a normal person would describe the site and
add biographical information. I plead the fifth.

Here's what I wrote about:
{% for item in site.posts %}
| * **{{ item.date | date_to_string }}**|**[{{ item.title }}]({{ item.url | absolute_url }})**|{{ item.description }}|
{% endfor %}

The best gif I've ever seen:

![Boomerang Bottle!](https://i.imgur.com/f5u2RL5.gif)
