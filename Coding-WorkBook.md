# 📘 Coding Workbook: Intermediate JavaScript & Applied ES6+

---

# 🟦 MODULE 1: Syntax & Execution Mechanics Workbook

## 🧩 Drill 1: Expression Evaluation Thinking

### 📝 Task

Analyze the following code block. Write down your predicted console output **before running the snippet** in your terminal.

```js
console.log(`Total: ${5 + 10}`);
console.log(`Check: ${"5" + 10}`);
console.log(`Flag: ${Boolean(0)}`);

```

### 🎯 Concept Focus

* Structural evaluation dynamics inside template string placeholders (`${}`).
* JavaScript implicit and explicit runtime type coercion mechanics.

---

## ⚙️ Challenge 1: Dynamic Message Builder

### 📝 Task

Write a clean, reusable system message generator using an arrow function closure.

### ⚙️ Implementation Requirements

* **Function Signature:** Define an arrow function named `generateTelemetryReport`.
* **Accepted Inputs:** `user` (String), `action` (String), `count` (Number).
* **Technical Constraints:** Must use a single-line backtick template literal with an embedded mathematical computation directly inside the string interpolation placeholder.

### ✅ Expected Output Match

```js
console.log(generateTelemetryReport("Sean", "API_REQUEST", 3));
// Output: "User Sean performed 3 actions today. Next milestone: 8 actions."

```

---

## 🧠 Debug Task: Broken String Logic

### ❌ Broken Implementation

The following code was deployed to output diagnostic details but displays literal characters instead of the variables:

```js
const name = "Alex";

// ERROR: Interpolation values are rendering out raw as literal characters
console.log('Hello ${name}');

```

### 🛠️ Execution Analysis & Fix

1. **Identify the Root Cause:** Explain why the single quotes (`'`) block expression compilation.
2. **Refactor the Code:** Rewrite the expression using the correct string literal syntax to allow dynamic runtime evaluation.

---

## 🚀 Extension: Conditional String Renderer

### 📝 Task

Build an inline status parser using an arrow function called `renderStatusMessage`. The function must evaluate an application string parameter (`"active"` or `"inactive"`) and return distinct outputs **without using if/else keywords or switch statements**.

### ⚙️ Constraints

* Must use a single-line template literal.
* Must handle the conditional branching logic entirely inside the placeholder using a ternary operator.

---

# 🟦 MODULE 2: Data Pipeline Workbook

## 🧩 Drill 1: Spread Prediction

### 📝 Task

Predict the state of both `a` and `b` at the end of execution. Does modifying `b` affect `a`? Explain why based on memory references.

```js
const a = [1, 2];
const b = [...a];
b.push(3);

console.log(a); // Predict this value
console.log(b); // Predict this value

```

---

## ⚙️ Challenge 1: Immutable Updater

### 📝 Task

Write an arrow utility function named `safelyUpdateConfig` that processes an incoming configuration model immutably.

### 📥 Sample Input Structure

```js
const globalConfig = { theme: "dark", layout: "grid", version: 1.2 };

```

### ⚙️ Implementation Requirements

* **Action:** Override the `theme` property value to `"light"`.
* **Constraint:** Do not mutate the original `globalConfig` object pointer. Return a completely new object instance using object spread syntax.

---

## ⚙️ Challenge 2: Flexible Summation Engine

### 📝 Task

Create an open-ended mathematical utility function called `computeProductStream`.

### ⚙️ Implementation Requirements

* **Signature:** Must use **Rest Parameter** (`...args`) syntax to accept a dynamic number of arguments.
* **Internal Logic:** Process the gathered array using `.reduce()` to return the total product (multiplication) of all provided numbers.

---

## 🧠 Debug Task: Loop Misuse Detection

### ❌ Broken Implementation

A developer is trying to iterate through an object's properties using the following loop, but it crashes at runtime with a `TypeError`:

```js
const servicePayload = { node_id: 101, region: "us-east" };

// CRASH: TypeError: servicePayload is not iterable
for (const val of servicePayload) {
  console.log(val);
}

```

### 🛠️ Execution Analysis & Fix

1. **Identify the Root Cause:** Explain the difference between standard enumerable object profiles and iterable collections.
2. **Refactor the Code:** Rewrite the loop with the proper modern loop construct to display the object keys and values safely.

---

## 🚀 Extension: Config Merger Engine

### 📝 Task

Create a utility function called `deepMergeConfigurations` that accepts an arbitrary number of configuration objects, combines them into one, and protects against data corruption.

