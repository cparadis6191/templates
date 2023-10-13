INPUTS ::= $(wildcard *.puml)
OUTPUTS ::= $(INPUTS:.puml=.png) $(INPUTS:.puml=.svg)

all: $(OUTPUTS)

%.png: %.puml
	plantuml -tpng $^

%.svg: %.puml
	plantuml -tsvg $^

.PHONY: clean

clean:
	rm --force $(OUTPUTS)
