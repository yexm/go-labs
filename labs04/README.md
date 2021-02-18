测试range循环和for循环，以及结构体循环和指针循环的性能区别。

实验结果：

    go test -bench=. -benchmem
    goos: darwin
    goarch: amd64
    pkg: go-labs/labs04
    Benchmark_Loop1-8        1785180               779 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop2-8        1715780               731 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop3-8        1422454               837 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop4-8          93202             12047 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop5-8          97647             11893 ns/op               0 B/op          0 allocs/op
    PASS
    ok      go-labs/labs04  9.221s


结论：对结构体列表的range循环最消耗性能，因为数据要重复复制。
