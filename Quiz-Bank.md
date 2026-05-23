# 🧪 JavaScript ES6+ Quizbank - Engine Mechanics, Functional Transformations & Modern Collections

## 🟦 SECTION 1 — Template Literals & Expression Evaluation

### Q1. Core Arithmetic Evaluation

What is output to the engine console?

```js
console.log(`Sum: ${10 - 3 + 2}`);

```

> **Answer:** `Sum: 9`
> **Explanation:** The evaluation context inside an execution token `${}` follows standard algebraic operator precedence. The resulting numeric primitive is cast to a string via implicit coercion before interpolation occurs.

### Q2. Type Operator Interception

What is output to the engine console?

```js
console.log(`Check: ${typeof 42}`);

```

> **Answer:** `Check: number`
> **Explanation:** The unary `typeof` operator evaluates its target operand first, returning a lower-case string representation (`"number"`). This result is then interpolated directly into the enclosing string.

### Q3. Evaluation Order & Concatenation Priorities

What is output to the engine console?

```js
console.log(`${"A" + "B"}C`);

```

> **Answer:** `ABC`
> **Explanation:** Expressions inside the interpolation token are computed during the initialization phase of the template literal. The strings `"A"` and `"B"` are concatenated to produce `"AB"`, which is then joined with the trailing literal character `"C"`.

### Q4. Implicit Coercion Matrix

What is output to the engine console?

```js
console.log(`Value: ${"10" / 2}`);

```

> **Answer:** `Value: 5`
> **Explanation:** While the `+` operator favors string concatenation, mathematical operators like subtraction (`-`), multiplication (`*`), and division (`/`) trigger implicit type coercion. The string primitive `"10"` is converted to a numeric primitive before the operation executes.

### Q5. Logical Short-Circuit Operations

What is output to the engine console?

```js
console.log(`Flag: ${false || "default"}`);

```

> **Answer:** `Flag: default`
> **Explanation:** The logical OR (`||`) operator checks operands from left to right and short-circuits at the first truthy value. Because `false` is inherently falsy, the evaluation passes the string literal `"default"` to the template literal string constructor.

### Q6. Boolean Math Transformations

What is output to the engine console?

```js
console.log(`Result: ${true + true}`);

```

> **Answer:** `Result: 2`
> **Explanation:** When coerced into a numeric context via arithmetic addition, the boolean primitive `true` resolves to `1` (while `false` resolves to `0`). The expression evaluates mathematically to $1 + 1 = 2$.

### Q7. Grammatical Boundaries of Interpolation Tokens

What structural categories of JavaScript code can safely reside within a template literal's `${}` syntax boundaries?

> **Answer:** Strictly expressions only.
> **Explanation:** The execution engine requires a value that can be evaluated and converted into a string. Imperative control-flow statements (such as `if...else` statements, loops like `for` or `while`, or variable declarations) do not evaluate to a value and will trigger a critical parsing error.

### Q8. Non-Primitive Binary Concatenation

What is output to the engine console?

```js
console.log(`Test: ${[1, 2] + [3, 4]}`);

```

> **Answer:** `Test: 1,23,4`
> **Explanation:** The arithmetic binary addition operator (`+`) forces objects to primitives by calling their internal `toString()` prototype method. The arrays resolve respectively to `"1,2"` and `"3,4"`. These are then concatenated directly, causing the `2` and `3` to merge without spaces or delimiters.

---

## 🟦 SECTION 2 — Arrow Functions, Closures & Lexical Scoping

### Q9. Implicit Single-Line Arrow Projections

What is output to the engine console?

```js
const f = () => 10;
console.log(f());

```

> **Answer:** `10`
> **Explanation:** Arrow functions configured without surrounding block curly braces `{}` feature an implicit return mechanism for their trailing expression.

### Q10. Statement Blocks vs. Implicit Returns

What is output to the engine console?

```js
const f = () => {
  10;
};
console.log(f());

```

> **Answer:** `undefined`
> **Explanation:** Introducing a structural block wrapper `{}` explicitly disables the arrow function's implicit return mechanism. Because the block lacks an explicit `return` keyword, the invocation evaluates to `undefined`.

### Q11. Implicit Object Literal Projections

What is output to the engine console?

```js
const f = () => ({ x: 1 });
console.log(f());

```

