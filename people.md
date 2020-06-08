---
layout: page
title: People
comments: false
permalink: /people/
---

<head>
<style> 
img {
}
  .left {
    float: left;
    padding: 0 10px 0 0;}
  }
</style>
</head>

<div id="people">
{% for person in site.data.people %}
<h3 id="{{ username }}">{{ person[1].name }}</h3>
  <img src="http://csu-signal.github.io/assets/images/krishnaswamy.png" width="150" height="150">
  <p align="left">
    {{ person[1].bio }}<br/>
    {% if person[1].location != null %}
      <strong>Location:</strong> {{ person[1].location }}<br/>
    {% endif %}
    {% if person[1].url_full != null %}
      <strong>Website:</strong> <a href="{{ person[1].url_full }}">{{ person[1].url_full }}</a>
    {% endif %}
  </p>
<hr>
{% endfor %}
</div>
