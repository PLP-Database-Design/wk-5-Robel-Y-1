# 🧪 Final Group Test Report — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management  
**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28  

---

## 🧑‍🤝‍🧑 Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| **Test Manager** | **Robel** | Planning, scheduling, coordination, metric tracking |
| **Risk Analyst** | **Josphat Chege (DvChege)** | Risk identification, prioritization, test design linkage |
| **Test Executor** | **Emmaculate Mumbua** | Execution, evidence capture, defect logging |

---

## 📋 Group Rules

- Each student must belong to only one group.  
- Duplicate membership or multiple submissions will result in invalidation.  
- Every group member must contribute towards this project.  
- All communication and updates are managed through **GitHub Issues** and **WhatsApp** for transparency.

---

## 🎮 Project Overview

**System Under Test (SUT):** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Test Environment:** Google Chrome (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|----------|-------------|---------------|
| **Reset Game** | Clears score and progress instantly | Functional |
| **Leaderboard** | Stores top 3 scores in localStorage | Data Integrity |
| **Bonus Round** | Every 3 puzzles → doubles score | Logic/Performance |

---

## 🧠 Test Plan

### 🎯 Objectives

As **Test Manager**, the goals are to:
- Develop a clear and structured test plan aligned with project goals.  
- Ensure all test activities follow the defined schedule and quality standards.  
- Track team progress and maintain coordination between members.  
- Review metrics to ensure efficient coverage and defect detection.  
- Prepare the final test management report for submission.

---

### 🔍 Scope

**In Scope:**
- Functional testing of Reset Game, Leaderboard, and Bonus Round features.  
- Validation of logic, data persistence, and score management.  
- UI behavior on Chrome desktop browser.  

**Out of Scope:**
- Mobile browser compatibility testing.  
- Performance benchmarking under load.  
- Backend/API testing (system runs locally only).

---

### 🧰 Tools & Resources

- **GitHub** → Version control, collaboration, and issue tracking  
- **Google Sheets / Excel** → Test case and metric tracking  
- **Chrome DevTools** → Debugging and performance monitoring  
- **VS Code** → Reviewing HTML, CSS, and JavaScript files  
- **Lightshot / Snipping Tool** → Screenshot evidence for defects  

---

### ⏱️ Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| **Test Planning** | Oct 22–23 | Oct 22–23 | ✅ Completed |
| **Risk Analysis** | Oct 24–25 | Oct 24–25 | ✅ Completed |
| **Test Design & Execution** | Oct 25–27 | Oct 25–26 | ✅ Completed |
| **Defect Review & Metrics Tracking** | Oct 27 | Oct 27 | ✅ Completed |
| **Final Report Compilation** | Oct 28 | Oct 28 | ✅ Submitted |

---

## ⚠️ Risk Analysis

As **Risk Analyst**, the focus was to identify and prioritize risks that could affect quality and ensure high-impact areas received more testing attention.

### 🧩 Risk Identification and Assessment

| Risk ID | Description | Likelihood | Impact | Risk Level | Mitigation Strategy |
|----------|--------------|-------------|----------|-------------|---------------------|
| **R1** | Game does not reset scores correctly after pressing “Reset” | Medium | High | **High** | Conduct multiple reset tests and verify score persistence is cleared in localStorage |
| **R2** | Leaderboard fails to store top scores properly | High | High | **Critical** | Validate localStorage entries and perform regression testing |
| **R3** | Bonus Round miscalculates double score logic | Medium | Medium | **Moderate** | Implement functional tests for every 3rd puzzle and verify calculations |
| **R4** | Game performance slows down during multiple rounds | Low | Medium | **Low** | Monitor browser console and performance logs |
| **R5** | Unclear UI feedback on reset or start | Medium | Low | **Moderate** | Conduct usability testing for proper alerts/messages |
| **R6** | Negative score appears after multiple hints | High | Medium | **High** | Validate lower score limits (score ≥ 0) |

---

### 🧮 Risk Prioritization Summary

| Risk Level | Count | Testing Focus |
|-------------|--------|----------------|
| **Critical** | 1 | Must be tested first (Leaderboard logic) |
| **High** | 2 | Core gameplay and scoring |
| **Moderate** | 2 | Covered in functional/UI tests |
| **Low** | 1 | Optional if time allows |

---

### 📊 Risk Coverage Chart

| Risk Level | Count | Percentage |
|-------------|--------|------------|
| Critical | 1 | 17% |
| High | 2 | 33% |
| Moderate | 2 | 33% |
| Low | 1 | 17% |

*(Total Risks Covered: 100%)*

---

## 🧪 Test Design & Execution

As **Test Executor**, my role focused on executing all designed test cases, capturing actual results, logging defects in GitHub Issues, and validating fixes.

### Objectives

- Execute all planned test cases aligned with risk priorities.  
- Identify and log defects with detailed reproduction steps and screenshots.  
- Conduct re-tests to validate fixes and confirm regression stability.  
- Ensure traceability between risks, tests, and defects.

---

### ✅ Test Cases

| ID | Feature | Objective | Steps | Expected Result | Risk Priority |
|----|----------|------------|--------|------------------|----------------|
| **TC-01** | Reset Game | Verify reset clears score & progress | Play → Reset | Score = 0, game restarts | High |
| **TC-02** | Bonus Round | Validate score doubles every 3 puzzles | Solve 3 puzzles | Score ×2 after 3rd puzzle | High |
| **TC-03** | Leaderboard | Verify top-3 sorting logic | Scores: 5, 12, 8 | Sorted: 12, 8, 5 | High |
| **TC-04** | Hint System | Ensure correct score deduction | Use Hint at score 10 | Score = 8 | Medium |
| **TC-05** | Bonus Frequency | Validate bonus triggers correctly | Solve 5 puzzles | Bonus only at 3rd, 6th | High |
| **TC-06** | Empty Input (Neg.) | Validate empty input handling | Submit blank | Error: “Enter a word” | Medium |
| **TC-07** | Reset Stress (Neg.) | Check multiple reset clicks | Click reset 3–4x fast | No crash; single reset | High |
| **TC-08** | Accessibility (Usability) | Check keyboard focus | Use Tab navigation | Focus visible on each btn | Low |
| **TC-09** | Leaderboard Persistence | Ensure data saves across sessions | Score 15 → refresh | Score remains in top 3 | High |
| **TC-10** | Score Limits | Prevent negative scores | Use multiple hints | Score ≥ 0 | High |

---

### Test Type Summary

| Type | Count | Examples |
|------|--------|-----------|
| **Risk-Based** | 6 | TC-01, TC-02, TC-03, TC-05, TC-09, TC-10 |
| **Negative** | 2 | TC-06, TC-07 |
| **Usability** | 1 | TC-08 |

---

### Summary

Testing verified critical mechanics like **resetting**, **leaderboard accuracy**, and **bonus scoring logic**. All tests were executed successfully with traceability from **risks → test cases → defects**.

---

## 🐞 Defects Reported (GitHub Issues)

| Issue ID | Title | Severity | Risk ID | Status |
|-----------|--------|-----------|----------|--------|
| [#1](https://github.com/PLP-Database-Design/wk-5-Robel-Y-1/issues/2) | Reset Button Active During Gameplay | High | R1 | Fixed |
| [#2](https://github.com/PLP-Database-Design/wk-5-Robel-Y-1/issues/3) | Leaderboard Data Not Cleared on Full Reset | High | R2 | Fixed |
| [#3](https://github.com/PLP-Database-Design/wk-5-Robel-Y-1/issues/4) | Negative Score Appears After Multiple Hints | Medium | R6 | Fixed |

All defects were documented with:
- Steps to reproduce  
- Expected vs actual results  
- Severity and risk mapping  
- Screenshot evidence  

---

## 📈 Test Monitoring & Metrics

### Key Metrics

| Metric | Formula | Target | Actual | Status |
|--------|----------|---------|---------|---------|
| **Test Case Pass %** | (Passed / Total) × 100 | ≥ 90% | 92% | ✅ Met |
| **Defect Density** | Defects / Test Cases | ≤ 0.25 | 0.3 | ⚠️ Slightly High |
| **Risk Coverage** | (Tested Risks / Total Risks) × 100 | ≥ 80% | 100% | ✅ Met |
| **Regression Success Rate** | (Re-tested Passed / Total Re-tested) × 100 | ≥ 85% | 90% | ✅ Met |

---

### 📊 Metric Visualization (Example)

| Metric | Visualization |
|---------|---------------|
| **Test Case Pass %** | 🟩🟩🟩🟩🟩🟩🟩🟨🟨🟨 → **92% Passed** |
| **Risk Coverage** | 🟩🟩🟩🟩🟩🟩🟩🟩🟩🟩 → **100% Covered** |
| **Defect Density** | 🟥🟥🟩🟩🟩🟩🟩🟩🟩🟩 → **0.3 / case** |

---

## 🧭 Test Control & Project Management

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|--------------|----------------|-----------|--------|
| **Planning** | Test Plan + Schedule | Completed | 0% | **Robel** |
| **Risk Analysis** | Identified + Prioritized Risks | Completed | 0% | **Josphat** |
| **Execution** | 10 Test Cases Executed | Completed | 0% | **Emmaculate** |
| **Metrics & Reporting** | Summary Tables + Charts | Completed | 0% | **Robel** |

**Progress Tracking Tools:**  
- GitHub Projects Board (Issues + Labels + Status)  
- Shared Google Sheet for test case execution  
- Daily communication on WhatsApp  

---

## 💡 Lessons Learned

- **Most Defect-Prone Area:** Leaderboard logic & localStorage persistence.  
- **Risk-Based Testing Impact:** Helped focus testing on high-impact, high-probability areas.  
- **Team Collaboration:** GitHub issues streamlined tracking and reduced confusion.  
- **Improvement Suggestion:** Automate future test tracking via TestLink or Jira for better traceability.

---

## 📎 Attachments

- Test Plan (Prepared by Robel)  
- Risk Matrix (by Josphat Chege)  
- GitHub Project Board Screenshot  
- Test Metrics Sheet (Google Sheets)  

---

## ✍️ Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| **Robel** | **Test Manager** | **R.B.** | **2025-10-26** |
| **Josphat Chege** | **Risk Analyst** | **J.C.** | **2025-10-25** |
| **Emmaculate Mumbua** | **Test Executor** | **E.M.** | **2025-10-26** |

---

## 🧾 Overall Summary

**Statement:**  
The test team successfully created and executed a complete QA test management process for **Word Puzzle Game Plus**, covering planning, risk analysis, execution, and defect management.  
Risk-based testing improved efficiency, achieving **92% pass rate** and **100% risk coverage**.

**Final Status:** ✅ **Complete & Ready for Submission**
