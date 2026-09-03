## Cross Interview 🗣️

As practice has shown, quality interview preparation is 80% of success. Therefore, the goal of this assignment is to 
help you improve your preparation.

## Task Objectives 🎯

- Gain practical interview experience from both sides
- Practice technical topics(e.g [interview-topics](<./interview-topics.md>)) and communication skills
- Help each other identify knowledge gaps
- Build confidence before the actual technical screening

## Interview Process 🔄

The cross-interview process will be similar to cross-check. Each student will receive names of people they should 
interview, which means you will also go through 5 interviews yourself. The interviewer should contact you to schedule 
the meeting.

Submit deadline your contact information **April, 1**.
Interviews take place from **April, 2 to April, 20**.
Interview language is **English**.

## Process 📝

1. Create an MD file with your contact information so people can reach you
2. Create a Pull Request containing this file
3. Add the link to the Pull Request in the cross-submit form

## Interview Topics 📚

### Pay attention: the candidate is not expected to answer all questions! The main purpose is to check the level and help each other learn.

<details>
<summary><strong>Click to expand: JavaScript Basics</strong></summary>

### JavaScript Basics

- **Data Types**
  - Primitives vs Objects
  - Type checking (typeof, instanceof)
  - Type conversions, == vs === (practical tasks)

- **Variables**
  - var vs let vs const
  - Hoisting
  - Temporal Dead Zone
  - Scope (global, function, block)

- **Operators**
  - Ternary operator
  - Nullish Coalescing (??)
  - Optional Chaining (?.)
  - Logical Operators (&&, ||, !)
  - Practical tasks with operators

- **Loops**
  - for, while, do while
  - for...of vs for...in
  - break and continue
  - Loop performance considerations

- **Arrays**
  - Creation and initialization
  - Most popular methods:
    - map vs forEach
    - filter vs find
    - sort, toSorted (node 20)
    - reduce
    - pop/push, shift/unshift
    - slice, splice
    - includes, indexOf
  - Mutating vs non-mutating methods
  - Array vs Set
  - Spread operator with arrays

- **Objects**
  - Object creation and initialization
  - How to get keys/values (Object.keys, values, entries)
  - How to copy objects:
    - Shallow copy: {...obj}, Object.assign
    - Deep copy: JSON.parse/stringify, structuredClone, using loops
  - Destructuring (practical tasks)
  - Computed property names
  - Object.freeze, Object.seal
  - Getter/setter (optional)
  - Object vs Map
  - Spread operator with objects

- **Functions**
  - Declaration vs Expression vs Arrow functions
  - Default parameters
  - Rest operator and arguments
  - 'this' keyword and context
  - Call vs Apply vs Bind
  - IIFE (Immediately Invoked Function Expression)
  - Closures
  - Higher-order functions
  - Callback functions

