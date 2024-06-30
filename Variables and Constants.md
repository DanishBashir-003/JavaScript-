const variable is for values that are not going to be re-asigned.
let variable cannot be used before being initialized or else we get an error
<em>var</em> can be used even before we initilize it, we dont get the error but it remains 'undefined' due to hoisting. The more indepth understanding of this concept is as under:
In JavaScript, variable declarations using `var`, `let`, and `const` are hoisted, but they behave differently during the hoisting process. Let's break down what happens when your code runs:

### Hoisting Explained

1. **Hoisting** is a JavaScript mechanism where variable and function declarations are moved to the top of their containing scope during the compile phase.

2. For variables declared with `var`, the declaration is hoisted, but the initialization remains in place. This means the variable is initialized to `undefined` until the assignment is encountered in the code.

3. For variables declared with `let` and `const`, both the declaration and the initialization stay in place, but the variables are put in a "temporal dead zone" from the start of the block until the declaration is encountered.

### Code Analysis

Here's your code with comments explaining each step:

```javascript
let firstName = 'John';    // Declares and initializes firstName
let lastName = 'Doe';      // Declares and initializes lastName
console.log(firstName, lastName, age); // Tries to log firstName, lastName, and age

var age = 30;              // Declares and initializes age
console.log(age);          // Logs age
```

### Step-by-Step Execution

1. **Hoisting Phase:**

   The JavaScript engine hoists variable declarations to the top of their scope. After hoisting, your code conceptually looks like this:

   ```javascript
   var age;  // age is hoisted and initialized to undefined

   let firstName = 'John';
   let lastName = 'Doe';
   console.log(firstName, lastName, age); // At this point, age is undefined

   age = 30;  // age is assigned the value 30
   console.log(age);  // Logs 30
   ```

2. **Execution Phase:**

   - `let firstName = 'John';` - `firstName` is declared and initialized with 'John'.
   - `let lastName = 'Doe';` - `lastName` is declared and initialized with 'Doe'.
   - `console.log(firstName, lastName, age);` - At this point, `age` has been declared (due to hoisting) but not yet initialized, so it is `undefined`. Therefore, this logs `John Doe undefined`.
   - `age = 30;` - `age` is now assigned the value 30.
   - `console.log(age);` - This logs `30`.

### Key Points

- **`var` Hoisting:** `var` declarations are hoisted to the top of their scope and initialized with `undefined`. This is why `age` is `undefined` when it is first logged.
- **`let` and `const` Hoisting:** `let` and `const` declarations are hoisted but not initialized, resulting in a ReferenceError if accessed before initialization.

If `age` were declared with `let` instead of `var`, accessing it before initialization would throw a ReferenceError:

```javascript
let firstName = 'John';
let lastName = 'Doe';
console.log(firstName, lastName, age); // ReferenceError: Cannot access 'age' before initialization
let age = 30;
console.log(age);
```

In summary, the difference in behavior arises because `var` initializes the variable to `undefined` during hoisting, whereas `let` and `const` do not initialize the variable, leading to a ReferenceError if accessed before declaration.
