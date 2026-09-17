# Foreign Classroom Student Portal

### Business Analysis | Product Requirements | Process Improvement | UAT

> A reconstructed Business Analysis case study demonstrating how I approached the analysis of a student-facing EdTech platform, from business problem discovery through requirements, process design, traceability and user acceptance testing.

---

## Executive Summary

Foreign Classroom is an education technology platform designed to support students seeking international study opportunities.

A key challenge was creating a structured experience that allowed users to discover relevant schools and programmes while also supporting the operational teams responsible for processing applications, managing partners and handling financial activities.

My role focused on translating business and user needs into structured requirements and delivery-ready artefacts.

The analysis covered:

- Business and functional requirements
- Stakeholder and persona analysis
- Student search and discovery
- Business rules
- User stories and acceptance criteria
- Process analysis
- Requirements traceability
- User acceptance testing
- Operational and product considerations

The case study demonstrates my approach to connecting **business objectives, user needs, product requirements and delivery validation**.

---

## My BA Contribution

I approached the initiative from both a **business-process** and **product** perspective.

My key areas of contribution included:

| Area | Contribution |
|---|---|
| Requirements Analysis | Translated business needs into structured requirements |
| Stakeholder Analysis | Identified user groups, responsibilities, goals and pain points |
| Process Analysis | Mapped the intended user and operational journey |
| Product Thinking | Considered usability, workflow dependencies and user experience |
| Requirements Engineering | Developed user stories, business rules and acceptance criteria |
| Traceability | Connected requirements to user stories and UAT scenarios |
| UAT | Defined scenarios for validating expected system behaviour |
| Documentation | Produced structured BA artefacts for delivery and stakeholder review |

---

## What I Was Solving

The core problem was not simply "how do we build a student portal?"

The broader question was:

> **How can we create a digital journey that makes it easier for students to discover suitable international education opportunities while giving internal teams and recruitment partners the visibility they need to support the application lifecycle?**

This distinction shaped the analysis.

The solution therefore had to consider both sides of the platform:

**Student experience**

Search → Discover → Review → Apply → Track

**Operational ecosystem**

Application → Processing → Partner visibility → Finance → Administration

---

## 📌 Project Overview

Foreign Classroom is an EdTech platform designed to streamline the process of connecting students with international educational institutions and supporting the application journey.

This case study documents the Business Analysis approach used to translate business needs and user expectations into structured product requirements and actionable development and testing artefacts.

The project involved analysing user journeys, defining functional requirements, improving search and application workflows, documenting business rules, and supporting User Acceptance Testing (UAT).

---

## 🎯 Business Problem

Students searching for international education opportunities may need to navigate multiple sources to discover institutions, programmes, locations, and available intakes.

From a product and business perspective, this creates opportunities to:

* Simplify education discovery
* Improve information accessibility
* Reduce friction in the application journey
* Provide different user groups with appropriate functionality
* Establish clearer and more structured workflows
* Improve coordination between students, processing teams, agents, influencers, and finance teams

The objective was therefore to support the development of a platform capable of bringing these activities into a more structured digital experience.

---

## 👤 My Role

**Business Analyst**

My responsibilities included:

* Requirements elicitation and analysis
* Stakeholder analysis
* Business process analysis
* Functional requirements documentation
* User story development
* Acceptance criteria definition
* Business rules documentation
* Search and filtering logic analysis
* Requirements traceability
* UAT planning and support
* Collaboration with product, design, development, and QA stakeholders
* Identification of process improvement opportunities

---

## 👥 Key Stakeholders

The platform supports multiple user groups with different needs.

| Stakeholder      | Primary Need                                                     |
| ---------------- | ---------------------------------------------------------------- |
| Students         | Search institutions and programmes and progress applications     |
| Influencers      | Manage referred students and monitor potential commissions       |
| Super Agents     | Manage applications and commission-related activities            |
| Processing Staff | Manage and process student applications                          |
| Finance Team     | Manage financial and commission-related activities               |
| Administrators   | Manage users, workflows, assignments, and platform configuration |

---

## 🔎 Key Business Analysis Challenge

One of the major areas analysed was the **institution and programme search experience**.

The search functionality needed to support different ways users naturally look for educational opportunities.

Users could search using combinations of:

* Country
* City
* School/Institution
* Programme level
* Programme type
* Department
* Faculty
* Intake year

The search design needed to remain flexible rather than forcing users to provide a fixed combination of fields.

---

## Challenges & Trade-offs

The analysis involved several areas where the requirements needed to balance user experience, operational needs and system behaviour.

### Search Flexibility vs. Search Simplicity

A highly flexible search experience gives users more ways to discover programmes, but too many filters can make the interface difficult to use.

The approach was therefore to support multiple search combinations while keeping each individual criterion straightforward.

### User Experience vs. Data Quality

Allowing users to enter unrestricted search values can create inconsistent results.

Where appropriate, controlled values and database-driven selections were preferred to improve consistency and reduce invalid combinations.

### Customer Experience vs. Operational Control

Students need a simple journey, while internal teams require more detailed information and controls.

The analysis therefore separated the customer-facing experience from the operational workflows supporting application processing, finance and administration.

