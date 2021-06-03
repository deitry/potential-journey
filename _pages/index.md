---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 3em 1em; background: #35373f; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration.
</p>

<h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2>
<ul class="post-list">
  {%- for post in site.posts -%}
  <li>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    <span class="post-meta">{{ post.date | date: date_format }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
  {%- endfor -%}
</ul>

This digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll). If you need any help, my [DMs are open on Twitter (@vaillancourtmax)](https://twitter.com/vaillancourtmax). Say hi! 👋

If this template helps you in any way, [consider buying me a coffee](https://ko-fi.com/maximevaillancourt)! ☕️

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
