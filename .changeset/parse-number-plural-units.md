---
"@ui-sdk/core": patch
---

`parseNumber` now reads a long unit name beside any whole number, like "5 літрів" in `uk-UA`. It only knew the plural forms for 1 and for a fraction, so a Number Input with `unitDisplay: "long"`, or with `currencyDisplay: "name"` and no decimals, refused an edit to its own formatted value in Ukrainian, Polish, Czech and other languages with more than two forms.
