# 🧠 Exhaustive TypeScript Interview Questions for All Frontend Developer Levels

This document aims to be a comprehensive collection of TypeScript interview questions, categorized by topic. Within each topic, questions progress from foundational (for junior developers) to advanced, scenario-based, and conceptual (for senior developers).

## 🔰 Core Concepts & Basics

1.  **What is TypeScript?** Explain its relationship to JavaScript. What are the main goals and benefits of using TypeScript?
2.  **How does TypeScript differ from JavaScript?** (Static typing, compilation step, features beyond current ECMAScript standards).
3.  **Why choose TypeScript over plain JavaScript?** Discuss advantages like improved code quality, maintainability, scalability, and team collaboration.
4.  **Is TypeScript a replacement for JavaScript?** Explain.
5.  **How do you install TypeScript?** How do you compile a TypeScript file to JavaScript (`tsc` command)?
6.  **What are the basic data types in TypeScript?** (e.g., `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`). How do these compare to JavaScript types?
7.  **What is type annotation in TypeScript?** Provide examples for variables, function parameters, and function return types.
8.  **What is type inference in TypeScript?** How does it work? When is it good to rely on it, and when should you use explicit annotations?
9.  **What is the `any` type?** When might it be used? What are its downsides, and why is its use generally discouraged?
10. **What is the `unknown` type?** How does it differ from `any`? Why is it a safer alternative to `any`? How do you work with values of type `unknown`?
11. **What is the `void` type?** When is it typically used (e.g., for functions that don't return a value)?
12. **What is the `never` type?** Explain its purpose and provide examples of functions that would return `never` (e.g., functions that always throw an error or have an infinite loop).
13. **How do you handle `null` and `undefined` in TypeScript?** Explain strict null checks (`strictNullChecks` compiler option).
14. **What are "literal types"?** (e.g., `'hello'`, `true`, `42`).
15. **What are "template literal types"?** How can they be used to model string patterns?
16. **What is the difference between `Array<T>` and `T[]` for defining array types?** Is there a preferred syntax?
17. **What are tuples in TypeScript?** How do they differ from arrays? Provide a use case.
18. **What are optional properties in objects/interfaces (`propertyName?: type`)?**
19. **What are readonly properties (`readonly propertyName: type`)?** How do they differ from `const`?

## 🖥️ (Interfaces & Type Aliases)

1.  **What are interfaces in TypeScript?** How are they used to define the shape of an object?
2.  **What are type aliases in TypeScript (`type Name = ...`)?** How can they be used?
3.  **What is the difference between an `interface` and a `type` alias?** When would you choose one over the other? (Discuss declaration merging for interfaces, extensibility, and use with primitives/unions/intersections for types).
4.  **Can interfaces extend other interfaces? Can type aliases?**
5.  **Can interfaces extend type aliases? Can type aliases extend interfaces?**
6.  **What are "index signatures" in interfaces/types?** (e.g., `[key: string]: any`). What are their use cases and potential pitfalls?
7.  **What are function types?** How can they be defined using interfaces or type aliases?
8.  **What are "hybrid types" (interfaces that describe objects that are both functions and have properties)?**
9.  **What is declaration merging for interfaces?** Provide an example. Does this apply to type aliases?

## ➡️ Enums

1.  **What are enums in TypeScript?** Why are they useful?
2.  **Explain numeric enums.** How are their values assigned by default? Can they be manually assigned?
3.  **Explain string enums.** What are their advantages over numeric enums (e.g., readability, debugging)?
4.  **What are heterogeneous enums?** (Mixing string and numeric members - generally discouraged).
5.  **What are `const enum`s?** How do they differ from regular enums at compile time? What are their benefits (e.g., inlining, performance)?
6.  **What are computed and constant members in enums?**
7.  **How can you get the string name of an enum member from its numeric value, and vice-versa (reverse mapping for numeric enums)?**
8.  **When might you prefer using string literal union types (e.g., `type Color = "red" | "green" | "blue"`) over enums?**

## 🛡️ Type Manipulation & Advanced Types

1.  **What is type assertion (or type casting) in TypeScript?** What are the two syntaxes (`<Type>value` and `value as Type`)? When is it used, and what are its risks?
2.  **What are union types (`|`)?** How are they used to allow a value to be one of several types?
3.  **What are intersection types (`&`)?** How are they used to combine multiple types into one? What happens if you intersect types with conflicting primitive properties?
4.  **What is "type narrowing"?** Explain common techniques for type narrowing (e.g., `typeof` checks, `instanceof` checks, truthiness checks, equality checks, `in` operator, discriminated unions, custom type guards).
5.  **What are "type guards"?** Explain built-in type guards and how to create custom type guards (using `is TypeName` predicate).
6.  **What are "discriminated unions" (or tagged unions)?** How do they work with a common literal property to enable powerful type narrowing in `switch` statements or `if/else` chains?
7.  **How can the `never` type be used for exhaustiveness checking in discriminated unions?**
8.  **What is the `as const` assertion?** What are its effects on object literals, arrays, and literal types? Why is it useful (e.g., for creating "const" enums with objects, or for more precise types)?
9.  **What are mapped types?** How do they allow you to create new types by transforming properties of an existing type (e.g., making all properties optional or readonly)?
10. **What are conditional types?** (`T extends U ? X : Y`). Provide examples of their use, such as creating types based on conditions or extracting type information.
11. **Explain the `infer` keyword within conditional types.** What is its purpose, and how can it be used to extract types from within other types?
12. **What are recursive types?** How can you define a type that refers to itself (e.g., for tree-like structures)?
13. **What are "variadic tuple types"?** How can they be used with spread syntax in tuple definitions?
14. **What is "branding" or "tagging" types?** How can it be used to simulate nominal typing in TypeScript's structural type system?

## ⚙️ Generics

1.  **What are generics in TypeScript?** Why are they important for creating reusable, type-safe components (functions, classes, interfaces)?
2.  **Provide an example of a generic function.** How does type inference work with generic type parameters?
3.  **Provide an example of a generic interface or class.**
4.  **What are generic constraints?** How can you use the `extends` keyword to limit the types that can be used as a type argument for a generic parameter?
5.  **How do you specify default types for generic type parameters?** (`<T = string>`).
6.  **Can you use multiple generic type parameters?**
7.  **How can generics be used with utility types to create powerful type transformations?**
8.  **Explain how type arguments are inferred in generic function calls. Can you explicitly pass type arguments?**

## 🛠️ Utility Types (Built-in)

_(Explain their purpose and provide examples for each)_

1.  **`Partial<T>`**
2.  **`Required<T>`**
3.  **`Readonly<T>`**
4.  **`Pick<T, K>`**
5.  **`Omit<T, K>`**
6.  **`Record<K, T>`** (where K is a union of string/number/symbol)
7.  **`Exclude<T, U>`**
8.  **`Extract<T, U>`**
9.  **`NonNullable<T>`**
10. **`Parameters<T>`** (where T is a function type)
11. **`ReturnType<T>`** (where T is a function type)
12. **`ConstructorParameters<T>`** (where T is a constructor type)
13. **`InstanceType<T>`** (where T is a constructor type)
14. **`Awaited<T>`** (for unwrapping Promise types)
15. **String manipulation utility types: `Uppercase<S>`, `Lowercase<S>`, `Capitalize<S>`, `Uncapitalize<S>`**
16. **How can you create your own custom utility types by combining these or using mapped/conditional types?**

## ✨ Classes & OOP

1.  **How are classes defined in TypeScript?** Explain `constructor`, properties, methods.
2.  **What are access modifiers in TypeScript classes?** (`public`, `private`, `protected`). How do they differ? Where can each be accessed?
3.  **What are `readonly` properties in classes?**
4.  **What are static members (properties and methods) in classes?** How are they accessed?
5.  **How does inheritance work with classes (`extends` keyword)?**
6.  **What is the `super()` call used for in a derived class constructor and for accessing base class methods?**
7.  **What are abstract classes and abstract methods?** When are they used? Can you instantiate an abstract class?
8.  **How can interfaces be used with classes (`implements` keyword)?** Can a class implement multiple interfaces?
9.  **Can a class extend another class and implement interfaces simultaneously?**
10. **Explain parameter properties in constructors** (e.g., `constructor(private name: string)`).
11. **How does `this` work in TypeScript classes, especially with methods and arrow functions within classes?**

## 📔 Decorators

_(Note: Decorators are an experimental feature and their syntax/behavior might change. Current date: May 2025)_

1.  **What are decorators in TypeScript?** What is their purpose (metaprogramming, adding annotations or modifying behavior of classes and members)?
2.  **How do you enable decorators in `tsconfig.json`?** (`experimentalDecorators`).
3.  **What are the different types of decorators?** (Class, Method, Accessor, Property, Parameter decorators).
4.  **Provide a simple example of a class decorator or a method decorator.**
5.  **How can decorator factories be used to customize decorators?**
6.  **What is the evaluation order of multiple decorators applied to a single declaration or within a class?**
7.  **What are some potential use cases for decorators?** (e.g., logging, dependency injection, data validation).
8.  **What is the relationship between TypeScript decorators and the ECMAScript proposals for decorators?**

## 📦 Modules & Namespaces

1.  **What is the module system in TypeScript?** How does it relate to ES Modules?
2.  **Explain `export` and `import` statements.** (Named exports, default exports, re-exports, namespace imports).
3.  **What are namespaces in TypeScript (`namespace X { ... }`)?** What was their original purpose (organizing code, avoiding global scope pollution pre-ES6 modules)?
4.  **What is the difference between TypeScript namespaces and ES Modules?** When should you prefer one over the other? (ES Modules are generally preferred for modern development).
5.  **What is module resolution in TypeScript?** Explain `classic` vs. `node` strategies.
6.  **What are ambient modules/declarations?** How do you declare types for modules that don't have their own TypeScript definitions (e.g., in a `d.ts` file)?
7.  **What is the `export =` and `import = require()` syntax?** When might you encounter it (e.g., when working with older CommonJS modules)?

## 📄 Declaration Files (`.d.ts`)

1.  **What are declaration files (`.d.ts`) in TypeScript?** What is their purpose?
2.  **How do you write a declaration file for a third-party JavaScript library that doesn't have its own types?**
3.  **What is DefinitelyTyped (`@types/package-name`)?** How does it help with using JavaScript libraries in TypeScript projects?
4.  **What is "declaration merging" in the context of interfaces and namespaces within declaration files?**
5.  **How can you declare global variables or types that are available throughout your project?** (e.g., using `declare global { ... }`).
6.  **What are ambient declarations (`declare var`, `declare function`, `declare module`)?**

## ⚙️ `tsconfig.json` & Compiler Options

1.  **What is the `tsconfig.json` file?** What is its primary role?
2.  **Explain some of the most important compiler options in `tsconfig.json`:**
    - `target`: (e.g., `ES5`, `ES2020`, `ESNext`)
    - `module`: (e.g., `CommonJS`, `ESNext`, `None`)
    - `outDir`: Output directory for compiled files.
    - `rootDir`: Root directory of source files.
    - `strict`: Enables all strict type-checking options.
    - `strictNullChecks`: Disallow `null` and `undefined` unless explicitly typed.
    - `noImplicitAny`: Raise error on expressions and declarations with an implied `any` type.
    - `esModuleInterop`: Enables compatibility with CommonJS modules using default imports.
    - `allowJs` / `checkJs`: Allowing/checking JS files in TS projects.
    - `sourceMap`: Generate sourcemap files for debugging.
    - `lib`: Specifies library files to be included in the compilation (e.g., `DOM`, `ES2020`).
    - `baseUrl` and `paths`: For path mapping/aliases.
    - `typeRoots` and `types`: To specify locations for type declarations.
    - `jsx`: JSX compilation mode.
3.  **How can you extend one `tsconfig.json` from another?**
4.  **What are `include` and `exclude` properties in `tsconfig.json` used for?**
5.  **How does TypeScript resolve modules?** (Briefly explain `moduleResolution` like `node` vs `classic`).

## 🔄 Interoperability with JavaScript

1.  **How can you gradually migrate a JavaScript project to TypeScript?** What are common strategies?
2.  **How can TypeScript consume JavaScript files?** (Using `allowJs`).
3.  **How can JavaScript consume TypeScript files?** (By compiling TS to JS).
4.  **What is JSDoc-based type checking?** How can you use JSDoc comments in `.js` files to get some benefits of TypeScript type checking without fully converting to `.ts`?
5.  **How do you handle third-party JavaScript libraries that don't have official TypeScript type definitions?** (DefinitelyTyped, writing custom `d.ts` files).

## 🌐 TypeScript with Frameworks & Runtimes (as of May 2025)

1.  **How is TypeScript commonly used with React?**
    - Typing props (`interface Props`, `type Props`).
    - Typing component state (`interface State`, `useState<Type>`).
    - Typing event handlers.
    - Using `React.FC` or `React.VFC` (though `React.FC` is less favored for children).
    - Typing React hooks (e.g., `useRef<Type>`).
    - JSX with TypeScript (`.tsx` files).
2.  **How is TypeScript used with Angular?** (Angular is built with TypeScript).
3.  **How is TypeScript used with Vue.js?** (Vue 3 has excellent TypeScript support).
    - Typing props, computed properties, methods in Options API or Composition API.
    - Using `<script lang="ts">`.
4.  **How do you integrate TypeScript with Node.js for backend development?**
    - Setting up `tsconfig.json` for Node.js (e.g., `module: "CommonJS"` or `"ESNext"` with appropriate settings).
    - Using `ts-node` for development.
    - Compiling to JS for production.
    - Typing Express.js routes and middleware.
5.  **What are some considerations when choosing module systems (`CommonJS` vs. `ESM`) in a Node.js TypeScript project?**
6.  **How do you set up a new TypeScript project from scratch?** (Install TS, create `tsconfig.json`, write code, compile).
7.  **What is the role of DefinitelyTyped (`@types/*`) when working with frameworks and libraries?**
8.  **How do you write unit tests for TypeScript code?** (Using Jest, Mocha, etc., with appropriate TypeScript setup like `ts-jest`).

## 🛠️ Tooling & Ecosystem

1.  **What is `tsc`?** (The TypeScript compiler).
2.  **What is `ts-node`?** How does it allow you to run TypeScript files directly without pre-compiling?
3.  **How do bundlers like Webpack, Rollup, Parcel, or Vite handle TypeScript?** (Usually via loaders or plugins like `ts-loader`, `esbuild`, or native support).
4.  **What is the role of Babel when working with TypeScript?** (Sometimes used for transpilation, especially if needing Babel plugins for other transformations, though `tsc` can handle most modern JS output).
5.  **How do you lint TypeScript code?** (ESLint with `@typescript-eslint/parser` and `@typescript-eslint/eslint-plugin`).
6.  **How do you format TypeScript code?** (Prettier).
7.  **How can source maps help in debugging TypeScript applications?**
8.  **What are project references in TypeScript?** How can they help manage large monorepos or multi-package projects?

## 💡 Advanced Concepts & Patterns

1.  **What is the difference between structural typing (duck typing) and nominal typing?** Which system does TypeScript use primarily? How can you achieve nominal-like typing if needed (e.g., using branded types)?
2.  **Explain control flow analysis in TypeScript.** How does the compiler use code flow to narrow types within conditional blocks?
3.  **How can you design type-safe APIs or libraries using TypeScript?**
4.  **Discuss strategies for managing and versioning shared types across multiple projects or microservices.** (e.g., private NPM packages, monorepos with shared type definitions).
5.  **What are some patterns for reducing type boilerplate in complex applications?** (e.g., effective use of generics, utility types, inference).
6.  **How can you model complex state machines or business logic safely using TypeScript's type system?** (e.g., discriminated unions for states, exhaustiveness checks).
7.  **How can you enforce specific business rules or constraints at the type level?**
8.  **What is "type-level programming" in TypeScript?** (Using the type system itself to perform computations or transformations at compile time – very advanced).
9.  **How does TypeScript handle function overloads?** How do you declare them, and what are the rules for implementation?
10. **What are some potential performance considerations when using TypeScript?** (Build time vs. runtime performance; `const enum`s).
11. **How do you debug type errors in complex TypeScript code?** (Understanding error messages, using "Go to Definition", simplifying code).

## 🌍 Real-World Scenarios & Problem Solving

1.  **You receive data from an API with a dynamic or unpredictable structure. How would you safely type and handle this data in TypeScript?** (e.g., using `unknown`, type guards, validation libraries like Zod or io-ts).
2.  **How would you approach refactoring a large JavaScript codebase to TypeScript? What are the key steps and challenges?**
3.  **You need to create a generic function that works with different data structures (e.g., arrays, objects) while maintaining type safety. How would you design it?**
4.  **A third-party library you're using has incorrect or incomplete type definitions. What are your options?** (Contributing to DefinitelyTyped, augmenting existing types, creating local `d.ts` files).
5.  **How do you ensure that changes to your type definitions don't break consuming parts of your application or other dependent projects (backward compatibility for types)?**
6.  **Describe a situation where TypeScript's type system significantly helped you catch a bug or improve code quality.**
7.  **How would you design types for a deeply nested and complex configuration object for an application?**
8.  **You need to write a utility function that transforms an object type by, for example, making all its properties functions that return the original property's type. How would you use mapped and conditional types to achieve this?**
9.  **How can TypeScript improve the developer experience (DX) in a large team?**
10. **What are some common pitfalls or anti-patterns to avoid when writing TypeScript?** (e.g., overuse of `any`, unnecessary type assertions, overly complex types that hinder readability).

---

This exhaustive list should cover a vast majority of TypeScript topics you might encounter. Remember to focus on understanding the "why" behind features and being able to articulate trade-offs and practical applications. Good luck!
