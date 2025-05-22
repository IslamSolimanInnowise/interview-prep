# Frontend Developer Interview FAQs (React Focused)

This document provides a comprehensive list of frequently asked questions for frontend developer interviews, with a focus on React. Questions range from trainee to architect levels, presented in a suggested study order.

## Ⅰ. The Web & Internet 🌐🔗

### Web & Internet Fundamentals

- How does the internet work? (High-level overview)
- What is HTTP/HTTPS? Explain common HTTP methods (GET, POST, PUT, DELETE, PATCH, etc.).
- What are HTTP status codes? (e.g., 200, 201, 400, 401, 403, 404, 500)
- What is DNS? How does DNS resolution work?
- What is a domain name? What is hosting?
- What is a browser? How does it render a webpage? (Critical Rendering Path)
- What are cookies? How are they used? What are their security implications?
- What is `localStorage` vs `sessionStorage` vs `cookies`?
- What is CORS (Cross-Origin Resource Sharing)? How do you handle it?
- What is RESTful API design?
- What is GraphQL? How is it different from REST? (More relevant for mid/senior)

### Web Performance

- Why is web performance important?
- What are Core Web Vitals (LCP, FID/INP, CLS)?
- How do you measure web performance? (Lighthouse, WebPageTest, DevTools)
- What are common techniques to optimize website loading speed?
  - Minification, compression (Gzip, Brotli), image optimization (formats like WebP, responsive images), caching (browser, CDN), code splitting, lazy loading, reducing HTTP requests.
- What is a CDN (Content Delivery Network)?
- How does browser rendering impact performance? (Reflow/Layout, Repaint/Composite)
- (Architect Level) How do you establish a performance budget? How do you monitor and maintain performance over time for a large application?

### Web Security

- What are common web security vulnerabilities? (XSS, CSRF, SQL Injection - though latter is backend, understanding helps)
- How can you prevent XSS (Cross-Site Scripting) on the frontend? (Sanitizing input, Content Security Policy)
- What is CSRF (Cross-Site Request Forgery)? How can it be mitigated? (Anti-CSRF tokens)
- What is Content Security Policy (CSP)?
- What is HTTPS and why is it important?
- What are JWTs (JSON Web Tokens)? How are they used for authentication?
- What are security considerations for storing sensitive data on the client-side?
- (Architect Level) How do you design a secure frontend architecture? What are threat modeling and secure coding practices?

### Accessibility (a11y)

- What is web accessibility (a11y)? Why is it important?
- What are WCAG (Web Content Accessibility Guidelines)?
- What are ARIA (Accessible Rich Internet Applications) attributes? When and how to use them?
- How do you make web applications accessible to keyboard users?
- How do you test for accessibility? (Automated tools, manual testing, screen readers)
- What are common accessibility issues and how to fix them? (e.g., color contrast, missing alt text, focus management)
- (Architect Level) How do you embed accessibility into the development lifecycle and company culture?

## Ⅱ. HTML (HyperText Markup Language) 🌐

### HTML - Trainee/Junior Level

- What is HTML?
- What is the basic structure of an HTML document?
- What are HTML tags and elements? Give some examples of common tags.
- What is the difference between an element and a tag?
- What are HTML attributes? Give an example.
- What is the purpose of the `<head>` tag?
- What is the purpose of the `<body>` tag?
- What are semantic HTML elements? Why are they important? (e.g., `<article>`, `<aside>`, `<nav>`, `<header>`, `<footer>`)
- Explain the difference between `<div>` and `<span>`.
- How do you create a hyperlink in HTML?
- How do you insert an image in HTML? What are the essential attributes for `<img>`?
- What are HTML lists? (ordered, unordered, definition)
- How do you create a table in HTML?
- What are HTML forms? What are some common form input types?
- What is the `<!DOCTYPE html>` declaration for?
- What are comments in HTML?
- What is the difference between `id` and `class` attributes?

### HTML - Mid Level

