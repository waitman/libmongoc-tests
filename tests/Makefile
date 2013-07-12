CC?=		clang
CFLAGS?=	-O2
PREFIX?=	/usr/local

all: libmongoc-tests

libmongoc-tests:
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I. -I$(PREFIX)/include -o test-mongoc-array test-mongoc-array.c -L$(PREFIX)/lib -lmongoc -lbson
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-buffer test-mongoc-buffer.c
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-client-pool test-mongoc-client-pool.c
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-collection test-mongoc-collection.c
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-list test-mongoc-list.c
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-queue test-mongoc-queue.c
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-rpc test-mongoc-rpc.c
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-uri test-mongoc-uri.c
	$(CC) -DBSON_BYTE_ORDER=1234 $(CFLAGS) -I./ -I$(PREFIX)/include $(PREFIX)/lib/libbson.a $(PREFIX)/lib/libmongoc.a -o test-mongoc-write-concern test-mongoc-write-concern.c

clean:
	rm -f test-mongoc-array
	rm -f test-mongoc-buffer
	rm -f test-mongoc-client-pool
	rm -f test-mongoc-collection
	rm -f test-mongoc-list
	rm -f test-mongoc-queue
	rm -f test-mongoc-rpc
	rm -f test-mongoc-uri
	rm -f test-mongoc-write-concern

run:
	./test-mongoc-array
	:
	./test-mongoc-buffer
	:
	./test-mongoc-client-pool
	:
	./test-mongoc-collection
	:
	./test-mongoc-list
	:
	./test-mongoc-queue
	:
	./test-mongoc-rpc
	:
	./test-mongoc-uri
	:
	./test-mongoc-write-concern

