TEXFILES=$(shell find preamble -type f -name "*.tex") $(shell find content -type f -name "*.tex") $(shell find conclusion -type f -name "*.tex")

index.pdf: index.tex $(TEXFILES)
	mkdir -p ./dist
	pdflatex --output-directory=./dist -interaction=nonstopmode --no-pdf index.tex
	pdflatex --output-directory=./dist -interaction=nonstopmode index.tex
	mv ./dist/index.pdf ./index.pdf

clean:
	rm -r dist index.pdf