- What is the difference between `GET` and `POST` methods in HTML forms?
- Explain the purpose and usage of `data-*` attributes.
- What are HTML entities? Give an example.
- How can you embed audio and video in HTML5?
- What is the `localStorage` and `sessionStorage` in HTML5? How do they differ?
- Explain the `<canvas>` vs `<svg>` elements. When would you use one over the other?
- What is the importance of the `alt` attribute on `<img>` tags?
- How do you make a website responsive using HTML and CSS (meta viewport tag)?
- What are `<iframe>` elements and what are their security implications?
- What is the purpose of `aria-*` attributes in HTML? (Accessibility)
- Explain the concept of character encoding in HTML (e.g., UTF-8).

### HTML - Senior/Architect Level

- Discuss the evolution of HTML (HTML4 vs HTML5). What are some key new features in HTML5?
- How can HTML be optimized for search engines (SEO)?
- Explain Shadow DOM. How does it relate to Web Components?
- Discuss the performance implications of different HTML structures and how to optimize them.
- How do you handle internationalization (i18n) and localization (l10n) at the HTML level?
- What are Progressive Web Apps (PWAs) and how does HTML structure contribute to them (e.g., manifest file)?
- Discuss strategies for handling offline capabilities in web applications using HTML5 APIs.
- How would you design an HTML structure for a highly scalable and maintainable large application?
- Discuss the security aspects related to HTML (e.g., preventing XSS by sanitizing user input rendered in HTML).

## Ⅲ. CSS (Cascading Style Sheets) 🎨

### CSS - Trainee/Junior Level

- What is CSS?
- What are the different ways to include CSS in a web page? (inline, internal, external)
- What is a CSS selector? Give examples of different types of selectors (element, class, ID, attribute).
- What is the CSS Box Model? Explain its components (content, padding, border, margin).
- What is the difference between `margin` and `padding`?
- What is CSS specificity? How is it calculated?
- What are `block`, `inline`, and `inline-block` display values?
- How do you change the font family and color of text?
- What is the `float` property used for?
- What is the `z-index` property and how does it work?
- What are pseudo-classes (e.g., `:hover`, `:focus`) and pseudo-elements (e.g., `::before`, `::after`)?
- How do you center a `div` element horizontally?
- What is the difference between `visibility: hidden;` and `display: none;`?

### CSS - Mid Level

- Explain CSS positioning (static, relative, absolute, fixed, sticky).
- What is Flexbox? Explain its main concepts (container, items, main axis, cross axis).
- What is CSS Grid Layout? How does it differ from Flexbox?
- What are media queries? How are they used for responsive web design?
- What are CSS variables (custom properties)? How do you use them?
- Explain the concept of `BEM` (Block, Element, Modifier) or other CSS methodologies.
- What are CSS preprocessors (e.g., Sass, LESS)? What are their advantages?
- How does `box-sizing: border-box;` work? Why is it useful?
- What are CSS transitions and animations?
- Explain the `!important` keyword in CSS and when (not) to use it.
- What are some techniques for hiding elements in CSS, and what are their implications for accessibility and layout?
- How do you handle browser compatibility issues in CSS?
- What is "critical CSS"?

### CSS - Senior/Architect Level

- Discuss advanced CSS layout techniques and when to use them (e.g., multi-column layout, writing modes).
- How would you structure CSS for a large-scale application? (e.g., CSS-in-JS, CSS Modules, Atomic CSS/Utility-first CSS like Tailwind CSS).
- Explain CSS performance optimization techniques (e.g., reducing selectors complexity, avoiding reflows/repaints).
- How does the browser render CSS? Explain the CSSOM.
- Discuss the pros and cons of different CSS architectures.
- How can CSS be used to improve website accessibility beyond basic ARIA?
- What is "containment" in CSS (`contain` property)?
- Discuss the future of CSS (e.g., Houdini, new CSS features).
- How would you design a theming system using CSS?
- Explain the concept of "CSS Custom Paint API" (Houdini).
- How do you approach CSS refactoring in a legacy project?

