---
layout: page
title: Public Talks
permalink: talks/
---

## Podcasts

{% assign talktitles = site.data.podcasts | group_by:"title" %}
{% for title in talktitles %}
{% include cv/podcasts.html talk=title %}
{% endfor %}

## Talks

{% assign talktitles = site.data.talks | group_by:"title" %}
{% for title in talktitles %}
{% include cv/talk.html talk=title %}
{% endfor %}

## Guest Lectures

{% assign talktitles = site.data.university_lectures | group_by:"title" %}
{% for title in talktitles %}
{% include cv/university_lectures.html talk=title %}
{% endfor %}