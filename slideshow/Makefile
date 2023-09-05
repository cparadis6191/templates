TARGET = slideshow

# beige blood moon serif sky white black league night simple solarized
THEME = solarized
# none fade slide convex concave zoom
TRANSITION = fade

FROM = --from=markdown $(TARGET).md
FFLAGS =

OUTPUT = $(TARGET).html

DIAGRAM_LUA = diagram.lua

TO = --to=revealjs --output=$(OUTPUT)
TFLAGS = --embed-resources --include-in-header=$(TARGET).css
TFLAGS += --lua-filter=$(DIAGRAM_LUA) --slide-level=2 --standalone
TFLAGS += --variable=theme=$(THEME) --variable=transition=$(TRANSITION)

DATE = --metadata=date:'$(shell date +'%B %d, %Y')'

$(OUTPUT): $(TARGET).md $(TARGET).css $(DIAGRAM_LUA) images/*
	pandoc $(FROM) $(FFLAGS) $(TO) $(TFLAGS) $(DATE)

$(DIAGRAM_LUA):
	curl --location --remote-name \
		https://raw.githubusercontent.com/pandoc-ext/diagram/v1.0.0/_extensions/diagram/$(DIAGRAM_LUA)

.PHONY: clean

clean:
	rm --force $(DIAGRAM_LUA) $(OUTPUT)
