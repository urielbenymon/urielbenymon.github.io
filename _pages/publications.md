---
layout: page
permalink: /publications/
title: Publications
description: ""
nav: true
nav_order: 1
---
<style>
.post-header h1.post-title {
  color: var(--global-theme-color);
}
</style>

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% comment %}
Enable publication search when bibliography entries are added:
{% include bib_search.liquid %}
{% endcomment %}

<div class="publications">

{% bibliography %}

</div>
