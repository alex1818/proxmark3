VPATH = ../../common ../../common/crapto1 ../../client
CC = gcc
LD = gcc
CFLAGS = -std=c99 -D_ISOC99_SOURCE -I../../common -I../../client -Wall -O3
LDFLAGS =

OBJS = crypto1.o crapto1.o parity.o util.o mfkey.o
EXES = mfkey32 mfkey64
WINEXES = $(patsubst %, %.exe, $(EXES))

all: $(OBJS) $(EXES)

%.o : %.c
	$(CC) $(CFLAGS) -c -o $@ $<

% : %.c $(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $(OBJS) $<

clean: 
	rm -f $(OBJS) $(EXES) $(WINEXES)
