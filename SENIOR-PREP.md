# Comprehensive Frontend Developer Interview FAQs (React Focused)

This document provides an exhaustive list of frequently asked questions for frontend developer interviews, with a strong emphasis on React and its ecosystem. Questions span all levels, from trainee to architect, and are organized by topic for a structured study approach.

## Ⅰ. The Web & Internet 🌐🔗

This section covers foundational knowledge about how the internet and web technologies work, including performance, security, and accessibility.

### Web & Internet Fundamentals

- How does the internet work? (High-level overview)
- What is HTTP/HTTPS? Explain common HTTP methods (GET, POST, PUT, DELETE, PATCH, OPTIONS, HEAD).
- What are HTTP status codes? (e.g., 200, 201, 400, 401, 403, 404, 500) Categorize them (1xx, 2xx, 3xx, 4xx, 5xx).
- What is DNS? How does DNS resolution work?
- What is a domain name? What is hosting?
- What is a browser? How does it render a webpage? (Critical Rendering Path)
- What are cookies? How are they used? What are their security implications?
- What is `localStorage` vs `sessionStorage` vs `cookies`? Discuss capacity, use cases, and security.
- What is CORS (Cross-Origin Resource Sharing)? How do you handle it? Why is it needed?
- What is RESTful API design? What are the principles of a RESTful API?
- What is GraphQL? How is it different from REST? (More relevant for mid/senior) What are its advantages and disadvantages?
- What are WebSockets? How do they differ from HTTP? When are they used (real-time communication)?
- What is Server-Sent Events (SSE)? How does it compare to WebSockets?
- What is AJAX?
- Explain the Fetch API. How do you make GET/POST requests? How do you handle responses and errors?
- What are HTTP headers? Give examples of request headers and response headers.
- What is the difference between HTTP/1.1, HTTP/2, and HTTP/3? What are the key improvements in newer versions (e.g., multiplexing, header compression, QUIC)?
- What is caching in the context of HTTP? (Browser cache, proxy cache, CDN cache).
- What is API versioning? Why is it important and what are common strategies?
- How do you debug network requests in the browser? (Network tab in DevTools).

### Web Performance

- Why is web performance important? (Discuss user experience, conversion rates, SEO, accessibility).
- What are the key metrics to measure web performance? (e.g., Core Web Vitals: LCP, FID/INP, CLS; also FCP, TTFB, TTI). Explain what each measures.
- How do you measure web performance? (Lighthouse, WebPageTest, DevTools)
- What is the Critical Rendering Path? How can you optimize it? How does CSS block rendering?
- What are common techniques to optimize website loading speed?
  - Minification, compression (Gzip, Brotli), image optimization (formats like WebP, AVIF, JPEG, PNG, SVG; compression; responsive images with `<picture>` or `srcset`), caching (browser, CDN), code splitting, lazy loading, reducing HTTP requests.
- What is a CDN (Content Delivery Network)? How does it improve performance and availability?
- How does browser rendering impact performance? (Reflow/Layout, Repaint/Composite)
- Explain techniques for reducing page load time (Minification, compression, caching, CDN, code splitting, image optimization, etc.).
- What is "code splitting"? How does it improve initial load time?
- What is "lazy loading"? For which types of assets is it most beneficial (images, components, routes)? How is it implemented? How can it be implemented using the HTML `loading` attribute?
- How do you optimize images for the web? (Formats: WebP, AVIF, JPEG, PNG, SVG; compression; responsive images with `<picture>` or `srcset`).
- What are browser caching mechanisms? (HTTP caching headers: `Cache-Control`, `Expires`, `ETag`, `Last-Modified`). How do they work?
- How can you minimize HTTP requests? (e.g., combining files (less critical with HTTP/2+), CSS sprites (less common now), inlining critical assets).
- Explain the difference between `async` and `defer` attributes for script loading. When would you use each?
- What is "tree shaking"? How does it help reduce bundle size? How do bundlers like Webpack or Rollup use it?
- How can you identify performance bottlenecks in a web application? (Using browser DevTools: Network tab, Performance tab, Lighthouse).
- What is "perceived performance" vs. "actual performance"? How can you improve perceived performance? (Skeletons screens, optimistic UI updates).
- How do fonts impact web performance? How can you optimize font loading? (`font-display`, WOFF2 format, preloading critical fonts).
- What is "render-blocking CSS/JS"? How do you mitigate it?
- Discuss strategies for optimizing CSS delivery.
- What are resource hints (`preload`, `prefetch`, `preconnect`, `dns-prefetch`)? How can they be used in HTML to optimize loading of critical resources?
- How does server-side rendering (SSR) or static site generation (SSG) impact different performance metrics compared to client-side rendering (CSR)?
- What is the impact of third-party scripts on performance? How can you manage them effectively?
- How would you approach optimizing a slow-loading webpage? Describe your step-by-step process. (For senior levels: involve profiling, identifying bottlenecks, prioritizing fixes).
- What is "Critical CSS"? How can you inline critical CSS for faster perceived load times?
- How can you reduce CSS file size? (Minification, removing unused CSS, using shorthand properties, efficient selectors).
- How does the browser parse CSS? From right to left or left to right? Why is this important for selector performance?
- (Architect Level) How do you establish a performance budget? How do you monitor and maintain performance over time for a large application?

### Web Security

- What are common web security vulnerabilities a frontend developer should be aware of?
- What is Cross-Site Scripting (XSS)?
  - Explain stored, reflected, and DOM-based XSS.
  - How can you prevent XSS vulnerabilities in frontend code (e.g., proper data escaping/encoding, sanitizing user input, Content Security Policy)? How do you prevent XSS in HTML forms? (Focus on HTML-level encoding, though primary defense is server-side/JS framework).
- What is Cross-Site Request Forgery (CSRF)? How can it be mitigated (e.g., CSRF tokens, SameSite cookies)? How does the frontend play a role?
- What is Content Security Policy (CSP)? How does it work and what types of attacks can it help prevent? How can HTML contribute to a Content Security Policy (CSP)? (e.g., through meta tags, though typically set via HTTP headers).
- What are common security best practices for handling user authentication and authorization on the client-side? (Token storage: `localStorage` vs. cookies with `HttpOnly` and `Secure` flags; handling JWTs).
- What is `HTTPS`? Why is it crucial? What is HSTS (HTTP Strict Transport Security)?
- What are `HttpOnly` and `Secure` flags for cookies? What do they do?
- What is the `SameSite` cookie attribute? How does it help prevent CSRF?
- What are Subresource Integrity (SRI) hashes? How do they enhance security when loading assets from CDNs?
- What is "clickjacking"? How can it be prevented (e.g., `X-Frame-Options` header)?
- What security considerations are there when using `<iframe>` elements? (e.g., `sandbox` attribute, `allow` attribute).
- What is the risk of using `dangerouslySetInnerHTML` in React or similar methods in other frameworks?
- How can you ensure dependencies (npm packages) are secure and up-to-date? (e.g., `npm audit`, dependabot).
- What is "Man-in-the-Middle" (MitM) attack in the context of web applications?
- How can frontend code contribute to protecting against data breaches (e.g., not logging sensitive info to console)?
- What are security headers you should be aware of beyond CSP and X-Frame-Options? (e.g., `Referrer-Policy`, `Permissions-Policy`).
- Why is it generally unsafe to use `eval()` or the `Function` constructor with arbitrary strings?
- (Architect Level) How do you design a secure frontend architecture? What are threat modeling and secure coding practices?

### Accessibility (a11y)

- What is web accessibility (a11y)? Why is it important (ethical, legal, business reasons)?
- What are the WCAG (Web Content Accessibility Guidelines)? Briefly explain their purpose and the four principles (POUR: Perceivable, Operable, Understandable, Robust). What are conformance levels (A, AA, AAA)?
- How can semantic HTML contribute to accessibility?
- What is ARIA (Accessible Rich Internet Applications)? When should you use ARIA attributes? When should you prefer native HTML semantics? What is the first rule of ARIA?
- Explain common ARIA roles, states, and properties with examples (e.g., `role="navigation"`, `aria-labelledby`, `aria-describedby`, `aria-hidden`, `aria-expanded`, `aria-live`).
- How do you ensure keyboard accessibility? (Focus order, visible focus indicators, keyboard-operable custom widgets). What is "keyboard accessibility"?
- What is the importance of providing text alternatives for non-text content (e.g., `alt` text for images, transcripts for audio, captions for video)? What makes a good `alt` text? When might you leave it empty (`alt=""`)?
- How do you ensure sufficient color contrast? What tools can help check this?
- How can you design accessible forms? (Labels, fieldsets, legends, error messages, validation, keyboard navigation). How do you ensure forms are accessible?
- How do screen readers work with web content? What can developers do to ensure a good screen reader experience? How can developers test with screen readers?
- What are common accessibility pitfalls to avoid in frontend development?
- How can you test for web accessibility? (Automated tools like axe, Lighthouse; manual testing with keyboard; screen reader testing).
- What is the `prefers-reduced-motion` media query? How should it be handled?
- How does responsive design contribute to accessibility?
- Discuss how to make dynamic content updates (e.g., in SPAs) accessible (ARIA live regions, managing focus).
- How would you approach auditing and improving the accessibility of an existing web application?
- How do you ensure that custom interactive elements (e.g., modals, tabs, accordions built with JS) are accessible?
- What is the purpose of `tabindex`? How can it be used to manage focus order (`0`, `-1`, positive values)? What are best practices for using `tabindex`?
- How do you make links accessible beyond just descriptive text? (Consider focus indicators, skip links).
- What is the difference between `<label>` and `aria-label` or `aria-labelledby`? When would you use ARIA labeling?
- How do you hide content accessibly? (e.g., visually hidden but available to screen readers vs. completely hidden with `display:none` or `aria-hidden="true"`).
- Why is it important to provide clear visual focus indicators for interactive elements (`:focus`, `:focus-visible`)?
- What are some accessibility considerations when using pseudo-elements like `::before` and `::after` for content?
- Can `display: none` or `visibility: hidden` affect accessibility? How?
- What care should be taken when overriding default browser styles for form elements to ensure they remain accessible?
- (Architect Level) How do you embed accessibility into the development lifecycle and company culture?

