---
title: 'Shopping List'
date: 2021-05-20T19:30:08+10:00
draft: false
weight: 20
summary: Managing, editing, and exporting shopping lists
---



```
cook shopping-list ./Baked Potato.cook ./Salads
```

or directory which contains symlinks

```
cook shopping-list "./Week Plan 3 (Healthy)"
```

Can output to json or yaml

```
cook shopping-list -output-format=json ./Baked Potato.cook ./Salads
```

### Custom output

Ingredients not listed

```
cook shopping-list -only-ingredients ./Baked Potato.cook ./Salads
```



```
cook shopping-list -compact ./Baked Potato.cook ./Salads
```
