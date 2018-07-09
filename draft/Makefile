MD2TeX	= md2tex
LaTeX	= platex
DVI2PDF	= dvipdfmx
DVIFLAGS	= -f ~/.local/share/fonts/map/dvipdfmx/cid-x.map
PDF	= minibook.pdf

TeXDocs	= operations.tex redirections.tex

all:	$(PDF)

$(PDF):	minibook.tex $(TeXDocs)
	$(LaTeX) minibook.tex
	$(DVI2PDF) $(DVIFLAGS) minibook.dvi

minibook.tex:	$(TeXDocs)
	touch minibook.tex

%.tex:	%.md
	md2tex --as-part $<
