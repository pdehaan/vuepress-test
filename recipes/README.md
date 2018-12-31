---
title: Recipes
---

THis is the recipes page for recipes on the site.
Ideally a paginated listing or something.

<p v-for="page in $site.pages.filter(page => page.path.startsWith('/recipes/') && page.path !== '/recipes/')" :key="page.key">
  <a :href="page.path" v-text="page.title" v-once />
</p>