## Ⅳ. JavaScript (JS) 🚀

### JavaScript - Trainee/Junior Level

- What is JavaScript?
- What are the different data types in JavaScript?
- How do you declare a variable (using `var`, `let`, `const`)? What are the differences?
- What is scope in JavaScript (global, function, block)?
- What is hoisting?
- What is the difference between `==` and `===`?
- What are `null` and `undefined`?
- How do you write a function in JavaScript?
- What are arrays and objects? How do you access their elements/properties?
- What are common array methods? (e.g., `push`, `pop`, `forEach`, `map`)
- How do you add comments in JavaScript?
- What is the DOM? How do you interact with it using JavaScript?
- What are events and event handling in JavaScript? (e.g., `click`, `mouseover`)
- What is `JSON`?
- How do you handle errors in JavaScript (try...catch)?

### JavaScript - Mid Level

- Explain closures in JavaScript. What are their use cases?
- What is `this` keyword in JavaScript? How does its value change? (global, object method, function, arrow function, event listener)
- Explain prototypes and prototypal inheritance.
- What are ES6+ features you use regularly? (e.g., arrow functions, template literals, destructuring, spread/rest operators, modules)
- What are Promises? How do they work? How do they compare to callbacks?
- What is `async/await`? How does it simplify asynchronous code?
- Explain event bubbling and event capturing. What is event delegation?
- What is the Event Loop in JavaScript? Explain its components (Call Stack, Web APIs, Callback Queue/Task Queue, Microtask Queue).
- What are higher-order functions?
- What are pure functions?
- Explain `map`, `filter`, `reduce` array methods in detail.
- What are JavaScript modules (ES6 modules)? How do they work?
- What is strict mode (`'use strict'`)?
- How do you perform deep vs. shallow copying of objects/arrays?
- What are common ways to deal with `this` context in callbacks or methods? (`.bind()`, arrow functions)

### JavaScript - Senior Level

- Explain JavaScript's memory management (garbage collection).
- What are generators and iterators?
- What are `WeakMap` and `WeakSet`? How do they differ from `Map` and `Set`?
- Explain `Symbol` type and its use cases.
- Discuss performance optimization techniques in JavaScript (e.g., debouncing, throttling, memoization, minimizing DOM manipulation).
- What are Service Workers? How do they enable PWAs?
- What are WebSockets? How do they differ from HTTP?
- Explain common JavaScript design patterns (e.g., Module, Singleton, Observer, Factory).
- How does JavaScript handle concurrency if it's single-threaded?
- What are Typed Arrays?
- Discuss security considerations in JavaScript (XSS, CSRF prevention techniques on the client-side).
- How would you manage state in a complex vanilla JavaScript application?
- What is Functional Programming vs Object-Oriented Programming in JavaScript?
- Explain Proxy objects.

### JavaScript - Architect Level

- Discuss strategies for building large-scale, maintainable JavaScript applications.
- How would you design an API for a JavaScript library or framework?
- Explain the trade-offs of different module systems (ESM, CommonJS, AMD, UMD) in various environments.
- Discuss the role of JavaScript engines (like V8) and their optimization techniques.
- How do you approach performance profiling and debugging in complex JavaScript applications?
- What are the challenges and solutions for micro-frontend architectures using JavaScript?
- Discuss JavaScript's impact on SEO and how to mitigate potential issues (e.g., for SPAs).
- How would you set up coding standards, linting, and type checking for a large JavaScript project?
- Discuss the implications of JavaScript fatigue and how to manage dependencies effectively.
- What are some advanced error handling and logging strategies for frontend applications?
- How does JavaScript interoperate with WebAssembly? What are the benefits?

## Ⅴ. TypeScript (TS) 🔷

### TypeScript - Trainee/Junior Level

