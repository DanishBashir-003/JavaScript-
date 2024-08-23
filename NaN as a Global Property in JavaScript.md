---

### NaN as a Global Property

NaN is a global property in JavaScript, which means it is automatically available throughout your code without needing to be explicitly declared. This global availability is due to its association with the global object. In web browsers, the global object is the `window` object. This means that properties and methods that belong to the global object, like NaN, can be accessed directly from `window`, and by extension, from anywhere in your script.

**What is a Global Object?**
The global object in JavaScript is a special object that acts as the container for all globally accessible properties and functions. In browsers, this global object is `window`, which means that when you declare a global variable or function, it becomes a property of the `window` object. For example, declaring `var x = 10;` in the global scope is equivalent to `window.x = 10;`.

**Why is the Global Object the `window` in Browsers?**
In browsers, the `window` object represents the window containing the DOM document, and it serves as the global object. This setup allows all scripts running on the web page to access global variables and functions via the `window` object. For example, `window.NaN` is the same as just typing `NaN` in the console.

**Immutable Nature of NaN**
NaN is immutable, meaning that its value cannot be altered. This immutability ensures that NaN behaves consistently across different contexts, making it a reliable indicator of an invalid number.

```javascript
window.NaN = 123;
console.log(NaN); // Output: NaN
```

**Explanation:** In this example, even though we attempt to assign a new value to `NaN` by setting `window.NaN = 123;`, the output remains `NaN`. This immutability is beneficial because it guarantees that NaN will always signify an invalid number, regardless of the context in which it’s used.

**Why Signal an Invalid Number?**
In JavaScript, signaling an invalid number using NaN is important for error detection and debugging. When performing calculations or processing data, encountering NaN can alert developers that an operation failed or that the input was invalid. This allows them to handle errors more effectively, preventing potential issues from propagating through the code.

For example, if a function is expected to return a numerical value but instead returns NaN, this can be used as a flag to indicate that something went wrong in the computation. The developer can then implement logic to handle this scenario, such as providing a fallback value or logging an error message.

---
