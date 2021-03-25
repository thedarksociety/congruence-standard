Standards and Style - Go
========================

My (iods/thedarksociety) code style and conventions of Go.


Getting Started
---------------

https://play.golang.org/

Golang (Go.com was not available at the time lol) is a simple programming language, that compiles fast, runs fast, and is easy to distribute.
* Focuses on simplicity and speed by harnessing power of today's multi-core processors

### The Problem

Google was compiling millions of lines of code, taking hours at a time. They built a solution with Go which solved:
* Slow compilation
* Cumbersome code
* Garbage collection (freeing unused memory)
* Concurrency
* Support for multi-core processors

Robert Grieseman, Rob Pike, and Ken Thompson created Go in 2007 at Google.

## Packages

The differences between libraries and packages.

Library | Executable
--------|---------------
Created for Reusability | Created for Running Program
Non-Executables | Executable
Importable | Non-Importable
Name Agnostic | Only be Named Main
No Main Function | func main

## Scope

## Control Flow

### Conditionals
In computer science, control flow (flow of control) is the order in which individual statements, instructions or function calls of imperative program are executed or evaluated.

```go
if condition {
    // do something
} else if condition {
    // do something
} else {
    // do something
}

a := 3
b := 4
```
An expression is evaluated, and if the result is **true** the code in the conditional block body is executed. If it is **false** it is ignored. Go supports nesting it's conditional statements.

Conditionals rely on a Boolean expression (one that evaluates to true or false) to decide whether the code they contain should be executed. If you need to only execute code if a condition is **false** using the **Boolean negation operator** `!` will allow you to make a true statement false or a false statement true.

Using `&&` will run code if both expressions are evaluated true, and using `||` will run code if **either** expression is evaluated true.

### Loops

Code that runs repeatedly is known as a loop.



## Methods

Methods are functions that are associated with values of a particular type. Essentially, the dot indicates that the thing on the right belongs to the thing it's left. Methods belong to an individual value, where functions belong to a package.

Blank Identifiers

Error Handling

Block and Variable Scope

## Pointers

Values that represent the address of a variable are known as **pointers**, they point to the location where the variable is stored and can be accessed.

* https://www.golang-book.com/books/intro/8
* https://flaviocopes.com/golang-methods-receivers/
* https://medium.com/@vCabbage/go-are-pointers-a-performance-optimization-a95840d3ef85
* https://www.ardanlabs.com/blog/2017/05/language-mechanics-on-stacks-and-pointers.html
* https://medium.com/a-journey-with-go/go-should-i-use-a-pointer-instead-of-a-copy-of-my-struct-44b43b104963
* https://dev.to/chen/gos-method-receiver-pointer-vs-value-1kl8
* https://qvault.io/2019/09/25/the-proper-use-of-pointers-in-go-golang/
* https://www.digitalocean.com/community/conceptual_articles/understanding-pointers-in-go

## Data Types

Code Types.


### Boolean

The `bool` type holds boolean values, which are either `true` or `false`.


### Strings

A string is a series of bytes that represents text characters. A rune, represents a single text character.


### Numbers

Go has many number types, but the two most used are `int` and `float64` which holds float-pointing numbers.


### Variables

A variable is a piece of storage that contains values of a specific type.
* If no value is assigned, it will be given a **0** value

Using **short variable declaration** you can declare and assign a variable using the `:=` operator.


## Development

### File Layout
```go
// Package Clause
package main

// Import Statements
import "fmt"

// Function References
func main() {
    fmt.Println("Go Code Style")
}
```

### Package Clause

A package is a grouping of code that all does similar things. The **package clause** gives the name of the package that this files code becomes part of. The package `main` is required if the code is to be run directly, i.e. an executable, and from the terminal.

* Every file must begin with a Package Clause
* A package is a group of related functions and other code
* Before you can use a package's functions, you have to import that package
* A package is essentially source level coupling

### Import Statements

Each Go file must import other packages in order to use their resources. Rather than loading all packages, the import statement allows for explicit declaration of packages for your Go file.

* Every Go file must import each Package it references
* Only import Packages that your Go file references

### Functions

A function is one or more lines of code you call or run from various places of a program. When calling a function, using arguments to provide the function with data will change it's output.

With Go, the function `main` is executed first.

* Go looks for the function `main` to run first


## Interfaces

> Interface values - regardless of their type and whether they are empty or not - hold two things:
> 1. the concrete type of some value (or no type); and
> 2. the value of that concrete type (or no value)

Go more or less requires you to check a type before getting a value. (Type Assertions?)

The first step, figure out what the type is. Sometimes there is a step before a step.
```go
if i == nil {
    // if i has a typed value in it, and can hold nil pointers
    // the value part can be nil, and the i==nil is false. i does have a type
}
```
### Empty Interfaces

Are they just adhoc interfaces?

## Naming Conventions

There are very few, and minimal rules when it comes to naming in Go. They are:
* Variables, functions, and types must start with a letter
* They should be written in camelCase
* lowercase functions are not **exported**
* Functions that start with Uppercase letters **ARE** exported

Only variables, functions, and types whose names begin with a capital letter are considered to be exported, meaning accessible outside of the current package.

## FAQs

**Where do I save my source code?**

Under my $GOPATH/src ($GOPATH can be anywhere)

**What does $GOPATH mean?**

Stores the Go source code files and compiled packages.

**Do you need to set this $GOPATH?**

Yes, set it yourself.

**How can you print it?**

Using the `go env GOPATH` command.

**What about semi-colons in Go?**

You _can_ use them to separate statements in Go; however, not only is it not required, it is generally frowned upon.

**What is this `go fmt` thing?**

The Go Compiler comes with a standard formatting tool. This tool can be run locally and will automatically fix all formatting.
