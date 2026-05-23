# 🧪 Modern JavaScript Applied Engineering Pack

### 📊 Level: Intermediate to Advanced ES6+ Data Pipelines

This challenge bank is optimized for technical assessments, code reviews, and deep-dive practice sessions. It prioritizes **immutable data operations**, **syntactic precision**, and **declarative data transformation**.

---

## 🟦 MODULE 1 — Execution Mechanics & Lexical Scope

### 🔤 Challenge 1: The Expression Composer

* **Objective:** Harness evaluation boundaries inside structural strings.
* **Task:** Write a pure function named `formatProduct` that generates an optimized pricing declaration.
* **Signatures & Constraints:**
* Inputs: `product` (string), `basePrice` (number), `discountPercentage` (number floating between `0` and `1`).
* Return: A single string constructed exclusively via template literals. The final computed price calculation must be evaluated inline inside an execution token `${}`.


* **Example Test Case:**

```js
formatProduct("MacBook Pro", 2000, 0.15);
// Returns: "MacBook Pro costs $2000, final price: $1700"

```

### ⚡ Challenge 2: Lexical Refactoring & Scope Binding

* **Objective:** Convert procedural declarations to concise expressions without losing functional fallbacks.
* **Task:** Refactor the following statement into an arrow function declaration.

```js
function calculateTax(price) {
  return price * 0.07;
}

```

* **Extension Requirements:**
* Bind the refactored code to a constant variable named `computeAssessment`.
* Implement an inline default evaluation parameter ensuring that if the tax rate argument is omitted, it defaults to `0.10`.



### 🛡 Challenge 3: Safe Boundary Divider

* **Objective:** Prevent mathematical evaluation corruption utilizing short-circuit parameters.
* **Task:** Create an arrow function named `safeDivide` processing inputs `numerator` and `denominator`. If the second parameter is missing, evaluate the process using a structural default fallback value of `1`.

### 🧠 Debug Task: String Interpolation Interception

* **Context:** A engineer complains that their script is outputting raw literal characters instead of injecting local execution state. Inspect, identify the root mechanical flaw, and supply the corrected block.

```js
const userAccount = "Sam";
// Identifies the failure line below:
console.log("Hello ${userAccount}, system initialization complete.");

```

### 🚀 Module Extension: Ternary Evaluation Matrix

* **Task:** Build a single-line structural expression using template literals that evaluates a boolean variable `isPremiumMember`. If true, interpolate `"Tier-1 Priority Access"`; otherwise, return `"Standard Baseline Access"`. The conditional logic must reside entirely inside the string interpolation expression.

---

## 🟦 MODULE 2 — Memory References & Immutable Transformations

### 🌊 Challenge 1: State Object Lifecycle Isolation

* **Objective:** Mutate data topology across memory reference profiles without altering upstream references.
* **Context:** Given the following operational application config state:

```js
const applicationState = { theme: "matrix-dark", runtimeVersion: 4 };

```

* **Task:** Write a transformation routine that outputs a completely new object reference. The output object must append a property key `compiled: true` and increment the value of `runtimeVersion` by `1`.
* **Assertion Boundary:** Running `applicationState.runtimeVersion === 5` must evaluate to `false`.

### 📦 Challenge 2: Variadic Operational Accumulator

* **Objective:** Manipulate indefinite parameter matrices using gather syntax operations.
* **Task:** Create an engineering utility named `multiplyAll` capable of accepting an open-ended collection of numerical arguments.
* **Requirements:**
* Must use rest parameter syntax (`...args`).
* Return the compound product of every input element provided. If no arguments are passed, return `0`.



### 🔁 Challenge 3: Control-Flow Imperative to Declarative Migration

* **Objective:** Move from tracked index variables to native structural value iterators.
* **Task:** Refactor this classic loop block into a modern, declarative `for...of` sequence to eliminate manual index management:

```js
const metricsStream = [102, 204, 306];
for (let index = 0; index < metricsStream.length; index++) {
  console.log(metricsStream[index]);
}

```

### 🧠 Debug Task: Structural Object Enumeration Failure

* **Context:** The engine throws a catastrophic `TypeError: obj is not iterable` when running the application block below. Pinpoint the structural reason why this execution fails and write the clean, modern ES6+ correction.

```js
const clusterNodes = { nodeAlpha: "10.0.0.1", nodeBeta: "10.0.0.2" };

for (const node Address of clusterNodes) {
  console.log(nodeAddress);
}

```

