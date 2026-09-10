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
