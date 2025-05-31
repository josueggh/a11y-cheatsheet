# ARIA Roles & Attributes Cheatsheet

A quick-access reference to help developers build accessible web components using [WAI-ARIA](https://www.w3.org/WAI/ARIA/) roles and attributes.
This guide focuses on practical ARIA usage in real-world UI elements like buttons, modals, tabs, and more — especially useful when building custom components in frameworks like React, Vue, or Angular.

---

## 🔍 Why use this?

Many modern web components rely on custom markup (`<div>`, `<span>`) instead of native HTML elements. ARIA helps make these components **accessible** to screen readers and assistive technologies.

Use this cheatsheet to:

- Understand which ARIA roles apply to each UI component
- Know what attributes are required or recommended
- Follow best practices for accessibility

---

## 🧩 ARIA Roles & Attributes Table

| Component        | ARIA Role     | Common ARIA Attributes                                         | Notes                                                                 |
|------------------|---------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| Button           | `button`      | `aria-pressed`, `aria-disabled`, `aria-label`                 | Use `aria-pressed` for toggle buttons                                |
| Progress Bar     | `progressbar` | `aria-valuemin`, `aria-valuemax`, `aria-valuenow`, `aria-label` | Provide current value and optional label                             |
| Modal / Dialog   | `dialog`      | `aria-modal`, `aria-labelledby`, `aria-describedby`           | Must trap focus inside the modal                                     |
| Tooltip          | `tooltip`     | `aria-describedby`, `aria-hidden`                             | Typically appears on hover/focus                                     |
| Accordion        | `region`      | `aria-expanded`, `aria-controls`, `aria-labelledby`           | Control visibility with `aria-expanded`                              |
| Tab List         | `tablist`     | -                                                              | Container for tabs                                                   |
| Tab              | `tab`         | `aria-selected`, `aria-controls`, `aria-labelledby`           | Use with `tablist` and `tabpanel`                                    |
| Tab Panel        | `tabpanel`    | `aria-labelledby`                                             | Associated with a `tab`                                              |
| Checkbox         | `checkbox`    | `aria-checked`, `aria-disabled`, `aria-label`                 | Use `aria-checked="mixed"` for tri-state checkboxes                  |
| Combobox         | `combobox`    | `aria-expanded`, `aria-controls`, `aria-activedescendant`     | Used for autocomplete/dropdowns                                      |
| Listbox          | `listbox`     | `aria-activedescendant`, `aria-disabled`                      | Often paired with `option` roles                                     |
| Option           | `option`      | `aria-selected`                                               | Inside listbox or combobox                                           |
| Switch           | `switch`      | `aria-checked`, `aria-label`                                  | Similar to checkbox but semantic for on/off                          |
| Navigation       | `navigation`  | `aria-label`                                                  | Use `aria-label` if there are multiple nav regions                   |
| Menu             | `menu`        | `aria-orientation`, `aria-labelledby`                        | Used in application menus                                            |
| Menu Item        | `menuitem`    | `aria-disabled`, `aria-haspopup`                             | Child of `menu`                                                      |

> 💡 **Tip:** Always prefer native semantic HTML elements (`<button>`, `<input>`, `<progress>`, etc.) when possible. Use ARIA only when semantic elements aren’t viable.

## 🛠️ Contributing

Have a suggestion or want to add a component to the table? Feel free to open a PR or issue!

---

## 📄 [License](LICENSE)
