# Statics in Kotlin

* Singleton - when you one instance/object of a class that is reused throughout the entire application
* How do you declare singletons in Kotlin?
    * Object Declaration
    * Companion Object
    
**Object Declaration Example**
```kotlin
object Value {
    val pi = 3.14
}

// accessing the value
// Value object is created internally in Kotlin and used as a singleton
Value.pi

```

**Companion Object Example**
```kotlin

class Value {
    companion object {
        val pi = 3.14
    }
}

// accessing the value 
Value.Companion.pi
Value.pi

```


* object declaration inside class is marked with companion keyword
* companion object is initialized (singleton) *when the corresponding class is LOADED*
* object declarations support inheritance
* object declarations are initialized lazily when accessed
* only one companion object can be created in a class  


**Examples using static fields and methods with object declaration**
```kotlin
fun main(args: Array<String>) {
    println(Maths.pi)
    val area = Maths.find(6, 2)
}

object Maths {
    // Static variable
    val pi = 3.14

    // Static Function
    fun findArea(l: Int, b: Int): Int {
        return l * b
    }
}
```