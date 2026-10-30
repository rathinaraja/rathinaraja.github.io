---
layout: page
permalink: /publications/
title: publications
description:
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>

<style>
/* A compact, uncluttered publication-search field. */
.publications-search,.bibsearch-form,.bib-search,.bibsearch,.search-bar{max-width:430px!important}
#bibsearch,.bibsearch-form input,.bib-search input,input#bibsearch{max-width:430px!important;width:100%;box-sizing:border-box;border-radius:9px;padding:.5rem .8rem}
.publications{margin-top:1.25rem}
/* Keep page titles in navigation, not repeated above the content. */
.post-header .post-title,.post-header h1,.page-header .page-title{display:none!important}
</style>
