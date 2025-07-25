
---
layout: page
title: The Work
permalink: /work/
---

<div class="container">
	<div class="work-grid">
	{% assign work_posts = site.posts | where: "tags", "work" %}
	{% if work_posts.size > 0 %}
		{% for post in work_posts %}
		<div class="work-card">
			{% if post.image %}
			<div class="work-card__image" style="background-image: url({{site.baseurl}}/images/{{post.image}})"></div>
			{% endif %}
			<div class="work-card__content">
				<h3 class="work-card__title">
					<a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
				</h3>
				<p class="work-card__date">{{ post.date | date: "%B %d, %Y" }}</p>
				<p class="work-card__excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
				<a href="{{ post.url | prepend: site.baseurl }}" class="work-card__link">Read more</a>
			</div>
		</div>
		{% endfor %}
	{% else %}
		<p>No work updates yet.</p>
	{% endif %}
	</div>
</div>
