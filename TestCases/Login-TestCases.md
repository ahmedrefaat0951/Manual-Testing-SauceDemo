# Login Test Cases

## TC-001 — Verify Login with Valid Credentials

**Preconditions:** User is on the SauceDemo login page.

### Test Data

- Username: `standard_user`
- Password: `secret_sauce`

### Steps

1. Enter the username.
2. Enter the password.
3. Click the **Login** button.

### Expected Result

The user is successfully logged in and redirected to the Products page.

### Actual Result

The user is successfully logged in and redirected to the Products page.

### Status

**PASS ✅**

---

## TC-002 — Verify Login with Invalid Username

**Preconditions:** User is on the SauceDemo login page.

### Test Data

- Username: `bob`
- Password: `secret_sauce`

### Steps

1. Enter the username.
2. Enter the password.
3. Click the **Login** button.

### Expected Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Username and password do not match any user in this service**

### Actual Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Username and password do not match any user in this service**

### Status

**PASS ✅**

---

## TC-003 — Verify Login with Invalid Password

**Preconditions:** User is on the SauceDemo login page.

### Test Data

- Username: `standard_user`
- Password: `1234`

### Steps

1. Enter the username.
2. Enter the password.
3. Click the **Login** button.

### Expected Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Username and password do not match any user in this service**

### Actual Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Username and password do not match any user in this service**

### Status

**PASS ✅**

---

## TC-004 — Verify Login with Empty Username

**Preconditions:** User is on the SauceDemo login page.

### Test Data

- Username: *(Leave empty)*
- Password: `secret_sauce`

### Steps

1. Leave the Username field empty.
2. Enter the password.
3. Click the **Login** button.

### Expected Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Username is required**

### Actual Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Username is required**

### Status

**PASS ✅**

---

## TC-005 — Verify Login with Empty Password

**Preconditions:** User is on the SauceDemo login page.

### Test Data

- Username: `standard_user`
- Password: *(Leave empty)*

### Steps

1. Enter the username.
2. Leave the Password field empty.
3. Click the **Login** button.

### Expected Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Password is required**

### Actual Result

The user is not logged in, and the following error message is displayed:

> **Epic sadface: Password is required**

### Status

**PASS ✅**
