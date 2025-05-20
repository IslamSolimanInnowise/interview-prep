# 💻 Exhaustive React & TypeScript Live Coding Interview Questions (All Levels - May 2025)

This list provides a wide range of live coding problems typically encountered in React (with TypeScript) frontend developer interviews, from junior to senior levels. The complexity can be scaled by adding constraints, TypeScript requirements, or follow-up features.

**Key things interviewers look for:**

- **Problem Understanding & Clarification:** Asking relevant questions.
- **Approach & Planning:** Articulating a plan before and during coding.
- **React Fundamentals:** Correct use of components, props, state, hooks, JSX.
- **TypeScript Proficiency:** Defining types/interfaces for props, state, function signatures, event handlers; using generics where appropriate.
- **JavaScript/ESNext Proficiency:** Efficient use of modern JS features.
- **Code Quality & Patterns:** Readability, maintainability, reusability, error handling, consistency.
- **Debugging Skills:** Identifying and fixing issues efficiently.
- **Communication:** Explaining your thought process clearly.
- **Testing (Conceptual):** Discussing how the component/hook would be tested.
- **Accessibility (A11y) & Performance:** Considering these aspects.
- **Handling Edge Cases:** Identifying and addressing potential edge cases.

## 🧩 Category 1: UI Component Building (Stateless & Stateful)

Focuses on creating presentational and simple stateful UI elements, with TypeScript for props and state.

1.  **Typed Counter:**

    - **Task:** Build a Counter component.
    - **Props (TS):** `initialCount?: number`, `step?: number`.
    - **State (TS):** Current count (`number`).
    - **Functionality:** Increment, Decrement buttons.
    - **Variations:** Reset button, prevent count below a `min` prop or above a `max` prop. Input field to set the count.

2.  **Typed Toggle/Switch:**

    - **Task:** Create a reusable Toggle/Switch component.
    - **Props (TS):** `isOn: boolean`, `onToggle: (newState: boolean) => void`, `label?: string`.
    - **Functionality:** Clicking toggles its state and calls `onToggle`.
    - **Variations:** Style it like a common UI switch. Add disabled state.

3.  **Character Counter Input with Max Length:**

    - **Task:** An input field with character counting.
    - **Props (TS):** `maxLength: number`, `onChange?: (text: string) => void`, `initialValue?: string`.
    - **State (TS):** Current input value (`string`).
    - **Display:** "X/Y characters" (e.g., "75/140").
    - **Variations:** Visual feedback when approaching/exceeding `maxLength`. Prevent typing past `maxLength`.

4.  **Typed Tabs Component:**

    - **Task:** A basic tab interface.
    - **Props (TS):** `tabs: Array<{ id: string | number; title: string; content: React.ReactNode }>`, `defaultTabId?: string | number`.
    - **State (TS):** Active tab ID.
    - **Functionality:** Clicking a tab displays its content.
    - **Variations:** Style active tab. Basic keyboard navigation (arrow keys to switch tabs). Allow tab content to be components.

5.  **Typed Star Rating:**

    - **Task:** A star rating component.
    - **Props (TS):** `count?: number` (default 5), `rating: number`, `onRatingChange?: (newRating: number) => void`, `readOnly?: boolean`, `starColor?: string`.
    - **Functionality:** Clicking a star sets the rating. Visual feedback for filled/empty stars.
    - **Variations:** Hover effect to preview rating. Half-star ratings. Different icon for stars.

6.  **Simple Image Carousel:**

    - **Task:** Display images with Next/Previous buttons.
    - **Props (TS):** `images: Array<{ src: string; alt: string }>`.
    - **State (TS):** Current image index.
    - **Variations:** Dot indicators, autoplay, looping, captions.

7.  **Typed Progress Bar:**

    - **Task:** A progress bar.
    - **Props (TS):** `percentage: number` (0-100), `label?: string`, `color?: string`.
    - **Functionality:** Visually represents the percentage.
    - **Variations:** Animated progress change, display percentage text.

8.  **Accessible Tooltip Component:**

    - **Task:** A tooltip that appears on hover/focus.
    - **Props (TS):** `content: React.ReactNode`, `position?: 'top' | 'bottom' | 'left' | 'right'`.
    - **Functionality:** Wraps a `children` element.
    - **Accessibility:** Ensure it's keyboard accessible and screen reader friendly (ARIA attributes).

9.  **Breadcrumbs Component:**

    - **Task:** Display a breadcrumb trail.
    - **Props (TS):** `items: Array<{ label: string; href?: string }>`.
    - **Functionality:** Renders a list of links, with the last item typically not being a link.
    - **Variations:** Customizable separator.

10. **Notification/Alert Component:**
    - **Task:** Display different types of notifications (success, error, warning, info).
    - **Props (TS):** `message: string`, `type: 'success' | 'error' | 'warning' | 'info'`, `onClose?: () => void`, `autoDismissDelay?: number`.
    - **Variations:** Dismiss button, auto-dismiss after a delay.

## ⚙️ Category 2: State Management & Hooks (with TypeScript)

