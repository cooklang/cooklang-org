---
title: 'Help'
date: 2019-02-11T19:30:08+10:00
draft: false
weight: 1
summary: Change me
---



* [Recipe](#recipe)
* [Shopping list](#shopping-list)
* [Server](#server)
* [Comminity](#community)
* [Configs](#configs)
* [Version](#version)


## Recipe

As last argument user can pass any particular recipe, multiple recipes or directory (to use all cook files in directory) also STDIN

### Read


```
$ cook recipe read ./Chimichanga.cook
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
cook recipe read -output-format=json ./Chimichanga.cook
```

TODO pdf

### Validate

Will check cook specification for any syntax errors or validation problems.

```
cook recipe validate ./Chimichanga.cook
```

### Prettify

To make pretty

```
cook recipe prettify ./Chimichanga.cook
```

### Image

Will fetch a random image from unsplash.com and put it next to cook file

```
cook recipe prettify ./Chimichanga.cook
```

## Shopping list

```
cook shopping-list ./Chimichanga.cook ./Salads
```

or directory which contains symlinks

```
cook shopping-list "./Week Plan 3 (Healthy)"
```

Can output to json or yaml

```
cook shopping-list -output-format=json ./Chimichanga.cook ./Salads
```

### Custom output

Ingredients not listed

```
cook shopping-list -only-ingredients ./Chimichanga.cook ./Salads
```



```
cook shopping-list -compact ./Chimichanga.cook ./Salads
```

## Community

```
cook community import dinners/mexican/chimichanga ./
```

or no output will save here


## Server

local web server a-la web app clone

```
cook server
```

options

`-port`

`-bind`



## Configs

Cook will try to get configs in local directory if .cook directory is present. Also in home. Or if passed with option option.

Possible configs are aisle config, units conversion and inflection.




### Aisle config
Used for grouping ingredients.

```
cook -aisle ./aisle.conf ...
```

#### Missing ingredients

```
cook -aisle ./aisle.conf aisle missing ./Chimichanga.cook
```

### Unit converstion config (TODO)

```
cook -units ./units.conf
```

### Inflection

To properly work with plural/singular words
```
cook -units ./inflection.conf ...
```

### Nutritions config (TODO)

```
cook -units ./nutritions.conf ...
```

### Default configs

It's possible to output default config.

```
cook defaults aisle.conf
```

## Version

The version command displays build information about the running binary, including the release version and the exact revision.
