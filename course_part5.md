# Part V — Patterns, Testing & Applied OOP

> Drafted from `course_data_source.pdf` concepts to expand Chapters 19–21 into Word-ready content. Add diagrams (pattern sketches, test pyramids, mini-project UI flow) when exporting.

## Chapter 19. Design Principles & Patterns (≈5 pages)

### 19.1 Core principles
- SOLID highlights: single responsibility for algorithms (sum/min/max), open/closed with strategy swaps for sorting, Liskov substitution reminders from inheritance chapter.
- Encapsulate variation: prefer composition for behaviors (e.g., comparator strategy for selection/bubble sorts).

### 19.2 Essential patterns in C#
- Strategy: inject different search or comparison functions (delegates from Part IV) into array processing.
- Factory: centralize object creation with validation (reuse guard clauses from Chapter 14 for min/max routines).
- Decorator: wrap repositories or services to add logging/diagnostics (ties to Chapter 18 metrics).

### 19.3 Labs
- Implement `ISortStrategy` with `SelectionSortStrategy` and `BubbleSortStrategy`; benchmark via Chapter 18 harness.
- Create a `MatrixFactory` that validates dimensions and fills with test data for traversal exercises.

---

## Chapter 20. Unit Testing & Contracts (≈4 pages)

### 20.1 Testing frameworks overview
- xUnit/NUnit basics; arranging tests (Arrange-Act-Assert) for methods computing sums, min/max, and searches.
- Parameterized tests for array/matrix scenarios (constant rows, triangular checks).

### 20.2 Contracts and assertions
- Precondition checks via exceptions; postconditions via assertions; invariants for classes with collections.
- Link to quiz themes: parameter matching (number/type/order) and operand validity.

### 20.3 Labs
- Write unit tests for `MinWithPointer` wrapper, set-difference routines, and duplicate-removal algorithms.
- Add guard-clause tests for constructors and property setters introduced in Part III.

---

## Chapter 21. Case Studies & Mini-Projects (≈6 pages)

### 21.1 Matrix utilities library
- Implement functions: `IsLowerTriangular`, `IsUpperTriangular`, `FindConstantRows`, `Difference(x, y)`, and `CompactDuplicates` (drawn from quiz scenarios).
- Provide both safe and unsafe variants where appropriate; document contracts.

### 21.2 Quiz engine or inventory mini-app
- Design domain entities (questions/items), repositories, and services using patterns from Chapters 19–20.
- Include UI/CLI loop with event notifications (delegate/event practice from Part IV).

### 21.3 Labs
- Ship a minimal console app that loads sample data, runs array/matrix algorithms, and reports metrics.
- Encourage students to extend with logging, persistence, and additional quiz question types.

---

## Word-export notes
- Insert diagrams for strategy/factory/decorator flows and testing pyramids; include sequence diagrams for mini-project workflows.
- Maintain consistent heading hierarchy and caption styles; reserve space for screenshots of running mini-projects.
