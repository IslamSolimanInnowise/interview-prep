# Frontend Developer Interview FAQs: Trainee to Middle+ Levels (React Focused)

This document provides a focused list of frequently asked questions for frontend developer interviews, specifically tailored for trainee, intern, junior (-, regular, +), and middle (-, regular, +) roles, with an emphasis on React and its ecosystem.

## Ⅰ. The Web & Internet 🌐🔗

This section covers foundational to intermediate knowledge about how the internet and web technologies work, including performance, security, and accessibility.

### Web & Internet Fundamentals

- How does the internet work? (High-level overview)
- What is HTTP/HTTPS? Explain common HTTP methods (GET, POST, PUT, DELETE, PATCH, OPTIONS, HEAD).
- What are HTTP status codes? (e.g., 200, 201, 400, 401, 403, 404, 500). Categorize them (1xx, 2xx, 3xx, 4xx, 5xx).
- What is DNS? How does DNS resolution work?
- What is a domain name? What is hosting?
- What is a browser? How does it render a webpage? (Critical Rendering Path - conceptual understanding).
- What are cookies? How are they used? What are their security implications (basic awareness)?
- What is `localStorage` vs `sessionStorage` vs `cookies`? Discuss capacity, use cases, and security (differences in persistence, basic security awareness).
- What is CORS (Cross-Origin Resource Sharing)? How do you handle it (conceptual understanding, awareness of preflight requests)? Why is it needed?
- What is RESTful API design? What are the principles of a RESTful API (conceptual)?
- What is GraphQL? How is it different from REST? What are its advantages and disadvantages (conceptual, awareness for Mid+)?
- What are WebSockets? How do they differ from HTTP? When are they used (real-time communication)?
- What is Server-Sent Events (SSE)? How does it compare to WebSockets?
- What is AJAX?
- Explain the Fetch API. How do you make GET/POST requests? How do you handle responses (e.g., `.json()`) and errors (e.g., `.catch()`, checking `response.ok`)?
- What are HTTP headers? Give examples of request headers (e.g., `Authorization`, `Content-Type`) and response headers (e.g., `Content-Type`, `Cache-Control`).
- What is the difference between HTTP/1.1 and HTTP/2 (basic idea: multiplexing, header compression)? HTTP/3 (awareness it exists, uses QUIC).
- What is caching in the context of HTTP? (Browser cache, proxy cache, CDN cache - conceptual).
- What is API versioning? Why is it important and what are common strategies (URL path, query param, header - awareness for Mid+)?
- How do you debug network requests in the browser? (Network tab in DevTools).

### Web Performance

- Why is web performance important? (Discuss user experience, conversion rates, SEO, accessibility).
- What are the key metrics to measure web performance? (e.g., Core Web Vitals: LCP, INP (formerly FID), CLS; also FCP, TTFB, TTI). Explain what each measures (conceptual).
- How do you measure web performance? (Lighthouse, WebPageTest, DevTools Network/Performance tabs).
- What is the Critical Rendering Path? How can you optimize it (minimize render-blocking resources)? How does CSS block rendering?
- What are common techniques to optimize website loading speed?
  - Minification, compression (Gzip, Brotli), image optimization (formats like WebP, AVIF, JPEG, PNG, SVG; compression; responsive images with `<picture>` or `srcset`), caching (browser, CDN), code splitting, lazy loading, reducing HTTP requests (less critical with HTTP/2+).
- What is a CDN (Content Delivery Network)? How does it improve performance and availability?
- How does browser rendering impact performance? (Reflow/Layout, Repaint/Composite - understanding these cause work for the browser).
- What is "code splitting"? How does it improve initial load time?
- What is "lazy loading"? For which types of assets is it most beneficial (images, components, routes)? How is it implemented (e.g., HTML `loading` attribute for images, `React.lazy` for components)?
- How do you optimize images for the web? (Formats: WebP, AVIF, JPEG, PNG, SVG; compression; responsive images with `<picture>` or `srcset` attribute).
- What are browser caching mechanisms? (HTTP caching headers: `Cache-Control`, `Expires`, `ETag`, `Last-Modified`). How do they work (conceptual understanding)?
- Explain the difference between `async` and `defer` attributes for script loading. When would you use each?
- What is "tree shaking"? How does it help reduce bundle size? How do bundlers like Webpack or Rollup use it?
- How can you identify performance bottlenecks in a web application? (Using browser DevTools: Network tab, Performance tab, Lighthouse).
- What is "perceived performance" vs. "actual performance"? How can you improve perceived performance? (Skeletons screens, optimistic UI updates - conceptual for Mid+).
- How do fonts impact web performance? How can you optimize font loading? (`font-display` property, WOFF2 format, preloading critical fonts).
- What is "render-blocking CSS/JS"? How do you mitigate it (e.g., moving scripts to end of body, using `async`/`defer`, inlining critical CSS)?
- Discuss strategies for optimizing CSS delivery (e.g., inlining critical CSS, loading non-critical CSS asynchronously).
- What are resource hints (`preload`, `prefetch`, `preconnect`, `dns-prefetch`)? How can they be used in HTML to optimize loading of critical resources (conceptual for Mid+)?
- How does server-side rendering (SSR) or static site generation (SSG) impact different performance metrics compared to client-side rendering (CSR) (conceptual)?
- What is the impact of third-party scripts on performance? How can you manage them effectively (e.g., async loading, auditing their impact)?
- How would you approach optimizing a slow-loading webpage? Describe your step-by-step process (identify issues with DevTools, prioritize fixes).
- What is "Critical CSS"? How can you inline critical CSS for faster perceived load times?
- How can you reduce CSS file size? (Minification, removing unused CSS, using shorthand properties).
- How does the browser parse CSS? From right to left or left to right? Why is this important for selector performance (conceptual for Mid+)?

### Web Security

