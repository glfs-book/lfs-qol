[Home](../)

[Prev: pkgsuite](./8-pkgsuite.md)

***

# Introduction to heirloom-ex-vi-bd1f88
Heirloom-ex-vi, also known as The Traditional Vi, is a portable version of 2.11BSD/SVR4 vi.

## Package Information
- Download (HTTP): https://github.com/n-t-roff/heirloom-ex-vi/archive/bd1f886598d20d457885c5c189fea34b027cbdef.zip
- Download md5sum: 4b533b4ff07b42a06b2bd51e6132c761
- Download Size: 372K
- Build Size: 2.5M
- Build Time: less than 0.1 SBU

## Additional Download
- Required patch: [heirloom-ex-vi-bd1f88-paths.patch](./patches/heirloom-ex-vi/heirloom-ex-vi-bd1f88-paths.patch)

## Package Dependencies
### Required
  [UnZip](https://www.linuxfromscratch.org/blfs/view/svn/general/unzip.html) (to unpack the distribution)

### Optional
  [The X Window System](https://www.linuxfromscratch.org/blfs/view/svn/x/installing.html) (to use wvi)

## Installation of heirloom-ex-vi
Optionally, before unpacking, move the distribution zipfile to a more sensible name:
```Bash
mv bd1f886598d20d457885c5c189fea34b027cbdef.zip heirloom-ex-vi-bd1f88.zip
```

It is of note that, during extraction, you may get the following error message:
```
lchmod (file attributes) error: Operation not supported
```
You may ignore said error message, everything is fine. The error message is being caused by an attempt
to set the file attributes on a symbolic link, which are ignored on most Unix and Unix-like systems, a
notable exception being macOS.

Apply a patch to make the installation paths conform with the others in this category:
```Bash
patch -Np1 -i ../heirloom-ex-vi-bd1f88-paths.patch
```

Compile heirloom-ex-vi by following the commands below:
```Bash
./configure &&
make
```

Now as the ***root*** user:
```Bash
make install
```

## Configuration of heirloom-ex-vi

The editor can be configured via the file ``~/.exrc``. The defaults are fine, but it is of note that
the configuration file gets ignored if anyone except the user executing vi has the ability to write
to it. Make sure your ``~/.exrc`` is ``chmod 644`` or similar in case you want to use it.
