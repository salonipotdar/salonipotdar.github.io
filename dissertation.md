---
layout: page
title: Visual Learning with Minimal Human Supervision
permalink: dissertation/
redirect_from: defense/
jsarr:
- js/scripts.js
---

<span class="dissertation-subtitle">

<span>

{% include dissertation/document.html %}

{% for talk in site.data.dissertation.talks %}
{% if talk.key == "award" %}
{% include dissertation/talk.html talk=talk %}
{% endif %}
{% endfor %}

**Committee**

- Martial Hebert - *Advisor, CMU, Robotics*
- Abhinav Gupta - *Co-Advisor, CMU, Robotics*
- Deva Ramanan - *CMU, Robotics*
- Alyosha Efros - *UC Berkeley, EECS*
- Andrew Zisserman - *University of Oxford*

{% for talk in site.data.dissertation.talks %}
{% if talk.key == "defense" %}
{% include dissertation/talk.html talk=talk %}
{% endif %}
{% endfor %}
