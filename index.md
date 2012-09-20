---
layout: page
title: nezuvian::dev_blog
---
{% include JB/setup %}


{% for post in site.posts %}
<div class="posts row">
    <div class="two columns">
      <span>{{ post.date | date_to_string }}</span> &raquo; 
    </div>
    <div class="ten columns">
      <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
      <div class="twelve.columns">
        {{ post.content }}
      </div>
    </div>
</div>
{% endfor %}  