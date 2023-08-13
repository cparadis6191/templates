TARGET = graph

OUTPUT = ${TARGET}.svg

${OUTPUT}: ${TARGET}.gv
	dot -Tsvg ${TARGET}.gv -o${OUTPUT}

.PHONY: clean

clean:
	rm --force ${OUTPUT}
