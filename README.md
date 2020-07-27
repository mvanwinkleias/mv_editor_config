# mv_editor_config

Many programming languages have many different style guides, and linters,
and so forth.  Sometimes the rules they impose effectively mandate the
use of an IDE.  Sometimes the rules they impose are "justified" by claiming
that a programmer (not using an IDE) would have problems interacting with
code unless youNameMethodsThus.

Regardless of some rules not improving the quality of code, it seems like
some programming languages just expect you to adhere to the rules without
thinking about it.

This repository might help you not hurt your brain by not having to think
about such things.

# License

copyright (C) 2020 Martin VanWinkle III, Institute for Advanced Study

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

See 

* http://www.gnu.org/licenses/

## Description

Under src/etc you will find configuration files for vim.  I'm going to
start using them and improving on them so that the next time a build
"fails" because of a trailing space, or because I wrote
```
if ( something )
{
	do_something();
}
```
instead of
```
if (something) {
    do_something();
}
```
I just wont have to care.

# Supplemental Documentation

Supplemental documentation for this project can be found here:

* [Supplemental Documentation](./doc/index.md)

# Installation

Ideally stuff should run if you clone the git repo, and install the deps specified
in either "DEBIAN/control" or "RPM/specfile.spec"

Optionally, you can build a package which will install the config in

* /opt/IAS/etc/mv-editor-config/

That way, you can symlink the config into wherever it needs to go, 
and when these standards update, you can install the updated package.

# Building a Package

## Requirements

### All Systems

* fakeroot

### Debian

* build-essential

### RHEL based systems

* rpm-build

## Export a specific tag (or just the project directory)

## Supported Systems

### Debian packages

```
  fakeroot make package-deb
```

### RHEL Based Systems

```
fakeroot make package-rpm
```

