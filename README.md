# Template C++ Project [Name]:

### Requirements

- [Cmake](https://cmake.org/download/) higher than `v3.28`;
- [Ninja](https://ninja-build.org/);
- C++ compiler:
  - Windows - [Clang](https://clang.llvm.org/get_started.html);
  - Linux - [gcc](https://gcc.gnu.org/);

#### Ubuntu 24.04:

```
sudo apt update
sudo apt install cmake ninja-build gcc g++
```

NOTE: Ubuntu 22.04 comes with cmake `v3.22` which does not include cmake presets, please update your cmake version.

#### Fedora 42

```
sudo dnf install cmake ninja-build gcc g++
```

NOTE: Make sure to run the `preset` command with `sudo`.

## Building and running the project

Two presets are provided, one for windows `windows-clang` and one for `linux`.

- List the presets available with `cmake --list-presets`;
- Run the project configure step with `cmake --preset <preset>`;
- Build the project `cmake --build --preset <preset>`;
- Run the main executable `./build/<preset>/bin/project_name` (Add the file extension `.exe` on Windows).
- Testing `ctest --preset <preset>`
