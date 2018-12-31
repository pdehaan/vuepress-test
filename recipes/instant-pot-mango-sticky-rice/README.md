---
title: Instant Pot Mango Sticky Rice
description: Refried beans, but in an instant pot.
recipeGroup:
  - label: Rice
    ingredients:
      - quantity: 1 cup
        item: Glutonus sweet rice (rinsed)
        note: (Or jasmine rice)
      - quantity: 1&frac14; cups
        item: Almond milk
        note: (Or other milk alternative)
      - quantity: 1 cup
        item: Frozen mangoes
    directions:
      - Add trivet Instant Pot and fill Instant Pot w/ 1 cup water.
      - Add nested bowl to Instant Pot and then do some stuff.
      - Rince [1 cup] glutonous rice under cold water.
      - Add rice, 1&frac14; cups almond milk to rice in 
      - Cover Instant Pot w/ lid and cook for 4 minutes on High.
      - After rice has finished cooking, allow to naturally vent for 10 minutes (and then quick release any remaining pressure).
  - label: Sauce
    ingredients:
      - quantity: "&frac13; cups"
        item: Almond milk
        note: (Or other milk alternative)
      - quantity: 2 Tbsp
        item: Brown sugar
    directions:
      - Add additional [&frac13; cups] almond milk and [2 Tbsp] brown sugar to cooked rice and stir.
      - Garnish w/ black sesame seeds, or whatever.
      - Eat
---

[&laquo; Recipes](/recipes/)

# {{ $page.title }}

{{ $description }}

<!--more-->

Some longer description of the recipe, that is more verbose than just a meta-tag caliber string...

---

<div v-for="group in $page.frontmatter.recipeGroup">

## {{ group.label }}
### Ingredients:

<ul>
  <li v-for="ingredient in group.ingredients">
    <span class="quantity" v-html="ingredient.quantity" />
    <span class="item">{{ ingredient.item }}</span>
    <span class="note" v-if="ingredient.note">{{ ingredient.note }}</span>
  </li>
</ul>

### Directions:

<ol>
  <li v-for="direction in group.directions" v-html="direction" />
</ol>

</div>

<div v-if="false">
  ## DEBUGGERY:

  ### $title={{ $title }}
  ### $description={{ $description }}
  ### frontmatter={{ $page.frontmatter.title }}

  <pre>{{ $page }}</pre>

  <pre>{{ $site }}</pre>
</div>