> **Answer:** `{ x: 1 }`
> **Explanation:** To return an object literal implicitly, it must be wrapped in grouping parentheses `()`. Without these parentheses, the engine interprets the object's curly braces as a structural block wrapper rather than a key-value data structure.

### Q12. Multi-tier Execution Context Bindings

What is output to the engine console?

```js
const obj = {
  value: 100,
  get: function () {
    return () => this.value;
  }
};

console.log(obj.get()());

```

> **Answer:** `100`
> **Explanation:** Arrow functions do not establish their own runtime execution context (`this`). Instead, they inherit `this` from their lexical scope. When `obj.get()` runs, its execution environment points to `obj`. The internal arrow function captures this context permanently, allowing it to read `obj.value` even when called globally.

### Q13. Semantic Behavior of `this` inside Arrow Syntax

How does the execution context pointer (`this`) operate inside an arrow function compared to standard function declarations?

> **Answer:** It uses lexical scoping rules instead of dynamic caller mapping.
> **Explanation:** Standard function declarations dynamically bind `this` based on how they are called. Arrow functions, on the other hand, inherit their `this` value directly from their parent scope at execution time. This means tools like `.bind()`, `.call()`, or `.apply()` cannot alter an arrow function's execution context.

### Q14. Dynamic Parameter Object Environments

What happens during the execution of this arrow expression block?

```js
const fn = () => arguments;
console.log(fn(1, 2, 3));

```

> **Answer:** `ReferenceError: arguments is not defined`
> **Explanation:** Arrow functions do not have access to the classic array-like `arguments` object. To capture an open-ended list of parameters within an arrow function, use modern ES6 rest syntax instead: `(...args) => args`.

### Q15. Nullish Coalescing Operators

What is output to the engine console?

```js
const f = (a, b) => a ?? b;
console.log(f(null, 5));

```

> **Answer:** `5`
> **Explanation:** The nullish coalescing operator (`??`) falls back to the right-hand operand only if the left-hand operand evaluates strictly to `null` or `undefined`. Unlike the logical OR (`||`) operator, it treats empty strings (`""`) and `0` as valid, defined values.

---

## 🟦 SECTION 3 — Default Initialization Parameters

### Q16. Parameter Dependency Evaluation

What is output to the engine console?

```js
function f(a = 1, b = a * 2) {
  return b;
}
console.log(f(3));

```

> **Answer:** `6`
> **Explanation:** Function parameters are evaluated sequentially from left to right. Because an explicit value of `3` is passed for `a`, the default fallback for `b` computes as $3 \times 2 = 6$.

### Q17. Cascade Default Evaluation

What is output to the engine console?

```js
function f(a = 1, b = a * 2) {
  return b;
}
console.log(f());

```

> **Answer:** `2`
> **Explanation:** When a function is called without arguments, the default value initialization steps down the parameter chain sequentially. First, `a` falls back to `1`, which allows `b` to resolve to $1 \times 2 = 2$.

### Q18. Triggering Parameter Default Initializers

What is output to the engine console?

```js
function f(x = 10) {
  return x;
}
console.log(f(undefined));

```

> **Answer:** `10`
> **Explanation:** Explicitly passing an argument of `undefined` signals to the engine that a value is missing, which triggers the default parameter initialization routine.

### Q19. Default Initializer Bypass Constraints

What is output to the engine console?

```js
function f(x = 10) {
  return x;
}
console.log(f(null));

```

> **Answer:** `null`
> **Explanation:** The engine treats `null` as an intentional, explicitly defined assignment of no value. Because it is a valid value, it completely bypasses default parameter initializers, which are only triggered by `undefined`.

### Q20. Lifecycle of Parameter Evaluation Mechanics

When exactly are default function parameters evaluated by the runtime engine?

> **Answer:** Dynamically at call-time.
> **Explanation:** Default parameter expressions do not compile to static values. Instead, they are evaluated fresh each time a function is called, allowing you to use dynamic expressions or instantiate new object references on every invocation.

### Q21. Sequential Parameter Inter-Dependency Constraints

Can a parameter default expression reference variables declared further down the parameter chain?

