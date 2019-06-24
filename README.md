# asdf-v

V ([The V Programming Language](https://vlang.io/)) plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

[![Build Status](https://travis-ci.com/ndac-todoroki/asdf-v.svg?branch=master)](https://travis-ci.com/ndac-todoroki/asdf-v)

## Install

Make sure you have `curl` and `make`. (and `asdf`.) Also, if you plan to use the `http` package and/or gui packages, you need some dependencies. Read https://github.com/vlang/v#running-the-examples.

To install the plugin, run this:

```
asdf plugin-add v https://github.com/ndac-todoroki/asdf-v.git
```

### BE CAREFUL

Currently V does not support custom installation. [vlang/v #457](https://github.com/vlang/v/issues/457)  
As a workaround, this plugin recreates a symlink of the V installation folder to `~/code/v` every time shim `v` is called. **It is preferred not to touch `~/code`.**

## Compiling from a Git reference or from source

Although this plugin is created to show installable versions from Github releases, since the V releases are not stable yet, and the tar files doesn't contain enough files, you can't install from them currently.
Instead, you can always install any version of the git commit id or git tag name.

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

### The `master` tag

Just until V gets stable, `asdf install v master` does the same as `asdf install v ref:master` (the installation would be separate). This is just for less-typing. When you want to update the `master` V, first uninstall it (`asdf uninstall v master`) and then install it again.
Keep in mind that `master` will always fetch the latest commit in the master branch, so it might be unstable, or worse, broken.


## Use

Check [asdf](https://github.com/asdf-vm/asdf) readme for instructions on how to install & manage versions of V.
