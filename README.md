# go-ldflags-configure
这是一个用 `-ldflags` 选项给变量注入值的例子  
`main.go` 文件中的 `version` 是等待被注入的变量

执行
```bash
$ go build -o test main.go && ./test
```
结果
```bash
program version: 0.0.1
```

执行
```bash
$ go build -ldflags "-X main.version=0.1.0" -o test main.go && ./test
```
结果
```bash
program version: 0.1.0
```
