# 🧪 Final Group Test Report — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

---

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| **Test Manager** | **Robel** | Planning, scheduling, coordination, metric tracking |
| **Risk Analyst** | **Josphat Chege (DvChege)** | Risk identification, prioritization, test design linkage |

| Test Executor | | Execution, evidence capture, defect logging |

---

## Group Rules

- Each student must belong to only one group.  
- Duplicate membership or multiple submissions will result in invalidation.  
- Every group member must contribute towards this project.  
- All communication and updates will be managed through GitHub Issues and WhatsApp for transparency.

---

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | Functional |
| Leaderboard | Stores top 3 scores in localStorage | Data Integrity |
| Bonus Round | Every 3 puzzles → doubles score | Logic/Performance |

---

## Test Plan

### 🎯 Objectives

As **Test Manager**, my objective is to:
- Develop a clear and structured test plan aligned with project goals.  
- Ensure all test activities follow the defined schedule and quality standards.  
- Track team progress and maintain coordination between members.  
- Review metrics to ensure efficient coverage and defect detection.  
- Prepare the final test management report for submission.

### 🔍 Scope

**In Scope:**
- Functional testing of Reset Game, Leaderboard, and Bonus Round features.  
- Validation of logic, data persistence, and score management.  
- UI behavior on Chrome desktop browser.  

**Out of Scope:**
- Mobile browser compatibility testing.  
- Performance benchmarking under load.  
- Backend/API testing (the system runs locally in browser only).

---

### 🧰 Tools & Resources

- **GitHub** → Version control, collaboration, issue tracking.  
- **Google Sheets / Excel** → Tracking test cases and metrics.  
- **Chrome DevTools** → Debugging UI and JavaScript behavior.  
- **VS Code** → Code review and file updates.  
- **Screenshot Tools (Lightshot / Snipping Tool)** → Defect evidence capture.

---

### ⏱️ Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| **Test Planning** | Oct 22–23 | Oct 22–23 | ✅ Completed |
| **Risk Analysis** | Oct 24–25 |  | Oct 24-25 |✅ Completed |
| **Test Design & Execution** | Oct 25–27 |  | ☐ In Progress |
| **Defect Review & Metrics Tracking** | Oct 27 |  | ☐ Pending |
| **Final Report Compilation** | Oct 28 |  | ☐ Scheduled |

---

## Risk Analysis
##  Risk Analysis  

As **Risk Analyst**, my objective is to identify, assess, and prioritize risks that could affect the quality and success of the Word Puzzle Game Plus project. The analysis ensures that high-impact areas receive proper testing attention and that mitigation plans are in place.  

###  Objectives  
- Identify potential risks that could disrupt testing or gameplay.  
- Evaluate the likelihood and impact of each risk.  
- Recommend mitigation strategies and link them to relevant test cases.  

---

###  Risk Identification and Assessment  

| Risk ID | Description | Likelihood | Impact | Risk Level | Mitigation Strategy |
|----------|--------------|-------------|----------|--------------|---------------------|
| **R1** | Game does not reset scores correctly after pressing “Reset” | Medium | High | **High** | Conduct multiple reset tests and verify score persistence is cleared in localStorage |
| **R2** | Leaderboard fails to store top scores properly | High | High | **Critical** | Validate localStorage entries after each game and perform regression testing |
| **R3** | Bonus Round logic miscalculates double score | Medium | Medium | **Moderate** | Implement functional test cases for every third puzzle; verify calculation accuracy |
| **R4** | Game performance slows down during multiple puzzle rounds | Low | Medium | **Low** | Monitor browser console performance and memory usage |
| **R5** | Unclear UI feedback when resetting or starting new round | Medium | Low | **Moderate** | Conduct usability testing to ensure user messages and alerts are visible |

---

###  Risk Prioritization Summary  

| Risk Level | Count | Testing Focus |
|-------------|--------|----------------|
| **Critical** | 1 | Must be tested first (Leaderboard logic) |
| **High** | 1 | Second priority — affects score integrity |
| **Moderate** | 2 | Covered in functional and UI testing |
| **Low** | 1 | Optional if time allows |

---

###  Risk-Based Testing Approach  
Testing will follow a **risk-based prioritization** model:  
1. Begin with **Critical and High** risks (Leaderboard and Reset Game).  
2. Continue with **Moderate** UI and logic risks.  
3. Perform exploratory testing on Low-priority risks if time permits.  

Each identified risk is linked to corresponding test cases and defect reports to ensure traceability and control.  

---

###  Summary  
The risk analysis highlights that **data persistence and score accuracy** are the highest-impact areas for the Word Puzzle Game Plus. Focusing test efforts here will reduce the likelihood of major user experience issues and improve system reliability before release.


---

## Test Cases

*(Handled by the Test Executor — section left blank.)*

---

## Defects

*(Handled by the Test Executor — section left blank.)*

---

## Metrics

As **Test Manager**, I am responsible for tracking progress and quality metrics.  
The following metrics will be used to measure testing effectiveness:

| Metric | Formula | Target | Purpose |
|--------|----------|---------|----------|
| Test Case Pass Rate | (Passed / Total) × 100 | ≥ 90% | Ensure sufficient coverage |
| Defect Density | Defects / Test Cases | ≤ 0.25 | Identify defect frequency |
| Risk Coverage | (Tested Risks / Total Risks) × 100 | ≥ 80% | Confirm focus on high-risk areas |
| Regression Success Rate | (Re-tested Passed / Total Re-tested) × 100 | ≥ 85% | Validate post-fix stability |

**Metric Tracking Approach:**  
Progress and results will be recorded in a shared Google Sheet linked to GitHub Issues, with daily updates from all members.

---

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|--------------|----------------|-----------|--------|
| **Planning** | Test Plan + Schedule | Completed | 0% | **Robel** |
| **Coordination** | Task Distribution + GitHub Setup | Completed | 0% | **Robel** |
| **Progress Tracking** | Weekly Report + Metrics | In Progress | 10% | **Robel** |
| **Report Compilation** | Final Consolidated Report | Pending | - | **Robel** |

**Progress Tracking Method:**  
- GitHub Issues board for test execution and defect status.  
- Group check-ins every 2 days for task updates.  
- Status tracked using simple traffic lights (🟢 On Track, 🟡 Delayed, 🔴 Risk).

**Change Control Notes:**  
Any schedule adjustments or test case updates must be approved by the Test Manager to maintain consistency.

---

## Lessons Learned

- **Most Defect-Prone Area (Expected):** Leaderboard logic and localStorage data persistence.  
- **Risk Analysis Impact:** Helped narrow testing scope toward functional and logic-based risks first.  
- **Team Communication:** Coordination via GitHub Issues was efficient; fewer misunderstandings.  
- **Improvements for Next Cycle:** Use automated test tracking tools (like TestLink or Jira) for better traceability.

---

## Attachments

- Test Plan (Prepared by Robel)  
- GitHub Project Board Screenshots (Progress Tracking)  
- Metrics Spreadsheet  

---

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| **Robel** | **Test Manager** | **R.B.** | **2025-10-26** |
|  | Risk Analyst |  |  |
|  | Test Executor |  |  |

---

## Overall Summary

**Statement:**  
The Test Manager successfully created the project plan, coordinated schedules, and established the progress-tracking framework. The next steps will focus on risk analysis, test execution, and final report consolidation.

**Test Status:** ✅ In Progress
