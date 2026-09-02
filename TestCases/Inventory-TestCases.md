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
