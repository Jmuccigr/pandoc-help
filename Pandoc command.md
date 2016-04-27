#Tweaking the Pandoc command

I'm assuming here that you're using [LibreOffice](http://libreoffice.org/). If not, you'll have to find the appropriate directory for the command in #1 below.

1. Bonus: Since I'm keeping all my bibliography in one .bib file, I've added an alias to the pandoc command that includes that bibliography switch to specify the bibliography file and the citeproc command:

`alias pandoc='pandoc --reference-odt=/Users/username/Library/Application\ Support/LibreOffice/4/user/template/Your_template.ott --bibliography=~/Documents/My\ Library.json'`

1. I also use lots of Unicode characters outside the "normal" Latin range, so here's another switch to help with that (courtesy of the error latex threw when I fed it some Hebrew):

`alias pandoc='pandoc --latex-engine=xelatex --reference-odt=/Users/username/Library/Application\ Support/LibreOffice/4/user/template/Your_template.ott --bibliography=~/Documents/My\ Library.json'`