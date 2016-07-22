
TEXFILES = GenericWorksheet.tex 

all: document 

.PHONY: clean document

document:
	pdflatex $(TEXFILES)

check: wordcount

diff-since:
	git latexdiff --math-markup=0 -b --main $(TEXFILES) --latexpand $(TEXFILES) $(base) HEAD

wordcount:
	echo "Word Count: `detex $(TEXFILES) | wc -w`"

clean:
	rm -f *.bak *.toc *.aux *.log *.swp *.bbl *.blg *.loa *.lof *.lot *.out
