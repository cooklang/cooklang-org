---
title: 'Help'
date: 2019-02-11T19:30:08+10:00
draft: false
weight: 4
summary: Syntax highlighting and menus can be configured via `config.toml`.
---

# Frequently Asked Questions

## Recipes

### How do I create a new recipe?
A recipe is just a text file using the cooklang markup language and the .cook file extension. To create a new recipe, just open a text editor and write out the steps! For details on how to use the cooklang markup language, see the [cooklang github specification page](https://github.com/cooklang/spec).

### Where do I put a recipe file after I've created it?
When you first install the app, a folder will be created at the root of your iCloud called "Cook". All Cook apps and programs will search that folder (and any sub-folders) for files related to the Cook app.

### Can I change the folder that the app uses for recipes?
This feature is not yet supported.

### Can I put recipes inside folders, will the app still find it?
Yep. You can bury that .cook file in as many layers of folders as you'd like. 

### How do I enable cooklang syntax highlighting in my text editor?
This feature is not yet supported.

### How do I add community-made recipes?
When you first install the app, you will be given the option to import a few sample recipes. If you would like to add 

### What are the best-practices when creating a recipe?
You can check out our full article on best-practices for creating recipes on our [github]()

### Can I import a recipe from a link?
This feature is not yet supported.

### Do I have to manually create every recipe I want to cook?
No! You can add any recipe you find online in the .cook format to your Cook folder and it will be automatically imported when you open the app.

### How do I share recipes I've made with the community?
If you're handy with Git, you can open a pull request to the community recipe repository and we'll add it!

### How do I remove a recipe?
You can remove a recipe by deleting the file from your .cook folder.

## Shopping lists

### How do I create a shopping list?
Go to a recipe you plan to cook, and at the top of the ingredients tab will be a button labeled "Add to shopping list". This  will add all of the ingredients for that recipe (and their quantities) to your shopping list. 

### Can I export a shopping list to another app or format?
In the Cook app, it is possible to export a shopping list as an email. Using the Cook command line tool, it is possible to export to other data formats (such as Json).

### How do I remove something from the shopping list?
Easy! Just tap and hold on the item in the shopping list, then tap "Remove".

### How do I change the default categories in the shopping list?
The categorization of the shopping list is configured by a simple configuration file.
