# Foreign Classroom Student Portal

## User Stories & Acceptance Criteria

**Document Type:** User Stories & Acceptance Criteria
**Project:** Foreign Classroom Student Portal
**Role:** Business Analyst
**Status:** Portfolio Reconstruction
**Confidentiality:** Anonymized

---

## 1. Overview

This document translates identified business and functional requirements into user stories and acceptance criteria.

The stories are structured around the needs of the major platform personas and follow the format:

> **As a [user], I want [capability], so that [business value].**

Acceptance criteria are written to provide a clear and testable definition of expected system behaviour.

---

# 2. Student User Stories

## US-001 — Search for Education Opportunities

**As a** student,

**I want to** search for institutions and programmes using relevant criteria,

**so that** I can discover education opportunities that match my interests.

### Acceptance Criteria

* **Given** I am on the search page, **when** I enter valid search criteria, **then** the system should return matching results.
* **Given** I provide one valid search criterion, **when** I submit the search, **then** the system should process the search.
* **Given** I provide multiple valid criteria, **when** I submit the search, **then** the system should return results matching the applicable criteria.
* **Given** no matching records exist, **when** I submit the search, **then** the system should display a clear no-results message.

---

## US-002 — Search by Country

**As a** student,

**I want to** search by country,

**so that** I can discover education opportunities within a preferred country.

### Acceptance Criteria

* **Given** the country field is available, **when** I select a country, **then** the system should accept the selection.
* **When** I submit the search, **then** relevant records associated with the selected country should be returned.
* **If** no records exist for the selected country, **then** an appropriate no-results message should be displayed.

---

## US-003 — Filter City by Country

**As a** student,

**I want to** select a city based on my chosen country,

**so that** I can narrow my search to a specific location.

### Acceptance Criteria

* **Given** I have selected a country, **when** I open the city field, **then** the system should display applicable cities.
* **Given** I change the selected country, **when** I access the city field, **then** the available city options should reflect the new country.
* The system should prevent or appropriately handle invalid country-city combinations.

---

## US-004 — Search by Programme

**As a** student,

**I want to** search using programme-related criteria,

**so that** I can find programmes relevant to my academic interests.

### Acceptance Criteria

* The system should allow applicable programme criteria to be selected.
* The user should be able to search using programme-related information without necessarily specifying a location.
* Matching programmes should be returned based on the selected criteria.
* Where no matching programme exists, the system should display an appropriate message.

---

## US-005 — Search by Institution

**As a** student,

**I want to** search for a specific institution,

**so that** I can find programmes offered by that institution.

### Acceptance Criteria

* The system should allow the user to enter or select an institution.
* The search should return relevant records associated with the selected institution.
* No matching institution/programme should produce an appropriate no-results response.

---

## US-006 — Combine Search Criteria

**As a** student,

**I want to** combine multiple search criteria,

**so that** I can narrow my results to more relevant opportunities.

### Acceptance Criteria

* The system should allow multiple applicable criteria to be selected.
* The system should process the selected criteria together.
* Results should reflect the applicable combination of criteria.
* The user should not be forced to complete unrelated search fields.

---

## US-007 — Review Search Results

**As a** student,

**I want to** review search results,

**so that** I can identify suitable institutions and programmes.

### Acceptance Criteria

* Search results should be presented clearly.
* Relevant institution and programme information should be displayed.
* Results should be consistently structured.
* The user should be able to identify suitable options from the results.

---

## US-008 — Select a Programme

**As a** student,

**I want to** select a programme from the search results,

**so that** I can review the opportunity and proceed with an application.

### Acceptance Criteria

* The user should be able to select a relevant programme.
* The system should display the applicable programme information.
* The user should have a clear path toward starting an application.

---

## US-009 — Start an Application

**As a** student,

**I want to** start an application for a selected programme,

**so that** I can begin the application process.

### Acceptance Criteria

* **Given** I have selected an eligible programme, **when** I choose to apply, **then** the application process should begin.
* The system should associate the application with the appropriate programme.
* The application should become available to the relevant processing workflow.

---

# 3. Processing Staff User Stories

## US-010 — Access Assigned Applications

**As a** processing staff member,

**I want to** access applications assigned to me,

**so that** I can process student applications.

### Acceptance Criteria

* The processing staff member should only access applications permitted by their role.
* Assigned applications should be identifiable.
* Relevant application information should be available for processing.

---

## US-011 — Process Student Application

**As a** processing staff member,

**I want to** process student applications,

**so that** applications can move through the appropriate workflow.

### Acceptance Criteria

