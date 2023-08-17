TARGET = document

FROM = --from=markdown-implicit_figures ${TARGET}.md
FFLAGS =

OUTPUT = ${TARGET}.pdf
DIAGRAM_LUA = diagram.lua

DATE = --metadata=date:'$(shell date +'%B %d, %Y')'

TO = --to=pdf --output=${OUTPUT}
TFLAGS = --lua-filter=${DIAGRAM_LUA} --number-sections
TFLAGS += --variable=geometry:'top=1in,bottom=1in,left=1in,right=1in'

${OUTPUT}: ${TARGET}.md ${DIAGRAM_LUA} images/*
	pandoc ${FROM} ${FFLAGS} ${TO} ${TFLAGS} ${DATE}

${DIAGRAM_LUA}:
	curl --location --remote-name \
	https://raw.githubusercontent.com/pandoc-ext/diagram/v1.0.0/_extensions/diagram/${DIAGRAM_LUA}

.PHONY: clean

clean:
	rm --force ${DIAGRAM_LUA} ${OUTPUT}
