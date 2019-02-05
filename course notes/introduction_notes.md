#Introduction to Kotlin Notes

**Table of Contents**
* Kotlin Features
* Kotlin Timeline
* Kotlin Compilation Process
* Variables and Data Types


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
* Double (64 bit)
* all variable types are objects, so they all must be initialized in order to have a default value 

















