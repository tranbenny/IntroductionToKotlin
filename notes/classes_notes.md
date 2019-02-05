# Classes in Kotlin

### Notes on Classes
* init blocks are executed right after the object is instantiated


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

### Interfaces