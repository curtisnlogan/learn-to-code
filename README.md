note: nothing should be getting done that isn't on the product backlog

note: 📝 Story Points & Modified Fibonacci (Minimalist)

Story Points

Relative measure of effort, complexity, uncertainty.

Not hours → compare tasks against each other.

Used for sprint planning & tracking velocity.

Modified Fibonacci Scale

Sequence: 1, 3, 5, 8, 13, 20, 40

Based on Fibonacci, simplified for practicality.

Non-linear → bigger jumps for larger, uncertain work.

Guidelines

1–3 = Small, simple, low effort.

5–8 = Medium, some complexity.

13 = Large, check if it needs splitting.

20–40 = Too big → likely an Epic, must be broken down.

✅ Takeaway: Use points for relative sizing. Break down anything too large.

note: tasks

1 (use verbs instead of nouns)

2 (create ideally-sized tasks)

4 (cover the acceptance criteria)

# Notes

## 1) Mindset for Learning to Code

**Sufficiency over totality.** You don’t need to understand every layer to make progress. Aim for *operational understanding*—enough to build, debug, and extend safely. Dive deeper only when the problem requires it.

* Modern stacks are layered abstractions (e.g., Python → ORM → DB driver → database → OS → hardware). Learn to work with “black boxes,” and peek inside as needed.
* A pro is comfortable saying: *“I don’t know that part yet; I’ll learn it when it matters.”*

**Skill shape.** Start I‑shaped (depth in one area), grow into a lean T‑shape (broad collaboration skills with one or two deep specialties).

**Reading vs writing.** Expect to spend **2–3 hours reading** (code, docs, debugging) for every hour of coding. That’s normal.

**Simplicity.** Maximize the amount of work *not* done. Avoid speculative features and premature optimization. Manage technical debt intentionally—don’t take the “easy now, costly later” path by default.

---

## 2) Agile Fundamentals (solo or teams)

**Iron Triangle (Time–Cost–Scope).** In Agile we typically **fix time and cost, flex scope, and protect quality**. Optimize for value delivered, not for completing a fixed wish list.

**Perception matters.** Users often equate “quality” with *feature completeness*, while devs think of maintainability, correctness, and polish. Cutting scope can be perceived as cutting quality—manage expectations explicitly.

**Reality check on scope.** A common rule of thumb: in custom software, a large share of features see little usage. Prioritize ruthlessly.

**Agile health questions** (use these to self-check your work):

* **Working software first:** Do you produce something usable early (not just at the end)?
* **Iterative:** Are you delivering value in small steps (1–4 weeks), layering capability over time?
* **Adaptive:** Do you change plans when you learn something new?
* **Prioritized:** Are you focusing on the most valuable items, not everything?
* **Collaborative/Reflective:** Are you communicating daily (or, solo, reviewing your own progress regularly)?
* **Simple:** Are you deliberately avoiding unnecessary work/features?

**A simple delivery flow:**

1. **Flexible scope** to start.
2. **Prioritized list** (backlog) by value.
3. **Incremental delivery** of working software.
4. **Respond to change** based on feedback.
5. **Satisfied customer** as the north star.

---

## 3) User Stories — Writing & Slicing

**Smallest unit of work.** A user story is the smallest deliverable slice of user-visible value.

**Format (What & Why):**

> *As a* \[user], *I want* \[thing] *so that* \[benefit].

**INVEST quality checklist:**

* **I**ndependent
* **N**egotiable
* **V**aluable
* **E**stimable
* **S**mall
* **T**estable

**Acceptance criteria (proof it’s done).** Testable outcomes that start with: *“I’ll know it’s done when…”*

**Tasks (optional for small stories).** The implementation steps—*how* you’ll build it.

**Example — Password Reset**

* **Story:** *As a customer, I want to reset my password so I can log back in.*
* **Acceptance Criteria:**

  * Reset link is sent to the registered email.
  * Link expires after 24 hours.
  * New password works at login.
* **Tasks:** Build reset UI; add API endpoint; hook up email service.

---

## 4) Story vs Epic vs Theme

* **User Story:** A small, testable slice for a specific user and need. Avoid technical jargon; focus on user value.
* **Epic:** A larger body of work that’s too big for one story and is completed over multiple iterations via child stories.
* **Theme:** A broader grouping of related work (e.g., “User Accounts”) used for organizing epics and stories.

**Example — Polls**

