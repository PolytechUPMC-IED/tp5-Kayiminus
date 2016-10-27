SLIB =  printer.c pbm2eps9.c
CC = gcc
CFLAGS = -O3 -Wall -funroll-loops
LDLIBS = -lpng
all : pbm2png.c pbm2eps9.o
	$(CC) $(CFLAGS) -s -o pbm2png pbm2png.c $(LDLIBS)
	$(CC) -s -o pbm2eps9 pbm2eps9.o printer.o

#pbm2eps9.o: pbm2eps9.c printer.h
#	  $(CC) $(CFLAGS) -c -o pbm2eps9.o pbm2eps9.c 

#printer.o: printer.c
#	$(CC) $(CFLAGS) -c -o printer.o printer.c 


%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $<


clean:
	rm -f pbm2eps9.o printer.o pbm2png pbm2eps
