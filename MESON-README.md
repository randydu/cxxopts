# Meson build for CXXOPTS (a lightweight C++ option parser library)

URL: 

- [Github: cxxopts](https://github.com/randydu/cxxopts.git);
- [The Meson Build system](https://mesonbuild.com/index.html);

unit-tests are not built as part of the meson-build.

## Versions

The "revision" of cxxopts.wrap and the version of this meson-build project matches the embedded submodule cxxopts version as following:

meson-cxxopts |  cxxopts 
------------|-----------
3.1         | v3.1.1


## Usage

copy cxxopts.wrap to "subprojects" sub-folder of your main project directory.


in meson.build:

```
# import

cxxopts_dep = dependency('cxxopts')

# use
srcs = ['main.cpp', ...]

executable('test', srcs, dependencies: [cxxopts_dep, ...])

```

in main.cpp:

```cpp
#include <cxxopts.hpp>

int main(int argc, char* argv[]){
  cxxopts::Options options("test", "A brief description"); 
  ...
}
```



