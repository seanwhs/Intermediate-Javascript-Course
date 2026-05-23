# 🧪 Intermediate JavaScript Lab Sheets - Applied ES6+ Curriculum

---

# 🟦 MODULE 1: Clean Syntax & Execution Mechanics

## 🧪 Lab 1.1: Template Literals Engine

### 🎯 Objective

Replace legacy string concatenation with the modern, reactive backtick evaluation system.

### 🧪 Task

Refactor the following snippet to construct the required output string dynamically without punctuation manual adjustments:

```js
const name = "Alex";
const score = 90;

// TODO: Refactor this line using template literal syntax
const output = name + " scored " + score + " points";

```

### ⚠️ Constraints

* Strict **ban** on the variable addition operator (`+`) for string construction.

### 🧠 Hint

Enclose the template string within backticks ``` and declare internal logic properties inside placeholder boundaries `${expression}`.

### ✅ Expected Output

```js
"Alex scored 90 points"

```

### 🚀 Stretch Goal

Inject an evaluated mathematical operator directly inside the string boundary to display a modified calculation value: `${score + 10}`.

---

## 🧪 Lab 1.2: Arrow Function Refactor

### 🎯 Objective

Convert standard function statement allocations into modern, concise arrow-style closures (`=>`).

### 🧪 Task

Rewrite this functional declaration into an inline arrow structure, taking advantage of implicit return structures:

```js
// TODO: Refactor into an arrow function assigned to a constant named 'multiply'
function multiply(a, b) {
  return a + b;
}

```

### ⚠️ Constraints

* The refactored statement must use arrow function syntax.
* Leverage implicit returns by omitting the explicit `return` keyword and block curly brackets entirely.

### 🧠 Hint

When an arrow function body consists of a single expression, the values are returned automatically.

### ✅ Expected Output

```js
console.log(multiply(3, 4)); // 12

```

---

## 🧪 Lab 1.3: Default Parameter Safety

### 🎯 Objective

Enforce strict parameter fallbacks at the signature level to eliminate missing argument vulnerabilities.

### 🧪 Task

Modify the parameters of this function declaration so that omitting arguments does not cause accidental `undefined` text rendering:

```js
// TODO: Add a signature fallback value of "Guest" to the 'name' parameter
function greet(name) {
  return "Hello " + name;
}

console.log(greet());

```

### ⚠️ Constraints

* Do not use manual internal logical checks (like `if (!name)`) inside the function block body.

### 🧠 Hint

Assign a value directly to the parameter name inside the function declaration parentheses: `function clear(param = defaultValue)`.

### ✅ Expected Output

```js
"Hello Guest"

```

### 🚀 Stretch Goal

Introduce a second optional argument configuration named `greeting` that defaults seamlessly to `"Hello"`.

---

## 🚀 Capstone 1: Safe Formatter Engine

### 🎯 Objective

Combine template syntax, arrow abstractions, and parameter fallbacks to construct a production-ready telemetry analyzer.

### 🧪 Task

Build a unified, single-line arrow utility named `formatEventLog`.

The logic must take two parameters, `event` and `user`, handling cases where values are missing by assigning default values (`"SYSTEM"` and `"Anonymous"`, respectively). It should output a standardized logging string.

### 🧪 Boilerplate

```js
// TODO: Complete this single-line function signature and body execution
const formatEventLog = ( /* Parameters here */ ) => // Implicit construction here

console.log(formatEventLog("LOGIN", "Sean"));
console.log(formatEventLog(undefined, undefined));

```

### ✅ Expected Output

```js
"[LOGIN] User: Sean"
"[SYSTEM] User: Anonymous"

```

---

# 🟦 MODULE 2: Data Pipelines

## 🧪 Lab 2.1: Spread Operator Clone

### 🎯 Objective

Understand state reference preservation by creating shallow copies that isolate original data models.

### 🧪 Task

Fix the code below so that updating the copied collection does not accidentally alter the values stored in the original source array:

```js
const arr = [1, 2, 3];

// TODO: Fix this line using the array spread operator to prevent shared reference assignment
const copy = arr; 

copy.push(4);

console.log("Original:", arr);
console.log("Copy:", copy);

```

### ⚠️ Constraints

* Do not manually loop through or hardcode the index elements of the array.

### 🧠 Hint

Enclose individual items extracted out of the target object context within deep brackets: `[...targetIterable]`.

### ✅ Expected Output

```js
Original: [1, 2, 3]
Copy: [1, 2, 3, 4]

