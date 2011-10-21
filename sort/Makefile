CXXFLAGS += -DNDEBUG -g0 -O3  # High optimization.
CXXFLAGS += -fopenmp # For omp_get_wtime().
FLAGS += -fopenmp

default: all

all: sort_bench

sort_bench.o: sort_bench.cpp
	$(CXX) $(CXXFLAGS) -c -o sort_bench.o sort_bench.cpp

sort_bench: sort_bench.o
	$(CXX) $(CXXFLAGS) -o sort_bench sort_bench.o

clean:
	rm -f sort_bench sort_bench.o