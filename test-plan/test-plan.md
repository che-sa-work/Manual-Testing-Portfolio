# Test Plan

## Online Loan Application System

**Document Version:** 1.0
**Project:** Online Loan Application System
**Testing Phase:** System Testing
**Test Environment:** QA
**Prepared By:** QA Team
**Status:** Completed

---

## 1. Objective

The objective of this test plan is to define the testing approach, scope, resources, test activities, and acceptance criteria for the Online Loan Application System.

The testing will verify that customers can successfully register, submit loan applications, and track application status while ensuring that business rules, validations, integrations, and error handling work as expected.

---

## 2. Application Overview

The Online Loan Application System allows customers to:

* Register and manage their accounts
* Log in securely
* Submit loan applications
* Provide personal and employment information
* Select loan products
* Enter requested loan amounts
* Upload supporting documents
* Submit applications for assessment
* View application status
* Receive application decisions

The system integrates with external services for customer verification and credit assessment.

---

## 3. Scope

### In Scope

* User registration
* User login
* Customer profile
* Loan product selection
* Loan application submission
* Required-field validation
* Business-rule validation
* Document upload
* Application status
* Application search
* Application approval/rejection status
* API integration
* Error handling
* Regression testing
* End-to-end loan application flow

### Out of Scope

* Performance/load testing
* Production deployment validation
* Third-party system internal processing
* Infrastructure testing
* Security penetration testing

---

## 4. Testing Types

The following testing activities will be performed:

* Functional Testing
* Positive Testing
* Negative Testing
* Boundary Testing
* Integration Testing
* API Testing
* Regression Testing
* End-to-End Testing
* Exploratory Testing
* User Acceptance Support

---

## 5. Test Approach

Testing will be risk-based and requirement-driven.

The QA process will include:

1. Review requirements and acceptance criteria.
2. Identify functional and business-rule scenarios.
3. Identify positive, negative, boundary, and edge cases.
4. Prepare test cases and test data.
5. Execute tests in the QA environment.
6. Record and investigate defects.
7. Retest resolved defects.
8. Execute regression testing.
9. Validate critical end-to-end workflows.
10. Prepare the test summary report.

---

## 6. Entry Criteria

Testing can begin when:

* Requirements and acceptance criteria are available.
* Test environment is accessible.
* Build has been deployed to QA.
* Required test accounts are available.
* Required test data is available.
* Major blocking defects from previous testing have been resolved or accepted.

---

## 7. Exit Criteria

Testing can be considered complete when:

* Planned critical and high-priority scenarios have been executed.
* All critical defects are resolved or formally accepted.
* High-severity defects have been resolved or have an approved workaround/risk acceptance.
* Regression testing has been completed.
* Critical end-to-end workflows have passed.
* Test results have been documented.

---

## 8. Test Data

Sample test data will include:

* Valid customer information
* Invalid customer information
* Existing customers
* New customers
* Different employment statuses
* Different loan amounts
* Boundary loan amounts
* Invalid loan amounts
* Duplicate applications
* Valid and invalid supporting documents

No real customer or personally identifiable information will be used.

---

## 9. Defect Management

Defects will be documented with:

* Defect ID
* Summary
* Environment
* Preconditions
* Steps to reproduce
* Expected result
* Actual result
* Severity
* Priority
* Evidence
* Status

Defects will be tracked through their lifecycle from identification through resolution and verification.

---

## 10. Risks

| Risk                             | Impact | Mitigation                                         |
| -------------------------------- | ------ | -------------------------------------------------- |
| Test environment unavailable     | High   | Coordinate environment availability before testing |
| Incomplete test data             | Medium | Prepare test data before execution                 |
| External integration unavailable | High   | Use agreed test stubs/mocks where applicable       |
| Late requirement changes         | Medium | Review impact and update affected tests            |
| Critical defect discovered late  | High   | Prioritize critical business flows early           |

---

## 11. Deliverables

The following deliverables will be produced:

* Test Plan
* Test Scenarios
* Test Cases
* Defect Reports
* Test Execution Results
* Test Summary Report

---

## 12. Approval

Testing completion and release readiness should be reviewed with the relevant QA, Product, Business, and Development stakeholders.

