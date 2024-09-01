---
layout: page
title: News
pagination:
  enabled: true
---


<div id="posts">
    {% for post in site.posts %}
        <div class="post-teaser">
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
        </div>
    {% endfor %}
</div>

<div class="pagination">
    {% if site.previous_page %}
        <a class="previous" href="{{ site.previous_page_path | relative_url }}">Previous</a>
    {% endif %}

    {% if site.next_page %}
        <a class="next" href="{{ site.next_page_path | relative_url }}">Next</a>
    {% endif %}
</div>
