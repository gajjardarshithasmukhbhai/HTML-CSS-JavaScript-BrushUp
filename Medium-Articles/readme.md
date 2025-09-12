# Top 30 JavaScript Interview Questions

**By Gourav Hammad**  
*August 4, 2025*

Wondering what the popular JavaScript Interview Questions which are asked in Frontend Interviews nowadays?

Well, don't worry. I have made this series to help you get all the JavaScript Interview Questions that are asked in 2025.

## Why is this Series important for your next JavaScript Interview?

I was asked these questions in my previous interviews, so I am sharing this with my personal experiences.

If you go through all these questions, you can easily crack your next JavaScript round for sure.

If you are a new user, then don't forget to check out my previous series, like Top 30 Frontend Interview Experiences, Top 30 ReactJS Interview Questions, which are already there in my publication (Frontend Army).

---

## Part 1: Questions 1-5

Let's begin with the first 5 questions for this Top 30 JavaScript Interview Questions series.

### 1. What are Preload, Reconnect, Prefetch, and Prerender?

**Answer:** These are resource hints that help the browser optimize loading behavior.

- **Preload**: Tells the browser to load a specific resource (like a font, image, or script) early during page load because it's important. It's useful for critical assets that are needed immediately.
```html
<link rel="preload" href="/main.css" as="style">
```

- **Reconnect**: Helps the browser establish early connections to another domain by pre-resolving DNS, opening TCP, or starting TLS. Commonly used for third-party APIs or CDNs.
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
```

- **Prefetch**: Lets the browser download a resource that might be needed for future navigation, but not right now. It's good for optimizing next-page loads.
```html
<link rel="prefetch" href="/dashboard.js">
```

- **Prerender**: Instructs the browser to render a page in the background so that when the user navigates to it, it appears instantly. This is more aggressive than prefetch.
```html
<link rel="prerender" href="/checkout">
```

Use these strategically. Overusing them can harm performance.

### 2. How can you do caching on a website?

**Answer:** Caching helps reduce redundant network requests and improve load times.

Here are some common techniques:

- **Browser Caching**: Controlled using headers like Cache-Control and ETag. This tells the browser how long it can keep a file before checking back with the server.
- **Service Workers**: Useful for caching assets and even API responses. Often used in Progressive Web Apps (PWAs).
- **CDN Caching**: Static assets (images, JS, CSS) can be cached at edge servers around the world to reduce latency.
- **Memory Caching**: You can store frequently used data in JavaScript variables or contexts like React state, but this is volatile and lost on refresh.
- **LocalStorage/IndexedDB**: Store data locally in the browser for offline use or to avoid refetching APIs repeatedly.

Headers example:
```
Cache-Control: public, max-age=86400
```

### 3. What are ETag, Cache-Control, and Document Fragment?

**Answer:** Following are the meanings of the above keywords.

- **ETag**: A response header that represents a specific version of a resource. When the browser sends a cached version of a resource, it uses If-None-Match with the ETag to ask the server whether it has changed. If not, the server sends back a 304 response.

- **Cache-Control**: Used to define caching policies for both browsers and CDNs. You can specify if a file should be cached, for how long, whether it's public or private, and more.

For Example:
```
Cache-Control: max-age=31536000, immutable
```

- **DocumentFragment**: A lightweight container for DOM nodes. It's not part of the main DOM tree, which makes it ideal for performance when appending multiple elements at once.

For Example:
```javascript
// Create a lightweight DocumentFragment to hold 
// elements temporarily in memory
const fragment = document.createDocumentFragment(); 

// Loop to create 1000 div elements
for (let i = 0; i < 1000; i++) {
  // Create a new <div> element
  const div = document.createElement('div');   

  // Set the text content of the div
  div.textContent = `Item ${i}`;   

  // Append the div to the fragment (not yet in the live DOM)
  fragment.appendChild(div); 
} 

