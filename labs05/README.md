测试整数和浮点数的运算效率。

实验结果：

      go test -bench=. -benchmem
      goos: darwin
      goarch: amd64
      pkg: go-labs/labs05
      Benchmark_IntAdd-8              1000000000               0.339 ns/op           0 B/op          0 allocs/op
      Benchmark_Int8Add-8             1000000000               0.323 ns/op           0 B/op          0 allocs/op
      Benchmark_Int16Add-8            1000000000               0.325 ns/op           0 B/op          0 allocs/op
      Benchmark_Int32Add-8            1000000000               0.342 ns/op           0 B/op          0 allocs/op
      Benchmark_Int64Add-8            1000000000               0.340 ns/op           0 B/op          0 allocs/op
      Benchmark_Float32Add-8          1000000000               0.317 ns/op           0 B/op          0 allocs/op
      Benchmark_Float64Add-8          1000000000               0.314 ns/op           0 B/op          0 allocs/op
      Benchmark_IntSub-8              1000000000               0.314 ns/op           0 B/op          0 allocs/op
      Benchmark_Int8Sub-8             1000000000               0.329 ns/op           0 B/op          0 allocs/op
      Benchmark_Int16Sub-8            1000000000               0.340 ns/op           0 B/op          0 allocs/op
      Benchmark_Int32Sub-8            1000000000               0.339 ns/op           0 B/op          0 allocs/op
      Benchmark_Int64Sub-8            1000000000               0.322 ns/op           0 B/op          0 allocs/op
      Benchmark_Float32Sub-8          1000000000               0.326 ns/op           0 B/op          0 allocs/op
      Benchmark_Float64Sub-8          1000000000               0.322 ns/op           0 B/op          0 allocs/op
      Benchmark_IntMul-8              1000000000               0.314 ns/op           0 B/op          0 allocs/op
      Benchmark_Int8Mul-8             1000000000               0.317 ns/op           0 B/op          0 allocs/op
      Benchmark_Int16Mul-8            1000000000               0.329 ns/op           0 B/op          0 allocs/op
      Benchmark_Int32Mul-8            1000000000               0.323 ns/op           0 B/op          0 allocs/op
      Benchmark_Int64Mul-8            1000000000               0.323 ns/op           0 B/op          0 allocs/op
      Benchmark_Float32Mul-8          1000000000               0.335 ns/op           0 B/op          0 allocs/op
      Benchmark_Float64Mul-8          1000000000               0.316 ns/op           0 B/op          0 allocs/op
      Benchmark_IntDiv-8              1000000000               0.330 ns/op           0 B/op          0 allocs/op
      Benchmark_Int8Div-8             1000000000               0.332 ns/op           0 B/op          0 allocs/op
      Benchmark_Int16Div-8            1000000000               0.311 ns/op           0 B/op          0 allocs/op
      Benchmark_Int32Div-8            1000000000               0.311 ns/op           0 B/op          0 allocs/op
      Benchmark_Int64Div-8            1000000000               0.316 ns/op           0 B/op          0 allocs/op
      Benchmark_Float32Div-8          1000000000               0.327 ns/op           0 B/op          0 allocs/op
      Benchmark_Float64Div-8          1000000000               0.316 ns/op           0 B/op          0 allocs/op
      PASS
      ok      go-labs/labs05  10.505s
结论：结果差不多。
