# Makefile

CC=/usr/bin/cc
OBJ_COMMON = ili9340.o xpt2046.o fontx.o
OBJ_TEST1 = ili9341_test1.o 
TEST1=ili9341_test1

LDFLAGS =  -lbcm2835 -lm -DBCM
CFLAGS =
CPPFLAGS =
DEFS =
HEADERS = ili9340.h xpt2046.h xfont.h

$(TEST1): $(OBJ_TEST1) $(OBJ_COMMON)
	$(CC) $(LDFLAGS) $(OBJ_TEST1) -o $@

.c.o: $(HEADERS) 
	$(CC) -c $(DEFS) $(CPPFLAGS) $(CFLAGS) $< -o $@