### 🚀 Module Extension: Deep Immutable Configurations

* **Task:** Create a system utility function named `mergeConfigLayers` that accepts three independent configuration objects (`systemDefault`, `environmentOverride`, `userPreference`).
* **Rules:** Combine them into a single comprehensive configuration output where properties from later objects overwrite earlier ones. The transformation must happen inline and preserve strict immutability across all three sources.

---

## 🟦 MODULE 3 — Object & Array Destructuring Architecture

### 📦 Challenge 1: Data Contract Deserialization & Normalization

* **Objective:** Extract raw network payloads and convert them to internal domain-model properties in one step.
* **Context:** Given a backend API transmission format:

```js
const networkPayload = {
  status_code: 200,
  payload_data: { account_id: 842, display_name: "Ava_Dev" }
};

```

* **Task:** Use an inline destructuring pattern to extract `account_id` and `display_name`, mapping them directly to two clean variables named `id` and `username`.

### 🧬 Challenge 2: Deep Path Extraction

* **Objective:** Drill through complex objects to safely extract nested variables.
* **Task:** Extract the nested property `locality` from the data graph below using a single line of destructuring syntax:

```js
const enterpriseGraph = {
  organization: {
    headquarters: {
      locality: "Singapore Financial District"
    }
  }
};

```

### 🔄 Challenge 3: Declared Function Parameters Demultiplexing

* **Objective:** Destructure object shapes directly inside the function signature block.
* **Task:** Author a function named `renderTelemetry` that accepts an object matching the schema below:

```js
const instance = { metadata: { serviceName: "Ingress_Gateway", deploymentRole: "Edge_Proxy" } };

```

* **Requirements:** Destructure `serviceName` and `deploymentRole` directly inside the function parameter parentheses. Return the formatted evaluation: `"Service: Ingress_Gateway | Role: Edge_Proxy"`.

### 🧠 Debug Task: Destructuring Reference Pointer Collapse

* **Context:** The application encounters a fatal runtime crash when executing the following line under empty-state conditions. Explain why the crash occurs and rewrite the statement to provide native structural resilience.

```js
const { operationalMatrix: { activeNode } } = {};

```

### 🚀 Module Extension: Flattening Destructured Extractions

* **Task:** Use complex nesting patterns along with object shorthand notation to convert the deep nested data target `{ matrix: { vector: { scalar: 100 } } }` into a flat local configuration footprint object: `{ scalar: 100 }`.

---

## 🟦 MODULE 4 — Functional Array Pipelines & Accumulators

### 🔁 Challenge 1: Element Projection Transformations

* **Objective:** Map structural strings cleanly into defined identifier conventions.
* **Task:** Map an input string collection: `["engine", "compiler", "runtime"]` into a transformed collection appending an architecture marker.
* **Expected Output:** `["ENGINE_SYSTEM", "COMPILER_SYSTEM", "RUNTIME_SYSTEM"]`

### 🔍 Challenge 2: Multi-Step Filter and Extraction Pipelines

* **Objective:** Chain functional concepts to filter records and isolate specific property data fields.
* **Context:** Given an enterprise runtime worker thread pool array:

```js
const workerPool = [
  { workerId: "Tx-101", executionState: "active" },
  { workerId: "Tx-102", executionState: "idle" },
  { workerId: "Tx-103", executionState: "active" }
  { workerId: "Tx-104", executionState: "terminated" }
];

```

* **Task:** Construct a chained functional array pipeline that isolates workers with an `"active"` execution state and returns an array containing only their raw string IDs.
* **Expected Output:** `["Tx-101", "Tx-103"]`

### 🧠 Challenge 3: Declarative Token Frequency Reduction

* **Objective:** Convert flat series tracking matrices into discrete frequency histograms using associative array collection structures.
* **Task:** Write a functional pipeline processing a raw tracking array:

```js
const logTokens = ["auth", "db", "auth", "gateway", "db", "auth"];

```

* **Expected Output Object:** `{ auth: 3, db: 2, gateway: 1 }`

### 🔥 Challenge 4: Pure Mathematical Pipeline Architecture

* **Objective:** Chain filter, map, and reduce operations into a clean, unmutated pipeline.
* **Task:** Write a unified processing pipeline processing an array of random readings: `[-12, 5, -3, 8, 22, -1, 0]`.
* **Pipeline Sequence Constraints:**
1. Strip away all negative metrics (`< 0`).
2. Square the remaining values ($x^2$).
3. Sum the resulting squares into a single final value.



