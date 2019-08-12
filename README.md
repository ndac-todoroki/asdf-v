# asdf-v

V ([The V Programming Language](https://vlang.io/)) plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

[![Build Status](https://travis-ci.com/ndac-todoroki/asdf-v.svg?branch=master)](https://travis-ci.com/ndac-todoroki/asdf-v)

## Install

Make sure you have `curl` and `cc`. (and `asdf`.) Also, if you plan to use the `http` package and/or gui packages, you need some dependencies. Read https://github.com/vlang/v#running-the-examples.

To install the plugin, run this:

```
asdf plugin-add v
```
(Now this plugin is on the asdf-plugins repo, so no Github urls are needed!)

## Compiling from a Github Release Tag

```
$ asdf install v 0.1.0
```

## Compiling from a Git reference or from source

Along with released versions, you can always install any version of the git commit id or git tag name.

### Using the CLI

You can download and compile a specific commit reference from the [V GitHub repository](https://github.com/vlang/v/commits/master) by running: `asdf install v ref:<commit reference>`. You can then set the local/global version to your new version by running:

```
asdf local v ref:<commit reference>
# Or
asdf global v ref:<commit reference>
```


### .tool-versions file

You can specify the version to install with a line like so in your `.tool-versions` file:

```
v ref:<commit reference>
```

### About symlinks

In the past, `V` required `~/code/v` to be the executable path, and `asdf-v` used and recreated a symlink every time the asdf shim was called.
`V` now doesn't use that directory (and ENV values), so current `asdf-v` versions do not create symlinks, and doesn't require/edit the `~/code` directory anymore.

## Use

Check [asdf](https://github.com/asdf-vm/asdf) readme for instructions on how to install & manage versions of V.
