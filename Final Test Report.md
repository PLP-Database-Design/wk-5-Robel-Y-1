# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | | Planning, scheduling, coordination, metric tracking |
| Risk Analyst | | Risk identification, prioritization, test design linkage |
| Test Executor | | Execution, evidence capture, defect logging |

## Group Rules

- Each student must belong to only one group.
- Duplicate membership or multiple submissions will result in invalidation.
- Every group member must contribute towards this project

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | |
| Leaderboard | Stores top 3 scores in localStorage | |
| Bonus Round | Every 3 puzzles → doubles score | |

## Test Plan

### Objectives

- 

### Scope

**In Scope:**
- 

**Out of Scope:**
- 

### Tools & Resources

- 

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| | | | |

##  Risk Analysis

### Risks

| **ID** | **Feature** | **Risk Description** | **Likelihood** | **Impact** | **Priority** | **Mitigation Strategy** |
|:--|:--|:--|:--|:--|:--|:--|
| R1 | Reset Game | Player accidentally clicks “Reset,” losing all progress and scores. | Medium | High | High | Add a confirmation prompt before resetting the game. |
| R2 | Leaderboard | Local storage may be cleared or unsupported, causing score loss. | High | Medium | High | Alert players that leaderboard data is browser-based and can be lost. |
| R3 | Bonus Round | Bonus logic (score ×2 after 3 puzzles) might fail due to calculation errors. | Medium | High | High | Validate bonus trigger logic with functional testing and debugging. |
| R4 | Hint Button | Multiple hints could be triggered or cost points incorrectly. | Medium | Medium | Medium | Disable hint button after first use and test deduction consistency. |
| R5 | Input Validation | Empty or invalid guesses may break validation flow. | Low | High | Medium | Add proper input checks and display user-friendly error messages. |
| R6 | UI Responsiveness | Layout may break or overlap on small screens. | High | Medium | High | Perform responsive testing on multiple devices and browsers. |
| R7 | Accessibility | Screen reader users may miss game feedback. | Medium | Low | Medium | Improve ARIA roles and live status updates. |
| R8 | Browser Compatibility | Different browsers may render localStorage or DOM updates differently. | Medium | Medium | Medium | Test across Chrome, Firefox, Safari, and Edge. |
| R9 | Performance | Frequent DOM changes might slow gameplay. | Low | Medium | Low | Optimize script execution and limit unnecessary updates. |

---

### Risk Coverage

| **Tested Risks Percent** | **Untested Risks Percent** |
|:--|:--|
| 85% | 15% |

---

### Summary Notes

- **High priority risks (R1, R2, R3, R6)** require focused regression and boundary testing.  
- Functional and responsive UI testing covers most identified risks.  
- LocalStorage and user interactions should be revalidated after major code updates.

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
| | | | | | | |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
| | | | | | |

## Metrics

- Test Case Pass Percent: 
- Defect Density: 
- Risk Coverage Percent: 
- Regression Success Rate: 

### Defect Summary

- Total Defects Logged: 
- Critical High: 
- Fix Rate: 

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| | | | | |

**Progress Tracking Method:**  
**Change Control Notes:**

## Lessons Learned

- Most Defect Prone Feature: 
- Risk Analysis Impact: 
- Team Communication Effectiveness: 
- Improvements for Next Cycle: 

## Attachments

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| | Test Manager | | |
| | Risk Analyst | | |
| | Test Executor | | |

## Overall Summary

**Statement:** 

**Test Status:** ☐ Completed / ☐ In Progress / ☐ Deferred
