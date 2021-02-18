测试值传参和指针传参的效率。

实验结果：

    go test -test.bench=.
    goos: darwin
    goarch: amd64
    pkg: go-labs/labs02
    Benchmark_Invoke1-8     1000000000               0.343 ns/op
    Benchmark_Invoke2-8     1000000000               0.331 ns/op
    PASS
    ok      go-labs/labs02  1.330s


结论：指针传参比值传参效率差不多。
