C++ OOP vs. Template Specialization
===================================

This repository contains some examples and benchmarks comparing C++ OOP and
template specialization.

Sort Benchmark
--------------

The file sort_bench.cpp contains a small example program that sorts
5-tuples of ints which are compared based on their first value.  This
is an example work load for key based sorting of records.  The sorting
is done in two variants: First, we have class Item1 which implements
operator< as an non-virtual function.  This means that the comparison
can be inlined in the std::sort() call.  Second, we have class Item2
which is identical to Item1 except that the less-than operator is
declared as virtual.

The resulting differences in running times on a Xeon X5550 @2.67 Ghz
machine, compiled with GCC 4.4.5 are as follows.


    Parameters
        # iterations: 10
        # items     : 100000000
        seed        : 42
  
    Generating input.
        time 0.836878 s

    std::sort with inlining
        time avg 5.43477 s dev 0.0817846

    std::sort without inlining
        time avg 11.0379 s dev 0.0425878
