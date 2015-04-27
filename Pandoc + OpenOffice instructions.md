---
title: Using pandoc templates
author: John Muccigrosso
---
 
# Instructions for setting up Pandoc and OpenOffice documents

I'm assuming here that you're using [LibreOffice](http://libreoffice.org/). If not, you'll have to find the appropriate directory for the command in #1 below. I'm also assuming you got Pandoc via [home-brew](http://brew.sh/). If not, you'll probably be using ~/.pandoc as your directory in #2.

* In the Pandoc command use "--reference-odt=/Users/username/Library/Application\ Support/LibreOffice/4/user/template/Your_template.ott" where Your_template.ott is the default template for new files (or another template if you want that).

## Method 1: Forking the master (preferred)

* Fork the pandoc-templates folder from jgm/pandoc-templates. This will allow incorporating future changes from the master branch and keep track of local changes as well.


## Method 2: Creating a local version
* Create a copy of Pandoc's built-in default.opendocument template file, which is in /usr/local/Cellar/pandoc/1.13.2/share/x86_64-osx-ghc-7.8.3/pandoc-1.13.2/data/templates/ in the homebrew version of Pandoc.
* Rename the old version of default.opendocument, so it's there as a backup. I used default.opendocument.orig.
* Put the copy of default.opendocument somewhere it won't get wiped out with upgrades to Pandoc.


## Finally

* Edit local default.opendocument to taste. (Mine has slots for more detailed author info, for example.)
* Symlink the copy into the Pandoc templates folder with the name default.opendocument. This will now replace the original copy.
* Make sure your OpenOffice template file has all the necessary styles that you named in default.opendocument.