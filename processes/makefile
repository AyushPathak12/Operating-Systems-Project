CC=gcc
HEADERS = consts.h parsing.h inventory.h
CFLAGS = -Wall -Wextra -lpthread -g
OBJECTS = server.o client.o

all: server client
	
server: server.o
	$(CC) server.o -o server $(CFLAGS)

server.o: server.c $(HEADERS) myshm.h
	$(CC) -c server.c -o server.o $(CFLAGS)

client: client.o
	$(CC) client.o -o client $(CFLAGS)

client.o: client.c $(HEADERS)
	$(CC) -c client.c -o client.o $(CFLAGS)

clean:
	-rm -f *.o server client
