# Time Complexity Analysis

## Selected Data Structure: Stack 

### Operations Overview

| Operation | Time Complexity | Explanation |
|-----------|-----------------|-------------|
| push()    | O(1)            | Adding an item to the top is constant time. |
| pop()     | O(1)            | Removing the top item is constant time. |
| peek()    | O(1)            | Viewing the most recent element takes no extra work. |
| is_empty()| O(1)            | A quick check of whether the stack has elements. |
| size()    | O(1)            | Retrieving the count of elements is instantaneous. |

### Practical Use Case in Enterprise Systems

**Scenario:** Browser Back Navigation

When navigating between websites:
1. push("google.com") → Stack: ["google.com"]
2. push("youtube.com") → Stack: ["google.com", "youtube.com"]
3. push("github.com") → Stack: ["google.com", "youtube.com", "github.com"]
4. pop() → returns "github.com" (navigate back) → Stack: ["google.com", "youtube.com"]
5. pop() → returns "youtube.com" (navigate back again) → Stack: ["google.com"]

**Why the stack works well:**  
- Last visited site is always the first one to return to (LIFO principle).  
- Consistent O(1) performance keeps browsing fast and responsive.  
- Intuitive design makes it reliable for session tracking.  

### Space Complexity
- **Memory usage:** O(n), where *n* is the number of stored pages.  
- **Reasoning:** Each visited page is added as a separate entry, so space grows linearly with activity.  

---

## Reflection Questions

### 1. How does your implementation compare to Python's built-in `list`?  
My Stack restricts operations to only those relevant for LIFO, reducing mistakes like inserting at the wrong position. In contrast, Python’s list is more flexible but less focused.

### 2. What trade-offs did you make between simplicity and performance?  
I prioritized clarity and maintainability. While a linked list could save on resizing costs, my approach using Python lists is easier to read and debug for beginners.

### 3. When would you choose your data structure over alternatives?  
Stacks are the right fit whenever the order of reversal matters—undo buttons, recursive algorithms, or parsing expressions. For queue-like tasks or random lookups, other structures are better.

### 4. What enterprise scenarios would benefit most?  
- Customer support systems: track escalation steps to roll back changes.  
- Cloud services: manage nested function calls or task scheduling.  
- Compiler design: evaluate expressions and balance symbols.  
- Logistics software: manage packaging or container unloading order.  
