# Club Event Approval Workflow Study
## Automation of a Manual College Process

---

**Course:** B.Tech CSE (Artificial Intelligence)
**Institution:** IFHE Hyderabad – ICFAI Tech School
**Batch:** 2023-2027

---

## Table of Contents

1. Introduction
2. Understanding the Current Process
3. Problems Identified
4. Proposed Improved Workflow
5. Evidence Log
6. Time Saving Estimate
7. Test Cases
8. Risks and Limitations
9. What I Learned

---

## 1. Introduction

For this task, I chose to study the **club event approval process** at my college. I picked this process because it is something I have heard friends talk about many times — getting permission for a club event involves a lot of waiting and follow-up messages, and it felt like a good candidate for a simple digital improvement.

I spoke to friends who are club leaders to understand how the process currently works. This report documents what I learned, how I would improve it, and what impact that improvement could have.

---

## 2. Understanding the Current Process

### 2.1 How It Works Today

The approval process works like this:

1. The **club leader** decides to hold an event and prepares a basic proposal.
2. The club leader **meets their assigned faculty advisor** — in person or over WhatsApp — and explains what the event is about.
3. The **faculty advisor reviews** the proposal. If they agree with it, they take it to the **higher authorities** (usually the Head of Department or the Student Affairs office).
4. The **higher authorities give final approval** or ask for changes.
5. Once approved, the club leader is informed and can go ahead with planning.

### 2.2 Current Process Flow

```
Club Leader
    |
    | (prepares proposal, contacts faculty over
    |  WhatsApp or in person)
    v
Faculty Advisor
    |
    | (reviews proposal, discusses with club leader
    |  if something is missing)
    v
Higher Authorities (HoD / Student Affairs)
    |
    | (gives final go-ahead or requests changes)
    v
Club Leader is Informed
    |
    v
Event Proceeds
```

---

## 3. Problems Identified

Through my conversations, a few recurring problems stood out:

| # | Problem | Impact |
|---|---------|--------|
| P1 | Club leader leaves out important details in the first message | Faculty has to ask follow-up questions, causing delays |
| P2 | Faculty and authorities are busy; responses come slowly | Club leader is left waiting with no idea of the status |
| P3 | Two clubs sometimes request the same venue on the same date | Conflict discovered late, causing last-minute changes |
| P4 | No formal record of the request or the approval | Disputes about what was agreed are hard to resolve |

These problems do not require artificial intelligence to fix. They need a structured form, a simple check for venue conflicts, and automatic notifications when something moves forward.

---

## 4. Proposed Improved Workflow

### 4.1 Core Idea

Add a lightweight digital system that sits between the existing steps. The system does only three things:

1. **Validates** that the submitted form is complete before passing it on.
2. **Checks** whether the requested venue and date are already taken.
3. **Sends notifications** so no one has to chase for updates.

The system does **not approve anything**. All decisions remain with the faculty advisor and the higher authorities, exactly as they are today.

### 4.2 Improved Process Flow

```
Club Leader fills online form
    |
    v
System: Is the form complete?
    |-- No  --> Club Leader gets a message asking them to fill the missing fields
    |
    v
System: Is the venue free on that date?
    |-- No  --> Club Leader is told about the conflict and asked to pick another slot
    |
    v
Faculty Advisor receives a clean summary notification
    |
    v
Faculty Advisor approves (or sends it back with a comment)
    |
    v
Higher Authorities (Student Affairs) receive a notification
    |
    v
Final approval given --> Club Leader is automatically notified
```

### 4.3 Design Decisions

| Decision | Reasoning |
|----------|-----------|
| Humans still approve everything | The faculty and administration hold authority. The system is a helper, not a decision-maker. |
| Simple rules, not AI | The checks needed (is the form complete? is the venue free?) are yes/no questions. A rules-based system is cheaper, easier to explain to staff, and easier to test than a machine learning model. |
| Manual fallback always available | If the digital system goes down or a faculty member prefers WhatsApp, the old process works exactly as before. Nothing breaks. |
| Every action is logged | A timestamped record of who submitted what and when means there is no confusion later about what was approved. |

---

## 5. Evidence Log

| Entry | Date | Type | Description |
|-------|------|------|-------------|
| E1 | 2026-10-22 | Peer input | Friends who are club leaders described the three-step flow: club leader → faculty advisor → higher authorities. |
| E2 | 2026-10-22 | Observation | Volume estimate: approximately 10–30 event requests per month across all clubs combined. |
| E3 | 2026-10-22 | Observation | Time estimates (Section 6) are based on conversations with club leaders and personal observation. |
| E4 | 2026-10-22 | Test result | 5 synthetic test cases run through the proposed routing logic. All 5 produced the expected result. |
| E5 | 2026-10-22 | Observation | The informal WhatsApp-based communication is the primary source of delays and missed follow-ups. |