```

---

## 🧪 Lab 2.2: Rest Parameter Sum

### 🎯 Objective

Design flexible functions that handle dynamic numbers of inputs by compiling indefinite parameter structures.

### 🧪 Task

Create an arrow function named `sum` that can take an unlimited number of arguments and return their mathematical total.

### 🧪 Boilerplate

```js
// TODO: Complete this function using a rest parameter gather layer combined with .reduce()
const sum = (...nums) => nums.reduce((acc, current) => acc + current, 0);

console.log(sum(1, 2, 3, 4));
console.log(sum(5, 10));

```

### 🧠 Hint

The rest parameter `...args` gathers separate sequential values into a true array instance, giving you immediate access to `.reduce()`.

### ✅ Expected Output

```js
10
15

```

---

## 🧪 Lab 2.3: Iteration Fix

### 🎯 Objective

Fix a control-flow error where an incorrect loop setup outputs index strings instead of actual collection values.

### 🧪 Task

Swap out the legacy index inspector variable with the modern iterable value scanner to log the actual values:

```js
// TODO: Modify this structural execution loop to fetch real element entries instead of internal keys
for (const i in [10, 20, 30]) {
  console.log(i);
}

```

### ✅ Expected Output

```js
10
20
30

```

---

## 🚀 Capstone 2: Data Pipeline Builder

### 🎯 Objective

Chain declarative array operations together to filter, sanitize, and aggregate raw server metrics into a clean data summary.

### 🧪 Task

Process the raw data stream below by building a functional processing pipeline. Your pipeline must filter out invalid empty data values (`null`), drop specific administrative actions (`"logout"`), and summarize the remaining matching logs into a neat occurrence counter object.

### 🧪 Boilerplate

```js
const data = ["login", "logout", "login", null, "login"];

// TODO: Chain your .filter() and .reduce() pipelines together here
const pipelineResult = data
  .filter(item => item !== null && item !== "logout")
  .reduce((acc, current) => {
    acc[current] = (acc[current] || 0) + 1;
    return acc;
  }, {});

console.log(pipelineResult);

```

### ✅ Expected Output

```js
{ login: 3 }

```

---

# 🟦 MODULE 3: Destructuring & Contracts

## 🧪 Lab 3.1: Object Extraction

### 🎯 Objective

Unpack specific properties from an object directly into local variables without using manual dot-notation lookups.

### 🧪 Task

Extract both the `name` and `age` fields from the provided user object using a single object destructuring statement:

```js
const user = { name: "Sean", age: 30 };

// TODO: Extract the properties out using a single destructuring contract line

console.log(name);
console.log(age);

```

### ✅ Expected Output

```js
"Sean"
30

```

---

## 🧪 Lab 3.2: Nested Extraction

### 🎯 Objective

Drill down through deep, nested object graphs to extract hidden terminal fields in a single line of code.

### 🧪 Task

Unpack the deeply nested `name` attribute out of the tracking block below using a multi-level destructuring pattern:

```js
const data = {
  user: {
    profile: {
      name: "Sean"
    }
  }
};

// TODO: Extract 'name' directly using structural pathway tracing matching the source layout

console.log(name);

```

### ✅ Expected Output

```js
"Sean"

```

---

## 🧪 Lab 3.3: Rename Fields

### 🎯 Objective

Alias incoming properties during the destructuring process to prevent name collisions and adapt external schemas to local naming standards.

### 🧪 Task

Extract the external snake_case property `user_name` from the API response object below, mapping it immediately to a new camelCase local variable named `username`:

```js
const apiResponse = { user_name: "Sean" };

// TODO: Destructure and rename 'user_name' to 'username' in a single assignment contract

console.log(username);

```

---

## 🚀 Capstone 3: API Normalizer

### 🎯 Objective

Flatten complex, nested, third-party payloads into a clean internal data format using advanced destructuring patterns.

### 🧪 Task

Extract the deep field `first_name` and rename it to `username`. At the same time, extract the `status` field and provide a default fallback value of `"active"` in case it's missing from the source payload.

### 🧪 Boilerplate

```js
const externalPayload = {
  id: 101,
  meta: {
    identity: {
      first_name: "Sean"
    }
  }
};

