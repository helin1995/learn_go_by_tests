# 通过测试学习go

## Ch1、Hello World

1、测试、开发规律
* 编写一个测试
* 让编译通过
* 运行测试，查看测试失败原因并检查错误消息是很有意义的
* 编写足够的代码让测试通过
* 重构

## Ch2、Iteration

1、基准测试（Benchmark）
```go
func BenchmarkFunc(b *testing.B) {
    for i := 0; i < b.N; i++ {
        Func()
    }
}
```
执行：go test -bench="."或者go test -bench=.
函数会执行b.N次

2、样例Example，完善文档，比如：
```go
func ExampleRepeat() {
	repeated := Repeat("a")
	fmt.Println(repeated)
	// Output: aaaaa
}
```