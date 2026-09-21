# Checkout Test Suite

This test suite contains both **Functional** and **UI** test cases covering the complete SauceDemo checkout flow:

**Cart → Checkout: Your Information → Checkout: Overview → Checkout: Complete!**

---

## TC-023 — Verify Checkout Can Be Opened from Cart

**Preconditions:** User is logged in as `standard_user` and is on the Cart page with at least one product added to the cart.

### Steps

1. Click the **Checkout** button.
2. Observe the resulting page.

### Expected Result

The user is redirected to the **Checkout: Your Information** page.

### Actual Result

The user was redirected to the **Checkout: Your Information** page.

### Status

**PASS ✅**

---

## Checkout: Your Information — Functional Test Cases

## TC-024 — Verify User Can Proceed with Valid Customer Information

**Preconditions:** User is logged in as `standard_user`, has at least one product added to the Cart, and is on the **Checkout: Your Information** page.

**Test Data:**

* First Name: `Ahmed`
* Last Name: `Refaat`
* ZIP/Postal Code: `12345`

### Steps

1. Enter a valid first name in the **First Name** field.
2. Enter a valid last name in the **Last Name** field.
3. Enter a valid ZIP/Postal Code in the **ZIP/Postal Code** field.
4. Click the **Continue** button.
5. Observe the resulting page.

### Expected Result

The user is redirected to the **Checkout: Overview** page without displaying a validation error.

### Actual Result

The user was redirected to the **Checkout: Overview** page without displaying a validation error.

### Status

**PASS ✅**

## TC-025 — Verify User Cannot Proceed with an Empty First Name

**Preconditions:** User is logged in as `standard_user`, has at least one product added to the Cart, and is on the **Checkout: Your Information** page.

**Test Data:**

* First Name: *(Leave empty)*
* Last Name: `Refaat`
* ZIP/Postal Code: `12345`

### Steps

1. Leave the **First Name** field empty.
2. Enter a valid last name in the **Last Name** field.
3. Enter a valid ZIP/Postal Code in the **ZIP/Postal Code** field.
4. Click the **Continue** button.
5. Observe the resulting page.

### Expected Result

The user should remain on the **Checkout: Your Information** page, and an error message indicating that the **First Name** field is required should be displayed.

### Actual Result

The user remained on the **Checkout: Your Information** page, and the error message `Error: First Name is required` was displayed.

### Status

**PASS ✅**

## TC-026 — Verify User Cannot Proceed with an Empty Last Name

**Preconditions:** User is logged in as `standard_user`, has at least one product added to the Cart, and is on the **Checkout: Your Information** page.

**Test Data:**

* First Name: `Ahmed`
* Last Name: *(Leave empty)*
* ZIP/Postal Code: `12345`

### Steps

1. Enter a valid first name in the **First Name** field.
2. Leave the **Last Name** field empty.
3. Enter a valid ZIP/Postal Code in the **ZIP/Postal Code** field.
4. Click the **Continue** button.
5. Observe the resulting page.

### Expected Result

The user should remain on the **Checkout: Your Information** page, and an error message indicating that the **Last Name** field is required should be displayed.

### Actual Result

The user remained on the **Checkout: Your Information** page, and the error message `Error: Last Name is required` was displayed.

### Status

**PASS ✅**

## TC-027 — Verify User Cannot Proceed with an Empty ZIP/Postal Code

**Preconditions:** User is logged in as `standard_user`, has at least one product added to the Cart, and is on the **Checkout: Your Information** page.

**Test Data:**

* First Name: `Ahmed`
* Last Name: `Refaat`
* ZIP/Postal Code: *(Leave empty)*

### Steps

1. Enter a valid first name in the **First Name** field.
2. Enter a valid last name in the **Last Name** field.
3. Leave the **ZIP/Postal Code** field empty.
4. Click the **Continue** button.
5. Observe the resulting page.

### Expected Result

The user should remain on the **Checkout: Your Information** page, and an error message indicating that the **ZIP/Postal Code** field is required should be displayed.

### Actual Result

The user remained on the **Checkout: Your Information** page, and the error message `Error: Postal Code is required` was displayed.

