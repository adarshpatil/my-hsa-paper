EPS := design-bigblock.eps design-rbhblp.eps motivation-cpu-cache.eps motivation-cpu.eps motivation-gpu.eps results-128M-cpu.eps results-128M-gpu.eps results-2xbw-cpu.eps results-2xbw-gpu.eps results-bypass.eps results-comparison-cpu.eps results-comparison-gpu.eps  results-cpu.eps  results-ddr3-2133-cpu.eps results-ddr3-2133-gpu.eps results-gpu.eps results-large-bloom.eps results-system.eps results-weighted-speedup.eps results-cpu-nodc.eps results-gpu-nodc.eps motivation-gpu-cache.eps motivation-bandwidth.eps results-pris.eps


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