Tests understanding and application of React Hooks with strong typing.

1.  **Typed Form with `useState` and Basic Validation:**

    - **Task:** A form with fields like `name: string`, `email: string`, `age: number`.
    - **State (TS):** An object `useState<{ name: string; email: string; age: number | '' }>`.
    - **Functionality:** Controlled inputs, submit handler, basic client-side validation (e.g., required, email format, age is a number). Display inline error messages.
    - **Type Safety:** Ensure event handlers and state updates are type-safe.

2.  **Data Fetching with `useEffect`, `useState`, and Typed Responses:**

    - **Task:** Fetch data from a public API (e.g., `https://jsonplaceholder.typicode.com/users`). Define an `interface` or `type` for the expected API response structure.
    - **State (TS):** `data: User[] | null`, `loading: boolean`, `error: Error | null`.
    - **Functionality:** Display data, loading indicator, or error message.
    - **Variations:** Refetch on button click. Fetch based on a prop ID, refetch if ID changes. Type the error object more specifically if possible.

3.  **`useContext` for Typed Global State (e.g., User Profile):**

    - **Task:** Create a context for user profile data (`{ id: number; username: string; theme: 'light' | 'dark' }`). Provide it. Consume it in a child component to display user info and apply theme styles. Create a function to update the theme via context.
    - **Type Safety:** Define types for context value and provider props.

4.  **`useReducer` for Complex State Management (e.g., Typed Todo List):**

    - **Task:** Manage a list of todos (`{ id: number; text: string; completed: boolean }`) using `useReducer`.
    - **Actions (TS):** Define types for actions like `ADD_TODO`, `TOGGLE_TODO`, `REMOVE_TODO` with appropriate payloads.
    - **Reducer (TS):** Ensure the reducer function is strongly typed.

5.  **Custom Hook: `useToggle(initialValue: boolean): [boolean, () => void]`:**

    - **Task:** Implement the `useToggle` hook with TypeScript.

6.  **Custom Hook: `useLocalStorage<T>(key: string, initialValue: T): [T, (value: T | ((val: T) => T)) => void]`:**

    - **Task:** Implement the generic `useLocalStorage` hook.
    - **Considerations:** Handle `JSON.stringify/parse` for non-string values. Handle cases where `localStorage` is unavailable.

7.  **Custom Hook: `useDebounce<T>(value: T, delay: number): T`:**

    - **Task:** Implement the generic `useDebounce` hook.

8.  **Custom Hook: `useFetch<T>(url: string, options?: RequestInit): { data: T | null; loading: boolean; error: Error | null; refetch: () => void }`:**

    - **Task:** Create a generic custom hook for data fetching.
    - **Functionality:** Handles loading, error states, and provides a `refetch` function.
    - **Type Safety:** Generic type `T` for the expected data response.

9.  **Custom Hook: `useForm<T extends Record<string, any>>(initialValues: T): { values: T; handleChange: (event: React.ChangeEvent<HTMLInputElement | HTMLTextAreaElement | HTMLSelectElement>) => void; handleSubmit: (onSubmit: (values: T) => void) => (event: React.FormEvent) => void; resetForm: () => void }`:**
    - **Task:** (Advanced) Create a generic custom hook for basic form handling.
    - **Functionality:** Manages form values, provides `handleChange`, `handleSubmit`, and `resetForm` utilities.

## 📝 Category 3: Typed Forms & User Input

More complex form scenarios with robust typing.

1.  **Multi-Step Form with Typed State & Validation:**

    - **Task:** A multi-step form where each step has its own fields and validation rules.
    - **State (TS):** Manage the overall form data object, current step.
    - **Validation (TS):** Use a library like Zod or Yup for schema-based validation, or implement custom validation functions with clear error types.
    - **Functionality:** Navigation between steps, summary page, final submission.

2.  **Dynamic Form Fields:**

    - **Task:** A form where users can dynamically add or remove sets of fields (e.g., adding multiple phone numbers or addresses).
    - **State (TS):** Manage an array of field group objects.
    - **Functionality:** Buttons to "Add another" and "Remove". Ensure unique keys for list rendering.

3.  **Form with Dependent Fields & Typed Logic:**
    - **Task:** A form where the options or visibility of one field depend on the value of another.
    - **Example:** If "Country" is "USA", show a "State" dropdown; if "Canada", show a "Province" dropdown.
    - **Type Safety:** Ensure the logic and types reflect these dependencies.

## 🌐 Category 4: API Interaction & Asynchronous Operations (with Types)

Robust data handling with TypeScript.

1.  **Paginated Data Table with Typed Data & API Calls:**

    - **Task:** Fetch paginated data from an API. Display it in a table. Implement "Next" and "Previous" page buttons.
    - **API Contract (TS):** Define types for the API response (e.g., `{ data: Item[]; totalPages: number; currentPage: number }`).
    - **State (TS):** Current page, items, loading, error.
    - **Variations:** Allow changing items per page.

