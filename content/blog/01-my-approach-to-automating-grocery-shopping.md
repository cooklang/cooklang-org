---
title: 'My approach to automating grocery shopping'
date: 2021-05-20T19:27:37+10:00
weight: 100
summary: How and why I created Cooklang in the first place.
---

The pandemic has presented everyone with unique challenges. For me, it became particularly hard to switch to online grocery shopping.

When I do my shopping offline, I usually don’t have to plan much, moving through the isles and picking up stuff as I go. It’s rare that I forget something, but more often I buy things I don’t actually need, but isn’t that part of how supermarkets work? In my typical order, I'd buy groceries for seven to ten days at a time and it would contain sixty to eighty items in my cart.

Shopping online is a different story. I can't reproduce the same behaviour and go down every isle. So, I realized I needed to plan my meals. I started writing down ingredients for meals I wanted to make on sticky notes and combining them to make an order.

This was really tedious. After a few orders, I noticed that it was kind of repetitive. Although my wife will tell you that I just was lazy and didn't want to do boring stuff, the developer in me said, ”It's time to automate this and never solve the same problem again.”

That's how [Cooklang](https://cooklang.org/) was born.

# About Cooklang

I thought, *what if I store my recipes in Markdown-like text files and tag ingredients with @ symbol?* Like this:

```
    Then add @salt and @ground black pepper{} to taste.
    Poke holes in @potato{2}.
    Place @bacon strips{1%kg} on a baking sheet and glaze with @syrup{1/2%tbsp}.
```

That will make recipe files human and machine readable.

Given these recipe files, computers can create a shopping list and much more: calculate nutrition values, costs or whatever else you could need, given that information for ingredients provided.

And the recipe is still human readable, so I can be agile and store my recipes in git and perfect them over time (like code refactoring).

Also, because it's just a simple text format I avoid "vendor lock-in" problems and can use my recipes the same way when I retire. My recipes are mine, forever.

# About tools

Having only a language specification isn't really helpful. Yes, I can store my recipes on GitHub and own them, but that's it.

I imagined it would be nice to have many small applications which can understand the language and do their own thing very well: calculate calories, shopping, costs, smart meal planning, etc. I was really excited.

I read a wonderful book, [Crafting Interpreters](http://craftinginterpreters.com/) by Robert Nystrom, and did a few experiments. I created a simple [parser](https://github.com/cooklang/CookInSwift) and [CLI app](https://github.com/cooklang/CookCLI). In this post, I wanted to focus on how I automated shopping. I might write another post about the parser and CLI, if anyone interested, so I will skip all the details about those for now.

So CLI can understand Cooklang files, extract ingredients, and group them:

```
    $ cook shopping-list \
    > Neapolitan\ Pizza.cook \
    > Root\ Vegetable\ Tray\ Bake.cook
    BREADS AND BAKED GOODS
        breadcrumbs                   150 g

    DRIED HERBS AND SPICES
        dried oregano                 3 tbsp
        dried sage                    1 tsp
        pepper                        1 pinch
        salt                          25 g, 2 pinches

    FRUIT AND VEG
        beetroots                     300 g
        carrots                       300 g
        celeriac                      300 g
        fresh basil                   18 leaves
        garlic                        3 gloves
        lemon                         1 item
        onion                         1 large
        red onion                     2 items
        thyme                         2 springs

    MEAT AND SEAFOOD
        parma ham                     3 packs

    MILK AND DAIRY
        butter                        15 g
        egg                           1 item
        mozzarella                    3 packs

    OILS AND DRESSINGS
        Dijon mustard                 1 tsp
        Marmite                       1 tsp
        cider                         150 ml
        olive oil                     3 tbsp

    OTHER (add new items into aisle.conf)
        tipo zero flour               820 g

    PACKAGED GOODS, PASTA AND SAUCES
        vegetable stock               150 ml
        water                         530 ml

    TINNED GOODS AND BAKING
        cannellini beans              400 g
        chopped tomato                3 cans
        fresh yeast                   1.6 g
        redcurrant jelly              1 tsp

```

I can set output format to json or yaml and feed this into other programs, or just use good old plain text output manipulation. CLI has a few more features like a web-server to explore the recipes with cooking mode and make shopping list in the browser.

I migrated a bunch of recipes from scattered sources into Cooklang format and stored them on GitHub repository [https://github.com/dubadub/cookbook](https://github.com/dubadub/cookbook).

# My grocery shopping approach

Unfortunately, I haven't fully automated my grocery shopping yet. I still need to do some manual steps, because my shop doesn't provide any API access (surprise!).

That's how my process looks now:

1/ I generate a list of all ingredients. I added directories with symlinks to recipes, which represent a meal plan. So it's easy to generate a list of ingredients for the whole directory like that:

```
    $ cook shopping-list --only-ingredients ./Plan\ I
```

2/ I remove anything I already have at home from the list.

3/ I paste all the ingredients to a multi search input on the shop's web-site.

4/ I manually go through each item and add it to my cart 😓.

5/ Done!

It has a manual step, but:

* it’s much faster than before.
* it’s less for me to think about;
* it makes the entire process more precise.

I'm really happy with this precision part. I noticed that I now cover all my needs but no longer over consume. I see this as a form of eco-sufficiency in some ways.

# What's next

I have only solved 80% of my problem, and I want to do more. I'm thinking about creating a mapping between ingredients from my recipes and links to them at my shop's website. That will allow me to use curl or Selenium to complete my solution.


-Alexey

Note, originally posted on [Daniweb](https://www.daniweb.com/programming/software-development/threads/537481/my-approach-to-automating-grocery-shopping).
