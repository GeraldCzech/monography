# Claims

Claims are the smallest reusable scientific knowledge units in BEBA.

## Structure

Claims are grouped by concept code.

```text
Claims/
  WG/        Warm Glow
  TR/        Trust
  BE/        Brand Equity
  EU/        Epistemic Uncertainty
  CO/        Commitment
```

Each claim file should contain YAML front matter plus a short explanation.

## Claim Status

- candidate: extracted from literature, not yet reviewed.
- active: currently used in BEBA working theory.
- canonical: accepted as stable for the current dissertation version.
- superseded: replaced but retained.

## Rule

One claim per file once a concept becomes central. Aggregated files may be used temporarily during migration.
