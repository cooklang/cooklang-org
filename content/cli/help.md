---
title: 'Using CookCLI'
date: 2021-05-31T11:31:08-08:00
draft: false
weight: 5
summary: Full documentation for CookCLI on Linux and MacOS.
---

This documentation is a work in progress.

# `$ cook --help` 

```
Usage: cook COMMAND

A toolkit for command-line interaction with cooklang text files

Commands:
  recipe			Manage recipes and recipe files
  shopping-list		Create a shopping list
  community			Pull recipes from the community recipe repository
  server			Run a webserver to serve your recipes on the web
  version			Show the CookCLI version information

Run `cook COMMAND --help` for more information on a command.
```

## `$ cook recipe --help`

```
Usage: cook recipe COMMAND

Read and edit cooklang recipe files

Commands:
read 		Parse and print a cooklang recipe file
validate	Check for syntax errors in a cooklang recipe file
prettify	Edit a cooklang recipe file for style consistency
image		Download a random image from upsplash.com to match the recipe title

Run `cook recipe COMMAND --help` for more information on a command.
```

### `$ cook recipe read --help`

```
Usage: cook recipe read [OPTIONS] FILE

Parse and print a cooklang recipe file

Options:
  -output-format={json|yaml}	Set the output format (default json)
  -only-ingredients				Print only the ingredients section of the output
  -only-steps					Print only the steps section of the output
  -compact						Print a machine-friendly version of the output
 ```

### `$ cook recipe validate --help`

```
Usage: cook recipe validate FILE

Validate the cooklang syntax of a cooklang recipe file
```

### `$ cook recipe prettify --help`

```
Usage: cook recipe prettify FILE

Edit the content of a cooklang recipe file for style consistency
```



### `$ cook recipe image --help`

```
Usage cook recipe image FILE

Download a random image from upsplash.com to match a recipe title
```

## `$ cook shopping-list --help`

```
Usage: cook shopping-list [OPTIONS] FILE...

Generate a shopping list from the given cooklang recipe file(s)

Options:
  -output-format={json|yaml}	Specify the output format of the shopping list file (default json)
  -only-ingredients				???
  -compact						???
```


## `$ cook community --help`

```
Usage: cook community COMMAND

A utility for interacting with the cook community recipe repository

Commands:
  fetch		Pull a recipe from the community recipe repository

Run `cook community COMMAND --help` for more information on a command.
```

### `$cook community fetch --help`

```
Usage: cook community fetch RECIPE [FILE]

Pull a recipe (as a subdirectory of https://github.com/cooklang/recipes/), optionally as a specified file name
```

## `$ cook server --help`

```
Usage: cook server [OPTIONS]

Run a webserver to serve your recipes on the web

Options:
  -port		Set the port on which the webserver should listen (default 8080)
  -bind		Set the IP to which the server should bind (default 127.0.0.1)
```

## `$ cook version --help`

```
Usage: cook version

Show the version information for CookCLI
```

# Questions and Issues

If you have a question about CookCLI that isn't answered here, open an issue on the [cooklang/CookCLI GitHub repository](https://github.com/cooklang/CookCLI).