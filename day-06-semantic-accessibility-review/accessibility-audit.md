# Accessibility & Semantic HTML Audit Log

## Audit Findings & Fixes

| Check | Finding | Fix / Next Action |
| :--- | :--- | :--- |
| **Semantic regions** | Generic `<div>` wrappers were used for the top banner and main body content. | Replaced generic wrappers with `<header>`, `<nav aria-label="Primary Navigation">`, `<main>`, `<section>`, and `<footer>`. |
| **Heading hierarchy** | An `<h3>` was previously used immediately under `<h1>` for visual sizing. | Changed section headings to `<h2>` so headings follow a strict `<h1>` → `<h2>` order without skipping levels. |
| **Image alt text** | Profile image had generic `alt="photo"` text. | Updated to descriptive alt text: `alt="Portrait of Swati Panda smiling in casual attire"`. |
| **Link purpose** | Footer used vague `"Click here"` link text. | Replaced with descriptive link text: `"Swati Panda's GitHub Profile"`. |
| **Form labels** | Input fields lacked explicit `for` and `id` associations, and radio buttons lacked a `<fieldset>`. | Added matching `for`/`id` attributes to every `<label>` and `<input>`, grouped radio buttons in a `<fieldset>` with `<legend>`, and noted `(Required)` in visible text. |
| **Keyboard focus** | Tested navigation and form controls using only `Tab`, `Shift+Tab`, and `Enter`. | Confirmed logical top-to-bottom tab order across all links, inputs, radio buttons, and the submit button with visible browser focus outlines. |
| **Table structure** | Skills table lacked a `<caption>` and column `scope` attributes. | Added a descriptive `<caption>` and `scope="col"` on all `<th>` elements. |
| **Narrow-screen usability** | Tested layout at 360px mobile viewport width. | Verified all text, tables, and form controls stack cleanly without horizontal overflow. |

---

## Reflection Questions

1. **Which accessibility issue did you find first?**
   Generic `<div>` tags were being used instead of semantic landmarks like `<main>` and `<nav>`, along with vague `"Click here"` link text.
2. **What changed when you tested the page without a mouse?**
   Using only `Tab` and `Shift+Tab` made it immediately obvious how critical visible focus rings and properly linked `<label for="...">` elements are—clicking or tabbing onto a label immediately focuses its input box.
3. **How did you decide what alt text to write?**
   For informative images like my profile portrait, I described the subject clearly and concisely; if an image is purely decorative, I use an empty `alt=""` so screen readers skip it.
4. **Which two checks will you repeat on every future project?**
   Checking strict heading hierarchy (`<h1>` to `<h2>` without skipping) and running a full `Tab`-only keyboard navigation test before pushing code.