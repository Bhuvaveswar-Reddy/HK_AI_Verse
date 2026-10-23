# Task 2: Curriculum Audit and Redesign Proposal

**Program:** B.Tech Computer Science & Engineering (Artificial Intelligence)  
**Institution:** ICFAI Tech School (IFHE Hyderabad)  
**Admission Batch:** 2023 Batch  
**Target Role:** Entry-Level AI Automation & Agent Engineering Intern  
**Date:** October 23, 2026  

---

## 1. Baseline & Program Scope

* **Baseline Credit Count:** **174 Credits** (calculated from published semester course tables).
* **Scope Limitations:** Official regulation documents and detailed course syllabi were unverified due to handbook access limits. Public structures establish the baseline, but exact course depth and prerequisites remain unexamined.

---

## 2. Redesign Summary

To align the degree with entry-level AI Automation roles, **24.7%** of the total programme credits are modified while maintaining a strictly balanced **174-credit total**.

| Change Type | Credits | Share of 174 Baseline | Description |
| :--- | :--- | :--- | :--- |
| **ADD (3 New Courses)** | 9 | 5.2% | Specialized workflow, cloud, and governance courses |
| **REDUCE (3 Core Swaps)** | 9 | 5.2% | Move overlapping core courses to elective status |
| **UPDATE (7 Refreshed)** | 25 | 14.4% | Modernize existing syllabi with vector DBs, APIs, & RAG |
| **Total Modified** | **43** | **24.7%** | Net modification percentage |

### Credit-Balanced Core Swaps
1. **Semester IV Swap (3 Credits):**  
   `ADD NEW-A2: Cloud, Containers & CI/CD` (3 cr) $\leftrightarrow$ `REDUCE AI211: Soft Computing` (3 cr).
2. **Semester V Swap (6 Credits):**  
   `ADD NEW-A1: AI Workflow & Agent Lab` (4 cr) + `NEW-A3: AI Safety & Governance` (2 cr) $\leftrightarrow$ `REDUCE AI1301: Predictive Analytics` (3 cr) + `AI1303: Blockchain Technology` (3 cr).

---

## 3. Evidence-Based Rationale & Job Mapping

Mapping industry requirements to curriculum changes:

| ID | Industry Requirement | Target Course & Action | Rationale |
| :--- | :--- | :--- | :--- |
| **R1** | Production Python & Testing | `ES202` (UPDATE) | Add automated testing, linting, and packaging workflows. |
| **R2** | Vector Databases & Embeddings | `AI1202` (UPDATE) | Add vector indexing alongside relational SQL. |
| **R3** | REST APIs, Webhooks, OAuth | `AI1208` (UPDATE) | Modernize web tech toward event-driven integration. |
| **R4** | AI Agents & Tool Building | `AI1203` (UPDATE) | Modernize AI core from search heuristics to LLM agents. |
| **R5** | ML Evaluation & Optimization | `AI1304` (UPDATE) | Absorb metaheuristics and experiment tracking. |
| **R6** | RAG, Prompting, LLMs | `AI1306` (UPDATE) | Shift NLP toward modern LLM application stacks. |
| **R7** | Monitoring & Logging | `SP301` (UPDATE) | Capstone requires failure recovery and live monitoring. |
| **R8** | Overlapping Core Theory | `AI211` (REDUCE) | Soft Computing overlaps ML; move to elective status. |
| **R9** | Overlapping Analytics | `AI1301` (REDUCE) | Predictive Analytics overlaps ML & Data Wrangling. |
| **R10** | Safety, Ethics, Governance | `AI1303` (REDUCE) / `NEW-A3` (ADD) | Swap Blockchain core for mandatory AI Safety & Ethics. |
| **R11** | Workflow Platforms (n8n, RPA) | `NEW-A1` (ADD) | Dedicated practical lab for process automation. |
| **R12** | Cloud Deployment & CI/CD | `NEW-A2` (ADD) | Bridges MLOps gap present in CSE but missing in CSE-AI. |

