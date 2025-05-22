# Frontend Developer Interview FAQs: Trainee to Junior+ Levels (React Focused)

This document provides a focused list of frequently asked questions for frontend developer interviews, specifically tailored for trainee, intern, and junior (including junior-, junior, junior+) roles, with an emphasis on React and its ecosystem.

## Ⅰ. The Web & Internet 🌐🔗

This section covers foundational knowledge about how the internet and web technologies work.

### Web & Internet Fundamentals

- How does the internet work? (High-level overview)
- What is HTTP/HTTPS? Explain common HTTP methods (GET, POST - know these well; PUT, DELETE - be aware of).
- What are HTTP status codes? (e.g., know 200, 404, 500; be aware of 201, 400, 401, 403).
- What is DNS? How does DNS resolution work? (High-level).
- What is a domain name? What is hosting?
- What is a browser? How does it render a webpage? (Critical Rendering Path - very basic understanding).
- What are cookies? How are they used?
- What is `localStorage` vs `sessionStorage` vs `cookies`? (Basic differences, use cases like storing user preferences vs. session info).
- What is CORS (Cross-Origin Resource Sharing)? (Conceptual understanding of why it exists).
- What is a RESTful API? (Very basic understanding of what an API is and how you interact with it).
- Explain the Fetch API (how to make a simple GET request, how to get JSON data).
- What are HTTP headers? (Awareness, e.g., `Content-Type`).

### Web Performance (Focus on Concepts)

- Why is web performance important? (User experience).
- What are some common techniques to make a website load faster?
  - Optimizing images (compressing them, choosing appropriate formats like JPG/PNG/SVG).
  - Minifying CSS/JS (conceptual understanding).
  - Using a CDN (conceptual understanding).
  - Lazy loading images (conceptual, e.g., HTML `loading="lazy"` attribute).
- Explain the difference between `async` and `defer` attributes for script loading.

### Web Security (Focus on Awareness)

- What is Cross-Site Scripting (XSS)? (Basic understanding of the risk). How does React help prevent XSS by default (JSX escaping)?
- What is HTTPS and why is it important? (Secure communication).
- Why should you be careful when using `dangerouslySetInnerHTML` in React?

### Accessibility (a11y) (Focus on Basics)

- What is web accessibility (a11y)? Why is it important?
- How can semantic HTML contribute to accessibility?
- What is the importance of `alt` text for images?
- Why is keyboard navigation important? (Basic awareness).
- What are ARIA attributes? (Very basic awareness that they exist to help accessibility).

## Ⅱ. HTML (HyperText Markup Language) 🌐

This section focuses on HTML structure, semantics, and features relevant for junior roles.