- What is TypeScript? Why use it over JavaScript?
- What are the basic types in TypeScript? (e.g., `string`, `number`, `boolean`, `any`, `void`)
- How do you define types for variables and function parameters/return values?
- What are interfaces in TypeScript? How are they different from `type` aliases?
- What are enums?
- What is `any` type and why should it be avoided?
- How do you compile TypeScript to JavaScript?
- What is a `tsconfig.json` file?

### TypeScript - Mid Level

- Explain generics in TypeScript. Provide a use case.
- What are union types and intersection types?
- What are literal types?
- Explain type inference in TypeScript.
- What are access modifiers (`public`, `private`, `protected`) in TypeScript classes?
- How do you work with `null` and `undefined` in TypeScript (strict null checks)?
- What are type assertions (casting)? (e.g., `as`, `<>`) When are they useful and when are they risky?
- How do you type objects with optional properties?
- What are mapped types? (e.g., `Partial<T>`, `Readonly<T>`, `Pick<T, K>`)
- Explain how to type functions and their parameters.
- What is the `unknown` type? How is it different from `any`?

### TypeScript - Senior/Architect Level

- What are conditional types? Provide a use case.
- What are decorators in TypeScript? (Experimental feature)
- Explain how to create custom utility types.
- How do you manage complex types across a large codebase? (e.g., declaration merging, namespaces vs modules)
- How would you integrate TypeScript into an existing JavaScript project? What are the strategies and challenges?
- Discuss advanced type manipulation techniques (e.g., `infer` keyword, variadic tuple types).
- How does TypeScript improve refactoring and maintainability?
- What are declaration files (`.d.ts`)? How do you create them for third-party JavaScript libraries?
- How can TypeScript be used to enforce design patterns or architectural constraints?
- Discuss build performance considerations with TypeScript.
- How do you handle nominal typing vs structural typing in TypeScript?
- What are some limitations of TypeScript's type system?

## Ⅵ. Data Structures & Algorithms (DSA) 📊

_While frontend roles may not focus as heavily on complex algorithms as backend roles, a good understanding of basic DSA is often expected, especially for optimizing UI rendering and logic._

### DSA - General Concepts

- What is Big O notation? Why is it important?
- Explain common data structures:
  - Arrays (and their dynamic nature in JS)
  - Objects (hash maps in JS)
  - Linked Lists (conceptual understanding)
  - Stacks & Queues (conceptual understanding and use cases, e.g., event loop, undo/redo)
  - Trees (especially the DOM tree, component trees in React)
  - Graphs (less common, but good to know basics for certain problems)
- Explain common algorithms:
  - Sorting algorithms (e.g., bubble sort, merge sort, quick sort - conceptual)
  - Searching algorithms (e.g., linear search, binary search)
  - Recursion

### DSA - Frontend Specific Problems

