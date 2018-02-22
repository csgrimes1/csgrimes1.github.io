---
layout: default
title: Home
---
This is where a normal person would describe the site and
add biographical information. I plead the fifth.

Here's what I wrote about:

<table><tbody>
{% for item in site.posts %}
<tr>
    <td>{{ item.date | date_to_string }}</td>
    <td><a href="{{ item.url | absolute_url }}">{{ item.title }}</a></td>
    <td>{{ item.description }}</td>
</tr>
{% endfor %}
</tbody></table>

The best gif I've ever seen:

![Boomerang Bottle!](https://i.imgur.com/f5u2RL5.gif)