* Authorized staff should be able to access relevant applications.
* Staff should be able to perform permitted processing activities.
* Application status should reflect applicable workflow changes.
* Unauthorized users should not be able to perform restricted processing activities.

---

## US-012 — View Application Status

**As a** processing staff member,

**I want to** view application status,

**so that** I can understand the current position of an application.

### Acceptance Criteria

* The current application status should be visible to authorized users.
* Status information should be associated with the correct application.
* Status changes should be reflected appropriately.

---

# 4. Influencer User Stories

## US-013 — View Referred Applications

**As an** influencer,

**I want to** view applications associated with my referrals,

**so that** I can monitor relevant student application activity.

### Acceptance Criteria

* The influencer should only see applications they are authorized to access.
* Relevant application information should be displayed.
* The information should be presented in a consistent format.

---

## US-014 — View Potential Commission

**As an** influencer,

**I want to** view potential commission information,

**so that** I can understand the potential commission associated with eligible applications.

### Acceptance Criteria

* Applicable potential commission information should be displayed.
* Commission information should be associated with the appropriate application.
* The system should provide explanatory information where applicable.

---

# 5. Super Agent User Stories

## US-015 — View Commission Information

**As a** super agent,

**I want to** view commission-related information,

**so that** I can monitor applicable commission activities.

### Acceptance Criteria

* Authorized commission information should be accessible.
* Information should be associated with the appropriate student/application.
* Relevant status information should be displayed.

---

## US-016 — View Transaction History

**As a** super agent,

**I want to** view transaction history,

**so that** I can review previous commission-related transactions.

### Acceptance Criteria

The transaction history should support applicable filtering by:

* Student
* Application
* Date range
* Amount

The results should reflect the selected filters.

---

# 6. Finance User Stories

## US-017 — Manage Commission Activities

**As a** finance team member,

**I want to** manage applicable commission information,

**so that** financial activities can be properly monitored.

### Acceptance Criteria

* Authorized finance users should be able to access commission-related information.
* Relevant records should be identifiable.
* Commission information should reflect applicable updates.
* Relevant notes should be available where required.

---

## US-018 — Manage Withdrawal Activities

**As a** finance team member,

**I want to** manage withdrawal activities,

**so that** commission withdrawal requests can be processed appropriately.

### Acceptance Criteria

* Authorized finance users should be able to access withdrawal information.
* Withdrawal records should contain the relevant information required for processing.
* Processing status should be identifiable.
* Unauthorized users should not access restricted financial functionality.

---

# 7. Administrator User Stories

## US-019 — Manage User Roles

**As an** administrator,

**I want to** manage user roles and permissions,

**so that** users have access to functionality appropriate to their responsibilities.

### Acceptance Criteria

* Administrators should be able to manage applicable user roles.
* Access should be determined by assigned permissions.
* Users should not have access to restricted functionality.

---

## US-020 — Assign Processing Staff

**As an** administrator,

**I want to** assign applications or student workflows to available processing staff,

**so that** applications can be handled by the appropriate operational team member.

### Acceptance Criteria

* The administrator should be able to assign an available processing staff member.
* The assigned staff member should be associated with the relevant workflow.
* Where an appropriate staff member is unavailable, the system should support the defined fallback process.
* The assignment should be visible to authorized users.

---

# 8. Cross-Functional Requirements

The following requirements apply across multiple user journeys:

### Role-Based Access

Users should only access information and functionality appropriate to their assigned role.

### Data Validation

The system should validate applicable inputs and provide meaningful feedback when information is invalid.

### Error Handling

The system should provide clear feedback when an operation cannot be completed.

### Data Consistency

Information displayed across related workflows should remain consistent.

### Traceability

Requirements should be traceable through user stories, acceptance criteria, test scenarios, and UAT.

---

# 9. Definition of Done

A user story can be considered ready for acceptance when:

* The requirement is clearly understood.
* Acceptance criteria have been defined.
* Required business rules have been identified.
* The functionality has been implemented.
* Applicable test scenarios have passed.
* UAT has been completed where required.
* Relevant defects have been resolved or formally accepted.

---

# 10. Business Analysis Value

The purpose of these stories is not simply to describe system features.

They create a shared understanding between:

**Business → Product → Design → Development → QA → Users**

Clear user stories and acceptance criteria reduce ambiguity, improve testability, and provide a practical bridge between business requirements and product delivery.

---

## Confidentiality Note

This document is an anonymized public portfolio reconstruction.

Specific proprietary information, confidential business data, personal information, production configurations, internal system details, and commercially sensitive information have been intentionally excluded.
