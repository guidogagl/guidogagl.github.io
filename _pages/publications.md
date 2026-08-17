---
layout: page
permalink: /publications/
title: publications
description: Grouped by type, newest first within each group.
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

Full record also on [Google Scholar](https://scholar.google.com/citations?user=cHr99doAAAAJ) and
[ORCID](https://orcid.org/0000-0003-2020-6439). Names in **bold** are mine.

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="bibliography">Preprints &amp; Under Review</h2>
{% bibliography --query @unpublished %}

<h2 class="bibliography">Journal Articles</h2>
{% bibliography --query @article %}

<h2 class="bibliography">Peer-Reviewed Conference Papers</h2>
{% bibliography --query @inproceedings %}

<h2 class="bibliography">Conference Abstracts</h2>
{% bibliography --query @misc %}

</div>
