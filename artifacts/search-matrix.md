# Foreign Classroom Student Portal

## Search Matrix & Business Rules

**Document Type:** Search Requirements & Business Rules
**Project:** Foreign Classroom Student Portal
**Role:** Business Analyst
**Status:** Portfolio Reconstruction
**Confidentiality:** Anonymized

---

## 1. Purpose

The search functionality is a core component of the student discovery experience.

The purpose of this document is to define how users can search for institutions and programmes using different combinations of educational and geographical criteria.

The analysis focuses on:

* Search criteria
* Search combinations
* Field relationships
* Cascading behaviour
* Input validation
* Result handling
* Sorting
* No-result scenarios
* Business rules

---

# 2. Search Criteria

The proposed search experience uses the following criteria:

| Field           | Description                              | Example            |
| --------------- | ---------------------------------------- | ------------------ |
| Country         | Country where the institution is located | United Kingdom     |
| City            | City where the institution is located    | London             |
| School Name     | Name of institution                      | University Example |
| Programme Level | Academic level                           | Master's           |
| Programme Type  | Type/category of programme               | Full-time          |
| Department      | Academic department                      | Computer Science   |
| Faculty         | Academic faculty                         | Faculty of Science |
| Intake Year     | Available intake year                    | 2027               |

---

# 3. Search Philosophy

The search experience should be **flexible rather than restrictive**.

Users should not be forced to provide every available search field before obtaining results.

The system should allow users to search according to the information they already know.

For example, a user may know:

* Only the country
* Country and city
* Only the school
* Only the programme
* Programme and intake year
* Country + programme
* Country + city + programme
* Multiple applicable criteria

---

# 4. Search Matrix

| Search Scenario            | Country | City | School | Programme | Intake | Expected Behaviour                              |
| -------------------------- | ------: | ---: | -----: | --------: | -----: | ----------------------------------------------- |
| Country only               |       ✓ |    — |      — |         — |      — | Return relevant records for selected country    |
| Country + City             |       ✓ |    ✓ |      — |         — |      — | Return records matching location                |
| School only                |       — |    — |      ✓ |         — |      — | Return records for selected institution         |
| Programme only             |       — |    — |      — |         ✓ |      — | Return matching programmes                      |
| Intake only                |       — |    — |      — |         — |      ✓ | Return records matching intake                  |
| Country + Programme        |       ✓ |    — |      — |         ✓ |      — | Return matching country/programme records       |
| Country + Intake           |       ✓ |    — |      — |         — |      ✓ | Return matching country/intake records          |
| Programme + Intake         |       — |    — |      — |         ✓ |      ✓ | Return matching programme/intake records        |
| Country + City + Programme |       ✓ |    ✓ |      — |         ✓ |      — | Return records matching all applicable criteria |
| Country + School           |       ✓ |    — |      ✓ |         — |      — | Return selected school within country           |
| School + Programme         |       — |    — |      ✓ |         ✓ |      — | Return relevant programmes at selected school   |
| Multiple criteria          |       ✓ |    ✓ |      ✓ |         ✓ |      ✓ | Apply all applicable criteria                   |

---

# 5. Country → City Cascading Rule

One of the key relationships identified is the dependency between **Country** and **City**.

The relationship is:

```text
Country
   ↓
Available Cities
   ↓
Search Results
```

### Business Rule

A city should be associated with the selected country.

### Example

If the user selects:

**Country:** United Kingdom

The city field should present cities associated with the United Kingdom dataset.

If the user changes the country, the available city options should update accordingly.

---

# 6. Search Input Behaviour

Search inputs should support controlled and consistent values where appropriate.

Where database values are available, the interface should use appropriate selection controls rather than relying entirely on free-text input.

This helps reduce:

* Spelling variations
* Duplicate values
* Invalid combinations
* Inconsistent search terms
* Poor-quality search results

---

# 7. Multi-Selection

Where business requirements allow multiple values, the search experience should support multi-selection.

For example:

```text
Country:
[United Kingdom] [Canada] [Australia]
```

or:

```text
Programme Level:
[Undergraduate] [Postgraduate]
```

The exact multi-selection behaviour should follow the applicable business rule for each field.

---

# 8. Search Result Sorting

Search results should be presented consistently.

Where alphabetical ordering is applicable, records should be sorted alphabetically to make them easier for users to scan.

For example:

```text
A
  Aston University

B
  Birmingham City University

C
  Coventry University
```

The applicable sorting rule should be defined at field/result level rather than assumed for every search scenario.

---

# 9. No Results Scenario

When a user's search criteria do not match any available record, the system should provide a clear response.

### Expected Behaviour

```text
Search
  ↓
No matching records
  ↓
"No results found"
  ↓
User can modify criteria
```

The system should avoid displaying a blank result area without explanation.

---

# 10. Invalid Search Scenario

Where a combination of search inputs is invalid or unsupported, the system should provide appropriate feedback.

Examples include:

