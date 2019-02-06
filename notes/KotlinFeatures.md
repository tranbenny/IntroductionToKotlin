# Features in Kotlin

**Contents**
* Null Safety


### Null Safety
* by default, variables cannot be null in kotlin
* if a value can be null, it has to be explicitly declared with ?
```kotlin
val name: String? = null

// How do we handle the null values safely?
// -----------------------------------------------

// 1. Safe Call: (?.) when you want to handle the cases where the value can be null
println("The length of name is ${name?.length}")

// 2. Safe Call with let block
// It executes the block ONLY IF name is not null
name?.let {
    println("The length of name is ${name.length}")
}

// 3. Non-null assertion operator
//  Use this for cases when you are sure the value will not be null
//  Otherwise, this throws NPE
println("The length of name is ${name!!.length}")

```


### Extension Functions
* allows you add functions to a class externally (without modifying the existing class)
