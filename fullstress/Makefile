NAME = equation
TEX = platex
BIB = pbibtex
DVI = dvipdfmx

all:$(NAME).pdf

$(NAME).pdf: $(NAME).dvi
	$(DVI) $<

$(NAME).dvi: $(NAME).tex $(NAME).bib
	$(TEX) $(NAME).tex
	$(BIB) $(NAME)
	$(TEX) $(NAME).tex
	$(TEX) $(NAME).tex

clean:
	rm -f *.aux *bbl *.blg *.dvi *.log *.toc *.lof *.lot *.out
