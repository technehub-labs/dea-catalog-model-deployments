# CR-MDP-CAT-05: CR Naming/Numbering Correction (programme batch CRs)

**Status**: Landed (this PR)
**Layer**: Catalog governance (CR records)
**Owner**: Emmanuel A. Otchere
**Date**: 2026-11-15
**Trigger**: The catalog population programme's driver-generated CRs landed without the house `CR-` prefix in their file names, headers, and cross-references (driver-generated CRs missed the house CR- prefix; MDP-CAT mapping recorded in this CR). Landed CRs are immutable; corrections are recorded by later PRs (BC-01A renumbering precedent). This CR renames the affected records to their house-form identifiers and records the mapping.
**Carrier**: Single PR on feature branch `feat/cr-mdp-cat-05`. PR review, not direct push.
**Lands against**: `main`

## 1. What this CR does

Renames the programme CR records to house-form file names, fixes their headers and cross-references, and updates the CR index and CHANGELOG headings, per this mapping:

| Landed as | Corrected to |
|---|---|
| `MDP-CAT-02` | `CR-MDP-CAT-02` |
| `MDP-CAT-03` | `CR-MDP-CAT-03` |
| `MDP-CAT-04` | `CR-MDP-CAT-04` |

## 2. NOT-List

- No content changes to the renamed CRs (naming/numbering only).
- No re-landing or re-admission of records.
- Historical commit messages keep their original (unprefixed) form; the corrected file names are the canonical reference.

## 3. Acceptance criteria

1. All mapped records exist under their house-form names; no unprefixed duplicates remain.
2. CR index rows and CHANGELOG headings reference the corrected names.
