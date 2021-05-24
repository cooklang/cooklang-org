---
title: 'Cook – Recipe Markup Language'
date: 2018-11-28T15:14:39+10:00
---

Cook is an open source markup language that helps to manage recipes in simple, flexible and something way.

* Readable as regular text – we thrive for simplicity
* Everything is a file – that means easy to organise, share and change (iterate)
* Small tool built in UNIX way


To get started with Cook, create a recipe file, tag ingredients with @ and now you have you recipe ready:

```
Then add @salt and @ground black pepper{} to taste.

Poke holes in @potato{2}.

Place @bacon strips{1%kg} on a baking sheet and glaze with @syrup{1/2%tbsp}.
```

There're a few more things to it. Check our human friendly [Language Specification](/docs/spec/).


## Cook CLI

[Cook CLI](/cli/) helps to create shopping lists and maintain recipes. It provides great help in automating the routine related to shopping. Can be accessed from UNIX command-line and can provide great help with custom scripts you create.


```
$ cook recipe read ./Baked Potato.cook
Ingredients
+++++++++++
bla bla bla

Steps
+++++
1. bla
...
12. bla
```

## iOS app

[iOS app](/app/) nicely presents your recipe files from iCloud drive and you can use it while cooking or for shopping and meal planning.


![Recipes](/app/recipes.png)
![Recipe](/app/recipe-ingredients.png)
![Shopping list](/app/shopping-list.png)
