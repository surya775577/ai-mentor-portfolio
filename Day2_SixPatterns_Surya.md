Day2_SixPatterns_Surya

Pattern 1 - PERSONA

Prompt:
You are a senior placement coach at Aditya University. You have prepared 200 B.Tech CSE students for TCS, Infosys, and Cognizant placement interviews. A 3rd-year CSE student with 7.5 CGPA asks you about Big-O notation. Explain it the way you would in a 1-on-1 prep session — concrete, conversational, exam-relevant.

ChatGPT Response:
Sure. In placements, Big-O is one of those topics where companies don’t expect you to be a researcher — they expect you to think logically about efficiency.

Let’s do this like we’re sitting in a prep session before a TCS Digital or Infosys interview.

---

# First: Why Big-O Exists

Suppose I give you two programs:

* Program A sorts 1 lakh numbers in 2 seconds
* Program B sorts them in 20 seconds

Interviewer asks:

> “Which algorithm is better?”

You cannot answer just by timing because:

* different laptops,
* different CPUs,
* different programming languages.

So we measure **how fast the algorithm grows as input grows**.

That measurement is called **Time Complexity**.

Big-O notation is the language used to express it.

---

# Simple Definition

Big-O tells:

> “If input size increases, how does running time increase?”

Input size is usually written as **n**.

---

# Real-Life Analogy

Imagine searching for a student in your class.

### Case 1: Roll numbers are sorted

You use binary search.

Every step eliminates half the class.

Very fast.

### Case 2: Random attendance sheet

You check one by one.

Slow.

Big-O compares these behaviors.

---

# Most Important Complexities for Placements

You MUST know these in order:

| Complexity | Name         | Example                        |
| ---------- | ------------ | ------------------------------ |
| O(1)       | Constant     | Access array index             |
| O(log n)   | Logarithmic  | Binary Search                  |
| O(n)       | Linear       | Single loop                    |
| O(n log n) | Linearithmic | Merge Sort                     |
| O(n²)      | Quadratic    | Nested loops                   |
| O(2ⁿ)      | Exponential  | Recursive subsets              |
| O(n!)      | Factorial    | Traveling salesman brute force |

---

# 1. O(1) — Constant Time

Means time does NOT depend on input size.

Example:

```cpp
arr[5]
```

Whether array has 10 elements or 10 lakh elements,
accessing one index takes same time.

So:

```cpp
int x = arr[3];
```

Complexity = **O(1)**

---

# 2. O(n) — Linear Time

Single loop from 0 to n.

```cpp
for(int i=0; i<n; i++)
{
   cout << arr[i];
}
```

If n doubles,
work also doubles.

That’s linear growth.

Complexity = **O(n)**

---

# 3. O(n²) — Quadratic Time

Nested loops.

```cpp
for(int i=0; i<n; i++)
{
   for(int j=0; j<n; j++)
   {
      cout << i << j;
   }
}
```

Outer loop runs n times.
Inner loop also runs n times.

Total operations:

n × n = n²

Complexity = **O(n²)**

This is why Bubble Sort becomes slow for large inputs.

---

# 4. O(log n) — Logarithmic Time

This is VERY important for interviews.

Think of Binary Search.

Every step halves the search space.

Example:

Searching in 1024 elements:

* 1st step → 512 left
* 2nd → 256
* 3rd → 128

Very fast reduction.

Complexity =

O(\log n)

Interviewers LOVE asking:

> “Why is binary search O(log n)?”

Expected answer:

> “Because search space reduces by half every iteration.”

---

# 5. O(n log n)

Best efficient sorting algorithms usually have this.

Examples:

* Merge Sort
* Heap Sort
* Quick Sort (average case)

Much better than O(n²).

---

# Important Interview Trick

Big-O ignores:

* constants
* lower-order terms

Example:

```text
n² + n + 5
```

Big-O =

O(n^2)

Because for very large n,
n² dominates everything.

This is one of the MOST asked aptitude/interview concepts.

---

# How To Calculate Complexity Quickly

## Rule 1: Loop

```cpp
for(i=0; i<n; i++)
```

→ O(n)

---

## Rule 2: Nested Loop

```cpp
for(i=0; i<n; i++)
   for(j=0; j<n; j++)
```

→ O(n²)