```
[Config Obj A] + [Config Obj B] + [Config Obj C] ───(Object Spread)───► [New Combined Config]

```

### ⚙️ Constraints

* Must accept an unknown number of input arguments using rest parameters.
* Later arguments must overwrite properties from earlier ones.
* The function must be pure and cause zero side effects to the original input parameters.

---

# 🟦 MODULE 3: Destructuring Workbook

## 🧩 Drill 1: Extraction Prediction

### 📝 Task

Predict the console output of the snippet below. What happens in memory during this single-line property assignment?

```js
const data = {
  user: { name: "Sam", age: 25 }
};

const { user: { name } } = data;

console.log(name);

```

---

## ⚙️ Challenge 1: API Normalizer

### 📝 Task

Extract nested keys from an unformatted legacy database structure and reshape them into a standardized internal object format.

### 📥 Target Source Layout

```js
const apiIncomingResponse = {
  response_code: 200,
  payload: {
    user_id: 42,
    user_name: "Sam"
  }
};

```

### ⚙️ Implementation Requirements

* Extract `user_id` and rename it to a local constant named `id`.
* Extract `user_name` and rename it to a local constant named `username`.
* **Constraint:** Complete this operation using a single object destructuring assignment statement.

---

## ⚙️ Challenge 2: Parameter Contract Function

### 📝 Task

Write an arrow function called `compileProfileString` that uses deep object destructuring directly inside its parameter signature slot.

### 📥 Expected Parameter Shape

```js
const inputAccount = { id: 42, info: { name: "Sam", city: "SG" } };

```

### ✅ Expected Output Match

```js
console.log(compileProfileString(inputAccount));
// Output: "User 42: Sam lives in SG"

```

---

## 🧠 Debug Task: Crash Analysis

### ❌ Broken Implementation

The following extraction layout crashes immediately if an external service returns an empty or incomplete response object:

```js
const serverResponse = {};

// CRASH: TypeError: Cannot read properties of undefined (reading 'name')
const { user: { name } } = serverResponse;

```

### 🛠️ Execution Analysis & Fix

Refactor the destructuring assignment statement to include defensive safety fallbacks (default values). This ensures the program handles empty or incomplete objects gracefully without crashing.

---

## 🚀 Extension: Deep Merge Extractor

### 📝 Task

Write a single-line destructuring expression that drills down through three layers of an unverified data structure to extract a target primitive value.

If any intermediate layer is missing, the code should fall back safely to a default value of `0` instead of crashing.

```js
const messyData = { a: {} }; // Missing deep children properties

```

---

# 🟦 MODULE 4: Functional Array Workbook

## 🧩 Drill 1: Output Prediction

### 📝 Task

Trace the execution steps of this functional array pipeline. Write out the final array instance structure produced by this chain:

```js
const result = [1, 2, 3]
  .map(x => x + 1)
  .filter(x => x > 2);

console.log(result); // What is the value of this array?

```

---

## ⚙️ Challenge 1: Tag Transformer

### 📝 Task

Convert an array of lowercase technological identifiers into an array of formatted tracking tags using declarative mapping strategies.

### 📥 Data Array

```js
const shortTags = ["js", "node", "react"];

```

### ✅ Expected Output Match

```js
console.log(transformedTags); 
// Output: ["JS_TAG", "NODE_TAG", "REACT_TAG"]

```

---

## ⚙️ Challenge 2: Active User Filter

### 📝 Task

Extract a targeted array subset from an array of user objects based on their operational status.

### 📥 Target Dataset

```js
const corporateAccounts = [
  { id: 1, active: true, department: "Ops" },
  { id: 2, active: false, department: "Dev" },
  { id: 3, active: true, department: "Exec" }
];

```

### ⚙️ Implementation Requirements

* Use `.filter()` to return an array containing only user objects where `active` matches `true`.

---

## ⚙️ Challenge 3: Frequency Builder

### 📝 Task

Build a data aggregation system using `.reduce()` to count item frequencies across a raw array stream.

### 📥 Input Data Stream

```js
const letterStream = ["x", "y", "x", "z", "x", "y"];

```

### ✅ Expected Output Match

```js
console.log(frequencyMap);
// Output: { x: 3, y: 2, z: 1 }

```

---

## 🧠 Debug Task: Reduce Failure

### ❌ Broken Implementation

A developer wants to sum an array of numbers using `.reduce()`, but the code returns `undefined` right after the first loop iteration:

```js
const totalValue = [1, 2, 3].reduce((acc, n) => {
  // ERROR: The total state tracking is lost here
  acc + n;
}, 0);

console.log(totalValue); // Output: undefined

```

