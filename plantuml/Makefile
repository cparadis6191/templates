TARGET = plantuml

OUTPUT = ${TARGET}.svg

${OUTPUT}: ${TARGET}.puml
	plantuml -tsvg ${TARGET}.puml

.PHONY: clean

clean:
	rm --force ${OUTPUT}
