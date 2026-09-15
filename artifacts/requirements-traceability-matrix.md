# Foreign Classroom Student Portal
## Requirements Traceability Matrix

**Document Type:** Requirements Traceability Matrix  
**Project:** Foreign Classroom Student Portal  
**Role:** Business Analyst  
**Status:** Portfolio Reconstruction  
**Confidentiality:** Anonymized

---

## 1. Purpose

The Requirements Traceability Matrix (RTM) establishes a clear relationship between business requirements, functional requirements, user stories, acceptance criteria, and validation activities.

The purpose is to ensure that every significant requirement can be traced from the original business need through implementation and testing.

---

## 2. Traceability Model

The project follows the following traceability chain:

**Business Requirement → Functional Requirement → User Story → Acceptance Criteria → Test Scenario → UAT**

This provides visibility across the product delivery lifecycle and helps identify gaps, duplication, or requirements that have not been adequately validated.

---

## 3. Requirements Traceability Matrix

| Business Requirement | Functional Requirement | User Story | Acceptance Criteria | Validation |
|---|---|---|---|---|
| BR-001 Centralized Education Discovery | FR-001 Access search functionality | US-001 Search for Education Opportunities | User can access and perform a search | UAT |
| BR-002 Flexible Search | FR-002, FR-003 Search using one or more criteria | US-001, US-006 | Single and multiple criteria can be used | UAT |
| BR-003 Structured Search Data | FR-002 Search criteria use available values | US-001, US-004 | Applicable search values can be selected | UAT |
| BR-004 Location-Based Search | FR-004 Country/city filtering | US-002, US-003 | City options reflect selected country | UAT |
| BR-005 Programme Discovery | FR-005 Return matching programmes | US-004 | Matching programmes are returned | UAT |
| BR-005 Programme Discovery | FR-007 Display programme information | US-007, US-008 | User can review programme information | UAT |
| BR-006 Application Initiation | FR-008 Proceed to application | US-009 | Eligible user can start an application | UAT |
| BR-007 Application Processing | FR-009 Access relevant applications | US-010, US-011 | Authorized staff can process applications | UAT |
| BR-008 Application Visibility | FR-012 Maintain application status | US-012 | Current application status is visible | UAT |
| BR-009 Role-Based Access | FR-010 Apply role-based access | US-010, US-013, US-019 | Users only access permitted functionality | UAT |
| BR-010 Data Validation | FR-011 Validate applicable inputs | US-001, US-006 | Invalid input is appropriately handled | UAT |
| BR-010 Data Validation | FR-006 No-results handling | US-001, US-004, US-005 | No matching records produce appropriate feedback | UAT |

---

# 4. Detailed Traceability

## Search & Discovery

| ID | Requirement | User Story | Test Focus |
|---|---|---|---|
| TR-001 | Users can search institutions | US-001 | Search returns relevant records |
| TR-002 | Users can search by country | US-002 | Country-based results |
| TR-003 | City depends on country | US-003 | Cascading location behaviour |
| TR-004 | Users can search by programme | US-004 | Programme search |
| TR-005 | Users can search by institution | US-005 | Institution search |
| TR-006 | Multiple criteria can be combined | US-006 | Combined filtering |
| TR-007 | Users can review results | US-007 | Results presentation |
| TR-008 | Users can select a programme | US-008 | Programme selection |

---

## Application Management

| ID | Requirement | User Story | Test Focus |
|---|---|---|---|
| TR-009 | Students can start applications | US-009 | Application initiation |
| TR-010 | Processing staff can access assigned applications | US-010 | Role-based application access |
| TR-011 | Processing staff can process applications | US-011 | Application workflow |
| TR-012 | Application status is visible | US-012 | Status visibility |

---

## Influencer & Agent Management

| ID | Requirement | User Story | Test Focus |
|---|---|---|---|
| TR-013 | Influencers can view referred applications | US-013 | Referral visibility |
| TR-014 | Influencers can view potential commission | US-014 | Commission information |
| TR-015 | Super Agents can view commission information | US-015 | Commission visibility |
| TR-016 | Super Agents can view transaction history | US-016 | Transaction filtering |

---

## Finance

| ID | Requirement | User Story | Test Focus |
|---|---|---|---|
| TR-017 | Finance can manage commission activities | US-017 | Commission management |
| TR-018 | Finance can manage withdrawal activities | US-018 | Withdrawal workflow |

---

## Administration

| ID | Requirement | User Story | Test Focus |
|---|---|---|---|
| TR-019 | Administrators can manage roles | US-019 | Role and permission management |
| TR-020 | Administrators can assign processing staff | US-020 | Staff assignment workflow |

---

# 5. Traceability Coverage

The RTM provides coverage across the major functional areas of the platform:

| Functional Area | Requirements Covered | User Stories | Validation |
|---|---:|---:|---|
| Search & Discovery | 8 | US-001 to US-008 | UAT |
| Application Management | 4 | US-009 to US-012 | UAT |
| Influencer Management | 2 | US-013 to US-014 | UAT |
| Super Agent Management | 2 | US-015 to US-016 | UAT |
| Finance | 2 | US-017 to US-018 | UAT |
| Administration | 2 | US-019 to US-020 | UAT |

---

# 6. Traceability Benefits

The RTM provides several benefits:

### Requirement Coverage

Helps confirm that identified requirements have corresponding functionality and validation activities.

### Gap Identification

Makes it easier to identify requirements that do not have user stories, acceptance criteria, or test coverage.

### Change Impact Analysis

When a requirement changes, its related user stories and test scenarios can be identified more easily.

### UAT Readiness

Provides a structured basis for determining what needs to be validated by business users.

### Stakeholder Visibility

Provides stakeholders with a simplified view of how business needs translate into delivered functionality.

---

# 7. Change Management

Requirements should be reviewed whenever there is a significant change to:

- Business objectives
- User needs
- Product functionality
- Business rules
- Workflow
- Acceptance criteria
- Regulatory or operational requirements

Changes should be assessed for their potential impact on related requirements, user stories, development activities, and testing.

---

# 8. Business Analyst Perspective

Traceability is more than maintaining a spreadsheet.

A strong Business Analyst uses traceability to maintain alignment between:

**Why we are building it → What we are building → How it should behave → How we verify it**

This helps reduce requirements gaps and ensures that delivery remains connected to the original business objective.

---

## Confidentiality Note

This document is an anonymized public portfolio reconstruction.

Specific proprietary information, confidential business data, personal information, production configurations, internal system details, and commercially sensitive information have been intentionally excluded.
