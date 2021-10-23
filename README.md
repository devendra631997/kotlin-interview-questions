# kotlin-interview-questions


### Kotlin is used for:
* Mobile Application (specially for android)
* web development 
* server side application
* Data Science ...

### Why to use kotlin ?
* Kotlin is fully compatible with java
* Kotlin works on different platform
* Kotlin is concise and safe
* Kotlin is esy to learn, especiallly if you already know java.
* Kotlin is free to use.
* Big community/support
### How does Kotlin work on Android?
Just like Java, the Kotlin code is also compiled into the Java bytecode and is executed at runtime by the Java Virtual Machine i.e. JVM. When a Kotlin file named Main.kt is compiled then it will eventually turn into a class and then the bytecode of the class will be generated. The name of the bytecode file will be MainKt.class and this file will be executed by the JVM.

### what is primary constructor in Kotlin ?
The primary constructor is part of the class header. Unlike java, you don't need to declare a constructor in the body of the class.

```kotlin
class Person(val firstName: String, var lastName: Int) {
    // class body
}
```
main idea is by removing the constructor keyword, our code gets simplified and easy to understand

### What is data class in kotlin ?
we frequently create classess whose main purpose is to hold data. In kotlin that is called a data class and is marked as data

```kotlin
data class User(val name: String, val age: Int)
```
To ensure consistency and meaningful behaviour of the generated code, data class has to fullfill the following requirement:
* the primary constructor needs to have at least one parameter;
* All primary constructor paramenters need to be marked as val and var;
* Data classess cannot  be abstract, open, sealed or inner;

### Explain null safety in kotlin ?
Kotlins's system is aimed at eliminating the danger of null references from code, also known as the billion dollar mistake.

One of the most common pitfalls in many programming languages, including java, is that accessing a member of a null reference exception . In java this would be the equivalent of a `NullPointerException` or NPE for short.
In kotlin, the type system distinguishes between reference that can hold `null` (nullable references) and those that can not (`non-null` reference). For example, a regular variable of type String can not hold null:

```kotlin
var a: String = "abc"
a = null // compilation error
```
To allow nulls, we can declare a variable as nullable string, written `String?`:
```kotlin
var b: String? = "abc"
b = null // ok
print(b)
```