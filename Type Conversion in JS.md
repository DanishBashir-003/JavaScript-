---

# Boxing and Autoboxing in JavaScript

In JavaScript, primitives like numbers, strings, booleans, null, and undefined are not objects and do not have methods in the same way objects do. However, JavaScript has a feature called **"boxing"** or **"autoboxing"** that temporarily wraps these primitives in their corresponding object types so that methods can be called on them.

Here's how it works:

1. **Primitive Value**:
   - You have a primitive value like a number or a string.

2. **Temporary Wrapper Object**:
   - When you try to call a method on a primitive, JavaScript automatically wraps it in a temporary object of the appropriate type (Number, String, Boolean).

3. **Method Call**:
   - The method is called on this temporary object.

4. **Discard Wrapper**:
   - After the method call, the temporary object is discarded, and the primitive value remains unchanged.

## Example: Converting a Number to a String

In your example, let's convert a number primitive to a string using the `toString()` method:

```javascript
//--|| Change number to a string ||--
let amount = 100;  // This is a number primitive
amount = amount.toString();  // JavaScript temporarily wraps the number in a Number object and calls toString()
console.log(amount, typeof amount);  // Output: "100" "string"
```

Here's the step-by-step explanation:

1. `let amount = 100;` initializes `amount` as a number primitive.
2. `amount.toString();` invokes the `toString` method on `amount`. JavaScript temporarily creates a `Number` object that wraps the value `100` and calls the `toString` method on this `Number` object.
3. The `toString` method returns the string representation of the number, which is `"100"`.
4. `amount` is then assigned this string value.
5. `console.log(amount, typeof amount);` logs the value and type of `amount`, which are `"100"` and `"string"`, respectively.

This mechanism allows primitive values to behave like objects when necessary, enabling a more flexible and powerful use of methods in JavaScript.

