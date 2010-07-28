CC = gcc
CFLAGS=-Wall -std=c99

DESTDIR=

all:
	$(CC) $(CFLAGS) io-pef.c  -o libpixbufloader-pef.so \
		`pkg-config --cflags gtk+-2.0` \
		-shared -fpic -DGDK_PIXBUF_ENABLE_BACKEND

clean:
	rm libpixbufloader-pef.so

install:
	chmod 644 libpixbufloader-pef.so
	mkdir -p $(DESTDIR)/usr/lib/gtk-2.0/2.10.0/loaders/
	cp libpixbufloader-pef.so $(DESTDIR)/usr/lib/gtk-2.0/2.10.0/loaders/

