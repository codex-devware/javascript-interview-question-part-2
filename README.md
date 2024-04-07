

# Question 1.Explain the difference between primitive and reference data types in JavaScript.

# Primitive data types: Numbers, strings, booleans, null, undefined (each value is stored directly in memory)
# Reference data types: Objects, arrays (store a reference to the location in memory where the actual data resides)


let num = 10; // Primitive (number)

let str = "hello"; // Primitive (string)

let obj = { name: "Alice" }; // Reference (object)

let arr = [1, 2, 3]; // Reference (array)




# Question 2. How do you declare variables in JavaScript? What are the differences between var, let, and const?

 var(function-scoped, can lead to hoisting issues)

 let(block-scoped, preferred for modern JavaScript)

 const(block-scoped, for constant values)

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



# Question 3. JavaScript for Dynamic Captions (Optional):

#If you want dynamic captions based on user interaction or data fetching, you can use JavaScript to manipulate the caption content.
#Access the caption element using document.querySelectorand update its text content using textContentproperty.


// Example: Update caption on image click

const image = document.querySelector(".image-container img");

const caption = document.querySelector(".image-container .caption");

image.addEventListener("click", () => {

  caption.textContent = "This image has been clicked!";
  
});



# Question 4: Describe the different types of operators in JavaScript.

#Answer:

#JavaScript offers various operators for performing calculations, comparisons, and other operations:
#Arithmetic operators ( +, -, *, /, %) for mathematical calculations.

#Comparison operators ( ==, ===, !=, !==, <, >, <=, >=) for comparing values.

#Logical operators ( &&, ||, !) for combining logical expressions.

#Assignment operators ( =, +=, -=, *=, /=, %=) for assigning values ​​and performing operations simultaneously.

#Increment/decrement operators ( ++, --) for increasing or decreasing a variable's value by 1.

#Bitwise operators ( &, |, ^, ~, <<, >>, >>>) for manipulating bits within a number (less common).


let a = 5, b = 3;

console.log(a + b);         // Outputs 8 (addition)

console.log(a === b);       // Outputs false (strict equality)

console.log(a > b || b < 0); // Outputs true (logical OR)

let c = 10;

c++;

console.log(c);             // Outputs 11 (post-increment)




# Question 5: Write a function that takes an array of numbers and returns the sum of all the elements.

# Answer:

function sum(numbers) {

    let total = 0;
    for (let num of numbers) {
        total += num;
    }
    return total;
}

let numbers = [1, 2, 3, 4, 5];

let result = sum(numbers);

console.log(result); // Output: 15



# Question 6: Explain the concept of closures in JavaScript and provide an example.

#A closure is a function that has access to the variable environment of its outer function, even after the outer function has returned.


function createGreeter(greeting) {
   
    return function(name) {
        console.log(greeting + ", " + name + "!");
    };
}

let greet = createGreeter("Hello");

greet("John"); // Output: Hello, John!

// Even though createGreeter has returned, the inner function still remembers the value of greeting


