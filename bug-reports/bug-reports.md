# Bug Reports

## Online Loan Application System

The following are sample defects created for portfolio demonstration purposes.

---

# BUG-001 — Application Can Be Submitted Without Required Employment Information

**Severity:** High
**Priority:** High
**Status:** Resolved
**Environment:** QA
**Module:** Loan Application

### Description

The application allows customers to submit a loan application when the required Employment Status field is blank.

### Preconditions

* Customer is logged in.
* Customer has access to the loan application.

### Steps to Reproduce

1. Open a new loan application.
2. Enter valid customer information.
3. Leave Employment Status blank.
4. Enter a valid loan amount.
5. Complete the remaining fields.
6. Click **Submit**.

### Expected Result

The application should not be submitted.

A validation message should indicate that Employment Status is required.

### Actual Result

The application is successfully submitted despite the required field being blank.

### Impact

Incomplete customer information can enter the downstream loan processing workflow.

### Evidence

* Screenshot of submitted application
* Test execution evidence
* Relevant request/response logs

### Suggested Investigation Area

Review client-side and server-side validation for the Employment Status field.

---

# BUG-002 — Incorrect Maximum Loan Amount Validation

**Severity:** High
**Priority:** High
**Status:** Resolved
**Environment:** QA
**Module:** Loan Application

### Steps to Reproduce

1. Start a new loan application.
2. Enter valid customer information.
3. Enter a loan amount of `500,001`.
4. Submit the application.

### Expected Result

The system should reject the amount because the maximum permitted amount is `500,000`.

### Actual Result

The application accepts the amount and proceeds to the next step.

### Impact

Customers may submit applications exceeding the configured product limit.

---

# BUG-003 — Incorrect Customer Information Displayed After API Retrieval

**Severity:** High
**Priority:** High
**Status:** Resolved
**Environment:** QA
**Module:** Customer Integration

### Steps to Reproduce

1. Log in using an existing test customer.
2. Start a new loan application.
3. Trigger customer information retrieval.
4. Capture the API response.
5. Compare the returned customer information with the UI.

### Expected Result

The customer information displayed in the UI should match the relevant fields returned by the API.

### Actual Result

The API returns the correct customer information, but the Employment Status displayed in the UI does not match the API response.

### Investigation

* API response was reviewed using Postman.
* UI field mapping was compared with the response.
* Test data combinations were reviewed.
* The mapping logic was identified as the source of the discrepancy.

### Impact

Incorrect customer information may affect downstream loan assessment.

### Resolution

Field mapping was corrected and regression testing was performed.

---

# BUG-004 — Duplicate Application Created After Double Submission

**Severity:** Medium
**Priority:** High
**Status:** Open
**Environment:** QA
**Module:** Loan Application

### Steps to Reproduce

1. Complete a valid loan application.
2. Click **Submit**.
3. Quickly click **Submit** again before the confirmation page loads.

### Expected Result

Only one loan application should be created.

### Actual Result

Two application records are created.

### Impact

Duplicate applications may require manual investigation and processing.

### Recommendation for Investigation

Review button state handling, request duplication prevention, and server-side idempotency.
