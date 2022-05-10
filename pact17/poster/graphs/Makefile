EPS := motivation-cpu-cache.eps  motivation-cpu.eps  motivation-gpu-cache.eps  motivation-gpu.eps  results-cpu.eps  results-gpu.eps

all: $(EPS) 

PDFS := $(EPS:.eps=.pdf)

pdf: $(PDFS)

#%.eps: %.gnu %.dat
	#gnuplot $<
	
%.pdf: %.eps
	epstopdf $<

#%.eps: results.plot *.dat
#	gnuplot $<

#%.eps: %.plot summary.dat
#	gnuplot $<

%.eps: %.tex barcolors.tex
	pdflatex $<
	pdftops -eps $*.pdf

clean:
	rm -f *.pdf *.eps *.aux *.log

cleaner:
	rm -f *.pdf *.aux *.log
