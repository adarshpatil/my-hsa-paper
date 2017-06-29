PAPER=thesis

default: paper

paper:
	pdflatex $(PAPER).tex 
	bibtex $(PAPER)
	pdflatex $(PAPER).tex
	pdflatex $(PAPER).tex
	pdflatex $(PAPER).tex

tidy:
	rm -f $(PAPER).aux $(PAPER).bbl $(PAPER).blg $(PAPER).brf $(PAPER).btx $(PAPER).log $(PAPER).out

clean: tidy
	rm -f $(PAPER).pdf
