#
# Makefile -- xxx
#
# (c) 2017 Prof Dr Andreas Müller, Hochschule Rapperswil
#
all:	xxx-handout.pdf MathSem-yyy-xxx.pdf

include ../slides/Makefile.inc

SOURCES = common.tex slides.tex $(slides)

MathSem-yyy-xxx.pdf:	MathSem-yyy-xxx.tex $(SOURCES)
	pdflatex MathSem-yyy-xxx.tex

xxx-handout.pdf:	xxx-handout.tex $(SOURCES)
	pdflatex xxx-handout.tex

thumbnail:	thumbnail.jpg # fix1.jpg

thumbnail.pdf:	MathSem-yyy-xxx.pdf
	pdfjam --outfile thumbnail.pdf --papersize '{16cm,9cm}' \
		MathSem-yyy-xxx.pdf 1
thumbnail.jpg:	thumbnail.pdf
	convert -density 300 thumbnail.pdf \
                -resize 1920x1080 -units PixelsPerInch thumbnail.jpg

fix1.pdf:	MathSem-yyy-xxx.pdf
	pdfjam --outfile fix1.pdf --papersize '{16cm,9cm}' \
		MathSem-yyy-xxx.pdf 1
fix1.jpg:	fix1.pdf
	convert -density 300 fix1.pdf \
                -resize 1920x1080 -units PixelsPerInch fix1.jpg

