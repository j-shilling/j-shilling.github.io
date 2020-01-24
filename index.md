---
layout: page
---

{% include JB/setup %}

<ul>
  {% for post in site.posts limit:10 %}
    <li style="list-style-type: none;">
	  <h3>
	    <a style="text-decoration: none;color: black;" href="{{ BASE_PATH }}{{ post.url }}">
		  {{ post.title }}
		</a>
	  </h3>
      <div style="padding: 0 0 10px 0">{{ post.date | date_to_string }}</div>
	  <p style="color: black; font-style: italic">
	    {{ post.content | strip_html | truncatewords:100 }}
		<a
		  style="text-decoration: none; color: black; font-style: normal"
		  href="{{ BASE_PATH }}{{ post.url }}">
		  read more
	    </a>
	  </p>
    </li>
  {% endfor %}
</ul>
