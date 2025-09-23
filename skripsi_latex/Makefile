# Simple Makefile to build LaTeX on Ubuntu with separated outputs
# Usage:
#   make pdf        # build PDF to skripsipdf/skripsigtkrshnaaa.pdf; aux to dist/
#   make clean      # remove auxiliary files inside dist/ but keep PDF
#   make distclean  # remove dist/ only (PDF kept); use 'make clobber' to remove PDF dir

DOC=main
BUILDDIR=dist
PDFDIR=skripsipdf
PDFNAME=skripsigtkrshnaaa.pdf

dirs:
	mkdir -p $(BUILDDIR) $(PDFDIR)

pdf: dirs
	pdflatex -interaction=nonstopmode -halt-on-error -output-directory=$(BUILDDIR) $(DOC).tex
	-bibtex $(BUILDDIR)/$(DOC)  # ignore failure if no citations yet
	pdflatex -interaction=nonstopmode -halt-on-error -output-directory=$(BUILDDIR) $(DOC).tex
	pdflatex -interaction=nonstopmode -halt-on-error -output-directory=$(BUILDDIR) $(DOC).tex
	cp -f $(BUILDDIR)/$(DOC).pdf $(PDFDIR)/$(PDFNAME)
	@echo "PDF generated at: $(PDFDIR)/$(PDFNAME)"

clean:
	@echo "Cleaning auxiliary files in $(BUILDDIR)/ ..."
	@rm -f $(BUILDDIR)/*.aux $(BUILDDIR)/*.bbl $(BUILDDIR)/*.blg $(BUILDDIR)/*.log \
	  $(BUILDDIR)/*.out $(BUILDDIR)/*.toc $(BUILDDIR)/*.lof $(BUILDDIR)/*.lot \
	  $(BUILDDIR)/*.synctex.gz $(BUILDDIR)/*.nav $(BUILDDIR)/*.snm $(BUILDDIR)/*.fls \
	  $(BUILDDIR)/*.fdb_latexmk

distclean:
	@echo "Removing build directory $(BUILDDIR)/ ..."
	@rm -rf $(BUILDDIR)

clobber:
	@echo "Removing build and PDF directories ..."
	@rm -rf $(BUILDDIR) $(PDFDIR)
