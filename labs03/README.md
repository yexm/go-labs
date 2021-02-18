测试对象创建的效率。

实验结果：

    go test -bench=. -benchmem
    goos: darwin
    goarch: amd64
    pkg: go-labs/labs03
    Benchmark_NewStruct1-8          1000000000               0.332 ns/op           0 B/op          0 allocs/op
    Benchmark_NewStruct2-8          1000000000               0.316 ns/op           0 B/op          0 allocs/op
    Benchmark_NewStruct3-8          1000000000               0.311 ns/op           0 B/op          0 allocs/op
    Benchmark_NewStruct4-8          1000000000               0.332 ns/op           0 B/op          0 allocs/op
    Benchmark_NewStruct5-8          222773493                5.28 ns/op            0 B/op          0 allocs/op
    PASS
    ok      go-labs/labs03  3.591s


结论：5的结果最差，其余差不多。