### Automation vs. Exception Handling

The normal process can be automated, but exceptions still require human intervention.

For example, where an appropriate Processing Staff member is unavailable, an Administrator needs the ability to intervene and reassign the relevant workload.

### Documentation vs. Delivery Speed

Not every requirement needs the same level of documentation.

The analysis focused detailed documentation on requirements that affected user experience, business rules, operational workflows, data dependencies and UAT.

---

## Outcome & Measurement

Because this is a reconstructed portfolio case study, actual production performance metrics are not disclosed.

However, the analysis identified measurable indicators that could be used to evaluate the solution after implementation.

| Objective | Potential KPI |
|---|---|
| Improve programme discovery | Search-to-programme-detail conversion rate |
| Improve application conversion | Programme-detail-to-application conversion rate |
| Reduce search friction | Search abandonment rate |
| Improve operational efficiency | Average application processing time |
| Improve application visibility | Percentage of applications with current status |
| Improve data quality | Invalid search/input rate |
| Improve operational ownership | Percentage of applications assigned to an active processing owner |
| Improve partner visibility | Partner application-status engagement |
| Improve financial transparency | Time taken to reconcile commission/withdrawal records |

### Measurement Approach

The recommended approach would be to establish baseline measurements before implementation and compare them with post-release performance.

This creates a clearer connection between:

**Business Requirement → Product Change → User Behaviour → Operational Outcome → Business KPI**

---
## 🧩 Search Requirements

The analysis defined a flexible search model capable of supporting scenarios such as:

### Country-only search

A user selects a country and retrieves relevant institutions/programmes.

### Country + City

A user selects a country followed by a city, with the city options dependent on the selected country.

### Programme search

A user searches using programme-related criteria without necessarily selecting a location.

### Institution search

A user searches directly for a specific institution.

### Combined search

Users can combine multiple available criteria to narrow results.

### No criteria

The search experience was designed to avoid unnecessarily forcing users to complete mandatory search fields.

---

## 📋 Key Business Rules

Some of the analysed business rules included:

1. Search criteria should remain flexible rather than requiring every field.
2. City options should be dependent on the selected country where applicable.
3. Search inputs should use available database values where appropriate.
4. Multiple applicable criteria should be capable of working together.
5. Search results should be presented in a logical and consistent order.
6. Invalid or unavailable search combinations should return an appropriate response.
7. Where no matching records exist, the system should clearly communicate that no results were found.
8. Search functionality should support different user journeys rather than assuming one standard search behaviour.

---

## 📝 Example User Story

### Student searches for an international programme

**As a** student,

**I want to** search for institutions and programmes using different criteria,

**So that** I can discover suitable international education opportunities without having to provide unnecessary information.

### Acceptance Criteria

**Given** I am on the search page,

**When** I enter one or more valid search criteria,

**Then** the system should return matching results.

**Given** I select a country,

**When** I open the city field,

**Then** the system should display cities associated with the selected country.

**Given** my search criteria do not match any available records,

**When** I submit the search,

**Then** the system should display an appropriate "No results found" message.

---

## 🔄 Requirements Traceability

The requirements process followed a traceable path:

```text
Business Need
     ↓
Stakeholder Need
     ↓
Business Requirement
     ↓
Functional Requirement
     ↓
User Story
     ↓
Acceptance Criteria
     ↓
Test Scenario
     ↓
UAT
```

This approach helped maintain alignment between what the business wanted, what users needed, what the product was expected to do, and what QA/UAT activities needed to validate.

---

## 🧪 User Acceptance Testing

UAT activities were considered across the major platform personas.

Testing focused on areas such as:

* User registration
* Authentication
* Profile management
* Application management
* Search functionality
* Application workflows
* Commission-related functionality
* Financial workflows
* Role-based access
* Data validation
* Error handling
* Workflow assignment

The UAT approach was designed to validate the product from the perspective of actual business users rather than testing functionality in isolation.

---

## 🏗️ Business Analysis Artefacts

The project involved the creation and analysis of several BA artefacts, including:

* Business Requirements Documentation
* System/User Requirements Documentation
* Process Flows
* User Stories
* Acceptance Criteria
* Business Rules
* Search Matrix
* Test Scenarios
* UAT Documentation
* Requirements Traceability Matrix
* Stakeholder Analysis
* User Personas
* Process Improvement Recommendations

---

## 💡 Product Thinking

Beyond documenting requirements, the analysis considered the broader product experience.

Key considerations included:

### User Experience

How easily can a student discover a suitable institution or programme?

### Business Value

How can the platform reduce friction in the international education application process?

### Operational Efficiency

How can processing teams manage applications more effectively?

### Scalability

Can the workflows support different user types and future platform expansion?

### Data Quality

How can structured data and controlled inputs improve search accuracy?

### Testability

Can requirements be translated into clear, measurable acceptance criteria?

---

## 📈 Expected Business Value

The proposed improvements were intended to contribute to:

* A more structured student discovery experience
* Reduced search friction
* Better requirements clarity
* Improved communication between business and technical teams
* More consistent product behaviour
* Improved UAT readiness
* Better traceability from requirements to testing
* More scalable platform workflows

