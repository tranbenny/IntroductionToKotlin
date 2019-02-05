# Notes on functions in Kotlin

### Functions in Kotlin
* Unit keyword is used for void methods
* methods are void type by default if a return type is not specified

**Example**
```kotlin

fun add(a: Int, b: Int): Int {
    return a + b
}

// sample void method
fun printParams(a: Int, b: Int): Unit {
    println("Params: $a, $b")
}

```

* supports default parameters
* supports named parameters 

**Tail Recursive Functions**
* keyword: tailrec
* tailrec explained: https://medium.com/@JorgeCastilloPr/tail-recursion-and-how-to-use-it-in-kotlin-97353993e17f
* tailrec allows for StackOverflow safe recursive functions 
* "In order to be eligible for the tailrec modifier, a function must call itself as the last operation it performs. You cannot use tail recursion when there is more code after the recursive call."
    * from article


**Example tailrec function**
```kotlin

// NOTE: use of BigInteger requires import
tailrec fun getFibonacciSequence(n: Int, a: BigInteger, b: BigInteger): BigInteger {
    if (n == 0) {
        return b
    } else {
        return getFibonacciSequence(n - 1, a + b, a)
    }
}


```
