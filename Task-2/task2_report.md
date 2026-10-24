# Curriculum Audit and Redesign Proposal
## B.Tech CSE (Artificial Intelligence) — Alignment with AI Automation Roles

---

**Course:** B.Tech CSE (Artificial Intelligence)
**Institution:** IFHE Hyderabad – ICFAI Tech School
**Batch:** 2023
**Assignment:** Task 2 – Curriculum Audit and Redesign
**Target Role:** Entry-Level AI Automation Intern
**Date:** October 2026

---

## 1. Introduction

For this task, I reviewed my own degree curriculum and compared it against real job postings for entry-level AI Automation roles. The goal was to identify what skills are missing or outdated and propose specific, credit-balanced changes to close those gaps.

---

## 2. Current Curriculum Baseline

**Programme:** B.Tech CSE (Artificial Intelligence), IFHE Hyderabad
**Total Credits:** 174 across 8 semesters + summer internship

| Semester | Credits | Focus Area |
|----------|---------|------------|
| Sem I | 21 | Engineering basics, Mathematics |
| Sem II | 22 | Programming, Chemistry, Maths |
| Sem III | 24 | DBMS, AI, Web Technologies |
| Sem IV | 25 | ML, Soft Computing, OS, OOP |
| Summer | 5 | Internship Program I |
| Sem V | 24 | Deep Learning, NLP, Big Data, Blockchain |
| Sem VI | 23 | Computer Vision, Special Project |
| Sem VII–VIII | 30 | Practice School / Thesis |
| **Total** | **174** | |

**What is missing:** Workflow automation tools (n8n, Zapier, RPA), cloud and CI/CD deployment, and responsible AI as a core subject — all absent from CSE-AI but present in industry job descriptions.

---

## 3. Job Market Analysis

I reviewed three job postings for entry-level AI Automation roles (all accessed in 2026):

**JD1 — AI Agent Engineer, General Motors** (July 2026, USA)
Required: Python, REST APIs, LLMs, RAG, vector databases, Docker, CI/CD, responsible AI.

**JD2 — AI Automation Specialist, Digital Mojo / Zuwa.ai** (September 2026, Hyderabad)
Required: n8n / Make / Zapier, API integration, Python scripting, agent building, error handling.

**JD3 — AI Process Automation Engineer, SoftOne Technologies** (October 2026, Hyderabad)
Required: Process mapping, automation pipeline testing, RPA basics, Python, audit trail documentation.

| Skill Required | JD1 | JD2 | JD3 | In My Curriculum? |
|----------------|-----|-----|-----|-------------------|
| Python / production coding | ✓ | ✓ | ✓ | Present |
| REST APIs and webhooks | ✓ | ✓ | ✓ | Partial |
| LLM apps and RAG | ✓ | ✓ | — | Partial |
| Workflow automation tools | — | ✓ | ✓ | **Absent** |
| Agent frameworks | ✓ | ✓ | — | **Absent** |
| Docker / CI-CD / Cloud | ✓ | — | — | **Absent** |
| Process mapping and testing | — | ✓ | ✓ | **Absent** |
| Responsible AI / ethics | ✓ | — | — | Elective only |

---

## 4. Proposed Changes

Total credits touched: **43 out of 174 (24.7%).** Total stays at 174 — every semester is credit-balanced.

### ADD — 3 New Courses (9 credits)

| Course | Semester | Credits | Reason |
|--------|----------|---------|--------|
| A1: AI Workflow Automation & Agent Engineering Lab | V | 4 | Workflow tools and agent building are in all 3 JDs but absent from the programme |
| A2: Cloud, Containers & CI/CD for AI Systems | IV | 3 | Docker and CI/CD are in the sister CSE programme but missing from CSE-AI |
| A3: AI Evaluation, Safety & Governance | V | 2 | Responsible AI is only an elective; JD1 lists it as a core requirement |

### REDUCE — 3 Courses Moved to Elective (9 credits freed)

| Course | Reason |
|--------|--------|
| AI211 Soft Computing (Sem IV, 3 cr) | Heavily overlaps with AI304 ML; not mentioned in any JD |
| AI301 Predictive Analytics (Sem V, 3 cr) | Overlaps with AI304 and AI305; content absorbed into updated ML course |
| AI303 Blockchain Technology (Sem V, 3 cr) | Not relevant to AI Automation roles; credits redirected to A3 |

### UPDATE — 7 Existing Courses Refreshed (25 credits, no credit change)

| Course | What Changes |
|--------|-------------|
| ES202 Industry Coding Practices | Add automated testing and packaging workflows |
| AI202 DBMS | Add vector indexing and embedding storage |
| AI208 Web Enabled Technologies | Add webhooks, OAuth, event-driven APIs |
| AI203 Artificial Intelligence | Add LLM agent concepts and tool use |
| AI304 Machine Learning | Add experiment tracking and evaluation frameworks |
| AI306 Natural Language Processing | Shift toward RAG, LLMs, and prompt engineering |
| SP301 Special Project | Require a deployed project with monitoring and audit trail |

### Semester Balance

| Semester | Before | After |
|----------|--------|-------|
| Sem IV | 25 | 25 (REDUCE AI211 −3 / ADD A2 +3) |
| Sem V | 24 | 24 (REDUCE AI301 & AI303 −6 / ADD A1 & A3 +6) |
| All others | unchanged | unchanged |
| **Total** | **174** | **174** |

---

## 5. Subject Exercises

Five problems from curriculum subjects, solved and verified:

| # | Subject | Problem | Answer | Verified |
|---|---------|---------|--------|---------|
| 1 | Algorithms (AI204) | T(n) = 3T(n/3) + n·log n — Master Theorem | Θ(n log²n) | ✓ |
| 2 | Databases (AI202) | Departments with avg salary > 60k, min 3 employees | SQL with HAVING clause | ✓ |
| 3 | Probability (BS105) | P(X ≥ 6) for Poisson λ=4 | 0.2149 | ✓ |
| 4 | Machine Learning (AI304) | TP=40, FP=10, FN=20, TN=930 — F1 score | F1 = 0.727 | ✓ |
| 5 | Operating Systems (AI205) | Round Robin (quantum=2ms): P1(0,6), P2(2,4), P3(4,2) | Avg wait = 4ms | ✓ |

---

## 6. Automation Lab Design (Linked to Task 1)

Course A1 is directly built on the club event approval workflow from Task 1.

**Students would:**
1. Map the approval process into steps with clear inputs, outputs, and owners
2. Build a rules engine that validates submissions and routes them to the right person
3. Handle failures with retries and a manual fallback
4. Ensure all approvals come from a human — the system never approves automatically
5. Maintain a timestamped audit log of every action
6. Calculate how much time the automated version saves vs. the manual process

**Why this works as a lab project:** Simple enough to build in one semester, realistic enough to cover every skill on the job descriptions — process mapping, API integration, error handling, human-in-the-loop design, audit logging, and ROI estimation.

---

## 7. What I Learned

The biggest gap in the CSE-AI programme is not depth — the core subjects are solid. The gap is in **practical tooling**: workflow automation platforms, deployment pipelines, and agent engineering are what entry-level roles ask for, and they are not taught anywhere in the current core. The most impactful change is not adding new courses but updating existing ones — a course called "Artificial Intelligence" that only covers classical search algorithms needs to move with the industry, even if the name stays the same.

---

*Job descriptions: JD1 (GM, July 2026), JD2 (Digital Mojo, September 2026), JD3 (SoftOne Technologies, October 2026)*
*Course data: IFHE programme structure page, accessed October 2026*
