# Login UI Test Cases

## TC-006 — Verify Required-Field Error Message Is Fully Visible and Readable

**Preconditions:** User is on the SauceDemo login page.

### Test Data

- Username: *(Leave empty)*
- Password: `secret_sauce`

### Steps

1. Leave the Username field empty.
2. Enter the password.
3. Click the **Login** button.

### Expected Result

The following error message is fully visible and readable:

> **Epic sadface: Username is required**

### Actual Result

The following error message is fully visible and readable:

> **Epic sadface: Username is required**

### Status

**PASS ✅**

---

## TC-007 — Verify Invalid Credentials Error Message Is Fully Visible and Readable

**Preconditions:** User is on the SauceDemo login page.

### Test Data

- Username: `bob`
- Password: `secret_sauce`

### Steps

1. Enter the username.
2. Enter the password.
3. Click the **Login** button.

### Expected Result

The following error message is fully visible and readable:

> **Epic sadface: Username and password do not match any user in this service**

### Actual Result

The following error message is displayed and readable, but parts of the text are clipped at the top and bottom:

> **Epic sadface: Username and password do not match any user in this service**

### Status

**FAIL ❌**
