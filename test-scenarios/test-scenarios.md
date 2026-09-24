# Test Cases

## Online Loan Application System

---

## TC-001 — Successful Customer Login

**Priority:** Critical
**Type:** Functional / Positive

### Preconditions

* Registered customer account exists.
* Account is active.
* Login page is accessible.

### Test Data

Username: `test.customer@example.com`
Password: `ValidPassword123`

### Steps

1. Open the login page.
2. Enter a valid username.
3. Enter a valid password.
4. Click **Login**.

### Expected Result

* User is successfully authenticated.
* User is redirected to the customer dashboard.
* Customer information is displayed correctly.

---

## TC-002 — Invalid Login Credentials

**Priority:** High
**Type:** Functional / Negative

### Steps

1. Open the login page.
2. Enter a registered username.
3. Enter an incorrect password.
4. Click **Login**.

### Expected Result

* User is not authenticated.
* An appropriate error message is displayed.
* User remains on the login page.

---

## TC-003 — Required Field Validation

**Priority:** High
**Type:** Negative

### Steps

1. Log in.
2. Navigate to the loan application.
3. Leave required customer information blank.
4. Click **Submit**.

### Expected Result

* Application is not submitted.
* Required fields are highlighted.
* Appropriate validation messages are displayed.

---

## TC-004 — Valid Loan Amount

**Priority:** Critical
**Type:** Functional / Positive

### Test Data

Requested loan amount: `100,000`

### Steps

1. Start a new loan application.
2. Enter valid customer information.
3. Enter a loan amount within the allowed range.
4. Complete all required fields.
5. Submit the application.

### Expected Result

* Application passes validation.
* Application is submitted successfully.
* Unique application reference number is generated.

---

## TC-005 — Loan Amount Below Minimum

**Priority:** High
**Type:** Boundary / Negative

### Test Data

Minimum allowed amount: `50,000`

Requested amount: `49,999`

### Steps

1. Start a new loan application.
2. Enter valid customer information.
3. Enter `49,999` as the requested loan amount.
4. Submit the application.

### Expected Result

The system should prevent submission and display a message indicating that the requested amount is below the allowed minimum.

---

## TC-006 — Loan Amount Above Maximum

**Priority:** High
**Type:** Boundary / Negative

### Test Data

Maximum allowed amount: `500,000`

Requested amount: `500,001`

### Expected Result

The system should prevent submission and display an appropriate validation message.

---

## TC-007 — Duplicate Loan Application

**Priority:** High
**Type:** Negative

### Steps

1. Submit a valid loan application.
2. Return to the application page.
3. Attempt to submit the same application again.

### Expected Result

The system should prevent an unintended duplicate application and display an appropriate message.

---

## TC-008 — Supporting Document Upload

**Priority:** High
**Type:** Functional

### Steps

1. Open a loan application.
2. Navigate to supporting documents.
3. Upload a valid supported document.
4. Save the application.

### Expected Result

* Document is uploaded successfully.
* Document name is displayed.
* Document is associated with the correct application.

---

## TC-009 — Customer Information Integration

**Priority:** Critical
**Type:** Integration / API

### Steps

1. Start a loan application for an existing customer.
2. Trigger customer information retrieval.
3. Capture the API response.
4. Compare API response data with the information displayed in the application.

### Expected Result

* API request is successful.
* Expected customer information is returned.
* Customer information displayed in the UI matches the expected response.
* Relevant fields are mapped correctly.

---

## TC-010 — Integration Failure Handling

**Priority:** High
**Type:** Integration / Negative

### Steps

1. Start a loan application.
2. Trigger the external customer verification service.
3. Simulate or use a test environment where the external service returns an error.

### Expected Result

* Application does not incorrectly display successful verification.
* User receives an appropriate error or retry message.
* The application remains in a valid state.
* Error information is logged for investigation.

---

## TC-011 — Application Reference Number

**Priority:** Critical
**Type:** Functional

### Steps

1. Complete all required loan application information.
2. Submit the application.
3. Observe the confirmation page.

### Expected Result

* Application is successfully submitted.
* A unique application reference number is generated.
* Reference number is displayed to the customer.

---

## TC-012 — End-to-End Loan Application

**Priority:** Critical
**Type:** End-to-End

### Steps

1. Log in as a valid customer.
2. Start a new loan application.
3. Select a loan product.
4. Enter customer information.
5. Enter employment information.
6. Enter loan amount.
7. Upload required documents.
8. Submit the application.
9. Verify customer/application information.
10. Verify credit assessment integration.
11. Verify application status.

### Expected Result

The complete loan application workflow should execute successfully without data loss or incorrect status transitions.