// TODO: Write the nested destructuring, aliasing, and default contract statement here
const {
  meta: {
    identity: { first_name: username }
  },
  status = "active"
} = externalPayload;

console.log(username);
...
console.log(status);

```

### ✅ Expected Output

```js
"Sean"
"active"

```

---

# 🟦 MODULE 4: Functional Arrays

## 🧪 Lab 4.1: map() Transformation

### 🎯 Objective

Perform immutable element modifications across an entire array collection using declarative transformation statements.

### 🧪 Task

Transform the array of base integers below into a completely new array where every original value is doubled:

```js
const nums = [1, 2, 3];

// TODO: Double all elements immutably using .map()
const doubled = nums.map(n => n * 2);

console.log(doubled);

```

### ✅ Expected Output

```js
[2, 4, 6]

```

---

## 🧪 Lab 4.2: filter() Extraction

### 🎯 Objective

Conditionally extract elements out of an array based on a boolean criteria check.

### 🧪 Task

Filter the array below to create a new subset containing only the numbers that are strictly greater than 1:

```js
const sourceNumbers = [1, 2, 3];

// TODO: Complete the evaluation statement using .filter()
const filteredNumbers = sourceNumbers.filter(n => n > 1);

console.log(filteredNumbers);

```

### ✅ Expected Output

```js
[2, 3]

```

---

## 🧪 Lab 4.3: Evaluation Methods

### 🎯 Objective

Differentiate between collection evaluation methods (`find`, `some`, `every`) by testing array elements against boolean conditions.

### 🧪 Task

Analyze the user session array below. Use `find()` to retrieve the first inactive user object, `some()` to check if any user is inactive, and `every()` to see if all users are currently active:

```js
const users = [
  { id: 1, active: true },
  { id: 2, active: false },
  { id: 3, active: true }
];

// TODO: Implement the three distinct evaluation queries below
const inactiveUser = users.find(u => !u.active);
const hasInactive   = users.some(u => !u.active);
const allActive     = users.every(u => u.active);

console.log(inactiveUser);
console.log(hasInactive);
console.log(allActive);

```

### ✅ Expected Output

```js
{ id: 2, active: false }
true
false

```

---

## 🚀 Capstone 4: Frequency Engine

### 🎯 Objective

Use the flexible accumulation system of `.reduce()` to count item occurrences and build custom aggregate metrics maps.

### 🧪 Task

Process the raw tag array below to count how many times each string occurs, compiling the results into a key-value frequency object.

### 🧪 Boilerplate

```js
const logs = ["a", "b", "a", "c", "b", "a"];

// TODO: Implement a frequency mapping engine using the .reduce() accumulator pattern
const totalFrequencies = logs.reduce((acc, log) => {
  acc[log] = (acc[log] || 0) + 1;
  return acc;
}, {});

console.log(totalFrequencies);

```

### ⚠️ Constraints

* You must use `.reduce()` with an explicitly declared initial object fallback value (`{}`).

### ✅ Expected Output

```js
{ a: 3, b: 2, c: 1 }

```

---

# 🟦 MODULE 5: Advanced Data Structures

## 🧪 Lab 5.1: Map Usage

### 🎯 Objective

Store and retrieve key-value pairs using a specialized Map, highlighting its ability to accept complex object instances as valid dictionary keys.

### 🧪 Task

Create a Map instance, associate an object reference key with a string access modifier value, and then read the stored value back using the map's built-in methods.

### 🧪 Boilerplate

```js
const registry = new Map();
const userKey = { id: 771 };

// TODO: Store 'userKey' inside the Map with the value "ADMIN_ACCESS"
registry.set(userKey, "ADMIN_ACCESS");

// TODO: Retrieve and print that exact value out below using the Map's lookup methods
console.log(registry.get(userKey));

```

### ✅ Expected Output

```js
"ADMIN_ACCESS"

```

---

## 🧪 Lab 5.2: Set Deduplication

### 🎯 Objective

Instantly strip duplicate entries out of primitive lists using high-performance Set operations combined with array spread syntax.

### 🧪 Task

Deduplicate the raw array below in a single step, ensuring the final output is a true array containing only unique numbers:

```js
const duplicateList = [1, 1, 2, 3, 3, 3, 4];

// TODO: Convert the list to a unique Set and unpack it back into a standard array format
const uniqueList = [...new Set(duplicateList)];

console.log(uniqueList);

