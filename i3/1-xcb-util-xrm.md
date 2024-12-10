# Introduction to xcb-util-xrm-1.3
XCB utility functions for the X resource manager. xcb-util-xrm is separate from
the other XCB Utilities.

## Package Information
- Download (HTTP): https://github.com/Airblader/xcb-util-xrm/releases/download/v1.3/xcb-util-xrm-1.3.tar.bz2
- Download md5sum: 6b5249f1e4e4e1c5e367d894d27dd0c0
- Download Size: 328K
- Build Size: 2.7M
- Build Time: < 0.1 SBU

## xcb-util-xrm Dependencies
### Required
  [util-macros](https://www.linuxfromscratch.org/blfs/view/svn/x/util-macros.html),
  [xcb-util](https://www.linuxfromscratch.org/blfs/view/svn/x/xcb-util.html)

## Installation of xcb-util-xrm
Install xcb-util-xrm by executing the following commands:
```Bash
mkdir -pv build && cd build

../configure            \
    --prefix=/usr       \
    --disable-static   &&

make
```

Now as the ***root*** user:
```Bash
make install
```