- **What is HTML?** What does HTML stand for?
- What is the primary purpose of HTML in web development? Explain its relationship with CSS and JavaScript.
- What is an HTML element? Describe its common structure (opening tag, content, closing tag).
- What is the difference between an element and a tag?
- What are HTML tags? Are all tags paired? Give an example of an empty/void tag (e.g., `<img>`, `<br>`).
- What are HTML attributes? Provide examples and explain their purpose (e.g., `id`, `class`, `src`, `href`, `alt`).
- Describe the basic structure of an HTML document. What are the essential components (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`)?
- What is the purpose of the `<head>` tag? What kinds of things go in it (e.g., `<title>`, `<meta>`, `<link>`)?
- What is the purpose of the `<body>` tag?
- What does `<!DOCTYPE html>` declaration do? Why is it important?
- What are semantic HTML elements? Why are they important? (e.g., `<article>`, `<aside>`, `<nav>`, `<header>`, `<footer>`, `<main>`, `<section>`). Give a few examples.
- Explain the difference between `<div>` and `<span>`. When and why would you use each?
- How do you create a hyperlink in HTML? What is the primary attribute used (`href`)?
- How do you insert an image in HTML? What are the essential attributes for `<img>` (`src`, `alt`)?
- What are HTML lists? (ordered (`<ol>`), unordered (`<ul>`), list items (`<li>`)). How do you create them?
  - Can you nest lists within each other?
- How do you create a basic table in HTML? What are the essential tags (`<table>`, `<tr>`, `<td>`, `<th>`)?
- What are HTML forms? What is the purpose of the `<form>` tag?
- What are some common form input types? (e.g., `text`, `password`, `checkbox`, `radio`, `submit`, `button`, `file`).
- What is the `<label>` element used for in forms? How do you associate it with an input field (using `for` and `id`)? Why is this important for accessibility?
- How do you add comments in HTML?
- What is the difference between `id` and `class` attributes? Can an element have multiple classes? Can it have multiple IDs?
- What is the difference between block-level and inline elements? Provide examples of each.
- What happens if a browser encounters an HTML tag it doesn't recognize?
- How do you set the character encoding for an HTML document (e.g., `<meta charset="UTF-8">`)?
- What is the purpose of the `lang` attribute in the `<html>` tag?
- What are HTML entities? Why are they needed for special characters (e.g., `&nbsp;`, `&lt;`, `&gt;`, `&amp;`)?
- How do you embed audio and video in HTML5 (using `<audio>` and `<video>` tags)? What are some basic attributes like `src` and `controls`?
- What is the HTML5 `placeholder` attribute for input fields?
- What is the `required` attribute in form inputs?
- What is the `target="_blank"` attribute on an anchor tag used for? What are the security implications and how can they be mitigated (e.g., `rel="noopener noreferrer"`)? (Junior+ might know mitigation)

## Ⅲ. CSS (Cascading Style Sheets) 🎨

This section covers CSS fundamentals, layout, and responsiveness relevant for junior roles.

- What is CSS? What does CSS stand for and what is its primary role in web development?
- What are the different ways to include CSS in a web page? (inline, internal/embedded, external). What are the pros and cons of each?
- What is a CSS selector? Why are they important?
- Give examples of different types of selectors (element/type, class, ID).
- What is an attribute selector? (e.g., `[type="text"]`).
- What is the universal selector (`*`)?
- How do you group selectors? (e.g., `h1, h2, h3 { color: blue; }`).
- Explain the basic syntax of a CSS rule (Selector, declaration block, property, value).
- What is the CSS Box Model? Explain its components (content, padding, border, margin).
- What is the difference between `margin` and `padding`?
- What is CSS specificity? How is it calculated (general idea: inline > ID > class/attribute > element)?
- What happens when two CSS rules have the same specificity and target the same element? (Order of appearance).
- What are `block`, `inline`, and `inline-block` display values? How do they affect layout?
- How do you change the font family, size, and color of text using CSS?
- What is the `float` property used for? (Basic understanding, awareness of clearing floats).
- What is the `clear` property?
- What is the `z-index` property and how does it work? What is a stacking context (basic idea)?
- What are pseudo-classes (e.g., `:hover`, `:focus`, `:nth-child()`)?
- What are pseudo-elements (e.g., `::before`, `::after`)? What's the difference between single colon (`:`) and double colon (`::`) notation?
- How do you center a `div` element horizontally using `margin: auto;`? How might you center it vertically (Flexbox is a common answer)?
- What is the difference between `visibility: hidden;` and `display: none;`? What about `opacity: 0;`?
- What are CSS combinators? (Descendant ` `, Child `>`, Adjacent Sibling `+`, General Sibling `~` - be able to explain at least descendant and child).
- What does the `!important` rule do in CSS? Why should its use generally be minimized?
- How do you add comments in CSS?
- What is the difference between `rem`, `em`, and `px` units? When might you use `em` or `rem` over `px`? (Accessibility, scalability).
- What are `vh` and `vw` units?
- How do colors work in CSS? Explain different ways to define colors (keywords, hex, RGB, RGBA).
- Explain CSS positioning: `static`, `relative`, `absolute`. How does `absolute` positioning relate to its nearest positioned ancestor?
- What is `fixed` positioning?
- What is `sticky` positioning? (Junior+)
- What is Flexbox? Explain its main concepts (container, items, `display: flex`, `flex-direction`, `justify-content`, `align-items`).
- What are media queries? How are they used for basic responsive web design (e.g., changing layout based on screen width)?
- What is the `viewport` meta tag and why is it crucial for RWD? (`<meta name="viewport" content="width=device-width, initial-scale=1.0">`).
- How does `box-sizing: border-box;` work? Why is it often preferred?
- What are CSS transitions? (Basic idea of animating property changes smoothly).
- What is the CSS Cascade? (Order of precedence: origin/importance, specificity, source order).
- What is CSS Inheritance? Which properties are typically inherited (e.g., `color`, `font-family`)?
- What are CSS Custom Properties (CSS Variables)? How do you declare (`--variable-name: value;`) and use them (`var(--variable-name)`)? (Junior+)

## Ⅳ. JavaScript (JS) 🚀

This section delves into JavaScript fundamentals, asynchronous concepts, and DOM manipulation relevant for junior roles.

- What is JavaScript? Is it a compiled or interpreted language? Is it single-threaded?
- What are the different data types in JavaScript? List all primitive types (`string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, `null`) and explain what an object (non-primitive type) is.
- How do you declare a variable using `var`, `let`, and `const`? What are the differences regarding scope (global, function, block), hoisting, and re-assignment/re-declaration?
- What is scope in JavaScript? Explain global scope, function (local) scope, and block scope.
- What is "hoisting" in JavaScript? How does it affect `var` variable declarations and function declarations?
- What is the difference between `==` (loose equality) and `===` (strict equality)? Explain type coercion and why `===` is generally preferred.
- What is the difference between `null` and `undefined`?
- How do you write functions in JavaScript? (Function Declaration, Function Expression).
- What are arrow functions (ES6)? What is a key difference in how `this` behaves in arrow functions compared to traditional functions? (Lexical `this`).
- What are arrays in JavaScript? How do you create them? How do you access elements (by index)?
- List some common array methods: `push`, `pop`, `shift`, `unshift`, `slice`, `splice`, `forEach`, `map`, `filter`. Explain what `forEach`, `map`, and `filter` do and what they return.
- What are objects in JavaScript? How do you create them (object literal)? How do you access, add, and modify properties (dot notation vs. bracket notation)?
- How do you add comments in JavaScript? (single-line `//` and multi-line `/* */`).
- What is the DOM (Document Object Model)? How do you select HTML elements using JavaScript (e.g., `getElementById`, `getElementsByClassName`, `querySelector`, `querySelectorAll`)?
- How do you create and add HTML elements to the DOM using JavaScript (e.g., `createElement`, `appendChild`)?
- How do you modify element attributes and content (e.g., `element.attribute`, `innerHTML`, `textContent`)? What are the security implications of using `innerHTML`? (Risk of XSS if content isn't sanitized).
- What are events and event handling in JavaScript? How do you attach an event listener to an element (e.g., `element.addEventListener('click', functionName)`)? What is the event object?
- What is `JSON`? How do you parse JSON (`JSON.parse()`) and stringify JavaScript objects to JSON (`JSON.stringify()`)?
- How do you handle errors in JavaScript using `try...catch` blocks?
- What are JavaScript operators? Give examples of arithmetic (`+`, `-`, `*`, `/`, `%`), assignment (`=`, `+=`), comparison (`===`, `!==`, `>`, `<`), logical (`&&`, `||`, `!`), and the ternary operator (`condition ? exprIfTrue : exprIfFalse`).
- What does "short-circuiting" mean in the context of logical operators (`&&`, `||`)?
- What are truthy and falsy values in JavaScript? List all falsy values (`false`, `0`, `""` (empty string), `null`, `undefined`, `NaN`).
- What is "Strict Mode" (`'use strict';`)? What are some of its benefits (e.g., helps catch common coding bloopers, prevents or throws errors on "unsafe" actions)?
- What is the `typeof` operator? What does it return for different types (e.g., `typeof null` is "object" - a common gotcha)?
- Explain template literals (template strings) from ES6. What are their benefits (multiline strings, interpolation `${expression}`)?
- Explain destructuring assignment for arrays and objects (ES6).
- What are default parameters in functions (ES6)?
- What is the spread syntax (`...`) for arrays and objects (ES6)? How can it be used for copying or merging?
- What are rest parameters (`...`) in functions (ES6)?
- What is `this` keyword in JavaScript? Explain how its value is determined in different contexts:
  - Global context (window in browsers, or `undefined` in strict mode).
  - Function context (simple call - `undefined` in strict mode, global object otherwise).
  - As a method of an object (`this` refers to the object).
  - In an arrow function (`this` is lexically bound from its surrounding scope).
  - In a DOM event handler (`this` refers to the element that triggered the event, unless it's an arrow function).
- What are Promises? Explain their states (`pending`, `fulfilled`, `rejected`). How do you use `.then()` for success and `.catch()` for errors? (Basic usage for handling async operations like `Workspace`).
- What is `async/await` (ES2017)? How does it make working with Promises look more synchronous? How do you handle errors using `try...catch` with `async/await`?
- What is the Event Loop in JavaScript? (Very high-level: Call Stack, Web APIs, Callback Queue/Task Queue. Understand that JS is single-threaded but can perform non-blocking operations).
- What is event bubbling? (Basic concept: event travels up the DOM tree).
- What is `localStorage` and `sessionStorage`? How do they differ (persistence)? How do you use `setItem`, `getItem`, `removeItem`?
- What are closures? (Basic understanding: a function has access to its outer function's scope even after the outer function has returned). Give a simple example. (Junior+)

## Ⅴ. TypeScript (TS) 🔷

This section focuses on TypeScript's features and benefits relevant for junior roles.

- What is TypeScript? Why use it over JavaScript? (Static typing, better tooling, helps catch errors early).
- What are the basic types in TypeScript? (e.g., `string`, `number`, `boolean`, `any`, `void`, `null`, `undefined`). Be able to define them for variables.
- How do you define types for variables and function parameters/return values? (Type annotation, e.g., `let name: string = "John"; function greet(name: string): string { return "Hello " + name; }`).
- What are interfaces in TypeScript? How are they used to define the shape of an object?
- What are type aliases (`type Name = ...`) in TypeScript? How can they be used?
- What is a key difference between an `interface` and a `type` alias? (Interfaces can be merged, types are generally more flexible for unions/intersections).
- What are enums? (Numeric or string named constants).
- What is the `any` type? When might it be used (e.g., migrating JS code, third-party libraries without types)? Why is its use generally discouraged?
- What is type inference in TypeScript? How does it work (TS tries to figure out the type for you)?
- How do you compile a TypeScript file to JavaScript (`tsc filename.ts`)?
- What is the `tsconfig.json` file? (It configures the TypeScript compiler).
- What is the `unknown` type? How does it differ from `any` (it's safer because you must narrow it before use)?
- What is the `void` type? When is it typically used (for functions that don't return a value)?
- How do you define an array of a specific type (e.g., `number[]` or `Array<number>`)?
- What are tuples in TypeScript? (Fixed number of elements with known types, e.g., `[string, number]`).
- How do you define optional properties in objects/interfaces (using `?`, e.g., `propertyName?: type`)?
- How do you define readonly properties (`readonly propertyName: type`)?
- What are union types (`|`)? How are they used to allow a value to be one of several types (e.g., `string | number`)?
- What are type assertions (or type casting)? What are the two syntaxes (`<Type>value` and `value as Type`)? When might you use this (e.g., when you know more about the type than TS does)? What are its risks (it can hide real type errors)? (Junior+)
- What are generics in TypeScript? (Basic understanding: creating reusable components/functions that can work over a variety of types rather than a single one). Give a very simple example like an identity function `function identity<T>(arg: T): T { return arg; }`. (Junior+)

## Ⅵ. Data Structures & Algorithms (DSA) 📊

This section covers basic DSA concepts relevant to frontend development for junior roles.

- What is Big O notation? (Conceptual understanding: how algorithm performance scales with input size; e.g., O(1), O(n), O(n^2) - what they mean generally).
- Common data structures used in JavaScript:
  - **Arrays:** How do you add/remove elements? How do you access elements? (Awareness that some operations like adding to the beginning can be less performant).
  - **Objects:** How are they used for key-value storage? How do you access properties?
- What is recursion? (Basic idea: a function that calls itself, need a base case).
- How would you iterate over an array? (e.g., `for` loop, `forEach`).
- How would you iterate over an object's properties? (e.g., `for...in` loop, `Object.keys()`).
- (Junior+) Simple algorithm problems:
  - Reverse a string.
  - Check if a string is a palindrome.
  - Find the maximum value in an array of numbers.
  - Implement a function to sum all numbers in an array.
  - FizzBuzz problem.

## Ⅶ. React ⚛️

This section is dedicated to React core concepts relevant for junior roles.

- **What is React?** What problems does it solve? Explain its primary purpose and philosophy (declarative, component-based).
- **What is JSX?** How does it differ from HTML? How does JSX get transpiled (e.g., by Babel into `React.createElement()` calls)? Can you use React without JSX? (Yes, but it's less common).
- **What is a React Component?**
  - How do you create Functional Components?
  - What was a Class Component? (Awareness, but functional components are preferred).
- **What are props?** How are they passed from a parent component to a child component? Are props mutable or immutable within the child component? (Immutable).
- **What is state in a React component?** How is it different from props? How is state managed in a functional component (using the `useState` Hook)?
- **How do you update state using `useState`?** (e.g., `const [count, setCount] = useState(0); setCount(newCount);`). Does `setCount` update state immediately (synchronously) or is it asynchronous? (Asynchronous, batched).
- **How do you handle events in React?** (e.g., `onClick`, `onChange`). How do you pass event handlers as props? What are React's synthetic events? (A cross-browser wrapper around the native event).
- **What is conditional rendering in React?** Describe different ways to achieve it (e.g., `if/else` statements, ternary operator `condition ? <JSX1> : <JSX2>`, logical `&&` operator `condition && <JSX>`).
- **How do you render lists of items in React?** (Using array methods like `.map()`). What is the significance of the `key` prop when rendering lists? Why should keys be stable and unique among siblings?
- **What is the Virtual DOM (VDOM)?** (Conceptual understanding: an in-memory representation of the real DOM, React uses it to optimize updates by diffing and batching changes).
- What was `create-react-app` (CRA)? (Awareness that it was a common way to start React projects, Vite is now often preferred).
- **What are React Fragments (`<React.Fragment>` or the short syntax `<>...</>`)?** Why are they useful (avoiding extra wrapper `div`s in the DOM)?
- How do you import and export components in JavaScript modules (ES6 `import`/`export`)?
- What is the `children` prop? How is it used (e.g., `<WrapperComponent>Children go here</WrapperComponent>`)?
- Explain the `useEffect` Hook.
  - What are its common use cases for side effects (e.g., data fetching after render, setting up subscriptions, manually changing the DOM)?
  - What is the dependency array (`[]`, `[dep1, dep2]`, or no array)? How does it control when the effect runs?
    - `[]`: Runs once after the initial render.
    - `[dep1, dep2]`: Runs after the initial render and whenever `dep1` or `dep2` changes.
    - No array: Runs after every render (use with caution).
  - How do you perform a cleanup in `useEffect` (by returning a function from the effect)? When does this cleanup function run (before the component unmounts, or before the effect runs again if dependencies changed)?
- How do you fetch data in a React component? (Typically using `useEffect` to trigger the fetch and `useState` to store the data, loading state, and error state).
- What are controlled components in forms? (Input form element whose value is controlled by React state). How do you implement one with `useState` and an `onChange` handler?
- How do you style React components? (Basic CSS stylesheets imported, inline styles - be aware of syntax differences `{}` and camelCase).
- (Junior+) What is the `useContext` Hook? How can it help avoid prop drilling for sharing data like themes or user authentication status?
- (Junior+) What are refs (`useRef`)? What's a common use case (e.g., accessing underlying DOM elements to manage focus or trigger animations)?

## Ⅷ. Next.js NEXT

This section covers Next.js fundamentals relevant for junior roles, especially if the role mentions Next.js.

- What is Next.js? Why might you choose it over a simpler React setup like Create React App or Vite? (Key benefits like pre-rendering (SSR/SSG), file-system routing, API routes, image optimization).
- What are some main features of Next.js? (Mention pre-rendering, routing, API routes).
- How does file-system routing work in Next.js? (Basic idea: files in the `pages` directory (or `app` directory for newer versions) become routes).
- What is the difference between a page (a file in `pages` or `app` that defines a route) and a regular React component in Next.js?
- How do you create dynamic routes in Next.js? (e.g., `pages/posts/[id].js` or `app/posts/[id]/page.js`).
- What is the `next/link` component used for? Why is it preferred over a regular `<a>` tag for internal navigation within a Next.js app (client-side navigation, prefetching)?
- What is pre-rendering in Next.js? What are the two forms of pre-rendering Next.js supports (Static Site Generation - SSG, and Server-Side Rendering - SSR)? (Conceptual understanding).
- (For Pages Router) What is `getStaticProps`? When does it run (at build time for SSG)? What is it used for (fetching data to pre-render a page)?
- (For Pages Router) What is `getServerSideProps`? When does it run (on each request for SSR)? What is it used for?
- (For App Router - Junior+) What are Server Components and Client Components? What does the `"use client"` directive do? (Very basic understanding that Server Components can run on the server and fetch data, Client Components run in the browser and can use state/effects).
- What are API Routes (in `pages/api/`) or Route Handlers (in `app/api/` or `app/.../route.js`) in Next.js? What are they used for (creating backend API endpoints within your Next.js app)?
- How do you create a new Next.js application (using `create-next-app`)?
- What is hydration in the context of Next.js? (The process of making the server-rendered HTML interactive on the client-side by attaching JavaScript event handlers).
- (Junior+) How does `next/image` help with image optimization? (Automatic resizing, format optimization, lazy loading by default).

## Ⅸ. React Ecosystem & Libraries 📚

This section explores awareness of common libraries and tools used with React for junior roles.

### State Management

- When might you need something more than `useState` for managing state? (e.g., when state needs to be shared between many components that are not directly related, or when state logic becomes very complex).
- What is the React Context API? How can it be used for sharing state without prop drilling? (Basic understanding of `createContext`, Provider, and `useContext`).
- Have you heard of Redux or other state management libraries like Zustand, Jotai, or Recoil? What problem do they generally try to solve? (Centralized state management for larger applications - conceptual awareness is sufficient for most junior roles unless specified).

### Routing

- What is client-side routing? Why is it used in Single Page Applications (SPAs)? (To navigate between "pages" without a full page reload).
- Have you used React Router? What are its main components like `<BrowserRouter>`, `<Route>`, and `<Link>` used for?
- How do you define a route that matches a specific URL path and renders a component?

### Data Fetching

- How do you typically fetch data from an API in a React application? (Using the `Workspace` API or a library like Axios within `useEffect`).
- Have you heard of libraries like SWR or React Query (TanStack Query)? What benefits might they offer for data fetching (e.g., caching, automatic refetching - conceptual awareness)?

### UI Libraries

- Have you worked with any React UI component libraries like Material UI, Ant Design, or Chakra UI? What are the benefits of using such libraries (pre-built, styled components, consistency)?
- What is Tailwind CSS? (Utility-first CSS framework - basic awareness of the concept).

### Form Handling

- What are some challenges when working with forms in React? (Managing input state, handling submission, validation).
- Have you heard of form libraries like Formik or React Hook Form? What problems do they help solve? (Simplify form state management and validation - conceptual awareness).

## Ⅹ. Design Patterns & Refactoring 🏗️

This section touches upon basic design principles and code improvement concepts for junior roles.

### Design Patterns (Conceptual Awareness)

- What does it mean to write reusable components in React? (Creating components that can be used in multiple places with different props).
- (Junior+) Have you heard of any common React patterns like Higher-Order Components (HOCs) or Custom Hooks? What is a Custom Hook used for (reusing stateful logic)?

### Refactoring

- What is code refactoring? (Improving code structure and readability without changing its external behavior).
- Why is it important to write clean and readable code? (Maintainability, easier for others to understand).
- What does DRY (Don't Repeat Yourself) principle mean in coding?

## XI. Testing 🧪

This section covers basic testing concepts for junior roles.

- Why is testing important in software development? (Helps catch bugs, ensures code works as expected, gives confidence when refactoring).
- What are unit tests? (Testing small, isolated pieces of code, like individual functions or components).
- Have you heard of Jest? What is it used for in the React ecosystem (a popular testing framework for JavaScript and React)?
- Have you heard of React Testing Library (RTL)? What is its main idea (testing components the way users interact with them)?
- How do you check if a component renders some text or an element in a test? (Basic idea of querying for elements and making assertions).
- What is an "assertion" in testing? (A statement that checks if a certain condition is true, e.g., `expect(value).toBe(expectedValue)`).

## XII. Tooling 🛠️

This section covers awareness of essential tools in frontend development for junior roles.

- **Package Managers:**
  - What is `npm` or `yarn`? What are they used for (installing and managing project dependencies)?
  - What is a `package.json` file? What kind of information does it hold (project metadata, dependencies, scripts)?
  - What is the `node_modules` folder?
- **Module Bundlers (Conceptual):**
  - Have you heard of Webpack or Vite? What is the general purpose of a module bundler (to bundle JavaScript modules and other assets for the browser)?
- **Transpilers (Conceptual):**
  - What is Babel? Why is it often used in modern JavaScript projects (to convert newer JavaScript syntax into older versions that more browsers can understand, and to transpile JSX)?
- **Linters & Formatters:**
  - What is ESLint? What is Prettier? What is their purpose (ESLint for finding code errors and enforcing code style, Prettier for automatically formatting code)? Why are they useful (code quality, consistency)?
- **Version Control (Git):**
  - What is Git? Why is it used for version control?
  - What are some basic Git commands you have used or know? (e.g., `git clone`, `git add`, `git commit`, `git push`, `git pull`, `git branch`, `git checkout`, `git merge`).
  - What is a Git branch? Why are branches useful (working on features in isolation)?
  - What is a "commit" in Git?
  - What is GitHub/GitLab/Bitbucket? (Platforms for hosting Git repositories and collaboration).
- **Developer Tools (Browser):**
  - How do you use your browser's Developer Tools?
    - Inspecting HTML and CSS (Elements panel).
    - Using the Console (for logging messages, errors, running simple JS).
    - Checking network requests (Network panel - basic understanding).
  - What are React DevTools? How can they help when working with React components (inspecting component hierarchy, props, state)?

## XIII. Live Coding Questions 💻

For junior levels, live coding questions usually focus on fundamentals and simple component building.

- **UI Component Implementation (React):**
  - Build a simple Counter component (with increment/decrement buttons, displaying the count).
  - Build a Toggle/Switch component (displays "ON"/"OFF" or changes style based on a boolean state).
  - Create an input field that updates a piece of state as the user types, and display the typed text elsewhere on the page.
  - Render a list of items (e.g., strings from an array) as `<li>` elements.
  - Conditionally render a message if a certain condition (e.g., a boolean state variable) is true.
- **JavaScript Fundamentals:**
  - Write a function that takes an array of numbers and returns their sum.
  - Write a function that reverses a given string.
  - Write a function that filters an array to only include even numbers.
  - FizzBuzz: Loop from 1 to 100. Print "Fizz" for multiples of 3, "Buzz" for multiples of 5, and "FizzBuzz" for multiples of both. Otherwise, print the number.
- **HTML/CSS (Less common for live coding, but possible):**
  - Create the HTML structure for a simple card component (e.g., image, title, description).
  - Write CSS to style a simple button or center an element on the page.

**Tips for Junior Live Coding:**

- **Think Aloud:** Explain what you are trying to do.
- **Ask Clarifying Questions:** If the problem isn't clear, ask.
- **Start with the Simplest Working Solution:** Get something basic on the screen, then improve it.
- **Syntax is Okay to Forget (a little):** Interviewers understand you might not remember every exact piece of syntax under pressure, especially for very junior roles. Focus on the logic and concepts. They are more interested in your problem-solving approach.
- **Basic TypeScript:** If the role involves TypeScript, try to add simple type annotations for props and state.

## XIV. Behavioral & Situational Questions 🤔

These questions assess your enthusiasm, learning ability, and how you might fit into a team.

- Why are you interested in frontend development?
- Why are you interested in this role/company?
- How do you like to learn new things?
- Tell me about a project you've worked on (even personal or academic) that you're proud of. What did you do? What did you learn?
- How do you approach a problem you don't know how to solve?
- Do you prefer working alone or in a team? Why?
- What are your strengths? What is an area you'd like to improve? (Be honest but positive).
- Do you have any questions for me/us? (Always prepare a few thoughtful questions about the role, team, company culture, or technologies they use).

This refocused list should be much more manageable for preparing for trainee to junior+ level interviews. Good luck!
