CC=gcc
CFLAGS=-Wall -I../common
LDFLAGS=
TARGETS=parse convg
all: $(TARGETS)

parse: parse.c
	$(CC) parse.c $(CFLAGS) $(LDFLAGS) -lm -o parse
convg: convg.c
	$(CC) convg.c $(CFLAGS) $(LDFLAGS) -lm -o convg

clean:
	$(RM) $(TARGETS) *.o
