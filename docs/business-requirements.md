# Foreign Classroom Student Portal

## Business Requirements Document

**Document Type:** Business Requirements
**Project:** Foreign Classroom Student Portal
**Role:** Business Analyst
**Status:** Portfolio Reconstruction
**Confidentiality:** Anonymized

---

## 1. Purpose

The purpose of this document is to define the business requirements for an EdTech platform designed to support students in discovering international educational opportunities and progressing through the application process.

The requirements focus on creating a structured digital experience for students while supporting the operational teams responsible for application processing and related activities.

---

## 2. Business Objective

The primary business objective is to provide a centralized platform through which students can:

* Discover international institutions and programmes
* Search using relevant educational criteria
* Review available opportunities
* Select suitable programmes
* Initiate applications
* Track application progress

The platform should also provide appropriate workflows for internal and external stakeholders supporting the student application journey.

---

## 3. Business Problem

The international education application journey involves multiple stakeholders, information sources, and operational activities.

Without a structured digital platform, users may experience:

* Difficulty discovering suitable programmes
* Inconsistent search experiences
* Unclear application processes
* Manual coordination between stakeholders
* Limited visibility of application status
* Increased operational effort

The proposed solution aims to reduce these challenges through a centralized and role-based digital platform.

---

## 4. Scope

### 4.1 In Scope

The portfolio case study covers:

* Student registration and access
* Institution and programme discovery
* Search and filtering
* Programme selection
* Application initiation
* Application processing
* Application status management
* User profile management
* Role-based workflows
* Commission-related workflows
* Finance-related workflows
* UAT support

### 4.2 Out of Scope

The following are excluded from this public reconstruction:

* Proprietary system architecture
* Production database structures
* Commercial agreements
* Actual student records
* Financial transaction data
* Internal credentials
* Private company processes
* Production URLs
* Confidential performance metrics

---

## 5. Stakeholder Requirements

| Stakeholder      | Requirement                                                                 |
| ---------------- | --------------------------------------------------------------------------- |
| Student          | Ability to search and identify suitable institutions and programmes         |
| Student          | Ability to initiate and manage applications                                 |
| Influencer       | Ability to monitor referred students and commission-related information     |
| Super Agent      | Ability to manage relevant applications and commission activities           |
| Processing Staff | Ability to process and manage assigned applications                         |
| Finance Team     | Ability to manage applicable financial and commission activities            |
| Administrator    | Ability to manage users, workflows, assignments, and platform configuration |

---

## 6. High-Level Business Requirements

### BR-001 — Centralized Education Discovery

The system shall provide a centralized platform for users to discover international institutions and educational programmes.

### BR-002 — Flexible Search

The system shall allow users to search for educational opportunities using one or more available criteria.

### BR-003 — Structured Search Data

The system shall use structured educational data to support consistent search and filtering.

### BR-004 — Location-Based Search

The system shall support location-based discovery, including country and city.

### BR-005 — Programme Discovery

The system shall allow users to search based on programme-related attributes.

### BR-006 — Application Initiation

The system shall allow eligible users to initiate an application after identifying a suitable programme.

### BR-007 — Application Processing

The system shall provide workflows that enable authorized staff to process applications.

### BR-008 — Application Visibility

The system shall provide appropriate users with visibility of relevant application information and status.

### BR-009 — Role-Based Access

The system shall provide functionality according to the user's assigned role and permissions.

### BR-010 — Data Validation

The system shall validate relevant user inputs and provide appropriate feedback when information is invalid or unavailable.

---

# 7. Search Requirements

Search functionality represents a major component of the student discovery experience.

## 7.1 Search Criteria

The system should support the following criteria:

* Country
* City
* Institution/School
* Programme Level
* Programme Type
* Department
* Faculty
* Intake Year

## 7.2 Search Behaviour

Users should be able to:

* Search using a single criterion
* Combine multiple criteria
* Search by institution
* Search by programme
* Search by location
* Search using combinations of location and programme criteria

No single search criterion should unnecessarily prevent a user from conducting a search.

---

## 7.3 Cascading Location Selection

Where country and city are used together:

**Country → City**

The available city options should be associated with the selected country.

This reduces invalid combinations and improves search accuracy.

---

## 7.4 Search Results

