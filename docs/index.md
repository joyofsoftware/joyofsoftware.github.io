---
layout: default
permalink: /index.html
---
<p></p>
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
	  <small>{{ post.date | date: "%d %B %Y" }}</small>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>
<p></p>
