﻿```go
package main

import "fmt"

type Callback func(x, y int) int

func main() {
	x, y := 1, 2
	fmt.Println(test(x, y, add))
}

func test(x, y int, callback Callback) int {
//提供一个接口，让外部去实现，在javascript中很常见

	return callback(x, y)
}

func add(x, y int) int {
	return x + y
}
```