# Foreign Classroom Student Portal

## UAT Test Scenarios & Results

**Document Type:** User Acceptance Testing
**Project:** Foreign Classroom Student Portal
**Role:** Business Analyst
**Status:** Portfolio Reconstruction
**Confidentiality:** Anonymized

---

## 1. Purpose

The purpose of User Acceptance Testing (UAT) was to validate that the platform's functionality aligned with documented business requirements and supported the expected user journeys.

Testing was approached from the perspective of business users rather than focusing only on technical functionality.

The primary objective was to determine whether the solution was suitable for the intended business processes and user needs.

---

# 2. UAT Scope

The UAT scenarios covered key workflows across the major platform personas:

* Student
* Influencer
* Super Agent
* Processing Staff
* Finance Staff
* Administrator

The scope included:

* User access
* Search and filtering
* Institution/programme discovery
* Programme selection
* Application initiation
* Application processing
* Application status
* Commission-related functionality
* Transaction history
* Withdrawal workflows
* Role-based access
* User assignment
* Validation and error handling

---

# 3. UAT Test Scenarios

## Search & Discovery

| Test ID | Persona | Scenario                            | Expected Result                           | Execution Status |
| ------- | ------- | ----------------------------------- | ----------------------------------------- | ---------------- |
| UAT-001 | Student | Search using country                | Relevant records are returned             | Anonymized       |
| UAT-002 | Student | Search using country and city       | Results reflect the selected location     | Anonymized       |
| UAT-003 | Student | Change country after selecting city | City options reflect the selected country | Anonymized       |
| UAT-004 | Student | Search using programme criteria     | Matching programmes are returned          | Anonymized       |
| UAT-005 | Student | Search using institution            | Relevant institution records are returned | Anonymized       |
| UAT-006 | Student | Search using multiple criteria      | Results reflect applicable criteria       | Anonymized       |
| UAT-007 | Student | Search with no matching records     | Clear no-results message is displayed     | Anonymized       |
| UAT-008 | Student | Review search results               | Relevant information is displayed clearly | Anonymized       |

---

# 4. Programme & Application

| Test ID | Persona          | Scenario                                 | Expected Result                            | Execution Status |
| ------- | ---------------- | ---------------------------------------- | ------------------------------------------ | ---------------- |
| UAT-009 | Student          | Select a programme                       | Programme information is displayed         | Anonymized       |
| UAT-010 | Student          | Start application for selected programme | Application process is initiated           | Anonymized       |
| UAT-011 | Processing Staff | Access assigned application              | Authorized application is accessible       | Anonymized       |
| UAT-012 | Processing Staff | Process application                      | Permitted processing actions are available | Anonymized       |
| UAT-013 | Processing Staff | Update application status                | Applicable status is reflected             | Anonymized       |
| UAT-014 | Processing Staff | Access unauthorized application          | Access is restricted appropriately         | Anonymized       |

---

# 5. Influencer

| Test ID | Persona    | Scenario                      | Expected Result                                | Execution Status |
| ------- | ---------- | ----------------------------- | ---------------------------------------------- | ---------------- |
| UAT-015 | Influencer | View referred applications    | Authorized referred applications are displayed | Anonymized       |
| UAT-016 | Influencer | View application information  | Permitted application information is displayed | Anonymized       |
| UAT-017 | Influencer | View potential commission     | Applicable potential commission is displayed   | Anonymized       |
| UAT-018 | Influencer | Access restricted application | Unauthorized information is not displayed      | Anonymized       |

---

# 6. Super Agent

| Test ID | Persona     | Scenario                           | Expected Result                              | Execution Status |
| ------- | ----------- | ---------------------------------- | -------------------------------------------- | ---------------- |
| UAT-019 | Super Agent | View commission information        | Relevant commission information is displayed | Anonymized       |
| UAT-020 | Super Agent | View transaction history           | Transaction records are displayed            | Anonymized       |
| UAT-021 | Super Agent | Filter transactions by student     | Results reflect selected student             | Anonymized       |
| UAT-022 | Super Agent | Filter transactions by application | Results reflect selected application         | Anonymized       |
| UAT-023 | Super Agent | Filter transactions by date range  | Results reflect selected date range          | Anonymized       |
| UAT-024 | Super Agent | Filter transactions by amount      | Results reflect selected amount criteria     | Anonymized       |

---

# 7. Finance

| Test ID | Persona       | Scenario                                 | Expected Result                                 | Execution Status |
| ------- | ------------- | ---------------------------------------- | ----------------------------------------------- | ---------------- |
| UAT-025 | Finance Staff | Access commission information            | Authorized information is displayed             | Anonymized       |
| UAT-026 | Finance Staff | Update applicable commission information | Updated information is reflected                | Anonymized       |
| UAT-027 | Finance Staff | Add/view commission notes                | Relevant notes are retained and displayed       | Anonymized       |
| UAT-028 | Finance Staff | Access withdrawal functionality          | Authorized withdrawal information is accessible | Anonymized       |
| UAT-029 | Finance Staff | Process withdrawal activity              | Applicable workflow can be processed            | Anonymized       |

---

# 8. Administration

