# Part II — Data Structures & Algorithms Warm-up

> Drafted from `course_data_source.pdf` concepts. This section expands Chapters 5–8 with ready-to-drop content for a Word-formatted course book. Add diagrams (array layouts, traversal paths, sorting swaps) when exporting.

## Chapter 5. Arrays, Indexing & Memory Model (≈6 pages)

### 5.1 Declaring and initializing arrays
- Syntax recap: `int[] x = new int[n];`, `int[] y = { 2, 4, 6, 8 };` (quiz Q46 exemplar).
- Default values and bounds; `IndexOutOfRangeException` prevention.
- Fixed-size arrays with string copy example (quiz Q24: 22-char buffer, 44 bytes total for char payload).

### 5.2 Array operands and element references
- Operands permitted in expressions: constants, literals, variables, array names and elements, function names, composite expressions (quiz Q4 inventory).
- Show legal vs. illegal operands with mini tables.

### 5.3 Copying, cloning, and shadow copies
- Manual copy loop: `for (i = 0; i < n; i++) y[i] = x[i];` plus equivalent `while`/`do…while` forms (quiz Q33 patterns).
- `Array.Copy` vs. `Clone`, and when to prefer spans or `Memory<T>` (preview).

### 5.4 Compacting and removing duplicates
- Example: remove duplicates by shifting elements left (quiz Q21 compacting snippet). Include figure placeholder for before/after arrays.
- Emphasize loop invariants: `n` shrinks when a duplicate is removed; adjust indices carefully.

### 5.5 Set-style operations on arrays
- Difference operation implementation (quiz Q20: compute `x - y`), with step trace and complexity note O(m·n).
- Intersection and union pointers; when to sort first.

### 5.6 Lab prompts
- Implement a safe copy routine with bounds checks; confirm equivalence variants produce same result.
- Build `SetDifference(int[] x, int m, int[] y, int n)` returning a new array; validate with edge cases.
- Compact an array and assert final length; add unit-test ideas for duplicate cases.

---

## Chapter 6. Multidimensional & Jagged Arrays (≈4 pages)

### 6.1 Rectangular arrays
- Declaration: `int[,] a = new int[n, m];` and `a.GetLength(0/1)` usage.
- Traversal patterns with nested loops; row-major iteration diagrams.

### 6.2 Triangles relative to diagonals
- Secondary-diagonal triangle traversals with loop templates (quiz Q23 options). Provide two concrete implementations with index maps.
- Checking triangular matrices: lower vs. upper (quiz Q28); include a quick diagnostic function and truth table.

### 6.3 Constant rows/columns detection
- Row-constant detection algorithm (quiz Q27): scan each row, compare against first element, record row indices.
- Column-constant detection variant for practice; suggest sentinel boolean flags.

### 6.4 Matrix scans for extrema
- Example: maximum in upper triangle formed by diagonals (quiz Q26) — discuss boundary conditions and iterations `for (i = 0; i < m/2; i++)`.
- Minimum/maximum with position tracking templates reused in sorting (ties: first vs. last occurrence distinctions from quiz Q18/19).

### 6.5 Lab prompts
- Implement functions `IsUpperTriangular` and `IsLowerTriangular` with unit tests for zero/non-zero entries.
- Write `ConstantRows(int[,] a)` returning row indices with equal elements; visualize with heatmap-style placeholders.
- Compute max in a diagonal-defined region and compare iterations vs. a naive full scan.

---

## Chapter 7. Classic Iterative Algorithms (≈5 pages)

### 7.1 Aggregations
- Sum of first n natural numbers: `while`/`for` variants (quiz Q16) — highlight correct forms (variants 3 & 5) and pitfalls (off-by-one, wrong initializer).
- Factorial patterns (quiz Q42) — valid loops (3, 4, 5) vs. invalid (0 multiplier, wrong range). Provide trace tables for n = 5.
- Dot product example (quiz Q5/31 sequences): `s += x[i] * y[i];` with complexity O(n).

### 7.2 Searches
- Linear search templates (quiz Q30): `while (i < n && x[i] != a) i++;` and do/while guarded variants.
- Early exit strategies; sentinel element idea (`x[n] = key;` in expanded discussion).

### 7.3 Extremes (min/max) with position tracking
- Max scans: standard forward/backward passes (quiz Q3 variants 1,3,4,6) with notes on initialization and bounds.
- Min scans: forward/backward (quiz Q6 variants 1,2,3,5,6) and sort-based approach (variant 2). Include tie-handling: first vs. last occurrence (quiz Q18 logic stores first min index `p`).

### 7.4 Iterative vs. recursive discussion
- Identify provided sequences as **iterative**, not recursive (quiz Q31 answer: none recursive). Briefly define recursion for contrast.

### 7.5 Lab prompts
- Implement `SumNatural(n)` with three loop styles; add asserts on known triangular numbers.
- Write `MinWithIndex(int[] a)` returning value and first index; extend to last index variant.
- Construct small test cases to invalidate incorrect factorial loops; capture outputs for n = 0..5.

---

## Chapter 8. Sorting & Selection Patterns (≈5 pages)

### 8.1 Swap mechanics and helper routines
- Swapping elements with a temp variable; illustrate with mini diagram and emphasize side-effect locality.
- Note: avoid unnecessary swaps when elements equal to maintain stability (bubble sort variant comment).

### 8.2 Selection sort
- Outline (quiz Q19 and Q32 variant 3/5 logic): find min in unsorted suffix, swap into position `i`.
- Complexity O(n²), not stable by default; small-table trace for n = 5 sample input.

### 8.3 Bubble sort
- Classic bubble (quiz Q32 variants 2 and 4): repeated adjacent comparisons until pass completes with no swaps (`vb` flag).
- Discuss best-case O(n), worst-case O(n²); emphasize early-exit optimization.

### 8.4 Comparison of quiz-listed snippets
- Valid ascending sorts: variants 1, 2, 3, and 5 (quiz Q32 correct set C). Explain why each produces sorted order; highlight misordered bounds that would break correctness.
- Distinguish bubble vs. selection in provided pseudocode (Q19 = selection sort, not bubble).

### 8.5 Stability, in-place property, and memory model
- Define stability; bubble is stable, selection is not (unless ties handled specially).
- All shown algorithms are in-place, O(1) extra memory.

### 8.6 Lab prompts
- Implement `SelectionSort(int[] a)` and `BubbleSort(int[] a)`; instrument with swap counters.
- Add unit tests: already-sorted, reverse-sorted, all-equal, and mixed cases.
- Visualize swaps with annotated arrays for student handouts.

---

### Conversion notes for Word export
- Insert chapter title pages and figure placeholders (array diagrams, traversal paths, swap animations).
- Use sidebars for **quiz answer keys** mapped to chapter topics (e.g., Q20 difference set, Q26 max in diagonal region).
- Maintain consistent page headers/footers and a glossary link back to Part I.
