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


# Type Assertion, Type Narrowing, and Generics:
1. Explain the difference between type assertion and type casting in TypeScript.
    Answer: Type assertion is a way to tell the compiler about the type of a variable, while type casting refers to converting one type to another in other languages like C#. In TypeScript, type assertion uses the as keyword or angle brackets < > to inform the compiler about a specific type, but it doesn't perform any runtime checking or transformations.
2. How does type narrowing work in TypeScript? Provide examples.
    Answer: Type narrowing allows narrowing down the type of a variable within a conditional block based on checks like type guards (typeof, instanceof, etc.) or truthiness checks. For example:
   ```typescript
    function printValue(value: string | number) {
        if (typeof value === 'string') {
            console.log(value.toUpperCase());
        } else {
            console.log(value.toFixed(2));
        }
    }
3. What are the key differences between interfaces and types in TypeScript? When would you choose one over the other?
    Answer: Interfaces and types in TypeScript are similar but have some differences. Interfaces are mainly used for defining object shapes and can be extended or implemented, while types are more flexible and can define union types, intersection types, and more complex structures. You might choose interfaces for defining object shapes and contracts while using types for broader type definitions.
4. What are generics in TypeScript, and why are they beneficial in writing reusable code?
    Answer: Generics allow writing flexible and reusable components, functions, or classes by letting types be specified later. They provide better type safety, enable writing more adaptable code, and avoid code duplication by allowing different types to be used in a single component.
    Advanced Generics and Constraints:
5. How do you use generics with interfaces in TypeScript? Provide an example.
    Answer: Generics can be applied to interfaces to create reusable interfaces that can work with different types. Example:
    ```typescript
    interface Box<T> {
        value: T;
    }
    let numberBox: Box<number> = { value: 10 };
6. Explain how you can create functions with generics. What advantages does it offer?
    Answer: Functions with generics allow writing functions that can work with different types, enhancing reusability and type safety. Example:
    ```typescript
    function identity<T>(arg: T): T {
        return arg;
    }
    let result = identity<string>('Hello');
7. Describe constraints in TypeScript generics and why they are used.
    Answer: Constraints in generics restrict the types that can be used in a generic component. They ensure that only specified types that meet certain criteria can be used, enhancing type safety and avoiding unexpected behaviors.
8. Illustrate the usage of the keyof constraint in TypeScript.
    Answer: The keyof constraint in TypeScript allows working with keys of an object type. It produces a union type of all the keys in the specified object type. Example:
    ```typescript
    interface Person {
        name: string;
        age: number;
        address: string;
    }
    type PersonKeys = keyof Person; // PersonKeys is 'name' | 'age' | 'address'
## Asynchronous Programming and Advanced Types:
9. How do you handle asynchronous operations in TypeScript? Discuss async/await and Promises.
    Answer: Asynchronous operations in TypeScript can be handled using async/await syntax for cleaner asynchronous code or by using Promises to manage asynchronous tasks and handle results or errors.
10. Explain conditional types in TypeScript and where they might be useful in practical scenarios.
    Answer: Conditional types allow creating types based on conditions. They are useful in scenarios where types need to be determined dynamically based on specific conditions or constraints, providing flexibility in typing.
11. Describe the concept of mapped types in TypeScript and how they can be applied.
    Answer: Mapped types in TypeScript allow transforming one type into another by iterating over the keys in an existing type. They can create new types based on existing ones, often used to create read-only or optional versions of types.
12. What are utility types in TypeScript? Can you provide examples of commonly used utility types?
    Answer: Utility types in TypeScript are predefined generic types that provide commonly needed functionality for working with types. Examples include 
    ```typescript
    Partial<T>, Pick<T, K>, Record<K, T>, Readonly<T>, etc.
## Application and Practical Usage:
13. When would you prefer using conditional types over other types of type definitions in TypeScript?
    Answer: Conditional types are preferable when types need to be determined dynamically based on specific conditions or when creating flexible, reusable types that depend on certain conditions or constraints.
14. Illustrate how you might use mapped types to create a new type based on an existing type in a real-world scenario.
    Answer: For instance, mapping a type to create a read-only version:
    ```typescript
    interface Product {
        name: string;
        price: number;
    }
    type ReadonlyProduct = Readonly<Product>;
15. Discuss scenarios where utility types such as Partial, Pick, or Record would be most helpful in TypeScript development.
    Answer:
    ```typescript
    Partial<T>: Useful when you need to make all properties of a type optional.
    Pick<T, K>: Handy for creating new types by picking specific properties from an existing type.
    Record<K, T>: Helpful for creating a type with specific keys and a corresponding value type.    

# Introduction to OOP:
1. What is Object-Oriented Programming (OOP), and what are its core principles?
    Answer: OOP is a programming paradigm centered around objects that encapsulate data and behavior. Its core principles include encapsulation, inheritance, polymorphism, and abstraction.
## Class and Object:
2. Explain the difference between a class and an object in OOP.
    Answer: A class is a blueprint/template that defines the properties and behaviors common to a set of objects. An object is an instance of a class, representing a specific entity with its own set of properties and behaviors.
## Inheritance:
3. How does inheritance work in OOP, and what are its benefits?
    Answer: Inheritance allows a new class (subclass/derived class) to inherit properties and behaviors from another class (superclass/base class). Benefits include code reuse, extensibility, and hierarchical organization of classes.
## Type Guards and Access Modifiers:
4. Explain the use of type guards in TypeScript, specifically using typeof, in, and instanceof.
    Answer: Type guards like typeof and instanceof help narrow down types, ensuring safer operations. typeof checks the type of a variable, instanceof checks if an object is an instance of a particular class, and in checks if a property exists in an object.
5. What are access modifiers in OOP, and how do they control access to class members?
    Answer: Access modifiers (e.g., public, private, protected) dictate the visibility of class members. public allows access from anywhere, private restricts access only within the class, and protected allows access within the class and its subclasses.
## Getters, Setters, and Statics:
6. Explain the usage and purpose of getters and setters in OOP.
    Answer: Getters and setters are methods used to retrieve and assign values to private properties, allowing controlled access and manipulation of class fields.
7. What are static methods or properties in OOP? How are they different from instance methods/properties?
    Answer: Static methods/properties belong to the class itself rather than instances. They're accessed using the class name and are shared among all instances, unlike instance methods/properties which are specific to each object.
## Polymorphism, Abstraction, and Encapsulation:
8. Describe polymorphism in OOP and provide examples of its implementation.
    Answer: Polymorphism allows objects of different classes to be treated as objects of a common superclass. Examples include method overriding and method overloading.
9. What is abstraction in OOP, and why is it essential?
 ** Answer: Abstraction focuses on hiding unnecessary implementation details while showcasing only essential features. It simplifies complex systems by displaying only relevant information to the user.
10. Explain encapsulation in OOP and its significance.
vbnet
    **
    ```typescript
    - **Answer:** Encapsulation involves bundling the data and methods that o