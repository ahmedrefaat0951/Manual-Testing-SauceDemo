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

## Checkout: Your Information

**Functional Test Cases**

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
