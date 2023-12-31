## Introduction to TypeScript:
1. What is TypeScript, and how does it differ from JavaScript?
   
    ```markdown
    TypeScript is a superset of JavaScript developed by Microsoft. It adds optional static typing, enhanced tooling, and better code organization features. TypeScript code needs to be transpiled into JavaScript to run in browsers.

2. Explain the advantages of using TypeScript over plain JavaScript.
   ```markdown
    TypeScript offers benefits such as type checking, improved IDE support, better tooling for larger projects, increased code maintainability, early error detection, and improved readability through type annotations.

### TypeScript Setup and Basics:
3 .How do you install TypeScript, and what is the purpose of a Node Version Manager (NVM)?
    Ans:
    TypeScript can be installed globally via npm using npm install -g typescript. Node Version Manager (NVM) allows managing multiple Node.js versions on a single machine, helpful when working on projects requiring different Node.js versions.

4. Can you demonstrate how to write and compile a basic TypeScript program?
    Ans:
    Certainly! A basic TypeScript program can be created by writing code in a .ts file and compiled to JavaScript using the TypeScript compiler (tsc). For example:
    TypeScript code (app.ts):
    ```typescript
    const message: string = 'Hello, TypeScript!';
    console.log(message);
    Command to compile:

    Copy code
    tsc app.ts
This generates a JavaScript file (app.js) that can be executed using Node.js.
## Data Types in TypeScript:
5. Discuss the basic data types in TypeScript and provide examples of each.
    Ans:
    Basic types include number, string, boolean, null, undefined, object, and array. Examples:
    ```typescript
    let num: number = 10;
    let str: string = 'Hello';
    let bool: boolean = true;
    let n: null = null;
    let u: undefined = undefined;
    let obj: object = { key: 'value' };
    let arr: number[] = [1, 2, 3];
6. Explain the concept of optional and literal types in TypeScript.
    Ans:
    Optional types allow variables to accept undefined or the specified type. Literal types restrict variables to a specific value. Example:
    ```typescript
    let optionalVar: number | undefined;
    let literalVar: 'red' | 'blue' | 'green';
## Functions in TypeScript:
7. Describe the syntax differences between defining functions in JavaScript and TypeScript.
    Ans:
    TypeScript allows annotating parameters and return types, enabling static typing. Example:
    ```typescript
    function add(a: number, b: number): number {
        return a + b;
    }
8. What are the benefits of using typed parameters and return types in TypeScript functions?
    Ans:
    Typed parameters and return types improve code readability, catch type-related errors during development, and provide better IDE support and auto-completion.
## Advanced TypeScript Concepts:
9. Explain the use of spread and rest operators in TypeScript with examples.
    Ans:
    The spread operator (...) expands an array or object into individual elements, while the rest operator collects multiple elements into an array. Examples:
    ```typescript
    const arr1: number[] = [1, 2, 3];
    const arr2: number[] = [...arr1, 4, 5]; // Spread operator

    function sum(...args: number[]): number {
        return args.reduce((acc, val) => acc + val, 0);
    }
10. How do you use destructuring in TypeScript, and what advantages does it offer?
    Ans:
    Destructuring allows extracting values from arrays or objects into variables. It offers concise syntax and simplifies working with complex data structures. Example:
    ```typescript
    const person = { name: 'John', age: 30 };
    const { name, age } = person;
11. Discuss the purpose and implementation of type aliases in TypeScript.
    Ans:
    Type aliases create custom names for types, making code more readable and maintainable. Example:
    ```typescript
    type UserID = string | number;
    let id: UserID = 'user123';
12. What are union and intersection types in TypeScript? Provide examples of their usage.
    Ans:
    Union types (|) allow a variable to hold values of multiple types, while intersection types (&) combine multiple types. Examples:
    ```typescript
    type NumOrStr = number | string; // Union type
    type Employee = { id: number; name: string } & { department: string }; // Intersection type
## Error Handling and Operators:
13. Explain the usage of the ternary operator, optional chaining, and nullish coalescing in TypeScript.
    Ans:

    The ternary operator (condition ? expr1 : expr2) provides a concise way of writing conditional statements. Optional chaining (?.) allows safely accessing properties of possibly undefined/null values. Nullish coalescing (??) returns the right-hand operand if the left-hand operand is null or undefined, otherwise, it returns the left-hand operand.
14. Discuss the differences between never, unknown, and nullable types in TypeScript.
    Ans:
    never represents the type of values that never occur (e.g., functions that never return). unknown is a type-safe version of any where values need to be checked before using them. Nullable types allow variables to hold either a specific type or null/undefined.
## Practical Application and Best Practices:
15. When would you choose to use TypeScript over JavaScript in a project, and why?
    Ans:
    ypeScript is preferable for larger projects, teams, or scenarios requiring stronger type checking, better tooling, improved maintainability, and reduced chances of type-related errors.
16. Can you describe scenarios where TypeScript's features significantly enhance code quality and maintainability?
    Ans:
    TypeScript's features shine in scenarios where a large codebase needs better organization, when working with multiple developers, and in projects where catching errors at compile-time is crucial to reduce runtime issues.