### 🛠️ Execution Analysis & Fix

1. **Identify the Root Cause:** Explain why this block returns `undefined` based on how block curly braces handle return values.
2. **Refactor the Code:** Fix the block structure to maintain the accumulated value across all iterations.

---

## 🚀 Extension: Analytics Engine

### 📝 Task

Build a pure, fluent data cleanup and processing pipeline that chains three functional array operations together.

```
[Raw Array] ──► .filter(Drop Falsy) ──► .map(Square Numbers) ──► .reduce(Sum Total) ──► Scalar Result

```

### ⚙️ Constraints

* **Step 1:** Strip out all falsy values (`0`, `null`, `undefined`, `false`).
* **Step 2:** Square each remaining number (`n  2`).
* **Step 3:** Calculate and return the total sum of the squared numbers.
* **Syntax Rule:** Write the entire solution as a continuous, readable method chain.

---

# 🟦 MODULE 5: Advanced Data Structures Workbook

## 🧩 Drill 1: Map Behavior

### 📝 Task

Analyze the lookup operations on this Map collection. Predict the final console output value and explain the underlying reference evaluation rules.

```js
const databaseMap = new Map();
databaseMap.set({ a: 1 }, "Authorized_Token");

console.log(databaseMap.get({ a: 1 })); // Will this return "Authorized_Token" or undefined? Why?

```

---

## ⚙️ Challenge 1: Session Tracker

### 📝 Task

Build a lightweight system session tracker module using a JavaScript `Map` instance.

### ⚙️ Implementation Requirements

* Create an operational engine that exposes two methods: `registerSession(userId, timestamp)` and `getSessionTime(userId)`.
* **Constraint:** The system must accept complex object references as keys, ensuring lookup keys don't get accidentally coerced into strings.

---

## ⚙️ Challenge 2: Unique Tracker

### 📝 Task

Build a deduplication pipeline that extracts distinct tags out of a raw data collection and counts their occurrences.

### 📥 Input Data Array

```js
const rawTags = ["a", "b", "a", "c", "b"];

```

### ⚙️ Implementation Requirements

* Use a `Set` to instantly find all unique strings in the input array.
* Use a separate `Map` to calculate and store the occurrence counts for each unique string.

---

## ⚙️ Challenge 3: Symbol Isolation

### 📝 Task

Protect critical system properties on an object from accidental modification by hiding them behind an isolated Symbol key.

### ⚙️ Implementation Requirements

* Create an object named `secureProfile`.
* Generate an internal tracking ID using `Symbol("hidden_id")`.
* Store a value under this Symbol key on the object. Verify that the hidden key does not show up during standard property evaluations like `for...in` loops or `Object.keys()`.

---

## 🧠 Debug Task: Set Confusion

### ❌ Broken Implementation

A script tries to enforce unique entries by adding items to a collection, but it contains duplicate object shapes at runtime:

```js
const collectionSet = new Set([1, 2, 2, 3]);
collectionSet.add({ id: 101 });
collectionSet.add({ id: 101 });

console.log(collectionSet.size); // The count is higher than the developer expected!

```

### 🛠️ Execution Analysis & Fix

Explain why the primitives are successfully deduplicated while the two identical object shapes are both kept inside the collection.

---

## 🚀 Extension: Hybrid Registry System

### 📝 Task

Design a data storage registry that combines the strengths of multiple data structures:

* Use a **Set** to keep a unique list of registration keys.
* Use a **Map** to connect those keys to dynamic, metadata records.
* Expose a `.exportSnapshot()` method that converts the internal data structures and outputs them as a clean, standard JavaScript object literal.

---

# 🧠 FINAL CAPSTONE WORKBOOK

## Problem: Mini Event Pipeline Engine

### 📝 Architectural Design

Build a lightweight event processing engine that cleans, transforms, and groups incoming system event arrays into structured metric summaries.

```
                  ┌───────────────────────────────┐
                  │ ["login", "logout", "login",  │
                  │   "error", "login"]           │
                  └───────────────┬───────────────┘
                                  │
                                  ▼
                    [ .filter() (Drop "error") ]
                                  │
                                  ▼
                  [ .map() (Force UPPERCASE) ]
                                  │
                                  ▼
                   [ .reduce() (Compile Counts) ]
                                  │
                                  ▼
                  ┌───────────────────────────────┐
                  │    { LOGIN: 3, LOGOUT: 1 }    │
                  └───────────────────────────────┘

```

### ⚙️ System Requirements

