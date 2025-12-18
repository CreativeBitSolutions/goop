# Part I — Foundations of C# and OOP

> Drafted from `course_data_source.pdf` concepts. This section is formatted as course-ready content (chapters, figures, callouts). Add diagrams and screenshots when converting to Word.

## Chapter 1. Orientation & Course Workflow (≈2 pages)

### 1.1 Course goals and outputs
- Build fluency with C# syntax, control flow, and memory model.
- Transition into OOP design and implementation with practical algorithms (search, min/max, sorting) from the source quiz.
- Produce lab-ready code snippets and visual aids for students.

### 1.2 Environment setup
- **Install** .NET SDK (LTS), Visual Studio or VS Code with C# extensions.
- **Create a starter project:** `dotnet new console -n OopFundamentals`.
- **Repository workflow:** branch → edit → run tests → commit → pull request.
- **Coding conventions:** PascalCase for types/methods, camelCase for locals/parameters, meaningful names.

### 1.3 How to use this notebook
- Each chapter has **concept briefs**, **worked examples**, and **lab prompts**.
- When converting to Word, insert **figures** for memory layout, control-flow graphs, and matrix traversal diagrams.
- Maintain a **running code file** per lab to validate outputs.

### 1.4 Quick navigation hints
- Keep a **glossary** at the end of the notebook for operators and data types.
- Use **page flags** or bookmarks for: operator reference, loop equivalence patterns, array traversal templates.

---

## Chapter 2. C# Syntax Essentials Refresher (≈6 pages)

### 2.1 Literals, identifiers, constants, variables
- Numeric literals: decimal/hex (`0xAB`), binary (`0b1010`), underscore separators.
- Character and string literals, escape sequences, verbatim strings (`@"C:\\path"`).
- **Constants:** `const int N = -1;` (compile-time allocation semantics).
- **Identifiers:** rules and casing; examples aligned with quiz items.

### 2.2 Expressions and operators
- **Arithmetic & precedence:** `+`, `-`, `*`, `/`, `%`, unary `+`/`-`.
- **Relational & logical:** `<`, `<=`, `>`, `>=`, `==`, `!=`, `&&`, `||`, `!`.
- **Ternary operator:** `var c = (a < b) ? a : b;` (quiz Q22 exemplar).
- **Bitwise & shift:** `&`, `|`, `^`, `~`, `<<`, `>>` with small tables:
  - Example: `171 & 205 = 0x89`, `171 | 205 = 0xEF`, `171 ^ 205 = 0x66`.
  - Example: `23 >> 3 = 0x2`, `23 << 3 = 0xB8`.
- **Operator precedence cheat sheet:** when to add parentheses; note short-circuiting.

### 2.3 Type system snapshot
- **Integral types:** `sbyte`, `byte`, `short`, `int`, `long`, `uint`, etc.; signed vs. unsigned.
- **Floating point:** `float`, `double`, `decimal` (precision guidance).
- **`struct` vs `class`:** value vs reference semantics.
- **`void` and `pointer` (`int*`) usage in unsafe context (preview for Chapter 16).

### 2.4 Naming and scope
- Block scope, loop variable scope, and shadowing notes.
- Guidelines for **symbolic constants** and **readonly fields**.

### 2.5 Lab prompts
- Evaluate provided bitwise expressions and confirm hexadecimal results.
- Rewrite small expressions with explicit parentheses to match quiz equivalence answers.

---

## Chapter 3. Control Flow Patterns (≈6 pages)

### 3.1 Conditionals
- `if/else`, nested conditionals, and `switch` usage.
- **Null/empty checks** and guard clauses to simplify branches.
- Common pitfalls: empty statement (`if (a > 0) ; else ;`) is syntactically valid but rarely intended (quiz Q7 examples).

### 3.2 Loop forms and equivalence
- **`for`**, **`while`**, **`do…while`** structures with entry/exit conditions.
- Illustrated equivalences drawn from quiz items (Q1, Q2, Q29, Q30, Q33):
  - Transform `while (i < n && x[i] != a) i++;` into `do/while` and guarded variants.
  - Compare `for (i = 0; i < n; i++) y[i] = x[i];` with equivalent `while`/`do…while` rewrites.
- **Loop invariants**: what stays true each iteration; helps with reasoning and testing.

### 3.3 Array traversals
- **One-dimensional:** forward, backward, sentinel-based searches.
- **Two-dimensional (matrix):**
  - Traverse triangles relative to main/secondary diagonals (quiz Q23 patterns).
  - Check for upper/lower triangular matrices (quiz Q28) and zero matrices.
- Include **figure placeholders** for traversal paths.

### 3.4 Early exit and continuation
- Using `break`/`continue` judiciously; when to prefer condition restructuring.
- Guarding against out-of-range access when shifting loop bounds.

### 3.5 Lab prompts
- Convert provided loop snippets between forms and validate equivalence.
- Implement a traversal that visits the triangle below the secondary diagonal and annotate visited indices.

---

## Chapter 4. Error Handling & Defensive Programming (≈3 pages)

### 4.1 Exceptions vs. validations
- When to throw vs. when to return status; mapping to method contracts.
- Input validation at boundaries (array indices, matrix dimensions).

### 4.2 Guard clauses in iterative algorithms
- Pre-validate `n` and bounds before loops (e.g., avoid `IndexOutOfRangeException`).
- Use **argument checks** in methods (e.g., `if (array == null) throw new ArgumentNullException(nameof(array));`).

### 4.3 Debugging quickstart
- Using breakpoints and watch windows to inspect loop counters and array values.
- Logging minimalist traces for algorithm steps (e.g., min/max updates, swap operations).
- Encourage students to **predict loop counts** before running code.

### 4.4 Lab prompts
- Add guard clauses to a min/max routine and verify behavior with edge cases.
- Practice stepping through a bubble sort and recording variable changes.

---

### Conversion notes for Word export
- Insert **title pages** and **chapter separators** with page numbers.
- Add **diagram placeholders** (memory layout, control-flow graphs, matrix traversal heatmaps).
- Keep a **margin note** column for quick quiz references.

