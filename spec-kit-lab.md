# 🌱 Build with Spec Kit — Hands-On Workshop

**Workshop:**GitHub Copilot Agentic DevOps Workshop  
**Duration:** 45 minutes | **Presenter:** Yuri Lausberg  
**Repo:** [github.com/github/spec-kit](https://github.com/github/spec-kit)

---

## What is Spec Kit?

Spec Kit is an open-source toolkit for **Specification-Driven Development (SDD)** — a methodology that flips the traditional development model. Instead of writing specs that serve code, **specifications become executable**, directly generating working implementations through AI agents. Focus on the *what* and *why*; let the agent handle the *how*.

---

## The 6-Step Process

| Step                  | Command                                        | What You Do |
|-----------------------|------------------------------------------------|-------------|
| **1. Initialize** | `specify init` | Scaffold a Spec Kit project with templates, scripts, and agent config |
| **2. Constitution** | `/speckit.constitution` | Define project principles, constraints, and guardrails |
| **3. Specify** | `/speckit.specify` | Describe *what* you want to build — requirements, not implementation |
| **4. Clarify** | `/speckit.clarify` | Resolve ambiguities, refine edge cases, add detail iteratively |
| **5. Plan** | `/speckit.plan` | Provide tech stack choices → agent generates a technical implementation plan |
| **6. Implement** | `/speckit.tasks` → `/speckit.implement` | Break into tasks, validate with `/speckit.analyze`, then build |

---

## Workshop Flow

### 🔧 Part 1 — Setup (5 min)

```bash
# Initialize a new Spec Kit project (requires uv + Python 3.11+)
uvx --from git+https://github.com/github/spec-kit.git specify init my-demo-app --ai copilot
```

> Opens in VS Code with agent instructions, slash commands, and automation scripts ready to go.

---

### 📜 Part 2 — Define the Constitution (5 min)

Establish the ground rules for your project:

```
/speckit.constitution This project follows a "Cloud-Native" approach using Azure.
We use TypeScript and React. We follow accessibility-first design.
All features must include unit tests. We prefer functional patterns.
```

> **Why it matters:** The constitution acts as persistent guardrails — the AI agent will respect these constraints throughout every subsequent step.

---

### 📝 Part 3 — Write the Spec (10 min)

Describe what you want to build in plain language:

```
/speckit.specify Build a task management dashboard where teams can create projects,
organize tasks in a Kanban board with drag-and-drop, assign team members,
and track progress. Tasks have priority levels, due dates, and comments.
```

Then refine with clarifying questions:

```
/speckit.clarify Focus on the Kanban board interaction model — what happens when
a task is dragged between columns? Should there be WIP limits? How are
notifications handled when a task is reassigned?
```

Validate completeness:

```
/speckit.checklist
```

> **Key insight:** Spend time here — a well-written spec produces dramatically better implementations. This is where human judgment has the most leverage.

---

### 🏗️ Part 4 — Plan & Build (20 min)

Generate the technical plan:

```
/speckit.plan Use Vite + React + TypeScript for the frontend.
Use a REST API with Express and PostgreSQL. Deploy to Azure Container Apps.
```

Break into tasks, audit, and implement:

```
/speckit.tasks
/speckit.analyze
/speckit.implement
```

> **Tip:** For complex projects, implement in phases. Start with core functionality, validate it works, then add features incrementally to avoid overwhelming the agent's context.

---

### 💬 Part 5 — Review & Reflect (5 min)

- Compare the generated output to the original spec
- Discuss: What did the agent get right? What needed human refinement?
- How does SDD change your team's development workflow?

---

## Key Takeaways

| Traditional Development | Spec-Driven Development |
|------------------------|------------------------|
| Specs serve code — written and discarded | Specs *are* the product — executable and versioned |
| One-shot prompts → unpredictable results | Multi-step refinement → predictable outcomes |
| Tech stack drives design | Intent drives design, tech stack is a parameter |
| AI fills in blanks | AI follows a structured, auditable plan |

---

## Quick Reference — All Commands

| Command | Purpose |
|---------|---------|
| `/speckit.constitution` | Set project principles and guardrails |
| `/speckit.specify` | Define requirements in plain language |
| `/speckit.clarify` | Refine and resolve ambiguities |
| `/speckit.checklist` | Validate spec completeness |
| `/speckit.plan` | Generate technical implementation plan |
| `/speckit.tasks` | Break plan into actionable task list |
| `/speckit.analyze` | Audit the plan for gaps and risks |
| `/speckit.implement` | Execute the plan and generate code |

---

> *"For decades, code has been king. Spec-Driven Development changes this — specifications become executable, directly generating working implementations rather than just guiding them."* — GitHub Spec Kit
