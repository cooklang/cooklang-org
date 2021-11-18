---
title: 'Using CookCLI'
date: 2021-05-31T11:31:08-08:00
draft: false
weight: 5
summary: Full documentation for CookCLI on Linux and MacOS.
---


{{< rawhtml >}}
   <a href="https://github.com/cooklang/CookCLI">
        <img style="position: absolute; top: 0; right: 0; border: 0;" src="https://github.blog/wp-content/uploads/2008/12/forkme_right_orange_ff7600.png?resize=149%2C149" alt="Fork me on GitHub">
    </a>
{{< /rawhtml >}}


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
   * [`seed`](#seed)
   * [`version`](#version)
* [Questions and Issues](#questions-and-issues)


# `cook` 

```
OVERVIEW: A toolkit for command-line interaction with Cooklang text files.
Documentation can be found at https://cooklang.org/cli/help/ and issues reported at https://github.com/Cooklang/CookCLI.

USAGE: cook <subcommand>

OPTIONS:
  -h, --help              Show help information.

SUBCOMMANDS:
  recipe                  Manage recipes and recipe files
  shopping-list           Create a shopping list
  server                  Run a webserver to serve your recipes on the web
  fetch                   Pull recipes from the community recipe repository
  seed                    Populate directory with seed recipes
  version                 Show the CookCLI version information

  See 'cook help <subcommand>' for detailed help.
```

## `recipe`

```
OVERVIEW: Manage recipes and recipe files

USAGE: cook recipe <subcommand>

OPTIONS:
  -h, --help              Show help information.

SUBCOMMANDS:
  read                    Parse and print a Cooklang recipe file
  validate                Check for syntax errors in one or more Cooklang recipe files (TODO)
  prettify                Edit a Cooklang recipe file for style consistency (TODO)
  image                   Download a random image from upsplash.com to match the recipe title

  See 'cook help recipe <subcommand>' for detailed help.
```

### `read`

```
OVERVIEW: Parse and print a Cooklang recipe file

USAGE: cook recipe read [<recipe-file>] [--output-format <output-format>] [--only-ingredients]

ARGUMENTS:
  <recipe-file>           A .cook file or STDIN

OPTIONS:
  --output-format <output-format>
                          Set the output format to json or yaml (default: text)
  --only-ingredients      Print only the ingredients section of the output
  -h, --help              Show help information.
 ```

<!-- ### `validate`

```
Usage: cook recipe validate FILE...

Validate the Cooklang syntax of one or more Cooklang recipe files
```

### `prettify`

```
Usage: cook recipe prettify FILE

Edit the content of a Cooklang recipe file for style consistency
```
 -->


### `image`

```
OVERVIEW: Download a random image from upsplash.com to match the recipe title

USAGE: cook recipe image <file>

ARGUMENTS:
  <file>                  A .cook file or STDIN

OPTIONS:
  -h, --help              Show help information.
```

## `shopping-list`

```
OVERVIEW: Create a shopping list

USAGE: cook shopping-list [--aisle <aisle>] [--inflection <inflection>] [<files-or-directory> ...] [--output-format <output-format>] [--only-ingredients]

ARGUMENTS:
  <files-or-directory>    File or directory with .cook files to include to shopping list

OPTIONS:
  -a, --aisle <aisle>     Specify an aisle.conf file to set grouping. Cook automatically checks current directory in ./config/aisle.conf and
                          $HOME/.config/cook/aisle.conf
  -i, --inflection <inflection>
                          Specify an inflection.conf file to define rules of pluralisation. Cook automatically checks current directory in
                          ./config/inflection.conf and $HOME/.config/cook/inflection.conf
  --output-format <output-format>
                          Set the output format to json or yaml (default: text)
  --only-ingredients      Print only the ingredients section of the output
  -h, --help              Show help information.
```


## `fetch`

```
OVERVIEW: Pull recipes from the community recipe repository

USAGE: cook fetch [<community-recipe-path>]

ARGUMENTS:
  <community-recipe-path> Path

OPTIONS:
  -h, --help              Show help information.
```

## `server`

```
OVERVIEW: Run a webserver to serve your recipes on the web

USAGE: cook server [--aisle <aisle>] [--inflection <inflection>] [--port <port>] [--bind <bind>] [<root>]

ARGUMENTS:
  <root>                  A path to serve cook files from

OPTIONS:
  -a, --aisle <aisle>     Specify an aisle.conf file to set grouping. Cook automatically checks current directory in ./config/aisle.conf and
                          $HOME/.config/cook/aisle.conf
  -i, --inflection <inflection>
                          Specify an inflection.conf file to define rules of pluralisation. Cook automatically checks current directory in
                          ./config/inflection.conf and $HOME/.config/cook/inflection.conf
  -p, --port <port>       Set the port on which the webserver should listen (default: 9080)
  -b, --bind <bind>       Set the IP to which the server should bind (default: 127.0.0.1)
  -h, --help              Show help information.
```

## `seed`

```
OVERVIEW: Populate directory with seed recipes

USAGE: cook seed [<seed-directory-path>]

ARGUMENTS:
  <seed-directory-path>   Path

OPTIONS:
  -h, --help              Show help information.
```

## `version`

```
OVERVIEW: Show the CookCLI version information

USAGE: cook version

OPTIONS:
  -h, --help              Show help information.
```

# Questions and Issues

If you have a question about CookCLI that isn't answered here, open an issue on the [Cooklang/CookCLI GitHub repository](https://github.com/Cooklang/CookCLI).
