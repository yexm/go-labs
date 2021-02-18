同labs07，区别是用slice替代链表结构。

试验结果：

    go test -bench=. -benchmem    labs07
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
    
    go test -bench=. -benchmem labs08
    goos: darwin
    goarch: amd64
    pkg: go-labs/labs08
    Benchmark_Loop1-8        1201026              1065 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop2-8         433276              2887 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop3-8          67934             16532 ns/op               0 B/op          0 allocs/op
    Benchmark_Loop4-8          14299             98045 ns/op          256000 B/op       1000 allocs/op
    Benchmark_Loop5-8           4281            340790 ns/op           16000 B/op       2000 allocs/op
    Benchmark_Loop6-8         348208              3565 ns/op             256 B/op          1 allocs/op
    PASS
    ok      go-labs/labs08  10.071s

结论：简单循环slice明显更快，但是加入查询后， slice的优势就可以忽略不计了。
