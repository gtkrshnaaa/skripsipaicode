# Simple Makefile to build LaTeX on Ubuntu
# Usage:
#   make pdf   # build PDF with pdflatex + bibtex (2-pass)
#   make clean # remove auxiliary files

DOC=main

pdf:
	pdflatex $(DOC).tex
	bibtex $(DOC) || true
	pdflatex $(DOC).tex
	pdflatex $(DOC).tex

clean:
	rm -f *.aux *.bbl *.blg *.log *.out *.toc *.lof *.lot *.synctex.gz *.toc
