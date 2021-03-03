SOURCE=$(wildcard *.cpp)
TARGETS=$(patsubst %.cpp, %, $(SOURCE))

CC= g++
CFLAGS= -std=c++11 -O3 -march=native -fopenmp 

all:$(TARGETS)
$(TARGETS):%:%.cpp intrin-wrapper.h utils.h
			   $(CC) $< $(CFLAGS) -o $@

.PHONY:clean all
clean:
	-rm -rf $(TARGETS)