> **Answer:** No, parameter definitions are constrained by a temporal dead zone.
> **Explanation:** Parameters are evaluated in strict order from left to right. An earlier parameter cannot reference a later one because the later parameter has not yet been initialized. Doing so will trigger a `ReferenceError`.

---

## 🟦 SECTION 4 — Spread / Rest Operators & Restructuring

### Q22. Shallow Array Unpacking Operations

What is output to the engine console?

```js
const a = [1, 2];
const b = [...a, 3, 4];
console.log(b);

```

> **Answer:** `[1, 2, 3, 4]`
> **Explanation:** The spread operator (`...`) unpacks the elements of an iterable structure (like an array) directly into the new array wrapper.

### Q23. Shallow Object Synthesis Mechanics

What is output to the engine console?

```js
const obj = { a: 1 };
const copy = { ...obj, b: 2 };
console.log(copy);

```

> **Answer:** `{ a: 1, b: 2 }`
> **Explanation:** The object spread syntax clones all enumerable properties from a source object directly onto a new object container.

### Q24. Reference Copying and Object Cloning Depth

Does spreading an object using modern `{ ...targetObject }` syntax yield a deep clone?

> **Answer:** No, it performs a shallow clone.
> **Explanation:** The spread operator only copies top-level properties. If a property points to a nested object or array, the operator merely copies the reference pointer, meaning the source and the clone will still share that nested object in memory.

### Q25. Rest Parameter Synthesis Loops

What is output to the engine console?

```js
function f(...args) {
  return args.length;
}
console.log(f(1, 2, 3));

```

> **Answer:** `3`
> **Explanation:** When used in a function signature, the rest operator gathers any remaining standalone arguments and packages them into a real JavaScript array structure.

### Q26. Syntactic Positioning Constraints of Rest Parameters

What structural rule governs where a rest parameter can be placed in a function signature?

> **Answer:** It must always occupy the final position in the signature.
> **Explanation:** Because a rest parameter gathers all remaining arguments passed to a function, placing it before other parameters makes parameter parsing ambiguous. Doing so will trigger an explicit syntax error.

---

## 🟦 SECTION 5 — Control-Flow Iterators & Loops

### Q27. Enumerable Property Traversal Focus

What properties does the `for...in` loop traverse?

> **Answer:** It iterates over all enumerable string keys of an object, including inherited prototype keys.
> **Explanation:** The `for...in` loop is designed for inspecting an object's properties rather than iterating over array elements.

### Q28. Iterable Protocol Traversal Execution

What values does the `for...of` statement target?

> **Answer:** It targets the values provided by an iterable object's internal `@@iterator` method.
> **Explanation:** The `for...of` loop works with built-in iterables such as `Array`, `String`, `Map`, `Set`, and `NodeList`. It focuses directly on the data values themselves rather than the object's keys or property configurations.

### Q29. Array Metadata Pollution Side Effects

What is output to the engine console?

```js
const arr = ["a", "b"];
arr.extra = "c";

for (const i in arr) {
  console.log(i);
}

```

> **Answer:** `"0"`, `"1"`, `"extra"`
> **Explanation:** Because arrays are built on top of objects, `for...in` iterates over all enumerable keys, converting indices into strings (`"0"`, `"1"`) and picking up any custom properties (like `"extra"`) attached to the array object or its prototype chain.

### Q30. Selecting the Right Array Iterator

Why is `for...of` preferred over `for...in` when working with array structures?

> **Answer:** It guarantees you only loop through the actual data items in the array.
> **Explanation:** `for...of` respects the array's index ordering and completely ignores arbitrary metadata properties or prototype extensions attached to the array container.

---

## 🟦 SECTION 6 — Object & Array Destructuring Architecture

### Q31. Default Value Fallbacks for Destructured Missing Keys

What is output to the engine console?

```js
const { a = 10 } = {};
console.log(a);

```

> **Answer:** `10`
> **Explanation:** If a destructured property key is missing or evaluates strictly to `undefined` in the source object, the variable falls back to the provided default assignment value.

### Q32. Binding Alias Mapping Operations

What is output to the engine console?

```js
const { x: y } = { x: 5 };
console.log(y);

```

> **Answer:** `5`
> **Explanation:** The colon syntax (`x: y`) instructs the engine to look up the property key `x`, pull out its value, and bind it to a new local variable named `y`.