// Append the fragment to the body in one go
// This avoids triggering layout/reflow 1000 times
// much better performance
document.body.appendChild(fragment);
```

### 4. How do you optimize assets? What is image compression? What's the difference between WebP, PNG, and JPG?

**Answer:** Asset optimization is about reducing file sizes and speeding up loading.

Some common practices:

- Minify CSS, JS, and HTML
- Use lazy loading for offscreen images
- Compress images
- Split large JS bundles and use code-splitting
- Serve assets via a CDN
- Use modern image formats like WebP or AVIF

**Image compression** reduces image file sizes with minimal quality loss.

- **Lossy compression**: Removes some image data to reduce size. Used in JPG, WebP.
- **Lossless compression**: Retains image data. Used in PNG, WebP (lossless mode).

#### Comparison Table

| Format | Best For | Compression | Transparency | Browser Support |
|--------|----------|-------------|--------------|-----------------|
| **JPG** | Photos, complex images | Lossy, smaller files | No | Universal |
| **PNG** | Graphics, logos, transparency needed | Lossless, larger files | Yes | Universal |
| **WebP** | Modern web, all purposes | Both lossy & lossless | Yes | Modern browsers |

When possible, serve responsive images using srcset and modern formats.

### 5. What is a Memory Leak?

**Answer:** A memory leak occurs when memory that is no longer needed is not released. Over time, these unreleased chunks accumulate, causing performance issues or even crashes.

In JavaScript, common causes include:

- Forgetting to clear setInterval or setTimeout
- Retaining references in closures unnecessarily
- Not removing event listeners on unmounted elements
- Detached DOM nodes that are still referenced in JS
- Overuse of global variables

To detect and fix memory leaks:

- Use Chrome DevTools (Memory tab) to take heap snapshots
- Check for increasing memory usage over time
- Use WeakMap or WeakSet for weak references if needed
- Always clean up after event listeners and timers

For Example:
```javascript
useEffect(() => {
  // Define the resize handler function
  const handler = () => {
    // Your custom logic goes here (e.g., updating layout or state)
  };

  // Attach the handler to the window resize event
  window.addEventListener('resize', handler);

  // Cleanup function to remove the event listener when component unmounts
  return () => {
    window.removeEventListener('resize', handler);
  };
}, []); 
// Empty dependency array ensures this effect runs only once on mount
```

Cleaning up like this ensures the handler doesn't linger after the component unmounts.

---

*This article will help prepare for JavaScript interviews in 2025. The questions are based on real interview experiences and cover important frontend development concepts.*

### 6. What is Event Delegation and how does it work?

**Answer:** Event delegation is a technique where you attach a single event listener to a parent element to handle events for multiple child elements, including dynamically added ones.

**How it works:**
- Uses event bubbling - events bubble up from child to parent elements
- One listener on parent handles events for all children
- Use `event.target` to identify which child element triggered the event

**Benefits:**
- Better performance (fewer event listeners)
- Works with dynamically added elements
- Less memory usage

Example:
```javascript
// Instead of adding listeners to each button
document.getElementById('parent').addEventListener('click', function(e) {
  if (e.target && e.target.classList.contains('button')) {
    console.log('Button clicked:', e.target.textContent);
  }
});
```

### 7. Explain the difference between `var`, `let`, and `const`.

**Answer:** These are different ways to declare variables in JavaScript with different scoping and behavior.

| Feature | `var` | `let` | `const` |
|---------|-------|-------|---------|
| **Scope** | Function or Global | Block | Block |
| **Hoisting** | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |
| **Re-declaration** | Allowed | Not allowed | Not allowed |
| **Re-assignment** | Allowed | Allowed | Not allowed |
| **Temporal Dead Zone** | No | Yes | Yes |

Examples:
```javascript
// var - function scoped, can be re-declared
var x = 1;
var x = 2; // OK
function test() {
  if (true) {
    var y = 3; // function scoped
  }
  console.log(y); // 3 - accessible outside block
}

// let - block scoped, cannot be re-declared
let a = 1;
// let a = 2; // Error: Identifier 'a' has already been declared
if (true) {
  let b = 3; // block scoped
}
// console.log(b); // Error: b is not defined

// const - block scoped, cannot be re-assigned
const c = 1;
// c = 2; // Error: Assignment to constant variable
const obj = { name: 'John' };
obj.name = 'Jane'; // OK - object properties can be modified
```

### 8. What are Promises and how do they work? Explain Promise chaining.

**Answer:** Promises are objects representing the eventual completion or failure of an asynchronous operation.

**Promise States:**
- **Pending**: Initial state
- **Fulfilled**: Operation completed successfully
- **Rejected**: Operation failed

**Basic Promise:**
```javascript
const promise = new Promise((resolve, reject) => {
  // Async operation
  setTimeout(() => {
    const success = Math.random() > 0.5;
    if (success) {
      resolve('Operation successful!');
    } else {
      reject('Operation failed!');
    }
  }, 1000);
});

promise
  .then(result => console.log(result))
  .catch(error => console.log(error));