---

## 6. Time Saving Estimate

### 6.1 Current Time Per Request

| Step | Person Involved | Estimated Time |
|------|----------------|----------------|
| Writing and sending the proposal | Club leader | 20 minutes |
| Faculty review and follow-up messages | Faculty advisor | 30 minutes |
| Passing to higher authorities and waiting | Faculty + Student Affairs | 25 minutes |
| Informing the club leader | Student Affairs | 10 minutes |
| **Total** | | **~85 minutes per request** |

At 20 requests per month: **85 × 20 = 1,700 minutes ≈ 28 hours/month**

### 6.2 Proposed Time Per Request

| Step | Person Involved | Estimated Time |
|------|----------------|----------------|
| Filling the online form | Club leader | 10 minutes |
| Automatic validation and venue check | System | <1 minute |
| Faculty review (pre-validated, cleaner information) | Faculty advisor | 15 minutes |
| Automatic notification to higher authorities | System | <1 minute |
| Final approval | Student Affairs | 10 minutes |
| Automatic notification to club leader | System | 0 minutes |
| **Total** | | **~35 minutes per request** |

At 20 requests per month: **35 × 20 = 700 minutes ≈ 12 hours/month**

### 6.3 Summary

| Measure | Current | Proposed | Difference |
|---------|---------|----------|------------|
| Time per request | ~85 minutes | ~35 minutes | ~50 minutes saved |
| Time for 20 requests/month | ~28 hours | ~12 hours | **~16 hours saved** |

**Break-even estimate:** Building a basic version (a form, a rules checker, and email notifications) would take roughly 60 hours of part-time work. At 16 hours saved per month, the effort would pay for itself in about **4 months**.

---

## 7. Test Cases

To verify that the routing logic works correctly, I wrote a simple Python script and ran five test cases through it.

| # | Test Name | Scenario | Expected Outcome | Result | Pass |
|---|-----------|----------|-----------------|--------|------|
| T1 | Complete valid request | Form fully filled, venue is free | Request moves to faculty review | Moved to faculty review | ✓ |
| T2 | Incomplete form | Venue field left blank | System returns request to club leader for correction | Returned with correction message | ✓ |
| T3 | Venue conflict | Requested venue already booked on that date | System notifies club leader of conflict | Conflict notification sent | ✓ |
| T4 | Duplicate submission | Same club submits the same event a second time | Request flagged, held for manual check | Flagged and held | ✓ |
| T5 | Unauthorised submitter | Person not in the club tries to submit a request | Request held, not routed forward | Held, not routed | ✓ |

**All 5 of 5 test cases passed.**

---

## 8. Risks and Limitations

| Risk | Why It Matters | Suggested Approach |
|------|----------------|-------------------|
| Faculty prefer WhatsApp over a formal system | A form they are forced to use will be ignored | Make the system optional at first; demonstrate usefulness before making it the default |
| No digital venue calendar exists | The venue-conflict check needs data to work | Start with a shared Google Calendar maintained by one person |
| Club rosters may be out of date | Valid submissions could get incorrectly flagged | Assign a club coordinator responsibility for keeping the roster current |
| Event volume may be very low | If there are only 3–4 events per month, the build effort may not be justified | Count actual requests for one month before committing to build |

---

## 9. What I Learned

This was my first time formally mapping out a process and thinking about how to improve it with automation. A few things stood out to me:

**Rules are often enough.** Before this exercise, I assumed any automation project would involve machine learning or an AI model. But once I drew out the actual steps, I realised everything the system needs to do is a simple yes/no check. A rules-based approach is not less sophisticated — in many cases it is the better engineering choice because it is predictable and easy to maintain.

**The biggest problem is visibility, not speed.** My estimate shows about 50 minutes saved per request. But what club leaders actually complained about was not knowing where their request was. A simple status tracker — "submitted, with faculty, with HoD, approved" — would solve most of the frustration even without complex automation.

**Measurement comes before building.** Real automation work starts with understanding the actual numbers, not with building first and hoping the improvement shows up later.

---

*Test implementation: `scripts/task1_workflow.py` — 5 test cases, all passing.*
*Effort model: `scripts/task1_model.py`*