### Q33. Elision Patterns in Array Destructuring

What is output to the engine console?

```js
const [a, , c] = [1, 2, 3];
console.log(c);

```

> **Answer:** `3`
> **Explanation:** Leaving an empty space separated by commas (known as an elision pattern) skips specific indices during array destructuring, allowing you to extract only the values you need.

### Q34. Risks of Unprotected Deep Pointer Resolution

What runtime problem can occur when using nested destructuring patterns without fallback values?

> **Answer:** The application will throw a fatal `TypeError`.
> **Explanation:** If you try to extract values from a deep path (e.g., `const { user: { profile } } = data;`) and a mid-level property like `user` is missing or `null`, the engine crashes because it cannot look up properties on `undefined` or `null`.

---

## 🟦 SECTION 7 — Declarative Array Projection Pipelines

### Q35. Array Element Transformations via Projection Loops

What is output to the engine console?

```js
const res = [1, 2, 3].map(x => x * 2);
console.log(res);

```

> **Answer:** `[2, 4, 6]`
> **Explanation:** The `.map()` method loops through an array, runs a transformation function on each element, and returns a brand-new array containing the transformed results.

### Q36. Filtering Arrays using Predicate Logic

What is output to the engine console?

```js
const res = [1, 2, 3].filter(x => x > 1);
console.log(res);

```

> **Answer:** `[2, 3]`
> **Explanation:** The `.filter()` method checks each element against a truthy/falsy condition and returns a new array with only the elements that pass the test.

### Q37. First Match vs. Total Search Resolution

What does the `.find()` method return when searching an array?

> **Answer:** It returns the first element that satisfies the testing function, or `undefined` if no match is found.
> **Explanation:** Unlike `.filter()`, which checks the entire array, `.find()` halts execution the moment it finds a matching item and returns that individual element directly.

### Q38. Partial Validation via Predicate Checking

What is output to the engine console?

```js
console.log([1, 2, 3].some(x => x === 2));

```

> **Answer:** `true`
> **Explanation:** The `.some()` method returns `true` as soon as it finds at least one element in the array that matches the given condition.

### Q39. Global Array Consistency Assertions

What is output to the engine console?

```js
console.log([1, 2, 3].every(x => x > 0));

```

> **Answer:** `true`
> **Explanation:** The `.every()` method returns `true` only if every single element in the array passes the provided validation test.

---

## 🟦 SECTION 8 — Accumulators & The Reduce Engine

### Q40. Processing Arrays with Accumulators

What is output to the engine console?

```js
console.log([1, 2, 3].reduce((a, b) => a + b, 0));

```

> **Answer:** `6`
> **Explanation:** The `.reduce()` method loops through an array and uses a callback function to combine all its elements into a single aggregate value.

### Q41. Understanding the Accumulator Variable

What role does the first parameter of the `.reduce()` callback function play?

> **Answer:** It serves as the running total or intermediate state of the reduction process.
> **Explanation:** The accumulator stores the value returned from processing the previous element and passes it forward to the next step in the loop.

### Q42. Skipping Initial Value Declarations

What happens if you do not provide an initial value as the second argument to `.reduce()`?

> **Answer:** The engine uses the first element of the array as the initial accumulator value and starts looping from the second element.
> **Explanation:** While this works for simple operations like summing numbers, it will cause a `TypeError` if you try to run it on an empty array without an initial value.

### Q43. Building Associative Maps with Reducers

What is output to the engine console?

```js
const result = ["a", "b", "a"].reduce((acc, x) => {
  acc[x] = (acc[x] || 0) + 1;
  return acc;
}, {});
console.log(result);

```

> **Answer:** `{ a: 2, b: 1 }`
> **Explanation:** Starting with an empty object literal `{}` as the initial accumulator, this pattern loops through an array of tokens and builds a frequency map, tracking how often each item appears.

---

## 🟦 SECTION 9 — Modern Advanced Collections (Maps, Sets, Symbols)

### Q44. Key-Value Lookup Map Mechanics

What is output to the engine console?

```js
const m = new Map();
m.set("x", 10);
console.log(m.get("x"));

```

> **Answer:** `10`
> **Explanation:** The standard modern `Map` collection uses explicit `.set(key, value)` and `.get(key)` API methods to safely store and retrieve data.

