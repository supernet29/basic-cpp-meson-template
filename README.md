# The C++ Basic Template

## What is it?

This is the template of the project that using meson build system.

It also uses GTest for Unit testing framework.

## How to build the project?

This project uses `build/` as build directory.
Following code shows how to setup the project and then build the project.

```sh
meson setup build
meson compile -C build
```

## How to run the unit test?

Before to run the unit test, it considers the project is already setup with in `build/` as build directory.

```sh
meson test -C build
```
