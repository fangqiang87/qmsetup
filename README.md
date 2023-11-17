# QtMediate CMake Modules

CMake Modules for QtMediate and other projects.

This project is independent from Qt and other 3rdparty libraries. Due to the fact that it encompasses some tools that need to be compiled, it cannot be included as a subproject.

## Support Platforms

+ Microsoft Windows
+ Apple Macintosh
+ GNU/Linux

## Dependencies

### Required Packages

Windows deploy command acquires the shared library paths by reading the PE files and searching the specified paths so that it doesn't depend on `dumpbin` tool.

Unix deploy command acquires the shared library paths by running `ldd`/`otool` command and fixes the *rpath*s by runing the `patchelf`/`install_name_tool` command, make sure you have installed them.

```sh
sudo apt install patchelf
```

### Open-Source Libraries
+ https://github.com/SineStriker/syscmdline
+ https://github.com/jothepro/doxygen-awesome-css

## Integrate

### Clone

Via Https
```sh
git clone --recursive https://github.com/SineStriker/qtmediate-cmake-modules.git
```
Via SSH
```sh
git clone --recursive git@github.com:SineStriker/qtmediate-cmake-modules.git
```

### Build & Install
```sh
cmake -B build -DCMAKE_INSTALL_PREFIX=/path/to
cmake -B build --target all
cmake -B build --target install
```

### Import
```sh
cmake -DqtmediateCM_DIR=/path/to/lib/cmake/qtmediateCM ...
```
```cmake
# CMakeLists.txt
find_package(qtmediateCM REQUIRED)
```

## Thanks

+ RigoLigoRLC
+ CrSjimo
+ wangwenx190