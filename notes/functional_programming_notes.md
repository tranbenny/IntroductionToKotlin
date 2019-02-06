# Functional Programming in Kotlin

* Kotlin supports higher-order functions
    * can accept function as a parameter
    * can return a function
    * can do both

### Lambdas in Kotlin

**Example**
```kotlin
val myLambda: (Int, Int) -> Int = {x: Int, y: Int -> x + y}
```
* single parameter lambda functions can utilize the **it** keyword
```kotlin
{str -> str.reversed() }

// same as above
{it.reversed() }

```



### Closures in Kotlin
* Closures: variables defined in the outer scope of a lambda expression
* in Java 8, you cannot modify closures outside the lambda
* In Kotlin, you can modify the closure outside the lambda

**Example**
```kotlin
fun main(args: Array<String>) {
    var result = 0
    
    val lambda: (Int, Int) -> Unit = {x, y -> result = x + y}
    addTwoNum(2, 4, lambda)
    println(result) // prints 6
}

fun addTwoNum(a: Int, b: Int, myFunc: (Int, Int) -> Unit) {
    myFunc(a, b)
}

```