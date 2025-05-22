# Essential Frontend Interview FAQs

This document contains a curated list of frequently asked interview questions covering HTML, CSS, JavaScript, TypeScript, React, Next.js, and other general frontend topics. It aims to highlight the most important concepts you're likely to encounter.

---

## 🏛️ HTML FAQs

1.  **What is HTML and its primary purpose?** Explain its relationship with CSS and JavaScript.
2.  **What is an HTML element?** Describe its common structure.
3.  **What are HTML attributes?** Provide common examples (e.g., `id`, `class`, `src`, `href`).
4.  **Describe the basic structure of an HTML document.** (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`).
5.  **What does `<!DOCTYPE html>` do and why is it important?**
6.  **Difference between `<head>` and `<body>`?**
7.  **Difference between block-level and inline elements?** Provide examples.
8.  **Difference between `<div>` and `<span>`?**
9.  **What is semantic HTML?** Why is it important (accessibility, SEO)? List some HTML5 semantic elements (e.g., `<article>`, `<section>`, `<nav>`, `<header>`, `<footer>`, `<main>`).
10. **Purpose of heading tags (`<h1>` to `<h6>`)?** How should they be used?
11. **How do you create hyperlinks?** Key attribute: `href`.
12. **How do you embed an image?** Essential attributes for `<img>` (especially `src` and `alt`). Why is `alt` text crucial?
13. **What are the different types of lists in HTML?** (`<ul>`, `<ol>`, `<dl>`).
14. **How do you create a basic table?** Essential tags: `<table>`, `<tr>`, `<td>`, `<th>`.
15. **Purpose of the `<form>` tag?** Key attributes: `action`, `method` (GET vs. POST).
16. **List common `<input>` types.** (e.g., `text`, `password`, `checkbox`, `radio`, `submit`, `file`).
17. **What is the `<label>` element used for?** Why is it important for accessibility?

---

## 🎨 CSS FAQs

1.  **What is CSS and its primary role?**
2.  **How do you apply CSS to HTML?** (External, internal, inline). Pros and cons?
3.  **Explain basic CSS syntax.** (Selector, declaration block, property, value).
4.  **Difference between `class` and `ID` selectors?**
5.  **What are CSS combinators?** (Descendant, child, adjacent sibling, general sibling).
6.  **What is the CSS Box Model?** (Content, padding, border, margin).
7.  **What is `box-sizing: border-box`?** Why is it useful?
8.  **Difference between `margin` and `padding`?**
9.  **What is CSS Specificity?** How is it calculated?
10. **Explain the "Cascade" in CSS.**
11. **What is CSS Inheritance?**
12. **What are pseudo-classes and pseudo-elements?** Provide examples.
13. **What is the `display` property?** Common values: `block`, `inline`, `inline-block`, `none`, `flex`, `grid`.
14. **Difference between `display: none;` and `visibility: hidden;`?**
15. **Explain the `position` property.** (`static`, `relative`, `absolute`, `fixed`, `sticky`).
16. **What is `z-index`?** What is a stacking context?
17. **What is Responsive Web Design (RWD)?**
18. **What are Media Queries?** How are they used?
19. **What is Flexbox?** Key concepts: main axis, cross axis, `flex-direction`, `justify-content`, `align-items`.
20. **What is CSS Grid Layout?** How does it differ from Flexbox? Key concepts: `grid-template-columns/rows`, `fr` unit, `gap`.
21. **Difference between `rem`, `em`, `px`, and viewport units (`vh`, `vw`)?**
22. **How do CSS Custom Properties (Variables) work?**
23. **What is the difference between CSS Transitions and Animations?**

---

## 🧠 JavaScript FAQs

### Foundational Concepts

1.  **What is JavaScript?** Single-threaded? Interpreted?
2.  **How do you include JavaScript in HTML?** Placement of `<script>` tags, `async`, `defer`.
3.  **JavaScript Data Types?** (Primitives and Objects).
4.  **Difference between `null` and `undefined`?**
5.  **Difference between `let`, `const`, and `var`?** (Scope, hoisting, reassignment).
6.  **What is hoisting in JavaScript?**
7.  **Difference between `==` and `===`?** Explain type coercion.
8.  **What are truthy and falsy values?** List falsy values.
9.  **What is "Strict Mode" (`'use strict';`)?**

### Scope & Closures

10. **Explain scope in JavaScript.** (Global, function, block).
11. **What are closures?** Provide an example and explain their use cases.
12. **What is an IIFE (Immediately Invoked Function Expression)?**

### Functions

13. **Different ways to define a function?** (Declaration, Expression, Arrow).
14. **What are arrow functions?** Key differences from traditional functions (especially `this` binding, `arguments`).
15. **What is the `this` keyword?** How is its value determined in different contexts?
16. **Explain `call()`, `apply()`, and `bind()` methods.**
17. **What are higher-order functions?**
18. **What is a callback function?**

### Objects & Prototypes

19. **How do you create objects?** (Literals, constructor functions, ES6 classes).
20. **Explain prototypal inheritance.** What is the prototype chain?
21. **What is the ES6 `class` syntax?** Is it just syntactic sugar?
22. **Difference between deep copy and shallow copy of an object?**

### Arrays

23. **Common array methods?** (`forEach`, `map`, `filter`, `reduce`, `push`, `pop`, `slice`, `splice`).
24. **Difference between `map()` and `forEach()`?**
25. **How does `Array.prototype.reduce()` work?**

### Asynchronous JavaScript

26. **Synchronous vs. asynchronous programming?**
27. **Explain the JavaScript Event Loop.** (Call Stack, Web APIs, Callback Queue, Microtask Queue).
28. **Difference between Microtask and Macrotask Queue?**
29. **What are Promises?** States (`pending`, `fulfilled`, `rejected`), `.then()`, `.catch()`, `.finally()`.
30. **What is `async/await`?** How does it relate to Promises? How do you handle errors?
31. **What is the Fetch API?** How do you make GET/POST requests?

### DOM Manipulation & Browser APIs

32. **What is the DOM?**
33. **How do you select HTML elements?** (`getElementById`, `querySelector`, etc.).
34. **Difference between `innerHTML`, `innerText`, and `textContent`?**
35. **Explain event handling.** (Event listeners, event object, bubbling/capturing, `stopPropagation()`, `preventDefault()`).
36. **What is event delegation?**
37. **What are `localStorage` and `sessionStorage`?** Differences and use cases.

### ES6+ Features

38. **What are template literals?**
39. **What is destructuring assignment?** (Arrays and Objects).
40. **What are spread syntax (`...`) and rest parameters (`...`)?**
41. **What are ES6 Modules (`import`/`export`)?**

---

## 🔷 TypeScript FAQs

1.  **What is TypeScript?** How does it differ from JavaScript? Main benefits?
2.  **Basic data types in TypeScript?** (`string`, `number`, `boolean`, `any`, `unknown`, `void`, `never`, arrays, tuples).
3.  **What is type annotation and type inference?**
4.  **Difference between `any` and `unknown`?** Why prefer `unknown`?
5.  **What are interfaces and type aliases?** What are the differences and when to use each?
6.  **What are enums?** (Numeric, string).
7.  **What are union types (`|`) and intersection types (`&`)?**
8.  **What are "type guards"?** (e.g., `typeof`, `instanceof`, custom with `is`).
9.  **What are generics?** Why are they useful? Provide an example of a generic function or interface.
10. **Common utility types?** (`Partial<T>`, `Required<T>`, `Readonly<T>`, `Pick<T, K>`, `Omit<T, K>`).
11. **How are classes defined?** Access modifiers (`public`, `private`, `protected`).
12. **What are declaration files (`.d.ts`)?** Purpose of DefinitelyTyped (`@types/package`)?
13. **What is `tsconfig.json`?** Key compiler options (`target`, `module`, `strict`, `outDir`).

---

## ⚛️ React FAQs

### Core Concepts

1.  **What is React?** Main features (Virtual DOM, JSX, Component-Based).
2.  **What is JSX?** How does it get transpiled?
3.  **Functional Components vs. Class Components?** Which is preferred now and why?
4.  **What is the Virtual DOM?** How does reconciliation work (briefly)?
5.  **Difference between `state` and `props`?**
6.  **What is "unidirectional data flow"?**
7.  **How do you handle events in React?** (SyntheticEvent).
8.  **What is conditional rendering?** Common ways to achieve it.
9.  **How do you render lists?** Importance of the `key` prop.
10. **What are React Fragments?**
11. **What are controlled vs. uncontrolled components in forms?**
12. **What does "lifting state up" mean?**

### Hooks

13. **What are Hooks?** Rules of Hooks?
14. **`useState()`:** How to use it for managing state. Asynchronous nature of `setState`.
15. **`useEffect()`:** Common use cases (side effects). Dependency array (`[]`, `[dep]`, no array). Cleanup function.
16. **`useContext()`:** How it helps avoid prop drilling.
17. **`useReducer()`:** When to prefer over `useState` for complex state logic.
18. **`useMemo()` and `useCallback()`:** What problems do they solve? (Performance optimization, referential equality).
19. **`useRef()`:** Common use cases (DOM access, storing mutable values without re-render).
20. **What are Custom Hooks?** Why are they useful?

### Advanced & State Management

21. **What are Higher-Order Components (HOCs)?** What are Render Props? (Conceptual understanding and alternatives like Hooks).
22. **What are Error Boundaries?**
23. **What is Context API in detail?** (Provider, Consumer/`useContext`). Potential performance issues.
24. **What is `React.memo()`?**
25. **(If Redux is mentioned or relevant to role) What is Redux?** Core principles (Store, Actions, Reducers). Data flow. What are common alternatives (Zustand, Jotai)?
26. **(As of May 2025) What are React Server Components (RSCs)?** High-level differences from Client Components and SSR. `"use client"` directive.

---

## 🚀 Next.js FAQs (Focus on App Router as of May 2025)

1.  **What is Next.js?** Why use it over vanilla React (CSR)? Key advantages?
2.  **Main rendering strategies in Next.js?** (CSR, SSR, SSG, ISR). Briefly explain each.
3.  **What is pre-rendering? What is hydration?**
4.  **Explain the `app` directory (App Router).** File-system routing (`page.js`, `layout.js`).
5.  **What are Layouts and Pages in the App Router?**
6.  **What are Server Components vs. Client Components in the App Router?** `"use client"` directive. Capabilities/limitations of each.
7.  **How is data fetching done in Server Components (App Router)?** (`async/await` directly, caching with `Workspace`).
8.  **How do you handle data fetching in Client Components?** (e.g., `useEffect` + `Workspace`, SWR/React Query).
9.  **What are Server Actions?** How do they work for mutations from Client Components?
10. **How does navigation work?** (`<Link>` component, `useRouter` from `next/navigation`).
11. **What is the `next/image` component?** Benefits?
12. **What are API Routes (Pages Router) / Route Handlers (App Router)?**
13. **What is Middleware in Next.js?** Use cases?
14. **How are environment variables handled?** (`NEXT_PUBLIC_`).
15. **Difference between `getStaticProps`, `getServerSideProps` (Pages Router) and data fetching in App Router Server Components?** (Conceptual difference in approach).

---

## 🌐 General Frontend & Web Concepts FAQs

### Performance

1.  **Why is web performance important?**
2.  **Key performance metrics?** (Core Web Vitals: LCP, FID/INP, CLS).
3.  **Techniques for reducing page load time?** (Minification, compression, caching, CDN, code splitting, image optimization).
4.  **What is lazy loading?** For images and components.
5.  **Difference between `async` and `defer` for script loading?**

### Security

6.  **What is XSS (Cross-Site Scripting)?** How to prevent it?
7.  **What is CSRF (Cross-Site Request Forgery)?** How to mitigate?
8.  **What is HTTPS?** Why is it crucial?
9.  **What is Content Security Policy (CSP)?**
10. **Best practices for token storage?** (`localStorage` vs. cookies with `HttpOnly`, `Secure`).

### Accessibility (A11y)

11. **What is Web Accessibility (A11y)?** Why important?
12. **What are WCAG principles (POUR)?**
13. **How does semantic HTML contribute to A11y?**
14. **What is ARIA?** When to use it? First rule of ARIA?
15. **Importance of `alt` text for images?**

### Networking & APIs

16. **Common HTTP methods?** (GET, POST, PUT, DELETE).
17. **Common HTTP status codes?** (2xx, 3xx, 4xx, 5xx categories and examples).
18. **What is REST?** Principles of RESTful APIs.
19. **What is CORS?** Why is it needed?

### Version Control (Git)

20. **What is Git?** Basic commands (`clone`, `add`, `commit`, `push`, `pull`, `branch`, `merge`, `rebase`).
21. **What are branches?** Why use them?
22. **Difference between `git merge` and `git rebase`?**

### Browser & Web APIs

23. **`localStorage` vs. `sessionStorage`?**
24. **What is the Fetch API?**
25. **What are Web Workers?** (Briefly, for background processing).
26. **What are Service Workers?** (Briefly, for offline support/PWAs).

### Software Engineering & Testing

27. **DRY, KISS, YAGNI principles?**
28. **Imperative vs. Declarative programming?** (React context).
29. **Different levels of testing?** (Unit, Integration, E2E). What is the Testing Pyramid?
30. **What are mocks/stubs in testing?**

---

## 💻 Common Live Coding Problem Areas (React & TypeScript)

Focus on your thought process, communication, and breaking down the problem.

1.  **UI Component Building:**
    - **Typed Counter:** Props for initial count/step, state for current count, increment/decrement functions.
    - **Typed Toggle/Switch:** Props for state and callback, internal state management.
    - **Character Counter Input:** Props for max length, state for input value, display count.
    - **Simple Tabs Component:** Props for tab data (id, title, content), state for active tab.
2.  **State Management & Hooks:**
    - **Typed Form with `useState` and Basic Validation:** Manage form state object, handle input changes, basic validation logic.
    - **Data Fetching with `useEffect`/`useState`:** Fetch from a public API, define types for response, handle loading/error states.
    - **Custom Hook (e.g., `useToggle`, `useDebounce`, `useLocalStorage`):** Implement a reusable hook with proper typing (generics if applicable).
3.  **List Rendering & Manipulation:**
    - **Filterable List:** Given an array of typed objects, render a list and an input field to filter the list client-side.
4.  **API Interaction:**
    - **Paginated Data Table:** Fetch and display paginated data, handle page navigation. Define types for API response and items.

**Remember for Live Coding:**

- Clearly state your understanding of the problem and ask clarifying questions.
- Define types/interfaces for props, state, and important data structures early.
- Explain your approach before and while coding.
- Handle basic edge cases and error states.
- Think about accessibility and performance if prompted or relevant.
- Test your component conceptually or with simple manual interactions.

This list should provide a solid foundation for your interview preparation!
