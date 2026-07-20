# Moglix Online Assessment

## Problem

Given a string containing only '(' and ')', determine the length of the longest valid (well-formed) parentheses substring.

---

## Solution

The implemented solution uses a **stack-based approach**.

### Algorithm

1. Initialize a stack and push `-1` as the base index.
2. Traverse the string from left to right.
3. For every `'('`, push its index onto the stack.
4. For every `')'`:
   - Pop the top element.
   - If the stack becomes empty, push the current index.
   - Otherwise, calculate the length of the current valid substring using:
     ```
     currentLength = currentIndex - stack.top()
     ```
   - Update the maximum length.

---

## Complexity Analysis

| Metric | Complexity |
|---------|------------|
| Time | **O(n)** |
| Space | **O(n)** |

---

## Alternative Approaches

- Dynamic Programming — **O(n)** Time, **O(n)** Space
- Two-Pass Traversal — **O(n)** Time, **O(1)** Space

---

## Language

C++17
