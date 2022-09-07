# getting-started-guides

This repository contains notes on getting started guides to various software tools for the Brooklyn College CIS student.

The webpage page is available at [guides.drkat.dev](https://guides.drkat.dev)

---

# Build info

The contents of this site is written in emacs' org mode, converted to markdown with ox-hugo, and generated to a static html site using hugo.

At the time of this writing, the following are used to build this site:

* Emacs 27.1
  * Org mode
  * [Ox-hugo](https://ox-hugo.scripter.co/) mode
* Hugo v0.75.1
  * book theme

## Installation and setup

Instructions for installing Hugo can be found at https://gohugo.io/getting-started/installing/

* mac `brew install hugo`

Install the book theme using `git submodule update --init --recursive`

## File Directory

At the highest level, files are organized into 3 directories. 

- The `docs` folder is used by github pages to build the site. 
- The `hugo` folder contains the configuration and theme files used by hugo to generate the website.
- The `notes` folder contains the org files with the text for each of the pages.

``` shell
├── docs
├── hugo
└── notes
```

## Common commands

1. Publish the org file to markdown in emacs, using keybinding `C-c C-e H h` as this will save the file into the correct format in the `content` directory. 
2. In the terminal, start the hugo server from the hugo folder to preview the website for changes `hugo server` while in development. Using the `-D` flag will include drafts to in the preview.
3. Once the site looks good, generate the files with `hugo -D`, this will prepare the subdirectory `hugo/public` with the resulting website.
4. Copy the files over from `hugo/public` to `docs` to prepare for github pages. Sample command used: `rm -r docs && mkdir docs && cp -r hugo/public/* docs`

---

# Hugo Configurations

Currently the configurations are in `hugo/config.toml` and `hugo/data/config/widgets.toml` are required for building the website and not added to this repository.