* **Too broad (treat as an Epic):**

  * *As an administrator, I can publish a poll in order to collect users’ feedback.*
  * Why: “Publishing a poll” implies multiple sub-capabilities: add title, add questions, choose expiry, set visibility, configure who can answer, etc.

* **Good user story (narrow, testable):**

  * *As an administrator, I can set an expiry date when publishing a poll so the poll hides automatically.*

* **Other child stories (examples):**

  * Add a title to a poll.
  * Add multiple questions to a poll.
  * Set visibility rules for a poll.
  * Configure who can answer a poll.

---

## 5) Debugging & Quality Practices

**Print debugging: pros & cons**

* ✅ *Pros:* trivial to add, good for tracing logic, works everywhere.
* ⚠️ *Cons:* clutters code, noisy output, poor control over verbosity, doesn’t scale to complex flows.

**Cleaner alternatives**

1. **Debugger:** Step through code, inspect variables, set breakpoints (e.g., `pdb`/IDE for Python; browser/Node inspector for JS).
2. **Structured logging:** Use log levels (DEBUG/INFO/WARN/ERROR). Turn verbosity on/off without editing call sites.
3. **Unit tests:** Catch regressions early so you spend less time chasing bugs via print statements.

**Error-handling rule of thumb**

* *Ask:* “Does this function know exactly what to do about this error?”

  * **Yes →** catch and handle it here.
  * **No →** let it propagate (raise) so the caller decides.

**Avoid over-engineering**

* Deliver the simplest thing that works; iterate.
* Don’t build the “final” expansive version first. Add capability incrementally based on feedback.

---

## 6) Prioritization & Expectation Management

**Value ≠ usage frequency only.** Some features are symbolic or carry legacy/cultural weight. Even if rarely used, cutting them can trigger backlash. Consider *perceived value* alongside data.

**Communicate trade‑offs.** Be explicit when scope changes: what’s deferred, what quality you’re protecting, and what value ships now.

---

## 7) Quick Checklists

**User Story Checklist**

* [ ] Clear user and intent (*As a… I want… so that…*)
* [ ] Passes INVEST
* [ ] Acceptance criteria are concrete and testable
* [ ] Small enough for a single iteration
* [ ] Tasks identified (if needed)

**Iteration Checklist**

* [ ] Working software early in the iteration
* [ ] Small, incremental additions (not giant leaps)
* [ ] Priorities reviewed against current learning
* [ ] Refactoring/quality protected
* [ ] Stakeholder expectations reset as needed

---

## 8) Learning Tactics You Can Try

* **Gamify your practice.** Use familiar game metaphors/examples to keep momentum.
* **Read first, then code.** Skim related code and docs before writing.
* **Set tiny goals.** Ship a minimal slice, then expand.
* **Log + tests by default.** Prefer structured logging and lightweight tests over ad‑hoc prints.
* **Review yourself.** End of day: what shipped, what I learned, what to try next.

---

### One‑page TL;DR

* Fix time & cost, vary scope, protect quality.
* Slice epics into small, testable user stories (INVEST + acceptance criteria).
* Deliver working software in small increments; adapt plans as you learn.
* Prefer debugger/logging/tests to scattered prints.
* Keep it simple; avoid premature complexity.
* Learn in layers; strive for operational understanding; grow toward a T‑shape.

---

# Learn to Code

## Tier 1: The Foundation

This is the bedrock. A weak foundation guarantees a low ceiling on your growth.

### **Principle #1: Embrace the Journey**

You will hit plateaus. It's not a sign of failure; it's part of the process. The difference between a hobbyist and a professional is daily consistency over sporadic intensity. When you get stuck on a hard problem, switch to a different, easier one. Show up almost every day.

### **Principle #2: Master the Fundamentals**

Data types, control flow, scope, memory, data structures. These are the atoms of software. Every complex system you admire is built from these simple parts. A deep understanding here is non-negotiable and will pay dividends for your entire career.

### **Principle #3: Build to Understand**

Tutorials provide knowledge; projects build skill. Escape "tutorial hell" by starting with the absolute simplest version of an idea imaginable, focusing only on getting that core piece working, and then iterating by adding one small feature at a time. Projects are the forge where knowledge is hammered into skill.

## Tier 2: The Process

Great code isn't accidental. It's the result of a deliberate, disciplined process.

### **Principle #4: Use Version Control Religiously**

Git is your time machine, your safety net, and your collaboration hub. It is not optional. Make small, atomic commits with clear messages.

### **Principle #5: Decompose Before You Code**

