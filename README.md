[![license](https://img.shields.io/github/license/micro-os-plus/platform-sifive-hifive1-xpack)](https://github.com/micro-os-plus/platform-sifive-hifive1-xpack/blob/xpack/LICENSE)
[![CI on Push](https://github.com/micro-os-plus/platform-sifive-hifive1-xpack/workflows/CI%20on%20Push/badge.svg)](https://github.com/micro-os-plus/platform-sifive-hifive1-xpack/actions?query=workflow%3A%22CI+on+Push%22)

# A source library xPack with the µOS++ SiFive HiFive1 board specific files

This project provides support for the SiFive HiFive1 development board.

The project is hosted on GitHub as
[micro-os-plus/platform-sifive-hifive1-xpack](https://github.com/micro-os-plus/platform-sifive-hifive1-xpack).

## Maintainer info

This page is addressed to developers who plan to include this source
library into their own projects.

For maintainer info, please see the
[README-MAINTAINER](README-MAINTAINER.md) file.

## Install

As a source library xPacks, the easiest way to add it to a project is via
**xpm**, but it can also be used as any Git project, for example as a submodule.

### Prerequisites

A recent [xpm](https://xpack.github.io/xpm/),
which is a portable [Node.js](https://nodejs.org/) command line application.

For details please follow the instructions in the
[xPack install](https://xpack.github.io/install/) page.

### xpm

Note: the package will be available from npmjs.com at a later date.

For now, it can be installed from GitHub:

```sh
cd my-project
xpm init # Unless a package.json is already present

xpm install github:micro-os-plus/platform-sifive-hifive1-xpack
```

When ready, this package will be available as
[`@xpack-sifive/platform-hifive1`](https://www.npmjs.com/package/@xpack-sifive/platform-hifive1)
from the `npmjs.com` registry:

```sh
cd my-project
xpm init # Unless a package.json is already present

xpm install @xpack-sifive/platform-hifive1@latest

ls -l xpacks/xpack-sifive-platform-hifive1
```

### Git submodule

If, for any reason, **xpm** is not available, the next recommended
solution is to link it as a Git submodule below an `xpacks` folder.

```sh
cd my-project
git init # Unless already a Git project
mkdir -p xpacks

git submodule add https://github.com/micro-os-plus/platform-sifive-hifive1-xpack.git \
  xpacks/micro-os-plus-platform-sifive-hifive1
```

## Branches

Apart from the unused `master` branch, there are two active branches:

- `xpack`, with the latest stable version (default)
- `xpack-develop`, with the current development version

All development is done in the `xpack-develop` branch, and contributions via
Pull Requests should be directed to this branch.

When new releases are published, the `xpack-develop` branch is merged
into `xpack`.

## User info

TBD

### Status

The SiFive HiFive1 definitions are fully functional. Only the
initial version is supported.

### Build & integration info

To include this package in a project, consider the following details.

#### Source folders

- `src`

#### Include folders

- `include`

The standard way to include the board files is

```c
#include <micro-os-plus/platform.h>
```

#### Preprocessor definitions

- `PLATFORM_SIFIVE_HIFIVE1`

#### Compiler options

- `-std=c++20` or higher for C++ sources
- `-std=c11` for C sources

#### C++ Namespaces

TBD

#### C++ Classes

TBD

### Examples

TBD

### Known problems

- none

### Tests

TBD

## License

The original content is released under the
[MIT License](https://opensource.org/licenses/MIT/),
with all rights reserved to
[Liviu Ionescu](https://github.com/ilg-ul/).
