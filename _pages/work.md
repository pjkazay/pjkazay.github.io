
---
layout: page
title: The Work
permalink: /work/
---

<div class="container">
	<div class="row">
	{% assign work_posts = site.posts | where: "tags", "work" %}
	{% if work_posts.size > 0 %}
		{% for post in work_posts %}
			{% include article-content.html %}
		{% endfor %}
	{% else %}
		<p>No work updates yet.</p>
	{% endif %}
	</div>
</div>
