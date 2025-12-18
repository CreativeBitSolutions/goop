# Part IV — Advanced Language Features & Unsafe Context

> Drafted from `course_data_source.pdf` concepts to expand Chapters 15–18 into Word-ready content. Add figures (delegate multicast chains, memory layout sketches, bitwise truth tables) when exporting.

## Chapter 15. Delegates, Events & Lambda Expressions (≈4 pages)

### 15.1 Delegates as type-safe function pointers
- Declaring delegate types; covariance/contravariance on parameters and returns.
- Referencing static vs. instance methods; multicast invocation lists.
- Quiz-aligned reminder: methods are valid operands in expressions when invoked, not their names alone.

### 15.2 Lambdas and closures
- Expression vs. statement lambdas; capturing variables; avoiding modified-closure pitfalls in loops.
- Passing lambdas to `List<T>.Find`, `Where`, or custom repository filters from Part III labs.

### 15.3 Events and publisher–subscriber
- Event keywords, add/remove accessors, and standard patterns (`EventHandler`, `EventHandler<T>`).
- UI/CLI examples: progress notifications for sorting (selection/bubble) and matrix scans.

### 15.4 Labs
- Build a `SortProgressReporter` that raises events per outer loop iteration (selection sort template from Part II).
- Create a `ThresholdNotifier` using delegates to evaluate array elements (min/max comparisons from quiz items).

---

## Chapter 16. Memory Management, Spans & Unsafe Code (≈5 pages)

### 16.1 Managed memory model
- Stack vs. heap, value vs. reference types; garbage collection basics.
- `ref`/`out` parameters: call-site matching by number, type, and order (quiz parameter-matching themes).

### 16.2 `Span<T>` and `ReadOnlySpan<T>`
- Safer stack-only slices; slicing arrays without allocations; pinning considerations.
- Using spans with searching/summing templates to reduce allocations.

### 16.3 Unsafe code fundamentals
- `unsafe` blocks, pointers, and fixed statements; when interoperability requires them.
- Tie back to quiz pointer signatures (e.g., `float*`, `void*`, double pointers) and why they are functions vs. procedures.

### 16.4 When (not) to use unsafe
- Prefer safe APIs; wrap unsafe helpers with validation and exception safety (echo Chapter 14 guidance).
- Minimal examples: copying buffers, scanning with pointer arithmetic vs. span-based loops.

### 16.5 Labs
- Write a `MinWithPointer` function using pointers, then wrap it with a safe `MinSafe(float[] x)` facade.
- Benchmark `Span<T>`-based traversal vs. array indexing for summing an array of `int`.

---

## Chapter 17. Bitwise Operations & Low-Level Utilities (≈3 pages)

### 17.1 Bitwise operators refresher
- AND/OR/XOR/NOT (`&`, `|`, `^`, `~`), shifts (`<<`, `>>`); signed vs. unsigned shift semantics.
- Quiz tie-ins: evaluate expressions like `a & b`, `a | b`, `a ^ b`, `~a`, and shift-based results in hex.

### 17.2 Practical patterns
- Masks for flags; extracting nibbles/bytes; parity checks.
- Use ternary and bitwise combos to replicate quiz-style conditional assignments.

### 17.3 Labs
- Build utilities to compute set operations over integer bitmasks (union/intersection/difference mirror quiz set problems).
- Implement `NormalizeToByte(int x)` that clamps via bitwise tricks; test with negative and overflow cases.

---

## Chapter 18. Performance & Diagnostics (≈3 pages)

### 18.1 Measuring and profiling
- `Stopwatch` for micro-benchmarks; avoid micro-optimizing before measuring.
- Use of analyzers/profilers; logging loop counters for algorithm diagnostics (e.g., swap counts in bubble sort).

### 18.2 Complexity reminders
- Big-O review of sorts/searches already covered; note impact of unsafe/pointer arithmetic on readability vs. speed.

### 18.3 Labs
- Instrument selection vs. bubble sort to compare iterations and swaps; chart results in Word.
- Add diagnostic counters to matrix traversal templates (triangles/diagonals) to surface hot paths.

---

## Word-export notes
- Add diagrams for delegate chains, memory layout (stack/heap/pinned buffers), and bitwise truth tables.
- Keep heading styles consistent with earlier parts; include captioned figures and code listings for lab steps.
