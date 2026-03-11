# Analysis File Format

Structure every saved analysis file exactly as follows:

```
# [Role Title] at [Company]
[Date] | Resume: [filename used]

## Fit Score: [LOW / MEDIUM / HIGH]
[Two to three sentence explanation of what drove the score.]

## Personal Fit
[One sentence. Either "No conflicts with stated preferences." or a plain summary of any conflicts flagged — e.g., "Role requires in-person attendance in [location]. Salary range not disclosed."]

---

## Qualifications

| Qualification | Status | Evidence or Gap |
|---|---|---|
| ... | `Strong` | ... |
| ... | `Partial` | ... |
| ... | `Gap` | ... |

---

## Strategic Notes

[Note 1]

[Note 2]

[Note 3]

---

## Suggested Resume Updates

[Only present if the post-analysis check-in surfaces undocumented experience. For each update, name the resume entry it belongs to and provide a ready-to-use draft bullet in the style of the existing resume. Omit this section entirely if no updates are needed.]

```

Wrap each status value in backticks so it renders as inline code: `Strong`, `Partial`, `Gap`.