1. **Sanitize:** Filter out any events with the value `"error"`.
2. **Normalize:** Transform the remaining event strings to uppercase.
3. **Aggregate:** Count the occurrences of each event string using a single `.reduce()` pipeline stage.
4. **Syntax Rule:** The entire processing pipeline must be written as a continuous, readable method chain.

### 📥 Test Input Data Array

```js
const rawSystemEvents = ["login", "logout", "login", "error", "login"];

```

### ✅ Expected Output Match

```js
console.log(processedEventSummary);
// Output: { LOGIN: 3, LOGOUT: 1 }

```

---

# 📊 INSTRUCTOR EVALUATION & SANDBOX IMPLEMENTATION

---

## 🧭 Instructor Marking Rubric System

Use this grading rubric to evaluate challenge submissions and assign scores across four core performance categories.

| Criteria | 🛑 Needs Work (0-1 pts) | 🟡 Proficient (2-3 pts) | 🟢 Advanced Mastery (4-5 pts) |
| --- | --- | --- | --- |
| **Immutability & State Safety** | Code frequently mutates arguments and base references directly. | Uses spread syntax correctly, but occasional shallow-copy referencing errors occur. | Keeps all data structures perfectly immutable. Code causes zero side effects. |
| **Pipeline Architecture** | Relies on manual loops (`for/while`) to process and modify array elements. | Uses array methods like `.map()` and `.filter()`, but writes them as separate, disconnected steps. | Chains methods together cleanly (`filter().map().reduce()`) into unified, readable pipelines. |
| **Destructuring Contracts** | Uses verbose dot-notation lookup paths. Missing properties crash the program. | Uses basic destructuring patterns, but aliasing and fallback safety defaults are missing. | Uses advanced, safe destructuring patterns along with clean aliasing and reliable fallbacks. |
| **Structure Optimization** | Uses plain objects for all associative lookups, causing string coercion bugs. | Integrates `Map` and `Set` collections correctly, but struggles with reference-equality lookup edge cases. | Uses `Map`, `Set`, and `Symbol` collections appropriately based on their performance advantages. |

---

## 💻 Interactive Coding Sandbox Version

This self-contained React application provides an interactive playground for this workbook. It features built-in test evaluation runners that automatically grade user solutions against module challenges in real time.

