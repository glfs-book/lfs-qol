# Introduction to yajl-2.1.0
Yajl is yet another json library.

## Package Information
- Download (HTTP): https://github.com/lloyd/yajl/archive/refs/tags/2.1.0.tar.gz
- Download md5sum: 6887e0ed7479d2549761a4d284d3ecb0
- Download Size: 84K
- Build Size: 2.3M
- Build Time: < 0.1 SBU

## Additional Downloads
- Required patch: https://gitlab.archlinux.org/archlinux/packaging/packages/yajl/-/raw/main/yajl-2.1.0-CVE-2017-16516.patch
- Required patch: https://gitlab.archlinux.org/archlinux/packaging/packages/yajl/-/raw/main/yajl-2.1.0-CVE-2022-24795.patch
- Required patch: https://gitlab.archlinux.org/archlinux/packaging/packages/yajl/-/raw/main/yajl-2.1.0-memory_leak.patch

## yajl Dependencies
### Required
  [cmake](https://www.linuxfromscratch.org/blfs/view/svn/general/cmake.html)
  [glibc](https://www.linuxfromscratch.org/lfs/view/development/chapter08/glibc.html)

## Installation of yajl
As of writing, the last commit to yajl is almost a decade old. With time,
vulnerabilities have emerged. Fix these by applying a few patches:
```Bash
patch -Np1 -i ../yajl-2.1.0-CVE-2017-16516.patch
patch -Np1 -i ../yajl-2.1.0-CVE-2022-24795.patch
patch -Np1 -i ../yajl-2.1.0-memory_leak.patch
```

Install yajl by executing the following commands:
```Bash
mkdir -pv build && cd build

cmake \
    -D CMAKE_INSTALL_PREFIX=/usr    \
    -D CMAKE_BUILD_TYPE=Release     \
    -D BUILD_SHARED_LIBS=ON         \
    -D CMAKE_SKIP_INSTALL_RPATH=ON  \
    -W no-dev -G Ninja ..          &&

ninja
```

Now as the ***root*** user:
```Bash
ninja install
```

## Command Explanations
  `-D CMAKE_SKIP_INSTALL_RPATH=ON`: This switch makes cmake remove hardcoded
  library search paths (rpath) when installing a binary executable file or a
  shared library. This package does not need rpath once it's installed into the
  standard location, and rpath may sometimes cause unwanted effects or even
  security issues. 
