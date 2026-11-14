# Change Requests: dea-catalog-model-deployments

This index tracks every change request that lands on this repository.

| CR | Title | Status | Notes |
|----|-------|--------|-------|
| [CR-MDP-CAT-01](CR-MDP-CAT-01-catalogue-foundation.md) | Catalogue foundation (kit bring-up) | Landed (this PR) | Standard kit: pointer, dependencies, schema projection, gates 1-6, workflows, FOUNDATIONS, record standard. No records admitted. |
| CR-MDP-CAT-02 | Initial population | Planned | Evidence-gated seed population per FOUNDATIONS §7. |

## Numbering

Series tag `CR-MDP-CAT-NN`, sequential. Cross-repo CRs that touch this
repository are recorded here with their home-repo identifier.
| [MDP-CAT-02](MDP-CAT-02-mdp-cat-02.md) | Entity Ingestion Groundwork (candidate intake queue + gates) | **Proposed (this PR)** | Gated intake: queue + blocking queue gate + admission tool (candidate-state subtrees, content-derived ids); pin v2.6.0→v2.8.0 + shard-aware toolchain re-vendor. No records. |
| [MDP-CAT-03](MDP-CAT-03-mdp-cat-03.md) | ModelDeployment Candidate Corpus | **Landed (this PR)** | 1000 queue submissions from 1 bank(s); manifest with sha256s; queue gate CONFORMANT; no entities change. |
| [MDP-CAT-04](MDP-CAT-04-mdp-cat-04.md) | ModelDeployment Candidate Admission Batch 01 (0bserverx/Qwen3.8-27B-Heretic-Abliterated-Uncensored-GGUF … ZhengPeng7/BiRefNet) | **Landed (this PR)** | Admitted 1000 `ModelDeployment` CANDIDATE records via the gated intake workflow (queue gate → admission tool → catalog gates); candidates +1000, canonical unchanged; records at `lifecycle_status: proposed` in `candidates/` subtrees. |
