---
layout: post
title: "Knowledge Graph and Graph Learning(KGGL Group)"
subtitle: "Knowledge Graph and Graph Learning group focuses on knowledge graphs and graph learning, sharing research and ideas."
tags: []
categories: [Groups]
comments: true
---
{{ content }} {% assign posts = paginator.posts | default: site.posts %}
{% assign group_coordinator_tag = "KGGL_C" %}
{% assign group_member_tag = "KGGL" %}

# Research Interests
This interest group focuses specifically on knowledge graphs and graph learning, aiming to explore these two fields and their intersection. A knowledge graph is a method of graphically representing knowledge that can help people understand complex information and relationships. Graph learning is a method of learning from graph data that can help us better understand data and relationships. In this group, we will discuss the latest research on knowledge graphs and graph learning, share practical experience, and exchange ideas with others interested in these two fields. Members are encouraged to ask questions, engage in discussions, and learn more about these technologies through collaborative projects.

# Coordinator
<ul class="posts-list list-unstyled" role="list">
  {% for post in posts %}
  <!-- if post category is not Groups -->
  <!-- only show posts tags is exactly group_coordinator_tag -->
    {% if post.tags contains group_coordinator_tag and post.categories != "Groups"%}
  <li class="post-preview">
    <article>
      {%- capture thumbnail -%} {% if post.thumbnail-img %} {{
      post.thumbnail-img }} {% elsif post.cover-img %} {% if
      post.cover-img.first %} {{ post.cover-img[0].first.first }} {% else %} {{
      post.cover-img }} {% endif %} {% else %} {% endif %} {% endcapture %} {%
      assign thumbnail=thumbnail | strip %} {% if site.feed_show_excerpt ==
      false %} {% if thumbnail != "" %}
      <div class="post-image post-image-normal">
        <a href="{{ post.url | absolute_url }}" aria-label="Thumbnail">
          <img src="{{ thumbnail | absolute_url }}" alt="Post thumbnail" />
        </a>
      </div>
      {% endif %} {% endif %}
      <a href="{{ post.url | absolute_url }}">
        <h2 class="post-title">{{ post.title | strip_html }}</h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">{{ post.subtitle | strip_html }}</h3>
        {% endif %}
      </a>
      <p class="post-meta">
        {% assign date_format = site.date_format | default: "%B %-d, %Y" %}
        Posted on {{ post.date | date: date_format }}
      </p>
      {% if thumbnail != "" %}
      <div class="post-image post-image-small">
        <a href="{{ post.url | absolute_url }}" aria-label="Thumbnail">
          <img src="{{ thumbnail | absolute_url }}" alt="Post thumbnail" />
        </a>
      </div>
      {% endif %} {% unless site.feed_show_excerpt == false %} {% if thumbnail
      != "" %}
      <div class="post-image post-image-short">
        <a href="{{ post.url | absolute_url }}" aria-label="Thumbnail">
          <img src="{{ thumbnail | absolute_url }}" alt="Post thumbnail" />
        </a>
      </div>
      {% endif %}
      <div class="post-entry">
        {% assign excerpt_length = site.excerpt_length | default: 50 %} {{
        post.excerpt | strip_html | truncatewords: excerpt_length }} {% assign
        excerpt_word_count = post.excerpt | number_of_words %} {% if
        post.content != post.excerpt or excerpt_word_count > excerpt_length %}
        <a href="{{ post.url | absolute_url }}" class="post-read-more"
          >[Read&nbsp;More]</a
        >
        {% endif %}
      </div>
      {% endunless %} {% if site.feed_show_tags != false and post.tags.size > 0
      %}
      <div class="blog-tags">
        <span>Tags:</span>
        <!-- role="list" needed so that `list-style: none` in Safari doesn't remove the list semantics -->
        <ul class="d-inline list-inline" role="list">
          {% for tag in post.tags %}
          <li class="list-inline-item">
            <a href="{{ '/tags' | absolute_url }}#{{- tag -}}">{{- tag -}}</a>
          </li>
          {% endfor %}
        </ul>
      </div>
      {% endif %}
    </article>
  </li>
  {% endif %} {% endfor %}
</ul>
# Memebers
<ul class="posts-list list-unstyled" role="list">
  {% for post in posts %}
  <!-- only show posts tags is exactly group_member_tag -->
    {% if post.tags contains group_member_tag and post.categories != "Groups"%}
  <li class="post-preview">
    <article>
      {%- capture thumbnail -%} {% if post.thumbnail-img %} {{
      post.thumbnail-img }} {% elsif post.cover-img %} {% if
      post.cover-img.first %} {{ post.cover-img[0].first.first }} {% else %} {{
      post.cover-img }} {% endif %} {% else %} {% endif %} {% endcapture %} {%
      assign thumbnail=thumbnail | strip %} {% if site.feed_show_excerpt ==
      false %} {% if thumbnail != "" %}
      <div class="post-image post-image-normal">
        <a href="{{ post.url | absolute_url }}" aria-label="Thumbnail">
          <img src="{{ thumbnail | absolute_url }}" alt="Post thumbnail" />
        </a>
      </div>
      {% endif %} {% endif %}
      <a href="{{ post.url | absolute_url }}">
        <h2 class="post-title">{{ post.title | strip_html }}</h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">{{ post.subtitle | strip_html }}</h3>
        {% endif %}
      </a>
      <p class="post-meta">
        {% assign date_format = site.date_format | default: "%B %-d, %Y" %}
        Posted on {{ post.date | date: date_format }}
      </p>
      {% if thumbnail != "" %}
      <div class="post-image post-image-small">
        <a href="{{ post.url | absolute_url }}" aria-label="Thumbnail">
          <img src="{{ thumbnail | absolute_url }}" alt="Post thumbnail" />
        </a>
      </div>
      {% endif %} {% unless site.feed_show_excerpt == false %} {% if thumbnail
      != "" %}
      <div class="post-image post-image-short">
        <a href="{{ post.url | absolute_url }}" aria-label="Thumbnail">
          <img src="{{ thumbnail | absolute_url }}" alt="Post thumbnail" />
        </a>
      </div>
      {% endif %}
      <div class="post-entry">
        {% assign excerpt_length = site.excerpt_length | default: 50 %} {{
        post.excerpt | strip_html | truncatewords: excerpt_length }} {% assign
        excerpt_word_count = post.excerpt | number_of_words %} {% if
        post.content != post.excerpt or excerpt_word_count > excerpt_length %}
        <a href="{{ post.url | absolute_url }}" class="post-read-more"
          >[Read&nbsp;More]</a
        >
        {% endif %}
      </div>
      {% endunless %} {% if site.feed_show_tags != false and post.tags.size > 0
      %}
      <div class="blog-tags">
        <span>Tags:</span>
        <!-- role="list" needed so that `list-style: none` in Safari doesn't remove the list semantics -->
        <ul class="d-inline list-inline" role="list">
          {% for tag in post.tags %}
          <li class="list-inline-item">
            <a href="{{ '/tags' | absolute_url }}#{{- tag -}}">{{- tag -}}</a>
          </li>
          {% endfor %}
        </ul>
      </div>
      {% endif %}
    </article>
  </li>
  {% endif %} {% endfor %}
</ul>