SRCS = frontseite.tex \
       heldendokument.tex \
       kampfbogen-konfig.tex \
       kampfbogen.tex \
       talentbogen-konfig.tex \
       talentbogen.tex


all: heldendokument.pdf

heldendokument.pdf: ${SRCS} talentbogen-extern.tex
	xelatex heldendokument.tex
	rm -rf *.log *.out *.aux

talentbogen-extern.tex: talente.py talente.yaml
	./talente.py

clean:
	rm talentbogen-extern.tex heldendokument.pdf