CFLAGS  := -O3 -Wall -Werror -Wno-unused-result -I ../libhrd/
LD      := gcc -O3
LDFLAGS := ${LDFLAGS} -libverbs -lrt -lpthread -lmemcached -lnuma

APPS    := main

all: ${APPS}

main: ../libhrd/hrd_conn.o ../libhrd/hrd_util.o main.o
	${LD} -o $@ $^ ${LDFLAGS}

PHONY: clean
clean:
	rm -f *.o ../libhrd/*.o ${APPS}
