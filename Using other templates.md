# Setting up pandoc to use other templates

## My set-up
1. pandoc via homebrew.
1. latex is basictex via homebrew casks. This gets installed in /usr/local/texlive/, but its home directory (found via `tlmgr conf` is '~/Library/texmf/tex/')

## Kevin Healy's templates

1. Symlink org-preamble-pdflatex.sty into the tex home dir (after pandoc complained upon trying to create pdf output):
`ln -s ~/Documents/github/cloned/latex-custom-kjh/needs-org-mode/org-preamble-pdflatex.sty  ~/Library/texmf/tex/latex/`
Then `sudo texhash`.
Got some help from [here](http://stackoverflow.com/questions/1390828/how-do-i-install-a-latex-sty-file-on-osx).

1. Install wrapfig via
`sudo tlmgr install wrap fig`. (This required an update to tlmgr itself via `tlmgr update --self`.)

1. Now it's complaining about a missing memoir-article-style.sty: `ln -s ~/Documents/github/cloned/latex-custom-kjh/needs-memoir/memoir-article-styles.sty ~/Library/texmf/tex/latex/`.

1. Next up csquotes package: `sudo tlmgr install csquotes`.

1. Now the soul package: `sudo tlmgr install soul`.

1. Tricky installing the Minion fonts. Follow directions [here](http://jklukas.blogspot.com/2010/02/installing-minionpro-tex-package.html) with all the corrections at bottom. Got enc.2.0.3.0 from [here](http://comments.gmane.org/gmane.comp.tex.minionpro/58).

sudo tlmgr install biblatex-chicago

sudo tlmgr install biblatex

sudo tlmgr install logreq

vc from [here](http://ctan.mirrorcatalogs.com/help/Catalogue/entries/vc.html).