When matching records exist, the system should return relevant results based on the selected criteria.

Search results should:

* Be clearly presented
* Use consistent data fields
* Be logically ordered
* Allow users to identify relevant institutions/programmes
* Support progression toward programme selection

---

## 7.5 No Results

When no records match the selected criteria, the system should provide a clear **No Results Found** message.

The message should help the user understand that the search did not return a matching record rather than suggesting that the system has failed.

---

# 8. Functional Requirements

| ID     | Functional Requirement                                                           |
| ------ | -------------------------------------------------------------------------------- |
| FR-001 | Users shall be able to access the search functionality.                          |
| FR-002 | Users shall be able to enter or select available search criteria.                |
| FR-003 | Users shall be able to search using one or more criteria.                        |
| FR-004 | City options shall be filtered based on the selected country where applicable.   |
| FR-005 | The system shall return records matching the selected criteria.                  |
| FR-006 | The system shall display an appropriate message when no records are found.       |
| FR-007 | Users shall be able to review relevant institution/programme information.        |
| FR-008 | Eligible users shall be able to proceed from programme selection to application. |
| FR-009 | Authorized staff shall be able to access relevant applications.                  |
| FR-010 | The system shall apply role-based access to relevant functionality.              |
| FR-011 | The system shall validate applicable inputs.                                     |
| FR-012 | The system shall maintain application status information.                        |

---

# 9. Non-Functional Considerations

The following quality attributes were considered during requirements analysis.

### Usability

The search and application experience should be intuitive enough for users with different levels of technical experience.

### Performance

Search operations should return results within an acceptable response time.

### Reliability

The platform should consistently process valid requests and provide appropriate feedback for invalid operations.

### Security

Users should only access functionality and information appropriate to their assigned roles.

### Scalability

The platform should support the addition of institutions, programmes, users, and future workflows.

### Maintainability

Requirements and business rules should be structured clearly enough to support future changes.

---

# 10. Business Rules

| ID      | Business Rule                                                                |
| ------- | ---------------------------------------------------------------------------- |
| BRL-001 | Search criteria may be used individually or in combination.                  |
| BRL-002 | City selection should be dependent on the selected country where applicable. |
| BRL-003 | Search inputs should use controlled values where appropriate.                |
| BRL-004 | The system should not require unnecessary search criteria.                   |
| BRL-005 | Invalid search combinations should be handled appropriately.                 |
| BRL-006 | No matching records should generate a clear no-results response.             |
| BRL-007 | Access to functionality should be determined by user role and permissions.   |
| BRL-008 | Application workflows should reflect the user's authorized responsibilities. |

---

# 11. Assumptions

The requirements analysis was based on the following assumptions:

1. Institution and programme information is maintained in a structured data source.
2. Users have access to the relevant platform functionality according to their roles.
3. Application processing follows defined operational workflows.
4. Search data is sufficiently structured to support filtering.
5. Appropriate access controls are implemented by the solution.

---

# 12. Dependencies

Key dependencies include:

* Availability of accurate institution data
* Availability of programme information
* User-role configuration
* Application workflow configuration
* Data quality
* Integration with relevant platform components

---

# 13. Business Analysis Approach

The requirements were developed by considering:

**Stakeholders → Business Needs → User Needs → Processes → Requirements → User Stories → Acceptance Criteria → Testing**

This approach ensured that requirements were connected to the underlying business problem rather than being documented as isolated system features.

---

# 14. Success Criteria

The solution should enable:

* Users to discover relevant education opportunities more efficiently
* Users to conduct flexible searches
* Users to progress from discovery toward application
* Staff to manage application workflows more effectively
* Stakeholders to access information appropriate to their roles
* Requirements to be clearly translated into testable functionality

---

## 15. Requirements Traceability

The requirements in this document will form the basis for subsequent portfolio artefacts, including:

* User Stories
* Acceptance Criteria
* Test Scenarios
* Requirements Traceability Matrix
* UAT Documentation

This establishes a traceable connection between the original business need and the final validation of the solution.

---

## 16. Confidentiality Note

This document is an anonymized public portfolio reconstruction.

Specific proprietary information, confidential business data, personal information, production configurations, internal system details, and commercially sensitive information have been intentionally excluded.
