## Build EpGUMSHOE. Requires the appropriate templates in the pandoc data folder.

## Markdown extension (e.g. md, markdown, mdown).
MEXT = md

## All markdown files in the working directory
SRC = colophon.$(MEXT) introduction.$(MEXT) timeofeclipse.$(MEXT) character.$(MEXT) rules.$(MEXT) designingscenarios.$(MEXT)

## Location of Pandoc support files.
PREFIX = $(shell eval echo ~$$USER)/.pandoc

all:	EclipseSHOE.pdf

EclipseSHOE.pdf:	$(SRC)
	pandoc --table-of-contents --template=$(PREFIX)/templates/latex.template $(SRC) -o $@

clean:
	rm -f *.pdf 
