# Day 05 — HTML Forms & Inputs Learning Log

## What I Built
I created an accessible **Student Registration Demo** form (`index.html`) inside `day-05-html-forms-inputs` using semantic HTML (`header`, `main`, `footer`, `form`, `fieldset`, `legend`) and properly labelled form controls (`text`, `email`, `number`, `select`, `radio`, `textarea`, and `checkbox`). All fields use fictional practice data only.

## Two Validation Checks Tested
1. **Email Format Check:** Entered `rohan.example.com` without an `@` symbol and clicked Submit; the browser blocked submission and displayed an invalid email prompt.
2. **Numeric Boundary Check (`min` / `max`):** Tested `14` (below `min="16"`) and `105` (above `max="99"`) in the Age field; the browser prevented submission and showed the allowed range.

## One Bug Fixed
While testing label associations, I temporarily changed the Full Name label from `for="full-name"` to `for="fullname"`. Clicking the label no longer focused the input box. Changing it back to `for="full-name"` restored click-to-focus functionality and proper accessibility linking.

## Why Client-Side Validation Is Not Enough
Browser-side HTML validation catches user mistakes early, but it can be bypassed easily by modifying HTML attributes in browser DevTools, disabling validation, or sending requests directly to a server. A real backend must always re-validate and sanitize all submitted data before saving or processing it.

## One Improvement for Later
Style the form with CSS to improve spacing, add clear focus outlines for keyboard users, and display custom inline error messages on mobile screens.