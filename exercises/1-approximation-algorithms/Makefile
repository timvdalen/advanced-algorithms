LATEX = pdflatex
LATEXOPTS = -interaction=nonstopmode -halt-on-error -shell-escape
DOC = report

all: once.a

once.%:
	$(LATEX) $(LATEXOPTS) $(DOC)

clean:
	rm -f $(DOC).{aux,log,toc,out,bbl,blg}

remove: clean
	rm -f $(DOC).pdf

release: remove once.a once.b once.c
