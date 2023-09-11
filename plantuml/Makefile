INPUTS ::= $(wildcard *.puml)
OUTPUTS ::= $(INPUTS:.puml=.svg)

all: $(OUTPUTS)

%.svg: %.puml
	plantuml -tsvg $^

.PHONY: clean

clean:
	rm --force $(OUTPUTS)
