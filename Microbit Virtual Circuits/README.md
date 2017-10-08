# LaTeX Template

## Makefile Dependencies
You'll need the following executables available on your `$PATH`:

* `pdflatex` (from TeX-live or a similar LaTeX distribution) for the
  `all` target.
* [`git-latex`](https://gitlab.com/git-latexdiff/git-latexdiff), for the `diff-since` target.
* `detex` (from TeX-live or a similar LaTeX distribution) for the `wordcount` target


## How to use this template for your workshop

* Copy the whole template directory and rename with your workshop name:
* `cp -r Template MySuperWorkshop`
* Aggregate your image files (if you have any) and place them in the
  `img` subdirectory.
* Edit `Session Preperation.tex` to list relevant information for
  workshop leader, helpers, teachers, etc
* Rename `GenericWorksheet.tex` to `MySuperWorkshop.tex`
* Edit `Makefile` so that `TEXFILES := GenericWorksheet.tex` now reads
  `TEXFILES := MySuperWorkshop.tex`
* Compile the LaTeX files to produce your PDF output by running `make`
