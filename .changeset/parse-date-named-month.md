---
"@ui-sdk/core": patch
---

`parseDate` now reads the day and the year beside a month name in the order the locale writes them there, which isn't always its numeric order. In `en-CA`, "Oct 16, 2026" gave `undefined` and "Oct 16, 26" gave 2016-10-26, so a Date Picker marked the first invalid and took the wrong date for the second. The same went for `sv-SE`, `en-ZA` and `af`.
