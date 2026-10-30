---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>

<style>
/* A compact, uncluttered publication-search field. */
.bibsearch-form,.bib-search,.bibsearch,.search-bar,.bibsearch-form input,.bibsearch input {max-width:360px!important;}
#bibsearch,.bibsearch-form input,.bib-search input,input#bibsearch{max-width:430px!important;width:100%;box-sizing:border-box;border-radius:9px;padding:.5rem .8rem}
.publications{margin-top:1.25rem}
/* Keep page titles in navigation, not repeated above the content. */
.post-header .post-title,.post-header h1,.page-header .page-title{display:none!important}
.publications #bibsearch,.publications input[type="search"],input#bibsearch,input#bib-search,input#bibsearch-input,.bibsearch-form input[type="text"],.bibsearch-form input[type="search"]{width:100%!important;max-width:360px!important;box-sizing:border-box!important;padding:.45rem .75rem!important;min-height:35px!important;font-size:.9rem!important} 

/* Hide only the automatic duplicate page heading, preserving all content headings. */
.post-header,.page-header{display:none!important}
</style>
