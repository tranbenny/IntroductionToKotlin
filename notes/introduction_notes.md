# Introduction to Kotlin Notes

**Table of Contents**
* Kotlin Features
* Kotlin Timeline
* Kotlin Compilation Process
* Variables and Data Types
* String Templates and Interpolation 


### Kotlin Features
* JVM language, requires JVM to execute byte code
* support to avoid NPE
* supports immutability
* supports OOP
* supports functional programming
	* can pass a function as a parameter to another function
	* functions can return another function
* less boilerplate code 
* Types of apps that can be built on Kotlin
	* Server-side Apps
	* Android 
	* Web Development
	* Desktop Applications
	* Native Development 


### Kotlin Timeline
* July 2011: Kotlin came out by JetBrains
* Feb 2012: open sourced under Apache 2 license
* Feb 2016: Kotlin v1.0 released
* May 2017: Google adopted Kotlin support for Android


### Kotlin Compilation Process
* Sample file: myfirstapp.kt
* Compiler converts this file -> myfirstappKt.class (bytecode)
	* bytecode = code that is understandable by the runtime enviroment 
	* bytecode is then run by the JVM
* main function snippet
```kotlin

fun main(args: Array<String>) {
	println("Hello World")
}

```

## Language and Syntax Features


### Variables and Data Types
####Keywords
* var: mutable variables
* val: immutable variables 

**Sample Variable Declarations** 
```kotlin

// sample variable declarations
var age: Int = 10
var age = 10

var msg: String = "Hello"
var msg = "Hello"

var isAlive: Boolean = true
var isAlive = true

```

#### Data Types (all data types in Kotlin are Objects)
* String
* Boolean (1 bit)
* Byte (8 bit)
* Char (16 bit)
* Short (16 bit)
* Int (32 bit)
* Long (64 bit)
* Float (32 bit)
	* requires 'f' or 'F' suffix
	* i.e. val floatValue = 4.5F
* Double (64 bit)
* all variable types are objects, so they all must be initialized in order to have a default value 


### String Templates and Interpolation 
**Example**
```kotlin
val name = "Benny"
// without string interpolation
println("My name is " + name)
// with string interpolation
println("My name is $name")

// example with expression
println("The name variable has length " + name.length)
println("The name variable has length ${name.length}")


```


### If expressions
** Example **
```kotlin

val a: Int = 2
val b: Int = 5

val maxIfExpressionExample:Int = if (a > b) {
    a
} else {
    b
}

```

### When Expressions
* similar to switch/case statements in java

**When, Range Conditional Example**
```kotlin 

val x = 1

when(x) {
    1 -> println("x is 1")
    2 -> println("x is 2")
    in 5..10 -> println("x is in the range of 3-10")
    else -> {
        println("$x is not handled")
        println("Unknown Case");
    }
}

// when expression example

var msg: String

msg = when(x) {
    1 -> "x is 1"
    2 -> "x is 2"
    in 5..10 -> "x is in the range of 5-10"
    else -> {
        println("$x is not handled")
        "Unknown Case"
    }
}


```


### Loops
Basic For Loop
```kotlin
// print all the even numbers between 1 - 10

for (x in 1..10) {
    if (x % 2 == 0) {
        println(x)
    }
}

```

### Exception Handling
















