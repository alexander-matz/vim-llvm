# About

This repository is a mirror of the `utils/vim` directory, containing files for filetype detection,
syntax highlighting, indentation for LLVM *.ll and *.td files.
I created this repository to allow easier installation using vim plugin managers like Plug etc.

All contents of this repository are taken directly and unmodified from the official LLVM repository, except
for the following files: `README.md`, `vimrc`, `CMakeLists.txt`.

# Installation

## Pathogen (https://github.com/tpope/vim-pathogen)

git clone https://github.com/alexander-matz/vim-llvm ~/.vim/bundle/vim-llvm

## Vundle (https://github.com/gmarik/vundle)

Plugin 'alexander-matz/vim-llvm'

## NeoBundle (https://github.com/Shougo/neobundle.vim)

NeoBundle 'alexander-matz/vim-llvm'

# Original Readme

This directory contains settings for the vim editor to work on llvm *.ll and
tablegen *.td files. It comes with filetype detection rules in the (ftdetect),
syntax highlighting (syntax), some minimal sensible default settings (ftplugin)
and indentation plugins (indent).

To install copy all subdirectories to your $HOME/.vim or if you prefer create
symlinks to the files here. Do not copy the vimrc file here it is only meant as an inspiration and starting point for those working on llvm c++ code.

Note: If you notice missing or incorrect syntax highlighting, please contact
<llvm-bugs [at] lists.llvm.org>; if you wish to provide a patch to improve the
functionality, it will be most appreciated. Thank you.

If you find yourself working with LLVM Makefiles often, but you don't get syntax
highlighting (because the files have names such as Makefile.rules or
TEST.nightly.Makefile), add the following to your ~/.vimrc:

  " LLVM Makefile highlighting mode
  augroup filetype
    au! BufRead,BufNewFile *Makefile*     set filetype=make
  augroup END
