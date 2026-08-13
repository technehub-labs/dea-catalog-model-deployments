# dea-catalog-model-deployments

> DEA catalog for **Model Deployment** and **Model Feedback Signal** — OpenDEAM v0.3.0 (ADR-0003).

## Model Deployment (`MDP`)

- **Entity id:** `dea:entity-model-deployment`
- **Allocation:** L4 · L4-model-operations
- **Status:** proposed

A running instance of an AI/ML Model, hosted on an Application Component, with its own version, monitoring state, and health.

## Model Feedback Signal (`MFS`)

- **Entity id:** `dea:entity-model-feedback-signal`
- **Allocation:** L4 · L4-model-operations
- **Status:** proposed

Drift, performance-degradation, or outcome-quality feedback captured from Events, used to trigger retraining of an AI/ML Model.

## Relationships (from the OpenDEAM model)

- **MDP → AIM** — instance of (realization, 0..N:1)
- **MDP → APC** — hosted by (composition, 0..N:1)
- **MFS → EVT** — derived from (dependency, 0..N:0..N)
- **MFS → AIM** — triggers retraining of (dependency, 0..N:0..N)

## Allocation contract

This repo's `metamodel-pointer.yaml` is validated in CI against the pinned
OpenDEAM root model (`v0.3.0`) via the reusable
`validate-against-model.yml` workflow. Drift fails CI.

Content (entity instances) lands when the entity promotes from
`proposed` to `planned`/`scaffold` per the model lifecycle.

## License

Apache 2.0 — see [LICENSE](./LICENSE) and [NOTICE](./NOTICE).
