# Part III — Object-Oriented Programming Core

> Drafted from `course_data_source.pdf` concepts to expand Chapters 9–14 into Word-ready content. Add diagrams (class/object relationships, constructor timelines, inheritance hierarchies) when exporting.

## Chapter 9. Classes, Objects & Encapsulation (≈6 pages)

### 9.1 Class anatomy
- Fields, properties, methods; access modifiers (`public`, `private`, `internal`, `protected`).
- Backing fields vs. auto-properties; init-only setters for immutability.
- Operand review in expressions (quiz Q4/Q9/Q35 context): valid identifiers, literals, array names/elements, method calls; exclude `using` and `void` as operands/returns.

### 9.2 Encapsulation and invariants
- Guarding state via property validation; prefer immutable value objects for safety.
- Show example of `Point` with encapsulated coordinates and validation method.
- Discuss data-hiding benefits for algorithmic routines (min/max, search) to prevent invalid states.

### 9.3 Object creation and identity
- `new` allocations, reference vs. value semantics; equality vs. reference equality.
- Copying objects safely vs. shallow memberwise copies.

### 9.4 Labs
- Implement a `Vector` class that wraps an `int[]` and exposes `Sum`, `Max`, and `IndexOf` using patterns from Part II.
- Add property validation to reject negative lengths; demonstrate failing test cases.

---

## Chapter 10. Constructors, Initialization & Object Lifetime (≈4 pages)

### 10.1 Constructor forms
- Parameterized, overloaded, and static constructors; optional parameters and default values.
- Chaining with `: this(...)` and `: base(...)`; when to perform validation.

### 10.2 Object lifetime and disposal
- Deterministic cleanup via `IDisposable` and `using` statements (contrast with `using` keyword as non-type operand in quiz lists).
- Highlight exception safety: avoid throwing after partially constructing objects; prefer factory helpers for complex setup.

### 10.3 Labs
- Build a `TimerScope` disposable that logs elapsed time for an algorithm (e.g., selection sort from Part II).
- Add a static constructor that precomputes lookup data; verify it runs once via unit test.

---

## Chapter 11. Composition, Aggregation & Associations (≈4 pages)

### 11.1 Modeling relationships
- Composition (owns lifecycle) vs. aggregation (shared references) vs. simple associations.
- Examples: `Order` → `OrderLine` (composition); `Course` → `Instructor` (aggregation); `Matrix` uses `Vector` (association).

### 11.2 Navigating safely
- Null-handling strategies: constructor injection, null-object patterns, and guard clauses.
- Iteration over child collections: reuse traversal patterns from Part II (nested loops) for reporting.

### 11.3 Labs
- Implement `Classroom` that aggregates `Student` objects; add method `TopStudent()` using max-with-index template.
- Draw UML-lite diagrams showing ownership arrows; include placeholder figures in Word export.

---

## Chapter 12. Inheritance & Polymorphism (≈6 pages)

### 12.1 Inheritance basics
- Base/derived classes, `virtual`, `override`, `sealed`; abstract classes vs. concrete implementations.
- Emphasize substitution: derived types must honor base contracts; avoid slicing by using references.

### 12.2 Polymorphic behavior
- Virtual dispatch in action with simple shape hierarchy; contrast with interface-based dispatch.
- Explain when to prefer composition over inheritance (favoring flexible relationships from Chapter 11).

### 12.3 Handling constructors in inheritance
- Base constructor calls and execution order; avoid calling virtual members from constructors.
- Exception considerations: fail-fast before base state is inconsistent.

### 12.4 Labs
- Create `Animal` → `Dog`/`Cat` hierarchy with `MakeSound()` virtual method and override behavior.
- Extend with `IWalkable` interface to preview Chapter 13; test polymorphic collections (`List<Animal>`).

---

## Chapter 13. Interfaces, Generics & Collections (≈6 pages)

### 13.1 Interfaces and contracts
- Defining behavior-only contracts; multiple interface implementations vs. single inheritance.
- Interface-based design for algorithms: e.g., `IMinMaxProvider` with `GetMin()`/`GetMax()` built atop Part II patterns.

### 13.2 Generics fundamentals
- Generic classes and methods; type parameters, constraints (`where T : struct/class`), and variance basics (`out`/`in`).
- Benefits: type safety, reduced casting, performance (avoid boxing).

### 13.3 Collections overview
- Core collections: `List<T>`, `Dictionary<TKey,TValue>`, arrays, and spans; iteration idioms (`for`, `foreach`, `while`).
- Sorting/searching utilities (`List<T>.Sort`, `Array.BinarySearch`), contrasted with manual algorithms from Chapter 8.

### 13.4 Labs
- Implement a generic `Repository<T>` with in-memory storage and `Find(Func<T, bool>)` filter; add unit test cases.
- Write a generic `Swap<T>(ref T a, ref T b)` using references to mirror the swap mechanics in selection/bubble sorts.

---

## Chapter 14. Exception Safety & Error Contracts in OOP (≈4 pages)

### 14.1 Exception design
- Custom exception types; include context-rich messages.
- Guard clauses for preconditions; prefer `ArgumentException`/`ArgumentNullException` for bad inputs.

### 14.2 Fail-fast constructors and property setters
- Validate arguments early; avoid leaving partially initialized objects.
- Idempotent setters that maintain invariants (e.g., lengths > 0, non-null arrays).

### 14.3 Interop with low-level/unsafe code (preview)
- Briefly note `unsafe` pointers and when to surface them via safe wrappers (ties to quiz items with pointer signatures).

### 14.4 Labs
- Add validation to `Vector`/`Matrix` types; throw on invalid bounds and test with negative/overflow cases.
- Wrap an unsafe min/max function in a safe API and document the contract.

---

## Word-export notes
- Insert figure placeholders for class diagrams, constructor call sequences, and interface hierarchies.
- Keep chapter title styles consistent with Parts I & II; include page numbers and captions for images.
- Maintain alignment with quiz-driven concepts (loop/operand legality, pointer/unsafe signatures) to match `course_data_source.pdf`.