---

## 4. AI Capability Testing Summary

Five core subject exercises were evaluated using Claude Sonnet 5.5 and verified:

1. **Algorithms (`AI1204`):** Solved recurrence $T(n)=3T(n/3)+n\log_2 n$. Result: $\Theta(n\log^2 n)$ — **Verified**.
2. **Databases (`AI1202`):** Aggregation query with `HAVING` and nested subqueries — **Verified**.
3. **Probability & Statistics (`BS105`):** Poisson tail probability $P(X \ge 6)$ for $\lambda=4$.
   * *Model Output:* $0.2148$ (claimed $CDF(5)=0.7852$).
   * *Verification:* Exact $CDF(5)=0.78513$, giving $0.2149$. **Error caught and corrected.**
4. **Machine Learning (`AI1304`):** Confusion matrix ($TP=40, FP=10, FN=20, TN=930$). Derived $F1=0.727$, highlighted imbalanced baseline ($0.94$) — **Verified**.
5. **Operating Systems (`AI1205`):** Round-robin process scheduling queue evaluation — **Verified**.

---

## 5. Integrated Automation Lab Design

* **Host Course:** `NEW-A1: AI Workflow Automation & Agent Engineering Lab` (Semester V, 4 credits).
* **Learning Outcomes:** (1) Map complex processes into state machines, (2) Enforce strict **Human-in-the-Loop Approval Control**, (3) Build automated failure recovery, (4) Track append-only audit logs.
* **Synthetic Test Bench:** 60 synthetic event requests (70% valid, 10% incomplete, 5% duplicates, 5% unauthorized, 5% schedule clashes, 5% API failures).
* **Acceptance Suite (7/7 Passing):**
  * *Human Approval Gate:* Log must record explicit human ID; automated approvals fail test.
  * *Failure Recovery:* API timeout triggers retry sequence then falls back to manual review.
  * *Measured Value:* Time-saved arithmetic evaluated against synthetic baseline.

---

## 6. Regulatory Alternatives & Limitations

* **Institutional Compliance Path:** If adding new core courses is restricted by university governance, students can complete this curriculum via the 12-credit Choice-Based Elective slots (`AI1403 Responsible AI`, `AI1406 NoSQL`, `CS422 Software Architecture`).
* **Validation Limitations:** Unvalidated draft; no external faculty or graduate interviews conducted.

---

## Appendix: Concise Course Map (174 Total Baseline Credits)

| Sem | Baseline Credits | Proposed Changes & Status | Proposed Credits |
| :--- | :--- | :--- | :--- |
| **Sem I** | 21 | All courses UNCHANGED (`EG101`, `ES101`, `BS101`, `BS102`, `BS103`, `ES105`) | 21 |
| **Sem II** | 22 | All courses UNCHANGED (`EG102`, `ES102`, `ES103`, `ES104`, `BS104`, `ES106`, `ES107`) | 22 |
| **Sem III** | 24 | UPDATE `AI1202` (Vector DB), UPDATE `AI1203` (Agents). Rest UNCHANGED | 24 |
| **Sem IV** | 25 | UPDATE `ES202`, UPDATE `AI1208`; **REDUCE `AI211` (-3) / ADD `NEW-A2` (+3)** | 25 |
| **Summ** | 5 | Internship Program I UNCHANGED | 5 |
| **Sem V** | 24 | UPDATE `AI1304`; **REDUCE `AI1301` (-3) & `AI1303` (-3) / ADD `NEW-A1` (+4) & `NEW-A3` (+2)** | 24 |
| **Sem VI** | 23 | UPDATE `SP301`, UPDATE `AI1306`. Rest UNCHANGED | 23 |
| **Sem VII** | 15 | Practice School / Thesis / Elective Option UNCHANGED | 15 |
| **Sem VIII** | 15 | Practice School / Thesis / Elective Option UNCHANGED | 15 |
| **Total** | **174** | **43 Credits Touched (24.7%) | Net Swap Balance: 0 Credits** | **174** |