### Status

**PASS ✅**

---

## Checkout: Your Information — UI Test cases

## TC-028 — Verify Checkout: Your Information Page Layout Is Displayed Correctly

**Preconditions:** User is logged in as `standard_user`, has at least one product added to the Cart, and is on the **Checkout: Your Information** page.

### Steps

1. Observe the overall layout of the **Checkout: Your Information** page.
2. Observe the alignment, spacing, and positioning of the form elements.
3. Verify all buttons and labels are displayed correctly.

### Expected Result

* The page title is clearly visible.
* The form elements are properly aligned and consistently spaced.
* The **First Name**, **Last Name**, and **ZIP/Postal Code** fields are clearly visible with their corresponding labels.
* The **Continue** and **Cancel** buttons are clearly visible and properly positioned.

### Actual Result

* The page title was clearly visible.
* The form elements were properly aligned and consistently spaced.
* The **First Name**, **Last Name**, and **ZIP/Postal Code** fields were clearly visible with their corresponding labels.
* The **Continue** and **Cancel** buttons were clearly visible and properly positioned.

### Status

**PASS ✅**

## TC-029 — Verify Checkout: Your Information Validation Feedback Is Displayed Correctly

**Preconditions:** User is logged in as `standard_user`, has at least one product added to the Cart, and is on the **Checkout: Your Information** page.

**Test Data:**

* First Name: *(Leave empty)*
* Last Name: `Refaat`
* ZIP/Postal Code: `12345`

### Steps

1. Leave the **First Name** field empty.
2. Enter `Refaat` in the **Last Name** field.
3. Enter `12345` in the **ZIP/Postal Code** field.
4. Click the **Continue** button.
5. Observe the displayed error message and the visual validation indicators on all three fields.

### Expected Result

* An error message indicating that the **First Name** field is required is displayed.
* The **First Name** field is visually identified as invalid.
* The **Last Name** and **ZIP/Postal Code** fields, which contain valid values, are not visually identified as invalid.

### Actual Result

* The error message `Error: First Name is required` was displayed.
* The **First Name**, **Last Name**, and **ZIP/Postal Code** fields were all visually marked as invalid, even though only the **First Name** field was empty and identified by the error message.

### Status

**FAIL ❌**

---

## Checkout: Your Information — Exploratory Testing

### Exploratory Finding — Checkout Fields Accept Non-Standard Input

During exploratory testing, non-standard values were entered into the checkout customer-information fields.

The following inputs were accepted and allowed the user to proceed to the **Checkout: Overview** page:

| First Name | Last Name | ZIP/Postal Code | Result |
|---|---|---|---|
| `1` | `Refaat` | `12345` | Accepted |
| `Ahmed` | `1` | `12345` | Accepted |
| `Ahmed` | `Refaat` | `a` | Accepted |
| `@` | `@` | `@` | Accepted |

**Observation:**

The application accepted these non-standard values without displaying a validation error.

**Status:** Investigation required

---

## Checkout: Overview — Functional Test Cases

## TC-030 — Verify Cart Products Are Preserved in Checkout: Overview

**Preconditions:** User is logged in as `standard_user`, has at least two products added to the Cart, and is on the Cart page.

### Steps

1. Observe the products displayed in the Cart before proceeding.
2. Click the **Checkout** button.
3. Enter valid customer information on the **Checkout: Your Information** page.
4. Click the **Continue** button.
5. Observe the products displayed on the **Checkout: Overview** page.
6. Compare the products displayed in the Cart with those displayed on the **Checkout: Overview** page.

### Expected Result

* All products added to the Cart are displayed on the **Checkout: Overview** page.
* No product is missing or unexpectedly added during the transition from the Cart to the **Checkout: Overview** page.

### Actual Result

* All products added to the Cart were displayed on the **Checkout: Overview** page.
* No product was missing or unexpectedly added during the transition.

### Status

**PASS ✅**

## TC-031 — Verify Checkout: Overview Price Total Calculation

**Preconditions:** User is logged in as `standard_user`, has the specified product added to the Cart, and is on the **Checkout: Overview** page.

