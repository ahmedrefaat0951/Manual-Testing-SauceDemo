# Checkout Test Suite

This test suite contains both **Functional** and **UI** test cases covering the complete SauceDemo checkout flow:

**Cart → Checkout: Your Information → Checkout: Overview → Checkout: Complete!**

---

## TC-023 — Verify Checkout Can Be Opened from Cart

**Preconditions:** User is logged in as `standard_user` and is on the Cart page with at least one product added to the cart.

### Steps

1. Click the **Checkout** button.
2. Observe the resulting page.

### Expected Result

The user is redirected to the **Checkout: Your Information** page.

### Actual Result

The user was redirected to the **Checkout: Your Information** page.

### Status

**PASS ✅**
