CC = gcc # compiler
FLAGS = -Wall -g # compilation flags
TARGETS = Sniffer Spoofer Sniff_and_spoof Gateway # exe targets

.PHONY: all clean

all: $(TARGETS)

Sniffer: Sniffer.o
	$(CC) $(FLAGS) -o Sniffer Sniffer.o -lpcap
Sniffer.o: Sniffer.c 
	$(CC) $(FLAGS) -c Sniffer.c
Spoofer: Spoofer.o
	$(CC) $(FLAGS) -o Spoofer Spoofer.o
Spoofer.o: Spoofer.c
	$(CC) $(FLAGS) -c Spoofer.c
Sniff_and_spoof: sniff_and_spoof.o
	$(CC) $(FLAGS) -o Sniff_and_spoof sniff_and_spoof.o -lpcap
sniff_and_spoof.o: sniff_and_spoof.c
	$(CC) $(FLAGS) -c sniff_and_spoof.c
Gateway: gateway.o
	$(CC) $(FLAGS) -o Gateway gateway.o 
gateway.o: gateway.c
	$(CC) $(FLAGS) -c gateway.c
clean:
	rm -f *.o *.h.gch $(TARGETS)
