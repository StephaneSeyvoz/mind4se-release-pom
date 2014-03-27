EXAMPLES = $(patsubst %/,%, $(sort $(dir $(wildcard */))))

all: $(EXAMPLES:%=%.all)
clean: $(EXAMPLES:%=%.clean)

%.all:
	$(MAKE) -C $(@:%.all=%) all

%.clean:
	$(MAKE) -C $(@:%.clean=%) clean
