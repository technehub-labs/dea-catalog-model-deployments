# CR-CR-MDP-CAT-03: ModelDeployment Candidate Corpus

**Status**: Landed (this PR)

**Naming/numbering correction**: this CR landed as `MDP-CAT-03` without the house `CR-` prefix (driver defect, fixed in the programme tooling). Renamed to `CR-MDP-CAT-03` by the naming-correction CR (CR-MDP-CAT-05); content unchanged.
**Layer**: Catalog content (candidate corpus intake)
**Owner**: Emmanuel A. Otchere
**Date**: 2026-11-15
**Admission authority**: candidate corpus only (canonical admission remains the evidence-gated step; FOUNDATIONS D-4/D-5)
**Trigger**: Catalog population programme (2026-11 owner directive): advance 10 foundational skeleton catalogs with evidence-backed candidate corpora (>=1,000 each) through a gated intake workflow. Model-deployments is fifth: the Hugging Face public model registry (top-1,000 by downloads) is the candidate seed source named per FOUNDATIONS §7; deployment_kind/environment values are provisional programmatic mappings documented per record.
**Carrier**: Single PR on feature branch `feat/mdp-cat-03`. PR review, not direct push.
**Lands against**: `main`
**Depends on**: MDP-CAT-02 (ingestion groundwork).

## 1. What this CR lands

**1000 ModelDeployment candidate submissions** in `contributions/queue/<shard>/<slug>.yaml` from 1 evidence bank(s):

| Bank | Source | Records |
|---|---|---|
| hf-deployments.json | Hugging Face public model registry (api/models by downloads) | 1000 |

Provenance in `ingestion/manifest.yaml` (bank sha256s, source URLs, retrieval dates, mapping note). Every submission carries `source_ref`, a `published-document` evidence citation, and published description prose. Provisional field mappings are documented per record and in the manifest; per-organization values are canonical-admission decisions.

> Provenance note: records reference published Hugging Face model cards; deployment_kind=api-endpoint and environment=production are provisional programmatic values (the hub publicly serves these artifacts) subject to canonical-admission review.

## 2. What changes

- `contributions/queue/<shard>/` — 1000 intake submissions (`status: queued`)
- `ingestion/manifest.yaml` — corpus provenance record (new)
- No `CATALOG.yaml` change (queue ≠ index)
- This CR file and the index row

## 3. Verification

- `check_contributions.py`: CONFORMANT (1000 queue files)
- No directory holds 800+ entries (slug-prefix distribution)
- Spot-checks: records trace to their published source identifiers

## 4. NOT-List

- NOT record admission (nothing under `entities/` changes; admission follows in MDP-CAT-04+).
- NOT a modification of gates, schemas, or intake tooling.
- NOT an authoritative assessment of provisional mapped values.

## 5. Acceptance criteria

1. 1000 gate-CONFORMANT submissions; manifest carries bank sha256s + source URLs.
2. Submissions carry no `id`; `status: queued`; `submitted_by: Emmanuel A. Otchere`.
3. `CATALOG.yaml` counts unchanged.