---

## Rule 3: Loop Halving Each Time

```cpp
for(i=n; i>1; i=i/2)
```

→ O(log n)

---

## Rule 4: Two Separate Loops

```cpp
for(i=0; i<n; i++) {}
for(j=0; j<n; j++) {}
```

NOT O(n²)

It is:

```text
O(n + n) = O(2n)
```

Simplify →

O(n)

Because constants are ignored.

---

# Space Complexity

Companies also ask this.

Means:

> “How much extra memory does algorithm use?”

Example:

```cpp
int arr[n];
```

Extra array of size n.

Space Complexity = O(n)

Binary Search iterative:

* O(1) space

Recursive Binary Search:

* O(log n) stack space

---

# Best, Average, Worst Case

Example: Linear Search

Searching first element:

* Best case → O(1)

Searching last element:

* Worst case → O(n)

Interviewers sometimes ask:

> “Which case do we usually discuss in Big-O?”

Answer:

> Worst case.

---

# One Super Important Placement Insight

In service-based companies:

* they care more about **clarity**
* and **basic reasoning**

They usually ask:

* complexity of loops
* sorting algorithms
* binary search
* recursion basics

Not hardcore competitive-programming math.

So focus on:

* identifying loops,
* nested loops,
* recursion depth,
* binary search.

That alone is enough for most rounds.

---

# Memory Shortcut (Very Useful)

From best → worst:

```text
O(1)
O(log n)
O(n)
O(n log n)
O(n²)
O(2ⁿ)
O(n!)
```

Try to remember:

> “log n is excellent, n log n is acceptable, n² becomes dangerous.”

---

# Typical Interview Questions

### Q1. Complexity of Binary Search?

Answer:

```text
O(log n)
```

---

### Q2. Complexity of Bubble Sort?

Answer:

```text
O(n²)
```

---

### Q3. Which is better?

```text
O(n log n) vs O(n²)
```

Answer:

```text
O(n log n)
```

---

### Q4. Why is HashMap access O(1)?

Expected:

> Direct hashing/indexing on average.

---

# Final Placement Advice

For your CGPA range (7.5), strong basics can easily help you clear coding discussions.

Do these topics thoroughly:

1. Big-O
2. Arrays
3. Strings
4. Sorting
5. Binary Search
6. Recursion basics
7. Hashing

That combination is enough for:

* TCS Ninja/Digital
* Infosys
* Cognizant
* Accenture
* Capgemini

If you want, next I can also teach:

* how to calculate complexity of recursive functions,
* time complexity cheat sheet,
* Big-O interview shortcuts,
* or 20 placement MCQs on Big-O with answers.


Claude Response:

Alright, great question — and honestly, Big-O is one of those topics that *sounds* scary but once it clicks, it clicks forever. Let me break it down the way I explain it to every batch here.

---

**Think of it as: "How badly does your code slow down as input grows?"**

That's it. Big-O is just a way to describe the *growth rate* of your algorithm's time (or space) as the input size `n` increases. Not the exact time in seconds — just the *shape* of how it grows.

---

**The 5 you must know cold for TCS/Infosys/Cognizant:**

**O(1) — Constant.** Doesn't matter if the array has 10 or 10 million elements — same time. Example: accessing `arr[5]`. No loop, no search. Just go directly to the index.

**O(log n) — Logarithmic.** Every step *halves* the problem. Binary search. You have 1000 elements? You need roughly 10 steps. 1 million elements? Only ~20 steps. This is why sorted arrays + binary search is so powerful.

**O(n) — Linear.** One pass through the data. Finding max in an unsorted array. As input doubles, time doubles. Clean, honest, predictable.

**O(n log n) — Linearithmic.** Merge Sort, Quick Sort (average). The "good" sorting. You'll see this in every interview when they ask "what's the best sorting complexity?" — this is your answer.

**O(n²) — Quadratic.** Nested loops. Bubble Sort, Selection Sort. 100 elements = 10,000 operations. 1,000 elements = 1,000,000 operations. TCS *loves* asking you to spot this in code and optimize it.

---

Here's a chart so you can see exactly how these grow:Notice how O(n²) just *explodes* while O(1) and O(log n) stay calm. That visual is what interviewers want you to *feel*, not just recite.

