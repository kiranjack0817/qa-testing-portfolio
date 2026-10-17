
# Test Cases — Swag Labs E-Commerce Application

| Document Field | Details |
|---|---|
| Project | Manual QA Portfolio |
| Document ID | QA-TC-001 |
| Version | 1.0 |
| Prepared By | Kiran Naik |
| Application | [Swag Labs](https://www.saucedemo.com/) |
| Status | Planned — Not Yet Executed |

## 1. Objective

This document defines repeatable manual test cases for core e-commerce workflows, including authentication, product inventory, sorting, cart management, and checkout.

Every test case includes a unique ID, priority, preconditions, execution steps, expected results, and an execution status.

## 2. Test Environment

Record the actual environment before execution.

- Operating System: To be recorded
- Browser and Version: To be recorded
- Viewport: To be recorded
- Execution Date: To be recorded
- Application: https://www.saucedemo.com/
- Test Data: Designated demo accounts and non-sensitive sample inputs

## 3. Test Cases

### TC-001 — Successful Login

**Priority:** P1  
**Module:** Authentication  
**Preconditions:** Application is accessible. A valid demo account is available.

**Steps**
1. Open the application.
2. Enter the designated valid username.
3. Enter the corresponding password.
4. Click Login.

**Expected Result**
- The user is authenticated.
- The inventory page is displayed.
- Product information and primary navigation controls are visible.

**Status:** Not Run

---

### TC-002 — Login with Invalid Password

**Priority:** P1  
**Module:** Authentication  
**Preconditions:** Application is accessible.

**Steps**
1. Open the login page.
2. Enter a designated demo username.
3. Enter an incorrect password.
4. Click Login.

**Expected Result**
- Authentication is rejected.
- An appropriate error message is displayed.
- The user remains on the login page.

**Status:** Not Run

---

### TC-003 — Login with Empty Username

**Priority:** P1  
**Module:** Authentication  
**Preconditions:** Login page is displayed.

**Steps**
1. Leave the username field empty.
2. Enter a password.
3. Click Login.

**Expected Result**
- Authentication does not proceed.
- A validation message identifies the missing username.

**Status:** Not Run

---

### TC-004 — Login with Empty Password

**Priority:** P1  
**Module:** Authentication  
**Preconditions:** Login page is displayed.

**Steps**
1. Enter a designated demo username.
2. Leave the password field empty.
3. Click Login.

**Expected Result**
- Authentication does not proceed.
- A validation message identifies the missing password.

**Status:** Not Run

---

### TC-005 — Login with a Locked-Out Demo Account

**Priority:** P2  
**Module:** Authentication  
**Preconditions:** A designated demo account documented as locked out is available.

**Steps**
1. Open the login page.
2. Enter the locked-out demo account credentials.
3. Click Login.

**Expected Result**
- Access is denied.
- An appropriate locked-out account message is displayed.
- The inventory page is not accessible through this login attempt.

**Status:** Not Run

---

### TC-006 — Logout Successfully

**Priority:** P1  
**Module:** Authentication  
**Preconditions:** User is logged in.

**Steps**
1. Open the navigation menu.
2. Select Logout.
3. Observe the destination page.

**Expected Result**
- The user returns to the login page.
- The authenticated session is ended according to the application's behaviour.
- Login controls are available.

**Status:** Not Run

---

### TC-007 — Verify Product Inventory

**Priority:** P1  
**Module:** Product Inventory  
**Preconditions:** User is logged in.

**Steps**
1. Open the inventory page.
2. Review the displayed product cards.
3. Inspect product names, prices, images, and available controls.

**Expected Result**
- Product cards are displayed.
- Each displayed product has the information and controls expected by the application.
- No unintended blank or visibly broken product cards are present.

**Status:** Not Run

---

### TC-008 — Open Product Details

**Priority:** P2  
**Module:** Product Inventory  
**Preconditions:** Inventory page is displayed and at least one product is available.

**Steps**
1. Select a product name or image.
2. Observe the product details page.
3. Compare the displayed product information with the inventory card.

**Expected Result**
- The appropriate product details are displayed.
- Product name and price are consistent between the inventory card and details page.
- Navigation back to inventory is available.

**Status:** Not Run

---

### TC-009 — Sort Products by Name: A to Z

**Priority:** P2  
**Module:** Product Sorting  
**Preconditions:** Inventory contains multiple products.

**Steps**
1. Open the product sorting control.
2. Select the name ascending option.
3. Review the order of the displayed product names.

**Expected Result**
- Products are ordered alphabetically from A to Z.
- The selected sorting option is reflected in the control.

**Status:** Not Run

---

### TC-010 — Sort Products by Name: Z to A

**Priority:** P2  
**Module:** Product Sorting  
**Preconditions:** Inventory contains multiple products.

**Steps**
1. Open the product sorting control.
2. Select the name descending option.
3. Review the order of the product names.

**Expected Result**
- Products are ordered alphabetically from Z to A.
- The selected sorting option is reflected in the control.

**Status:** Not Run

---

### TC-011 — Sort Products by Price: Low to High

**Priority:** P2  
**Module:** Product Sorting  
**Preconditions:** Inventory contains multiple products with different prices.

**Steps**
1. Open the sorting control.
2. Select the price ascending option.
3. Review the displayed product prices.

**Expected Result**
- Products are displayed in ascending numerical price order.
- The selected sorting option is reflected in the control.

**Status:** Not Run

---

### TC-012 — Sort Products by Price: High to Low

**Priority:** P2  
**Module:** Product Sorting  
**Preconditions:** Inventory contains multiple products with different prices.

**Steps**
1. Open the sorting control.
2. Select the price descending option.
3. Review the displayed product prices.

**Expected Result**
- Products are displayed in descending numerical price order.
- The selected sorting option is reflected in the control.

**Status:** Not Run

---

### TC-013 — Add One Product to the Cart

**Priority:** P1  
**Module:** Shopping Cart  
**Preconditions:** User is logged in and at least one product is available.

**Steps**
1. Select Add to cart for one product.
2. Observe the product control.
3. Observe the cart item count.

**Expected Result**
- The selected product is added to the cart.
- The corresponding control changes to its remove action, where supported.
- The cart count reflects the added item.

**Status:** Not Run

---

### TC-014 — Add Multiple Products to the Cart

**Priority:** P1  
**Module:** Shopping Cart  
**Preconditions:** User is logged in and multiple products are available.

**Steps**
1. Add two distinct products to the cart.
2. Observe the cart count.
3. Open the cart.

**Expected Result**
- Both selected products appear in the cart.
- The displayed cart count matches the number of selected items.
- Product names and prices match the inventory.

**Status:** Not Run

---

### TC-015 — Remove a Product from Inventory Cart Selection

**Priority:** P2  
**Module:** Shopping Cart  
**Preconditions:** At least one product has been added to the cart from the inventory page.

**Steps**
1. Locate the selected product.
2. Click its Remove control.
3. Observe the cart count.
4. Open the cart and inspect its contents.

**Expected Result**
- The selected product is removed from the cart.
- The cart count is updated correctly.
- The removed product is absent from the cart.

**Status:** Not Run

---

### TC-016 — Verify Cart Contents After Navigation

**Priority:** P2  
**Module:** Shopping Cart  
**Preconditions:** At least one product has been added to the cart.

**Steps**
1. Open the cart.
2. Navigate back to the inventory page using the application control.
3. Open the cart again.

**Expected Result**
- Cart contents remain consistent during the supported navigation flow.
- Product selection and cart count are not unintentionally changed.

**Status:** Not Run

---

### TC-017 — Remove a Product from the Cart Page

**Priority:** P2  
**Module:** Shopping Cart  
**Preconditions:** At least one product appears in the cart.

**Steps**
1. Open the cart.
2. Click Remove for one selected product.
3. Review the cart contents and count.

**Expected Result**
- The selected product is removed.
- Remaining products stay in the cart.
- The displayed count reflects the remaining items, where shown.

**Status:** Not Run

---

### TC-018 — Checkout with an Empty First Name

**Priority:** P1  
**Module:** Checkout Validation  
**Preconditions:** A product is in the cart and checkout can be started.

**Steps**
1. Open the cart.
2. Click Checkout.
3. Leave First Name empty.
4. Enter values into the other required fields.
5. Continue.

**Expected Result**
- The checkout form is not accepted.
- A validation message identifies the missing first name.
- The user can correct the input.

**Status:** Not Run

---

### TC-019 — Checkout with an Empty Last Name

**Priority:** P1  
**Module:** Checkout Validation  
**Preconditions:** A product is in the cart and the checkout information page is displayed.

**Steps**
1. Enter a valid first name.
2. Leave Last Name empty.
3. Enter a valid postal code.
4. Continue.

**Expected Result**
- The form is not accepted.
- A validation message identifies the missing last name.

**Status:** Not Run

---

### TC-020 — Checkout with an Empty Postal Code

**Priority:** P1  
**Module:** Checkout Validation  
**Preconditions:** A product is in the cart and the checkout information page is displayed.

**Steps**
1. Enter a valid first name.
2. Enter a valid last name.
3. Leave Postal Code empty.
4. Continue.

**Expected Result**
- The form is not accepted.
- A validation message identifies the missing postal code.

**Status:** Not Run

---

### TC-021 — Verify Checkout Overview

**Priority:** P1  
**Module:** Checkout  
**Preconditions:** A product is in the cart and valid checkout information has been provided.

**Steps**
1. Complete the checkout information form.
2. Continue to the overview page.
3. Compare the products and prices with the cart.
4. Review the subtotal, tax, and displayed total.

**Expected Result**
- The selected products appear in the overview.
- Product names, quantities where applicable, and prices are consistent with the cart.
- The subtotal equals the sum of the displayed item prices.
- The displayed total reconciles with the subtotal and displayed tax according to the application's calculation rules.

**Status:** Not Run

---

### TC-022 — Complete the Checkout Flow

**Priority:** P1  
**Module:** Checkout  
**Preconditions:** Checkout overview is displayed with a valid cart.

**Steps**
1. Review the selected products and displayed totals.
2. Click Finish.
3. Observe the confirmation page.

**Expected Result**
- The checkout flow completes successfully.
- A confirmation message is displayed.
- The completed order flow presents the expected confirmation state.

**Status:** Not Run

---

### TC-023 — Cancel Checkout and Return to Inventory

**Priority:** P2  
**Module:** Checkout Navigation  
**Preconditions:** Checkout has been started from a cart containing at least one product.

**Steps**
1. Navigate to the checkout information or overview page.
2. Select the available Cancel control.
3. Observe the destination page.

**Expected Result**
- The application returns to the expected preceding shopping page.
- Navigation does not unintentionally complete the order.
- The cart state is consistent with the application's supported behaviour.

**Status:** Not Run

---

### TC-024 — Verify Keyboard Navigation on the Login Page

**Priority:** P3  
**Module:** Basic Accessibility and Usability  
**Preconditions:** Login page is displayed.

**Steps**
1. Use Tab to move through the login controls.
2. Observe focus visibility.
3. Enter test inputs using the keyboard.
4. Use the keyboard to activate Login where supported.

**Expected Result**
- The principal login controls can be reached using the keyboard.
- Keyboard focus is visible.
- The controls can be operated without requiring a mouse, subject to the application's supported behaviour.

**Status:** Not Run

## 4. Execution Status Definitions

| Status | Meaning |
|---|---|
| Not Run | The test has not been executed |
| Pass | Actual behaviour matches the expected result |
| Fail | Actual behaviour differs from the expected result |
| Blocked | Execution cannot continue because of an identified blocker |
| Not Applicable | The scenario does not apply to the tested configuration |

A test should be marked Failed only after the behaviour has been observed and compared with its expected result.

## 5. Execution Record

Record the following for each executed test:

- Test Case ID
- Execution Date
- Browser and Version
- Actual Result
- Status
- Evidence Reference
- Defect ID, if applicable
- Notes

Do not claim an executed test, discovered defect, coverage percentage, or pass rate until the result has been verified.

## 6. Traceability

Test cases cover the planned authentication, product inventory, sorting, cart management, checkout, and basic keyboard usability scope defined in `docs/test-plan.md`.

Additional scenarios discovered during exploratory testing should be documented and assigned unique IDs before being added to the execution record.
