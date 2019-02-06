# Classes in Kotlin

### Notes on Classes
* init blocks are executed right after the object is instantiated
* by default all classes are final (non-inheritable)

Example Dog Class
```kotlin
class Dog constructor(breed: String, age: Int, color: String) {    
    init {
        this.breed = breed
        this.age = age
        this.color = color 
    }
}

// creates the same object as above with simplified syntax
class Dog constructor(val breed: String, val age: Int, val color: String) {
    init {
    
    } 
}

```

### Inheritance
* keywords: open
    * used for declaring a base class
    * open modifier allows a class to be inherited by others
    * child class also needs to initialize the parent class

Example for when the child class has a primary constructor
```kotlin
// Parent class
open class Computer(val name: String,
                    val brand: String) {

}

// Child class
class Laptop(name: String,
             brand: String,
             val batteryLife: Double) : Computer(name, brand) {

}

```

Example for when the child class does not have a primary constructor
```kotlin
class Laptop : Computer {
    val batteryLife: Double

    constructor(name: String, brand: String, batteryLife: Double): super(name, brand) {
        this.batteryLife = batteryLife
    }

    constructor(name: String, brand: String): this(name, brand, 0.0) {

    }
}

```


### Interfaces
* interface keyword for defining interfaces
* all interface methods are default abstract
* interfaces can have default method implementations 
    * adding an open keyword to the methods will allow it to be overridden
* fields are abstract  

Interface Example
```kotlin

interface Remote {
    
    abstract var brand: String
    
    fun powerOn()
    fun powerOff()
    
    fun about() {
        println("I am Remote interface")
    }
}

class Television: Remote {
    
    var brand: String = ""
    
    override fun powerOn() {
        println("The TV is now switched ON")
    } 
    
    override fun powerOff() {
        println("The TV is now switched OFF")
    }
}

```

### Data Classes
* keyword data
* keyword data allows two classes to pass an equality check if the data in both objects are the same 
    * otherwise, the equality check will fail because they are 2 separate instances
* data classes cannot also be marked as open or sealed
* data classes can implement interfaces 
* automatically derives the implementation of equals, hashCode, toString methods from fields declared in the constructor
* adds copy() function
* adds componentN() function

**Why use Data Classes?**
* sometimes we just need classes to hold data/state (no specific functionality)

**copy() function**
* copy function can copy an existing object into a new object
* copy allows you to modify some nwe properties for the new object
* leaves the original class untouched
```kotlin
val customer = Customer(3, "James")
val newCustomer = customer.copy(name = "James LastName")
```

**componentN() function**
* allows for [destructuring declaration](https://kotlinlang.org/docs/reference/multi-declarations.html)