Declaring variables:

Kotlin: val greeting: String = "Hello, World!"
TypeScript: let greeting: string = "Hello, World!";
Defining functions:

Kotlin:
kotlin
Copy code
fun greet(name: String) {
    println("Hello, $name!")
}
TypeScript:
javascript
Copy code
function greet(name: string): void {
    console.log(`Hello, ${name}!`);
}
Control flow statements:

Kotlin:
kotlin
Copy code
val number = 42
if (number > 0) {
    println("$number is positive")
} else if (number < 0) {
    println("$number is negative")
} else {
    println("$number is zero")
}
TypeScript:
typescript
Copy code
const number: number = 42;
if (number > 0) {
    console.log(`${number} is positive`);
} else if (number < 0) {
    console.log(`${number} is negative`);
} else {
    console.log(`${number} is zero`);
}
Object-oriented programming:

Kotlin:
kotlin
Copy code
interface Greeter {
    fun greet(name: String)
}

class EnglishGreeter : Greeter {
    override fun greet(name: String) {
        println("Hello, $name!")
    }
}
TypeScript:
typescript
Copy code
interface Greeter {
    greet(name: string): void;
}

class EnglishGreeter implements Greeter {
    greet(name: string) {
        console.log(`Hello, ${name}!`);
    }
}
Functional programming:

Kotlin:
kotlin
Copy code
fun main() {
    val list = listOf(1, 2, 3, 4, 5)
    val squares = list.map { it * it }
    println(squares)
}
TypeScript:
typescript
Copy code
function main() {
    const list: number[] = [1, 2, 3, 4, 5];
    const squares: number[] = list.map(x => x * x);
    console.log(squares);
}
