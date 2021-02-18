测试几种链表遍历查找的性能差异。

实验结果：

    go test -bench=. -benchmem    
    goos: darwin
    goarch: amd64
    pkg: go-labs/labs07
    Benchmark_Loop1-8         311688              3902 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop2-8         258488              4646 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop3-8          62006             16604 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop4-8          15566             82921 ns/op          256256 B/op       1001 allocs/op
    Benchmark_Loop5-8           3760            310976 ns/op           16016 B/op       2002 allocs/op
    Benchmark_Loop6-8         270974              4343 ns/op             256 B/op          1 allocs/op
    Benchmark_Loop7-8         244359              4833 ns/op             600 B/op          7 allocs/op
    PASS
    ok      go-labs/labs07  9.544s


结论：有空做个查询表达式解析器吧。