- **Classes**
  - Constructor
  - Public vs Private fields and methods (#)
  - Static methods and properties
  - Inheritance (extends)
  - super keyword
  - Getters and setters in classes

- **Asynchronous JavaScript**
  - Callbacks
  - Promise and its methods:
    - then, catch, finally
    - Promise.all, Promise.race
    - Promise.allSettled, Promise.any
  - Promises vs async/await
  - Error handling (try/catch/finally)
  - Event Loop (high level understanding)
  - Microtasks vs Macrotasks (optional)

- **Error Handling**
  - try/catch/finally
  - throw
  - Error types
  - Custom errors

- **Advanced Topics (Optional)**
  - Prototypes and prototypal inheritance
  - Symbol
  - Generators and iterators
  - WeakMap and WeakSet
  - Proxy and Reflect

</details>

<details>
<summary><strong>Click to expand: TypeScript Basics</strong></summary>

### TypeScript Basics

- **Types**
  - Primitive types (string, number, boolean, null, undefined, symbol, bigint)
  - Array types (number[], Array<number>)
  - Tuple types
  - Enum
  - Any, unknown, never, void
  - Type vs Interface

- **Type Annotations**
  - Variable type annotations
  - Function parameter and return type annotations
  - Optional parameters (?)
  - Default parameters

- **Interfaces**
  - Interface declaration
  - Optional properties
  - Readonly properties
  - Extending interfaces
  - Interface vs Type alias

- **Type Aliases**
  - Creating type aliases
  - Union types (|)
  - Intersection types (&)
  - Literal types

- **Functions in TypeScript**
  - Function type expressions
  - Call signatures
  - Optional and default parameters
  - Rest parameters with types
  - Function overloading

- **Classes in TypeScript**
  - Class properties and methods typing
  - Access modifiers (public, private, protected)
  - Readonly properties
  - Implementing interfaces
  - Abstract classes and methods

- **Generics**
  - Generic functions
  - Generic interfaces
  - Generic classes
  - Generic constraints
  - Using type parameters in generic constraints

- **Type Assertions**
  - as syntax
  - Angle-bracket syntax
  - Non-null assertion operator (!)

- **Advanced Types (Optional)**
  - Utility types (Partial, Required, Readonly, Pick, Omit, Record)
  - Mapped types
  - Conditional types
  - Type guards (typeof, instanceof, in)
  - Discriminated unions

</details>

<details>
<summary><strong>Click to expand: HTML/CSS Basics</strong></summary>

### HTML/CSS Basics

- **Selectors**
  - Selector types (element, class, id, attribute)
  - Selector specificity and weights
  - Combinator selectors (descendant, child, sibling)

- **Pseudo-classes and Pseudo-elements**
  - Common pseudo-classes (:hover, :focus, :nth-child, etc.)
  - Pseudo-elements (::before, ::after, ::first-letter, etc.)

- **CSS Units**
  - Absolute units (px)
  - Relative units (em, rem, %, vh, vw)
  - em vs rem

- **Layout**
  - Box model (margin, border, padding, content)
  - Display property (block, inline, inline-block, none)
  - Position property (static, relative, absolute, fixed, sticky)
  - FlexBox:
    - flex-direction, justify-content, align-items
    - flex-wrap, flex-grow, flex-shrink, flex-basis
  - Grid:
    - grid-template-columns, grid-template-rows
    - gap, grid-area
    - auto-fill vs auto-fit

- **Responsive Design**
  - Media queries
  - Mobile-first vs Desktop-first approach
  - Viewport meta tag

</details>

<details>
<summary><strong>Click to expand: Client Side (Browser APIs)</strong></summary>

### Client Side (Browser APIs)

- **Global Object Window**
  - document
  - location
  - history
  - navigator
  - localStorage/sessionStorage
  - cookies (optional)

- **DOM Manipulation**
  - Selection methods:
    - getElementById vs getElementsByClassName vs getElementsByTagName
    - querySelector vs querySelectorAll
  - Creating elements (createElement, createTextNode)
  - Inserting elements (append, appendChild, insertBefore, insertAdjacentHTML)
  - Removing elements (remove, removeChild)
  - HTML attributes (getAttribute, setAttribute, dataset)
  - classList (add, remove, toggle, contains)
  - Traversing DOM:
    - children vs childNodes
    - firstChild vs firstElementChild
    - nextSibling vs nextElementSibling
    - parentNode vs parentElement

- **Event Handling**
  - addEventListener vs on[Event]
  - Event object
  - preventDefault vs stopPropagation vs stopImmediatePropagation
  - Event phases (capturing, target, bubbling)
  - Event delegation
  - target vs currentTarget
  - Common events (click, input, change, submit, keydown, etc.)

- **Web Storage**
  - localStorage vs sessionStorage
  - Methods: setItem, getItem, removeItem, clear
  - Storage limitations
  - Storage events

- **Forms (Optional)**
  - Form validation
  - FormData API
  - Input types

</details>

## Live Coding Section 💻

**Important**: At least 15 minutes of the interview should be dedicated to live coding. This practical part helps assess 
the candidate's ability to apply JavaScript and TypeScript fundamentals in real problem-solving scenarios.

### Guidelines for Interviewers:

1. **Preparation**: Prepare 2-3 coding tasks before the interview
2. **Self-solve**: Solve all tasks yourself beforehand to understand potential solutions and common pitfalls
3. **Guidance**: Be ready to guide the student in the right direction if they get stuck
4. **Tool**: Use [https://codeshare.io/](https://codeshare.io/) for real-time collaborative coding 
5. **Observation**: Pay attention to:
   - Problem-solving approach
   - Code structure and readability
   - Use of appropriate methods and syntax
   - Debugging skills
   - Communication while coding

### Guidelines for Interviewees:

1. **Think aloud**: Explain your thought process as you code
2. **Ask questions**: Clarify requirements if something is unclear
3. **Start simple**: Begin with a basic solution, then optimize if needed
4. **Test your code**: Walk through your solution with example inputs
5. **Don't panic**: It's okay to make mistakes - focus on problem-solving approach

### Examples of Coding Tasks 📝

Choose 2-3 tasks based on the candidate's level and time available. Tasks are organized by difficulty.

<details>
<summary><strong>Click to expand: Easy Level Tasks (5 tasks)</strong></summary>

#### Easy Level

**1. Sum of Array Elements**
```
Write a function that takes an array of numbers and returns their sum.
Example: sumArray([1, 2, 3, 4]) → 10
```

**2. Reverse a String**
```
Write a function that reverses a string without using built-in reverse method.
Example: reverseString("hello") → "olleh"
```

**3. Find Maximum Number**
```
Write a function that finds the largest number in an array without using Math.max.
Example: findMax([3, 7, 2, 9, 1]) → 9
```

**4. Count Vowels**
```
Write a function that counts the number of vowels (a, e, i, o, u) in a string.
Example: countVowels("hello world") → 3
```

**5. Palindrome Checker**
```
Write a function that checks if a string is a palindrome (reads the same forwards and backwards).
Example: isPalindrome("racecar") → true, isPalindrome("hello") → false
```

</details>

<details>
<summary><strong>Click to expand: Medium Level Tasks (5 tasks)</strong></summary>

#### Medium Level

**6. Remove Duplicates**
```
Write a function that removes duplicate values from an array.
Example: removeDuplicates([1, 2, 2, 3, 4, 4, 5]) → [1, 2, 3, 4, 5]
```

**7. FizzBuzz**
```
Write a function that prints numbers from 1 to n. For multiples of 3, print "Fizz" 
instead of the number, for multiples of 5 print "Buzz", and for multiples of both print "FizzBuzz".
Example: fizzBuzz(15) → [1, 2, "Fizz", 4, "Buzz", "Fizz", 7, 8, "Fizz", "Buzz", 11, "Fizz", 13, 14, "FizzBuzz"]
```

**8. Flatten Array**
```
Write a function that flattens a nested array one level deep.
Example: flattenArray([1, [2, 3], [4, [5]]]) → [1, 2, 3, 4, [5]]
```

**9. Object Property Counter**
```
Write a function that counts how many times each element appears in an array and returns an object.
Example: countOccurrences(['a', 'b', 'a', 'c', 'b', 'a']) → {a: 3, b: 2, c: 1}
```

**10. Capitalize Words**
```
Write a function that capitalizes the first letter of each word in a sentence.
Example: capitalizeWords("hello world from javascript") → "Hello World From Javascript"
```

</details>

<details>
<summary><strong>Click to expand: Advanced Level Tasks (5 tasks)</strong></summary>

#### Advanced Level

**11. Debounce Function**
```
Implement a debounce function that delays the execution of a function until after 
a specified time has elapsed since the last time it was invoked.
Example usage: 
const debouncedFn = debounce(() => console.log('Hello'), 1000);
debouncedFn(); // Will execute after 1 second if not called again
```

**12. Deep Clone Object**
```
Write a function that creates a deep copy of an object (including nested objects and arrays).
Example: 
const original = {a: 1, b: {c: 2}};
const copy = deepClone(original);
copy.b.c = 3;
console.log(original.b.c); // Should still be 2
```

**13. Group By Property**
```
Write a function that groups an array of objects by a specified property.
Example: 
groupBy([
  {name: 'John', age: 25},
  {name: 'Jane', age: 25},
  {name: 'Bob', age: 30}
], 'age')
→ {
  25: [{name: 'John', age: 25}, {name: 'Jane', age: 25}],
  30: [{name: 'Bob', age: 30}]
}
```

**14. Promise Chain**
```
Create a function that takes an array of URLs and fetches them sequentially (one after another),
not in parallel. Return an array of results.
Hint: Use Promise chaining or async/await.
```

**15. Custom Array Method**
```
Implement your own version of Array.prototype.map() without using the built-in map method.
Your function should work exactly like the original map method.
Example: 
customMap([1, 2, 3], x => x * 2) → [2, 4, 6]
```

</details>

<details>
<summary><strong>Click to expand: TypeScript Specific Tasks (Optional)</strong></summary>

**TypeScript Task 1: Type-Safe Function**
```
Create a function that takes an array of objects with name and age properties.
The function should return only the names of people older than 18.
Add proper TypeScript types for all parameters and return values.
```

**TypeScript Task 2: Generic Function**
```
Create a generic function that takes an array and returns the first element.
If the array is empty, it should return undefined.
Add proper type annotations so TypeScript knows the return type.
```

</details>

### Tips for Successful Live Coding:

- **Start with easier tasks** to build confidence
- **Allow time for thinking** - don't rush the candidate
- **Provide hints** if stuck for more than 2-3 minutes
- **Discuss alternative solutions** after completing a task
- **Focus on understanding**, not perfect syntax
- **Consider edge cases** together (empty arrays, null values, etc.)

### Required:
- MD file with contact information created
- Pull Request created and submitted
- Conducted 5 interviews with other students
- Participated in 5 interviews as interviewee
- **For Interviewers**: Recorded each interview and submitted recording links in the feedback form

### Recommendations for Interviewers:
- **Record the interview session** and keep the recording accessible for at least 2 weeks after the deadline (April, 20).
This is important for transparency and to allow coordinators to verify the fairness of evaluations if needed.
- Submit the recording link in the feedback form after each interview
- Be respectful and supportive
- Focus on understanding, not just right/wrong answers
- Ask follow-up questions to help clarify understanding
- Provide constructive feedback
- Keep track of time (recommended 60-90 minutes per interview)
- Document areas where the candidate excelled and areas for improvement

### Recommendations for Interviewees:
- Be on time for scheduled interviews
- Be honest if you don't know something
- Try to explain your thought process
- Ask questions if something is unclear
- Take notes on topics you need to study more
- Thank the interviewer for their time

## Contact Information File Template 📋

Create a file named `contact-info.md` with the following structure:

```markdown
# Contact Information 

**Name:** [Your Full Name]

**Discord:** [Your Discord username]

**Telegram:** [Your Telegram username] (optional)

**Email:** [Your email] (optional)

**Preferred Interview Times:**
- [e.g., Monday-Friday, 18:00-22:00 UTC+3]
- [e.g., Weekends, 10:00-20:00 UTC+3]

**Additional Notes:**
[Any additional information about your availability or preferences]
```

## Tips for Successful Interviews 💡

1. **Preparation**: Review all topics before conducting interviews
2. **Communication**: Practice explaining concepts clearly
3. **Active Listening**: Pay attention to the candidate's answers
4. **Time Management**: Allocate time wisely across different topics
5. **Feedback**: Provide constructive feedback to help each other grow
6. **Documentation**: Keep notes during interviews for your own learning
7. **Flexibility**: Adapt difficulty based on candidate's level
8. **Positive Attitude**: Create a comfortable learning environment

## Evaluation Criteria 📊

Since the goal of this task is to help students overcome their fear of interviews, learn to manage nervousness, practice
expressing their thoughts clearly on given topics, and identify their strengths and weaknesses, **there are ONLY TWO** 
possible score variants:

**1 point** - Student submitted their contact information, scheduled interview dates, attended the cross-interviews, 
and made an effort to demonstrate their skills and knowledge.

**0 points** - Student did not submit their contact information, did not attend scheduled interviews, or did not attempt
to answer at least one question during the cross-interviews.

**Task coefficient: 100** - This means the final score will be multiplied by 100.

**Note**: This task is about practice and learning, not about being perfect. The focus is on participation, effort, 
and personal growth through the interview experience. Coordinators and mentors will review the recordings and provide 
feedback when necessary to help you improve.

## FAQ ❓

**Q: What if I can't answer a question during my interview?**
A: It's okay! Be honest and use it as a learning opportunity. Note the topic and study it afterward.

**Q: How long should each interview last?**
A: Recommended duration is 60-90 minutes, but you can adjust based on mutual agreement.

**Q: What if someone doesn't contact me for an interview?**
A: Reach out to the course coordinators if you don't hear from your assigned interviewers.

**Q: Should I cover all topics in one interview?**
A: No, focus on main topics per interview. It's impossible to cover everything in detail.

**Q: Why do I need to record the interview?**
A: Recording helps coordinators verify the fairness and accuracy of evaluations. It ensures transparency and protects
both interviewer and interviewee. The recording should be kept accessible for at least 2 weeks after the deadline.

**Q: What tools can I use to record the interview?**
A: You can use Discord (with screen recording), Zoom, Google Meet, Microsoft Teams, or any other platform that allows 
video/audio recording. Make sure to inform the interviewee that the session will be recorded before starting.

Good luck with your cross-interviews! 🚀
