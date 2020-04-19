# ProgramingWithTypeInKotlin
- 'final' by defaults
- 'abstract' class
- Modifiers
- Sealed Classes
- Constructors
- Data Class

## Classes
- Class  is final by defaults.
- Methods are final by defaults.
```kotlin
  class TestClass() {
        fun addNum() {}
    }

 class TestClassMain() :TestClass() { // here you will get error that final class cannot be inherited 
      fun multi() {}
    }
```
```kotlin
// use 'open' to show class can be derived.
// also with function we have to use 'open' 
//Example
 open class Student() {
        val firstName = "Supriya"
        val lastNAme = "Bharti"
        open fun getStudent(): String = "$firstName  $lastNAme"
    }

    class College() : Student() {
        override fun getStudent(): String {
            return ""
        }
    }
```
## abstract
```kotlin

    abstract class Student {
        abstract fun getName() // must be implements
        open fun getRollNo() {} // can be override 
        fun getAddress() {} // cannot be override because this is the final class
    }
```
## Constructor
```kotlin
 open class Student(name: String, id: String) {
        val name: String
        val id: String

        init {
            this.name = name
            this.id = id
        }
    }
    ```
    ```kotlin
    //Constructor type 2
    class College(address: String){
        val addrs = address
    }
```

