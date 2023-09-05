INPUTS = $(wildcard *.gv)
OUTPUTS = $(INPUTS:.gv=.svg)

all: $(OUTPUTS)

%.svg: %.gv
	dot -Tsvg $^ -o$@

.PHONY: clean

clean:
	rm --force $(OUTPUTS)
