CC=g++
CFLAGS=-Wall -std=c++11

BUILD=./build
TARGET=$(BUILD)/in1weekend
SRC=./src
SRCS=$(SRC)/*.cpp
INC=-I./include
OBJS=$(SRCS:.cpp=.o)

$(TARGET): $(OBJS)
	$(CC) -o $@ $^
	rm -rf $^

%.o: %.cpp
	$(CC) $(CFLAGS) $(INC) -o $@ -c $<

clean:
	rm -rf $(TARGET) $(OBJS)