.PHONY: all clean

CFLAGS_EXTRA ?= -ggdb3 -fopenmp -O0 -std=c99 -Wall -Werror -Wextra
IN_EXT ?= .c
LIBS :=
OUT_EXT ?= .out

OUTS := $(addsuffix $(OUT_EXT), $(basename $(wildcard *$(IN_EXT))))

all: $(OUTS)

%$(OUT_EXT): %$(IN_EXT)
	$(CC) $(CFLAGS) $(CFLAGS_EXTRA) -o '$@' '$<' $(LIBS)

clean:
	rm -f *'$(OUT_EXT)'
