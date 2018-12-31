---
title: Instant Pot Refried Beans
description: Refried beans, but in an instant pot.
recipe:
  ingredients:
    - quantity: 1.5 cups
      item: Pinto beans
      note: (Or black beans)
    - item: Water
  directions:
    - Put [1&frac12; cups] uncooked beans into Instant Pot.
    - Add enough water to cover by 1-2".
    - Cover Instant Pot w/ lid and cook for 40 minutes on High.
    - After beans have finished cooking, allow to naturally vent for 10 minutes (and then quick release any remaining pressure).
    - Strain.
    - Mash beans using a wooden spoon or potato masher.
---

[&laquo; Recipes](/recipes/)

# {{ $page.title }}

{{ $description }}

<!--more-->

Some longer description of the recipe, that is more verbose than just a meta-tag caliber string...

---

## Ingredients:

<ul>
  <li v-for="ingredient in $page.frontmatter.recipe.ingredients">
    <span class="quantity" v-html="ingredient.quantity" />
    <span class="item">{{ ingredient.item }}</span>
    <span class="note" v-if="ingredient.note">{{ ingredient.note }}</span>
  </li>
</ul>

## Directions:

<ol>
  <li v-for="direction in $page.frontmatter.recipe.directions" v-html="direction" v-once />
</ol>

---

## DEBUGGERY:

### $title={{ $title }}
### $description={{ $description }}
### frontmatter={{ $page.frontmatter.title }}

<pre>{{ $page }}</pre>

<pre>{{ $site }}</pre>
