TimSort
==================
A C++ port of Java timsort implementation

The original is http://cr.openjdk.java.net/~martin/webrevs/openjdk7/timsort/raw_files/new/src/share/classes/java/util/TimSort.java

BENCHMARK
==================
bench.cpp, invoked by `make bench`, is a simple benchmark.
An example output is (scale: sec.):

    $ make bench
    g++ -lboost_unit_test_framework  -DNDEBUG -O2 -Wall -Wextra bench.cpp -o bench
    ./bench
    int
    size    100000
    std::sort        0.61
    std::stable_sort 0.64
    timsort          0.93
    double
    size	100000
    std::sort        0.64
    std::stable_sort 0.78
    timsort          1
    boost::rational
    size	100000
    std::sort        5.5
    std::stable_sort 4.32
    timsort          6.02

Looks not so great...(´･_･`)
