---
title: 'Cook – Recipe Markup Language'
date: 2021-05-20T15:14:39+10:00
---

Cook is a markup language at the center of our open-source ecosystem for cooking and recipe management.

Cook and the tools we've built to use it, you can:

* simplify your personal recipe management;
* streamline your shopping routine;
* make cooking more fun.

Here's how the Cook ecosystem makes that happen:

* All recipes are human-readable text files.
* Everything is a file. No databases. And you have complete control over your information.
* All the tools are simple, focused, and efficient; the UNIX way.

## Getting Started

**Create a recipe file**, where each line is a step in the recipe. Tag your ingredients with @ and {}, then save your file to iCloud. For a complete reference on the CookLang markup language specification, see the full [language specification](/docs/spec).

```
Then add @salt and @ground black pepper{} to taste.

Poke holes in @potato{2}.

Place @bacon strips{1%kg} on a baking sheet and glaze with @syrup{1/2%tbsp}.
```

**Install a recipe viewer.** We support a few tools for viewing CookLang recipes:
* [The iOS app for iPad and iPhone](/app/) allows you to read your recipe files directly from iCloud.
* [The CookCLI program for Mac and Linux](/cli/) provides a web server for presenting your recipes, viewable with any web browser.

**Cook something!** Open a recipe on your viewer of choice, whip out the ingredients, and make something tasty.

## CookCLI

The [Cook CLI](/cli/) command line program provides a suite of tools to create shopping lists and maintain recipes. We've built it to be simple and useful for automating your cooking and shopping routine with existing UNIX command line and scripting tools. It can also function as a web server for your recipes, making them browsable on any device with a web browser.


## iOS app

We created the [iOS app](/app/) to assist you while cooking, shopping, and meal planning. Simply connect the app to your iCloud, open a recipe, and start cooking.

![Recipes](/app/recipes.png)
![Recipe](/app/recipe-ingredients.png)
![Shopping list](/app/shopping-list.png)
