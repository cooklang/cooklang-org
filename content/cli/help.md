---
title: 'Using CookCLI'
date: 2021-05-31T11:31:08-08:00
draft: false
weight: 5
summary: Full documentation for CookCLI on Linux and MacOS.
---

This documentation is a work in progress.

Table of Contents
=================

* [`cook`](#cook)
   * [`recipe`](#recipe)
      * [`read`](#read)
      * [`validate`](#validate)
      * [`prettify`](#prettify)
      * [`image`](#image)
   * [`shopping-list`](#shopping-list)
   * [`fetch`](#fetch)
   * [`server`](#server)
   * [`version`](#version)
* [Questions and Issues](#questions-and-issues)


# `cook` 

```
Usage: cook [OPTIONS] COMMAND

A toolkit for command-line interaction with CookLang text files

Options:
  -aisle        Specify an aisle.conf file to override shopping list default settings
  -units        Specify a units.conf file to override units default settings
  -inflection   Specify an inflection.conf file to override default inflection settings

Commands:
  recipe	     	   Manage recipes and recipe files
  shopping-list	   Create a shopping list
  fetch 			     Pull recipes from the community recipe repository
  server			     Run a webserver to serve your recipes on the web
  version			     Show the CookCLI version information

Run `cook COMMAND --help` for more information on a command.
```

## `recipe`

```
Usage: cook recipe COMMAND

Read and edit CookLang recipe files

Commands:
read 		  Parse and print a CookLang recipe file
validate	Check for syntax errors in one or more CookLang recipe files
prettify	Edit a CookLang recipe file for style consistency
image		  Download a random image from upsplash.com to match the recipe title

Run `cook recipe COMMAND --help` for more information on a command.
```

### `read`

```
Usage: cook recipe read [OPTIONS] FILE

Parse and print a CookLang recipe file

Options:
  -output-format={json|yaml}	Set the output format (default json)
  -only-ingredients				Print only the ingredients section of the output
  -only-steps					Print only the steps section of the output
  -compact						Print a machine-friendly version of the output
 ```

### `validate`

```
Usage: cook recipe validate FILE...

Validate the CookLang syntax of one or more CookLang recipe files
```

### `prettify`

```
Usage: cook recipe prettify FILE

Edit the content of a CookLang recipe file for style consistency
```



### `image`

```
Usage cook recipe image FILE

Download a random image from upsplash.com to match a recipe title
```

## `shopping-list`

```
Usage: cook shopping-list [OPTIONS] FILE...

Generate a shopping list from the given CookLang recipe file(s)

Options:
  -output-format={json|yaml}	Specify the output format of the shopping list file (default json)
  -only-ingredients				    Output only ingredient names (excludes quantities)
  -compact						        Output in a machine-friendly format
```


## `fetch`

```
Usage: cook fetch RECIPE [FILE]

Pull a recipe (as a subdirectory of https://github.com/CookLang/recipes/), optionally as a specified file name
```

## `server`

```
Usage: cook server [OPTIONS]

Run a webserver to serve your recipes on the web

Options:
  -port		Set the port on which the webserver should listen (default 8080)
  -bind		Set the IP to which the server should bind (default 127.0.0.1)
```

## `version`

```
Usage: cook version

Show the version information for CookCLI
```

# Questions and Issues

If you have a question about CookCLI that isn't answered here, open an issue on the [CookLang/CookCLI GitHub repository](https://github.com/CookLang/CookCLI).