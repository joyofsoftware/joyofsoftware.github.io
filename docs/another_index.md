**joy of software**

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
	  <small>{{ post.date | date: "%B %Y" }}</small>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>