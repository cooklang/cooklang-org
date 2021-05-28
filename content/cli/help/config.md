---
title: 'Config'
date: 2021-05-20T19:30:08+10:00
draft: false
weight: 40
summary: Details on configuring the various options for CookCLI.
---


Cook will try to get configs in local directory if .cook directory is present. Then it will look in home directory. Or if passed with option, it will use from an option.

Possible configs are aisle config, units conversion and inflection.


### Aisle config
Used for grouping ingredients.

```
cook -aisle ./aisle.conf ...
```

#### Missing ingredients

```
cook -aisle ./aisle.conf aisle missing ./Baked Potato.cook
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