```

**Promise Chaining:**
```javascript
fetch('/api/user/1')
  .then(response => response.json())
  .then(user => fetch(`/api/posts/${user.id}`))
  .then(response => response.json())
  .then(posts => {
    console.log('User posts:', posts);
    return posts.length;
  })
  .then(count => console.log(`Total posts: ${count}`))
  .catch(error => console.error('Error:', error));
```

**Promise.all() and Promise.race():**
```javascript
// Promise.all - waits for all promises
Promise.all([promise1, promise2, promise3])
  .then(results => console.log('All completed:', results));

// Promise.race - returns first completed promise
Promise.race([promise1, promise2, promise3])
  .then(result => console.log('First completed:', result));
```

### 9. What is the difference between `==` and `===` in JavaScript?

**Answer:** These are comparison operators with different behavior regarding type coercion.

**`==` (Loose Equality):**
- Performs type coercion before comparison
- Converts operands to the same type, then compares

**`===` (Strict Equality):**
- No type coercion
- Compares both value and type
- Recommended for most comparisons

**Examples:**
```javascript
// Loose equality (==) - performs type coercion
console.log(5 == '5');        // true (string '5' converted to number)
console.log(true == 1);       // true (boolean true converted to 1)
console.log(null == undefined); // true (special case)
console.log(0 == false);      // true (false converted to 0)
console.log('' == false);     // true (empty string converted to 0)

// Strict equality (===) - no type coercion
console.log(5 === '5');       // false (different types)
console.log(true === 1);      // false (different types)
console.log(null === undefined); // false (different types)
console.log(0 === false);     // false (different types)
console.log('' === false);    // false (different types)
```

**Type Coercion Rules for `==`:**
```javascript
// String to Number
console.log('123' == 123);    // true

// Boolean to Number
console.log(true == 1);       // true
console.log(false == 0);      // true

// Object to Primitive
console.log([1,2,3] == '1,2,3'); // true

// Special cases
console.log(NaN == NaN);      // false (even with ===)
console.log(+0 === -0);       // true
```

### 10. Explain Closures in JavaScript with examples.

**Answer:** A closure is a function that has access to variables from its outer (enclosing) scope even after the outer function has finished executing.

**How Closures Work:**
- Inner function maintains reference to outer function's variables
- Creates a private scope
- Variables remain in memory due to closure reference

**Basic Example:**
```javascript
function outerFunction(x) {
  // Outer function's variable
  let outerVariable = x;
  
  // Inner function (closure)
  function innerFunction(y) {
    // Can access both outer and inner variables
    return outerVariable + y;
  }
  
  return innerFunction;
}

const addFive = outerFunction(5);
console.log(addFive(3)); // 8 - still has access to outerVariable
```

**Practical Examples:**

**1. Data Privacy:**
```javascript
function createCounter() {
  let count = 0; // Private variable
  
  return {
    increment: () => ++count,
    decrement: () => --count,
    getCount: () => count
  };
}

const counter = createCounter();
console.log(counter.increment()); // 1
console.log(counter.increment()); // 2
console.log(counter.getCount());  // 2
// console.log(counter.count);    // undefined - private!
```

**2. Function Factories:**
```javascript
function multiplyBy(multiplier) {
  return function(number) {
    return number * multiplier;
  };
}

const double = multiplyBy(2);
const triple = multiplyBy(3);

console.log(double(5)); // 10
console.log(triple(5)); // 15
```

**3. Module Pattern:**
```javascript
const userModule = (function() {
  let users = []; // Private data
  
  return {
    addUser: function(user) {
      users.push(user);
    },
    getUsers: function() {
      return [...users]; // Return copy to prevent external modification
    },
    getUserCount: function() {
      return users.length;
    }
  };
})();

userModule.addUser({ name: 'John', age: 30 });
console.log(userModule.getUserCount()); // 1
```

**Common Closure Gotcha:**
```javascript
// Problem: All buttons alert "3"
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100); // 3, 3, 3
}

// Solution 1: Use let (block scope)
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100); // 0, 1, 2
}

// Solution 2: Use closure with IIFE
for (var i = 0; i < 3; i++) {
  (function(index) {
    setTimeout(() => console.log(index), 100); // 0, 1, 2
  })(i);
}
```

---

## Part 2: Questions 11-15
*Coming Soon...*

## Part 2: Questions 11-15
*Coming Soon...*

## Part 3: Questions 16-20
*Coming Soon...*

## Part 4: Questions 21-25
*Coming Soon...*

## Part 5: Questions 26-30
*Coming Soon...*