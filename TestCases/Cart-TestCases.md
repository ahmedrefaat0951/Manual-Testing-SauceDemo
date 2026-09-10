# Cart Test Cases

## TC-017 — Verify Cart Can Be Opened and Added Products Are Preserved

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

**Test Data:** Any available product on the Products page.

### Steps

1. Add a product to the cart.
2. Click the shopping cart icon.
3. Observe the Cart page.

### Expected Result

* The Cart page is displayed.
* The added product is displayed in the Cart.
* The cart badge count corresponds to the number of products added.

### Actual Result

* The Cart page was displayed.
* The added product was displayed in the Cart.
* The cart badge count corresponded to the number of products added.

### Status

**PASS ✅**

---

## TC-018 — Verify Product Can Be Removed from Cart

**Preconditions:** User is logged in as `standard_user` and is on the Cart page with one product added to the cart.

### Steps

1. Locate the product in the Cart.
2. Click the **Remove** button.
3. Observe the Cart page and cart icon.

### Expected Result

* The selected product is removed from the Cart.
* The cart badge number is no longer displayed on the cart icon.

### Actual Result

* The selected product was removed from the Cart.
* The cart badge number was no longer displayed on the cart icon.

### Status

**PASS ✅**

---

## TC-019 — Verify Multiple Products Are Displayed Correctly in Cart

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Add two different products to the cart.
2. Click the shopping cart icon.
3. Observe the Cart page and cart badge.

### Expected Result

* Both added products are displayed in the Cart.
* The cart badge displays **2**.

### Actual Result

* Both added products were displayed in the Cart.
* The cart badge displayed **2**.

### Status

**PASS ✅**

---

## TC-020 — Verify Continue Shopping Returns to Products Page

**Preconditions:** User is logged in as `standard_user` and is on the Cart page with one product added to the cart.

### Steps

1. Click the **Continue Shopping** button.
2. Observe the page and cart icon.

### Expected Result

* The Products page is displayed.
* The previously added product remains in the cart.
* The cart badge displays **1**.

### Actual Result

* The Products page was displayed.
* The previously added product remained in the cart.
* The cart badge displayed **1**.

### Status

**PASS ✅**

---

## TC-021 — Verify Cart Page Layout Is Displayed Correctly

**Preconditions:** User is logged in as `standard_user` and is on the Cart page with at least three products added to the cart.

### Steps

1. Observe the overall layout of the Cart page.
2. Observe the placement and alignment of the cart contents.
3. Observe the placement and alignment of the **Continue Shopping** and **Checkout** buttons.

### Expected Result

* The Cart contents are displayed within the main content area.
* The **Continue Shopping** button is displayed on the left side below the cart contents.
* The **Checkout** button is displayed on the right side below the cart contents.
* The page elements are properly aligned and displayed consistently without visual defects.

### Actual Result

* The Cart contents were displayed within the main content area.
* The **Continue Shopping** button was displayed on the left side below the cart contents.
* The **Checkout** button was displayed on the right side below the cart contents.
* The page elements were properly aligned and displayed consistently without any visible visual defects.

### Status

**PASS ✅**

