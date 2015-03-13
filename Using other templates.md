# Setting up pandoc to use other templates

## My set-up
1. pandoc via homebrew.
1. latex is basictex via homebrew casks. This gets installed in /usr/local/texlive/, but its home directory (found via `tlmgr conf` is '~/Library/texmf/tex/')

## Kevin Healy's templates

1. Symlink org-preamble-pdflatex.sty into the tex home dir (after pandoc complained upon trying to create pdf output) and then `sudo texhash`:
`ln -s ~/Documents/github/cloned/latex-custom-kjh/needs-org-mode/org-preamble-pdflatex.sty  ~/Library/texmf/tex/latex/`
Got some help from [here](http://stackoverflow.com/questions/1390828/how-do-i-install-a-latex-sty-file-on-osx).

1. Then install wrap fig via
`sudo tlmgr install wrap fig`. (This required an update to tlmgr itself via `tlmgr update --self`.)

1. Now memoir. (Instructions [here](http://www.ctan.org/tex-archive/macros/latex/contrib/memoir/).)
    1. First `tlmgr install memoir`.
    2. Then move to the memoir dir '' and ``.