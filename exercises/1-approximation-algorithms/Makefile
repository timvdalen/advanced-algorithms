LATEX = pdflatex
LATEXOPTS = -interaction=nonstopmode -halt-on-error -shell-escape
DOC = report

all: once.a

.SECONDARY:

exercises/II/%.eps: exercises/II/%.dot
	dot $< -Teps -o $@

cleandot:
	rm -f exercises/II/*.eps exercises/II/*-eps-converted-to.pdf

once.%: $(patsubst %,exercises/II/%.eps, 1-opt-cover 1-alg-cover 1-opt-independent 1-alg-independent)
	$(LATEX) $(LATEXOPTS) $(DOC)

clean: cleandot
	rm -f $(DOC).{aux,log,toc,out,bbl,blg}

remove: clean
	rm -f $(DOC).pdf

release: remove once.a once.b once.c
