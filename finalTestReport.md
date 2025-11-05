# 🧪 Final Group Test Report — React Web Application

**Level:** Intermediate QA | **Week 5:** Test Management
**Course:** Software Testing & Quality Assurance
**Module:** Test Management (Week 5)
**Project Type:** Group Assessment
**Submission Date:** 2025-11-05

---

## 👥 Team Information

| Role          | Name         | Responsibilities                                         |
| ------------- | ------------ | -------------------------------------------------------- |
| Test Manager  | Bett Romanus | Planning, scheduling, coordination, metric tracking      |
| Risk Analyst  | James Nganga | Risk identification, prioritization, test design linkage |
| Test Executor | Ruth Wangui  | Execution, evidence capture, defect logging              |

---

## 📜 Group Rules

* Each student must belong to only one group.
* Duplicate membership or multiple submissions will result in invalidation.
* Every group member must contribute towards this project.

---

## 💡 Project Overview

**System Under Test:** React Web Application
**Technology Stack:** React.js, JavaScript, CSS
**Environment:** Chrome Browser (Desktop & Mobile, Version 129+)

### Features Under Test

| Feature          | Description                                          | Risk Category |
| ---------------- | ---------------------------------------------------- | ------------- |
| Registration     | Allows user signup with validation                   | High          |
| Login            | Authenticates registered users                       | High          |
| Navigation Bar   | Provides access to app pages; responsive menu design | Medium        |
| Comments Section | Allows commenting on posts                           | Medium        |
| Search Articles  | Returns posts matching user search input             | High          |

---

## 🧩 1️⃣ Test Plan

### Objectives

* Verify registration and login workflows for user authentication.
* Validate responsive design of the navigation bar on various screen sizes.
* Ensure comment persistence across page reloads.
* Test article search functionality for expected result matching.

### Scope

**In Scope:**

* Functional testing (register, login, comments, search).
* UI and responsive layout validation.
* Risk-based and regression testing.

**Out of Scope:**

* Backend database integration testing.
* API-level automation.

### Resources

**Roles:** Defined above.
**Tools Used:**

* Chrome DevTools
* GitHub Issues (defect tracking)
* Google Sheets (test case management)
* Snipping Tool (evidence screenshots)

### Schedule

| Phase       | Planned Duration | Actual Duration | Status      |
| ----------- | ---------------- | --------------- | ----------- |
| Planning    | 1 day            | 1 day           | ✅ Completed |
| Test Design | 1 day            | 1 day           | ✅ Completed |
| Execution   | 2 days           | 2 days          | ✅ Completed |
| Reporting   | 1 day            | 1 day           | ✅ Completed |

### Entry Criteria

* Application build deployed locally and accessible.
* Stable features for register, login, and search modules.

### Exit Criteria

* 100% test case execution.
* All high-severity defects logged and tracked.

### Environment

* **Browser:** Chrome (Desktop, Mobile)
* **OS:** Windows 11 / macOS Sonoma
* **Devices:** 13” laptop, Android mobile device

---

## ⚠️ 2️⃣ Risk Analysis

### Identified Risks

| ID | Feature        | Risk Description                                    | Likelihood | Impact | Priority | Mitigation Strategy                   |
| -- | -------------- | --------------------------------------------------- | ---------- | ------ | -------- | ------------------------------------- |
| R1 | Registration   | No confirmation message on successful signup        | High       | Medium | High     | Implement success alert after signup  |
| R2 | Login          | Allows login with any password or unregistered user | High       | High   | Critical | Fix backend validation logic          |
| R3 | Navbar         | Unresponsive and obstructs content on mobile        | Medium     | High   | High     | Add hamburger menu or CSS media query |
| R4 | Comments       | Comments disappear after refresh                    | High       | Medium | High     | Ensure persistent storage (API/local) |
| R5 | Search Feature | Always returns hardcoded result                     | High       | High   | High     | Connect input query to dynamic fetch  |
| R6 | Validation     | Allows single-character usernames/passwords         | Medium     | Medium | Medium   | Add regex-based input validation      |

### Risk Coverage

🟢 **High Risks:** R1, R2, R3, R4, R5
🟠 **Medium Risk:** R6
**Tested Risks Percent:** 100%

---

## 🧠 3️⃣ Test Design & Execution

### Test Cases

