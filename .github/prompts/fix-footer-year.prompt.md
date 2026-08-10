---
description: Fix the footer year bug across all pages. Use when the year doesn't render in the footer.
---

Fix the footer year issue in {{pages}}: the HTML uses `<span id="yr">` but the script queries
`getElementById('year')`. Make the IDs match so the current year renders.