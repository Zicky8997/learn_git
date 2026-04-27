### **Chapter 2: Meaningful Names**

Good naming is one of the most underrated skills in programming. When you name a variable, function, or class well, you're essentially telling a story — anyone reading your code should immediately understand *why* something exists, *what* it does, and *how* it's used, no comment needed.

A few things to watch out for: don't use names that carry a different meaning than what you intend, and be consistent with your spelling. Avoid filler words like *ProductInfo* vs. *ProductData* — they sound different but mean the same thing, which just creates confusion. Pick names you can actually say out loud and search for; it makes talking through code with teammates and tracking down bugs much easier. As a general rule, classes should read like nouns (*Customer*, *Account*), and methods like verbs (*postPayment*, *save*).

---

### **Chapter 3: Functions**

Think of functions as the building blocks of your program's story. The golden rule: keep them small and make sure each one does exactly *one thing*. When a function tries to do too much, it becomes a nightmare to name, test, and reason about.

Every line inside a function should operate at the same level of detail — don't mix big-picture logic with low-level string manipulation in the same breath. Arguments are a necessary evil; zero is ideal, and anything beyond three is a red flag. Also, a function should either *do* something or *answer* something — not both. And when things go wrong, throw exceptions rather than returning error codes; it keeps your main logic clean and readable.

---

### **Chapter 4: Comments**

Here's a slightly uncomfortable truth: most comments are a sign that the code itself isn't clear enough. Comments don't get updated when code changes, so they go stale and start lying to you. The real goal is to write code so expressive that comments become unnecessary.

That said, some comments are genuinely useful — legal headers, notes on why you made a weird design decision, or TODOs for future work. What you should avoid: comments that just repeat what the code already says, notes to yourself that mean nothing to anyone else, and above all, commented-out code. Delete it. That's what version control is for.

---

### **Chapter 6: Objects and Data Structures**

Objects and data structures serve opposite purposes, and mixing them up causes real headaches. Objects *hide* their data and expose behavior — you tell them what to do. Data structures *expose* their data and don't really *do* anything. Neither is universally better; the right choice depends on whether you're more likely to add new types or new behaviors down the road.

A well-designed class shouldn't just wrap fields in getters and setters — it should give you a clean, abstract way to work with the underlying data without exposing the implementation details. Along the same lines, try not to chain long sequences of method calls like `a.getB().getC().doSomething()` — it's brittle and hard to follow. Tell objects what to do, don't interrogate them. Finally, Data Transfer Objects (DTOs) — simple structs with public fields and no logic — are perfectly valid for things like database communication or parsing incoming messages.
