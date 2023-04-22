---
title: "Pointers In Golang"
datePublished: Sat Apr 22 2023 17:03:29 GMT+0000 (Coordinated Universal Time)
cuid: clgs8bx2m00050al6dfs50znc
slug: pointers-in-golang
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682182936344/96a6a753-7c7c-440b-b0cd-8f8283d8c051.png
tags: pointers, golang, devops, hashnode, wemakedevs

---

Pointers in Go are variables that store the memory address of another variable. They are denoted by the `*` symbol preceding the type of variable they will point to. For example, to declare a pointer to an integer variable, you would write `var ptr *int`.

To assign a value to a pointer, you need to use the address-of operator `&` followed by the variable you want to assign to the pointer. For example, if you have an integer variable `x`, you can assign its memory address to a pointer variable `ptr` like this:

```go
var x int = 42
var ptr *int = &x
```

To access the value that a pointer points to, you need to dereference the pointer using the `*` operator. For example, to print the value of `x` through the pointer `ptr`, you would write:

```go
fmt.Println(*ptr)
```

You can also modify the value of a variable through a pointer by dereferencing the pointer and assigning a new value to it. For example, to change the value of `x` through the pointer `ptr`, you would write:

```go
*ptr = 21
```

After this assignment, the value of `x` would be 21.

Go also provides a shorthand for declaring and initializing a pointer to a new variable using the `new()` function. For example, to declare and initialize a pointer to a new integer variable, you would write:

```go
ptr := new(int)
```

This creates a new integer variable and returns a pointer to it.

Finally, pointers can also be used to point to structs in Go. For example, to declare a pointer to a `Person` struct, you would write:

```go
type Person struct {
    name string
    age  int
}

var p *Person = &Person{"Alice", 30}
```

This declares a new `Person` struct and assigns its memory address to the `p` pointer variable.

In conclusion, pointers are a powerful feature of Go that allows you to manipulate and modify variables by reference. They are used extensively in Go code to create more efficient and flexible programs.