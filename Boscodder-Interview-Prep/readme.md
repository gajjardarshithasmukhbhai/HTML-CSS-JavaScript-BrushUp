# Front-End Interview Preparation for MAANG Companies

## Table of Contents
1. [HTML](#html)
2. [CSS](#css)
3. [JavaScript](#javascript)
4. [Frameworks and Libraries (React)](#frameworks-and-libraries-react)
5. [TypeScript](#typescript)
6. [Testing](#testing)
7. [Performance Optimization](#performance-optimization)
8. [Tools and Build Systems](#tools-and-build-systems)
9. [Version Control](#version-control)
10. [System Design](#system-design)
11. [Common Interview Questions](#common-interview-questions)
12. [Mock Interviews](#mock-interviews)
13. [Additional Resources](#additional-resources)

---

## HTML

### Semantic HTML
**Q: What are semantic elements in HTML, and why are they important?**

A: Semantic elements clearly describe their meaning in a human- and machine-readable way.

**Benefits:**
- Improved accessibility for screen readers
- Better SEO ranking
- Cleaner, more maintainable code
- Better browser support

**Common semantic tags:**
- `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`
- `<h1>-<h6>`, `<p>`, `<figure>`, `<figcaption>`

**Q: How do you make a web page accessible?**

A: 
- Use semantic HTML elements
- Provide alt text for images
- Ensure proper heading hierarchy
- Use ARIA labels and roles when needed
- Maintain good color contrast
- Ensure keyboard navigation works
- Use descriptive link text

**Q: What is the difference between `<div>` and `<section>`?**

A: 
- `<div>`: Generic container with no semantic meaning
- `<section>`: Represents a distinct section of content with thematic meaning

### HTML5 Features
**Q: What are some new HTML5 features?**

A:
- **Form elements:** `<datalist>`, `<output>`, `<progress>`
- **Multimedia:** `<audio>`, `<video>`, `<track>`
- **APIs:** Geolocation, Web Storage, Web Workers
- **Input types:** email, date, number, range, color

### Accessibility Best Practices
**Q: What are ARIA roles and when would you use them?**

A: ARIA (Accessible Rich Internet Applications) roles provide semantic information about elements to assistive technologies.

**Common ARIA attributes:**
- `role="button"` - for clickable elements that aren't buttons
- `aria-label` - provides accessible name
- `aria-hidden="true"` - hides decorative elements
- `aria-expanded` - indicates if collapsible element is open

---

## CSS

### CSS Fundamentals
**Q: Explain the CSS box model.**

A: The CSS box model describes how elements are rendered:
1. **Content** - actual content
2. **Padding** - space between content and border
3. **Border** - surrounds padding and content
4. **Margin** - space outside the border

**Q: How do you center an element horizontally and vertically in CSS?**

A: Multiple methods:

```css
/* Flexbox */
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Grid */
.container {
  display: grid;
  place-items: center;
}

/* Absolute positioning */
.element {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

### Flexbox
**Q: What are the differences between Flexbox and Grid?**

A:
- **Flexbox:** One-dimensional layout (row OR column)
  - Best for components and small-scale layouts
  - Content-first approach
  
- **Grid:** Two-dimensional layout (rows AND columns)
  - Best for page layouts
  - Layout-first approach

### Responsive Design
**Q: What is mobile-first design?**

A: Mobile-first is a design strategy where you start designing for mobile devices and progressively enhance for larger screens.

```css
/* Mobile first (default) */
.container { width: 100%; }

/* Tablet */
@media (min-width: 768px) {
  .container { width: 750px; }
}

/* Desktop */
@media (min-width: 1200px) {
  .container { width: 1170px; }
}
```

### CSS Preprocessors
**Q: What are the advantages of using CSS preprocessors like Sass?**

A:
- **Variables** for reusable values
- **Nesting** for better organization
- **Mixins** for reusable code blocks
- **Functions** for calculations
- **Imports** for modular stylesheets

---

## JavaScript

### ES6+ Features
**Q: Explain the difference between 'let', 'const', and 'var'.**

A:
- **var:** Function-scoped, hoisted, can be redeclared
- **let:** Block-scoped, hoisted but not initialized, cannot be redeclared
- **const:** Block-scoped, must be initialized, cannot be reassigned

**Q: What is a closure, and how does it work?**

A: A closure is a function that has access to variables in its outer scope even after the outer function returns.

```javascript
function outerFunction(x) {
  return function innerFunction(y) {
    return x + y; // Has access to 'x'
  };
}
const addFive = outerFunction(5);
console.log(addFive(3)); // 8
```

**Q: How does the event loop work in JavaScript?**

A: The event loop handles asynchronous operations:
1. **Call Stack** - executes synchronous code
2. **Web APIs** - handle async operations (setTimeout, DOM events)
3. **Task Queue** - holds callbacks from completed async operations
4. **Event Loop** - moves tasks from queue to call stack when stack is empty

### Asynchronous JavaScript
**Q: What's the difference between Promises and async/await?**

A:
```javascript
// Promise
fetch('/api/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));

// Async/await
async function fetchData() {
  try {
    const response = await fetch('/api/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
```

### DOM Manipulation
**Q: How do you select and modify DOM elements?**

A:
```javascript
// Selection
const element = document.getElementById('myId');
const elements = document.querySelectorAll('.myClass');

// Modification
element.textContent = 'New text';
element.classList.add('active');
element.style.color = 'red';

// Creation
const newDiv = document.createElement('div');
newDiv.textContent = 'Hello';
document.body.appendChild(newDiv);
```

### Prototypal Inheritance
**Q: Explain prototypal inheritance in JavaScript.**

A: JavaScript uses prototypal inheritance where objects can inherit directly from other objects.

```javascript
// Constructor function
function Person(name) {
  this.name = name;
}

Person.prototype.greet = function() {
  return `Hello, I'm ${this.name}`;
};

// ES6 Class (syntactic sugar)
class Person {
  constructor(name) {
    this.name = name;
  }
  
  greet() {
    return `Hello, I'm ${this.name}`;
  }
}
```

---

## Frameworks and Libraries (React)

### JSX and Virtual DOM
**Q: What is the virtual DOM, and how does it work in React?**

A: Virtual DOM is a JavaScript representation of the actual DOM. React uses it for:
1. **Performance** - batches updates and minimizes DOM manipulation
2. **Predictability** - makes UI updates more predictable
3. **Developer Experience** - enables declarative programming

**Process:**
1. State changes trigger re-render
2. New virtual DOM tree is created
3. Diffing algorithm compares old and new trees
4. Only changed elements are updated in real DOM

### State and Props
**Q: Explain the difference between state and props in React.**

A:
- **Props:** Read-only data passed from parent to child
- **State:** Mutable data managed within a component

```javascript
// Props
function Welcome({ name, age }) {
  return <h1>Hello, {name}! You are {age} years old.</h1>;
}

// State
function Counter() {
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

### Hooks
**Q: What are React Hooks and why are they useful?**

A: Hooks let you use state and lifecycle features in functional components.

**Common hooks:**
- `useState` - manages component state
- `useEffect` - handles side effects
- `useContext` - consumes context
- `useMemo` - memoizes expensive calculations
- `useCallback` - memoizes functions

```javascript
function UserProfile({ userId }) {
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);
  
  useEffect(() => {
    async function fetchUser() {
      const response = await fetch(`/api/users/${userId}`);
      const userData = await response.json();
      setUser(userData);
      setLoading(false);
    }
    
    fetchUser();
  }, [userId]);
  
  if (loading) return <div>Loading...</div>;
  
  return <div>Welcome, {user.name}!</div>;
}
```

### Redux
**Q: How does Redux help in managing state in large applications?**

A: Redux provides predictable state management through:
- **Single source of truth** - one store for entire app
- **State is read-only** - only changed through actions
- **Pure functions** - reducers specify how state changes

**Redux flow:**
1. Action is dispatched
2. Reducer processes action and returns new state
3. Store updates and notifies subscribers
4. Components re-render with new state

---

## TypeScript

### Introduction to TypeScript
**Q: What are the benefits of using TypeScript?**

A:
- **Type Safety** - catches errors at compile time
- **Better IDE Support** - autocomplete, refactoring
- **Self-documenting** - types serve as documentation
- **Easier Refactoring** - confident code changes
- **Better Team Collaboration** - clear interfaces

**Q: How do you define and use interfaces in TypeScript?**

A:
```typescript
interface User {
  id: number;
  name: string;
  email: string;
  isActive?: boolean; // Optional property
}

function createUser(userData: User): User {
  return {
    id: userData.id,
    name: userData.name,
    email: userData.email,
    isActive: userData.isActive ?? true
  };
}
```

### Advanced Types
**Q: Explain the concept of generics in TypeScript.**

A: Generics allow you to create reusable components that work with multiple types.

```typescript
// Generic function
function identity<T>(arg: T): T {
  return arg;
}

// Generic interface
interface ApiResponse<T> {
  data: T;
  status: number;
  message: string;
}

// Usage
const stringResponse: ApiResponse<string> = {
  data: "Hello",
  status: 200,
  message: "Success"
};
```

---

## Testing

### Unit Testing with Jest
**Q: What is the difference between unit testing and integration testing?**

A:
- **Unit Testing:** Tests individual components/functions in isolation
  - Fast execution
  - Easy to debug
  - Mock dependencies
  
- **Integration Testing:** Tests how multiple components work together
  - Tests real interactions
  - Slower but more realistic
  - Uses actual dependencies

**Q: How do you mock dependencies in Jest?**

A:
```javascript
// Mock a module
jest.mock('./userService');

// Mock implementation
const mockGetUser = jest.fn();
jest.mock('./userService', () => ({
  getUser: mockGetUser
}));

// Test
test('displays user name', async () => {
  mockGetUser.mockResolvedValue({ name: 'John Doe' });
  
  render(<UserProfile userId={1} />);
  
  expect(await screen.findByText('John Doe')).toBeInTheDocument();
});
```

### End-to-End Testing
**Q: Explain the benefits of end-to-end testing with Cypress.**

A:
- **Real browser testing** - tests actual user interactions
- **Time travel debugging** - see what happened at each step
- **Automatic waiting** - no need for manual waits
- **Real-time reloads** - see tests run as you write them

---

## Performance Optimization

### Critical Rendering Path
**Q: What is the critical rendering path, and why is it important?**

A: The sequence of steps browsers take to render a page:
1. **DOM Construction** - parse HTML into DOM tree
2. **CSSOM Construction** - parse CSS into CSSOM tree
3. **Render Tree** - combine DOM and CSSOM
4. **Layout** - calculate element positions
5. **Paint** - fill in pixels

**Optimizations:**
- Minimize render-blocking resources
- Inline critical CSS
- Defer non-critical JavaScript

### Lazy Loading
**Q: How does lazy loading improve performance?**

A: Lazy loading defers loading of non-critical resources until needed:
- **Reduced initial load time**
- **Lower bandwidth usage**
- **Better user experience**

```javascript
// Image lazy loading
<img src="placeholder.jpg" data-src="actual-image.jpg" loading="lazy" />

// Component lazy loading
const LazyComponent = React.lazy(() => import('./LazyComponent'));

function App() {
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <LazyComponent />
    </Suspense>
  );
}
```

### Code Splitting
**Q: Explain the benefits of code splitting.**

A: Code splitting breaks your bundle into smaller chunks:
- **Faster initial loads** - only load what's needed
- **Better caching** - unchanged chunks stay cached
- **Parallel downloads** - multiple chunks can load simultaneously

---

## Tools and Build Systems

### Webpack
**Q: How does Webpack help in building and bundling front-end applications?**

A: Webpack is a module bundler that:
- **Bundles modules** - combines multiple files into fewer bundles
- **Transforms code** - using loaders (Babel, TypeScript, CSS)
- **Optimizes output** - minification, tree shaking, code splitting
- **Development server** - hot module replacement

### Package Managers
**Q: What are the benefits of using Babel in a JavaScript project?**

A: Babel transpiles modern JavaScript to older versions:
- **Browser compatibility** - use latest features in older browsers
- **Future-proofing** - write code with upcoming features
- **Plugin ecosystem** - extend functionality with plugins

**Q: How do you configure ESLint and Prettier in a project?**

A:
```json
// .eslintrc.json
{
  "extends": ["eslint:recommended", "@typescript-eslint/recommended"],
  "rules": {
    "no-console": "warn",
    "prefer-const": "error"
  }
}

// .prettierrc
{
  "semi": true,
  "trailingComma": "es5",
  "singleQuote": true,
  "printWidth": 80
}
```

---

## Version Control

### Git Basics
**Q: How do you initialize a Git repository?**

A:
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <repository-url>
git push -u origin main
```

**Q: Explain the Gitflow workflow.**

A: Gitflow is a branching model with:
- **main/master** - production-ready code
- **develop** - integration branch for features
- **feature/** - new features
- **release/** - prepare for production release
- **hotfix/** - quick production fixes

**Q: What are the best practices for writing commit messages?**

A:
- Use imperative mood ("Add feature" not "Added feature")
- Keep first line under 50 characters
- Capitalize first letter
- No period at the end
- Use body to explain what and why

---

## System Design

### Basics of System Design
**Q: How would you design a scalable news feed system?**

A: Key components:
1. **User Service** - manage user data and relationships
2. **Content Service** - handle post creation and storage
3. **Feed Generation Service** - create personalized feeds
4. **Notification Service** - real-time updates
5. **CDN** - cache and deliver content globally
6. **Database** - user data, posts, relationships
7. **Cache** - frequently accessed data

**Architecture patterns:**
- Microservices for scalability
- Event-driven architecture for real-time updates
- Load balancers for traffic distribution

**Q: What are micro-frontends, and what are their advantages?**

A: Micro-frontends extend microservices to the frontend:

**Advantages:**
- **Team independence** - different teams can work on different parts
- **Technology diversity** - use different frameworks
- **Scalable development** - easier to scale teams
- **Deployment flexibility** - deploy parts independently

**Q: Explain the MVC pattern and its use in front-end development.**

A: Model-View-Controller separates concerns:
- **Model** - data and business logic
- **View** - user interface
- **Controller** - handles user input and coordinates model/view

---

## Common Interview Questions

### Coding Challenges
**Q: Write a function to reverse a linked list.**

A:
```javascript
function reverseLinkedList(head) {
  let prev = null;
  let current = head;
  
  while (current !== null) {
    const next = current.next;
    current.next = prev;
    prev = current;
    current = next;
  }
  
  return prev;
}
```

**Q: How would you optimize a web application for faster load times?**

A:
- **Minimize HTTP requests** - combine files, use sprites
- **Optimize images** - compress, use appropriate formats
- **Enable compression** - gzip/brotli
- **Use CDN** - serve static assets from edge locations
- **Minimize code** - remove unused CSS/JS
- **Lazy load** - defer non-critical resources
- **Cache strategies** - browser and server-side caching

### Behavioral Questions
**Q: Describe a time when you had to work under a tight deadline.**

A: Use STAR method (Situation, Task, Action, Result):
- **Situation:** Describe the context
- **Task:** Explain your responsibility
- **Action:** Detail what you did
- **Result:** Share the outcome and what you learned

---

## Additional MAANG-Specific Questions

### JavaScript Deep Dive
**Q: Explain hoisting in JavaScript.**

A: Hoisting moves variable and function declarations to the top of their scope:

```javascript
console.log(x); // undefined (not ReferenceError)
var x = 5;

// Equivalent to:
var x;
console.log(x);
x = 5;

// Function hoisting
sayHello(); // Works!
function sayHello() {
  console.log("Hello!");
}
```

**Q: What is the difference between `==` and `===`?**

A:
- `==` (loose equality) - performs type coercion
- `===` (strict equality) - no type coercion

```javascript
"5" == 5   // true (string converted to number)
"5" === 5  // false (different types)
```

**Q: Explain the `this` keyword in JavaScript.**

A: `this` refers to the object that is executing the current function:

```javascript
// In methods
const obj = {
  name: "John",
  greet() {
    console.log(this.name); // "John"
  }
};

// Arrow functions don't have their own `this`
const obj2 = {
  name: "Jane",
  greet: () => {
    console.log(this.name); // undefined (inherits from enclosing scope)
  }
};
```

### React Advanced
**Q: What are Higher-Order Components (HOCs)?**

A: Functions that take a component and return a new component with enhanced functionality:

```javascript
function withLoading(WrappedComponent) {
  return function WithLoadingComponent({ isLoading, ...props }) {
    if (isLoading) {
      return <div>Loading...</div>;
    }
    return <WrappedComponent {...props} />;
  };
}

const UserListWithLoading = withLoading(UserList);
```

**Q: Explain React's reconciliation algorithm.**

A: React's diffing algorithm optimizes re-renders:
1. **Element type comparison** - different types = complete rebuild
2. **Key comparison** - helps identify moved elements
3. **Props comparison** - only update changed props
4. **Component comparison** - same type = update instance

**Q: What is Context API and when should you use it?**

A: Context provides a way to pass data through component tree without props drilling:

```javascript
const ThemeContext = React.createContext();

function App() {
  return (
    <ThemeContext.Provider value="dark">
      <Header />
    </ThemeContext.Provider>
  );
}

function Header() {
  const theme = useContext(ThemeContext);
  return <h1 className={theme}>Welcome</h1>;
}
```

### Performance and Optimization
**Q: What are Web Vitals and why are they important?**

A: Web Vitals are essential metrics for user experience:
- **LCP (Largest Contentful Paint)** - loading performance
- **FID (First Input Delay)** - interactivity
- **CLS (Cumulative Layout Shift)** - visual stability

**Q: How do you implement memoization in React?**

A:
```javascript
// React.memo for components
const ExpensiveComponent = React.memo(({ data }) => {
  return <div>{/* expensive rendering */}</div>;
});

// useMemo for expensive calculations
function DataProcessor({ items }) {
  const processedData = useMemo(() => {
    return items.map(item => expensiveOperation(item));
  }, [items]);
  
  return <div>{processedData}</div>;
}

// useCallback for function memoization
function Parent() {
  const [count, setCount] = useState(0);
  
  const handleClick = useCallback(() => {
    setCount(c => c + 1);
  }, []);
  
  return <Child onClick={handleClick} />;
}
```

### Security
**Q: What are common security vulnerabilities in web applications?**

A:
- **XSS (Cross-Site Scripting)** - malicious scripts in user input
- **CSRF (Cross-Site Request Forgery)** - unauthorized actions
- **SQL Injection** - malicious database queries
- **Clickjacking** - invisible UI elements

**Prevention:**
- Sanitize user input
- Use HTTPS
- Implement CSP (Content Security Policy)
- Validate on both client and server

### Browser APIs
**Q: Explain the Fetch API and how it differs from XMLHttpRequest.**

A:
```javascript
// Fetch API - modern, promise-based
async function fetchUser(id) {
  try {
    const response = await fetch(`/api/users/${id}`);
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return await response.json();
  } catch (error) {
    console.error('Fetch error:', error);
  }
}

// XMLHttpRequest - older, callback-based
function fetchUserXHR(id, callback) {
  const xhr = new XMLHttpRequest();
  xhr.open('GET', `/api/users/${id}`);
  xhr.onreadystatechange = function() {
    if (xhr.readyState === 4 && xhr.status === 200) {
      callback(JSON.parse(xhr.responseText));
    }
  };
  xhr.send();
}
```

---

## Mock Interview Practice

### Tips for Success
1. **Stay Calm** - Take deep breaths and think through problems
2. **Ask Questions** - Clarify requirements before coding
3. **Think Aloud** - Explain your thought process
4. **Start Simple** - Build working solution first, then optimize
5. **Test Your Code** - Walk through edge cases

### Common Patterns
1. **Two Pointers** - for array problems
2. **Sliding Window** - for substring problems
3. **Hash Maps** - for counting/lookup problems
4. **Recursion/DP** - for optimization problems

### System Design Tips
1. **Clarify Requirements** - ask about scale, features, constraints
2. **High-Level Design** - start with major components
3. **Deep Dive** - discuss specific components in detail
4. **Scale** - address bottlenecks and scalability

---

## Study Resources

### Books
- "You Don't Know JS" by Kyle Simpson
- "JavaScript: The Good Parts" by Douglas Crockford
- "Eloquent JavaScript" by Marijn Haverbeke

### Online Platforms
- **LeetCode** - coding challenges
- **FreeCodeCamp** - comprehensive tutorials
- **MDN Web Docs** - authoritative web documentation

### Practice Platforms
- **Pramp** - mock interviews
- **InterviewBit** - coding practice
- **System Design Primer** - system design concepts

---

## MAANG+ Company-Specific Questions

### Top Interview Questions from Leading Tech Companies

#### JavaScript Closures
**Q: What is a closure in JavaScript? Provide an example.**

A: A closure is a feature where an inner function has access to the outer (enclosing) function's variables.

```javascript
function outerFunction(outerVariable) {
  return function innerFunction(innerVariable) {
    console.log('Outer Variable: ' + outerVariable);
    console.log('Inner Variable: ' + innerVariable);
  }
}

const newFunction = outerFunction('outside');
newFunction('inside');
```

#### Responsive Design Implementation
**Q: How would you implement a design that needs to be responsive across various devices?**

A: Utilize CSS media queries to apply different styles based on device characteristics like width, height, or orientation. Employ a fluid grid layout and use relative units (em, rem, %) instead of pixels to ensure elements scale proportionally.

```css
/* Mobile first approach */
.container { width: 100%; }

@media (min-width: 768px) {
  .container { width: 750px; }
}

@media (min-width: 1200px) {
  .container { width: 1170px; }
}
```

#### JavaScript Promises vs Async/Await
**Q: Explain the difference between .then() and async/await in handling asynchronous operations in JavaScript.**

A: `.then()` is used with promises for asynchronous operations, chaining multiple calls for sequential execution. `async/await` makes asynchronous code look synchronous and is syntactic sugar over Promises, improving readability and error handling.

```javascript
// Using .then()
fetch('/api/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));

// Using async/await
async function fetchData() {
  try {
    const response = await fetch('/api/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
```

#### React Component Lifecycle
**Q: Describe the lifecycle of a React component and how you would use it to fetch data.**

A: React components have several lifecycle methods: `constructor()`, `render()`, `componentDidMount()`, `shouldComponentUpdate()`, `componentDidUpdate()`, and `componentWillUnmount()`. To fetch data, use `componentDidMount()` for class components or `useEffect()` hook in functional components to perform side effects, including data fetching after the initial render.

```javascript
// Class component
class UserProfile extends React.Component {
  componentDidMount() {
    this.fetchUserData();
  }
  
  fetchUserData = async () => {
    const response = await fetch(`/api/users/${this.props.userId}`);
    const userData = await response.json();
    this.setState({ user: userData });
  }
}

// Functional component with hooks
function UserProfile({ userId }) {
  const [user, setUser] = useState(null);
  
  useEffect(() => {
    async function fetchUser() {
      const response = await fetch(`/api/users/${userId}`);
      const userData = await response.json();
      setUser(userData);
    }
    fetchUser();
  }, [userId]);
}
```

#### Cross-Origin Resource Sharing (CORS)
**Q: What is CORS and how do you handle it in web applications?**

A: CORS is a security feature that restricts web applications from making requests to a domain different from the one which served the web page. To handle it, configure the server to include CORS headers like `Access-Control-Allow-Origin` in the response, specifying which domains are allowed to access the resources.

```javascript
// Server-side (Express.js)
app.use((req, res, next) => {
  res.header('Access-Control-Allow-Origin', '*');
  res.header('Access-Control-Allow-Methods', 'GET, POST, PUT, DELETE');
  res.header('Access-Control-Allow-Headers', 'Content-Type, Authorization');
  next();
});
```

#### Front-End Performance Optimization
**Q: What strategies would you employ to optimize the performance of a web application?**

A: Optimization strategies include minimizing and compressing assets (CSS, JavaScript, images), implementing lazy loading for images and components, using CDN for static assets, optimizing CSS selectors, and leveraging browser caching.

- **Code splitting** - Load only necessary code
- **Image optimization** - Use WebP format, compress images
- **Minification** - Remove unnecessary characters from code
- **Gzip compression** - Compress assets during transfer
- **Service workers** - Cache resources for offline access

#### Single Page Application (SPA) SEO Challenges
**Q: What are the SEO challenges with SPAs and how can they be addressed?**

A: SPAs often struggle with SEO as content is dynamically loaded, making it hard for search engine crawlers to index. Solutions include server-side rendering (SSR), using the History API to update URLs for different views, and leveraging pre-rendering services or static site generators.

- **Server-side rendering (SSR)** - Render pages on server
- **Static site generation (SSG)** - Pre-build pages at build time
- **Meta tag management** - Dynamically update meta tags
- **Structured data** - Use JSON-LD for rich snippets

#### Event Delegation in JavaScript
**Q: Explain event delegation and its advantages.**

A: Event delegation is a technique where instead of adding an event listener to each similar child element, you add a single event listener to a parent element. It leverages the event bubbling phase to catch events from child elements. Advantages include reduced memory usage (fewer event listeners) and dynamically handling events from elements added after the initial page load.

```javascript
// Instead of adding listeners to each button
document.querySelectorAll('.button').forEach(btn => {
  btn.addEventListener('click', handleClick);
});

// Use event delegation
document.getElementById('container').addEventListener('click', (e) => {
  if (e.target.classList.contains('button')) {
    handleClick(e);
  }
});
```

### Amazon Interview Questions

**Q: How would you implement infinite scrolling?**

A: Use Intersection Observer API to detect when user reaches bottom of page, then fetch and append more data.

```javascript
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      loadMoreContent();
    }
  });
});

observer.observe(document.querySelector('#load-more-trigger'));
```

**Q: Explain the difference between localStorage and sessionStorage.**

A: 
- **localStorage:** Persists until explicitly cleared, larger storage capacity
- **sessionStorage:** Cleared when tab closes, session-specific data

### Google Interview Questions

**Q: How would you implement a search autocomplete feature?**

A: Use debouncing to limit API calls, cache results, and implement trie data structure for efficient prefix matching.

```javascript
function debounce(func, delay) {
  let timeoutId;
  return function (...args) {
    clearTimeout(timeoutId);
    timeoutId = setTimeout(() => func.apply(this, args), delay);
  };
}

const debouncedSearch = debounce(searchAPI, 300);
```

**Q: What is the difference between null and undefined?**

A:
- **undefined:** Variable declared but not assigned
- **null:** Intentional absence of value

### Microsoft Interview Questions

**Q: How do you handle state management in large React applications?**

A: Use Redux for global state, Context API for theme/auth, local state for component-specific data, and consider state machines for complex workflows.

**Q: Explain the concept of tree shaking.**

A: Tree shaking removes unused code from bundles during build process, reducing bundle size and improving performance.

### Meta (Facebook) Interview Questions

**Q: How would you implement a real-time chat feature?**

A: Use WebSockets for real-time communication, implement message queuing, handle connection states, and optimize for mobile networks.

```javascript
const socket = new WebSocket('wss://chat-server.com');

socket.onmessage = (event) => {
  const message = JSON.parse(event.data);
  displayMessage(message);
};

function sendMessage(text) {
  socket.send(JSON.stringify({ text, timestamp: Date.now() }));
}
```

**Q: What are React Portals and when would you use them?**

A: Portals render children into DOM nodes outside parent component hierarchy, useful for modals, tooltips, and overlays.

### Apple Interview Questions

**Q: How do you ensure cross-browser compatibility?**

A: Use feature detection, progressive enhancement, vendor prefixes, polyfills, and thorough testing across browsers.

**Q: Explain the box model and box-sizing property.**

A: Box model includes content, padding, border, margin. `box-sizing: border-box` includes padding and border in element's total width/height.

### Airbnb Interview Questions

**Q: How would you implement a date picker component?**

A: Create reusable component with keyboard navigation, accessibility features, localization support, and customizable styling.

**Q: What is the purpose of useCallback hook?**

A: `useCallback` memoizes functions to prevent unnecessary re-renders in child components.

### ByteDance/TikTok Interview Questions

**Q: How would you optimize video loading and playback?**

A: Use adaptive bitrate streaming, preload metadata, implement buffering strategies, and optimize for mobile networks.

**Q: Explain the concept of code splitting in React.**

A: Code splitting divides application into smaller chunks loaded on demand, improving initial load time.

### Atlassian Interview Questions

**Q: How do you implement drag and drop functionality?**

A: Use HTML5 Drag and Drop API or libraries like react-beautiful-dnd for complex interactions.

```javascript
function handleDragStart(e) {
  e.dataTransfer.setData('text/plain', e.target.id);
}

function handleDrop(e) {
  e.preventDefault();
  const data = e.dataTransfer.getData('text/plain');
  e.target.appendChild(document.getElementById(data));
}
```

### Uber Interview Questions

**Q: How would you implement a real-time location tracking system?**

A: Use Geolocation API, WebSockets for real-time updates, implement efficient data structures for location storage.

**Q: Explain the concept of Progressive Web Apps (PWAs).**

A: PWAs use modern web technologies to provide native app-like experiences with offline functionality, push notifications, and installability.

### Canva Interview Questions

**Q: How would you implement undo/redo functionality?**

A: Use command pattern with history stack to track state changes and enable reversible operations.

```javascript
class CommandHistory {
  constructor() {
    this.history = [];
    this.currentIndex = -1;
  }
  
  execute(command) {
    this.history = this.history.slice(0, this.currentIndex + 1);
    this.history.push(command);
    this.currentIndex++;
    command.execute();
  }
  
  undo() {
    if (this.currentIndex >= 0) {
      this.history[this.currentIndex].undo();
      this.currentIndex--;
    }
  }
}
```

### Dropbox Interview Questions

**Q: How would you implement file upload with progress tracking?**

A: Use FormData API with XMLHttpRequest or Fetch API to track upload progress and handle large files.

```javascript
function uploadFile(file) {
  const formData = new FormData();
  formData.append('file', file);
  
  const xhr = new XMLHttpRequest();
  
  xhr.upload.onprogress = (e) => {
    const progress = (e.loaded / e.total) * 100;
    updateProgressBar(progress);
  };
  
  xhr.open('POST', '/upload');
  xhr.send(formData);
}
```

### LinkedIn Interview Questions

**Q: How do you implement lazy loading for images?**

A: Use Intersection Observer API to load images when they enter viewport.

```javascript
const imageObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const img = entry.target;
      img.src = img.dataset.src;
      imageObserver.unobserve(img);
    }
  });
});

document.querySelectorAll('img[data-src]').forEach(img => {
  imageObserver.observe(img);
});
```

### Lyft Interview Questions

**Q: How would you implement a route optimization algorithm?**

A: Use algorithms like Dijkstra's for shortest path, consider real-time traffic data, and implement caching for frequently requested routes.

### Twitter Interview Questions

**Q: How do you implement an infinite scroll timeline?**

A: Use virtual scrolling for performance, implement intersection observer for loading triggers, and manage memory efficiently.

**Q: Explain the concept of Web Workers.**

A: Web Workers run JavaScript in background threads, enabling heavy computations without blocking main UI thread.

### Shopify Interview Questions

**Q: How would you implement a shopping cart feature?**

A: Use local storage for persistence, implement cart state management, handle price calculations, and sync with server.

```javascript
class ShoppingCart {
  constructor() {
    this.items = JSON.parse(localStorage.getItem('cart')) || [];
  }
  
  addItem(product) {
    const existingItem = this.items.find(item => item.id === product.id);
    if (existingItem) {
      existingItem.quantity += 1;
    } else {
      this.items.push({ ...product, quantity: 1 });
    }
    this.saveToStorage();
  }
  
  getTotalPrice() {
    return this.items.reduce((total, item) => total + (item.price * item.quantity), 0);
  }
  
  saveToStorage() {
    localStorage.setItem('cart', JSON.stringify(this.items));
  }
}
```

### Pinterest Interview Questions

**Q: How would you implement a masonry layout?**

A: Use CSS Grid or JavaScript libraries like Masonry.js to create Pinterest-style grid layouts.

```css
.masonry-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  grid-auto-rows: 10px;
  gap: 10px;
}

.masonry-item {
  grid-row-end: span var(--row-span);
}
```

### Additional Common Questions Across Companies

**Q: How do you handle memory leaks in JavaScript?**

A: Remove event listeners, clear timers, avoid global variables, use WeakMap/WeakSet, and profile memory usage.

**Q: What is the difference between shallow and deep copying?**

A: Shallow copy copies only top-level properties, deep copy recursively copies all nested objects.

```javascript
// Shallow copy
const shallow = { ...original };

// Deep copy
const deep = JSON.parse(JSON.stringify(original));
// Or use libraries like Lodash
const deep = _.cloneDeep(original);
```

**Q: How do you implement error boundaries in React?**

A: Use class components with componentDidCatch or static getDerivedStateFromError methods.

```javascript
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }
  
  static getDerivedStateFromError(error) {
    return { hasError: true };
  }
  
  componentDidCatch(error, errorInfo) {
    console.error('Error caught:', error, errorInfo);
  }
  
  render() {
    if (this.state.hasError) {
      return <h1>Something went wrong.</h1>;
    }
    return this.props.children;
  }
}
```

**Q: Explain the concept of Server-Side Rendering (SSR).**

A: SSR renders pages on server before sending to client, improving SEO and initial load performance.

**Q: How do you implement authentication in a single-page application?**

A: Use JWT tokens, implement token refresh logic, store tokens securely, and handle route protection.

```javascript
// Token management
class AuthService {
  static setToken(token) {
    localStorage.setItem('authToken', token);
  }
  
  static getToken() {
    return localStorage.getItem('authToken');
  }
  
  static isAuthenticated() {
    const token = this.getToken();
    return token && !this.isTokenExpired(token);
  }
  
  static logout() {
    localStorage.removeItem('authToken');
    window.location.href = '/login';
  }
}
```


## Final Tips

### Interview Preparation
- Practice coding problems daily
- Build projects to demonstrate skills
- Study system design fundamentals
- Practice explaining concepts clearly

### During the Interview
- Communicate clearly
- Ask clarifying questions
- Show your problem-solving process
- Be honest about what you don't know

### Post-Interview
- Send thank you notes
- Reflect on areas for improvement
- Continue learning and practicing

Remember: Consistency and practice are key to success in MAANG interviews!



