# OOP in C# — Course Support (Table of Contents)

> Drafted from the concepts surfaced in `course_data_source.pdf`, targeting a 100-page illustrated course notebook. Page counts are estimates to guide drafting.

## Part I. Foundations of C# and OOP (≈20 pages)
1. **Orientation & Course Workflow** (≈2 pages)
   - Environment setup (SDK, IDEs, project templates)
   - How to use the course notebook, examples, and labs
2. **C# Syntax Essentials Refresher** (≈6 pages)
   - Literals, identifiers, constants, variables
   - Expressions and operator groups (arithmetic, relational, logical, ternary, bitwise, shift)
   - Type system overview (integral, floating, `struct`, pointers, `void`)
3. **Control Flow Patterns** (≈6 pages)
   - Conditionals (`if`, `switch`, ternary) and common pitfalls
   - Iteration forms (`for`, `while`, `do…while`, nested loops) and loop equivalence patterns
   - Pattern-based traversal of arrays and matrices (triangles, diagonals)
4. **Error Handling & Defensive Programming** (≈3 pages)
   - Exceptions vs. validation
   - Guard clauses in iterative algorithms
   - Debugging quickstart

## Part II. Data Structures & Algorithms Warm-up (≈20 pages)
5. **Arrays, Indexing & Memory Model** (≈6 pages)
   - 1D arrays: declaration, initialization, bounds
   - Array operands and element references
   - Copying, compacting, and difference/intersection patterns
6. **Multidimensional & Jagged Arrays** (≈4 pages)
   - Traversal schemes (row/column-wise, triangles relative to main/secondary diagonals)
   - Detecting constant rows/columns; zero/triangular matrix checks
7. **Classic Iterative Algorithms** (≈5 pages)
   - Aggregations (sum, product, dot product)
   - Searches (linear variants, sentinel style)
   - Extremes (min/max with position tracking)
8. **Sorting & Selection Patterns** (≈5 pages)
   - Selection sort, bubble sort, swap mechanics
   - Stability and complexity notes

## Part III. Object-Oriented Programming Core (≈30 pages)
9. **Classes, Objects & Encapsulation** (≈6 pages)
   - Fields, properties, methods; access modifiers
   - Immutable vs. mutable designs; data validation
10. **Constructors, Initialization & Object Lifetime** (≈4 pages)
    - Overloading, optional parameters, static constructors
    - IDisposable pattern fundamentals
11. **Composition, Aggregation & Associations** (≈4 pages)
    - Containment patterns (arrays of objects, nested objects)
    - Navigating relationships safely
12. **Inheritance & Polymorphism** (≈6 pages)
    - Base/derived classes, virtual/override/sealed
    - Abstract classes vs. interfaces; substitution principles
13. **Interfaces, Generics & Collections** (≈6 pages)
    - Designing reusable contracts; implementing collection interfaces
    - Generic classes/methods; variance basics
    - Core collections (`List<T>`, `Dictionary<TKey,TValue>`, arrays vs. spans)
14. **Exception Safety & Error Contracts in OOP** (≈4 pages)
    - Custom exceptions, fail-fast guards
    - Exceptions in constructors and property setters

## Part IV. Advanced Language Features & Unsafe Context (≈15 pages)
15. **Delegates, Events & Lambda Expressions** (≈4 pages)
    - Event-driven design; multicast delegates
16. **Memory Management, Spans & Unsafe Code** (≈5 pages)
    - Stack vs. heap; `ref`/`out` semantics; pointers in C# (`unsafe`, fixed buffers)
    - Interop considerations; when and why to avoid unsafe code
17. **Bitwise Operations & Low-Level Utilities** (≈3 pages)
    - Bitwise AND/OR/XOR/NOT, shifts; common numeric tricks
    - Examples drawn from quiz-style expressions
18. **Performance & Diagnostics** (≈3 pages)
    - Benchmarking loops and allocations
    - Profiling and logging patterns

## Part V. Patterns, Testing & Applied OOP (≈15 pages)
19. **Design Principles & Patterns** (≈5 pages)
    - SOLID essentials; strategy, decorator, and factory patterns in C#
20. **Unit Testing & Contracts** (≈4 pages)
    - xUnit/NUnit basics; arranging tests around OOP features
    - Assertions for algorithmic routines (min/max, search, sorting)
21. **Case Studies & Mini-Projects** (≈6 pages)
    - Building a matrix utilities library (search, triangular checks, sorting)
    - Small OOP application: inventory or quiz engine using earlier algorithms

## Appendices (≈10 pages)
A. **Cheat Sheets & Equivalence Patterns** (≈4 pages)
   - Loop-to-loop equivalences from the source quiz (while ↔ do/while ↔ for)
   - Common traversal templates for arrays and matrices
B. **Reference Tables** (≈3 pages)
   - Operator precedence (including bitwise/shift)
   - Type ranges and default values
C. **Glossary & Further Reading** (≈3 pages)
   - Terms, recommended docs, and study roadmap

---
**Total projected length:** ≈100 pages with illustrations, code listings, and annotated diagrams.
