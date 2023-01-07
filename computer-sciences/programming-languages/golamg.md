# Go

main.go
```go
package main

import "fmt"

func Sum(x, y int) int {
	return x + y
}
func SumAndMul(x, y int) (int, int) {
	return x + y, x * y
}
func main() {
	fmt.Println("Hello, World.")
	fmt.Println(Sum(2, 3))
	fmt.Println(SumAndMul(2, 3))
}
```

```
$ go run main.go
Hello, World.
5
5 6
```