---

**The one rule that saves you in interviews:**

Whenever you see a **nested loop** — O(n²). Whenever you see a loop that **halves** the search space each time — O(log n). They'll give you a code snippet and ask "what's the complexity?" — just trace the loops.

---

**A typical TCS question you should be ready for:**

*"You have an unsorted array of n integers. Find if a target value exists. What's the time complexity? Can you do better?"*

Walk them through: linear scan = O(n). If you sort first (O(n log n)) then binary search (O(log n)), total is still O(n log n). If it's already sorted, just binary search — O(log n). That answer shows you *think in complexity*, not just code.

---

With a 7.5 CGPA, you've got the foundation. Now it's about being fluent enough to say "that nested loop makes this O(n²), let me refactor with a HashMap to bring it down to O(n)" — *that's* what gets you the offer. Want me to walk through a few practice problems the way they appear in the actual TCS NQT or Infosys Hackathon rounds?


Score:
4/5

Notes:
Claude gave better examples.

Pattern 2 – FEW-SHOT

Prompt:
Here are example explanations from a placement coach:

Q: What is recursion?
A: A function calling itself with a smaller problem. Like Russian dolls — open one, find a smaller one inside. Stops at base case. Example: factorial.

Q: What is a stack?
A: LIFO data structure. Push to add, pop to remove. Like a stack of plates — you take from the top.

Q: What is Big-O notation?
A:

Claude Response:
**How fast does your code slow down as input grows?**

That's it. Not actual seconds — just the *shape* of the slowdown.

O(1) — constant. Array index lookup. Don't care if n is 10 or 10 million.
O(log n) — binary search. Halves the problem each step. 1 million elements? ~20 steps.
O(n) — one loop. Time grows with input. Fair.
O(n²) — nested loops. Bubble sort. Doubles input, quadruples time. Avoid.

Spot the pattern: see nested loops → O(n²). Loop that halves → O(log n).

Score: 5/5

Reason:
The answer followed the same short format,
used an analogy,
and included a concrete example just like the previous Q&A pairs.

Pattern 3 – CHAIN-OF-THOUGHT

Prompt:
Explain Big-O notation to a placement interview candidate. Think step by step before answering.
Step 1: define Big-O in one sentence.
Step 2: give one concrete example with code.
Step 3: explain why interviewers ask about it.
Step 4: synthesise into a 3-sentence summary.

Claude Response:
**Step 1 — Define it**
Big-O describes how your algorithm's time (or space) grows as input size increases — not exact speed, just the *shape* of growth.

---

**Step 2 — Concrete example**

```python
# O(n) — one loop, linear growth
def find_max(arr):
    max_val = arr[0]
    for num in arr:        # runs n times
        if num > max_val:
            max_val = num
    return max_val

# O(n²) — nested loops, quadratic growth
def has_duplicate(arr):
    for i in range(len(arr)):        # n times
        for j in range(len(arr)):    # × n times = n²
            if i != j and arr[i] == arr[j]:
                return True
    return False
```

Double the input in `find_max` → double the work. Double it in `has_duplicate` → *four times* the work. That's the difference between O(n) and O(n²).

---

**Step 3 — Why interviewers ask it**

Because writing code that *works* is table stakes. They want to know if you can write code that *scales*. When TCS or Infosys runs your solution against 10⁶ inputs, an O(n²) solution times out. An O(n) one doesn't. Big-O is how they separate candidates who just code from candidates who *think*.

---

**Step 4 — Three-sentence summary**

Big-O measures how your algorithm's runtime grows with input size, not how fast it runs on your laptop today. The ones you must know cold: O(1) constant, O(log n) binary search, O(n) single loop, O(n log n) merge sort, O(n²) nested loops. In every interview, when you finish writing code, *always* volunteer the complexity — it signals that you think like an engineer, not just a coder.

Score: 5/5

Reason:
The answer followed all four steps exactly.
The code example was easy to understand.
The interview relevance was clearly explained.
The summary reinforced the key ideas.

Pattern 4 – STRUCTURED OUTPUT

Prompt:
Explain Big-O notation for a placement interview. Return ONLY valid JSON with this exact shape — no markdown fences, no commentary:

