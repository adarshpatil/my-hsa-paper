EPS := template.eps motivation-cpu-cache.eps motivation-gpu-cache.eps motivation-cpu.eps motivation-gpu.eps results-cpu.eps results-cpu-antt.eps results-cpu-speedup.eps results-gpu-antt.eps results-gpu-speedup.eps design-rbhblp.eps results-gpu.eps design-bigblock.eps results-bypass.eps results-large-bloom.eps results-system.eps results-weighted-speedup.eps results-comparison-cpu.eps results-comparison-gpu.eps results-128M-cpu.eps results-128M-gpu.eps results-ddr3-2133-cpu.eps results-ddr3-2133-gpu.eps results-2xbw-cpu.eps results-2xbw-gpu.eps


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
