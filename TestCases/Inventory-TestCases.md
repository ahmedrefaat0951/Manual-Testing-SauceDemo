# Inventory Test Cases

## TC-008 — Verify Products Can Be Sorted by Name (A–Z)

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Open the sorting dropdown.
2. Select **Name (A to Z)**.
3. Observe the order of the products.

### Expected Result

The products are displayed in alphabetical order from A to Z based on their product names.

### Actual Result

The products are displayed in alphabetical order from A to Z based on their product names.

### Status

**PASS ✅**

---

## TC-009 — Verify Products Can Be Sorted by Name (Z–A)

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Open the sorting dropdown.
2. Select **Name (Z to A)**.
3. Observe the order of the products.

### Expected Result

The products are displayed in alphabetical order from Z to A based on their product names.

### Actual Result

The products are displayed in alphabetical order from Z to A based on their product names.

### Status

**PASS ✅**

---

## TC-010 — Verify Products Can Be Sorted by Price (Low to High)

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Open the sorting dropdown.
2. Select **Price (low to high)**.
3. Observe the order of the products.

### Expected Result

The products are displayed in ascending order by price, from lowest to highest.

### Actual Result

The products were displayed in ascending order by price, from lowest to highest. The two products priced at **$15.99** are positioned next to each other.

### Status

**PASS ✅**

---

## TC-011 — Verify Products Can Be Sorted by Price (High to Low)

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Open the sorting dropdown.
2. Select **Price (high to low)**.
3. Observe the order of the products.

### Expected Result

The products are displayed in descending order by price, from highest to lowest.

### Actual Result

The products were displayed in descending order by price, from highest to lowest.

### Status

**PASS ✅**

---

## TC-012 — Verify Add to Cart Functionality

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

**Test Data:** Any available product on the Products page.

### Steps

1. Locate a product.
2. Click the **Add to cart** button.
3. Observe the product card and cart icon.

### Expected Result

* The **Add to cart** button changes to **Remove**.
* The cart icon displays a badge showing **1**.
* The selected product is added to the cart.

### Actual Result

* The **Add to cart** button changed to **Remove**.
* The cart icon displayed a badge showing **1**.
* The selected product was added to the cart.

### Status

**PASS ✅**

---

## Exploratory Testing

During exploratory testing of the Products page, the sorting dropdown was interacted with beyond the predefined sorting scenarios. Clicking the dropdown arrow was found to have no effect, while clicking the displayed sort option text opened the dropdown. This behavior was documented as `BUG-001`.
