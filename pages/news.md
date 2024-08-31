---
layout: page
title: News
permalink: /news/
pagination:
  enabled: true
  permalink: "/news/page:num/"
  sort_field: "date"
  sort_reverse: true
---


<div id="posts">
    {% for post in paginator.posts %}
        <div class="post-teaser">
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
        </div>
    {% endfor %}
</div>

<div class="pagination">
    {% if paginator.previous_page %}
        <a class="previous" href="{{ paginator.previous_page_path | relative_url }}">Previous</a>
    {% endif %}

    {% if paginator.next_page %}
        <a class="next" href="{{ paginator.next_page_path | relative_url }}">Next</a>
    {% endif %}
</div>
