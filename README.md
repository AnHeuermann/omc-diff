# omc-diff

[![build](https://github.com/AnHeuermann/omc-diff/actions/workflows/build.yml/badge.svg)](https://github.com/AnHeuermann/omc-diff/actions/workflows/buil.yml)

## Dependencies

  - Flex
  - C compiler
  - CMake

## Installation Windows

Use MSYS2 install the dependencies and run:

```bash
$ cmake -S . -B build -Wno-dev -G "MSYS Makefiles" -DCMAKE_INSTALL_PREFIX=$(pwd)/install
$ cmake --build build/ --target install
```

## Installation Linux

```bash
$ cmake -S . -B build -Wno-dev -G "Unix Makefiles" -DCMAKE_INSTALL_PREFIX=$(pwd)/install
$ cmake --build build/ --target install
```

## License

Source code taken from [github.com/OpenModelica/OpenModelica](https://github.com/OpenModelica/OpenModelica) under the [OSMC-License.txt](./OSMC-License.txt).
This work is licensed under GNU Affero General Public License version 3, see
[LICENSE.md](./LICENSE.md)


