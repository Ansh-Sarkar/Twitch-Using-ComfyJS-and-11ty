---
title: "Hello World"
layout: "base.njk"
templateEngineOverride: njk , md
---

This is a Home Page

# From the Blog

<br/>

{%- for post in collections.posts | randomPost -%}
    <a href = "{{ post.url }}">{{ post.data.title }}</a>
{%- endfor -%}

<br/>

## Articles
<ul>
{%- for article in collections.articles -%}
    <li>
        <a href = "{{ article.url }}">{{ article.data.title }}</a>
    </li>
{%- endfor -%}
</ul>