---
title: "Maps In Golang"
datePublished: Tue Apr 25 2023 18:20:02 GMT+0000 (Coordinated Universal Time)
cuid: clgwldwyk000b0am87xsm4gmr
slug: maps-in-golang
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682446717206/c0e26eaf-59cb-49e2-aea2-8c265336a112.png
tags: go, developer, devops, wemakedevs

---

What is a Map?

A map is a built-in type in Go that associates a key with a value. In other words, a map is a collection of key-value pairs. The keys in a map must be unique, and the values can be of any type.

The syntax for declaring a map in Go is as follows:

```go
var m map[key-type]value-type
```

Here, `key-type` represents the type of the key, and `value-type` represents the type of the value. For example, to declare a map that maps strings to integers, you would use the following code:

```go
var m map[string]int
```

Creating a Map:

To create a map in Go, you can use the make function, which allocates and initializes a new map. The make function takes two arguments: the type of the map's keys and the type of its values. Here's an example:

```go
m := make(map[string]int)
```

In this example, we've created a map that maps strings to integers. We can now add key-value pairs to the map using the following syntax:

```go
m["one"] = 1
m["two"] = 2
m["three"] = 3
```

Accessing a Map:

To access a value in a map, you can use the square bracket notation and provide the key of the value you want to access. Here's an example:

```go
fmt.Println(m["two"])
```

In this example, we're printing the value associated with the key "two" in the map. This will output the following:

```go
2
```

If the key is not present in the map, Go will return the zero value for the value type. For example:

```go
fmt.Println(m["four"])
```

This will output:

```go
0
```

Checking for Existence:

You can check if a key exists in a map using the following syntax:

```go
value, ok := m[key]
```

Here, `value` will be set to the value associated with the key, and `ok` will be a boolean value indicating whether the key exists in the map or not. If the key exists, `ok` will be true, and `value` will contain the value associated with the key. If the key does not exist, `ok` will be false, and `value` will contain the zero value for the value type.

Here's an example:

```go
value, ok := m["two"]
if ok {
    fmt.Println(value)
} else {
    fmt.Println("Key not found")
}
```

This will output:

```go
2
```

Deleting from a Map:

To delete a key-value pair from a map, you can use the `delete` function. The `delete` the function takes two arguments: the map and the key to delete. Here's an example:

```go
delete(m, "two")
```

Adding and Updating Values:

To add or update a value in a map, you can use the square bracket notation and provide the key of the value you want to add or update. Here's an example:

```go
m["four"] = 4
m["one"] = 10
```

In this example, we're adding a new key-value pair that maps the string "four" to the integer 4, and we're updating the value associated with the key "one" to 10.

Iterating over a Map:

To iterate over a map in Go, you can use a `for` loop and the `range` keyword. The `range` keyword returns both the key and the value of each key-value pair in the map. Here's an example:

```go
for key, value := range m {
    fmt.Println(key, value)
}
```

In this example, we're printing each key-value pair in the map.

Sorting a Map:

Maps in Go are unordered, which means that the order of the key-value pairs in a map is not guaranteed. However, you can sort the keys of a map and iterate over them in a sorted order using the `sort` package in the standard library. Here's an example:

```go
keys := make([]string, 0, len(m))
for key := range m {
    keys = append(keys, key)
}
sort.Strings(keys)

for _, key := range keys {
    fmt.Println(key, m[key])
}
```

In this example, we're creating a slice of strings to store the keys of the map, then we're appending each key to the slice. We're then sorting the slice using the `sort.Strings` function and iterating over the sorted keys.