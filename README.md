oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g @taskmemos/tm
$ tm COMMAND
running command...
$ tm (--version)
@taskmemos/tm/0.0.0 linux-x64 node-v16.17.0
$ tm --help [COMMAND]
USAGE
  $ tm COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`tm hello PERSON`](#tm-hello-person)
* [`tm hello world`](#tm-hello-world)
* [`tm help [COMMANDS]`](#tm-help-commands)
* [`tm plugins`](#tm-plugins)
* [`tm plugins:install PLUGIN...`](#tm-pluginsinstall-plugin)
* [`tm plugins:inspect PLUGIN...`](#tm-pluginsinspect-plugin)
* [`tm plugins:install PLUGIN...`](#tm-pluginsinstall-plugin-1)
* [`tm plugins:link PLUGIN`](#tm-pluginslink-plugin)
* [`tm plugins:uninstall PLUGIN...`](#tm-pluginsuninstall-plugin)
* [`tm plugins:uninstall PLUGIN...`](#tm-pluginsuninstall-plugin-1)
* [`tm plugins:uninstall PLUGIN...`](#tm-pluginsuninstall-plugin-2)
* [`tm plugins update`](#tm-plugins-update)

## `tm hello PERSON`

Say hello

```
USAGE
  $ tm hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/taskmemos/tm/blob/v0.0.0/dist/commands/hello/index.ts)_

## `tm hello world`

Say hello world

```
USAGE
  $ tm hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ tm hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [dist/commands/hello/world.ts](https://github.com/taskmemos/tm/blob/v0.0.0/dist/commands/hello/world.ts)_

## `tm help [COMMANDS]`

Display help for tm.

```
USAGE
  $ tm help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for tm.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.19/src/commands/help.ts)_

## `tm plugins`

List installed plugins.

```
USAGE
  $ tm plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ tm plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.5.0/src/commands/plugins/index.ts)_

## `tm plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ tm plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ tm plugins add

EXAMPLES
  $ tm plugins:install myplugin 

  $ tm plugins:install https://github.com/someuser/someplugin

  $ tm plugins:install someuser/someplugin
```

## `tm plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ tm plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ tm plugins:inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.5.0/src/commands/plugins/inspect.ts)_

## `tm plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ tm plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ tm plugins add

EXAMPLES
  $ tm plugins:install myplugin 

  $ tm plugins:install https://github.com/someuser/someplugin

  $ tm plugins:install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.5.0/src/commands/plugins/install.ts)_

## `tm plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ tm plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ tm plugins:link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.5.0/src/commands/plugins/link.ts)_

## `tm plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ tm plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ tm plugins unlink
  $ tm plugins remove
```

## `tm plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ tm plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ tm plugins unlink
  $ tm plugins remove
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.5.0/src/commands/plugins/uninstall.ts)_

## `tm plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ tm plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ tm plugins unlink
  $ tm plugins remove
```

## `tm plugins update`

Update installed plugins.

```
USAGE
  $ tm plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.5.0/src/commands/plugins/update.ts)_
<!-- commandsstop -->
