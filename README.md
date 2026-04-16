# 🏛️ Yes, Prime Minister

> Turn chaos into architecture.
> Transform any request into an executable engineering decision.

---

## ⚡ What is this

**Yes, Prime Minister** is an advanced orchestration Skill designed for **OpenCode + Cursor**.

It does one thing exceptionally well:

> **Convert vague input into architecture-aware, execution-ready engineering tasks.**

---

## 🧠 Core Capabilities

Given any input:

* a vague requirement
* a bug report
* a casual comment
* a code snippet
* an idea

This Skill will automatically:

### 1️⃣ Architecture Scanning

* Understand the codebase structure
* Identify service boundaries and module relationships
* Locate the real execution paths

### 2️⃣ Memory Synchronization

* Aggregate `.cursor/rules`, `AGENTS.md`, README, and historical changes
* Reconstruct project-level “long-term memory”
* Prevent repeated mistakes

### 3️⃣ Task Reconstruction

Rewrite the request into:

* Engineering objective
* Constraints
* Execution plan
* Acceptance criteria

### 4️⃣ Specialist Agent Generation

Automatically create:

> **A senior developer agent that behaves as if it already knows your entire codebase**

### 5️⃣ Minimal-Surface Execution

* Preserve existing structure
* Avoid unnecessary rewrites
* Strictly follow current conventions

---

## 🧬 Why this exists

Typical AI coding problems:

* Works at file-level only
* Ignores system architecture
* Forgets historical decisions
* Produces uncontrolled changes

**Yes, Prime Minister solves:**

> ❌ “Just write code”
> ✅ “Understand the system before writing code”

---

## 🏗️ How it works

```text
User Input
   ↓
[Skill Activation]
   ↓
Codebase Scanning
   ↓
Architecture Modeling
   ↓
Memory Synchronization
   ↓
Task Reconstruction
   ↓
Specialist Agent Generation
   ↓
Minimal-Scope Execution
   ↓
Validation
```

---

## 🧾 Output Structure

Each invocation produces:

1. One-line decision
2. Architecture-aware summary
3. Specialist agent / task brief
4. Next action or execution result

---

## 🧩 Example

### Input

```text
Help me optimize this order execution logic
```

### Output (simplified)

```text
Decision: This belongs to the order execution path and requires state machine analysis.

Architecture Summary:
The system uses a hybrid WebSocket + REST trading architecture...

Specialist Agent:
You are a high-frequency trading systems engineer...
```

---

## 🔧 Installation

### OpenCode

Place the skill at:

```text
.opencode/skills/yes-prime-minister/SKILL.md
```

---

### Cursor (Recommended)

Combine with:

```text
.cursor/rules/
```

Use it as a:

> High-priority orchestration layer for engineering tasks

---

## ⚙️ Usage

Trigger explicitly:

```text
@yes-prime-minister
```

Or use it as your default reasoning layer.

---

## 🎯 Use Cases

* Multi-file changes
* Large codebase understanding
* Refactoring
* Debugging
* Architecture design
* Trading systems (highly recommended)
* AI agent systems

---

## ⚠️ Design Principles

* Understand before acting
* Minimize changes
* Always validate
* Preserve memory

---

## 🧠 One-line Summary

> **This is a Skill that doesn’t write code.**
> **It decides how code should be written before it exists.**

---

## 🏁 Next Steps

Possible extensions:

* Git history intelligence
* Multi-agent orchestration
* Trading-system-specific mode
* Debug-specialized workflows
* Architecture evolution tracking

---

**Yes, Prime Minister.**
Now you are in control of your codebase.
