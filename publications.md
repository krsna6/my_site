---
layout: page
title: Publications
permalink: /publications/
toc: true
---

You can find a full list of my publications on my [Google Scholar](https://scholar.google.com/citations?hl=en&user=rvBdf6wAAAAJ&view_op=list_works&sortby=pubdate) profile. I have highlighted a few relevant papers here.

## Patents

{% bibliography -f papers -q @*[pubtype=patent]* %}

## Journal Publications

{% bibliography -f papers --query @*[pubtype=journal]*%}

## Preprint

{% bibliography -f papers --query @*[pubtype=arxiv]*%}

## Conference Publications

{% bibliography -f papers --query @*[pubtype=conf]*%}



<details><summary><b>Older publications</b></summary>
{% bibliography --file uvce %}
</details>

