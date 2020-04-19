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


