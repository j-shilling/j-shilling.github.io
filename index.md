---
layout: page
---

{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts limit:5 %}
    <li style="list-style-type: none;">
	  <h3>
	    <a style="text-decoration: none;color: black;" href="{{ BASE_PATH }}{{ post.url }}">
		  {{ post.title }}
		</a>
	  </h3>
      <span>{{ post.date | date_to_string }}</span>
	  <p>
	    {{ post.content | strip_html | truncatewords:100 }}
	  </p>
    </li>
  {% endfor %}
</ul>
