## 📘 What is Memorization?

**Memorization** is like keeping a notebook of answers to questions you've already solved.  
Next time you need the answer, you just look it up instead of solving it again!

---

## 🔧 How Memorization Works

1. Call a function (ask a question)
2. Check if the answer is already in your "memory book" (cache)
3. If it is:
   - ✅ Return the cached answer
4. If it isn't:
   - 🧠 Solve the problem
   - 📝 Save the answer in your cache
   - 🔁 Return the result

---

## 💡 Code Example

```javascript
const memoryBook = {};

function memorizedAdd(a, b) {
  const key = `${a},${b}`;
  if (memoryBook[key]) {
    return memoryBook[key]; // returning cached result
  }
  const result = a + b;
  memoryBook[key] = result; // storing result
  return result;
}
```

Without memorization, this function would recalculate every time it's called.  
With memorization, it checks and returns the stored result instead.

---

## ✅ Benefits of Memorization

- ⚡ Faster Code Execution
- 🧠 More Efficient Resource Usage
- 🛠 Easier to Maintain and Scale

⏱ **Performance Comparison**  
- Before Memorization: 10 seconds  
- After Memorization: 1 second  

---

## 🧠 Tips for Effective Memorization

- Use a dedicated cache object
- Choose the appropriate cache size  
  `const cacheSize = 100`
- Implement cache invalidation when needed

---

## 📌 Conclusion

Memorization is a **simple yet powerful** technique to optimize your JavaScript code.