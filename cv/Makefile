# Build the CV. Requires a TeX distribution (MacTeX / TeX Live).
#
#   make        -- build CV_donghwan_kim.pdf
#   make install-- build and copy the PDF to ../files/ (what the website serves)
#   make clean  -- remove LaTeX auxiliary files

TEX  = CV_donghwan_kim.tex
PDF  = $(TEX:.tex=.pdf)
DEST = ../files/CV_donghwan_kim.pdf

.PHONY: all install clean

all: $(PDF)

$(PDF): $(TEX)
	latexmk -pdf -interaction=nonstopmode -halt-on-error $(TEX)

install: $(PDF)
	cp $(PDF) $(DEST)

clean:
	latexmk -C
