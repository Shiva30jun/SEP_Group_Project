# Project Title: School Repairs – Create a platform for tracking and reporting the condition of public school buildings

## Project Overview
This project aims to develop a centralized platform to monitor and report the condition of public school buildings within the Waterloo Region District School Board (WRDSB). WRDSB was selected due to recent findings indicating that approximately 45% of its 123 schools are below the state of good repair, with a maintenance backlog estimated at $178 million. The platform seeks to streamline maintenance reporting, enhance transparency, and ensure efficient resource allocation to address critical infrastructure needs, ultimately improving the safety and learning environment for students and staff across the region.

## Key Issues
Recent assessments have highlighted significant challenges regarding the condition of public school buildings in the Waterloo Region. According to the Financial Accountability Office (FAO) of Ontario:

- **Aging and Deteriorating Infrastructure**: Approximately 45% of WRDSB's 123 schools are below the state of good repair, with 55 schools requiring rehabilitation or replacement.
- **Significant Maintenance Backlog**: The infrastructure backlog for these schools is estimated at $178 million, with an additional $401 million needed to bring all schools to a state of good repair over the next decade, totaling $579 million in projected costs.
- **Lack of Centralized Reporting System**: Currently, there's no unified platform for reporting and tracking maintenance issues, leading to delays and inefficiencies.


## Actionable Requirements

### 1. Aging and Infrastructure Condition

**User Story**:  
As a WRDSB Facilities Manager, I want to prioritize schools with aging infrastructure so that maintenance efforts can be effectively allocated to ensure safe learning environments.

**Priority**: 🔴 High  
**GitHub Issue**: #1

**Purpose**:  
Approximately 45% of WRDSB's 123 schools are below the state of good repair, with 55 schools requiring rehabilitation or replacement. This significant proportion of aging infrastructure poses safety risks and hinders the delivery of quality education. Addressing this issue is critical to maintaining safe, functional, and modern educational facilities.

**Implementation Strategy**:
- Conduct comprehensive facility condition assessments across all WRDSB public schools.
- Develop a centralized database to track the condition and maintenance history of each school facility.
- Establish a prioritization framework based on severity, risk, and impact to allocate resources effectively.
- Secure funding through grants and budget allocations to address the identified infrastructure needs.

**Sub-Issues**:

- **Sub-Issue 1**: Develop a Standardized Assessment Protocol
  - **Priority**: 🔴 High
  - **Goal**: Create a consistent methodology for evaluating the condition of school facilities.
  - **Approach**: Collaborate with experts to define assessment criteria and scoring systems.
  - **Tasks**:
    - Review existing assessment tools and identify best practices.
    - Design assessment forms and guidelines.
    - Pilot the assessment protocol in a subset of schools and refine based on feedback.

- **Sub-Issue 2**: Implement a Centralized Facility Condition Database
  - **Priority**: 🟠 Medium
  - **Goal**: Establish a digital repository to store and manage facility condition data.
  - **Approach**: Utilize a relational database system (e.g., PostgreSQL) with a user-friendly interface.
  - **Tasks**:
    - Define data fields (e.g., building age, condition scores, maintenance history).
    - Develop the database schema and implement the system.
    - Train staff on data entry and retrieval processes.

    ```sql
    CREATE TABLE facility_conditions (
        id SERIAL PRIMARY KEY,
        school_name VARCHAR(255) NOT NULL,
        address TEXT,
        construction_year INT,
        last_assessment_date DATE,
        condition_score DECIMAL(5,2),
        recommended_action VARCHAR(100),
        notes TEXT
    );

    CREATE INDEX idx_condition_score ON facility_conditions(condition_score);
    ```

- **Sub-Issue 3**: Establish a Prioritization Framework for Maintenance and Rehabilitation
  - **Priority**: 🔴 High
  - **Goal**: Allocate resources effectively by prioritizing facilities based on need.
  - **Approach**: Develop a scoring system that considers condition scores, student population, and potential risks.
  - **Tasks**:
    - Define prioritization criteria and weightings.
    - Apply the framework to the assessed data to generate a ranked list of schools.
    - Review and adjust the framework periodically to reflect changing needs.

- **Sub-Issue 4**: Monitor and Report on Infrastructure Improvement Progress
  - **Priority**: 🟠 Medium
  - **Goal**: Ensure transparency and accountability in addressing infrastructure issues.
  - **Approach**: Implement a reporting system to track progress and communicate with stakeholders.
  - **Tasks**:
    - Develop key performance indicators (KPIs) for infrastructure improvements.
    - Generate regular progress reports.
    - Solicit feedback and adjust as necessary.


### 2. Significant Maintenance Backlog

**User Story**:  
As a WRDSB Facilities Manager, I want to prioritize the maintenance backlog so that resources are allocated efficiently for all public schools' safety standards.

**Priority**: 🔴 High  
**GitHub Issue**: #2

**Purpose**:  
The WRDSB faces a substantial infrastructure backlog, estimated at $178 million, with an additional $401 million required over the next decade to bring all schools to a state of good repair, totaling $579 million in projected costs. This backlog poses risks to student safety, disrupts educational activities, and may lead to increased costs if not addressed promptly.