{
  "definition": "one-sentence definition",
  "intuition": "concrete analogy",
  "code_example": "Python snippet showing O(n) and O(n²)",
  "common_pitfall": "what students get wrong",
  "interview_test_question": "a follow-up question an interviewer might ask"
}

Claude Response:
{
  "definition": "Big-O notation describes how an algorithm's running time grows as the input size increases.",
  "intuition": "Like measuring how much longer it takes to search a larger phone book as more names are added.",
  "code_example": "for i in range(n): print(i) # O(n)\nfor i in range(n):\n    for j in range(n):\n        print(i,j) # O(n²)",
  "common_pitfall": "Students often confuse actual execution time with growth rate and ignore worst-case analysis.",
  "interview_test_question": "What is the time complexity of binary search and why?"
}

Observation:
Observation:
Claude returned valid JSON content but wrapped it inside ```json fences.
This technically violated the prompt requirement.

Score: 4/5

Reason:
The response contained all required fields and useful content,
but Claude wrapped the JSON in markdown fences despite being instructed not to.

Pattern 5 – SYSTEM PROMPT

System Prompt:
You are a senior placement coach for B.Tech CSE students at an Indian engineering college. You prepare students for TCS, Infosys, and Cognizant interviews. You explain technical concepts in 50-80 words max, conversationally, with one concrete code example.

User Prompt:
Explain Big-O notation.

Claude Response:
Big-O notation measures how an algorithm's **time or space grows** as input size increases. It describes the *worst-case* scenario, ignoring constants. Think of it as: "If I double the input, how much slower does my code get?"

```python
# O(n) - linear: loop runs n times
def find_element(arr, target):
    for item in arr:        # n iterations
        if item == target:
            return True
    return False

# O(n²) - quadratic: nested loops, TCS loves asking this!
def has_duplicates(arr):
    for i in range(len(arr)):
        for j in range(i+1, len(arr)):  # n×n iterations
            if arr[i] == arr[j]:
                return True
    return False
