# Inventory UI Test Cases

## TC-014 — Verify Product Cards Are Displayed Correctly

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Observe all product cards displayed on the Products page.
2. Check the product image, name, description, price, and action button for each product.
3. Compare the layout and positioning of these elements across the product cards.

### Expected Result

All product cards should contain:

* A product image.
* A product name.
* A product description.
* A product price.
* An action button.

All elements should be properly aligned and displayed consistently without visual defects.

### Actual Result

All product cards contained:

* A product image.
* A product name.
* A product description.
* A product price.
* An action button.

All elements were properly aligned and displayed consistently without any visible visual defects.

### Status

**PASS ✅**

---

## TC-015 — Verify Header Elements Are Displayed Correctly

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Observe the header at the top of the Products page.
2. Check the **Swag Labs** logo, hamburger menu, and cart icon.
3. Add a product to the cart and observe the cart icon.
4. Compare the positioning and alignment of the header elements.

### Expected Result

The header should contain:

* The **Sauce Labs** logo.
* The hamburger menu icon.
* The shopping cart icon.

The header elements should be properly aligned and displayed consistently without visual defects.

When a product is added to the cart, the cart badge should be displayed correctly on the cart icon.

### Actual Result

The header contained:

* The **Sauce Labs** logo.
* The hamburger menu icon.
* The shopping cart icon.

The header elements were properly aligned and displayed consistently without any visible visual defects.

After adding a product to the cart, the cart badge was displayed correctly on the cart icon.

### Status

**PASS ✅**

---

## TC-016 — Verify Products Page Controls Are Displayed Correctly

**Preconditions:** User is logged in as `standard_user` and is on the Products page.

### Steps

1. Observe the area directly below the main header.
2. Check the **Products** page title.
3. Check the sorting dropdown and the currently selected sorting option.
4. Observe the position and alignment of the page title and sorting control.

### Expected Result

The Products page controls should contain:

* The **Products** page title.
* A sorting dropdown displaying the currently selected sorting option.
* A dropdown arrow indicating the sorting control.

The page title and sorting control should be properly aligned and displayed consistently without visual defects.

### Actual Result

The Products page controls contained:

* The **Products** page title.
* A sorting dropdown displaying the currently selected sorting option.
* A dropdown arrow indicating the sorting control.

The page title and sorting control were properly aligned and displayed consistently without any visible visual defects.

### Status

**PASS ✅**
