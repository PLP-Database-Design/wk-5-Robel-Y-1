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
| **Test Executor** | **Emmaculate Mumbua**| Execution, evidence capture, defect logging |

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
| **Risk Analysis** | Oct 24–25 | Oct 24–25 | ✅ Completed |
| **Test Design & Execution** | Oct 25–27 | Oct 25–26 | ✅ Completed |
| **Defect Review & Metrics Tracking** | Oct 27 |  |✅ Completed |
| **Final Report Compilation** | Oct 28 |  | ✅ Completed |

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

## Test design and execution

As the **Test Executor**, my role focused on executing all designed test cases, capturing actual results, logging defects in GitHub Issues, and validating bug fixes through re-tests. 

### Objectives
- Execute all planned functional, negative, and usability test cases aligned with risk priorities.
- Identify and log any defects discovered during testing, complete with screenshots or reproduction steps.
- Re-test fixed issues to confirm stability and ensure no regressions occurred.
- Support overall project quality by maintaining accuracy, consistency, and traceability throughout execution.

### Test Cases
Below are the designed and executed test cases for the Word Puzzle Game Plus system.
Testing focused on functionality, logic correctness, risk-prone areas, and usability.

#### **TC-01 — Reset Game**  
**Feature:** Reset Game  
**Objective:** Verify that resetting clears score and progress instantly.  
**Steps:**  
1. Play two puzzles to accumulate score.  
2. Click **“Reset”** button.  
3. Observe score and puzzle state.  
**Expected Result:** Score resets to **0** and the first puzzle appears again.  
**Risk Priority:** **High**  

#### **TC-02 — Bonus Round (Score Doubling)**  
**Feature:** Bonus Round  
**Objective:** Verify score doubling after every 3 puzzles.  
**Steps:**  
1. Solve 3 puzzles correctly.  
2. Check score before and after 3rd completion.  
**Expected Result:** Score is doubled automatically after the 3rd puzzle.  
**Risk Priority:** **High**  

#### **TC-03 — Leaderboard Sorting**  
**Feature:** Leaderboard  
**Objective:** Verify top-3 sorting logic.  
**Steps:**  
1. Achieve scores **5**, **12**, and **8**.  
2. Open leaderboard view.  
**Expected Result:** Scores sorted in descending order → **12, 8, 5**.  
**Risk Priority:** **High**  

#### **TC-04 — Hint System Deduction**  
**Feature:** Hint System  
**Objective:** Ensure hint deducts correct points from total score.  
**Steps:**  
1. Play a puzzle with score **10**.  
2. Click **“Hint.”**  
3. Check updated score.  
**Expected Result:** **2 points deducted → new score = 8.**  
**Risk Priority:** **Medium**  

#### **TC-05 — Bonus Round Trigger Frequency**  
**Feature:** Bonus Round  
**Objective:** Validate that bonus triggers exactly every 3 puzzles.  
**Steps:**  
1. Solve puzzles **1–5** in sequence.  
2. Monitor bonus triggers.  
**Expected Result:** Bonus applies after **puzzle 3** and **puzzle 6** only.  
**Risk Priority:** **High**  

#### **TC-06 — Empty Input Validation (Negative Test)**  
**Feature:** Input Field Validation  
**Objective:** Verify that submitting an empty input shows an error message.  
**Steps:**  
1. Click **“Submit”** without typing any guess.  
2. Observe system response.  
**Expected Result:** Validation error displayed — “Please enter a word.”  
No crash or score change.  
**Risk Priority:** **Medium**  

#### **TC-07 — Reset Button Stress (Negative Test)**  
**Feature:** Reset Button  
**Objective:** Check game behavior when clicking “Reset” repeatedly.  
**Steps:**  
1. Click **“Reset”** button 3–4 times quickly.  
2. Observe any lag or errors.  
**Expected Result:** Game resets once; no freezing or multiple triggers.  
**Risk Priority:** **High**  

#### **TC-08 — Keyboard Accessibility (Usability Test)**  
**Feature:** Button Focus / Navigation  
**Objective:** Verify accessibility for keyboard navigation.  
**Steps:**  
1. Use **Tab** key to move through buttons (Submit, Hint, Reset).  
2. Check focus visibility.  
**Expected Result:** Each button gets a clear visual outline when focused.  
**Risk Priority:** **Low**  

#### **TC-09 — Leaderboard Persistence**  
**Feature:** Leaderboard  
**Objective:** Ensure leaderboard data saves across sessions.  
**Steps:**  
1. Play and score **15 points.**  
2. Refresh browser or reopen game.  
**Expected Result:** Score remains visible in the **top 3 leaderboard list.**  
**Risk Priority:** **High**  

#### **TC-10 — Score Calculation Limits**  
**Feature:** Score Calculation  
**Objective:** Confirm no negative score appears after using multiple hints.  
**Steps:**  
1. Use **Hint** 4 times without solving any puzzle.  
2. Check current score.  
**Expected Result:** Score cannot go below zero (**minimum = 0**).  
**Risk Priority:** **High**  

---

### Summary of Test Types:

| **Type** | **Count** | **Examples** |
|-----------|------------|--------------|
| **Risk-Based** | 6 | TC-01, TC-02, TC-03, TC-05, TC-09, TC-10 |
| **Negative** | 2 | TC-06, TC-07 |
| **Usability** | 1 | TC-08 |


### Summary
Through systematic testing and detailed reporting, I verified the game’s key mechanics—such as score resetting, leaderboard accuracy, and bonus round logic—ensuring that Word Puzzle Game Plus met functional expectations and delivered a consistent user experience.

---

## Defects

All identified defects were logged and tracked on GitHub for traceability and evidence.

**Logged Issues:**
- [#1-Reset Button Active During Gameplay](https://github.com/PLP-Database-Design/wk-5-Robel-Y-1/issues/2#issue-3553699642)  
  *Severity:* High | *Risk:* R1 (Reset Functionality)
- [#2 – Leaderboard Data Not Cleared on Full Reset](https://github.com/PLP-Database-Design/wk-5-Robel-Y-1/issues/3#issue-3553712585)  
  *Severity:* High | *Risk:* R2 (Leaderboard Logic)
- [#3 –Negative Score Appears After Multiple Hints ](https://github.com/PLP-Database-Design/wk-5-Robel-Y-1/issues/4#issue-3553780108)  
  *Severity:* Medium | *Risk:* R2 (Score Calculation)

 *Each issue includes: steps to reproduce, expected vs. actual result, severity, risk mapping, and screenshot evidence.*

### Summary of Findings
- The Leaderboard persistence defect - was the most critical, linked to high data integrity risk (R2).
- Reset functionality defect - revealed a usability gap requiring confirmation before progress loss.
- Negative Score Appears After Multiple Hints -affected gameplay logic but did not cause system crashes.

*All defects were documented with reproducible steps, screenshots, and assigned severity in GitHub. Fixes were validated through regression testing.*

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
| **Josphat Chege** | **Risk Analyst** | **J.C.** | **2025-10-25** |
| **Emmaculate Mumbua** | **Test Executor** | **E.M.** | **2025-10-26** |

---

## Overall Summary

**Statement:**  
The Test Manager successfully created the project plan, coordinated schedules, and established the progress-tracking framework. The next steps will focus on risk analysis, test execution, and final report consolidation.

**Test Status:** ✅ Completed
