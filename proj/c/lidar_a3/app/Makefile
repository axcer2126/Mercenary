PWD = $(shell pwd)

INC_DIRS += -I$(PWD)/../ds

LIBS = -lm

SRCS = $(wildcard *.c)
OBJS = $(SRCS:%.c=%.o)

LIB_DIR = $(PWD)/../ds
LIB_OBJS = $(shell find $(LIB_DIR) -name '*.o')

TARGET = main

all: $(OBJS)
all: $(TARGET)

$(TARGET): $(OBJS)
custom_vector_test: main.o
	$(CC) -o $@ $< $(LIB_OBJS) $(LIBS)

.c.o:
	@echo "**********************************"
	@echo "********** Main Program **********"
	@echo "**********************************"
	$(CC) -c $< -o $@ $(INC_DIRS)

clean:
	rm -rf *.o
	rm -rf $(TARGET)
