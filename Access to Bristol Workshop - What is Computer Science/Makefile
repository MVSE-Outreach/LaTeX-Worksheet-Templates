PDFLATEX := pdflatex
TEXFILES := BigHexWorksheet.tex

.PHONY: all
all: document

.PHONY: document
document:
	$(PDFLATEX) $(TEXFILES)

.PHONY: check
check: wordcount

.PHONY: diff-since
diff-since:
	git latexdiff --math-markup=0 \
	              --bibtex \
	              --main $(TEXFILES) \
	              --latexpand $(TEXFILES) \
	              HEAD

.PHONY: wordcount
wordcount:
	echo "Word Count: `detex $(TEXFILES) | wc -w`"

.PHONY: clean
clean:
	@-rm -f *.bak \
	        *.toc \
	        *.aux \
	        *.log \
	        *.swp \
	        *.bbl \
	        *.blg \
	        *.loa \
	        *.lof \
	        *.lot \
	        *.out
