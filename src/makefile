CC=gcc

CFLAGS=-s -g -Wall -D_GNU_SOURCE=1 -D_REENTRANT -pedantic -lm
IMAGE_FLAGS=-lSDL2_image
MIXER_FLAGS=-lSDL2_mixer
FONTS_FLAGS=-lSDL2_ttf
SFLAGS=-lSDL2
SOURCES=main.c functions.c global.c
OBJECTS=main.o functions.o global.o
BINARIES=breakout

all: $(BINARIES)

breakout: main.o functions.o global.o
	$(CC) -o breakout main.o functions.o global.o $(CFLAGS) $(SFLAGS) $(IMAGE_FLAGS) $(MIXER_FLAGS) $(FONTS_FLAGS)

main.o: main.c
	$(CC) -c main.c $(CFLAGS) $(SFLAGS) $(IMAGE_FLAGS) $(MIXER_FLAGS) $(FONTS_FLAGS)

funcoes.o: functions.c
	$(CC) -c functions.c $(CFLAGS) $(SFLAGS) $(IMAGE_FLAGS) $(MIXER_FLAGS) $(FONTS_FLAGS)

globais.o: global.c
	$(CC) -c global.c $(CFLAGS) $(SFLAGS) $(IMAGE_FLAGS) $(MIXER_FLAGS) $(FONTS_FLAGS)

clean:
	rm -rf *.o *.exe *.bak *.c~ $(BINARIES) core a.out
