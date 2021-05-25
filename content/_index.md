---
title: 'Cook – Recipe Markup Language'
date: 2021-05-20T15:14:39+10:00
---

Cook is the markup language at the center of an open-source ecosystem for cooking and recipe management.

Together with tools based on it it aims to:
* simplify personal recipe management;
* reduce shopping routine;
* make cooking more fun.

> Cook ecosystem features:
> * Recipes are all in human-readable format.
> * Everything stored as files. That means it's easy to organize, share and improve your recipes as often as needed. Symlinks make its easy to create meal plans.
> * Embraces UNIX way: small but sharp tool for just one task.


## How to get started with Cook

Create a recipe file, tag ingredients with @ and now you have your recipe ready:

```
Then add @salt and @ground black pepper{} to taste.

Poke holes in @potato{2}.

Place @bacon strips{1%kg} on a baking sheet and glaze with @syrup{1/2%tbsp}.
```

There are a few more things to it. Check out full [Language Specification](/docs/spec/).


## Cook CLI

[Cook CLI](/cli/) helps to create shopping lists and maintain recipes. It provides great help in automating the routine related to shopping. Can be accessed from UNIX command-line and useful for scripting you create to automate your routine.


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

Also can start as a server and provide access to recipes.

## iOS app

[iOS app](/app/) created to assist you while cooking, shopping and meal planning. You organise recipe files on iCloud drive on your Mac and the app will present them.

![Recipes](/app/recipes.png)
![Recipe](/app/recipe-ingredients.png)
![Shopping list](/app/shopping-list.png)
