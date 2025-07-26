# JavaScript Array Methods Cheat Sheet

This README summarizes key differences and use cases for some commonly used JavaScript array methods: `find()`, `filter()`, `map()`, and `forEach()`.

---

## `find()`

- Returns the **first** element in an array that satisfies a given condition.
- If no element matches, returns `undefined`.
- Stops searching after finding the first match.

**Use case:** When you need to locate a single element meeting a condition.

---

## `filter()`

- Returns a **new array** containing **all** elements that satisfy a given condition.
- Returns an empty array if no elements match.
- Checks the entire array before returning results.

**Use case:** When you need to find all elements matching a condition.

---

## `map()`

- Loops through an array and returns a **new array** with transformed elements.
- Does **not** modify the original array.

**Use case:** When you want to create a new array with modified values from the original array.

---

## `forEach()`

- Loops through an array and executes a function on each element.
- Does **not** return a new array.
- Mainly used for side effects like logging or making API calls.

**Use case:** When you want to perform an action on each element without creating a new array.

---

## Summary Table

| Method    | Returns                  | Stops After First Match? | Modifies Original Array? | Use Case                       |
|-----------|--------------------------|-------------------------|-------------------------|-------------------------------|
| `find()`  | First matching element or `undefined` | Yes                     | No                      | Find single element            |
| `filter()`| New array of all matches | No                      | No                      | Find multiple elements         |
| `map()`   | New array of transformed elements | No                      | No                      | Transform elements into new array |
| `forEach()`| `undefined` (void)       | No                      | No                      | Perform side effects           |

---

*Created by Muhammad Jareer — Full Stack Developer*

---