2.  **Optimistic Updates with Typed Actions:**

    - **Task:** Implement a feature (e.g., liking a post) that involves an API call. Update the UI optimistically before the API call completes. Handle potential API errors by reverting the UI.
    - **Type Safety:** Type the request, response, and potential error states.

3.  **Real-time Data with WebSockets (Conceptual with Typed Messages):**
    - **Task:** (Often conceptual for live coding unless very simple) Outline how you would connect to a WebSocket server and handle incoming messages with defined types.
    - **Types (TS):** Define interfaces for different message types received from or sent to the WebSocket.
    - **State (TS):** Manage the connection status and received data.

## 📜 Category 5: Typed List Rendering & Manipulation

Efficient and type-safe rendering and interaction with lists.

1.  **Filterable and Sortable Table/List with Generic Types:**

    - **Task:** Create a reusable component that can render a list/table of generic items `T[]`. It should accept `filterFn?: (item: T, searchTerm: string) => boolean` and `sortConfig?: { key: keyof T; direction: 'asc' | 'desc' }`.
    - **Functionality:** Provide UI for search input and sort controls.

2.  **Virtualized List (Conceptual or Simplified with Types):**
    - **Task:** (Advanced) Discuss or implement a very simplified version of a virtualized list that renders only visible items from a large typed array `T[]`.
    - **Props (TS):** `items: T[]`, `itemHeight: number`, `renderItem: (item: T, style: React.CSSProperties) => React.ReactNode`.

## ✨ Category 6: Advanced UI Patterns & Custom Hooks (with TypeScript)

Complex components and reusable logic with strong typing.

1.  **Type-Safe Modal Component with Portals & Focus Trapping:**

    - **Task:** Build a reusable and accessible Modal.
    - **Props (TS):** `isOpen: boolean`, `onClose: () => void`, `title?: string`, `children: React.ReactNode`.
    - **Features:** Use React Portals, trap focus within the modal, close on Escape key.

2.  **`useQuery` or `useMutation` like Custom Hook (Simplified):**

    - **Task:** (Advanced) Create a simplified version of a data fetching/mutation hook similar to those in React Query or Apollo Client.
    - **Generics (TS):** Use generics for request parameters, response data, and error types.
    - **Features:** Manage loading, error, success states; caching (very basic); refetching.

3.  **Type-Safe Drag and Drop Reordering:**

    - **Task:** (Advanced) Implement reordering of items in a list using HTML Drag and Drop API, ensuring state updates are type-safe.
    - **State (TS):** Manage an array of typed items `T[]`.

4.  **Generic Table Component with Custom Renderers:**

    - **Task:** Create a highly reusable Table component.
    - **Props (TS):** `data: T[]`, `columns: Array<{ key: keyof T | string; header: string; render?: (item: T) => React.ReactNode }>`.
    - **Functionality:** Renders data based on columns. If `render` function is provided for a column, use it; otherwise, display `item[key]`.

5.  **Finite State Machine with `useReducer` and Discriminated Unions:**
    - **Task:** Model a simple finite state machine (e.g., data fetching states: `idle | loading | success | error`) using `useReducer`.
    - **Types (TS):** Use discriminated unions for states and actions to ensure type safety and exhaustive checks in the reducer.

## 🔧 Category 7: React with JavaScript/TypeScript Fundamentals

Problems testing core JS/TS skills within a React component structure.

1.  **Data Transformation for Rendering:**

    - **Task:** Given a complex, nested data structure (e.g., API response), write functions to transform it into a flatter or more suitable structure for rendering in React components. Ensure all transformations are type-safe.
    - **Example:** Grouping items by category, calculating derived values.

2.  **Implementing a Search Algorithm (Client-Side):**

    - **Task:** Implement a client-side search for a list of items. Discuss different approaches (e.g., simple `includes`, more advanced fuzzy search if prompted) and their performance implications. Type the search function and results.

3.  **Custom Event Emitter with Typed Events:**
    - **Task:** (Advanced) Implement a simple event emitter class or object in TypeScript that can be used within a React application (e.g., via context or a custom hook) to communicate between loosely coupled components.
    - **Types (TS):** Allow typed event names and payloads.

### General Tips for React/TypeScript Live Coding:

- **Setup:** If using an online editor, quickly set up basic types for props or state even for simple components. `React.FC<Props>` or typing function parameters directly.
- **Type Inference:** Leverage TypeScript's type inference but don't be afraid to add explicit types where it improves clarity or catches potential errors.
- **`any` as a Last Resort:** Try to avoid `any`. If you must use it temporarily, explain why and how you'd refine it later. `unknown` is often a safer choice.
- **Utility Types:** Demonstrate knowledge of common utility types like `Partial`, `Pick`, `Omit` if the situation calls for it.
- **Error Handling:** Think about `null` / `undefined` checks, especially when dealing with API data or optional props.
- **Readability:** Your types should make the code easier to understand, not harder.

This more exhaustive list, with a focus on TypeScript integration, should prepare you well for a wide array of React live coding challenges. Practice these by actually coding them out!
