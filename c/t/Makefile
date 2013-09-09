all: libxxx.a a.c
	gcc -I. libxxx.a -o a a.c

all1: libxxx.so a.c
	gcc -I. -L. -lxxx -o a a.c

libxxx.a: b.o
	ar r libxxx.a b.o

b.o: b.c
	gcc -I. -c -o b.o b.c

libxxx.so:
	gcc -I. -shared -fpic b.c -o libxxx.so

clean:
	rm *.o libxxx.* a