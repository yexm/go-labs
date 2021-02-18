测试类型判断和类型转换的效率。

执行结果：

    go test -test.bench=.
    goos: darwin
    goarch: amd64
    pkg: go-labs/labs01
    Benchmark_TypeSwitch-8          83987925                14.4 ns/op
    Benchmark_NormalSwitch-8        535543136                2.33 ns/op
    Benchmark_InterfaceSwitch-8     137492682                8.31 ns/op
    PASS
    ok      go-labs/labs01  4.817s

结论：类型判断和类型转换这两个操作都比直接操作多几倍的消耗。

