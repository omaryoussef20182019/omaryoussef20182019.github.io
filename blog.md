---
layout: default
title: "All Projects and Detailed Case Studies"
permalink: /blog/
---

<main class="container mb-5">
  <section id="full-blog-list" class="mb-5 theme-section">
    <h1 class="theme-heading mb-4">All Projects and Detailed Case Studies</h1>
    <div class="list-group">
      {% for post in site.posts %}
        <a href="{{ post.url }}" class="list-group-item list-group-item-action theme-list-item">
          <div class="d-flex w-100 justify-content-between">
            <h5 class="mb-1">{{ post.title }}</h5>
            <small>{{ post.date | date: "%Y-%m-%d" }}</small>
          </div>
          <p class="mb-1">{{ post.excerpt | strip_html | truncate: 150 }}</p>
        </a>
      {% endfor %}
    </div>
  </section>
</main>
