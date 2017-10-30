if HAVE_LYX
LYX_PDFS = \
  UsersGuide-EN.pdf \
  UsersGuide-CN.pdf

UsersGuide-EN.pdf : UsersGuide-EN.lyx
	lyx -f -e pdf2 $^

UsersGuide-CN.pdf : UsersGuide-CN.lyx
	lyx -f -e pdf4 $^

%.tex : %.lyx
	lyx -f -e pdflatex $<
endif

if HAVE_HEVEA
LYX_HTML = \
  UsersGuide-EN.html \
  UsersGuide-CN.html

%.html : %.tex
	hevea book.hva -s $<
	hevea book.hva -s $<
endif

dist_doc_DATA = GettingStart-CN.txt \
	GettingStart-EN.txt \
	performence.txt \
	zlog.conf \
	$(LYX_PDFS) \
	$(LYX_HTML)