**Test Data:**

* Product: **Sauce Labs Bike Light**
* Item Price: `$9.99`

### Steps

1. Observe the **Item total**, **Tax**, and **Total** values in the **Price Total** section.
2. Calculate the expected Total using the displayed Item total and Tax values.
3. Compare the calculated amount with the displayed **Total**.

### Expected Result

The displayed **Total** should equal the sum of the **Item total** and **Tax** values.

### Actual Result

The **Item total** was `$9.99` and the **Tax** was `$0.80`.

The calculated total was `$10.79`, which matched the displayed **Total** of `$10.79`.

### Status

**PASS ✅**

## TC-032 — Verify Checkout: Overview Tax Calculation Consistency

**Preconditions:** User is logged in as `standard_user`, has the specified product added to the Cart, and is on the **Checkout: Overview** page.

**Test Data:**

| Product                   | Item Price |
| ------------------------- | ---------: |
| **Sauce Labs Bike Light** |    `$9.99` |
| **Sauce Labs Backpack**   |   `$29.99` |
| **Sauce Labs Onesie**     |    `$7.99` |

### Steps

1. Observe the **Item total** and **Tax** values in the **Price Total** section for the **Sauce Labs Bike Light**.
2. Calculate the tax percentage based on the displayed **Item total** and **Tax** values.
3. Repeat steps 1 and 2 for the **Sauce Labs Backpack** and **Sauce Labs Onesie**.
4. Compare the calculated tax percentages for all three products.

### Expected Result

The application should apply a consistent tax percentage to the item total across products with different prices.

### Actual Result

* **Sauce Labs Bike Light:** Item total was `$9.99`, and Tax was `$0.80`, corresponding to approximately **8%**.
* **Sauce Labs Backpack:** Item total was `$29.99`, and Tax was `$2.40`, corresponding to approximately **8%**.
* **Sauce Labs Onesie:** Item total was `$7.99`, and Tax was `$0.64`, corresponding to approximately **8%**.

The calculated tax percentage was consistent across all three products.

### Status

**PASS ✅**

## TC-033 — Verify Checkout: Overview Price Calculation for Multiple Products

**Preconditions:** User is logged in as `standard_user`, has the specified products added to the Cart, and is on the **Checkout: Overview** page.

**Test Data:**

| Product                 | Item Price |
| ----------------------- | ---------: |
| **Sauce Labs Onesie**   |    `$7.99` |
| **Sauce Labs Backpack** |   `$29.99` |

### Steps

1. Observe the **Item total**, **Tax**, and **Total** values in the **Price Total** section.
2. Calculate the expected **Item total** using the prices of all products in the Cart.
3. Calculate the expected **Tax** using the observed 8% tax rate.
4. Calculate the expected **Total** using the calculated Item total and Tax.
5. Compare the calculated values with the displayed **Item total**, **Tax**, and **Total**.

### Expected Result

* The displayed **Item total** should equal the combined price of all products in the Cart.
* The displayed **Tax** should be consistent with the observed 8% tax rate.
* The displayed **Total** should equal the Item total plus Tax.

### Actual Result

* The combined product price was `$37.98`, which matched the displayed **Item total** of `$37.98`.
* The calculated tax was `$3.04`, which matched the displayed **Tax** of `$3.04`.
* The calculated total was `$41.02`, which matched the displayed **Total** of `$41.02`.

### Status

**PASS ✅**

## TC-034 — Verify Cancel Button Behavior on Checkout: Overview Page

**Preconditions:** User is logged in as `standard_user`, has at least one product added to the Cart, and is on the **Checkout: Overview** page.

### Steps

1. Observe the products currently displayed on the **Checkout: Overview** page.
2. Click the **Cancel** button.
3. Observe the resulting page.
4. Compare the Cart contents with those observed before clicking **Cancel**.

### Expected Result

* The user is redirected to the **Cart** page.
* The products previously added to the Cart remain unchanged.

### Actual Result

* The user was redirected to the **Products** page.
* The products previously added to the Cart remained unchanged.

### Status

**FAIL ❌**
