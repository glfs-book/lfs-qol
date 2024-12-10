# lfs-qol (Linux From Scratch - Quality of Life)

This repository is dedicated to documenting the installation of some packages
on an LFS system that do not appear in LFS, MLFS, BLFS, and GLFS.

This project also assumes you are using a SysVinit LFS system.

Such packages that are included are, but not limited to:
- Fuse-2.9.9 (needed for appimages)
- Flatpak
- Hyprland
- i3

# Where to read

Each folder in this repo is a category or dedicated to installing a single
package but require multiple packages before being able to install the package
at the end.

Navigate to a folder and you should see multiple `.md` (Markdown) files. Github
should display the included README.md in each folder, displaying info on what
the category/folder is about. If you have cloned this repo, you will have to
view the `README.md` manually. Each `.md` file in each folder will be numbered,
all except the `README.md`. This means you should follow each `.md` file
numerically as they may build on each previous one. Each `README.md` will go in
depth about it. When viewing on Github, each file should be styled correctly.

# Standards

As stated above, each file is a Markdown file. The exceptions are Git specific
files and the licenses. If you are viewing these files not on Github, you will
see how the files themselves are laid out in a text format. Please read
https://www.markdownguide.org/basic-syntax/ to find out what each symbol is
supposed to mean and do.

Another standard is that each line is limited to 80 maximum characters long.

The last standard is each markdown file follows the same format as the LFS
books:
- Package introduction
- Package information, including download links
- Add users if necessary
- Apply patches if necessary
- Build package
- Install package
- Configuration if necessary

# Licenses

The three licenses are named `MIT0-LICENSE`, `BLFS-LICENSE`, and `CC-LICENSE`
(MIT0, BLFS' MIT, and Creative Commons Attribution-NonCommercial-ShareAlike 2.0
respectively)