Think first, code second. A blank editor is an invitation to write chaotic, tangled code that has high cyclomatic complexity, so resist the urge. Instead, start with the high-level goal, like *"build a login page,"* and keep breaking it down into concrete steps—`validateEmail()`, `hashPassword()`, `checkUserInDatabase()`—until you can't go any further. This process forces you to clarify your logic upfront and turns an intimidating mountain into a series of small, climbable hills. Each small function is easier to write, test, and debug, which prevents the days of rewrites that come from rushing in without a plan.

The Single Responsibility Principle states that every module, class, or function should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the module, class or function. However, a function is too small when it doesn't add value by encapsulating a meaningful or reusable piece of logic.

Embrace the DRY (Don't Repeat Yourself) principle; abstracting duplicated logic into reusable pieces multiplies clarity and reduces bugs.

### **Principle #6: Write for Humans**

Your primary audience is not the computer; it's the next developer who has to touch your code—and that developer is often a future version of you.

Strive for clarity by using clear, descriptive names for variables and functions. Practice conciseness by writing comments that explain the *why*, not the *what*—the code itself should be self-explanatory.

### **Principle #7: Build with Confidence: Test & Debug**

Untested code is broken by default. Testing and debugging are two sides of the same coin: building robust, reliable software.

* **Testing** is your proactive strategy. A powerful approach is Test-Driven Development (TDD), where you write a failing test before you write the code to make it pass. This "Red-Green-Refactor" cycle forces you to define exactly what you want your code to do before you figure out how to do it. It's the ultimate tool for building with confidence, creating a safety net that allows you to refactor fearlessly.
* **Debugging** is your reactive strategy. Bugs are an expected outcome, not a moral failing. When a test fails or a user finds a bug, approach it like a scientist, not a gambler. First, reproduce the bug reliably, ideally by writing a failing test that captures it. Then, isolate the exact line or interaction causing the failure using a debugger or targeted logging. Once found, correct the logic with the goal of making the failing test pass. Finally, verify that all existing tests still pass, ensuring your fix hasn't broken anything else and that the new test prevents the bug from ever returning.

### **Principle #8: Use AI as a Power Tool, Not a Crutch**

AI is the new calculator of programming—powerful, transformative, and unavoidable. But just like calculators don’t replace arithmetic, AI doesn’t replace understanding. Treat it as an accelerator, not a substitute.

* **For exploration:** Use AI to brainstorm solutions, generate alternative approaches, or summarize complex documentation.
* **For productivity:** Offload boilerplate code, setup scripts, or repetitive transformations.
* **For learning:** Ask AI *why* a solution works, not just *what* the solution is. Compare its output to your own reasoning to expose gaps in your understanding.
* **For discipline:** Never blindly paste AI-generated code. Read, refactor, and test it as if it were written by a junior teammate—because it often is.

The professional’s advantage isn’t in using AI—it’s in using it *well*. The developers who thrive will be those who pair deep fundamentals with smart leverage of these new tools.

## Tier 3: The Professional

Technical skill gets you in the door. Professional habits build a career.

### **Principle #9: Read Great Code**

You cannot write what you have not read. Make it a habit to read the source code of the libraries and tools you use every day. See how experts structure their projects, name their variables, and solve complex problems. Curiosity is the fuel for a long-term career.

### **Principle #10: Learn in Public**

Don't code in a vacuum. Share your work, write about what you're learning, and ask for feedback. Teaching is the highest form of understanding. Explaining a concept to someone else is the fastest way to expose the gaps in your own knowledge.

## Project Checklist

### Pre-Coding:

* **#2 (Fundamentals):** Do I understand the core concepts required for this project?
* **#3 (Build to Understand):** What is the absolute simplest, "version 0.1" of this that I can build first?
* **#5 (Decomposition):** Is the problem broken down into its smallest parts on paper or in a doc?

### During-Coding:

* **#4 (VCS):** Am I making small, logical commits with clear, professional messages?
* **#6 (Write for Humans):** Is my code readable? Am I avoiding copy-paste and abstracting repeated logic?
* **#7 (Testing & Debugging):** Have all features been manually verified? Have I written an automated test for a critical piece of logic?
* **#8 (AI Use):** If I used AI to generate code or explanations, did I fully understand, review, and test what it produced before trusting it?

### Post-Coding & Iteration:

* **#9 (Read Code):** Can I find how an expert solved a similar problem on GitHub and compare their solution to mine?
* **#10 (Learn in Public):** Can I write a short blog post or a README section explaining a challenge I solved in this project?
