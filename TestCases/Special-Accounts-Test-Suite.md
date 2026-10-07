# Special Accounts Test Suite

This test suite covers the predefined user accounts provided by SauceDemo that exhibit account-specific behavior.

The primary functional and UI test suites were executed using `standard_user` as the baseline account. This suite focuses on behaviors that are specific to, or meaningfully affected by, the respective user accounts and avoids duplicating the baseline test coverage.

# Account: `locked_out_user` — Test Cases

## TC-044 — Verify Locked-Out User Cannot Log In

**Preconditions:** User is on the SauceDemo login page.

### Test Data

* Username: `locked_out_user`
* Password: `secret_sauce`

### Steps

1. Enter the username.
2. Enter the password.
3. Click the **Login** button.

### Expected Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Sorry, this user has been locked out.**

### Actual Result

The user was not logged in, and the following error message was displayed:

> **Epic sadface: Sorry, this user has been locked out.**

### Status

**PASS ✅**

# Account: `problem_user` — Test Cases

## TC-045 — Verify Product Sorting

**Preconditions:** User is logged in as `problem_user` and is on the Products page.

### Test Data

* Sorting options:

  * `Name (Z to A)`
  * `Price (low to high)`
  * `Price (high to low)`

### Steps

1. Open the **Sort** dropdown.
2. Select **Name (Z to A)**.
3. Verify the product order.
4. Repeat steps 1–3 for **Price (low to high)** and **Price (high to low)**.

### Expected Result

The products are reordered according to the selected sorting option.

### Actual Result

The selected sorting options did not change the product order. The products remained in **Name (A to Z)** order.

### Status

**FAIL ❌**
