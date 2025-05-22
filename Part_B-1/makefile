TEX=pdflatex
BIB=bibtex

FLG=-shell-escape -synctex=1 


TITLE  = Part_B-1


#make the pdf
all:  $(TITLE).pdf

#run pdflatex and bibtex (runs only if you update something in pdfs or in the tex file)
$(TITLE).pdf:  $(TITLE).tex ./refs.bib
	$(TEX) $(FLG) $< 
	$(TEX) $(FLG) $< 
	$(BIB) $(TITLE) || true
	$(TEX) $(FLG) $< 
	$(TEX) $(FLG) $< 

	#remove all output except the pdf file
	rm -f *.aux 
	rm -f *.log 
	rm -f *.out 
	rm -f *.bbl 
	rm -f *.toc 
	rm -f *.blg 
	rm -f *-blx.bib 
	rm -f *.xml 
clean:
	rm -f $(OUT)
	rm -f *.aux 
	rm -f *.log 
	rm -f *.out 
	rm -f *.bbl 
	rm -f *.blg 
	rm -f *.toc 
	rm -f *.synctex.gz
	rm -f *-blx.bib 
	rm -f *.xml 
	rm -f $(TITLE).pdf
