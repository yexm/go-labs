测试小数据量循环和map取数据以及硬编码取数据的性能消耗。

试验结果：

    go test -bench=. -benchmem
    goos: darwin
    goarch: amd64
    pkg: go-labs/labs06
    Benchmark_Loop1-8       291104751                3.89 ns/op            0 B/op          0 allocs/op
    Benchmark_Loop2-8       310581496                3.96 ns/op            0 B/op          0 allocs/op
    Benchmark_Loop3-8       100000000               12.9 ns/op             0 B/op          0 allocs/op
    Benchmark_Loop4-8       292445773                4.25 ns/op            0 B/op          0 allocs/op
    Benchmark_Loop5-8       1000000000               0.315 ns/op           0 B/op          0 allocs/op
    PASS
    ok      go-labs/labs06  7.141s


结论：硬编码 < 指针slice的range循环 < for循环，但是量级是一样的，看情况用。但是map差了一个量级，小数据量尽量少用。
