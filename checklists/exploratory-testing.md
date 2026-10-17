
# Exploratory Testing Checklist — Swag Labs

| Field | Details |
|---|---|
| Project | Manual QA Portfolio |
| Document ID | QA-EXP-001 |
| Application | https://www.saucedemo.com/ |
| Testing Type | Exploratory Testing |
| Prepared By | Kiran Naik |
| Status | Planned |
| Execution Date | To be recorded |

## 1. Objective

Explore important application workflows beyond the predefined test cases to identify unexpected behaviour, inconsistent data, usability issues, and potential functional defects.

Exploratory testing combines learning, test design, execution, and observation. Each finding must be supported by actual observations and reproducible steps.

## 2. Test Session Information

Record before each session:

- Date and start/end time
- Browser name and version
- Operating system and version
- Screen resolution and viewport, where available
- Application URL
- Test account type, without recording its password
- Session charter and testing scope
- Execution limitations or environmental issues

## 3. Session A — Authentication

### Login Page
- [ ] Verify that the login page loads successfully.
- [ ] Verify that username and password fields are visible and usable.
- [ ] Verify that password characters are masked.
- [ ] Navigate between controls using the keyboard.
- [ ] Observe focus visibility and tab order.
- [ ] Attempt login using the designated valid demo account.
- [ ] Attempt login with an incorrect password.
- [ ] Attempt login with an empty username.
- [ ] Attempt login with an empty password.
- [ ] Attempt login with both fields empty.
- [ ] Review error messages for clarity and consistency.
- [ ] Verify that a locked-out demo account is handled as expected.

### Session and Navigation
- [ ] Log out and observe the destination page.
- [ ] Use browser Back after logout and observe session behaviour.
- [ ] Refresh the login page.
- [ ] Verify that the application responds consistently to repeated login attempts.

Record unexpected behaviour without assuming that it is a defect until the expected behaviour and reproducibility are established.

## 4. Session B — Product Inventory and Sorting

### Product Display
- [ ] Verify that product cards are displayed.
- [ ] Inspect product names, prices, and descriptions.
- [ ] Check whether product images load and correspond to the displayed products.
- [ ] Open selected product details and compare information.
- [ ] Navigate back to the inventory page.
- [ ] Observe page layout and content alignment.

### Sorting
- [ ] Select name ascending and inspect the order.
- [ ] Select name descending and inspect the order.
- [ ] Select price ascending and inspect the order.
- [ ] Select price descending and inspect the order.
- [ ] Switch between sorting options repeatedly.
- [ ] Observe whether the selected sorting option matches the displayed order.

## 5. Session C — Shopping Cart

- [ ] Add one product to the cart.
- [ ] Verify the cart count.
- [ ] Add a second distinct product.
- [ ] Compare the cart count with the selected items.
- [ ] Open the cart and compare its contents with the selected products.
- [ ] Remove one product from the inventory page.
- [ ] Remove one product from the cart page.
- [ ] Use Continue Shopping and return to the inventory.
- [ ] Open the cart again and observe state consistency.
- [ ] Refresh the page and observe cart state.
- [ ] Use browser Back and Forward to inspect navigation behaviour.
- [ ] Explore the empty-cart state.
- [ ] Observe button labels after add/remove operations.

## 6. Session D — Checkout

### Customer Information
- [ ] Start checkout with a product in the cart.
- [ ] Submit with all required fields empty.
- [ ] Leave First Name empty.
- [ ] Leave Last Name empty.
- [ ] Leave Postal Code empty.
- [ ] Correct an invalid submission and retry.
- [ ] Inspect validation messages.
- [ ] Enter normal valid sample information.
- [ ] Explore leading/trailing spaces and reasonable boundary inputs.
- [ ] Observe handling of unsupported or unusual characters without running security attacks.

### Checkout Overview
- [ ] Compare overview items with the cart.
- [ ] Compare item prices with inventory prices.
- [ ] Verify the displayed subtotal against the sum of item prices.
- [ ] Verify the displayed total against the application's displayed subtotal, tax, and calculation rules.
- [ ] Cancel checkout and observe the destination.
- [ ] Restart checkout and observe whether data remains as expected.

### Order Completion
- [ ] Complete the checkout flow using non-sensitive sample information.
- [ ] Verify the confirmation message.
- [ ] Observe the available post-order navigation.
- [ ] Use browser navigation after completion and record the observed behaviour.

## 7. Session E — Usability and Responsive Behaviour

- [ ] Verify primary controls are visible and usable at the selected desktop size.
- [ ] Check for overlapping, clipped, or hidden content.
- [ ] Inspect long-page scrolling behaviour.
- [ ] Check keyboard access for important actions.
- [ ] Observe focus visibility on interactive controls.
- [ ] Resize the browser to a narrower viewport.
- [ ] Inspect the login, inventory, cart, and checkout layouts where practical.
- [ ] Check whether validation messages remain visible and understandable.
- [ ] Record browser-specific issues only after reproducing them.

## 8. Exploratory Session Log

| Field | Entry |
|---|---|
| Session ID | QA-EXP-S01 |
| Charter | Authentication and session behaviour |
| Areas Explored | To be recorded |
| Time Spent | To be recorded |
| Observations | To be recorded |
| Test Cases Added | To be recorded |
| Potential Defect IDs | To be recorded |
| Limitations | To be recorded |

Duplicate this section for each distinct exploratory session.

## 9. Observation and Defect Record

For each noteworthy observation, record:

- Observation ID
- Feature or workflow
- Preconditions
- Actions performed
- Expected behaviour, if established
- Actual observed behaviour
- Reproduction frequency
- Supporting screenshot or evidence reference
- Related test case
- Classification: Expected Behaviour, Question, Potential Defect, or Confirmed Defect

Only classify an observation as a confirmed defect after validating the expected behaviour and reproducing the discrepancy.

## 10. Completion Criteria

An exploratory session is complete when:

- The defined charter has been explored.
- Relevant checklist items have execution notes.
- Important observations are documented.
- Reproducible potential defects have sufficient evidence.
- New test ideas are recorded.
- Limitations and remaining risks are documented.

Exploratory testing does not establish that the application is defect-free. Findings apply only to the tested environment and scope.

## 11. Revision History

| Version | Change | Status |
|---|---|---|
| 1.0 | Initial exploratory testing checklist | Planned |
