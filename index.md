---
layout: page
title: nezuvian::dev_blog
---
{% include JB/setup %}


{% for post in site.posts %}
<div class="posts row">
    <div class="date-sidebar two columns">
      <span>{{ post.date | date_to_string }}</span>
    </div>
    <div class="text-body ten columns">
      <h2 class="post-title"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>      
      <div class="post-body twelve columns">        
        {{ post.content | replace:"more start -->",'' | replace:"<!-- more end",'' }}
        <a href="{{ BASE_PATH }}{{ post.url }}">Read more &raquo;</a>
      </div>
      {% assign tags_list = post.tags %}
      {% include JB/tags_list %}
    </div>
</div>
{% endfor %}  