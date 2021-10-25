---
title: 'CookLang – Recipe Markup Language'
date: 2021-05-20T15:14:39+10:00
---

![Recipes](/example.png)

CookLang and the tools we've built to use it, you can:

* simplify your personal recipe management;
* streamline your shopping routine;
* make cooking more fun.

Here's how the CookLang ecosystem makes that happen:

* All recipes are human-readable text files.
* Everything is a file. No databases. And you have complete control over your information.
* All the tools are simple, focused, and efficient; the UNIX way.

## Getting Started

**Create a recipe file**, where each line is a step in the recipe. Tag your ingredients with `@` and `{}`, then save your file. For a complete reference on CookLang, see the [language specification page](/docs/spec).

**Install a recipe viewer.** We support a few tools for viewing CookLang recipes:
* [The CookCLI program for Mac and Linux](/cli/) provides a webserver for presenting your recipes, viewable with any web browser.
* [The iOS app for iPad and iPhone](/app/) allows you to read your recipe files directly from iCloud.

**Cook something!** Open a recipe on your viewer of choice, whip out the ingredients, and make something tasty.

## CookCLI

The [Cook CLI](/cli/) command line program provides a suite of tools to create shopping lists and maintain recipes. We've built it to be simple and useful for automating your cooking and shopping routine with existing UNIX command line and scripting tools. It can also function as a webserver for your recipes, making them browsable on any device with a web browser.

```
# create sample recipes
cook seed

# check content of "Neapolitan Pizza" recipee
cook recipe read "Neapolitan Pizza.cook"

# create a shopping list for all sample recipes
cook shopping-list .
```

## iOS app

We created the [iOS app](/app/) to assist you while cooking, shopping, and meal planning. Simply connect the app to your iCloud, open a recipe, and start cooking.

![Recipes](/app/recipes.png)
![Recipe](/app/recipe-ingredients.png)
![Shopping list](/app/shopping-list.png)
