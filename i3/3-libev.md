# Introduction to libev-4.33
Libev is a full-featured, high-performant event loop loosely modelled after
libevent.

## Package Information
- Download (HTTP): http://dist.schmorp.de/libev/libev-4.33.tar.gz
- Download md5sum: a3433f23583167081bf4acdd5b01b34f
- Download Size: 570K
- Build Size: 2.9M
- Build Time: 0.1 SBU

## libev Dependencies
### Required
  [cmake](https://www.linuxfromscratch.org/blfs/view/svn/general/cmake.html)
  [glibc](https://www.linuxfromscratch.org/lfs/view/development/chapter08/glibc.html)

## Installation of libev
Install libev by executing the following commands:
```Bash
mkdir -pv build && cd build

../configure        \
    --prefix=/usr  &&

make
```

Now as the ***root*** user:
```Bash
make install
```
