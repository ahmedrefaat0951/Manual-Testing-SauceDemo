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