```

### ✅ Expected Output

```js
[1, 2, 3, 4]

```

---

## 🧪 Lab 5.3: Symbol Key Isolation

### 🎯 Objective

Enforce strict key isolation on object properties using non-colliding primitive Symbols to protect critical meta-attributes from accidental overrides.

### 🧪 Task

Generate a new unique identifier key using `Symbol()`, attach it to the target user record object, and demonstrate that the property remains safely isolated during standard key inspections:

```js
const secureKey = Symbol("internal_id");
const clientRecord = { name: "Alex" };

// TODO: Assign the value 999 to the clientRecord object using the secureKey Symbol as the key
clientRecord[secureKey] = 999;

console.log(clientRecord[secureKey]);
console.log(Object.keys(clientRecord)); // Check if the Symbol property is hidden from key lists

```

### ✅ Expected Output

```js
999
["name"] // The symbol is successfully isolated from general key loops

```

---

## 🚀 Capstone 5: Multi-Structure System

### 🎯 Objective

Combine specialized structures (Sets, Maps, and Symbols) to process a raw batch log stream while preserving item lookup order.

### 🧪 Task

Process the raw data array below. First, remove duplicate items using a Set. Next, store the resulting unique elements inside a Map where each entry is bound to a hidden, non-colliding Symbol key value.

### 🧪 Boilerplate

```js
const streamInput = ["alpha", "alpha", "beta", "gamma", "beta"];

// 1. Deduplicate the raw stream data using a Set
const uniqueItems = [...new Set(streamInput)];

// 2. Initialize a storage Map container
const secureStorageMap = new Map();

// TODO: Loop through the unique items, create a hidden Symbol key for each, and store them in the Map
uniqueItems.forEach(item => {
  const privateId = Symbol(item);
  secureStorageMap.set(privateId, item);
});

console.log(secureStorageMap.size);

```

### ✅ Expected Output

```js
3

```

---

# 🧠 FINAL CAPSTONE LAB

## 🚀 Full Data Pipeline System

### 🎯 Objective

Combine everything you've learned across all modules to build a complete, production-grade telemetry analytics engine.

```
[ Raw Event Logs Stream ]
          │
          ▼
    Clean & Sanitize  <── Exclude invalid values & "logout" entries
          │
          ▼
  Deduplicate Items   <── Isolate unique events using a Set
          │
          ▼
 Compile Metrics Map  <── Store frequencies in a Map under a secure Symbol key
          │
          ▼
[ Polished Operational Data Structure ]

```

### 🧪 Task

Write a unified, modular program that processes the raw logs array below by executing the following operational pipeline steps:

1. **Clean & Sanitize:** Use `.filter()` to strip away empty data entries (`null`, `undefined`) and exclude generic `"logout"` events.
2. **Deduplicate:** Use a `Set` to isolate the unique collection values remaining in the stream.
3. **Aggregate:** Use `.reduce()` on your sanitized data to compile an occurrence frequency summary.
4. **Secure Storage:** Store the final frequency metrics object inside a `Map` container under a secure, non-colliding `Symbol("analytics_key")` lookup reference.

### 🧪 Final Evaluation Template

```js
const operationalLogs = ["login", null, "login", "logout", "login", undefined, "initialize", "initialize"];

// Step 1: Clean and filter the log stream
const sanitizedLogs = operationalLogs.filter(log => log !== null && log !== undefined && log !== "logout");

// Step 2: Deduplicate to isolate unique operations
const uniqueOperations = [...new Set(sanitizedLogs)];

// Step 3: Count event frequencies using reduce
const analyticsSummary = sanitizedLogs.reduce((acc, log) => {
  acc[log] = (acc[log] || 0) + 1;
  return acc;
}, {});

// Step 4: Secure the results in a Map container using a Symbol key
const secureAnalyticsMap = new Map();
const metricsKey = Symbol("analytics_key");

secureAnalyticsMap.set(metricsKey, analyticsSummary);

// --- Verification Assertions ---
console.log("Unique Tracked Ops:", uniqueOperations);
console.log("Pipeline Metrics:", secureAnalyticsMap.get(metricsKey));

```

### ✅ Expected Output

```js
Unique Tracked Ops: ["login", "initialize"]
Pipeline Metrics: { login: 3, initialize: 2 }

```

---

# 🧭 END OF LAB SHEET PACK
