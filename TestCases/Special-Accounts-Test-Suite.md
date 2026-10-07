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

## TC-046 — Verify Products Can Be Added to Cart

**Preconditions:** User is logged in as `problem_user` and is on the Products page.

### Test Data

* Products:

  * `Sauce Labs Backpack`
  * `Sauce Labs Bike Light`
  * `Sauce Labs Bolt T-Shirt`
  * `Sauce Labs Fleece Jacket`
  * `Sauce Labs Onesie`
  * `Test.allTheThings() T-Shirt (Red)`

### Steps

1. Click the **Add to cart** button for each product.
2. Observe the button and the Cart icon state after each attempt.

### Expected Result

Each selected product is added to the Cart.

### Actual Result

* `Sauce Labs Backpack`, `Sauce Labs Bike Light`, and `Sauce Labs Onesie` were added to the Cart successfully.
* `Sauce Labs Bolt T-Shirt`, `Sauce Labs Fleece Jacket`, and `Test.allTheThings() T-Shirt (Red)` were not added to the Cart.

### Status

**FAIL ❌**

## TC-047 — Verify Products Can Be Removed from Cart

**Preconditions:** User is logged in as `problem_user` and is on the Products page with the following products added to the Cart:

* `Sauce Labs Backpack`
* `Sauce Labs Bike Light`
* `Sauce Labs Onesie`

### Steps

1. Click the **Remove** button for each product.
2. Observe the button and the Cart icon state after each attempt.

### Expected Result

Each selected product is removed from the Cart, and the corresponding **Remove** button changes to **Add to cart**.

### Actual Result

The selected products were not removed from the Cart. The **Remove** buttons remained unchanged, and the Cart icon continued to display a count of **3**.

### Status

**FAIL ❌**