### 🧠 Debug Task: Missing Accumulator State Propagation

* **Context:** An engineer tracking metric points notices the following code block constantly returns `undefined`. Pinpoint the architectural flaw and fix the code loop:

```js
const aggregateValue = [12, 24, 36].reduce((accumulator, element) => {
  accumulator + element;
}, 0);

```

### 🚀 Module Extension: Contextual Log Analytics Processing

* **Task:** Given an unparsed system trace event log: `["init", "handshake", "sys_error", "handshake", "terminate", "sys_error"]`. Write a chained functional processing array sequence that:
1. Filters out all `"sys_error"` flags.
2. Transforms remaining event strings to uppercase.
3. Reduces the remaining output into a sorted frequency table mapping logs to occurrences.



---

## 🟦 MODULE 5 — Advanced Collection Types & Custom Key Spaces

### 🗺 Challenge 1: High-Performance Registry Map Architecture

* **Objective:** Implement key-value storage that avoids prototype pollution risks.
* **Task:** Use an ES6 `Map` collection to build a fast session tracking lookup engine.
* **Requirements:**
* Create helper routines to add, read, and clear session tokens.
* Use numeric user IDs as structural map keys and numeric timestamps as evaluation map values.



### 🎯 Challenge 2: Hybrid Uniqueness & Counting Operations

* **Objective:** Combine uniqueness guarantees with standard key-value maps to parse raw tracking records.
* **Task:** Process a dirty transaction stream array: `["txA", "txB", "txA", "txC", "txB", "txA"]`.
* **Requirements:**
1. Use a native `Set` to extract a unique list of transactions.
2. Use an ES6 `Map` to calculate the final occurrence frequencies for each unique transaction.



### 🧩 Challenge 3: Non-Enumerable Metaprogramming Fields

* **Objective:** Hide internal tracking data from standard iteration methods.
* **Task:** Create an application user account data object. Attach an internal identifier tag to this object using an ES6 `Symbol` key.
* **Requirement Boundary:** This hidden tracking key must remain fully readable via direct access, yet disappear completely during standard loops or `Object.keys()` serialization routines.

### 🧠 Debug Task: Set Cardinality Mechanics

* **Context:** Look over this state management script. Explain exactly what properties the storage reference holds at conclusion, and clarify why the secondary execution call failed to change its size.

```js
const uniqueRegistrar = new Set([100, 200, 200, 300]);
uniqueRegistrar.add(300);

```

### 🚀 Module Extension: Multi-tier Data Pipeline Engine

* **Task:** Sketch out a small processing system using three different structural data shapes working together:
* Use a `Set` to validate that new entries are unique.
* Save validated entries into a master `Map` storage architecture.
* Export the final records as a clean, standardized configuration object layout.



---

## 🧠 FINAL CAPSTONE PROJECT CHALLENGE

### Real-Time Telemetry Stream Processing Engine

* **Scenario:** You are building an edge-node telemetry processor that clean and formats raw log event arrays before sending them to a central monitoring dashboard.

#### Raw System Inputs:

```js
const operationalTelemetryStream = [
  "telemetry_tick", 
  "database_sync", 
  "telemetry_tick", 
  "network_drop_warning", 
  "telemetry_tick", 
  "database_sync"
];

```

#### Engineering Requirements:

1. **Filter Isolation:** Filter out all instances of `"network_drop_warning"` to keep the log pipeline clean.
2. **Data Uniformity Projection:** Normalize all event tokens into strict uppercase strings.
3. **Data Reducer Consolidation:** Reduce the transformed elements into a clean, flat object metric block showing exact transaction frequency counts.
4. **Immutability Constraints:** Write the entire operation as a single, continuous expression chain without creating temporary variables or modifying the source data array.

#### Expected Output Format:

```js
{ 
  TELEMETRY_TICK: 3, 
  DATABASE_SYNC: 2 
}

```

---

## 🎯 PEDAGOGICAL DESIGN PRINCIPLES

This collection is built around specific learning goals to help engineers write clean, production-ready code:

* **Transfer Over Recall:** Replaces standard boilerplate templates with novel real-world problems that test real conceptual mastery.
* **Immutability Enforcement:** Requires clean separation of data state transformations to avoid unintended side effects across memory pointers.
* **Pipeline Mental Model:** Trains developers to break down procedural, multi-step operations into reliable, declarative code chains.
* **Defensive Error Shielding:** Emphasizes testing edge cases and handling empty states to ensure applications run smoothly under unexpected conditions.
