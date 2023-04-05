# OpenSim Creator: Dependencies <img src="textures/logo.svg" align="right" alt="OpenSim Creator Logo" width="128" height="128" />

> A collection of build scripts/patches for building OpenSim Creator's dependencies.

The objective of this repository is to build all of OpenSim Creator's dependencies from
source on each platform into a single standalone archive file that can be used with
`-DCMAKE_PREFIX_PATH` in OpenSim Creator's build. This removes the need for each dependency
to be installed system-wide, separately built, etc.

The reason this repository is separate from OpenSim Creator's main repository is because
dependencies change less frequently, and because it takes a long time (>1h) to build all
of OpenSim Creator's dependencies from source via CI. Separating the two means that this
repo's CI can build dependencies ahead-of-time for the main OpenSim Creator build.

# Building

Requires `cmake`, a build system (e.g. `make` on Linux), and a C/C++ compiler:

```bash
cmake -S . -B build-dir -DCMAKE_INSTALL_PREFIX=install-dir
cmake --build build-dir  # creates library folder structure in `install-dir`
```

# 🥰 Contributing

(see the Contributing section in OpenSim Creator's main repository and post issues etc. there)
