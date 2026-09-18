# Replication Protocol

## Objective

This protocol defines a reproducible procedure for evaluating the stochastic behavior of Climate Stress Test — Brazil 2026–2030.

## Software

- NetLogo: record the exact compatible version used for each release.
- Model release: Version 2.0.
- Operating system: record for each experiment when relevant.

## Baseline

Use the baseline parameter set documented in `README.md` and `METHODOLOGY.md`.

## Single-run reproducibility test

1. Open the Version 2.0 `.nlogo` model.
2. Confirm the baseline parameters.
3. Run `setup`.
4. Verify the seed initialization.
5. Run `run-to-2030`.
6. Execute `print-summary`.
7. Record final systemic risk, peak systemic risk, and final average damage.
8. Repeat with the same model version and seed to verify deterministic reproducibility of the stochastic sequence.

## Multi-run experiment

For each scenario:

- Fail-open
- Balanced
- Resilient

run at least 30 independent replications.

Each replication should use a distinct seed.

Record:

- scenario;
- replication number;
- seed;
- final systemic risk;
- peak systemic risk;
- final average damage;
- any additional metrics selected before the experiment.

## Recommended statistical summary

For each metric and scenario, report:

- N;
- mean;
- median;
- standard deviation;
- minimum;
- maximum;
- selected uncertainty interval.

If comparisons are performed statistically, the analysis method and assumptions must be stated explicitly.

## Reproducibility record

Every released experiment should preserve:

```text
model version
NetLogo version
scenario
parameter set
seed
replication number
execution date
output file
analysis script/version
```

## Important distinction

A fixed seed provides reproducibility of a particular stochastic trajectory. It does not provide statistical evidence.

A replication study is required to characterize stochastic variation.