## Ⅱ. HTML (HyperText Markup Language) 🌐

This section focuses on HTML structure, semantics, and features.

### HTML - Trainee/Junior Level

- **What is HTML?** What does HTML stand for?
- **What is the primary purpose of HTML in web development?** Explain its relationship with CSS and JavaScript.
- **What is an HTML element?** Describe its common structure (opening tag, content, closing tag).
- What is the difference between an element and a tag?
- **What are HTML tags?** Are all tags paired? Give an example of an empty/void tag.
- **What are HTML attributes?** Provide examples and explain their purpose (e.g., `id`, `class`, `src`, `href`).
- **Describe the basic structure of an HTML document.** What are the essential components (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`)?
- What is the purpose of the `<head>` tag? What is the difference between the `<head>` and `<body>` sections?
- What is the purpose of the `<body>` tag?
- **What does `<!DOCTYPE html>` declaration do?** Why is it important? What happens if you omit it?
- **What are semantic HTML elements?** Why are they important? (e.g., `<article>`, `<aside>`, `<nav>`, `<header>`, `<footer>`, `<main>`). Discuss accessibility, SEO, developer understanding, maintainability.
- List some semantic elements introduced in HTML5. (e.g., `<article>`, `<section>`, `<aside>`, `<nav>`, `<header>`, `<footer>`, `<main>`).
- **Explain the difference between `<div>` and `<span>`.** When and why would you use each?
- **How do you create a hyperlink in HTML?** What is the primary attribute used? What is the purpose of the `href` attribute in an anchor (`<a>`) tag?
- **How do you insert an image in HTML?** What are the essential attributes for `<img>`?
- **What are HTML lists?** (ordered, unordered, description/definition)
  - How do you create an unordered list? What tag is used for list items?
  - How do you create an ordered list? What are some attributes for ordered lists (e.g., `type`, `start`, `reversed`)?
  - How do you create a description list (formerly definition list)? What are the tags involved (`<dl>`, `<dt>`, `<dd>`)?
  - Can you nest lists within each other? How?
- **How do you create a table in HTML?** What are the essential tags (`<table>`, `<tr>`, `<td>`)?
- **What are HTML forms?** What is the purpose of the `<form>` tag? What are some common form input types?
- **How do you add comments in HTML?** Why are comments useful?
- **What is the difference between `id` and `class` attributes?** Can an element have multiple classes? Can it have multiple IDs?
- What is the difference between block-level and inline elements? Provide examples of each. How does their default behavior affect layout? Can this behavior be changed?
- What happens if a browser encounters an HTML tag it doesn't recognize?
- How do you set the character encoding for an HTML document? Why is `UTF-8` commonly recommended?
- What is the purpose of the `lang` attribute in the `<html>` tag?

### HTML - Mid Level

- What is the difference between `GET` and `POST` methods in HTML forms? What are the `action` and `method` attributes of a form? When would you use each?
- Explain the purpose and usage of `data-*` attributes. How and why are they used?
- What are HTML entities? Why are they needed? Give examples of common entities (e.g., `&nbsp;`, `&lt;`, `&gt;`, `&amp;`, `&copy;`).
- How can you embed audio and video in HTML5? What are some important attributes for the `<video>` tag (e.g., `src`, `controls`, `autoplay`, `loop`, `muted`, `poster`, `preload`)? How do you provide multiple video/audio source formats for better browser compatibility? (using `<source>` element). How do you embed audio in HTML?
- Explain the `<canvas>` vs `<svg>` elements. When would you use one over the other? How is SVG different from raster image formats (like PNG, JPG)? How can you embed SVG in HTML?
- What is the importance of the `alt` attribute on `<img>` tags? Why is it critical for accessibility?
- How do you make a website responsive using HTML and CSS (meta viewport tag)?
- What are `<iframe>` elements and what are their security implications? What are its security considerations (e.g., `sandbox` attribute, `allow` attribute)?
- What is the purpose of `aria-*` attributes in HTML? (Accessibility)
- Explain the concept of character encoding in HTML (e.g., UTF-8).
- Explain the appropriate use cases for `<article>`, `<section>`, `<div>`, `<aside>`, and `<nav>`. How do you decide which to use? Provide scenarios.
- What is the purpose of the `<main>` element? How many `<main>` elements can a page typically have?
- What's the difference between `<strong>`, `<b>`, `<em>`, and `<i>` tags? Discuss their semantic meaning versus presentational styling.
- How would you structure a typical blog homepage versus a single blog post page using semantic HTML5 elements?
- What is the purpose of heading tags (`<h1>` to `<h6>`)? How should they be used for structuring content and for SEO?
- How do you represent a quotation in HTML? Differentiate between `<blockquote>` and `<q>`. What is the `cite` attribute used for in these contexts?
- Explain the purpose of the `<figure>` and `<figcaption>` elements.
- What is the `<address>` tag used for?
- What is the DOM (Document Object Model)? How does HTML structure relate to the DOM tree? (Basic understanding for juniors, deeper for seniors regarding manipulation and virtual DOMs).
- What is the difference between HTML and XHTML? Is XHTML still widely used today?
- Explain different ways to specify a URL in `href` (absolute, relative, root-relative).
- What is the purpose of the `target` attribute in anchor tags? What does `target="_blank"` do? What are the security implications of `_blank` and how can they be mitigated (e.g., `rel="noopener noreferrer"`)?
- How do you link to a specific part of a page (internal link/fragment identifier)?
- What is the difference between `<a href="#top">` and `<a href="#">`?
- How do you create an email link? A telephone link?
- What is the purpose of the `title` attribute on an anchor tag (and other elements)?
- How do you make an image a link?
- What are the `width` and `height` attributes on an `<img>` tag? How do they impact page rendering and layout shifts?
- Explain the `<picture>` element. How can it be used for responsive images or art direction?
- What are image maps (`<map>` and `<area>`)? Are they still commonly used?
- How can you make media elements accessible (e.g., captions/subtitles for video, transcripts for audio)?
- What is the purpose of `<th>`? How is it different from `<td>`?
- Explain the use of `<thead>`, `<tbody>`, and `<tfoot>`. Why are they useful for structuring tables?
- How do you make table cells span multiple rows or columns (`rowspan`, `colspan`)?
- What is the `<caption>` element used for with tables?
- How can you make HTML tables more accessible? (e.g., `scope` attribute, `id` and `headers` attributes).
- List and describe several common input types in HTML5 (e.g., `text`, `password`, `checkbox`, `radio`, `submit`, `button`, `file`, `hidden`, `date`, `email`, `number`, `range`, `search`, `tel`, `url`).
- What is the purpose of the `name` attribute on form inputs?
- What is the purpose of the `value` attribute on form inputs?
- Explain the `<label>` element. How do you associate a label with a form control (explicitly vs. implicitly)? Why is this important for accessibility?
- What is the `<textarea>` element used for?
- How do you create a dropdown list/select box? What are the `<select>` and `<option>` tags? What is the `multiple` attribute for `<select>`?
- What is the `<optgroup>` element used for?
- What is the difference between `<button>` and `<input type="button">` (or `type="submit"`, `type="reset"`)? When might you prefer `<button>`?
- Explain HTML5 form validation. Discuss attributes like `required`, `pattern`, `minlength`, `maxlength`, `min`, `max`, `step`, and `type` validation.
- What is the `novalidate` attribute on a form?
- What is the `placeholder` attribute? What are its accessibility limitations (i.e., not a replacement for `<label>`)?
- What is the `autocomplete` attribute? How can it enhance user experience? What are security/privacy considerations?
- What are the `<fieldset>` and `<legend>` elements used for in forms?
- How do you disable a form control? (using the `disabled` attribute). What is the `readonly` attribute?
- What is the purpose of the `<datalist>` tag? How does it provide suggestions for input fields?
- How can you group radio buttons so that only one can be selected at a time?

### HTML - Senior/Architect Level

- Discuss the evolution of HTML (HTML4 vs HTML5). What are some key new features in HTML5?
- How can HTML be optimized for search engines (SEO)? Explain how well-structured, semantic HTML impacts SEO.
- Explain Shadow DOM. How does it relate to Web Components? What problems does it solve?
- Discuss the performance implications of different HTML structures and how to optimize them. How can you optimize HTML structure for faster page load times and rendering? (e.g., minimizing DOM depth, critical rendering path).
- How do you handle internationalization (i18n) and localization (l10n) at the HTML level?
- What are Progressive Web Apps (PWAs) and how does HTML structure contribute to them (e.g., manifest file)?
- Discuss strategies for handling offline capabilities in web applications using HTML5 APIs.
- How would you design an HTML structure for a highly scalable and maintainable large application?
- Discuss the security aspects related to HTML (e.g., preventing XSS by sanitizing user input rendered in HTML).
- What are Web Components (Custom Elements, Shadow DOM, HTML Templates)? How do they relate to HTML and extending its vocabulary?
- What is the purpose of the `<template>` tag?
- What is Web Storage (`localStorage` and `sessionStorage`)? How do they differ from cookies? Discuss capacity, use cases, and security.
- What is the HTML5 Drag and Drop API? Briefly outline how it works. How do you make an HTML element draggable?
- What is the purpose of the `contenteditable` attribute? What are the risks associated with it?
- What is the `spellcheck` attribute and how is it used?
- Explain the `<details>` and `<summary>` elements. How can they create simple accordions?
- What is the purpose of the `<progress>` and `<meter>` tags? How do they differ?
- What is Microdata? How is it used in HTML for semantic purposes? How does it compare to RDFa and JSON-LD for structured data?
- What is the difference between `src` and `href` attributes? Provide examples of elements that use each.
- How do you include external CSS in HTML? What are different ways to apply CSS to HTML? (External, internal, inline - discuss pros and cons).
- Why is the `<title>` tag crucial for both SEO and user experience?
- What is the purpose of the `<meta name="description">` tag?
- What are Open Graph meta tags? How do they influence how content appears when shared on social media (e.g., Facebook, Twitter Cards)?
- How do you specify canonical URLs in HTML (e.g., `<link rel="canonical">`)? Why is this important for duplicate content issues?
- What is structured data (e.g., Schema.org vocabulary using JSON-LD, Microdata, RDFa)? How is it implemented in or alongside HTML to improve SEO and enable rich snippets?
- What is the impact of invalid HTML on performance, SEO, and browser rendering?
- Explain the difference between progressive enhancement and graceful degradation. How does this philosophy apply to HTML development?
- How do you display code snippets effectively in HTML? Discuss the use of `<code>`, `<pre>`, and the importance of escaping characters.
- What happens if the browser doesn't support JavaScript? How can HTML provide a baseline experience (e.g., `<noscript>` tag)?
- What is an "HTML validator"? Why is it useful to validate your HTML?
- What are some common HTML mistakes developers make?
- Be prepared to explain a standard HTML5 boilerplate.

## Ⅲ. CSS (Cascading Style Sheets) 🎨

This section covers CSS fundamentals, layout, responsiveness, and advanced topics.

### CSS - Trainee/Junior Level

- **What is CSS?** What does CSS stand for and what is its primary role in web development?
- **What are the different ways to include CSS in a web page?** (inline, internal/embedded, external). What are the pros and cons of each?
- **What is a CSS selector?** Why are they important? Give examples of different types of selectors (element, class, ID, attribute).
- **What is the CSS Box Model?** Explain its components (content, padding, border, margin).
- **What is the difference between `margin` and `padding`?**
- **What is CSS specificity?** How is it calculated (inline, IDs, classes/attributes/pseudo-classes, elements/pseudo-elements)?
- What happens when two CSS rules have the same specificity and target the same element?
- **What are `block`, `inline`, and `inline-block` display values?**
- **How do you change the font family and color of text?**
- **What is the `float` property used for?** What are its common issues (e.g., container collapse)?
- What is the `clear` property and how is it used to address issues with floats?
- **What is the `z-index` property and how does it work?** What is a "stacking context"?
- **What are pseudo-classes (e.g., `:hover`, `:focus`) and pseudo-elements (e.g., `::before`, `::after`)?** What's the difference between single colon (`:`) and double colon (`::`) notation?
- **How do you center a `div` element horizontally?** Vertically? Both?
- **What is the difference between `visibility: hidden;` and `display: none;`?** What about `opacity: 0;`? Discuss impact on layout and accessibility.
- Explain the basic syntax of a CSS rule. (Selector, declaration block, property, value).
- What is the difference between `class` and `ID` selectors? When should you use one over the other? Can an element have multiple classes? Multiple IDs?
- What are attribute selectors? Provide examples.
- What are universal selectors (`*`) and type selectors (e.g., `h1`, `div`)?
- What are combinators in CSS? Explain descendant (` `), child (`>`), adjacent sibling (`+`), and general sibling (`~`) combinators with examples.
- How do you group selectors?
- What does the `!important` rule do in CSS? Why should its use be minimized?
- How do you add comments in CSS?
- What is the difference between `rem`, `em`, `px`, `vh`, `vw`, `%` and other CSS units? When would you use each?
- How do colors work in CSS? Explain different ways to define colors (keywords, hex, RGB, RGBA, HSL, HSLA).

### CSS - Mid Level

- **Explain CSS positioning** (static, relative, absolute, fixed, sticky). What is a "containing block"?
- **What is Flexbox?** Explain its main concepts (container, items, main axis, cross axis, `flex-direction`, `justify-content`, `align-items`, `flex-grow`, `flex-shrink`, `flex-basis`).
- **What is CSS Grid Layout?** How does it differ from Flexbox? Explain grid lines, tracks, cells, areas, `grid-template-columns/rows`, `fr` unit, `gap`.
- **What are media queries?** How are they used for responsive web design? Explain common media features.
- What is the `viewport` meta tag and why is it crucial for RWD?
- What is the difference between mobile-first and desktop-first approaches to RWD?
- **What are CSS variables (custom properties)?** How do you declare and use them? What are their benefits?
- **Explain the concept of `BEM` (Block, Element, Modifier)** or other CSS methodologies (SMACSS, OOCSS, ITCSS).
- **What are CSS preprocessors (e.g., Sass, LESS)?** What are their advantages (variables, nesting, mixins, functions, inheritance, partials)?
- **How does `box-sizing: border-box;` work?** Why is it useful? Why is `border-box` often preferred over `content-box`?
- **What are CSS transitions and animations?** Explain `@keyframes`. Differentiate between them.
- Explain the "Cascade" in CSS. What factors determine which styles are applied (origin and importance, selector specificity, order of appearance)?
- Explain the concept of CSS Inheritance. Which properties are typically inherited? How can you explicitly make a property inherit? (`inherit` keyword).
- What is the difference between `inherit`, `initial`, `unset`, and `revert` keyword values?
- What is the `:root` pseudo-class? How is it commonly used?
- What is the purpose of CSS Resets or Normalizers? How do they differ?
- Explain the `:is()` and `:where()` pseudo-classes. How do they affect specificity?
- What is the `:has()` relational pseudo-class?
- What are collapsing margins? How do they occur and how can you prevent them?
- How does `outline` differ from `border`?
- What is CSS Multi-column Layout?
- What is the `aspect-ratio` property?
- How do you make images responsive? (e.g., `max-width: 100%`).
- What are Container Queries (`@container`)? How do they differ from Media Queries?
- What is the `transform` property? List some common transform functions.
- What are CSS Blend Modes (`mix-blend-mode`, `background-blend-mode`)?
- What are CSS Filters (`filter` property)?
- What is the `clip-path` property used for?
- How do you create gradients in CSS?
- What are common CSS properties for styling text?
- What are web fonts? How do you use `@font-face`? What is `font-display`?
- What are CSS logical properties and values (e.g., `margin-inline-start`)? Why are they important for internationalization?
- What is PostCSS? How is it different from a preprocessor?
- What are CSS Modules? How do they help with local scope?
- What are CSS-in-JS solutions? Pros and cons?

### CSS - Senior/Architect Level

- Discuss advanced CSS layout techniques and when to use them (e.g., multi-column layout, writing modes, subgrid).
- How would you structure CSS for a large-scale application? (e.g., CSS-in-JS, CSS Modules, Atomic CSS/Utility-first CSS like Tailwind CSS). Compare different approaches.
- Explain CSS performance optimization techniques (e.g., reducing selectors complexity, avoiding reflows/repaints, understanding hardware acceleration for animations).
- How does the browser render CSS? Explain the CSSOM and Render Tree.
- Discuss the pros and cons of different CSS architectures.
- How can CSS be used to improve website accessibility beyond basic ARIA?
- What is "containment" in CSS (`contain` property)?
- Discuss the future of CSS (e.g., Houdini, new CSS features like Cascade Layers `@layer`).
- How would you design a theming system using CSS? (Custom properties, JS interaction).
- Explain the concept of "CSS Custom Paint API" (Houdini). How do Houdini APIs extend CSS capabilities?
- How do you approach CSS refactoring in a legacy project?
- What is the `will-change` property? When and how should it be used cautiously?
- What are CSS Shapes (`shape-outside`)?
- What is `object-fit` and `object-position`?
- How can `@layer` (CSS Cascade Layers) help in managing CSS specificity and organizing large codebases?
- What are some common CSS anti-patterns to avoid?
- How can CSS choices impact web accessibility? (Color contrast, focus indicators, hiding content).

## Ⅳ. JavaScript (JS) 🚀

This section delves into JavaScript fundamentals, asynchronous programming, DOM manipulation, ES6+ features, and more.

### JavaScript - Trainee/Junior Level

- **What is JavaScript?** Is it a compiled or interpreted language? Is it single-threaded or multi-threaded?
- **What are the different data types in JavaScript?** List all primitive types and explain what an object is.
- **How do you declare a variable (using `var`, `let`, `const`)?** What are the differences regarding scope, hoisting, and re-assignment?
- **What is scope in JavaScript (global, function, block)?**
- **What is hoisting?** How does it affect variable and function declarations?
- **What is the difference between `==` (loose equality) and `===` (strict equality)?** Explain type coercion.
- **What are `null` and `undefined`?**
- **How do you write a function in JavaScript?** (Declaration, Expression).
- **What are arrays and objects?** How do you access their elements/properties?
- **What are common array methods?** (e.g., `push`, `pop`, `shift`, `unshift`, `forEach`, `map`, `filter`, `slice`, `splice`).
- **How do you add comments in JavaScript?** (single-line and multi-line).
- **What is the DOM?** How do you interact with it using JavaScript (selecting, creating, modifying elements)?
- **What are events and event handling in JavaScript?** (e.g., `click`, `mouseover`, `addEventListener`).
- **What is `JSON`?** How do you parse JSON (`JSON.parse()`) and stringify objects to JSON (`JSON.stringify()`)?
- How do you handle errors in JavaScript (try...catch)?
- What are JavaScript operators? (Arithmetic, assignment, comparison, logical, ternary).
- What does "short-circuiting" mean for logical operators (`&&`, `||`)?
- What are truthy and falsy values in JavaScript? List all falsy values.
- What is "Strict Mode" (`'use strict';`)? What are some of its benefits?
- What is the `typeof` operator? Common gotchas (e.g., `typeof null`)?

### JavaScript - Mid Level

- **Explain closures in JavaScript.** What are their use cases (data privacy, partial application, callbacks)? How can they lead to memory leaks?
- **What is `this` keyword in JavaScript?** Explain how its value is determined in different contexts (global, function call, method call, constructor, arrow functions, event handlers, `call`, `apply`, `bind`).
- **Explain prototypes and prototypal inheritance.** What is the prototype chain? How does `__proto__` (or `Object.getPrototypeOf()`) work?
- **What are ES6+ features you use regularly?** (e.g., arrow functions, template literals, destructuring, spread/rest operators, default parameters, modules, classes, Promises, `let`/`const`).
- **What are Promises?** Explain their states (`pending`, `fulfilled`, `rejected`). How do you create and use them (`.then()`, `.catch()`, `.finally()`)? How do they compare to callbacks? What is "Callback Hell"?
- **What is `async/await`?** How does it simplify asynchronous code and relate to Promises? How do you handle errors with `async/await` (`try...catch`)?
- **Explain event bubbling and event capturing (trickling).** What is event delegation? Why is it useful? How can you stop event propagation?
- **What is the Event Loop in JavaScript?** Explain its components (Call Stack, Web APIs/Browser APIs, Callback Queue/Task Queue, Microtask Queue). What's the difference between Microtask and Macrotask Queues?
- **What are higher-order functions?** Provide examples.
- **What are pure functions?** Characteristics and benefits?
- **Explain `map`, `filter`, `reduce` array methods in detail.**
- **What are JavaScript modules (ES6 modules)?** How do `import`/`export` work? Discuss static vs. dynamic imports.
- How do you perform deep vs. shallow copying of objects/arrays?
- What is an IIFE (Immediately Invoked Function Expression)? Use cases?
- What are arrow functions? Key differences from traditional functions (`this` binding, `arguments` object, `new` keyword, `prototype`).
- What is the `arguments` object? How does it differ from rest parameters (`...`)?
- What are common ways to iterate over an object's properties? (`for...in`, `Object.keys()`, `Object.values()`, `Object.entries()`).
- What is the difference between `innerHTML`, `innerText`, and `textContent`? Security implications of `innerHTML`?
- What is `localStorage` and `sessionStorage`? Differences, use cases, limits.
- What is optional chaining (`?.`) and the nullish coalescing operator (`??`)?

### JavaScript - Senior Level

- **Explain JavaScript's memory management (garbage collection).** High-level understanding of mark-and-sweep. Common causes of memory leaks and how to prevent them.
- **What are generators (`function*`) and iterators?** The iteration protocol (`Symbol.iterator`).
- **What are `WeakMap` and `WeakSet`?** How do they differ from `Map` and `Set`? Use cases?
- **Explain `Symbol` type and its use cases.** (Unique property keys, well-known symbols).
- **Discuss performance optimization techniques in JavaScript** (e.g., debouncing, throttling, memoization, minimizing DOM manipulation, efficient loops, code splitting, lazy loading).
- **What are Service Workers?** How do they enable PWAs (offline support, push notifications, background sync)?
- **What are Web Workers?** How do they enable concurrency? Limitations?
- **Explain common JavaScript design patterns** (e.g., Module, Singleton, Observer, Factory, Facade, Proxy, Decorator, Command).
- **How does JavaScript handle concurrency if it's single-threaded?** (Event loop, async operations).
- **What are Typed Arrays?** When might they be used?
- Discuss security considerations in JavaScript (XSS, CSRF prevention techniques on the client-side).
- How would you manage state in a complex vanilla JavaScript application?
- What is Functional Programming vs Object-Oriented Programming in JavaScript? Concepts like immutability, pure functions, HOFs, composition.
- Explain `Proxy` and `Reflect` objects. Use cases?
- What is function currying? Benefits?
- What is function composition?
- How do you implement private members in JavaScript classes (closures, naming conventions, WeakMaps, ES private class fields `#`)?
- What is `Object.freeze()`, `Object.seal()`, and `Object.preventExtensions()`?
- What is "tree shaking"? How do bundlers use it?
- What is "code splitting" and "lazy loading" for JS modules/components?
- Explain memoization. How to implement it?
- What is `BigInt`?

### JavaScript - Architect Level

- **Discuss strategies for building large-scale, maintainable JavaScript applications.** (Modular design, design patterns, state management strategies, microfrontends).
- **How would you design an API for a JavaScript library or framework?** (Considerations for usability, extensibility, performance).
- **Explain the trade-offs of different module systems (ESM, CommonJS, AMD, UMD)** in various environments.
- **Discuss the role of JavaScript engines (like V8) and their optimization techniques** (JIT compilation, inline caching, hidden classes - conceptual).
- **How do you approach performance profiling and debugging in complex JavaScript applications?** (Browser DevTools, specific libraries).
- **What are the challenges and solutions for micro-frontend architectures using JavaScript?**
- Discuss JavaScript's impact on SEO and how to mitigate potential issues (e.g., for SPAs).
- How would you set up coding standards, linting, and type checking for a large JavaScript project?
- Discuss the implications of JavaScript fatigue and how to manage dependencies effectively.
- What are some advanced error handling and logging strategies for frontend applications?
- How does JavaScript interoperate with WebAssembly (Wasm)? What are the benefits?
- What is tail call optimization? Does JavaScript support it widely?

## Ⅴ. TypeScript (TS) 🔷

This section focuses on TypeScript's features, benefits, and how it enhances JavaScript development.

### TypeScript - Trainee/Junior Level

- **What is TypeScript?** Why use it over JavaScript? What are its main goals and benefits (improved code quality, maintainability, scalability, team collaboration)?
- **What are the basic types in TypeScript?** (e.g., `string`, `number`, `boolean`, `any`, `void`, `null`, `undefined`, `symbol`, `bigint`).
- **How do you define types for variables and function parameters/return values?** (Type annotation).
- **What are interfaces in TypeScript?** How are they used to define the shape of an object?
- **How are interfaces different from `type` aliases?** When would you choose one over the other (declaration merging, extensibility vs. primitives/unions/intersections)?
- **What are enums?** (Numeric, string).
- **What is `any` type and why should it be avoided?**
- How do you compile TypeScript to JavaScript (`tsc` command)?
- What is a `tsconfig.json` file? What is its primary role?
- What is type inference? When is it good to rely on it?
- What is the `unknown` type? How is it different from `any` and why is it safer?
- What is the `never` type? Use cases?
- What are array types (`Array<T>` vs `T[]`) and tuples?
- What are optional properties (`propertyName?: type`) and readonly properties (`readonly propertyName: type`)?

### TypeScript - Mid Level

- **Explain generics in TypeScript.** Provide a use case for generic functions, interfaces, or classes.
- **What are union types (`|`) and intersection types (`&`)?**
- **What are literal types?** (e.g., `'hello'`, `true`, `42`). What about template literal types?
- Explain type narrowing techniques (e.g., `typeof`, `instanceof`, `in` operator, discriminated unions, type guards).
- What are type guards (using `is TypeName`)?
- What are discriminated unions (tagged unions)? How do they enable powerful type narrowing?
- **What are access modifiers (`public`, `private`, `protected`) in TypeScript classes?**
- How do you work with `null` and `undefined` in TypeScript (strict null checks compiler option)?
- **What are type assertions (casting)?** (e.g., `as Type`, `<Type>value`). When are they useful and when are they risky?
- **What are mapped types?** Explain built-in utility types like `Partial<T>`, `Required<T>`, `Readonly<T>`, `Pick<T, K>`, `Omit<T, K>`, `Record<K, T>`.
- Explain how to type functions and their parameters, including function types.
- What are `const enum`s? How do they differ from regular enums?
- What is the `as const` assertion? Why is it useful?
- Explain some important `tsconfig.json` compiler options (`target`, `module`, `strict`, `noImplicitAny`, `esModuleInterop`, `sourceMap`, `outDir`, `baseUrl`, `paths`).
- How can classes implement interfaces (`implements` keyword)?

### TypeScript - Senior/Architect Level

- **What are conditional types?** (`T extends U ? X : Y`). Provide a use case. Explain the `infer` keyword.
- **What are decorators in TypeScript?** (Experimental feature). Types of decorators? Use cases?
- **Explain how to create custom utility types** by combining mapped types, conditional types, etc.
- **How do you manage complex types across a large codebase?** (e.g., declaration merging for interfaces, namespaces vs ES modules, project references).
- **How would you integrate TypeScript into an existing JavaScript project?** What are the strategies and challenges (e.g., `allowJs`, JSDoc type checking)?
- **Discuss advanced type manipulation techniques** (e.g., `infer` keyword, variadic tuple types, recursive types, template literal types for complex string patterns).
- How does TypeScript improve refactoring and maintainability at scale?
- **What are declaration files (`.d.ts`)?** How do you write them for third-party JavaScript libraries? What is DefinitelyTyped (`@types/*`)?
- How can TypeScript be used to enforce design patterns or architectural constraints (e.g., using branded types for nominal typing)?
- Discuss build performance considerations with TypeScript.
- How do you handle nominal typing vs structural typing in TypeScript?
- What are some limitations of TypeScript's type system?
- What is module resolution in TypeScript (`classic` vs. `node`)?
- What are ambient modules/declarations?
- How does TypeScript handle function overloads?
- How can you use TypeScript for type-safe APIs or libraries?
- What is "type-level programming" in TypeScript? (Advanced).

## Ⅵ. Data Structures & Algorithms (DSA) 📊

This section covers DSA concepts relevant to frontend development.

### DSA - General Concepts

- **What is Big O notation?** Why is it important for frontend developers (e.g., optimizing rendering, efficient state updates)?
- Explain common data structures and their relevance in frontend:
  - **Arrays** (and their dynamic nature in JS, common methods and their complexity).
  - **Objects** (as hash maps in JS, property access complexity).
  - **Linked Lists** (conceptual understanding, use cases like managing a queue of operations).
  - **Stacks & Queues** (conceptual understanding, use cases like event loop, undo/redo functionality, call stack).
  - **Trees** (especially the DOM tree, component trees in React, state structure).
  - **Graphs** (less common, but good to know basics for certain problems like routing or social connections).
  - **Sets** (for unique collections).
  - **Maps** (for key-value pairs, advantages over plain objects for map-like operations).
- Explain common algorithms:
  - **Sorting algorithms** (e.g., bubble sort, insertion sort, merge sort, quick sort - conceptual understanding of how they work and their complexity).
  - **Searching algorithms** (e.g., linear search, binary search - when to use binary search).
  - **Recursion** (definition, base cases, use in traversing tree-like structures like DOM or component hierarchies).
  - **Iteration** (vs. recursion for tree traversal).

### DSA - Frontend Specific Problems

- How would you efficiently render a large list of items? (Virtualization/Windowing, pagination).
- How to implement a `debounce` or `throttle` function? Explain use cases (e.g., search input, window resize).
- How to flatten a deeply nested array?
- How to find an element in the DOM or a component tree efficiently? (Traversal methods).
- Problems related to string manipulation (e.g., palindrome check, anagram check, finding most frequent character).
- Problems related to array manipulation (e.g., remove duplicates, merge sorted arrays, find missing number).
- Logic for UI components (e.g., a typeahead/autocomplete search, a carousel, pagination logic).
- Understanding how data structures are used in frameworks (e.g., React's reconciliation uses concepts related to tree traversal and diffing algorithms).
- How might you implement a simple client-side search/filter functionality on a list of items efficiently?
- When rendering a large, nested tree-like structure (e.g., a file explorer UI), what performance considerations related to data structures and algorithms might arise?
- How can you efficiently manage and update state that represents a collection of items (e.g., a list of todos, items in a cart), considering immutability?
- (Architect Level) Discuss algorithmic complexity when designing reusable components or core framework logic.
- (Architect Level) Discuss how you might implement a client-side cache with an LRU (Least Recently Used) eviction policy.

## Ⅶ. React ⚛️

This section is dedicated to React, covering core concepts, hooks, advanced patterns, and performance.

### React - Trainee/Junior Level

- **What is React?** What problems does it solve? Explain its primary purpose and philosophy (declarative, component-based).
- **What is JSX?** How does it differ from HTML? How does JSX get transpiled? Can you use React without JSX?
- **What is a React component?**
  - Differentiate between Functional Components and Class Components. Which is generally preferred now and why?
  - How do you create a simple component?
- **What are props?** How are they passed from parent to child? Are they mutable or immutable?
- **What is state in a React component?** How is it different from props? Is it mutable or immutable by convention?
- **How do you update state in a functional component (`useState`)?** Does `setState` update state synchronously or asynchronously? Explain batching.
- **How do you handle events in React?** (e.g., `onClick`, `onChange`). How are React events different from native DOM events (SyntheticEvent)?
- **What is conditional rendering?** Describe different ways to achieve it (e.g., `if/else`, ternary operator, logical `&&`, element variables).
- **How do you render lists of items in React?** What is the significance of the `key` prop in lists? What happens if you don't use keys, or use non-unique/index keys incorrectly?
- **What is the Virtual DOM (VDOM)?** How does it work? How does it help improve performance?
- What is `create-react-app` (CRA)? Why are tools like Vite often preferred now?
- **What are React Fragments (`<React.Fragment>` or `<>...</>`)?** Why are they useful?
- Explain the basic lifecycle of a class component (e.g., `constructor`, `render`, `componentDidMount`, `componentWillUnmount`). (Focus is shifting to hooks, but basics might be asked for legacy code understanding).
- How do you import/export components?
- What is an "element" in React vs. a "component"?
- What is "unidirectional data flow"?
- What is the `children` prop?

### React - Mid Level

- **Explain React Hooks in detail:** `useState`, `useEffect`, `useContext`.
- **What are the "Rules of Hooks"?** (Only call Hooks at the top level, only call Hooks from React functions). Why are these rules important?
- **Explain the `useEffect` hook.**
  - What are its common use cases (side effects, data fetching, subscriptions)?
  - What is the dependency array (`[]`, `[dep1, dep2]`, no array)? How does it control when the effect runs?
  - How do you perform cleanup in `useEffect`? When does the cleanup function run?
- **How do you fetch data in React components?** (Using `useEffect` and `useState`, or libraries).
- **What is Context API?** When would you use it? How do you create, provide, and consume context (`useContext`)?
- **What is prop drilling?** What are common ways to avoid it (Context API, state management libraries, component composition)?
- **What are controlled components vs. uncontrolled components in forms?** When would you use each?
- **What are Higher-Order Components (HOCs)?** What are their use cases? Potential downsides or alternatives (Hooks, Render Props)?
- **What are Render Props?** How do they work? Use cases for sharing code?
- **How do you optimize React performance?**
  - Using `React.memo()`, `useCallback()`, `useMemo()`. Explain each.
  - Virtualizing long lists.
  - Code-splitting with `React.lazy()` and Suspense.
- **Explain error boundaries.** How do they work? Can a functional component be an error boundary?
- **What are refs?** When and how to use them (`useRef()`, `createRef()`, `forwardRef()`)? Accessing DOM elements, storing mutable values.
- How does React handle forms? (Controlled components, form libraries).
- What are synthetic events in React?
- How do you style React components? (CSS, CSS Modules, Styled-components, Emotion, Tailwind CSS, etc.). Pros and cons of different approaches.
- Explain `useReducer()`. When might you prefer it over `useState`?
- What is `useLayoutEffect()`? How does it differ from `useEffect()`?
- What is "lifting state up"?
- Explain the process of "reconciliation" in React. What is the heuristic algorithm React uses (diffing algorithm)?
- What is `React.StrictMode`?

### React - Senior Level

- **Deep dive into reconciliation algorithm.** How does React decide when to re-render? What is the diffing strategy for elements of different types, DOM elements of the same type, and components of the same type? How do keys optimize this?
- **Explain advanced patterns with Hooks** (custom Hooks for reusable logic, complex state logic with `useReducer`). How do you create a custom Hook?
- **How do `useMemo` and `useCallback` work internally and when are they truly beneficial?** Discuss referential equality and its impact.
- **Discuss different state management strategies in React** (Context API vs Redux/Zustand/Jotai/Recoil, etc.). Pros and cons of each. When to choose which?
- How would you implement server-side rendering (SSR) or static site generation (SSG) with React (e.g., using Next.js or Remix)?
- **What are concurrent features in React** (e.g., `useTransition()`, `useDeferredValue()`)? How do they improve user experience by allowing interruptible rendering?
- How do you handle internationalization (i18n) and localization (l10n) in a React application?
- Discuss advanced component composition patterns (e.g., compound components).
- How do you manage large forms with complex validation in React? (Libraries like React Hook Form, Formik).
- Explain how React's event system works internally.
- **What are React Suspense and `React.lazy()` for code splitting?** How do they work together?
- What is Micro Frontends with React? Challenges and benefits.
- How would you structure a large React application for scalability and maintainability? (Folder structure, component organization).
- Accessibility (a11y) in React applications: managing focus, ARIA attributes in JSX, keyboard navigation for custom components.
- What are Portals in React? Use cases (modals, tooltips)?
- What is the React Fiber architecture? Main goals (incremental rendering, concurrency)? (High-level).
- (As of May 2025) What are React Server Components (RSCs)? How do they differ from Client Components and traditional SSR? Benefits and limitations? (`"use client"` directive).
- What is "hydration" in SSR/SSG? What can cause hydration errors?
- What is the difference between `React.createElement()` and `React.cloneElement()`?
- What is the `Profiler` API in React DevTools?

### React - Architect Level

- **Design a scalable and performant architecture for a complex React application.** Consider state management, routing, data fetching, component structure, and code organization.
- **Discuss the trade-offs of choosing different state management libraries (Redux, Zustand, Jotai, Recoil, Context API) for large-scale projects.** Factors to consider?
- **How would you establish and enforce coding standards, best practices, and component libraries (design systems) for a team of React developers?**
- **Evaluate the pros and cons of monorepo vs. polyrepo for React projects.**
- **Discuss strategies for migrating a legacy application (e.g., jQuery, Angular) to React.** Challenges and approaches?
- **How do you approach performance monitoring and optimization in a large, long-running React application?** Tools and techniques.
- **What are the challenges and solutions for building a reusable and maintainable Design System with React?**
- **Architecting for testability in React applications.** How to ensure components and logic are easily testable?
- How do you handle security concerns specific to React applications (e.g., XSS in JSX, `dangerouslySetInnerHTML`, securing API interactions)?
- Discuss the future direction of React and its ecosystem. How do you prepare your architecture for upcoming changes?
- How do you lead a team of React developers, mentor juniors, and make high-level technical decisions that impact the frontend stack?
- When would you choose _not_ to use React for a project? What are the alternatives and their trade-offs?
- How do React Server Components change the way you think about data fetching and application architecture?
- Discuss challenges and strategies for state management in applications using both Server and Client Components.

## Ⅷ. Next.js NEXT

This section covers Next.js, a popular React framework, focusing on its features like rendering strategies, routing, and data fetching.

### Next.js - Trainee/Junior Level

- **What is Next.js?** Why use it over Create React App or Vite with vanilla React? What are its key advantages?
- **What are the main features of Next.js?** (e.g., Rendering Strategies: SSR, SSG; File-system Routing, API Routes, Image Optimization, Code Splitting).
- **How does file-system routing work in Next.js?** (App Router vs. Pages Router basics).
- What is the difference between a page and a component in Next.js?
- **How do you create dynamic routes in Next.js?** (e.g., `[slug].js` or `app/blog/[slug]/page.js`).
- **What is the `next/link` component used for?** Why is it preferred over `<a>` for internal navigation?
- How do you fetch data for pages in Next.js? (Basic understanding of `getStaticProps`, `getServerSideProps` for Pages Router, or simple `async/await` in Server Components for App Router).
- **What are API routes in Next.js (Pages Router) / Route Handlers (App Router)?** What are they used for?
- How do you create a new Next.js application? (`create-next-app`).
- What is pre-rendering in Next.js?
- What is hydration?

### Next.js - Mid Level

- **Explain `getStaticProps`, `getStaticPaths`, and `getServerSideProps` in detail (Pages Router).** When to use each? What do they return? Explain `fallback` in `getStaticPaths`.
- **Data fetching in the App Router:**
  - How is data fetching done in Server Components (using `async/await`)?
  - How does caching work with `Workspace` requests in Server Components? How to control it (`cache: 'no-store'`, `revalidate`)?
  - What are Server Actions? How do they enable server-side code execution from Client Components?
  - How do you fetch data in Client Components (e.g., `useEffect`, SWR/TanStack Query)?
- **What is Incremental Static Regeneration (ISR)?** How is it achieved (e.g., `revalidate` option)?
- **How does Next.js handle image optimization (`next/image`)?** Benefits over `<img>` tag? Key props (`src`, `width`, `height`, `alt`, `fill`, `priority`).
- How do you set up environment variables in Next.js? Build-time vs. runtime? `NEXT_PUBLIC_`.
- What is the `_app.js` (or `_app.tsx`) file used for (Pages Router)?
- What is the `_document.js` (or `_document.tsx`) file used for (Pages Router)? How does it differ from `_app.js`?
- How do you implement client-side data fetching in Next.js (e.g., with SWR or TanStack Query)?
- How does Next.js handle internationalization (i18n)? (Built-in for Pages Router, libraries for App Router).
- **What are middleware in Next.js?** Use cases (authentication, redirects, A/B testing)? How to create them? `matcher` config. Edge Runtime.
- **Explain the App Router concepts:**
  - Layouts (`layout.js`), Pages (`page.js`), Loading UIs (`loading.js`), Error UIs (`error.js`).
  - Server Components vs. Client Components (`"use client"` directive). Capabilities and limitations.
  - Route Groups (`(folderName)`).
  - Route Handlers (`route.js`) for API endpoints.
- What is `next/font` for optimizing web fonts?
- What is `next/script` for optimizing third-party scripts? (`strategy` prop).
- How do redirects and rewrites work (`next.config.js`)?

### Next.js - Senior/Architect Level

- **Discuss advanced data fetching patterns in Next.js** (e.g., data revalidation on-demand with `revalidatePath`/`revalidateTag`, streaming with Suspense, combining Server Actions with client-side libraries).
- **How would you architect a large-scale application using Next.js?** (App Router structure, organizing Server/Client Components, layouts, API handlers, state management).
- **Explain the Next.js build process (`next build`) and deployment strategies** (Vercel, Netlify, AWS Amplify, self-hosting).
- **How do you optimize a Next.js application for performance (Core Web Vitals)?** Beyond built-ins, consider bundle analysis, dynamic imports (`next/dynamic`), memoization.
- **Discuss authentication and authorization strategies in Next.js applications** (Middleware, API routes, session management, third-party providers).
- How do you manage state in a complex Next.js application that uses different rendering strategies and Server/Client Components?
- **When would you choose Server Components vs. Client Components in the App Router?** Deep dive into trade-offs, data flow, and interaction patterns.
- How do you integrate Next.js with a headless CMS (Contentful, Strapi, Sanity)? Discuss preview mode (Draft Mode) and webhooks for ISR.
- Discuss strategies for caching in Next.js (data fetching cache, Route Segment Config, CDN caching, client-side caching).
- How do you handle A/B testing in a Next.js application? (Middleware, feature flags).
- Compare Next.js with other React frameworks (e.g., Remix). Strengths and weaknesses.
- How would you design a resilient and scalable backend using Next.js API routes/Route Handlers or by integrating with external backend services?
- What is the Edge Runtime for API Routes/Handlers and Middleware? Benefits and limitations.
- What is Turbopack? How is it intended to improve build performance?
- What is `generateStaticParams` for SSG with dynamic routes in App Router?
- What are Parallel Routes and Intercepting Routes in App Router? Use cases?
- Discuss advanced `next.config.js` configurations (custom Webpack, headers, PWA settings).

## Ⅸ. React Ecosystem & Libraries 📚

This section explores common libraries and tools used in conjunction with React.

### State Management (Redux, Zustand, Jotai, Recoil, etc.)

- **General:**
  - Why do we need state management libraries? When is local component state or Context API not enough?
  - What are the differences between local component state (`useState`, `useReducer`), Context API, and global state management libraries?
- **Redux (if experienced with):**
  - What are the core principles of Redux? (Single source of truth, State is read-only, Changes are made with pure functions/reducers).
  - Explain Actions, Reducers, Store, Dispatch, and the typical data flow.
  - What is middleware in Redux (e.g., `redux-thunk`, `redux-saga`)? Why is it used (e.g., handling asynchronous actions)?
  - How does `connect` HOC (legacy) or `useSelector`/`useDispatch` hooks work with React Redux?
  - What is immutability and why is it important in Redux? How do you update state immutably?
  - How do you structure your Redux store for a large application? (Ducks pattern, feature-based, Redux Toolkit's `createSlice`).
  - What are selectors? Why use them (e.g., `reselect` for memoized selectors)?
  - What is Redux Toolkit? How does it simplify Redux development?
- **Zustand/Jotai/Recoil/Valtio (if experienced with):**
  - How do these libraries differ from Redux in their approach to state management? What are their core concepts (e.g., atoms for Jotai/Recoil, store hooks for Zustand)?
  - What are the benefits of using Zustand/Jotai/Recoil? (e.g., simplicity, less boilerplate, atomic state, better performance in some cases due to more granular updates).
  - How do they handle asynchronous operations or side effects?
  - How do they compare in terms of bundle size, performance, and developer experience?

### Routing (React Router)

- How does React Router work to enable client-side routing in a Single Page Application (SPA)?
- What are the main components of React Router (v6+)? (`<BrowserRouter>`, `<Routes>`, `<Route>`, `<Link>`, `<NavLink>`, `<Outlet>`, `useNavigate`, `useParams`).
- How do you create nested routes and layouts using `<Outlet>`?
- How do you implement programmatic navigation (`useNavigate`)?
- How do you handle route parameters (`useParams`) for dynamic routes?
- How do you implement protected/private routes for authentication?
- What is the difference between `BrowserRouter` and `HashRouter`?
- How do you handle "Not Found" (404) pages with React Router?
- How does data loading often integrate with routing in meta-frameworks like Next.js or Remix (loaders, actions)?

### Data Fetching & Caching (Axios, Fetch API, SWR, React Query/TanStack Query)

- How do you make API calls in React applications? Compare native Fetch API with libraries like Axios (features, error handling, interceptors).
- What are the benefits of using server state libraries like SWR or TanStack Query (formerly React Query)?
  - Caching strategies (e.g., `stale-while-revalidate`).
  - Automatic refetching (on window focus, reconnect, interval).
  - Pagination and infinite scrolling support.
  - Optimistic updates.
  - Request deduplication.
  - Loading and error state management.
- How do these libraries differentiate between server state and client state?
- How do you handle mutations (POST, PUT, DELETE requests) and update cache with these libraries?
- Explain key concepts/configurations like query keys, mutation functions, `onSuccess`/`onError` callbacks.
- How can these libraries be used in a Next.js context (both Pages and App Router)?

### UI Libraries (Material UI, Ant Design, Chakra UI, Tailwind CSS with Headless UI)

- What are the pros and cons of using pre-built component libraries versus building custom components?
- How do you customize components from these libraries to fit a specific design?
- How do these libraries typically handle theming and design tokens?
- When would you choose to build custom components from scratch versus using a library?
- How does Tailwind CSS (a utility-first CSS framework) differ from traditional component libraries? How can it be used with headless UI components (like Headless UI, Radix UI) in React?
- What are considerations for accessibility when using UI component libraries?

### Form Handling (Formik, React Hook Form)

- What are the common challenges of handling forms in React (managing form state, validation, submission, error handling)?
- How do libraries like Formik or React Hook Form simplify form handling in React?
  - State management for form inputs.
  - Validation (schema-based with Yup/Zod or custom).
  - Handling form submission and asynchronous operations.
  - Managing errors and touched states.
- Compare controlled vs. uncontrolled component approaches within the context of these libraries. How do they optimize performance (e.g., React Hook Form's focus on minimizing re-renders)?
- How do you integrate these form libraries with UI component libraries?

## Ⅹ. Design Patterns & Refactoring 🏗️

This section explores software design patterns applicable to frontend and React, as well as code refactoring principles.

### Design Patterns

- **General:**
  - What are design patterns? Why are they useful in software development?
  - Can you name a few common JavaScript design patterns? (e.g., Module, Singleton, Observer/Pub-Sub, Factory, Facade, Proxy, Decorator, Command). Explain one or two.
  - How do design patterns help in creating maintainable, scalable, and reusable code?
- **React Specific:**
  - What are common React design patterns?
    - **Higher-Order Components (HOCs):** What are they? Use cases? Potential issues (prop collisions, wrapper hell)?
    - **Render Props:** How do they work? Use cases for sharing logic?
    - **Custom Hooks:** How are they a pattern for reusing stateful logic?
    - **Compound Components:** Explain the pattern and provide an example (e.g., a Tabs or Select component).
    - **Provider Pattern (Context API):** How is it used for dependency injection or global state?
    - **Container/Presentational Components (Smart/Dumb Components):** Though less emphasized with Hooks, what was the idea? How do Hooks blur this line?
  - How do Hooks change the way we use some traditional React patterns (e.g., replacing HOCs or Render Props in many cases)?
  - Discuss the pros and cons of different patterns for solving specific problems (e.g., sharing logic between components, managing complex state).
- **Architect Level:**
  - How do architectural patterns (e.g., MVC, MVVM, Flux/Redux, Micro Frontends, Atomic Design) influence frontend development and React architectures?
  - How do you choose appropriate design patterns for a given problem considering scalability, maintainability, team familiarity, and performance?
  - Discuss patterns for managing cross-cutting concerns (e.g., logging, error handling, internationalization) in a large React application.

### Refactoring

- What is code refactoring? Why is it important for the health of a codebase?
- When should you refactor code? What are common "code smells" that indicate a need for refactoring? (e.g., duplicated code, long methods/components, large classes, excessive comments, tight coupling).
- Describe some refactoring techniques you have used (e.g., Extract Method/Component, Introduce Parameter Object, Encapsulate Field, Rename Variable/Function).
- How do you refactor a large legacy codebase safely without introducing regressions? (Incremental changes, good test coverage).
- How does strong test coverage support and enable effective refactoring?
- How do you balance the need for refactoring with ongoing feature development and deadlines?
- (Architect Level) How do you lead a team effort in large-scale refactoring? What strategies and tools would you use? What metrics can be used to track progress and success of refactoring efforts?
- (Architect Level) Discuss refactoring towards specific architectural goals, such as improving modularity, testability, or performance.

## XI. Testing 🧪

This section covers the principles and practices of testing frontend applications, especially React applications.

### Testing - Trainee/Junior Level

- **Why is testing important in software development?** What are the benefits?
- **What are different types of tests?** Briefly explain Unit, Integration, and End-to-End (E2E) tests.
- **What is Jest?** What is it primarily used for in the React ecosystem? (Test runner, assertion library, mocking).
- **What is React Testing Library (RTL)?** What is its core philosophy ("The more your tests resemble the way your software is used, the more confidence they can give you.")? How does it encourage testing behavior over implementation details?
- How do you write a simple unit test for a React component using Jest and RTL? (Rendering the component, basic queries, simple assertions).
- What are "matchers" in Jest? Give examples (e.g., `toBe`, `toEqual`, `toBeTruthy`, `toHaveBeenCalled`).
- How do you select/query for elements in RTL? (e.g., `getByText`, `getByRole`, `getByLabelText`, `getByTestId`). Which queries are preferred and why (accessibility-focused queries)?
- What is a "test case" or "test suite"?

### Testing - Mid Level

- How do you test React components with props and state? (Passing props, checking rendered output based on state).
- **How do you mock functions and modules in Jest?** (`jest.fn()`, `jest.spyOn()`, `jest.mock()`). Why is mocking necessary?
- **How do you test asynchronous operations in React components** (e.g., data fetching)? (Using `async/await` with RTL's `waitFor`, `findBy*` queries).
- **How do you test custom Hooks?** (Using `@testing-library/react-hooks` or `@testing-library/react`'s `renderHook`).
- **What is code coverage?** How do you interpret it? Is 100% coverage always the goal? Why or why not?
- **How do you simulate user events** (e.g., clicks, input changes, form submissions) with RTL and `@testing-library/user-event`?
- What is the difference between `getBy*`, `queryBy*`, and `findBy*` queries in RTL? When to use each?
- How do you test components that use Context API or Redux? (Wrapping with providers, mocking context values or store state).
- **What are snapshot tests?** What are their pros and cons? When are they useful, and when might they be problematic?
- What are the characteristics of a good unit test? (FIRST: Fast, Isolated, Repeatable, Self-Validating, Timely/Thorough).
- How do you test error boundaries in React?
- How do you debug failing tests?

### Testing - Senior/Architect Level

- **How do you set up a comprehensive testing strategy for a large application?** (The testing pyramid: balancing unit, integration, and E2E tests).
- What are the differences between test runners like Jest, Mocha, Jasmine? Frameworks like Cypress, Playwright?
- **What is Cypress or Playwright?** When would you use them for E2E testing? What are the benefits and challenges of E2E tests?
- **How do you test for accessibility (a11y) automatically and manually?** (e.g., using `jest-axe` with RTL, browser extensions, screen reader testing).
- **How do you approach visual regression testing?** What tools can be used?
- **How do you integrate testing into a CI/CD pipeline?** What are the benefits?
- Discuss challenges and strategies for testing micro-frontends.
- How do you measure the effectiveness and ROI of your tests beyond simple code coverage? (e.g., defect detection rate, confidence in releases).
- What are some best practices for writing maintainable, reliable, and effective tests? (Avoiding brittle tests, clear assertions, good test descriptions).
- How do you decide what to test and what not to test? Prioritizing tests based on risk and impact.
- Discuss contract testing for microservices or between frontend and backend. Why is it useful?
- What is Test-Driven Development (TDD)? What are its benefits and drawbacks?
- What is Behavior-Driven Development (BDD)? How does it relate to testing?
- How do you test Next.js applications, considering different rendering strategies (SSG, SSR, ISR) and features like API Routes/Route Handlers or Middleware?
- How do you test Server Components and Client Components in Next.js App Router?

## XII. Tooling 🛠️

This section covers the essential tools used in modern frontend development.

- **Package Managers:**
  - What is `npm`? What is `yarn`? What is `pnpm`? What are the key differences and benefits?
  - What is a `package.json` file? What are its main sections (`dependencies`, `devDependencies`, `scripts`)?
  - What is `package-lock.json` or `yarn.lock`? Why are they important for reproducible builds?
  - What are semantic versioning (SemVer - `MAJOR.MINOR.PATCH`) and its implications for managing dependencies?
- **Module Bundlers (Webpack, Parcel, Rollup, esbuild, Vite):**
  - What is a JavaScript module bundler? Why is it needed in modern frontend development?
  - Explain the basic concepts of Webpack (entry, output, loaders, plugins, mode).
  - What is tree shaking? How does it help reduce bundle size?
  - What is code splitting? How does it improve initial load performance? How do bundlers enable it?
  - How does Vite differ from Webpack, especially during development (native ES modules, esbuild)?
  - What is the role of Rollup, Parcel, or esbuild in the ecosystem?
- **Transpilers (Babel):**
  - What is Babel? Why is it used in JavaScript and React projects (transpiling newer JS features, JSX)?
  - How does Babel work (core concepts: parsing, transforming, generating; presets, plugins)?
- **Linters & Formatters (ESLint, Prettier, Stylelint):**
  - What is linting? What is formatting? Why are they important for code quality, consistency, and preventing bugs?
  - How do you configure ESLint (e.g., rules, plugins, extends) and Prettier? How can they work together?
  - What is Stylelint for CSS?
- **Version Control (Git):**
  - Explain basic Git commands (`clone`, `add`, `commit`, `push`, `pull`, `branch`, `checkout`, `merge`, `rebase`, `status`, `log`, `stash`).
  - What is a Git branch? Why are branches useful in a team environment?
  - What is `git merge`? What are merge conflicts and how do you resolve them?
  - What is `git rebase`? How does it differ from merging? When might you prefer one over the other?
  - Explain common Git workflows (e.g., Feature Branching, Gitflow, GitHub Flow).
  - What is a `HEAD` in Git? What is a detached HEAD?
  - What is `.gitignore` file used for?
  - What are pull requests (PRs) or merge requests (MRs)?
- **Developer Tools (Browser & Framework-specific):**
  - How do you use browser developer tools effectively for debugging and profiling JavaScript, CSS, and network requests? (Elements, Console, Sources, Network, Performance, Application tabs).
  - What are React DevTools or similar tools for other frameworks? How do they help in debugging component hierarchy, state, and props?
  - What are source maps? Why are they useful for debugging transpiled code?
- **CI/CD (Continuous Integration/Continuous Deployment/Delivery):**
  - What is CI/CD? What are its benefits for frontend development (faster releases, better quality, automated testing and deployment)?
  - What tools have you used for CI/CD (e.g., Jenkins, GitLab CI, GitHub Actions, Vercel, Netlify)? (More relevant for mid/senior/architect).
- **Task Runners (Historically Gulp/Grunt, now often part of bundler scripts):**
  - What is a task runner? Are they still as relevant?
- **API Testing Tools (Postman, Insomnia):**
  - How might tools like Postman or Insomnia be used in a frontend workflow (testing API endpoints, checking responses)?

## XIII. Live Coding Questions 💻

This section lists common problem areas for live coding interviews, typically involving React and TypeScript.

### Example Problem Areas & Components

- **UI Component Implementation (Stateless & Stateful):**
  - **Typed Counter:** Props: `initialCount?: number`, `step?: number`. State: current count. Func: Increment, Decrement. Variations: Reset, min/max, input field.
  - **Typed Toggle/Switch:** Props: `isOn: boolean`, `onToggle: (newState: boolean) => void`, `label?: string`. Func: Clicking toggles state. Variations: Style like UI switch, disabled state.
  - **Character Counter Input:** Props: `maxLength: number`. Display: "X/Y characters". Variations: Visual feedback, prevent typing past max.
  - **Typed Tabs Component:** Props: `tabs: Array<{ id: string | number; title: string; content: React.ReactNode }>`. State: Active tab ID. Func: Clicking a tab displays its content. Variations: Active tab styling, keyboard navigation.
  - **Typed Star Rating:** Props: `count?: number`, `rating: number`, `onRatingChange?: (newRating: number) => void`. Func: Clicking a star sets rating. Variations: Hover effect, half-stars.
  - **Simple Image Carousel:** Props: `images: Array<{ src: string; alt: string }>`. State: Current image index. Func: Next/Previous buttons. Variations: Dot indicators, autoplay.
  - **Typed Progress Bar:** Props: `percentage: number`, `label?: string`. Func: Visually represents percentage. Variations: Animation, text display.
  - **Accessible Tooltip Component:** Props: `content: React.ReactNode`. Func: Wraps children, appears on hover/focus. A11y: Keyboard accessible, ARIA attributes.
  - **Breadcrumbs Component:** Props: `items: Array<{ label: string; href?: string }>`.
  - **Notification/Alert Component:** Props: `message: string`, `type: 'success' | 'error' | 'warning' | 'info'`, `onClose?: () => void`. Variations: Dismiss button, auto-dismiss.
  - **Build a Modal/Dialog:** Ensure accessibility (focus trapping, keyboard close).
  - **Implement a simple Accordion.**
- **State Management & Hooks (with TypeScript):**
  - **Typed Form with `useState` and Basic Validation:** Fields like name, email, age. Controlled inputs, submit handler, display inline errors.
  - **Data Fetching with `useEffect`, `useState`, Typed Responses:** Fetch from public API (e.g., JSONPlaceholder). Define interface/type for response. Handle loading/error states.
  - **`useContext` for Typed Global State:** E.g., User Profile (`{ id, username, theme }`). Provide, consume, update theme.
  - **`useReducer` for Complex State Management:** E.g., Typed Todo List (`{ id, text, completed }`). Define types for actions and reducer.
  - **Custom Hook: `useToggle(initialValue: boolean): [boolean, () => void]`**.
  - **Custom Hook: `useLocalStorage<T>(key: string, initialValue: T): [T, Setter<T>]`**. Handle `JSON.stringify/parse`.
  - **Custom Hook: `useDebounce<T>(value: T, delay: number): T`**.
  - **Custom Hook: `useFetch<T>(url: string, options?: RequestInit)`**. Generic, handles loading/error, provides `refetch`.
  - **Custom Hook: `useForm<T>(initialValues: T)`**. Basic generic form handling.
- **JavaScript/Algorithm Challenges (Frontend Flavored):**
  - Implement `throttle`.
  - Handle nested comments rendering.
  - Write a function to deeply compare two objects/arrays.
  - Implement a simple search/filter functionality on a list of data.
  - Flatten an array of objects.
  - Client-side data transformation for rendering.
- **CSS Challenges:**
  - Recreate a simple layout (e.g., a card, a header).
  - Center an element in various ways.
  - Implement a responsive grid.
- **React Specific:**
  - Refactor a class component to a functional component with Hooks.
  - Manage state for a small application.
  - Pass data between components (parent-child, child-parent, sibling-sibling).

### Tips for Live Coding

- **Think Aloud:** Explain your approach and thought process. This is often more important than the perfect solution.
- **Ask Clarifying Questions:** Make sure you understand the requirements and constraints before diving in.
- **Start Simple:** Get a basic version working, then iterate and add complexity or features.
- **Write Clean Code:** Pay attention to variable naming, function/component structure, and overall readability.
- **Test Your Code:** Even simple manual tests in the browser or `console.log` statements can help verify functionality.
- **Handle Edge Cases (if time allows or prompted):** Think about what could go wrong or how the component might be misused.
- **Communicate:** If you get stuck, explain what you're trying to do and where you're facing difficulty. The interviewer might offer a hint.
- **TypeScript Specific:** Define types for props, state, and function signatures. Use generics where appropriate. Avoid `any` if possible; use `unknown` as a safer alternative if needed temporarily.

## XIV. Behavioral & Situational Questions 🤔

These questions assess soft skills, problem-solving approach, teamwork, and experience.

- Tell me about a challenging project you worked on. What were the challenges, and how did you overcome them?
- Describe a time you had a conflict with a team member. How did you resolve it?
- How do you stay updated with new technologies and trends in frontend development?
- Tell me about a time you made a mistake or failed. What did you learn from it?
- How do you handle tight deadlines or pressure?
- How do you approach debugging a complex issue? Describe your thought process.
- What are your strengths and weaknesses as a developer? (Be honest, show self-awareness).
- Why are you interested in this role/company?
- Where do you see yourself in 5 years? / What are your career goals?
- How do you contribute to code reviews (both giving and receiving feedback)? What do you look for?
- Describe your experience working in an Agile/Scrum environment.
- How do you prioritize tasks when you have multiple commitments?
- How do you approach learning new technologies or frameworks?
- How do you collaborate with other developers, designers, and product managers in a team?
- How do you handle disagreements or differing opinions on technical decisions within a team?
- How do you communicate technical concepts to non-technical stakeholders?
- How do you estimate the time required for a task or feature?
- How do you ensure the quality of your code before submitting it?
- Imagine you're starting a new project. What questions would you ask to understand the requirements better?
- How do you contribute to a positive and productive team environment?
- (Senior/Architect) Tell me about a time you had to make a difficult technical decision. What was your process?
- (Senior/Architect) How do you mentor junior developers?
- (Senior/Architect) Describe a time you introduced a new technology or process to your team. What was the outcome?

## XV. Architect Level Specific Questions 🏛️

Beyond senior-level questions, architect roles focus more on high-level design, strategy, leadership, and broad impact.

- How do you design a frontend system for scalability, reliability, and maintainability? What are key architectural considerations?
- Discuss your experience with micro-frontend architectures: pros, cons, common patterns, and implementation strategies. How do you handle communication and state sharing between micro-frontends?
- How do you evaluate and choose new technologies, frameworks, or libraries for a project or an organization? What criteria do you use?
- Describe your approach to establishing a technical vision and roadmap for a frontend team or product. How do you align it with business goals?
- How do you ensure consistency (UI/UX, code quality, best practices) and quality across multiple frontend teams or projects within an organization? (Design systems, shared libraries, governance, automation).
- Discuss strategies for managing and reducing technical debt in a large and evolving codebase. How do you prioritize it?
- How do you foster a culture of innovation, learning, and continuous improvement within a development team?
- How do you balance business requirements, user experience goals, and technical constraints/feasibility when making architectural decisions?
- What is your experience with leading and mentoring other senior engineers or tech leads? How do you help them grow?
- How do you measure the success or impact of frontend architectural changes or initiatives? What metrics are important?
- Discuss the role of a frontend architect in cross-functional teams and collaboration with backend architects, DevOps, product management, and UX design.
- How do you approach building, evolving, and governing a Design System at scale for a large organization?
- What are the key architectural considerations for internationalizing (i18n) and localizing (l10n) a complex global application?
- How do you ensure long-term platform stability and maintainability while also allowing for innovation and adoption of new technologies?
- Discuss your approach to API design from a frontend perspective – what makes a good API for frontend consumption (e.g., RESTful vs. GraphQL considerations, payload structure, error handling)?
- How do you approach non-functional requirements like security, performance, and accessibility from an architectural standpoint?
- What are your thoughts on build vs. buy decisions for core frontend infrastructure or tooling?
- How do you manage dependencies and their potential risks (security, compatibility, obsolescence) at an architectural level?
- Describe your process for conducting architectural reviews and providing constructive feedback.
