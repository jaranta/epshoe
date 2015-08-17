## Build EpGUMSHOE.

## Markdown extension (e.g. md, markdown, mdown).
MEXT = md

## All markdown files in the working directory
SRC = colophon.$(MEXT) introduction.$(MEXT) timeofeclipse.$(MEXT) character.$(MEXT) rules.$(MEXT) exsurgents.$(MEXT) designingscenarios.$(MEXT)

all:	EclipseSHOE.pdf

EclipseSHOE.pdf:	$(SRC)
	pandoc --table-of-contents --template=latex.template $(SRC) -o $@

clean:
	rm -f *.pdf 