| ID    | Feature         | Objective                                | Steps                                   | Expected Result                    | Actual Result                   | Status          | Risk Link |
| ----- | --------------- | ---------------------------------------- | --------------------------------------- | ---------------------------------- | ------------------------------- | --------------- | --------- |
| TC-01 | Registration    | Check registration confirmation message  | Register new user                       | Success alert shown                | No alert shown                  | ❌ Fail          | R1        |
| TC-02 | Login           | Validate correct login restriction       | Attempt login with invalid credentials  | Error message shown, login blocked | Login successful with any input | ❌ Fail          | R2        |
| TC-03 | Login           | Validate unregistered user login attempt | Try to login with non-existent account  | Should deny login                  | Allows access                   | ❌ Fail          | R2        |
| TC-04 | Navbar          | Test responsive behavior                 | Resize browser to mobile width          | Collapses neatly without overlap   | Blocks page content             | ❌ Fail          | R3        |
| TC-05 | Comments        | Check comment persistence                | Post comment → Refresh page             | Comment remains visible            | Comment disappears              | ❌ Fail          | R4        |
| TC-06 | Search          | Verify correct search output             | Enter search term, e.g., “React”        | Returns posts matching “React”     | Always same hardcoded result    | ❌ Fail          | R5        |
| TC-07 | Form Validation | Validate input restrictions              | Enter blank or 1-char username/password | Reject short or blank inputs       | Rejects blanks, accepts short   | ⚠️ Partial Pass | R6        |

---

## 🪲 4️⃣ Defect Reporting

| ID | Issue Title                                          | Severity | Risk ID | Status | GitHub Link |
| -- | ---------------------------------------------------- | -------- | ------- | ------ | ----------- |
| D1 | No registration confirmation message displayed       | Medium   | R1      | Open   | —           |
| D2 | Login accepts any password or non-registered user    | Critical | R2      | Open   | —           |
| D3 | Navbar blocks content on small screens               | High     | R3      | Open   | —           |
| D4 | Comments lost after page reload                      | High     | R4      | Open   | —           |
| D5 | Search always returns static result                  | High     | R5      | Open   | —           |
| D6 | Single-character credentials allowed on registration | Medium   | R6      | Open   | —           |

---

## 📊 5️⃣ Test Monitoring & Metrics

| Metric                  | Description            | Result    |
| ----------------------- | ---------------------- | --------- |
| Test Case Pass %        | (1 / 7) × 100          | **14.3%** |
| Defect Density          | (6 defects / 7 cases)  | **0.86**  |
| Risk Coverage           | (6 / 6) × 100          | **100%**  |
| Regression Success Rate | N/A (first test cycle) | —         |

### Charts Summary

🔴 Failed — 85.7%
🟢 Passed — 14.3%
🟠 Risk Coverage — 100%

---

## 🧭 6️⃣ Test Control & Project Management

| Phase     | Deliverable  | Actual Output | Variance | Owner |
| --------- | ------------ | ------------- | -------- | ----- |
| Planning  | Test Plan    | Delivered     | 0%       | Bett  |
| Design    | Test Cases   | Delivered     | 0%       | James |
| Execution | Test Results | Delivered     | 0%       | Ruth  |
| Reporting | Final Report | Delivered     | 0%       | All   |

**Progress Tracking Method:** Google Sheets & GitHub Issues
**Change Control Notes:** Added responsive UI testing after initial discovery of navbar issue.

---

## 💬 Reflection

### Lessons Learned

* **Most Defect-Prone Feature:** Login and Search functionality.
* **Risk Analysis Impact:** Helped prioritize high-risk authentication and UI areas.
* **Collaboration Effectiveness:** Defect documentation and role division improved focus.
* **Improvements for Next Cycle:** Implement automated end-to-end tests using Jest & React Testing Library.

---

## 📎 Attachments

---

## ✅ Sign Off

| Name         | Role          | Initials | Date       |
| ------------ | ------------- | -------- | ---------- |
| Bett Romanus | Test Manager  | BR       | 2025-11-05 |
| James Nganga | Risk Analyst  | JN       | 2025-11-05 |
| Ruth Wangui  | Test Executor | RW       | 2025-11-05 |

---

## 🏁 Overall Summary

**Statement:**
Testing revealed multiple critical defects in core authentication and search modules. Risk-based prioritization ensured key problem areas were identified early. The team recommends a full regression cycle after code fixes and backend validation updates.

**Test Status:** 🔴 Testing Completed with Critical Defects Logged
