
# Test Plan — Swag Labs E-Commerce Application

| Document Field | Details |
|---|---|
| Project | Manual QA Portfolio |
| Application | [Swag Labs / SauceDemo](https://www.saucedemo.com/) |
| Document ID | QA-TP-001 |
| Version | 1.0 |
| Status | Planned |
| Testing Type | Manual Functional, Exploratory and Regression Testing |
| Prepared By | Kiran Naik |
| Execution Status | Not Started |

## 1. Objective

The objective of this test plan is to define the scope, strategy, test conditions, resources, risks and completion criteria for evaluating the Swag Labs sample e-commerce application.

Testing will focus on validating critical user journeys, identifying functional issues, checking negative scenarios, and documenting reproducible findings.

The goal is to demonstrate a professional, risk-based QA process and provide clear evidence that supports informed release decisions.

## 2. Application Overview

Swag Labs is a sample web application representing an online shopping experience.

The core workflows selected for this assessment are:

- User authentication
- Product inventory and product details
- Product sorting
- Shopping cart operations
- Checkout information and validation
- Order completion and confirmation

The application is used solely as a portfolio test target. This project does not represent an engagement with the application's owner.

## 3. Scope of Testing

### 3.1 In Scope

**Authentication**
- Successful login using designated demo credentials
- Invalid username or password
- Empty required fields
- Error message visibility and clarity
- Logout behaviour
- Navigation after authentication

**Product Inventory**
- Product list visibility and content consistency
- Product information and price display
- Product details navigation, where available
- Sorting by available supported attributes
- Add-to-cart and remove-from-cart controls

**Shopping Cart**
- Adding one or multiple products
- Removing products from the cart
- Cart item count and displayed products
- Navigation between inventory and cart
- Cart state during supported navigation flows

**Checkout**
- Required customer information
- Empty and incomplete form submissions
- Valid and invalid input handling
- Order summary and item consistency
- Price calculations, including subtotal and displayed totals
- Order completion and confirmation behaviour

**Usability and Basic Compatibility**
- Visibility and usability of primary controls
- Layout at the selected desktop viewport
- Basic keyboard navigation and focus behaviour
- Clear feedback for validation errors
- Additional viewport or browser checks where accessible

### 3.2 Out of Scope

- Source-code review and internal implementation testing
- Backend infrastructure and database testing
- Real payment gateway or financial transaction testing
- Load, stress and performance testing
- Dedicated penetration testing or security certification
- Native Android and iOS application testing
- Production customer data or real customer accounts

Security-sensitive behaviour will not be probed beyond authorised, low-risk functional checks.

## 4. Test Strategy

Testing will follow a risk-based approach, prioritising authentication, cart consistency and checkout because these workflows directly affect the shopping journey.

### Functional Testing

Verify that each feature behaves according to its observable requirements and supported application behaviour.

### Negative Testing

Check invalid credentials, missing mandatory information, unsupported input and rejected operations.

### Boundary and Validation Testing

Examine required-field handling, input constraints, and relevant minimum or maximum values where the application exposes such rules.

### Exploratory Testing

Investigate plausible user behaviours beyond the predefined cases, including navigation changes, repeated actions and unexpected sequences.

### Regression Testing

Repeat selected critical scenarios after a relevant change or fix. When no application change is available, document the scenarios as a repeatable regression baseline rather than claiming that a fix was verified.

### Usability and Compatibility Checks

Evaluate essential control visibility, error feedback, keyboard access and selected browser or viewport behaviour.

## 5. Test Environment

Record the actual environment used during execution.

| Attribute | Planned Configuration |
|---|---|
| Target | Public Swag Labs demo |
| Environment | Web application accessed through a browser |
| Primary Browser | Chrome, version to be recorded |
| Operating System | Windows, version to be recorded |
| Viewport | Desktop resolution, to be recorded |
| Secondary Browser | Optional, subject to availability |
| Test Account | Designated demo account |
| Test Data | Non-sensitive test inputs |
| Execution Method | Manual testing |

The actual browser version, operating system, viewport and execution date must be recorded in the execution report. Planned configuration must not be presented as an already-tested environment.

## 6. Test Data Strategy

Use designated demo accounts and non-sensitive inputs intended for the sample application.

Test data categories include:

- Valid demo credentials
- Invalid username and password combinations
- Empty required fields
- Valid and incomplete checkout information
- Product selection and removal sequences
- Different product combinations for cart validation
- Supported sorting options
- Repeated actions and navigation sequences

Do not use personal, employer or real customer data. Do not publish credentials, tokens or sensitive account information in evidence.

## 7. Test Execution Process

1. Access the demo application and verify that it is available.
2. Record the browser, operating system, viewport and execution date.
3. Review the planned scenarios and confirm the applicable test data.
4. Execute each test case and compare actual results with expected results.
5. Record Pass, Fail, Blocked or Not Run for every applicable case.
6. Capture appropriate screenshots and concise reproduction steps for failures.
7. Log reproducible deviations in the defect register.
8. Re-test resolved issues only when a relevant change is available.
9. Prepare an execution summary with outstanding risks and limitations.

A scenario must not be marked as Passed solely because the page loaded or an element was visible. Its defined expected behaviour must be verified.

## 8. Defect Reporting and Prioritisation

Each reported defect should include:

- Unique defect ID
- Concise, specific title
- Application area and environment
- Preconditions and test data, where relevant
- Reproducible steps
- Expected result
- Actual result
- Severity and suggested priority
- Screenshot or other supporting evidence
- Current status and retest outcome, when applicable

### Severity Guidelines

| Severity | Definition |
|---|---|
| Critical | A verified issue causing a major system failure, severe data impact or complete loss of a critical capability |
| High | A major functional failure affecting a critical workflow with no reasonable workaround |
| Medium | A meaningful functional issue with limited impact or an available workaround |
| Low | A minor visual, usability or non-critical functional issue |

Severity must reflect the observed impact. Priority should be evaluated separately based on business urgency, user impact and release context.

These classifications are portfolio guidelines and may be adapted to a client's defect management process.

## 9. Entry Criteria

Testing may begin when:

- The demo application is accessible.
- The planned scope and scenarios have been reviewed.
- Appropriate demo test data is available.
- The browser and execution environment have been recorded.
- The application is sufficiently stable to attempt the selected workflows.

If these conditions are not met, record the limitation and its impact.

## 10. Exit Criteria

The planned testing activity may be considered complete when:

- Every in-scope test case has an execution status.
- Critical user journeys have been attempted.
- Failed and blocked cases have supporting explanations.
- Verified defects have reproducible evidence.
- Outstanding risks and untested areas are documented.
- An execution summary is prepared.

Completion of testing does not imply that the application is defect-free.

Any release recommendation must reflect the observed results and the limitations of the test scope.

## 11. Risks and Mitigations

| Risk | Mitigation |
|---|---|
| Public demo is unavailable | Record the blocker and resume when access is restored |
| Demo behaviour differs from expectations | Verify observable behaviour before logging a defect |
| Test data or cart state becomes inconsistent | Repeat the scenario from a documented starting state |
| Browser-specific differences occur | Record browser versions and reproduce before reporting |
| Evidence contains sensitive information | Review and sanitise screenshots before publication |
| Scope expands during execution | Record additional scenarios separately and assess their impact |

## 12. Deliverables

The planned portfolio deliverables are:

1. Test plan and scope definition
2. Detailed test cases and expected results
3. Exploratory testing checklist
4. Reusable defect report template
5. Execution report with measured outcomes
6. Supporting evidence for verified findings
7. Summary of coverage, limitations and residual risks

## 13. Assumptions and Limitations

- Testing is performed against the publicly accessible demo application.
- No access to internal source code, backend services or production systems is assumed.
- Application behaviour must be observed during execution rather than inferred from this plan.
- Defects, test results, coverage figures and execution timings will be recorded only after verification.
- Findings describe the observed demo behaviour and must not be generalised to production systems.

## 14. Approval and Revision History

| Version | Change | Status |
|---|---|---|
| 1.0 | Initial test plan created | Planned |
