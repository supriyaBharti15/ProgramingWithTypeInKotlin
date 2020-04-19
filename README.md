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
## Data class
```kotlin
val s1 = Student(1, "supriya")
        val s2 = Student(1, "supriya")
        if (s1 == s2) println("Equal") else println("Not Equal")
    //Output will be Not Equal

 println(s1) //Output :MainActivity$Student@c337130
    class Student(val id: Int, val name: String) {}
```
```kotlin
val s1 = Student(1, "supriya")
        val s2 = Student(1, "supriya")
        if (s1 == s2) println("Equal") else println("Not Equal")
    //Output will be  Equal
 println(s1) //Output : Student(id=1, name=supriya)
 /Make the copy
        val s1Copy = s1.copy(1, "navin")
        println(s1Copy) // Output :: Student(id=1, name=navin)
        if (s1 == s1Copy) println("Equal") else println("Not Equal") // Output :: Not Equal
 
    data class Student(val id: Int, val name: String) {}
```