```jsx
import React, { useState } from 'react';
import { Play, CheckCircle, AlertCircle, RefreshCw } from 'lucide-react';

export default function WorkbookSandbox() {
  const [activeTab, setActiveTab] = useState('mod1');
  const [userCode, setUserCode] = useState({
    mod1: `// Challenge 1: Write your generateTelemetryReport function here\nconst generateTelemetryReport = (user, action, count) => {\n  return \`\`; \n};`,
    mod2: `// Challenge 1: Write your safelyUpdateConfig function here\nconst safelyUpdateConfig = (config) => {\n  return {};\n};`
  });
  const [testResults, setTestResults] = useState({ mod1: null, mod2: null });

  const challengeSpecs = {
    mod1: {
      title: "Module 1 - Dynamic Message Builder Test",
      runTest: (codeString) => {
        try {
          const evalContext = new Function(`${codeString}; return generateTelemetryReport;`)();
          const sampleOutput = evalContext("Sean", "API_REQUEST", 3);
          const matchTarget = "User Sean performed 3 actions today. Next milestone: 8 actions.";
          if (sampleOutput === matchTarget) {
            return { success: true, message: "Perfect! Template literals evaluated correctly." };
          }
          return { success: false, message: `Output Mismatch. Received: "${sampleOutput}"` };
        } catch (err) {
          return { success: false, message: `Runtime Compilation Error: ${err.message}` };
        }
      }
    },
    mod2: {
      title: "Module 2 - Immutable Updater Test",
      runTest: (codeString) => {
        try {
          const evalContext = new Function(`${codeString}; return safelyUpdateConfig;`)();
          const original = { theme: "dark", layout: "grid" };
          const result = evalContext(original);
          if (original.theme === "dark" && result?.theme === "light") {
            return { success: true, message: "Excellent! Config updated immutably without altering the source." };
          }
          return { success: false, message: "State Safety Failure: Original config mutated or wrong output values." };
        } catch (err) {
          return { success: false, message: `Runtime Compilation Error: ${err.message}` };
        }
      }
    }
  };

  const handleRunEvaluation = (moduleId) => {
    const outcome = challengeSpecs[moduleId].runTest(userCode[moduleId]);
    setTestResults(prev => ({ ...prev, [moduleId]: outcome }));
  };

  return (
    <div style={{ maxWidth: '1100px', margin: '30px auto', fontFamily: 'system-ui, sans-serif', padding: '0 20px' }}>
      <div style={{ borderBottom: '2px solid #e2e8f0', paddingBottom: '15px', marginBottom: '25px' }}>
        <h2 style={{ color: '#1e293b', margin: '0 0 5px 0' }}>💻 ES6+ Integrated Learning Sandbox</h2>
        <p style={{ color: '#64748b', margin: 0 }}>Implement your solutions, evaluate assignments, and track test coverage in real time.</p>
      </div>

      <div style={{ display: 'flex', gap: '10px', marginBottom: '20px' }}>
        <button 
          onClick={() => setActiveTab('mod1')}
          style={{ padding: '10px 18px', borderRadius: '6px', border: 'none', cursor: 'pointer', fontWeight: '6px', backgroundColor: activeTab === 'mod1' ? '#2563eb' : '#e2e8f0', color: activeTab === 'mod1' ? '#fff' : '#475569' }}
        >
          Module 1 Challenge
        </button>
        <button 
          onClick={() => setActiveTab('mod2')}
          style={{ padding: '10px 18px', borderRadius: '6px', border: 'none', cursor: 'pointer', fontWeight: '6px', backgroundColor: activeTab === 'mod2' ? '#2563eb' : '#e2e8f0', color: activeTab === 'mod2' ? '#fff' : '#475569' }}
        >
          Module 2 Challenge
        </button>
      </div>

      <div style={{ display: 'grid', gridTemplateColumns: '1fr 1fr', gap: '25px' }}>
        <div>
          <h4 style={{ color: '#334155', marginBottom: '10px' }}>📝 Live Source Workarea</h4>
          <textarea
            value={userCode[activeTab]}
            onChange={(e) => setUserCode(prev => ({ ...prev, [activeTab]: e.target.value }))}
            style={{ width: '100%', height: '340px', fontFamily: 'monospace', fontSize: '14px', padding: '15px', borderRadius: '8px', border: '1px solid #cbd5e1', backgroundColor: '#0f172a', color: '#38bdf8', lineHeight: '1.5' }}
          />
          <button
            onClick={() => handleRunEvaluation(activeTab)}
            style={{ marginTop: '12px', display: 'flex', alignItems: 'center', gap: '8px', padding: '12px 24px', backgroundColor: '#16a34a', color: '#fff', border: 'none', borderRadius: '6px', fontWeight: 'bold', cursor: 'pointer', transition: 'background-color 0.2s' }}
          >
            <Play size={16} /> Evaluate Solution
          </button>
        </div>

        <div>
          <h4 style={{ color: '#334155', marginBottom: '10px' }}>📊 Unit Test Validation Terminal</h4>
          <div style={{ padding: '20px', borderRadius: '8px', backgroundColor: '#f8fafc', border: '1px solid #e2e8f0', height: '340px', boxSizing: 'border-box' }}>
            <h5 style={{ margin: '0 0 15px 0', color: '#475569', fontSize: '15px' }}>{challengeSpecs[activeTab].title}</h5>
            
            {testResults[activeTab] ? (
              <div style={{ display: 'flex', alignItems: 'flex-start', gap: '12px', padding: '15px', borderRadius: '6px', backgroundColor: testResults[activeTab].success ? '#f0fdf4' : '#fef2f2', border: `1px solid ${testResults[activeTab].success ? '#bbf7d0' : '#fecaca'}` }}>
                {testResults[activeTab].success ? <CheckCircle color="#16a34a" size={24} style={{ flexShrink: 0 }} /> : <AlertCircle color="#dc2626" size={24} style={{ flexShrink: 0 }} />}
                <div>
                  <h6 style={{ margin: '0 0 4px 0', fontSize: '14px', color: testResults[activeTab].success ? '#15803d' : '#991b1b' }}>
                    {testResults[activeTab].success ? "Passed Evaluation Metric" : "Validation Deficit"}
                  </h6>
                  <p style={{ margin: 0, fontSize: '13px', fontFamily: 'monospace', color: '#334155' }}>{testResults[activeTab].message}</p>
                </div>
              </div>
            ) : (
              <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', height: '80%', color: '#94a3b8' }}>
                <RefreshCw size={36} style={{ marginBottom: '10px', animation: 'spin 4s linear infinite' }} />
                <p style={{ fontSize: '13px', margin: 0 }}>Awaiting submission code execution input parameters...</p>
              </div>
            )}
          </div>
        </div>
      </div>
    </div>
  );
}

```

---

# 🧭 END OF CODING WORKBOOK SHEET
