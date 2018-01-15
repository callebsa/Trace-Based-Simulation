
TEX = $(wildcard *.tex)
BIB = thesis.bib
FIGS = $(wildcard figures/*)
FGA = $(wildcard frontpageAndAbstract/*)

.PHONY: frontpageAndAbstract thiesis all
all: 
	make build 
	make clean

thesis: $(TEX) $(BIB) $(FIGS) 
	latexmk -pdf -f thesis.tex

frontpageAndAbstract: 
	cd frontpageAndAbstract && latexmk -pdf -f frontpageAndAbstract.tex



build: 
	make frontpageAndAbstract 
	make thesis
	
clean:
	rm -f *.out *.log *.bcf *.toc *.run.xml frontpageAndAbstract.pdf
	cd frontpageAndAbstract/ && rm -f *.out *.log *.bcf *.toc *.run.xml frontpageAndAbstract.pdf

cleanAux:
	rm -f *.out *.log *.bcf *.toc *.run.xml frontpageAndAbstract.pdf
