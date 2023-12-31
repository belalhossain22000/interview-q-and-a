# JavaScript Interview Questions and Answers

## Basics:

1. **What is JavaScript?**
   - **Answer:** JavaScript is a high-level, interpreted programming language used to create interactive and dynamic content on web pages. It's commonly used for client-side scripting in web development.

2. **Explain the difference between `null` and `undefined` in JavaScript.**
   - **Answer:** `null` represents an intentional absence of any value, while `undefined` indicates a variable that has been declared but has not been assigned a value.

3. **How does hoisting work in JavaScript?**
   - **Answer:** Hoisting is JavaScript's default behavior of moving declarations (both variable and function declarations) to the top of their containing scope during the compilation phase, allowing variables and functions to be used before they are declared.

## Data Types and Variables:

4. **Discuss the different data types in JavaScript.**
   - **Answer:** JavaScript has primitive data types like `string`, `number`, `boolean`, `null`, `undefined`, along with non-primitive/reference types like `object`, `array`, `function`.

5. **What is the difference between `let`, `const`, and `var` in variable declaration?**
   - **Answer:** `let` and `const` are block-scoped and cannot be re-declared within the same scope, but `let` variables can be reassigned while `const` variables cannot. `var` is function-scoped and allows re-declaration and reassignment.

## Functions and Scope:

6. **How do you define a function in JavaScript?**
   - **Answer:** Functions can be defined using the `function` keyword or using arrow functions `() => {}`.

7. **Discuss the difference between `function` and `arrow function` syntax.**
   - **Answer:** Arrow functions have a concise syntax and do not bind their own `this`. They are anonymous and cannot be used as constructors, while regular functions can.

## Objects and Prototypes:

8. **What are objects in JavaScript?**
   - **Answer:** Objects in JavaScript are collections of key-value pairs where values can be of any data type. They are used to represent complex entities and are fundamental to JavaScript.

9. **Explain the concept of prototypal inheritance in JavaScript.**
   - **Answer:** In JavaScript, objects have a prototype property that allows inheritance. When a property is accessed on an object, if the object lacks this property, JavaScript checks its prototype chain until it finds the property or reaches the end of the chain (usually `Object.prototype`).

## Arrays and Iteration:

10. **How do you iterate over arrays in JavaScript?**
    - **Answer:** Arrays can be iterated using methods like `forEach()`, `for...of` loop, `map()`, `filter()`, `reduce()`, and `for` loop.

11. **Discuss the difference between `forEach()` and `map()` in JavaScript.**
    - **Answer:** `forEach()` is used to execute a provided function once for each array element without returning a new array, while `map()` creates a new array by applying a function to each element of the original array.

## Promises and Asynchronous JavaScript:

12. **What are Promises in JavaScript?**
    - **Answer:** Promises are objects representing the eventual completion or failure of an asynchronous operation. They allow handling asynchronous operations in a more readable and manageable way.

13. **Explain `async/await` in JavaScript.**
    - **Answer:** `async/await` is a modern approach to handle asynchronous code in JavaScript. `async` keyword defines a function that returns a Promise, and `await` is used to pause the execution of an async function until the Promise is resolved.

## ES6+ Features:

14. **Discuss some ES6+ features introduced in JavaScript.**
    - **Answer:** ES6+ introduces features like arrow functions, `let` and `const` for variable declaration, template literals, destructuring, spread/rest operators, classes, modules, and more.

## Error Handling and Debugging:

15. **How do you handle errors in JavaScript?**
    - **Answer:** Errors in JavaScript can be handled using `try...catch` blocks, where code that might throw an error is placed within `try`, and error handling logic is in `catch`.

16. **What tools are commonly used for JavaScript debugging?**
    - **Answer:** Debugging in JavaScript can be done using browser dev tools (Chrome DevTools, Firefox DevTools), IDEs (VSCode), and debuggers like Node Inspector.

## DOM Manipulation and Events:

17. **Explain DOM manipulation in JavaScript.**
    - **Answer:** DOM manipulation involves accessing and modifying HTML elements using JavaScript to dynamically change content, style, or structure of a webpage.

18. **How do you handle events in JavaScript?**
    - **Answer:** Events in JavaScript are handled using event listeners (e.g., `addEventListener()`) that listen for specific events (e.g., click, keypress) and execute a function when the event occurs.