| Test ID | Persona       | Scenario                            | Expected Result                                           | Execution Status |
| ------- | ------------- | ----------------------------------- | --------------------------------------------------------- | ---------------- |
| UAT-030 | Administrator | View user roles                     | User role information is displayed                        | Anonymized       |
| UAT-031 | Administrator | Manage user permissions             | Applicable permissions can be managed                     | Anonymized       |
| UAT-032 | Administrator | Assign processing staff             | Available processing staff can be assigned                | Anonymized       |
| UAT-033 | Administrator | Reassign workflow                   | Workflow can be reassigned to an appropriate staff member | Anonymized       |
| UAT-034 | Administrator | Handle unavailable processing staff | Defined fallback process is supported                     | Anonymized       |

---

# 9. Validation & Error Handling

| Test ID | Persona  | Scenario                           | Expected Result                               | Execution Status |
| ------- | -------- | ---------------------------------- | --------------------------------------------- | ---------------- |
| UAT-035 | Student  | Enter invalid search combination   | System handles invalid criteria appropriately | Anonymized       |
| UAT-036 | Student  | Search with no matching records    | No-results message is displayed               | Anonymized       |
| UAT-037 | Any User | Attempt unauthorized functionality | Access is appropriately restricted            | Anonymized       |
| UAT-038 | Any User | Submit invalid information         | Appropriate validation feedback is displayed  | Anonymized       |

---

# 10. UAT Acceptance Criteria

The solution is considered acceptable when:

* Critical business workflows function as expected.
* Users can complete their intended journeys.
* Search functionality produces appropriate results.
* Application workflows support defined business processes.
* Role-based access behaves appropriately.
* Validation and error handling provide meaningful feedback.
* Critical UAT defects have been resolved or formally accepted.
* Business stakeholders agree that the solution meets the agreed requirements.

---

# 11. Defect Classification

UAT issues can be classified according to their impact on business operations.

| Severity | Description                                               |
| -------- | --------------------------------------------------------- |
| Critical | Prevents a critical business process from being completed |
| High     | Significantly affects an important business workflow      |
| Medium   | Affects functionality but a workaround may exist          |
| Low      | Minor issue with limited business impact                  |

---

# 12. UAT Defect Management

Identified issues should be recorded and tracked through an agreed defect-management process.

A typical workflow is:

```text
Issue Identified
      ↓
Issue Logged
      ↓
Severity Assigned
      ↓
Development / QA Review
      ↓
Fix Implemented
      ↓
Retest
      ↓
Business Validation
      ↓
Closed / Accepted
```

---

# 13. UAT Results

Because this public case study has been anonymized, detailed production test evidence, tester identities, defect records, and confidential execution metrics are not disclosed.

The UAT artefact demonstrates the **testing framework and business validation approach** used to assess whether requirements were reflected correctly in the solution.

For a live project, the execution record would include:

| Metric                       | Result        |
| ---------------------------- | ------------- |
| Test scenarios planned       | 38            |
| Test scenarios executed      | Not disclosed |
| Passed                       | Not disclosed |
| Failed                       | Not disclosed |
| Blocked                      | Not disclosed |
| Defects raised               | Not disclosed |
| Critical defects outstanding | Not disclosed |
| UAT decision                 | Not disclosed |

---

# 14. UAT Sign-Off Framework

A typical sign-off would capture:

| Field              | Description                                    |
| ------------------ | ---------------------------------------------- |
| Project            | Foreign Classroom Student Portal               |
| UAT Owner          | Business/Product Representative                |
| Testing Period     | Project-specific                               |
| Business Area      | Student Application / Education Recruitment    |
| UAT Status         | Project-specific                               |
| Outstanding Issues | Project-specific                               |
| Business Decision  | Accepted / Accepted with Conditions / Rejected |
| Sign-Off           | Authorized Business Stakeholder                |

---

# 15. Business Analyst Contribution

The Business Analyst's role in UAT extends beyond writing test cases.

Key contributions include:

* Translating requirements into testable scenarios
* Ensuring acceptance criteria are measurable
* Validating business rules
* Supporting business users during UAT
* Clarifying expected system behaviour
* Reviewing identified defects
* Supporting defect prioritization
* Confirming that fixes address the original requirement
* Maintaining traceability between requirements and testing

---

# 16. Traceability to Requirements

The UAT scenarios connect directly to the requirements and user stories documented elsewhere in this repository.

Example:

```text
BR-002 Flexible Search
        ↓
FR-003 Multiple Search Criteria
        ↓
US-006 Combine Search Criteria
        ↓
Acceptance Criteria
        ↓
UAT-006 Multiple Criteria Search
```

Another example:

```text
BR-006 Application Initiation
        ↓
FR-008 Proceed to Application
        ↓
US-009 Start Application
        ↓
Acceptance Criteria
        ↓
UAT-010 Start Application
```

This demonstrates end-to-end requirements traceability from business need through validation.

---

# 17. Key Learning

Effective UAT is not simply about determining whether a button works.

The key question is:

> **Can the intended business user successfully complete the business process the solution was designed to support?**

This distinction helps the Business Analyst maintain focus on business outcomes rather than purely technical validation.

---

## Confidentiality Note

This document is an anonymized public portfolio reconstruction.

Specific proprietary information, confidential business data, personal information, production configurations, internal system details, tester identities, defect records, and commercially sensitive information have been intentionally excluded.