- How would you efficiently render a large list of items? (Virtualization/Windowing)
- How to implement a debounce or throttle function?
- How to flatten a nested array?
- How to find an element in the DOM or a component tree efficiently?
- Problems related to string manipulation, array manipulation.
- Logic for UI components (e.g., a typeahead/autocomplete search, a carousel).
- Understanding how data structures are used in frameworks (e.g., React's reconciliation uses concepts related to tree traversal).
- (Architect Level) Discuss algorithmic complexity when designing reusable components or core framework logic.

## Ⅶ. React ⚛️

### React - Trainee/Junior Level

- What is React? What problems does it solve?
- What is JSX? Why is it used?
- What is a React component? (functional vs class components - basic differences)
- What are props? How are they passed? Are they mutable?
- What is state in a React component? How is it different from props?
- How do you update state in a functional component (`useState`)?
- How do you handle events in React?
- What is conditional rendering? (e.g., using `if`, ternary operator, `&&`)
- How do you render lists of items in React? What is the importance of `key` props?
- What is the Virtual DOM? How does it work?
- What is `create-react-app`?
- What are React Fragments? Why use them?
- Explain the basic lifecycle of a class component (e.g., `constructor`, `render`, `componentDidMount`, `componentWillUnmount`). (Though focus is shifting to hooks, basics might be asked)
- How do you import/export components?

### React - Mid Level

- Explain React Hooks in detail (`useState`, `useEffect`, `useContext`).
- What are the rules of Hooks?
- Explain the `useEffect` hook. How do you manage side effects? What is the dependency array?
- How do you fetch data in React components?
- What is Context API? When would you use it? How to use `useContext`?
- What is prop drilling? How can it be avoided?
- What are controlled vs uncontrolled components?
- What are Higher-Order Components (HOCs)?
- What are Render Props?
- How do you optimize React performance? (e.g., `React.memo`, `useCallback`, `useMemo`)
- Explain error boundaries.
- What are refs? When and how to use them (`useRef`)?
- How does React handle forms?
- What are synthetic events in React?
- How do you style React components? (CSS, CSS Modules, Styled Components, etc.)

### React - Senior Level

- Deep dive into reconciliation algorithm. How does React decide when to re-render?
- Explain advanced patterns with Hooks (custom Hooks, complex state logic with `useReducer`).
- How do `useMemo` and `useCallback` work internally and when are they truly beneficial?
- Discuss different state management strategies in React (Context API vs Redux/Zustand/Jotai, etc.). Pros and cons.
- How would you implement server-side rendering (SSR) or static site generation (SSG) with React?
- What are concurrent features in React (e.g., `startTransition`, `useDeferredValue`)? How do they improve user experience?
- How do you handle internationalization (i18n) in a React application?
- Discuss advanced component composition patterns.
- How do you manage large forms with complex validation in React?
- Explain how React's event system works internally.
- What are React Suspense and React Lazy for code splitting?
- What is Micro Frontends with React?
- How would you structure a large React application for scalability and maintainability?
- Accessibility (a11y) in React applications.

### React - Architect Level

- Design a scalable and performant architecture for a complex React application.
- Discuss the trade-offs of choosing different state management libraries for large-scale projects.
- How would you establish and enforce coding standards, best practices, and component libraries for a team of React developers?
- Evaluate the pros and cons of monorepo vs. polyrepo for React projects.
- Discuss strategies for migrating a legacy application to React.
- How do you approach performance monitoring and optimization in a large React application?
- What are the challenges and solutions for building a design system with React?
- Architecting for testability in React applications.
- How do you handle security concerns specific to React applications (e.g., XSS in JSX, securing API keys)?
- Discuss the future direction of React and its ecosystem.
- How do you lead a team of React developers, mentor juniors, and make high-level technical decisions?
- When would you choose _not_ to use React for a project?

## Ⅷ. Next.js NEXT

### Next.js - Trainee/Junior Level

- What is Next.js? Why use it over Create React App?
- What are the main features of Next.js? (SSR, SSG, Routing, API Routes)
- How does file-system routing work in Next.js?
- What is the difference between a page and a component in Next.js?
- How do you create dynamic routes in Next.js?
- What is `Link` component in Next.js used for?
- How do you fetch data for pages in Next.js? (e.g., `getStaticProps`, `getServerSideProps` - basics)
- What are API routes in Next.js?

### Next.js - Mid Level

- Explain `getStaticProps`, `getStaticPaths`, and `getServerSideProps` in detail. When to use each?
- What is Incremental Static Regeneration (ISR)?
- How does Next.js handle image optimization (`next/image`)?
- How do you set up environment variables in Next.js?
- What is the `_app.js` (or `_app.tsx`) file used for?
- What is the `_document.js` (or `_document.tsx`) file used for?
- How do you implement client-side data fetching in Next.js (e.g., with SWR or React Query)?
- How does Next.js handle internationalization (i18n)?
- What are middleware in Next.js? (Newer versions)
- How does routing work with the App Router vs Pages Router?

### Next.js - Senior/Architect Level

- Discuss advanced data fetching patterns in Next.js.
- How would you architect a large-scale application using Next.js?
- Explain the Next.js build process and deployment strategies (Vercel, AWS, etc.).
- How do you optimize a Next.js application for performance (Core Web Vitals)?
- Discuss authentication and authorization strategies in Next.js applications.
- How do you manage state in a complex Next.js application that uses different rendering strategies?
- When would you choose server components vs client components in the App Router?
- How do you integrate Next.js with a headless CMS?
- Discuss strategies for caching in Next.js (data, pages, assets).
- How do you handle A/B testing in a Next.js application?
- Compare Next.js with other React frameworks (e.g., Remix).
- How would you design a resilient and scalable backend using Next.js API routes or by integrating with external backend services?

## Ⅸ. React Ecosystem & Libraries 📚

### State Management (Redux, Zustand, Jotai, Recoil, etc.)

- **General:**
  - Why do we need state management libraries?
  - What are the differences between local component state, Context API, and global state management libraries?
- **Redux (if experienced with):**
  - What are the core principles of Redux? (Single source of truth, State is read-only, Changes are made with pure functions)
  - Explain Actions, Reducers, Store, Dispatch.
  - What is middleware in Redux (e.g., `redux-thunk`, `redux-saga`)? Why is it used?
  - How does `connect` HOC or `useSelector`/`useDispatch` hooks work?
  - What is immutability and why is it important in Redux?
  - How do you structure your Redux store for a large application? (Ducks pattern, Redux Toolkit)
  - What are selectors? Why use them (e.g., `reselect`)?
- **Zustand/Jotai/Recoil (if experienced with):**
  - How do these libraries differ from Redux? What are their core concepts?
  - What are the benefits of using Zustand/Jotai/Recoil? (e.g., simplicity, boilerplate reduction, atomic state)
  - How do they handle asynchronous operations?
  - How do they compare in terms of bundle size and performance?

### Routing (React Router)

- How does React Router work?
- What are the main components of React Router? (`<BrowserRouter>`, `<Routes>`, `<Route>`, `<Link>`, `<Navigate>`)
- How do you create nested routes?
- How do you implement programmatic navigation? (`useNavigate`)
- How do you handle route parameters? (`useParams`)
- How do you implement protected routes?
- What is the difference between `BrowserRouter` and `HashRouter`?

### Data Fetching & Caching (Axios, Fetch API, SWR, React Query/TanStack Query)

- How do you make API calls in React applications? (Fetch vs Axios)
- What are the benefits of using libraries like SWR or React Query?
  - Caching, background updates, pagination, optimistic updates, error handling, etc.
- How do these libraries manage server state vs client state?
- Explain key concepts like `stale-while-revalidate`.
- How do you handle mutations (POST, PUT, DELETE) with these libraries?

### UI Libraries (Material UI, Ant Design, Chakra UI, Tailwind CSS with Headless UI)

- What are the pros and cons of using component libraries?
- How do you customize components from these libraries?
- How do they handle theming?
- When would you build custom components vs using a library?
- How does Tailwind CSS differ from component libraries? (Utility-first approach)

### Form Handling (Formik, React Hook Form)

- What are the challenges of handling forms in React?
- How do libraries like Formik or React Hook Form simplify form handling?
  - Validation, submission, state management, error handling.
- Compare controlled vs uncontrolled approaches with these libraries.

## Ⅹ. Design Patterns & Refactoring 🏗️

### Design Patterns

- **General:**
  - What are design patterns? Why are they useful?
  - Can you name a few common JavaScript design patterns? (Module, Singleton, Observer, Factory, Facade, Proxy)
  - How do design patterns apply to frontend development?
- **React Specific:**
  - What are common React design patterns? (HOC, Render Props, Compound Components, Provider Pattern, Custom Hooks as patterns)
  - How do Hooks change the way we use some traditional React patterns?
  - Discuss the pros and cons of different patterns for solving specific problems (e.g., sharing logic, state management).
- **Architect Level:**
  - How do architectural patterns (e.g., MVC, MVVM, Flux, Micro Frontends) influence frontend development?
  - How do you choose appropriate design patterns for a given problem considering scalability and maintainability?

### Refactoring

- What is code refactoring? Why is it important?
- When should you refactor code? What are common code smells?
- Describe some refactoring techniques you have used.
- How do you refactor a large legacy codebase safely?
- How does testing support refactoring?
- How do you balance refactoring with feature development?
- (Architect Level) How do you lead a team effort in large-scale refactoring? What metrics can be used to track progress/success?

## XI. Testing 🧪

### Testing - Trainee/Junior Level

- Why is testing important?
- What are different types of tests? (Unit, Integration, End-to-End)
- What is Jest? What is it used for?
- What is React Testing Library (RTL)? What is its philosophy? (Testing user behavior)
- How do you write a simple unit test for a React component?
- What are matchers in Jest? (e.g., `toBe`, `toEqual`, `toHaveBeenCalled`)
- How do you select elements in RTL? (e.g., `getByText`, `getByRole`)

### Testing - Mid Level

- How do you test components with props and state?
- How do you mock functions and modules in Jest?
- How do you test asynchronous operations?
- How do you test custom Hooks?
- What is code coverage? How do you interpret it?
- How do you simulate user events (e.g., clicks, input changes) with RTL?
- What is the difference between `getBy*`, `queryBy*`, and `findBy*` queries in RTL?
- How do you test components that use Context API or Redux?
- What are snapshot tests? What are their pros and cons?

### Testing - Senior/Architect Level

- How do you set up a testing strategy for a large application?
- What are the differences between Jest, Mocha, Jasmine?
- What is Cypress or Playwright? When would you use them for E2E testing?
- How do you test for accessibility (a11y)?
- How do you approach visual regression testing?
- How do you integrate testing into a CI/CD pipeline?
- Discuss challenges in testing micro-frontends.
- How do you measure the effectiveness of your tests?
- What are some best practices for writing maintainable and effective tests?
- How do you decide what to test and what not to test? (Test pyramid)
- Discuss contract testing for microservices.

## XII. Tooling 🛠️

- **Package Managers:**
  - What is `npm`? What is `yarn`? What are the differences?
  - What is a `package.json` file? What is `package-lock.json` or `yarn.lock`?
  - What are semantic versioning (SemVer) and its implications?
- **Module Bundlers (Webpack, Parcel, Rollup, Vite):**
  - What is a module bundler? Why is it needed?
  - Explain the basic concepts of Webpack (entry, output, loaders, plugins, mode).
  - What is tree shaking?
  - What is code splitting? How does it improve performance?
  - How does Vite differ from Webpack (e.g., native ES modules during development)?
- **Transpilers (Babel):**
  - What is Babel? Why is it used?
  - How does Babel work (presets, plugins)?
- **Linters & Formatters (ESLint, Prettier):**
  - What is linting? What is formatting? Why are they important?
  - How do you configure ESLint and Prettier?
- **Version Control (Git):**
  - Basic Git commands (`commit`, `push`, `pull`, `branch`, `merge`, `rebase`).
  - What is a merge conflict? How do you resolve it?
  - Explain common Git workflows (e.g., Gitflow, GitHub Flow).
- **Developer Tools:**
  - How do you use browser developer tools for debugging and profiling? (Elements, Console, Sources, Network, Performance tabs)
  - What are React DevTools?
- **CI/CD (Continuous Integration/Continuous Deployment):**
  - What is CI/CD? What are its benefits?
  - What tools have you used for CI/CD (e.g., Jenkins, GitLab CI, GitHub Actions)? (More relevant for senior/architect)

## XIII. Live Coding Questions 💻

_Live coding sessions often involve solving practical frontend problems or implementing UI components. Be prepared to explain your thought process._

### Example Problem Areas

- **UI Component Implementation:**
  - Build a simple counter.
  - Build a toggle switch.
  - Build a modal/dialog.
  - Build a simple To-Do list application (CRUD operations).
  - Build a star rating component.
  - Build a basic tabs component.
  - Implement a simple accordion.
  - Create a progress bar.
- **JavaScript/Algorithm Challenges (Frontend Flavored):**
  - Implement `debounce` or `throttle`.
  - Write a function to fetch data from an API and display it.
  - Handle nested comments rendering.
  - Write a function to deeply compare two objects/arrays.
  - Implement a simple search/filter functionality on a list of data.
  - Solve problems involving DOM manipulation (though often abstracted by React, understanding helps).
  - Flatten an array of objects.
  - Simple form validation logic.
- **CSS Challenges:**
  - Recreate a simple layout (e.g., a card, a header).
  - Center an element in various ways.
  - Implement a responsive grid.
- **React Specific:**
  - Refactor a class component to a functional component with Hooks.
  - Create a custom Hook.
  - Manage state for a small application.
  - Pass data between components.

**Tips for Live Coding:**

- **Think Aloud:** Explain your approach and thought process.
- **Ask Clarifying Questions:** Make sure you understand the requirements.
- **Start Simple:** Get a basic version working, then iterate and add complexity.
- **Write Clean Code:** Pay attention to naming, structure, and readability.
- **Test Your Code:** Even simple manual tests or `console.log` can help.
- **Handle Edge Cases (if time allows or prompted):** Think about what could go wrong.
- **Communicate:** If you get stuck, explain what you're trying to do.

## XIV. Behavioral & Situational Questions 🤔

_These questions assess your soft skills, problem-solving approach, teamwork, and experience._

- Tell me about a challenging project you worked on. What were the challenges, and how did you overcome them?
- Describe a time you had a conflict with a team member. How did you resolve it?
- How do you stay updated with new technologies and trends in frontend development?
- Tell me about a time you made a mistake or failed. What did you learn from it?
- How do you handle tight deadlines or pressure?
- How do you approach debugging a complex issue?
- What are your strengths and weaknesses as a developer?
- Why are you interested in this role/company?
- Where do you see yourself in 5 years?
- How do you contribute to code reviews? What do you look for?
- Describe your experience working in an Agile/Scrum environment.
- How do you prioritize tasks when you have multiple commitments?
- (Senior/Architect) Tell me about a time you had to make a difficult technical decision. What was your process?
- (Senior/Architect) How do you mentor junior developers?
- (Senior/Architect) How do you handle disagreements about technical approaches within a team?
- (Senior/Architect) Describe a time you introduced a new technology or process to your team. What was the outcome?

## XV. Architect Level Specific Questions 🏛️

_Beyond the senior-level questions in each category, architect roles focus more on high-level design, strategy, leadership, and impact._

- How do you design a frontend system for scalability, reliability, and maintainability?
- Discuss your experience with micro-frontend architectures: pros, cons, and implementation strategies.
- How do you evaluate and choose new technologies, frameworks, or libraries for a project or an organization?
- Describe your approach to establishing technical vision and roadmap for a frontend team or product.
- How do you ensure consistency and quality across multiple frontend teams or projects? (Design systems, shared libraries, governance)
- Discuss strategies for managing technical debt in a large and evolving codebase.
- How do you foster a culture of innovation and continuous improvement within a development team?
- How do you balance business requirements, user experience, and technical constraints when making architectural decisions?
- What is your experience with leading and mentoring other senior engineers or tech leads?
- How do you measure the success or impact of frontend architectural changes?
- Discuss the role of a frontend architect in cross-functional teams and collaboration with backend, DevOps, and product teams.
- How do you approach building and evolving a Design System at scale?
- What are the key considerations for internationalizing and localizing a complex global application?
- How do you ensure long-term platform stability while also allowing for innovation and adoption of new technologies?
- Discuss your approach to API design from a frontend perspective – what makes a good API for frontend consumption?

**Good luck with your interview preparation!** 🚀