* Invalid country/city combination
* Invalid programme selection
* Unsupported criteria combination
* Invalid input value

The system should guide the user toward correcting the search rather than simply failing silently.

---

# 11. Search Result Requirements

A successful search should return information that enables the user to identify relevant opportunities.

Search results should provide sufficient information to support the next decision in the journey.

At minimum, applicable results should allow the user to identify:

* Institution
* Location
* Programme
* Programme level/type
* Relevant intake information

Additional information may be presented on the institution or programme detail page.

---

# 12. Search-to-Application Journey

The search feature should connect naturally to the broader student journey.

```text
Search Criteria
      ↓
Search Results
      ↓
Institution / Programme
      ↓
Programme Details
      ↓
Apply
      ↓
Application Workflow
```

The search function should therefore be treated as part of the wider product journey rather than an isolated feature.

---

# 13. Business Rules

| Rule ID   | Business Rule                                                                  |
| --------- | ------------------------------------------------------------------------------ |
| SR-BR-001 | Search should support one or more applicable criteria.                         |
| SR-BR-002 | Search fields should not be unnecessarily mandatory.                           |
| SR-BR-003 | City options should be associated with the selected country.                   |
| SR-BR-004 | Changing country should update applicable city options.                        |
| SR-BR-005 | Search values should use controlled database values where appropriate.         |
| SR-BR-006 | Multiple criteria should be capable of working together.                       |
| SR-BR-007 | Supported fields may allow multiple selections where applicable.               |
| SR-BR-008 | Search results should be consistently presented.                               |
| SR-BR-009 | Applicable results should be alphabetically ordered.                           |
| SR-BR-010 | No matching records should generate a clear no-results response.               |
| SR-BR-011 | Invalid search combinations should be handled appropriately.                   |
| SR-BR-012 | Search results should support progression toward programme review/application. |
| SR-BR-013 | Search should not require users to provide information they do not have.       |

---

# 14. Functional Requirements Derived from Search Rules

| Requirement ID | Requirement                                                                  |
| -------------- | ---------------------------------------------------------------------------- |
| SR-FR-001      | The system shall allow users to search using one or more available criteria. |
| SR-FR-002      | The system shall allow country-based searching.                              |
| SR-FR-003      | The system shall allow city-based filtering where applicable.                |
| SR-FR-004      | The system shall associate cities with their relevant countries.             |
| SR-FR-005      | The system shall allow institution-based searching.                          |
| SR-FR-006      | The system shall allow programme-based searching.                            |
| SR-FR-007      | The system shall allow intake-based filtering.                               |
| SR-FR-008      | The system shall support applicable combinations of search criteria.         |
| SR-FR-009      | The system shall support multi-selection for applicable fields.              |
| SR-FR-010      | The system shall display an appropriate no-results message.                  |
| SR-FR-011      | The system shall provide appropriate feedback for invalid inputs.            |
| SR-FR-012      | The system shall present search results consistently.                        |

---

# 15. Example Search Scenarios

## Scenario 1 — Country Only

**Input:**

Country = United Kingdom

**Expected Result:**

The system returns relevant institutions/programmes associated with the selected country.

---

## Scenario 2 — Country + City

**Input:**

Country = United Kingdom
City = London

**Expected Result:**

The system returns relevant records associated with London, United Kingdom.

---

## Scenario 3 — Programme Only

**Input:**

Programme = Business Analytics

**Expected Result:**

The system returns relevant programmes matching the selected programme criteria.

---

## Scenario 4 — Country + Programme

**Input:**

Country = United Kingdom
Programme = Business Analytics

**Expected Result:**

The system returns relevant Business Analytics opportunities associated with the selected country.

---

## Scenario 5 — No Results

**Input:**

Criteria combination produces no matching record.

**Expected Result:**

The system displays a clear no-results message and allows the user to modify their criteria.

---

# 16. Business Analyst Considerations

Several BA considerations influenced the search design.

### User Flexibility

Users may arrive with different levels of information. The system should not assume every user knows the institution, location, programme, and intake simultaneously.

### Data Quality

Controlled search values help maintain consistency between user input and database records.

### Dependency Management

Country-city dependency reduces invalid geographic combinations.

### Usability

The search experience should minimize unnecessary effort while still providing useful filtering.

### Scalability

The model should support the addition of institutions, locations, programmes, departments, faculties, and intakes without requiring fundamental changes to the search concept.

---

# 17. Traceability

The search requirements connect to other project artefacts:

```text
Business Need
      ↓
Search Requirements
      ↓
Business Rules
      ↓
Functional Requirements
      ↓
User Stories
      ↓
Acceptance Criteria
      ↓
UAT Scenarios
```

This provides a complete requirements-to-validation chain for the search feature.

---

## Confidentiality Note

This document is an anonymized public portfolio reconstruction.

Specific proprietary information, confidential business data, production configurations, internal system details, personal information, and commercially sensitive information have been intentionally excluded.
