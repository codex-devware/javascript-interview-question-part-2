

# 1.Explain the difference between primitive and reference data types in JavaScript.

# Primitive data types: Numbers, strings, booleans, null, undefined (each value is stored directly in memory)
# Reference data types: Objects, arrays (store a reference to the location in memory where the actual data resides)


let num = 10; // Primitive (number)

let str = "hello"; // Primitive (string)

let obj = { name: "Alice" }; // Reference (object)

let arr = [1, 2, 3]; // Reference (array)




# 2. How do you declare variables in JavaScript? What are the differences between var, let, and const?

# var(function-scoped, can lead to hoisting issues)

# let(block-scoped, preferred for modern JavaScript)

# const(block-scoped, for constant values)

// var (not recommended for modern JS)

function sayHi() {

    var message = "Hello";
    console.log(message); // Accessible within the function
}
sayHi();

// let (preferred)
if (true) {

    let greeting = "Hi there!";
    console.log(greeting); // Accessible only within the `if` block
}

// const (for constants)

const PI = 3.14159;

PI = 10; // This will result in an error, as `const` cannot be reassigned

