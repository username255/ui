---
"@ui-sdk/core": patch
---

`convertColor` and `formatColor` now wrap an HSL, HSV or HWB hue below 0 around the wheel, so `-90` is the color at `270`. It came out as a different color before. `parseColor` already wrapped it, so this only showed with a color built in code, like a hue turned by `hue - 90`.
