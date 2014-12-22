## Build EpGUMSHOE scenarios. Requires the appropriate templates in the pandoc data folder.

## Markdown extension (e.g. md, markdown, mdown).
MEXT = md

## All markdown files in the working directory
SRC = $(wildcard *.$(MEXT))

## Location of Pandoc support files.
PREFIX = $(shell eval echo ~$$USER)/.pandoc

PDFS=$(SRC:.md=.pdf)
HTML=$(SRC:.md=.html)


all:	$(PDFS) $(HTML) 

pdf:	clean $(PDFS)
html:	clean $(HTML)

%.html:	%.md
	pandoc -t html5 -S -s --template=$(PREFIX)/templates/html.template --css=$(PREFIX)/.css/epgumshoe.css -o $@ $<

%.pdf:	%.md
	pandoc -S --table-of-contents --template=$(PREFIX)/templates/latex.template -o $@ $<

clean:
	rm -f *.html *.pdf 