> **Note:** Specific commercial or operational performance figures are not disclosed because this public case study has been anonymized.

---

## 🧠 Key Lessons

### 1. Requirements need context

A requirement is more useful when its underlying business objective and user need are understood.

### 2. Flexibility matters in product design

Users do not always follow one predictable path. Search and discovery experiences should accommodate different ways of achieving the same objective.

### 3. Good acceptance criteria reduce ambiguity

Clear acceptance criteria create a common understanding between business, product, development, and QA teams.

### 4. Traceability improves delivery confidence

Connecting requirements to user stories, acceptance criteria, and test scenarios makes it easier to determine whether business needs have actually been addressed.

### 5. A Business Analyst should think beyond documentation

Effective BA work involves understanding the problem, challenging assumptions, identifying opportunities, and helping teams deliver useful outcomes.

---

## What I Would Improve Next

If the product were being taken into a subsequent delivery phase, I would explore:

### 1. Search Analytics

Introduce analytics around:

- Most frequently searched countries
- Most searched programmes
- Searches returning zero results
- Search-to-application conversion
- Frequently abandoned searches

This could help product and business teams identify gaps in the available catalogue.

### 2. Search Personalisation

Explore whether search behaviour and student preferences could eventually support personalised programme recommendations.

Any recommendation capability would require appropriate data, transparency and validation before being used in production.

### 3. Application Funnel Analytics

Track the journey:

**Search → Programme View → Apply → Application Completion**

This would help identify where users drop out of the journey.

### 4. Operational Dashboarding

Provide Processing Staff and management with operational metrics such as:

- Open applications
- Pending applications
- Applications by status
- Processing turnaround time
- Workload by staff member
- Exceptions requiring intervention

### 5. Continuous Requirements Improvement

Use production feedback, analytics, stakeholder feedback and UAT findings to continuously refine requirements rather than treating the initial requirements baseline as static.

---

## 🛠️ Skills Demonstrated

**Business Analysis**

* Requirements Engineering
* Requirements Elicitation
* Requirements Management
* Business Process Analysis
* Stakeholder Management
* Business Rules
* Functional Requirements
* Non-Functional Requirements
* Requirements Traceability

**Product**

* User-Centred Analysis
* Product Discovery
* User Journeys
* Feature Definition
* Workflow Analysis
* Product Requirements

**Agile**

* User Stories
* Acceptance Criteria
* Backlog Refinement
* Sprint Collaboration
* UAT

**Data & Technology**

* Data-driven requirements
* Search/filter logic
* Database-oriented thinking
* Power BI
* SQL
* Excel

---

## Portfolio Artefacts

The following artefacts demonstrate the analysis and delivery approach used throughout the case study.

| Artefact | Description |
|---|---|
| [Business Requirements](./docs/business-requirements.md) | Business objectives, requirements, scope and business rules |
| [User Stories](./docs/user-stories.md) | User stories and acceptance criteria across platform personas |
| [Stakeholder & Persona Analysis](./docs/stakeholder-and-persona-analysis.md) | Stakeholder responsibilities, goals, pain points and requirements |
| [Process Flow](./diagrams/process-flow.md) | High-level representation of the proposed user and operational flow |
| [Search Matrix](./artifacts/search-matrix.md) | Search combinations, rules and functional requirements |
| [Requirements Traceability Matrix](./artifacts/requirements-traceability-matrix.md) | Traceability from business requirements through UAT |
| [UAT Test Scenarios](./artifacts/uat-test-scenarios.md) | UAT scenarios, acceptance criteria and defect-management approach |
---
## Case Study Navigation

**Start here:**  
[Project Overview](./README.md)

**Understand the requirements:**  
[Business Requirements](./docs/business-requirements.md) → [User Stories](./docs/user-stories.md)

**Understand the users:**  
[Stakeholder & Persona Analysis](./docs/stakeholder-and-persona-analysis.md)

**Understand the process:**  
[Process Flow](./diagrams/process-flow.md)

**Explore the detailed analysis:**  
[Search Matrix](./artifacts/search-matrix.md) → [Requirements Traceability Matrix](./artifacts/requirements-traceability-matrix.md)

**Validate the solution:**  
[UAT Test Scenarios](./artifacts/uat-test-scenarios.md)

## 🔐 Confidentiality & Disclaimer

This case study is a **public portfolio reconstruction** based on professional Business Analysis experience.

Confidential company information, proprietary data, credentials, personally identifiable information, internal URLs, commercial information, and sensitive implementation details have been excluded or generalized.

The purpose of this case study is to demonstrate Business Analysis methodology, problem-solving ability, requirements thinking, and product delivery skills.

---

## 👋 About Me

I am a Business Analyst focused on combining **business analysis, product thinking, data, and technology** to solve business problems and improve digital products.

My interests include:

* Business Analysis
* Product Management
* Data Analytics
* AI-enabled Business Transformation
* Digital Products
* Process Improvement
* Requirements Engineering

---

### ⭐ What this project demonstrates

> **I don't just document requirements. I connect business problems to user needs, product requirements, delivery, and measurable outcomes.**