### Q45. Advantages of Maps Over Standard Objects

What is the primary advantage of using a Map collection instead of a standard plain object literal?

> **Answer:** Maps accept any data type as a valid key and protect against prototype pollution.
> **Explanation:** While object keys are limited to strings or symbols, Map keys can be functions, objects, or any primitive type. Maps also stay isolated from the default `Object.prototype` keys, making them much more secure for dynamic data.

### Q46. Determining Set Cardinality Sizes

What is output to the engine console?

```js
console.log(new Set([1, 1, 2]).size);

```

> **Answer:** `2`
> **Explanation:** Set structures automatically filter out duplicate values. Passing `[1, 1, 2]` drops the duplicate `1`, leaving a set of two unique elements, so its `.size` property returns `2`.

### Q47. Unique Value Enforcement Guarantees

What core guarantee does a native `Set` collection provide?

> **Answer:** It guarantees that every element it stores is unique.
> **Explanation:** A Set uses the `SameValueZero` algorithm to compare incoming items, ensuring that duplicates are ignored and every value exists exactly once within the collection.

### Q48. Uniqueness Constraints of the Symbol Primitive

What does this equality test resolve to?

```js
console.log(Symbol("a") === Symbol("a"));

```

> **Answer:** `false`
> **Explanation:** Every time you call the `Symbol()` factory function, it creates a completely unique token in memory. The optional string argument is just a descriptive label and has no effect on equality tests.

### Q49. Enumeration Visibility Profiles of Symbols

Are object properties keyed by an ES6 `Symbol` visible during standard `for...in` loop traversals?

> **Answer:** No.
> **Explanation:** Symbol properties are explicitly hidden from standard iteration methods like `for...in`, `Object.keys()`, and `Object.getOwnPropertyNames()`. To retrieve them, you must use the specialized `Object.getOwnPropertySymbols()` method.

---

## 🟦 SECTION 10 — Advanced Mixed Execution Dynamics

### Q50. Type Coercion via Addition Operators

What is output to the engine console?

```js
console.log("5" + 2);

```

> **Answer:** `"52"`
> **Explanation:** If either operand of the binary `+` operator is a string, the engine prioritizes string concatenation over arithmetic addition, coercing the number `2` into a string.

### Q51. Type Coercion via Subtraction Operators

What is output to the engine console?

```js
console.log("5" - 2);

```

> **Answer:** `3`
> **Explanation:** Unlike the addition operator, the subtraction operator (`-`) only has a mathematical purpose. This forces the engine to convert the string `"5"` into a numeric primitive to complete the calculation.

### Q52. Reference Immutability vs. Structural Value Mutability

If a variable is declared using the `const` assignment keyword, can you safely change its values?

```js
const collection = [1, 2, 3];
collection[0] = 99; // Is this allowed?

```

> **Answer:** Yes, structural values can be changed, but the variable reference itself cannot be reassigned.
> **Explanation:** The `const` keyword simply ensures that the variable reference pointer in memory cannot change. It does not make objects or arrays immutable. To lock an object down completely, use the `Object.freeze()` method.

### Q53. Array Allocation Realities of the Projection Loop

Does running the `.map()` method change the contents of the original source array?

> **Answer:** No, it always leaves the source array untouched.
> **Explanation:** The `.map()` method adheres to functional programming principles by allocating a fresh array memory bucket for its output, keeping the source array completely unmutated.

### Q54. Core Benefits of Declarative Coding Styles

Why do production teams prefer modern functional pipelines (`.filter()`, `.map()`, `.reduce()`) over traditional procedural control loops?

> **Answer:** They encourage predictable data flow and make code easier to test and maintain.
> **Explanation:** These methods help reduce shared state bugs, eliminate side effects, and make code easier to reason about by replacing complex loop logic with clean, specialized operations.

---

## 🧠 FINAL REVIEW SUMMARY

This quiz bank serves as an overview of modern JavaScript execution behavior. Reviewing these questions reinforces:

* **The distinction between statements and expressions** when writing template strings.
* **How scoping rules change** when refactoring classic functions into arrow expressions.
* **How parameters are initialized** under different edge cases.
* **How the engine handles object references** during destructuring and spread operations.
* **How to chain array methods effectively** to build reliable,
* immutable data pipelines.
