---
layout: archive
title: "Sitemap"
title_pt: "Mapa do Site"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

<div class="lang-en">
<p>Index of all pages, R&amp;D portfolio items, publications, and talks available on this website. An <a href="{{ base_path }}/sitemap.xml">XML sitemap</a> is also generated.</p>
</div>
<div class="lang-pt">
<p>Índice completo das páginas, projetos de P&amp;D, publicações e apresentações disponíveis neste site. Também há uma versão em <a href="{{ base_path }}/sitemap.xml">sitemap XML</a>.</p>
</div>

<h2><span class="lang-en">Pages</span><span class="lang-pt">Páginas</span></h2>
{% for post in site.pages %}
  {% if post.sitemap != false and post.title %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% for collection in site.collections %}
  {% unless collection.output == false or collection.label == "posts" %}
    <h2>{{ collection.label | capitalize }}</h2>
    {% for post in collection.docs reversed %}
      {% include archive-single.html %}
    {% endfor %}
  {% endunless %}
{% endfor %}

