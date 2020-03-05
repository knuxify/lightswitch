# lightswitch

Argument parser generator for POSIX-compatible shells.

## Features

- Quickly create argument parsers for any shell app.
- Fully compatible with standard sh - no bashisms.
- Generates a help switch automatically.

## How does it work?

lightswitch takes a [configuration file](https://github.com/knuxify/lightswitch/wiki/Configuration) which is used to generate a small script with the switch functions.

## Configuration file format spec (temporarily here)

Comments start with ``#``.

Each line follows the following spec:

```
"switch" : "description" > outputvar < type
```

* ``switch`` - the switch(es). Separated by ``|``, if there are multiple. Required.
* ``description`` - the description. Required.
* ``outputvar`` - variable to save output to. Required.
* ``type`` - type of input. This enables extra checks for certain things. Available types: default, file, directory. Not required. Defaults to ``default``.
