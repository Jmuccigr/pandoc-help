#Instructions for setting up Pandoc and OpenOffice documents

1. In the Pandoc command use "--reference-odt=/Users/john_muccigrosso/Library/Application\ Support/LibreOffice/4/user/template/Your_template.ott" where Your_template.ott is the default template for new files (or another template if you want that).

2. Create a copy of Pandoc's built-in default.opendocument template file, which is in /usr/local/Cellar/pandoc/1.13.2/share/x86_64-osx-ghc-7.8.3/pandoc-1.13.2/data/templates/ in the homebrew version of Pandoc.

3. Rename the old version of default.opendocument, so it's there as a backup. I used default.opendocument.orig.

4. Put the copy of default.opendocument somewhere it won't get wiped out with upgrades to Pandoc. I used my github folder so I can share it.

5. Edit the copy to taste.

6. Symlink the copy into the Pandoc templates folder with the name default.opendocument. This will now replace the original copy (which you renamed, so you still have it).

7. Make sure your OpenOffice template file has all the necessary styles that you named in default.opendocument.

8. Bonus: Since I'm keeping all my bibliography in one .bib file, I've added an alias to the pandoc command that includes that file and the citeproc command:
`alias pandoc=pandoc --reference-odt=/Users/john_muccigrosso/Library/Application\ Support/LibreOffice/4/user/template/Your_template.ott --bibliography=~/Documents/My\ Library.bib`