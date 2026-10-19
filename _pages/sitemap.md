---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

A list of all the pages and projects found on the site. For you robots out there, there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Pages</h2>
<div class="list__item">
  <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
    <h2 class="archive__item-title" itemprop="headline">
      <a href="{{ base_path }}/" rel="permalink">Home (EN)</a>
    </h2>
  </article>
</div>
<div class="list__item">
  <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
    <h2 class="archive__item-title" itemprop="headline">
      <a href="{{ base_path }}/fr/" rel="permalink">Accueil (FR)</a>
    </h2>
  </article>
</div>
{% for post in site.pages %}
  {% if post.title and post.title != "" and post.sitemap != false and post.url != "/sitemap/" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% if site.posts.size > 0 %}
<h2>Posts</h2>
{% for post in site.posts %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
{% unless collection.output == false or collection.label == "posts" or collection.docs.size == 0 %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
  <h2>{% if label == "portfolio" %}Research &amp; Projects{% else %}{{ label | capitalize }}{% endif %}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs reversed %}
  {% unless collection.output == false or collection.label == "posts" %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endfor %}