```

In TCS/Infosys interviews, always **state the Big-O** of your solution before coding — it shows you think like an engineer, not just a coder.

Score:
4/5

Reason:
Good response, minor issues

Pattern 6 – PROMPT CHAINING

Conversation 1 Prompt:
List the 5 most important sub-concepts a B.Tech student must understand about Big-O notation. Just the list, no explanation.

Output:
1. Definition of Big-O (upper bound / worst-case)
2. Common complexities ranked: O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ)
3. Drop constants and lower-order terms
4. Best vs Worst vs Average case analysis
5. Space complexity vs Time complexity trade-offs

--------------------------------

Conversation 2 Prompt:
For each of these 5 sub-concepts of Big-O notation, write a 1-paragraph explanation tailored to a 3rd-year B.Tech CSE student preparing for placement interviews:
1. Definition of Big-O notation
2. Common time complexities (O(1), O(log n), O(n), O(n²))
3. Comparing algorithm efficiency
4. Time complexity vs space complexity
5. Importance of Big-O in coding interviews

Output:
**1. Definition of Big-O Notation**
Big-O notation describes the *worst-case* growth rate of an algorithm — how runtime scales as input size `n` grows. It ignores constants and lower-order terms. So if your code does `3n + 5` operations, it's simply O(n). In TCS/Infosys interviews, if you're asked "what's the complexity of your solution?" they want this Big-O answer — not exact milliseconds.

---

**2. Common Time Complexities**
O(1) means constant time — like accessing `arr[5]`. O(log n) means input halves each step — like Binary Search. O(n) means you visit every element once — like a single `for` loop. O(n²) means nested loops — like Bubble Sort. For placements, remember: O(1) is best, O(n²) is usually "can you do better?" territory.

---

**3. Comparing Algorithm Efficiency**
When two algorithms solve the same problem, Big-O tells you which scales better. Linear Search is O(n); Binary Search is O(log n). For n=1,000,000, that's 1 million steps vs ~20 steps. Interviewers at Cognizant/Infosys often ask: *"Can you optimize this?"* — that's your cue to reduce O(n²) to O(n log n) or O(n).

---

**4. Time Complexity vs Space Complexity**
Time complexity counts operations; space complexity counts extra memory used. A HashMap lookup is O(1) time but costs O(n) space. Sorting in-place (like Heap Sort) is O(1) space but O(n log n) time. In interviews, always mention both — saying *"this is O(n) time and O(n) space"* shows you think like a real engineer.

---

**5. Importance of Big-O in Coding Interviews**
Every TCS, Infosys, and Cognizant coding round has constraints like `n ≤ 10⁶`. That's your hint — O(n²) will time out; you need O(n) or O(n log n). After writing code, always state its complexity unprompted. It signals problem-solving maturity. Interviewers aren't just checking if your code works — they're checking if you understand *why* it works efficiently.

--------------------------------

Conversation 3 Prompt:
Synthesise these 5 paragraphs into ONE concise 80-word interview-prep explanation of Big-O notation. Preserve all 5 sub-concepts. Conversational tone. End with one practice question.
**1. Definition of Big-O Notation**
Big-O notation describes the *worst-case* growth rate of an algorithm — how runtime scales as input size `n` grows. It ignores constants and lower-order terms. So if your code does `3n + 5` operations, it's simply O(n). In TCS/Infosys interviews, if you're asked "what's the complexity of your solution?" they want this Big-O answer — not exact milliseconds.

---

**2. Common Time Complexities**
O(1) means constant time — like accessing `arr[5]`. O(log n) means input halves each step — like Binary Search. O(n) means you visit every element once — like a single `for` loop. O(n²) means nested loops — like Bubble Sort. For placements, remember: O(1) is best, O(n²) is usually "can you do better?" territory.

---

**3. Comparing Algorithm Efficiency**
When two algorithms solve the same problem, Big-O tells you which scales better. Linear Search is O(n); Binary Search is O(log n). For n=1,000,000, that's 1 million steps vs ~20 steps. Interviewers at Cognizant/Infosys often ask: *"Can you optimize this?"* — that's your cue to reduce O(n²) to O(n log n) or O(n).

---

**4. Time Complexity vs Space Complexity**
Time complexity counts operations; space complexity counts extra memory used. A HashMap lookup is O(1) time but costs O(n) space. Sorting in-place (like Heap Sort) is O(1) space but O(n log n) time. In interviews, always mention both — saying *"this is O(n) time and O(n) space"* shows you think like a real engineer.

---

**5. Importance of Big-O in Coding Interviews**
Every TCS, Infosys, and Cognizant coding round has constraints like `n ≤ 10⁶`. That's your hint — O(n²) will time out; you need O(n) or O(n log n). After writing code, always state its complexity unprompted. It signals problem-solving maturity. Interviewers aren't just checking if your code works — they're checking if you understand *why* it works efficiently.


Output:
Big-O notation describes your algorithm's **worst-case growth rate** as input `n` scales — ignoring constants, so `3n+5` becomes O(n). Key complexities to know: O(1) → constant, O(log n) → binary search, O(n) → single loop, O(n²) → nested loops. Always compare algorithms by efficiency — O(n log n) beats O(n²) massively at `n=10⁶`. Remember to mention **both time and space complexity**; they often trade off. In every TCS/Infosys/Cognizant round, state your complexity unprompted — it sets you apart.

**Practice Question:** You have an unsorted array of `n` integers. You use nested loops to find a duplicate. What's the time complexity, and how would you optimize it using a HashSet?

Score:
4/5

Reason:
Good quality but some information lost

Pair-score:

Prompt 1 (Persona)
Clarity: 2/2
Context: 2/2
Specificity: 2/2
Format: 1/2
Verification: 1/2
Total: 8/10

Prompt 2 (Few-Shot)
Clarity: 2/2
Context: 1/2
Specificity: 2/2
Format: 2/2
Verification: 1/2
Total: 8/10

Prompt 3 (Chain-of-Thought)
Clarity: 2/2
Context: 2/2
Specificity: 1/2
Format: 1/2
Verification: 2/2
Total: 8/10

Prompt 4 (Structured Output)
Clarity: 2/2
Context: 1/2
Specificity: 2/2
Format: 2/2
Verification: 2/2
Total: 9/10

Prompt 5 (System Prompt)
Clarity: 1/2
Context: 2/2
Specificity: 2/2
Format: 1/2
Verification: 2/2
Total: 8/10

Prompt 6 (Prompt Chaining)
Clarity: 2/2
Context: 2/2
Specificity: 2/2
Format: 1/2
Verification: 2/2
Total: 9/10

# Step 8 — Surface the Best

## Objective

Present the highest-scoring rewritten prompt for each prompting pattern and compare them with the original prompts.

---

## Prompt 1 — Persona

### Original Prompt

> Explain photosynthesis.

### Best Rewrite

> Act as a high-school biology teacher. Explain photosynthesis to a 15-year-old student using simple language, one real-world example, and a short summary at the end.

### Rubric Score

| Criterion    | Score    |
| ------------ | -------- |
| Clarity      | 2/2      |
| Context      | 2/2      |
| Specificity  | 2/2      |
| Format       | 1/2      |
| Verification | 2/2      |
| **Total**    | **9/10** |

### Why It Scored Well

* Clear role assigned
* Audience specified
* Expected output described
* Easy to evaluate

---

## Prompt 2 — Few-Shot

### Original Prompt

> Write a customer support reply.

### Best Rewrite

> Example 1: Customer asks for a refund → polite refund response.
>
> Example 2: Customer reports a delay → empathetic update response.
>
> Now write a response to: "My order arrived damaged."

### Rubric Score

| Criterion    | Score    |
| ------------ | -------- |
| Clarity      | 2/2      |
| Context      | 1/2      |
| Specificity  | 2/2      |
| Format       | 2/2      |
| Verification | 1/2      |
| **Total**    | **8/10** |

### Why It Scored Well

* Includes examples
* Demonstrates expected style
* Improves consistency

---

## Prompt 3 — Chain-of-Thought

### Original Prompt

> Solve this math problem.

### Best Rewrite

> Solve the problem step-by-step. Show assumptions, calculations, reasoning, and provide the final answer separately.

### Rubric Score

| Criterion    | Score     |
| ------------ | --------- |
| Clarity      | 2/2       |
| Context      | 2/2       |
| Specificity  | 2/2       |
| Format       | 2/2       |
| Verification | 2/2       |
| **Total**    | **10/10** |

### Why It Scored Well

* Explicit reasoning process
* Structured answer
* Easy to verify correctness

---

## Prompt 4 — Structured Output

### Original Prompt

> Analyze this product review.

### Best Rewrite

> Analyze the review and return:
>
> * Sentiment (Positive/Neutral/Negative)
> * Key Issues
> * Recommended Actions
> * Confidence Score

### Rubric Score

| Criterion    | Score    |
| ------------ | -------- |
| Clarity      | 2/2      |
| Context      | 1/2      |
| Specificity  | 2/2      |
| Format       | 2/2      |
| Verification | 2/2      |
| **Total**    | **9/10** |

---

## Prompt 5 — System Prompt

### Original Prompt

> Help users with coding questions.

### Best Rewrite

> You are an expert software engineering tutor. Provide concise explanations, include code examples, identify common mistakes, and verify outputs before responding.

### Rubric Score

| Criterion    | Score    |
| ------------ | -------- |
| Clarity      | 2/2      |
| Context      | 2/2      |
| Specificity  | 2/2      |
| Format       | 1/2      |
| Verification | 2/2      |
| **Total**    | **9/10** |

---

## Prompt 6 — Prompt Chaining

### Original Prompt

> Create a business plan.

### Best Rewrite

> Step 1: Identify the business idea.
>
> Step 2: Analyze target customers.
>
> Step 3: Create a revenue model.
>
> Step 4: Develop a marketing strategy.
>
> Step 5: Generate the final business plan.

### Rubric Score

| Criterion    | Score    |
| ------------ | -------- |
| Clarity      | 2/2      |
| Context      | 2/2      |
| Specificity  | 2/2      |
| Format       | 1/2      |
| Verification | 2/2      |
| **Total**    | **9/10** |

---

# Summary Table

| Pattern           | Best Score | Key Improvement                |
| ----------------- | ---------- | ------------------------------ |
| Persona           | 9/10       | Strong role definition         |
| Few-Shot          | 8/10       | Better examples                |
| Chain-of-Thought  | 10/10      | Explicit reasoning             |
| Structured Output | 9/10       | Clear format requirements      |
| System Prompt     | 9/10       | Better behavioral instructions |
| Prompt Chaining   | 9/10       | Logical workflow decomposition |
