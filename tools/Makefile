CC=gcc
CFLAGS=-Wall -I../common
LDFLAGS=
TARGETS=upinfo upshell upload
COMMONOBJS=../common/up3d.o ../common/up3dcomm.o ../common/up3ddata.o
NCURSESLIBS=$(shell pkg-config --libs ncurses)

all: $(TARGETS)

upinfo: upinfo.c $(COMMONOBJS)
	$(CC) upinfo.c $(CFLAGS) $(LDFLAGS) $(COMMONOBJS) -lm -lusb-1.0 -o upinfo

upshell: upshell.c $(COMMONOBJS)
	$(CC) upshell.c $(CFLAGS) $(LDFLAGS) $(COMMONOBJS) -lm -lusb-1.0 $(NCURSESLIBS) -o upshell


upload: upload.c $(COMMONOBJS)
	$(CC) upload.c $(CFLAGS) $(LDFLAGS) $(COMMONOBJS) -lm -lusb-1.0 -o upload

clean:
	$(RM) $(TARGETS) *.o
