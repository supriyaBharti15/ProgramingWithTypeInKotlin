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

