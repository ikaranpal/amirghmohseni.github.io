---
layout: post
title:  "Growth of Liquidity Providers"
summary: "Review LPs in Uniswap and Growth stats"
author: amir007
date: '2023-10-08 12:35:23 +0130'
category: ['uniswap','dune', 'liquidity provider']
tags: uniswap
thumbnail: /assets/img/posts/uniswap-growth-lp.png
keywords: Uniswap, Dune, Liquidity Providers, Review Uniswap LPs
usemathjax: false
permalink: /blog/uniswap-growth-lp/
---

## Adding Multiple Categories in Posts

<iframe src="https://dune.com/embeds/3119526/5205138" width="100%" height="400"></iframe>

To add categories in blog posts all you have to do is add a **category** key with category values in frontmatter of the post :

```yml
---
category: ['jekyll', 'guides', 'sample_category']
---
```

Then to render this category using link and pages. All we need to do is,

1. Create a new file with [your_category_name].md inside categories folder.

2. Copy categories/sample_category.md file and replace the content in [your_category_name].md in that. (Please don't copy the code below its just sample, since it renders the jekyll syntax dynamically)

```jsx
---
layout: page
title: Guides
permalink: /blog/categories/your_category_name/
---

<h5> Posts by Category : {{ page.title }} </h5>

<div class="card">
{% for post in site.categories.your_category_name %}
 <li class="category-posts"><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>
```

Using the category, all the posts associated with the category will be listed on
`http://localhost:4000/blog/categories/your_category_name`
