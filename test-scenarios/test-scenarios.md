# Test Scenarios

## Online Loan Application System

| ID     | Module             | Test Scenario                                                                | Priority |
| ------ | ------------------ | ---------------------------------------------------------------------------- | -------- |
| TS-001 | Registration       | Verify a new customer can register successfully                              | High     |
| TS-002 | Registration       | Verify registration validation for required fields                           | High     |
| TS-003 | Registration       | Verify duplicate email registration is prevented                             | High     |
| TS-004 | Login              | Verify user can log in with valid credentials                                | Critical |
| TS-005 | Login              | Verify invalid credentials are rejected                                      | High     |
| TS-006 | Login              | Verify account behavior after multiple failed login attempts                 | Medium   |
| TS-007 | Loan Application   | Verify customer can start a new loan application                             | Critical |
| TS-008 | Loan Application   | Verify required customer information is validated                            | High     |
| TS-009 | Loan Application   | Verify valid loan amount can be entered                                      | Critical |
| TS-010 | Loan Application   | Verify minimum loan amount validation                                        | High     |
| TS-011 | Loan Application   | Verify maximum loan amount validation                                        | High     |
| TS-012 | Loan Application   | Verify invalid characters are rejected from numeric fields                   | Medium   |
| TS-013 | Loan Application   | Verify supporting documents can be uploaded                                  | High     |
| TS-014 | Loan Application   | Verify unsupported document formats are rejected                             | Medium   |
| TS-015 | Loan Application   | Verify duplicate loan submission is prevented                                | High     |
| TS-016 | Integration        | Verify customer information is correctly retrieved from the customer service | Critical |
| TS-017 | Integration        | Verify credit assessment request is sent with correct information            | Critical |
| TS-018 | Integration        | Verify system handles integration timeout                                    | High     |
| TS-019 | Integration        | Verify system handles an unsuccessful API response                           | High     |
| TS-020 | Application Status | Verify submitted application receives a reference number                     | Critical |
| TS-021 | Application Status | Verify customer can view submitted application status                        | High     |
| TS-022 | Application Status | Verify approved application displays correct status                          | Critical |
| TS-023 | Application Status | Verify rejected application displays correct status                          | High     |
| TS-024 | Regression         | Verify existing customer application flow after release changes              | Critical |
| TS-025 | End-to-End         | Verify complete loan application journey from login to decision              | Critical |

## Scenario Categories

### Functional

Verify that each feature performs according to the documented requirements.

### Negative

Verify that invalid inputs, missing information, duplicate submissions, and unsuccessful integrations are handled correctly.

### Boundary

Verify values at and around business-rule limits, such as minimum and maximum loan amounts.

### Integration

Verify correct data exchange between the loan application and external services.

### Regression

Verify that existing functionality continues to work after changes.

### End-to-End

Verify the complete business journey from customer login through loan application submission and decision.
