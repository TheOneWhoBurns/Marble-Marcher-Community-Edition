# Marble Marcher Mod

[![Build Status](https://travis-ci.org/jgoldfar/MarbleMarcher.svg?branch=master)](https://travis-ci.org/jgoldfar/MarbleMarcher)

## This branch is for tweaking the original source code with all kinds of stuff.

Marble Marcher is a video game demo that uses a fractal physics engine and fully procedural rendering to produce beautiful and unique gameplay unlike anything you've seen before.

The goal of the game is to reach the flag as quickly as possible.  But be careful not to
fall off the level or get crushed by the fractal!  There are 24 levels to unlock.

Download Link: https://codeparade.itch.io/marblemarcher

Video Explanation: https://youtu.be/9U0XVdvQwAI

## System Dependencies
* [Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page)
* [SFML 2.5.0](https://www.sfml-dev.org)
* [AntTweakBar](http://anttweakbar.sourceforge.net/doc/)
### MacOS
On macOS these can be conveniently installed using [Homebrew](https://brew.sh):

`brew install eigen sfml`

(Note that SFML might require a newer version than the one from Homebrew, in which case a manual installation is required)

Alternatively, [vcpkg](https://github.com/Microsoft/vcpkg) can be used:

`vcpkg install eigen3 sfml`
### Arch Linux
`sudo pacman -S eigen sfml git cmake make`



## Building
### MacOS
* `mkdir build && cd build`
* `cmake ..`
    * If you use `vcpkg`, add the flag `-DCMAKE_TOOLCHAIN_FILE=[path/to/vcpkg]/scripts/buildsystems/vcpkg.cmake`
* `cd ..`
* `cmake --build build`

Alternatively, one can use the platform-dependent build system, for example `Make`:

* `make -C build`
### Arch Linux
* `cd ~`
* `git clone https://github.com/HackerPoet/MarbleMarcher.git`
* `cd MarbleMarcher`
* `mkdir build && cd build`
* `cmake ..`
* `cd ..`
* `cmake --build build`
* `cp build/MarbleMarcher ./`


## Launching
* If running MarbleMarcher from a tarball and you see a message like

> ./MarbleMarcher: error while loading shared libraries: libsfml-graphics.so.2.5: cannot open shared object file: No such file or directory

You'll just need to run MarbleMarcher with the correct `LD_LIBRARY_PATH`:

```shell
LD_LIBRARY_PATH=`pwd`/usr/lib ./MarbleMarcher
```