- What are common web security vulnerabilities a frontend developer should be aware of (focus on XSS, CSRF)?
- What is Cross-Site Scripting (XSS)?
  - Explain stored, reflected, and DOM-based XSS (conceptual understanding).
  - How can you prevent XSS vulnerabilities in frontend code (e.g., React's default JSX escaping, properly encoding data, sanitizing user input if `dangerouslySetInnerHTML` is used, awareness of Content Security Policy)? How do you prevent XSS in HTML forms (server-side validation is key, client-side can help UX)?
- What is Cross-Site Request Forgery (CSRF)? How can it be mitigated (e.g., CSRF tokens, SameSite cookies - conceptual)? How does the frontend play a role (submitting tokens)?
- What is Content Security Policy (CSP)? How does it work and what types of attacks can it help prevent (conceptual)?
- What are common security best practices for handling user authentication on the client-side? (Token storage: `localStorage` vs. cookies with `HttpOnly` and `Secure` flags - pros & cons; handling JWTs - conceptual).
- What is `HTTPS`? Why is it crucial? What is HSTS (HTTP Strict Transport Security) (awareness for Mid+)?
- What are `HttpOnly` and `Secure` flags for cookies? What do they do?
- What is the `SameSite` cookie attribute? How does it help prevent CSRF?
- What are Subresource Integrity (SRI) hashes? How do they enhance security when loading assets from CDNs (conceptual for Mid+)?
- What is "clickjacking"? How can it be prevented (e.g., `X-Frame-Options` header - awareness)?
- What security considerations are there when using `<iframe>` elements? (e.g., `sandbox` attribute).
- What is the risk of using `dangerouslySetInnerHTML` in React or similar methods in other frameworks?
- How can you ensure dependencies (npm packages) are secure and up-to-date? (e.g., `npm audit`, dependabot - awareness).
- What is "Man-in-the-Middle" (MitM) attack in the context of web applications (conceptual)?
- How can frontend code contribute to protecting against data breaches (e.g., not logging sensitive info to console, being careful with data display)?
- Why is it generally unsafe to use `eval()` or the `Function` constructor with arbitrary strings?

### Accessibility (a11y)

- What is web accessibility (a11y)? Why is it important (ethical, legal, business reasons)?
- What are the WCAG (Web Content Accessibility Guidelines)? Briefly explain their purpose and the four principles (POUR: Perceivable, Operable, Understandable, Robust). What are conformance levels (A, AA, AAA) (awareness)?
- How can semantic HTML contribute to accessibility?
- What is ARIA (Accessible Rich Internet Applications)? When should you use ARIA attributes (when native HTML isn't enough)? When should you prefer native HTML semantics? What is the first rule of ARIA (if you can use a native HTML element or attribute, do so)?
- Explain common ARIA roles (e.g., `role="button"`, `role="navigation"`) and properties (e.g., `aria-label`, `aria-hidden`, `aria-expanded`) with simple examples.
- How do you ensure keyboard accessibility? (Focus order, visible focus indicators, interactive elements being focusable and operable with keyboard). What is "keyboard accessibility"?
- What is the importance of providing text alternatives for non-text content (e.g., `alt` text for images, transcripts for audio, captions for video)? What makes a good `alt` text? When might you leave it empty (`alt=""`)?
- How do you ensure sufficient color contrast? What tools can help check this (browser dev tools, online checkers)?
- How can you design accessible forms? (Using `<label>` correctly, associating labels with inputs, `fieldset`/`legend` for grouping, providing clear error messages). How do you ensure forms are accessible?
- How do screen readers work with web content (conceptual)? What can developers do to ensure a good screen reader experience (semantic HTML, ARIA where needed, alt text)?
- What are common accessibility pitfalls to avoid in frontend development (e.g., vague link text, relying on color alone, poor focus management)?
- How can you test for web accessibility? (Automated tools like axe, Lighthouse; manual testing with keyboard; screen reader testing - awareness).
- What is the `prefers-reduced-motion` media query? How should it be handled (provide alternatives or reduce motion)?
- How does responsive design contribute to accessibility?
- Discuss how to make dynamic content updates (e.g., in SPAs) accessible (ARIA live regions - conceptual for Mid+).
- What is the purpose of `tabindex`? How can it be used to manage focus order (`0`, `-1`, positive values - use positive values with caution)? What are best practices for using `tabindex`?
- How do you make links accessible beyond just descriptive text? (Contextual link text, ARIA attributes if necessary).
- What is the difference between `<label>` and `aria-label` or `aria-labelledby`? When would you use ARIA labeling?
- How do you hide content accessibly? (e.g., visually hidden class for screen readers vs. `display:none` or `aria-hidden="true"` for complete hiding).
- Why is it important to provide clear visual focus indicators for interactive elements (`:focus`, `:focus-visible`)?

## Ⅱ. HTML (HyperText Markup Language) 🌐

This section focuses on HTML structure, semantics, and features relevant for these levels.

- **What is HTML?** What does HTML stand for?
- **What is the primary purpose of HTML in web development?** Explain its relationship with CSS and JavaScript.
- **What is an HTML element?** Describe its common structure (opening tag, content, closing tag).
- What is the difference between an element and a tag?
- **What are HTML tags?** Are all tags paired? Give an example of an empty/void tag (e.g., `<img>`, `<br>`, `<hr>`, `<input>`).
- **What are HTML attributes?** Provide examples and explain their purpose (e.g., `id`, `class`, `src`, `href`, `alt`, `title`, `lang`, `disabled`, `type`).
- **Describe the basic structure of an HTML document.** What are the essential components (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`)?
- What is the purpose of the `<head>` tag? What kind of elements can go in the `<head>` (e.g., `<title>`, `<meta>`, `<link>`, `<script>`, `<style>`)? What is the difference between the `<head>` and `<body>` sections?
- What is the purpose of the `<body>` tag?
- **What does `<!DOCTYPE html>` declaration do?** Why is it important? What happens if you omit it (browser quirks mode)?
- **What are semantic HTML elements?** Why are they important (accessibility, SEO, developer understanding, maintainability)? List some common semantic elements introduced in HTML5 (e.g., `<article>`, `<section>`, `<aside>`, `<nav>`, `<header>`, `<footer>`, `<main>`).
- **Explain the difference between `<div>` and `<span>`.** When and why would you use each?
- **How do you create a hyperlink in HTML?** What is the primary attribute used? What is the purpose of the `href` attribute in an anchor (`<a>`) tag?
- **How do you insert an image in HTML?** What are the essential attributes for `<img>` (`src`, `alt`)?
- **What are HTML lists?** (ordered `<ol>`, unordered `<ul>`, description/definition `<dl>`).
  - How do you create an unordered list? What tag is used for list items (`<li>`)?
  - How do you create an ordered list? What are some attributes for ordered lists (e.g., `type`, `start`)?
  - How do you create a description list? What are the tags involved (`<dl>`, `<dt>`, `<dd>`)?
  - Can you nest lists within each other? How?
- **How do you create a basic table in HTML?** What are the essential tags (`<table>`, `<tr>`, `<td>`)? What is the purpose of `<th>`? How is it different from `<td>`?
- **What are HTML forms?** What is the purpose of the `<form>` tag? What are the `action` and `method` attributes of a form? Explain the difference between `GET` and `POST` methods. When would you use each?
- List and describe several common input types in HTML5 (e.g., `text`, `password`, `checkbox`, `radio`, `submit`, `button`, `file`, `hidden`, `date`, `email`, `number`).
- What is the purpose of the `name` attribute on form inputs?
- What is the purpose of the `value` attribute on form inputs?
- Explain the `<label>` element. How do you associate a label with a form control (explicitly using `for` and `id`, vs. implicitly by wrapping)? Why is this important for accessibility?
- What is the `<textarea>` element used for?
- How do you create a dropdown list/select box? What are the `<select>` and `<option>` tags? What is the `multiple` attribute for `<select>`?
- **How do you add comments in HTML?** Why are comments useful?
- **What is the difference between `id` and `class` attributes?** Can an element have multiple classes? Can it have multiple IDs?
- What is the difference between block-level and inline elements? Provide examples of each. How does their default behavior affect layout? Can this behavior be changed (using CSS `display` property)?
- What happens if a browser encounters an HTML tag it doesn't recognize? (It usually treats it as an inline element or ignores it for rendering purposes but it remains in the DOM).
- How do you set the character encoding for an HTML document? Why is `UTF-8` commonly recommended?
- What is the purpose of the `lang` attribute in the `<html>` tag?
- Explain the purpose and usage of `data-*` attributes. How and why are they used (storing custom data, accessible via JS)?
- What are HTML entities? Why are they needed? Give examples of common entities (e.g., `&nbsp;`, `&lt;`, `&gt;`, `&amp;`, `&copy;`).
- How can you embed audio and video in HTML5? What are some important attributes for the `<video>` tag (e.g., `src`, `controls`, `autoplay`, `loop`, `muted`, `poster`)? How do you provide multiple video/audio source formats for better browser compatibility (using the `<source>` element)?
- Explain the `<canvas>` vs `<svg>` elements. When would you use one over the other (canvas for pixel manipulation/games, SVG for resolution-independent graphics/icons)? How can you embed SVG in HTML (inline, `<img>`, `<object>`, `<iframe>`)?
- What is the importance of the `alt` attribute on `<img>` tags? Why is it critical for accessibility?
- How do you make a website responsive using HTML and CSS (meta viewport tag)?
- What are `<iframe>` elements used for? What are their security considerations (e.g., `sandbox` attribute)?
- What is the DOM (Document Object Model)? How does HTML structure relate to the DOM tree (conceptual understanding)?
- Explain different ways to specify a URL in `href` (absolute, relative, root-relative).
- What is the purpose of the `target` attribute in anchor tags? What does `target="_blank"` do? What are the security implications of `_blank` and how can they be mitigated (e.g., `rel="noopener noreferrer"`)?
- How do you link to a specific part of a page (internal link/fragment identifier using `#id`)?
- What are the `width` and `height` attributes on an `<img>` tag? How do they impact page rendering and layout shifts (preventing CLS)?
- Explain the `<picture>` element. How can it be used for responsive images or art direction (providing different image sources based on media conditions)?
- Explain the use of `<thead>`, `<tbody>`, and `<tfoot>`. Why are they useful for structuring tables (semantics, scrolling for large tables)?
- How do you make table cells span multiple rows or columns (`rowspan`, `colspan`)?
- What is the `<caption>` element used for with tables?
- How can you make HTML tables more accessible (e.g., `scope` attribute on `<th>`, `id` and `headers` attributes for complex tables - Mid+)?
- Explain HTML5 form validation. Discuss attributes like `required`, `pattern`, `minlength`, `maxlength`, `min`, `max`, `step`, and `type` validation (e.g., `type="email"`).
- What is the `novalidate` attribute on a form?
- What is the `placeholder` attribute? What are its accessibility limitations (i.e., not a replacement for `<label>`)?
- What are the `<fieldset>` and `<legend>` elements used for in forms (grouping related controls)?
- How do you disable a form control (using the `disabled` attribute)? What is the `readonly` attribute and how does it differ from `disabled`?
- What is the difference between `src` and `href` attributes? Provide examples of elements that use each (`<img>` uses `src`, `<a>` and `<link>` use `href`).
- How do you include external CSS in HTML? What are different ways to apply CSS to HTML (External `<link>`, internal `<style>`, inline `style` attribute - discuss pros and cons of each)?

## Ⅲ. CSS (Cascading Style Sheets) 🎨

This section covers CSS fundamentals, layout, responsiveness, and intermediate topics.

- **What is CSS?** What does CSS stand for and what is its primary role in web development?
- **What are the different ways to include CSS in a web page?** (inline, internal/embedded, external). What are the pros and cons of each?
- **What is a CSS selector?** Why are they important? Give examples of different types of selectors (element/type, class, ID, attribute, pseudo-class, pseudo-element).
- **What is the CSS Box Model?** Explain its components (content, padding, border, margin).
- **What is the difference between `margin` and `padding`?**
- **What is CSS specificity?** How is it calculated (inline, IDs, classes/attributes/pseudo-classes, elements/pseudo-elements - general weighting)?
- What happens when two CSS rules have the same specificity and target the same element? (The last one declared in the source order wins).
- **What are `block`, `inline`, and `inline-block` display values?** How do they differ in terms of layout behavior (width, height, margin, surrounding content)?
- **How do you change the font family, size, and color of text using CSS properties like `font-family`, `font-size`, `color`?**
- **What is the `float` property traditionally used for?** What are its common issues (e.g., container collapse)?
- What is the `clear` property and how is it used to address issues with floats (e.g., `clear: both` on an element after floated elements, or using a clearfix technique)?
- **What is the `z-index` property?** What does it do, and on which elements does it work (positioned elements)? What is a "stacking context"? How is a new stacking context formed (e.g., by `position` other than `static` with a `z-index`, `opacity < 1`, `transform`)?
- **What are pseudo-classes?** Give examples (e.g., `:hover`, `:focus`, `:active`, `:nth-child()`, `:first-child`, `:last-child`, `:not()`).
- **What are pseudo-elements?** Give examples (e.g., `::before`, `::after`, `::first-letter`, `::first-line`, `::placeholder`). What's the difference between single colon (`:`) and double colon (`::`) notation (single for older pseudo-classes/elements, double preferred for pseudo-elements)?
- **How do you center an element (e.g., a `div`) horizontally? Vertically? Both?** Discuss different methods (e.g., `margin: auto` for horizontal centering of block elements with a width; Flexbox or Grid for both horizontal and vertical centering).
- **What is the difference between `visibility: hidden;` and `display: none;`?** What about `opacity: 0;`? Discuss impact on layout, accessibility, and event handling.
- Explain the basic syntax of a CSS rule. (Selector, declaration block, property, value).
- What is the difference between `class` and `ID` selectors? When should you use one over the other (ID for unique elements, class for multiple reusable styles)? Can an element have multiple classes? Multiple IDs (no, ID must be unique)?
- What are attribute selectors? Provide examples of different attribute selectors (e.g., `[attr]`, `[attr=value]`, `[attr^=value]`, `[attr$=value]`, `[attr*=value]`).
- What are universal selectors (`*`) and type selectors (e.g., `h1`, `div`)?
- What are combinators in CSS? Explain descendant (` `), child (`>`), adjacent sibling (`+`), and general sibling (`~`) combinators with examples.
- How do you group selectors? (Comma-separated list).
- What does the `!important` rule do in CSS? Why should its use be minimized (it breaks the cascade and makes debugging harder)?
- How do you add comments in CSS? (`/* comment */`).
- What is the difference between `rem`, `em`, `px`, `vh`, `vw`, `%` and other CSS units? When would you use each (px for fixed, em/rem for scalable typography/layout, vh/vw for viewport-relative sizing)?
- How do colors work in CSS? Explain different ways to define colors (keywords, hex, RGB, RGBA, HSL, HSLA).
- What are CSS vendor prefixes (e.g., `-webkit-`, `-moz-`, `-ms-`)? Are they still as necessary as they once were (less so, but sometimes for newer or experimental features)? How do tools like Autoprefixer help?
- **What is Flexbox?** What are its main use cases (1D layout)?
- Explain the difference between the main axis and the cross axis in Flexbox. How can `flex-direction` change them?
- Explain `display: flex` and `display: inline-flex`.
- What are the key properties for the flex container? (`flex-direction`, `flex-wrap`, `justify-content`, `align-items`, `align-content`, `gap`). Explain common values for `justify-content` and `align-items`.
- What are the key properties for flex items? (`order`, `flex-grow`, `flex-shrink`, `flex-basis`, `flex` shorthand, `align-self`). Explain `flex-grow: 1`.
- **What is CSS Grid Layout?** What are its main use cases (2D layout)?
- How does CSS Grid differ fundamentally from Flexbox? When would you choose Grid over Flexbox, or use them together?
- Explain `grid-template-columns` and `grid-template-rows`. How do you define track sizes (fixed, percentage, `auto`, `fr` unit)? What is the `fr` unit?
- How do you place items onto the grid? (Line-based placement: `grid-column-start/end`, `grid-row-start/end`; shorthand `grid-column`, `grid-row`). (Named areas are Mid+).
- What is the `gap` (or `row-gap`, `column-gap`) property in Grid/Flexbox?
- **What are Media Queries?** How do you use them in CSS (`@media`)? Explain common media features (e.g., `width`, `height`, `orientation`).
- What is the difference between mobile-first and desktop-first approaches to RWD? Which is generally recommended and why (mobile-first often leads to cleaner code and better performance on mobile)?
- What are breakpoints in RWD? How do you choose them (based on content, not specific devices)?
- **What are CSS Custom Properties (CSS Variables)?** How do you declare and use them? What are their benefits (e.g., theming, maintainability, reducing repetition)? How do they differ from preprocessor variables (they are live in the browser)?
- **How does `box-sizing` property work?** Explain the difference between `content-box` (default) and `border-box`. Why is `border-box` often preferred (easier to reason about element dimensions)?
- Explain the "Cascade" in CSS. What factors determine which styles are applied (origin and importance, selector specificity, order of appearance)?
- Explain the concept of CSS Inheritance. Which CSS properties are typically inherited by default (e.g., `color`, `font-family`), and which are not (e.g., `background-color`, `border`, `padding`, `margin`)?
- How can you explicitly make a property inherit from its parent? (using the `inherit` keyword).
- What is the difference between `inherit`, `initial`, `unset`, and `revert` keyword values (conceptual for Mid+)?
- What is the `:root` pseudo-class? How is it commonly used, especially with CSS Custom Properties (defining global variables)?
- What is the purpose of CSS Resets or Normalizers (e.g., Normalize.css, Reset CSS)? How do they differ (reset removes all default styles, normalize makes them consistent)?
- Explain CSS positioning: `static` (default), `relative`, `absolute`, `fixed`, and `sticky`. How does each relate to the document flow and containing blocks?
- How do you create basic CSS transitions for smooth property changes? (Individual properties: `transition-property`, `transition-duration`, `transition-timing-function`, `transition-delay`, or shorthand `transition`).
- How do you create basic CSS animations using `@keyframes` and the `animation` property?
- What is the `transform` property? List some common 2D transform functions (`translate()`, `rotate()`, `scale()`, `skew()`). How do transforms affect the document flow (they don't, the element's original space is preserved)?
- What are CSS preprocessors (e.g., Sass/SCSS, LESS)? What are their main benefits (variables, nesting, mixins, functions, partials/imports)? (Conceptual understanding of benefits and common features).
- How can you hide an element visually but keep it accessible to screen readers (e.g., using a "visually-hidden" class with specific CSS properties)?

## Ⅳ. JavaScript (JS) 🚀

This section delves into JavaScript fundamentals, asynchronous programming, DOM manipulation, ES6+ features, and more, tailored for these levels.

- **What is JavaScript?** Is it a compiled or interpreted language? Is it single-threaded or multi-threaded?
- **What are JavaScript Data Types?** List all primitive types (`string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, `null`) and explain what an object (non-primitive type) is.
- **What is the difference between `null` and `undefined`?**
- **What are variables in JavaScript?** How do you declare them using `var`, `let`, and `const`? Explain the differences regarding scope (global, function, block), hoisting, and re-assignment/re-declaration.
- **What is "hoisting" in JavaScript?** How does it affect variable (with `var`) and function declarations?
- What is the Temporal Dead Zone (TDZ) for `let` and `const`? (Conceptual understanding that you can't access them before declaration).
- **What are JavaScript operators?** Give examples of arithmetic, assignment, comparison, logical (`&&`, `||`, `!`), bitwise (awareness), and ternary operators.
- **What is the difference between `==` (loose equality) and `===` (strict equality)?** Explain type coercion and why `===` is generally preferred.
- What is type coercion (or type conversion)? Provide examples of implicit and explicit coercion.
- What does "short-circuiting" mean in the context of logical operators (`&&`, `||`)?
- What are truthy and falsy values in JavaScript? List all falsy values (`false`, `0`, `-0`, `0n`, `""` (empty string), `null`, `undefined`, `NaN`).
- **How do you write functions in JavaScript?** (Function Declaration/Statement, Function Expression, Arrow Functions).
- What is the difference between a function declaration and a function expression regarding hoisting? (Declarations are fully hoisted, expressions are not).
- **What are arrow functions (ES6)?** What are their key characteristics and differences from traditional functions (e.g., lexical `this` binding, no `arguments` object, cannot be used as constructors)?
- **What is the `this` keyword in JavaScript?** Explain how its value is determined in different contexts:
  - Global context (window in browsers, or `undefined` in strict mode modules).
  - Function context (simple call - value depends on strict mode).
  - As a method of an object (`this` refers to the object).
  - With the `new` keyword (constructor call - `this` refers to the newly created instance).
  - With `call()`, `apply()`, and `bind()` (how they explicitly set `this`).
  - In arrow functions (`this` is lexically inherited from the surrounding scope).
  - In DOM event handlers (`this` typically refers to the element that triggered the event, unless an arrow function is used as the handler).
- **Explain scope in JavaScript.** Define global scope, function (local) scope, and block scope (introduced by `let` and `const`).
- What is lexical (or static) scope? (Scope is determined by where variables/functions are declared during authoring time).
- **What are closures?** Explain how they work with an example. Why are they useful (e.g., data privacy/encapsulation, partial application, callbacks, remembering state)?
- What is an IIFE (Immediately Invoked Function Expression)? What are its use cases (e.g., avoiding global scope pollution, creating private scope)?
- **What are objects in JavaScript?** How do you create objects (object literal, constructor functions, `Object.create()`, ES6 classes - focus on literals and constructors/classes)?
- How do you access, add, modify, and delete properties of an object? (dot notation vs. bracket notation - when to use bracket notation).
- **Explain prototypal inheritance in JavaScript.** How does it work? What is the prototype chain? (Conceptual: objects inherit from other objects).
- What is the `prototype` property on functions? What is `__proto__` (or `Object.getPrototypeOf()`) on objects?
- How does the `new` keyword work? What steps does it perform (creates new object, sets prototype, calls constructor with `this`, returns object)?
- What is the ES6 `class` syntax? Is it just syntactic sugar over prototypal inheritance? Explain `constructor`, methods, `super` (for inheritance).
- How can you check if an object has a specific property? (`in` operator, `hasOwnProperty()`).
- What are common ways to iterate over an object's properties? (`for...in` loop - iterates over enumerable properties including inherited ones; `Object.keys()`, `Object.values()`, `Object.entries()` - iterate over own enumerable properties).
- **What are arrays in JavaScript?** Are they a special type of object (yes)?
- List common array methods for adding/removing elements: `push`, `pop`, `shift`, `unshift`, `splice`. Explain what each does.
- List common array methods for iteration and transformation: `forEach`, `map`, `filter`, `reduce`, `some`, `every`, `find`, `findIndex`. Explain their purpose and provide examples.
- What is the difference between `map()` and `forEach()`? (`map` returns a new array, `forEach` does not).
- How does `Array.prototype.reduce()` work? Provide a practical example (e.g., summing an array, flattening an array of arrays).
- How can you create a new array from an existing one? (e.g., `slice()`, spread syntax `...`).
- How do you check if a variable is an array? (`Array.isArray()`).
- What is the difference between `for...in` and `for...of` loops when iterating over an array? (`for...in` iterates over keys/indices as strings and includes inherited properties; `for...of` iterates over values and works with iterables). Which one is generally preferred for arrays and why (`for...of`)?
- What is synchronous vs. asynchronous programming? Why is asynchronous programming important in JavaScript, especially in the browser (to avoid blocking the main thread)?
- **Explain the JavaScript Event Loop in detail (for Mid+).** Discuss the roles of the Call Stack, Web APIs (Browser APIs), Callback Queue (Task Queue / Macrotask Queue), and Microtask Queue.
- What is the difference between the Microtask Queue and the Macrotask Queue? Which tasks have higher priority? Give examples of tasks that go into each (e.g., `Promise.then()` for microtask, `setTimeout()` for macrotask).
- What are callback functions in the context of asynchronous operations? What is "Callback Hell" (Pyramid of Doom) and how can it be avoided (Promises, `async/await`)?
- **What are Promises?** Explain their states (`pending`, `fulfilled`, `rejected`). How do you create and use them (`new Promise()`, `.then()`, `.catch()`, `.finally()`)?
- What is a Promise chain? How do you handle errors in a Promise chain (a single `.catch()` at the end can handle errors from any preceding promise)?
- **What is `async/await`?** How does it relate to Promises? What are its benefits (makes async code look more synchronous and easier to read)?
- How do you handle errors in `async/await` functions? (using `try...catch` blocks).
- What is the Fetch API? How does it compare to `XMLHttpRequest` (XHR) (Fetch is Promise-based, more modern API)? How do you make GET and POST requests using Fetch?
- Explain `setTimeout()` and `setInterval()`. How can you clear them (`clearTimeout()`, `clearInterval()`)?
- **What is the DOM (Document Object Model)?** How is it represented (a tree structure)?
- What is the difference between `window` and `document` objects? (`window` is the global object in browsers, `document` represents the loaded page).
- How do you select HTML elements using JavaScript? (e.g., `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, `querySelectorAll`). What are the differences in what they return (single element vs. HTMLCollection/NodeList)?
- How do you create, add, modify, and remove HTML elements and their attributes using JavaScript? (e.g., `createElement`, `appendChild`, `removeChild`, `setAttribute`, `removeAttribute`, `classList`).
- What is the difference between `innerHTML`, `innerText`, and `textContent`? What are the security implications of using `innerHTML` (potential XSS if input is not sanitized)?
- Explain event handling in JavaScript. (Event listeners, event objects, `addEventListener()`, `removeEventListener()`).
- What is event bubbling and event capturing (trickling)? How can you stop event propagation (`event.stopPropagation()`)? What is `event.preventDefault()` used for?
- What is event delegation? Why is it useful (performance for many similar elements, handling dynamically added elements) and how is it implemented (attach listener to parent, check `event.target`)?
- What are data attributes (`data-*`) and how can you access them using JavaScript (`element.dataset`)?
- **What are template literals (template strings) from ES6?** What are their benefits (multiline strings, string interpolation `${expression}`)?
- **What is destructuring assignment (ES6) for arrays and objects?** Provide examples.
- **What is the spread syntax (`...`) and rest parameters (`...`) (ES6)?** Provide examples for arrays, objects, and function arguments. How do they differ?
- What are default parameters in functions (ES6)?
- What are ES6 Modules (`import`/`export`)? How do they differ from other module systems (e.g., CommonJS - conceptual)? Discuss static vs. dynamic imports (Mid+).
- What are Symbols in ES6? What are their use cases (e.g., unique property keys, well-known symbols like `Symbol.iterator` - conceptual for Mid+)?
- What are Maps and Sets in ES6? How do they differ from objects and arrays? (Map for key-value pairs where keys can be any type, Set for unique values).
- What is optional chaining (`?.`) (ES2020)?
- What is the nullish coalescing operator (`??`) (ES2020)? How does it differ from the logical OR (`||`) operator?
- What is `Array.prototype.at()` (ES2022)? (Allows negative indexing).
- How do you perform a shallow copy vs. a deep copy of an object? (Shallow: spread syntax, `Object.assign`. Deep: `JSON.parse(JSON.stringify(obj))` - with its limitations, or custom recursive function/library).
- What is JSON? How do you parse it (`JSON.parse()`) and stringify to it (`JSON.stringify()`)?

## Ⅴ. TypeScript (TS) 🔷

This section focuses on TypeScript's features, benefits, and how it enhances JavaScript development, for these levels.

- **What is TypeScript?** Explain its relationship to JavaScript. What are the main goals and benefits of using TypeScript (static typing, better tooling, catching errors early, improved code readability and maintainability)?
- How does TypeScript differ from JavaScript (static typing, compilation step)?
- How do you install TypeScript? How do you compile a TypeScript file to JavaScript (`tsc` command)?
- **What are the basic data types in TypeScript?** (e.g., `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`, `any`, `unknown`, `void`, `never`).
- **What is type annotation in TypeScript?** Provide examples for variables, function parameters, and function return types.
- **What is type inference in TypeScript?** How does it work? When is it good to rely on it, and when should you use explicit annotations (for clarity, function boundaries)?
- **What is the `any` type?** When might it be used (migrating JS, complex third-party types)? What are its downsides (loses type safety), and why is its use generally discouraged?
- **What is the `unknown` type?** How does it differ from `any` (safer, requires type checking/assertion before use)? Why is it a safer alternative to `any`?
- **What is the `void` type?** When is it typically used (for functions that don't return a value)?
- What is the `never` type? Explain its purpose and provide examples (functions that always throw or have infinite loops).
- How do you handle `null` and `undefined` in TypeScript? Explain strict null checks (`strictNullChecks` compiler option).
- What are literal types? (e.g., type `Direction = 'left' | 'right'; let dir: Direction = 'left';`).
- What is the difference between `Array<T>` and `T[]` for defining array types? (Syntax preference, both are same).
- What are tuples in TypeScript? How do they differ from arrays (fixed size, known types at each position)? Provide a use case.
- What are optional properties in objects/interfaces (`propertyName?: type`)?
- What are readonly properties (`readonly propertyName: type`)? How do they differ from `const` (`const` is for variables, `readonly` for properties)?
- **What are interfaces in TypeScript?** How are they used to define the shape of an object?
- **What are type aliases in TypeScript (`type Name = ...`)?** How can they be used?
- **What is the difference between an `interface` and a `type` alias?** When would you choose one over the other (interfaces for object shapes and declaration merging; types for primitives, unions, intersections, mapped types)?
- Can interfaces extend other interfaces? Can type aliases (using intersection types `&`)?
- What are enums in TypeScript? Why are they useful (named constants)?
- Explain numeric enums and string enums. What are advantages of string enums (readability, debugging)?
- What are type assertions (or type casting) in TypeScript? What are the two syntaxes (`<Type>value` and `value as Type`)? When is it used (when you know more than the compiler), and what are its risks (can suppress legitimate type errors)?
- **What are union types (`|`)?** How are they used to allow a value to be one of several types?
- **What are intersection types (`&`)?** How are they used to combine multiple types into one?
- What is "type narrowing"? Explain common techniques for type narrowing (e.g., `typeof` checks, `instanceof` checks, truthiness checks, equality checks, `in` operator).
- What are "type guards"? How to create custom type guards (using `value is TypeName` predicate).
- What are "discriminated unions" (or tagged unions)? How do they work with a common literal property to enable powerful type narrowing (Mid+)?
- **What are generics in TypeScript?** Why are they important for creating reusable, type-safe components (functions, classes, interfaces)?
- Provide an example of a generic function (e.g., `function identity<T>(arg: T): T { return arg; }`). How does type inference work with generic type parameters?
- Provide an example of a generic interface or type alias.
- What are generic constraints? How can you use the `extends` keyword to limit the types that can be used as a type argument (e.g., `<T extends Lengthwise>`)?
- Explain some common built-in utility types and their purpose (Mid+):
  - `Partial<T>` (makes all properties of T optional).
  - `Required<T>` (makes all properties of T required).
  - `Readonly<T>` (makes all properties of T readonly).
  - `Pick<T, K>` (creates a type by picking specified keys K from T).
  - `Omit<T, K>` (creates a type by omitting specified keys K from T).
  - `Record<K, T>` (constructs an object type with keys of type K and values of type T).
- How are classes defined in TypeScript? Explain `constructor`, properties, methods.
- What are access modifiers in TypeScript classes? (`public` (default), `private`, `protected`). How do they differ?
- How can interfaces be used with classes (`implements` keyword)? Can a class implement multiple interfaces?
- Explain parameter properties in constructors (e.g., `constructor(private name: string)` as shorthand).
- What is the `tsconfig.json` file? What is its primary role (compiler configuration)?
- Explain some of the most important compiler options in `tsconfig.json` (Mid+): `target`, `module`, `outDir`, `rootDir`, `strict`, `strictNullChecks`, `noImplicitAny`, `esModuleInterop`, `sourceMap`.
- What are declaration files (`.d.ts`) in TypeScript? What is their purpose (providing type information for JavaScript code)?
- What is DefinitelyTyped (`@types/package-name`)? How does it help with using JavaScript libraries in TypeScript projects?

## Ⅵ. Data Structures & Algorithms (DSA) 📊

This section covers DSA concepts relevant to frontend development for these levels.

- **What is Big O notation?** Why is it important for frontend developers (e.g., understanding performance implications of loops, array operations)? (Conceptual: O(1), O(n), O(n log n), O(n^2)).
- Explain common data structures and their relevance in frontend:
  - **Arrays:** Common methods like `push`, `pop`, `map`, `filter`, `reduce`, `find`, `slice`, `splice`. Basic understanding of their typical performance (e.g., accessing by index is O(1), `unshift`/`shift` can be O(n)).
  - **Objects:** Used for key-value pairs (like dictionaries or hash maps). Accessing/adding/deleting properties is typically fast (average O(1)).
  - **Stacks & Queues:** Conceptual understanding (LIFO for stack, FIFO for queue). Use cases like managing browser history (stack-like) or task scheduling (queue-like in event loop).
  - **Trees:** Especially the DOM tree (how HTML is structured) and component trees in React. Basic tree traversal ideas (conceptual).
  - **Sets:** For storing unique collections of values.
  - **Maps:** For key-value pairs where keys can be any type (unlike plain objects where keys are strings/symbols).
- Explain common algorithms:
  - **Iteration vs. Recursion:** Understand both ways to repeat operations. What is recursion (function calling itself)? What is a base case in recursion?
  - **Searching algorithms:** Linear search (iterating through an array). Binary search (for sorted arrays - conceptual understanding of how it's more efficient).
- **Frontend Specific Problems/Concepts:**
  - How would you efficiently render a list of items that could be very long? (Pagination is a common approach; virtualization/windowing is a Mid+ concept).
  - How to implement a `debounce` or `throttle` function? Explain use cases (e.g., debouncing search input, throttling scroll/resize events).
  - How to flatten a simple nested array (e.g., `[[1, 2], [3, 4]]` to `[1, 2, 3, 4]`).
  - Problems related to string manipulation (e.g., reverse a string, check if a string is a palindrome, count character occurrences).
  - Problems related to array manipulation (e.g., remove duplicates from an array, merge two sorted arrays (Mid+), find the missing number in a sequence).
  - Logic for UI components (e.g., pagination logic, simple filtering of a list based on user input).

## Ⅶ. React ⚛️

This section is dedicated to React, covering core concepts, hooks, and patterns relevant for these levels.

- **What is React?** What problems does it solve? Explain its primary purpose and philosophy (declarative, component-based, UI library).
- **What are the main features of React?** (e.g., Virtual DOM, JSX, Component-Based Architecture, Unidirectional Data Flow).
- **What is JSX?** How does it differ from HTML? Explain how JSX gets transpiled (into `React.createElement()` calls). Can you use React without JSX (yes, but it's verbose)?
- **What are React Components?**
  - Differentiate between Functional Components and Class Components. Which is generally preferred now and why (Hooks make functional components more powerful and concise)?
  - How do you create a simple Functional Component?
- **What is the Virtual DOM (VDOM)?** How does it work (in-memory representation, diffing algorithm)? How does it help improve performance (minimizes direct DOM manipulation)?
- What is an "element" in React? How is it different from a "component" (element is what a component returns, a description of what to render; component is a function or class that produces elements)?
- **What is the difference between `state` and `props` in React?**
  - Are they mutable or immutable (props are immutable from child's perspective; state is managed within the component and updated via its setter)?
  - How is data passed between components? (Parent to Child via props). How can a child communicate back to a parent (passing callback functions as props)?
- What is "unidirectional data flow" in React? (Data flows down from parent to child via props).
- **How do you handle events in React?** (e.g., `onClick`, `onChange`). How are React events different from native DOM events (SyntheticEvent - a cross-browser wrapper)?
- **What is conditional rendering in React?** Describe different ways to achieve it (e.g., `if/else`, ternary operator, logical `&&` operator, element variables).
- **How do you render lists of items in React?** What is the significance of the `key` prop in lists? What happens if you don't use keys, or use non-unique/index keys incorrectly (issues with reconciliation, state management in list items)?
- **What are React Fragments (`<React.Fragment>` or `<>...</>`)?** Why are they useful (avoiding unnecessary wrapper DOM elements)?
- How do you style components in React? Discuss different approaches (inline styles, CSS stylesheets, CSS Modules - conceptual for Mid+, Styled-components/Emotion - awareness for Mid+).
- What is "prop drilling"? What are common ways to avoid it (Context API, state management libraries - conceptual for Mid+)?
- What does "lifting state up" mean? When and why would you do it (when multiple components need to share/reflect the same changing data)?
- What are controlled components vs. uncontrolled components in forms? When would you use each (controlled for React handling state, uncontrolled for simpler forms or integrating with non-React code)?
- What is the `children` prop? How is it used (to pass content between opening and closing tags of a component)?
- Explain the process of "reconciliation" in React. What is the heuristic algorithm React uses (diffing algorithm - conceptual understanding)?
- **What are Hooks in React?** Why were they introduced? What problems do they solve (allow using state and other React features in functional components)?
- **What are the "Rules of Hooks"?** (Only call Hooks at the top level, only call Hooks from React functions). Why are these rules important (to ensure hooks are called in the same order on every render)?
- **Explain the `useState()` Hook.** How do you update state with it? Does `setState` (from `useState`) update state synchronously or asynchronously (asynchronously, batched for performance)?
- **Explain the `useEffect()` Hook.**
  - What are its common use cases (side effects: data fetching, subscriptions, manually changing the DOM)?
  - What is the dependency array (`[]`, `[dep1, dep2]`, no array)? How does it control when the effect runs?
  - How do you perform cleanup in `useEffect` (by returning a function)? When does the cleanup function run (before component unmounts, or before effect runs again)?
- **Explain the `useContext()` Hook.** How does it help avoid prop drilling by providing a way to pass data through the component tree without having to pass props down manually at every level?
- Explain the `useReducer()` Hook (Mid+). When might you prefer it over `useState` (for more complex state logic, or when next state depends on previous one)? Provide a simple example.
- Explain the `useCallback()` Hook (Mid+). What problem does it solve (memoizing callback functions to prevent unnecessary re-renders of child components that rely on referential equality of props)? How does it relate to referential equality and performance optimization (e.g., with `React.memo`)?
- Explain the `useMemo()` Hook (Mid+). What problem does it solve (memoizing expensive computations so they are not re-calculated on every render)? How does it differ from `useCallback` (`useCallback` memoizes functions, `useMemo` memoizes values)?
- Explain the `useRef()` Hook. What are its common use cases (accessing DOM elements, storing mutable values that don't trigger re-renders)? How is it different from `createRef()` (used in class components or for refs not tied to component lifecycle)?
- What are Custom Hooks? Why are they powerful (reusing stateful logic)? How do you create one? Provide a simple example (e.g., `useToggle`, `useFormInput`).
- What is `React.memo()`? How does it work for optimizing functional components (shallow comparison of props)? How does it compare to `PureComponent` for class components?
- What are Error Boundaries? How do they work (using class components with `componentDidCatch` or `static getDerivedStateFromError` to catch JS errors in their child component tree), and why are they important for robust applications? Can a functional component be an error boundary directly (no, but you can use a class component wrapper or a library)?
- What are Portals in React (Mid+)? What are their use cases (e.g., modals, tooltips, rendering children into a different DOM node)?
- What is `React.lazy()` for code-splitting? How is it used with `Suspense` (Mid+)?

## Ⅷ. Next.js NEXT

This section covers Next.js, a popular React framework, focusing on features relevant for these levels. (Focus on this if the role requires Next.js)

- **What is Next.js?** What problems does it solve as a React framework (e.g., pre-rendering, routing, API creation)?
- Why would you choose Next.js over a client-side React setup (e.g., using Create React App or Vite with vanilla React)? What are the key advantages (SEO benefits from pre-rendering, performance, built-in routing, API routes)?
- **What are the main features of Next.js?** (e.g., Rendering Strategies - SSR, SSG, ISR; File-system Routing, API Routes/Route Handlers, Image Optimization, Internationalization - conceptual for Mid+).
- How do you create a new Next.js application? (Using `create-next-app`).
- Explain the different rendering strategies available in Next.js (conceptual understanding of each):
  - Client-Side Rendering (CSR)
  - Server-Side Rendering (SSR)
  - Static Site Generation (SSG)
  - Incremental Static Regeneration (ISR) (Mid+)
- What is pre-rendering in Next.js? Which rendering strategies involve pre-rendering (SSR, SSG, ISR)?
- What is hydration? Why is it necessary (to make server-rendered HTML interactive)?
- **App Router (`app/` directory - Preferred for new projects as of May 2025)** (Focus on these if job description implies modern Next.js)
  - What is the `app` directory in Next.js? How does file-system based routing work within it (folders define segments, `page.js` defines UI)?
  - What are Layouts (`layout.js`/`layout.tsx`)? How do they enable shared UI? What is a Root Layout?
  - What are Pages (`page.js`/`page.tsx`)?
  - What are Server Components and Client Components in the App Router?
    - By default, are components in the App Router Server or Client Components (Server)?
    - What is the `"use client"` directive? When and why do you use it (for components needing interactivity, state, effects, browser APIs)?
    - What are the capabilities of Server Components (e.g., direct data access, no state/effects)?
    - How is data fetching typically done in Server Components? (Using `async/await` with `Workspace`).
  - How do you create dynamic route segments (e.g., `[slug]`)?
  - How does navigation work in the App Router? (Using `<Link>` component from `next/link`).
  - How do you create API endpoints in the App Router? (Using Route Handlers in `route.js`/`route.tsx` files).
- **Pages Router (`pages/` directory - For existing projects or if specified)**
  - What was the `pages` directory used for? How did file-system based routing work?
  - How was dynamic routing handled in the Pages Router? (e.g., `[id].js`).
  - What were API Routes in the `pages/api` directory?
  - What was `_app.js` (or `_app.tsx`) used for (global layout, shared state)?
  - What was `_document.js` (or `_document.tsx`) used for (customizing `<html>` and `<body>` tags)?
  - How did data fetching methods like `getStaticProps` and `getServerSideProps` work in the Pages Router? What are their main differences (build time vs. request time)?
  - (Mid+) What is `getStaticPaths` used for (defining dynamic paths for SSG)?
- What is the `next/image` component? What benefits does it provide over the standard `<img>` tag (automatic image optimization, responsive images, lazy loading)?
- What are the key props for `next/image`? (`src`, `width`, `height`, `alt`; `fill` and `priority` for Mid+).
- What is the `next/font` component/module? How does it help optimize web fonts (self-hosting, reducing layout shift)?
- What is `next/script` component (Mid+)? How can it be used to optimize the loading of third-party scripts using its `strategy` prop?
- How do you handle environment variables in Next.js? (`.env` files, `NEXT_PUBLIC_` prefix for browser exposure).
- What is `next.config.js` used for (basic configurations like redirects, rewrites, image domains - Mid+)?

## Ⅸ. React Ecosystem & Libraries 📚

This section explores common libraries and tools used in conjunction with React, focusing on conceptual understanding for these levels.

### State Management (Redux, Zustand, Jotai, Recoil, etc.)

- Why might you need a state management library beyond React's built-in state (`useState`) and Context API? (For large applications with complex, shared state).
- What are the differences between local component state, Context API, and global state management libraries (conceptual)?
- **Redux (if mentioned or experienced):**
  - What are the core principles of Redux (single source of truth, state is read-only, changes via pure functions/reducers - conceptual)?
  - Explain Actions, Reducers, Store, Dispatch (basic understanding of the flow).
  - What is Redux Toolkit? How does it simplify Redux development (reduces boilerplate)?
- **Zustand/Jotai/Recoil/Valtio (awareness for Mid+):**
  - Have you heard of other state management libraries? How might they differ from Redux (often simpler, less boilerplate)?

### Routing (React Router)

- How does React Router work to enable client-side routing in a Single Page Application (SPA)? (Updates URL, renders different components without full page reload).
- What are the main components of React Router (v6+)? (`<BrowserRouter>`, `<Routes>`, `<Route>`, `<Link>`, `<NavLink>`, `<Outlet>`, `useNavigate`, `useParams` - be familiar with `Link`, `Route`, `Routes`, `useNavigate`, `useParams`).
- How do you create nested routes and layouts using `<Outlet>` (Mid+)?
- How do you implement programmatic navigation (`useNavigate`)?
- How do you handle route parameters (`useParams`) for dynamic routes?
- How do you implement protected/private routes for authentication (conceptual: conditional rendering based on auth state)?

### Data Fetching & Caching (Axios, Fetch API, SWR, React Query/TanStack Query)

- How do you make API calls in React applications? Compare native Fetch API with libraries like Axios (Axios has features like interceptors, easier error handling, broader browser support historically).
- What are the benefits of using server state libraries like SWR or TanStack Query (formerly React Query) (Mid+)?
  - Caching strategies (e.g., `stale-while-revalidate` - conceptual).
  - Automatic refetching.
  - Loading and error state management.
- How do you handle mutations (POST, PUT, DELETE requests) and update cache with these libraries (Mid+ - conceptual: invalidating queries)?

### UI Libraries (Material UI, Ant Design, Chakra UI, Tailwind CSS with Headless UI)

- What are the pros and cons of using pre-built component libraries versus building custom components (pros: speed, consistency, accessibility often built-in; cons: bundle size, customization limits, learning curve)?
- How do you customize components from these libraries to fit a specific design (usually via props, theme providers, or overriding styles)?
- How does Tailwind CSS (a utility-first CSS framework) differ from traditional component libraries?

### Form Handling (Formik, React Hook Form)

- What are the common challenges of handling forms in React (managing form state for multiple inputs, validation, submission, error handling)?
- How do libraries like Formik or React Hook Form simplify form handling in React (Mid+)?
  - State management for form inputs.
  - Validation (schema-based with Yup/Zod or custom).
  - Handling form submission.
- Compare controlled vs. uncontrolled component approaches in forms.

## Ⅹ. Design Patterns & Refactoring 🏗️

This section explores basic software design principles and code improvement relevant for these levels.

### Design Patterns

- What are design patterns? Why are they useful in software development (provide reusable solutions to common problems, improve code structure and communication)?
- **React Specific (Focus on Custom Hooks and Context API for these levels):**
  - What are Custom Hooks in React? How are they a pattern for reusing stateful logic? Provide a simple example.
  - How is the Provider Pattern (using Context API) used for sharing data without prop drilling?
  - (Mid+) What were Higher-Order Components (HOCs) or Render Props? How do Custom Hooks often provide a simpler alternative?
  - (Mid+) What are Container/Presentational Components (Smart/Dumb Components)? What was the idea (separating logic from UI)? How do Hooks affect this pattern?

### Refactoring

- What is code refactoring? Why is it important for the health of a codebase (improving readability, maintainability, reducing complexity)?
- When should you refactor code? What are common "code smells" that indicate a need for refactoring (e.g., duplicated code, long functions/components, unclear names)?
- What does the DRY (Don't Repeat Yourself) principle mean?
- How does strong test coverage support and enable effective refactoring (gives confidence that changes don't break existing functionality)?

## XI. Testing 🧪

This section covers the principles and practices of testing frontend applications for these levels.

- **Why is testing important in software development?** What are the benefits (catching bugs early, ensuring code quality, facilitating refactoring, documentation)?
- **What are different types of tests?** Briefly explain Unit, Integration, and End-to-End (E2E) tests. Focus on understanding Unit and basic Integration tests.
- **What is Jest?** What is it primarily used for in the React ecosystem (Test runner, assertion library, mocking capabilities)?
- **What is React Testing Library (RTL)?** What is its core philosophy ("test behavior, not implementation details")? How does it encourage testing components the way users interact with them?
- How do you write a simple unit test for a React component using Jest and RTL? (Rendering the component, basic queries to find elements, simple assertions about content or presence).
- What are "matchers" in Jest? Give examples (e.g., `toBe`, `toEqual`, `toBeTruthy`, `toContain`, `toHaveBeenCalled`).
- How do you select/query for elements using React Testing Library? (e.g., `getByText`, `getByRole`, `getByLabelText`, `getByTestId`). Which queries are preferred and why (accessibility-focused queries like `getByRole` are often best)?
- What is a "test case" (usually an `it` or `test` block) or "test suite" (usually a `describe` block)?
- How do you test React components with props? (Pass props when rendering the component in your test and assert the output changes accordingly).
- How do you mock functions in Jest (`jest.fn()`)? Why is mocking necessary (to isolate tests, avoid actual API calls or complex dependencies)?
- How do you test asynchronous operations in React components (e.g., data fetching) (Mid+)? (Using `async/await` with RTL's `waitFor` or `findBy*` queries).
- How do you test custom Hooks (Mid+)? (Using `@testing-library/react`'s `renderHook`).
- What is code coverage? How do you interpret it (percentage of code executed by tests)? Is 100% coverage always the goal (not necessarily, focus on testing critical paths and logic)?
- How do you simulate user events (e.g., clicks, input changes, form submissions) with RTL and `@testing-library/user-event`?
- What is the difference between `getBy*`, `queryBy*`, and `findBy*` queries in RTL? When to use each (`getBy*` throws error if not found, `queryBy*` returns null, `findBy*` for async elements)?
- What are snapshot tests (Mid+)? What are their pros and cons (pros: quick way to test UI structure; cons: can be brittle, may hide implementation details, require frequent updates)?

## XII. Tooling 🛠️

This section covers essential tools used in modern frontend development, focusing on awareness and basic usage for these levels.

- **Package Managers:**
  - What is `npm`? What is `yarn`? What is `pnpm` (awareness for Mid+)? What are they used for (installing, managing, and sharing project dependencies/packages)?
  - What is a `package.json` file? What are its main sections (`name`, `version`, `dependencies`, `devDependencies`, `scripts`)?
  - What is `package-lock.json` or `yarn.lock`? Why are they important for reproducible builds (they lock down the exact versions of dependencies)?
  - What is semantic versioning (SemVer - `MAJOR.MINOR.PATCH`) and its implications for managing dependencies (understanding `^` and `~` in version numbers)?
- **Module Bundlers (Webpack, Parcel, Rollup, esbuild, Vite):**
  - What is a JavaScript module bundler? Why is it needed in modern frontend development (to bundle multiple JS files and assets into fewer files for the browser, enable features like code splitting, transformations)?
  - Have you heard of Webpack or Vite? What do they do? (Conceptual understanding is fine; Vite often preferred for new projects due to speed).
  - What is tree shaking (bundlers removing unused code to reduce bundle size - conceptual)?
  - What is code splitting (bundlers breaking code into smaller chunks that can be loaded on demand - conceptual)?
- **Transpilers (Babel):**
  - What is Babel? Why is it used in JavaScript and React projects (to convert newer JavaScript syntax and JSX into code that older browsers can understand)?
- **Linters & Formatters (ESLint, Prettier, Stylelint):**
  - What is linting (analyzing code for potential errors and style issues)? What is formatting (automatically styling code)? Why are they important for code quality, consistency, and preventing bugs?
  - Have you used ESLint or Prettier? How do they help?
- **Version Control (Git):**
  - Explain basic Git commands: `git clone`, `git add`, `git commit -m "message"`, `git push`, `git pull`, `git branch <name>`, `git checkout <branch/commit>`, `git merge <branch>`, `git status`, `git log`.
  - What is a Git branch? Why are branches useful in a team environment (working on features/bugs in isolation)?
  - What is `git merge`? What are merge conflicts and how do you resolve them (manually editing files to choose correct changes)?
  - Explain a common Git workflow (e.g., create a feature branch, make commits, push, create a Pull Request/Merge Request for review and merging into main/develop).
  - What is `.gitignore` file used for?
  - What are pull requests (PRs) or merge requests (MRs)? (A way to propose changes and have them reviewed before merging).
- **Developer Tools (Browser & Framework-specific):**
  - How do you use browser developer tools effectively for debugging and development?
    - Elements/Inspector panel (inspecting/modifying DOM and CSS).
    - Console panel (logging messages, errors, interacting with JS).
    - Sources panel (debugging JS, setting breakpoints, stepping through code - Mid+).
    - Network panel (analyzing network requests, checking status codes, response payloads - basic usage).
  - What are React DevTools or similar tools for other frameworks? How do they help in debugging component hierarchy, state, and props?
  - What are source maps? Why are they useful for debugging transpiled code (they map compiled code back to original source)?
- **CI/CD (Continuous Integration/Continuous Deployment/Delivery) (Awareness for Mid+):**
  - What is CI/CD (conceptual: automating build, test, deployment)? What are its benefits (faster releases, better quality)?

## XIII. Live Coding Questions 💻

This section lists common problem areas for live coding interviews for these levels, typically involving React and basic TypeScript if applicable.

- **UI Component Implementation (Stateless & Stateful) using React:**
  - **Typed Counter:** Props: `initialCount?: number`. State: current count. Func: Increment, Decrement buttons.
  - **Typed Toggle/Switch:** Props: `isOn: boolean`, `onToggle: (newState: boolean) => void`. Func: Clicking toggles its state.
  - **Character Counter Input:** Props: `maxLength: number`. Display: "X/Y characters".
  - **Basic Tabs Component:** Props: `tabs: Array<{ title: string; content: string | React.ReactNode }>`. State: Active tab ID. Func: Clicking a tab displays its content.
  - **Simple Star Rating (display only or basic interaction):** Props: `rating: number`. Func: Visually represents rating.
  - **Simple Image Carousel (Next/Previous buttons, no complex features):** Props: `images: Array<string (url)>`. State: Current image index.
  - **Basic Progress Bar:** Props: `percentage: number`. Visually represents percentage.
  - **Basic Modal/Dialog (focus on rendering/closing, less on advanced a11y for junior):** Props: `isOpen: boolean`, `onClose: () => void`.
  - **Simple Accordion (one item open at a time).**
  - **Todo List (Add item, display list. Bonus: remove item, toggle complete - for Junior+/Mid).**
- **State Management & Hooks (with TypeScript if applicable):**
  - **Simple Form with `useState`:** Few input fields, controlled components, display submitted data. Basic client-side validation (e.g., required field).
  - **Data Fetching with `useEffect`, `useState`:** Fetch data from a public API (e.g., `https://jsonplaceholder.typicode.com/todos/1`). Define a simple `interface` or `type` for the expected API response structure (if TS). Handle loading and display data or error message.
  - **Custom Hook: `useToggle(initialValue: boolean): [boolean, () => void]` (simple version).**
  - **(Mid+) Custom Hook: `useLocalStorage<T>(key: string, initialValue: T): [T, (value: T | ((val: T) => T)) => void]` (simpler version without advanced error handling).**
  - **(Mid+) Custom Hook: `useDebounce<T>(value: T, delay: number): T` (understanding the concept and basic implementation).**
- **JavaScript/Algorithm Challenges (Frontend Flavored):**
  - Reverse a string.
  - Check if a string is a palindrome.
  - Find the most frequent character in a string / Count characters in a string.
  - Flatten a simple nested array (e.g., one or two levels deep).
  - Remove duplicates from an array.
  - FizzBuzz problem.
  - Sum all numbers in an array.
  - Filter an array based on a condition.
- **CSS Challenges (Less common for extensive live coding, more for discussion or small snippets):**
  - Recreate a simple layout (e.g., a card, a header with logo and nav).
  - Center an element horizontally and vertically using Flexbox.
- **React Specific:**
  - Manage state for a small interactive component.
  - Pass data from a parent to a child component using props.
  - Call a parent function from a child component (callback props).

## XIV. Behavioral & Situational Questions 🤔

These questions assess soft skills, problem-solving approach, teamwork, and experience, relevant for all these levels.

- Tell me about a challenging project you worked on (can be personal, academic, or professional if applicable). What were the challenges, and how did you overcome them?
- Describe a time you had a conflict with a team member or classmate. How did you resolve it (or attempt to)?
- How do you stay updated with new technologies and trends in frontend development? What are you learning currently?
- Tell me about a time you made a mistake or failed at something. What did you learn from it?
- How do you handle tight deadlines or pressure (if experienced, otherwise how you imagine you would)?
- How do you approach debugging an issue in your code? Describe your thought process.
- What are your strengths as a developer (or aspiring developer)? What is an area you'd like to improve or learn more about?
- Why are you interested in this role/company? (Do your research!).
- Where do you see yourself in 3-5 years? / What are your career goals in frontend development?
- How do you contribute to code reviews (if experienced, or how would you approach it)? What do you look for when reviewing someone else's code, or what kind of feedback do you find helpful?
- Describe your experience working in an Agile/Scrum environment (if any, otherwise conceptual understanding).
- How do you prioritize tasks when you have multiple things to do?
- How do you approach learning new technologies or programming concepts?
- How do you collaborate with others in a team (developers, designers, product managers - if experienced, otherwise how you prefer to)?
- How do you handle feedback, especially constructive criticism?
- Imagine you're starting a new project/task. What questions would you ask to understand the requirements better?
- How do you contribute to a positive and productive team environment?
