---
title: 'Recipe'
date: 2019-02-11T19:30:08+10:00
draft: false
weight: 10
summary: Change me
---



As last argument user can pass any particular recipe, multiple recipes or directory (to use all cook files in directory) also STDIN

### Read


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

Also possible to format the output. Supported formats are json and yaml:

```
cook recipe read -output-format=json ./Baked Potato.cook
```

TODO pdf

### Validate

Will check cook specification for any syntax errors or validation problems.

```
cook recipe validate ./Baked Potato.cook
```

### Prettify

To make pretty

```
cook recipe prettify ./Baked Potato.cook
```

### Image

Will fetch a random image from unsplash.com and put it next to cook file

```
cook recipe prettify ./Baked Potato.cook
```
