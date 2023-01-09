BUILD_DIR := build
SRC_DIRS := src

TARGET := $(BUILD_DIR)/in1weekend 

SRCS := $(shell find $(SRC_DIRS) -name '*.cpp' -or -name '*.c' -or -name '*.s')

OBJS := $(SRCS:%=%.o)

INC_DIRS := -I./include

CPPFLAGS := $(INC_FLAGS) -Wall
CFLAGS := $(INC_FLAGS) -Wall


$(TARGET): $(OBJS)
	$(CXX) $(OBJS) -o $@
	rm -rf $^

%.c.o: %.c
	$(CC) $(CPPFLAGS) $(CFLAGS) -c $< -o $@

%.cpp.o: %.cpp
	$(CXX) $(CPPFLAGS) $(CXXFLAGS) -c $< -o $@


.PHONY: clean
clean:
	rm -rf $(TARGET)