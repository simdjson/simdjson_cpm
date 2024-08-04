# Simple demo of simdjson as a CMake dependency using CPM
[![VS17-CI](https://github.com/simdjson/simdjson_cpm/actions/workflows/visual_studio.yml/badge.svg)](https://github.com/simdjson/simdjson_cpm/actions/workflows/visual_studio.yml)

This repository is meant to serve as an example of how to use [simdjson](https://github.com/simdjson/simdjson) as a `CMake` dependency using CPM.

Usage:

```
cmake -B build
cmake --build build
```

It will build two binaries, one of which will use the static simdjson library.

Please refer to the main [simdjson](https://github.com/simdjson/simdjson) project for further documentation.
