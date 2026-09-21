# Replication Protocol

## Objective

This protocol defines a reproducible procedure for evaluating the stochastic behavior of Climate Stress Test — Brazil 2026–2030.

## Software

- NetLogo: record the exact compatible version used for each release (designed for NetLogo 7.x).
- Model release: Version 2.4.0.
- Operating system: record for each experiment when relevant.

## Baseline

Use the baseline parameter set documented in `README.md` and `METHODOLOGY.md`.

## Single-run reproducibility test

1. Open the Version 2.4.0 `.nlogox` model (`model/climate_stress_test_brazil_2026_2030.nlogox`).
2. Confirm the baseline parameters.
3. Run `setup`.
4. Verify the seed initialization (`random-seed 20260916`).
5. Run `run-to-2030`.
6. Execute `print-summary`.
7. Record final systemic risk, peak systemic risk, final average damage, total cascade load, and realized network structural metrics.
8. Repeat with the same model version and seed to verify deterministic reproducibility of the stochastic sequence.

## Automated Scenario Comparison

To execute a controlled comparison across all three built-in scenarios (`FAIL OPEN`, `BALANCED`, and `RESILIENT BY DESIGN`) under identical initial conditions (same seed `20260916` and network topology):

1. Open the model and set desired sliders.
2. Run `compare-scenarios`.
3. Review the comparative table printed in the Command Center output.

## Multi-run experiment

For exploratory statistical evaluation, run repeated replications across independent seeds using the automated procedure:

```text
replication-test 3
```

This procedure executes 30 independent 60-month runs (incrementing the seed sequentially: `20260916 + run-id`) and reports:

- replication number / run ID;
    
- seed;
    
- final systemic risk (`SYSTEM_RISK`);
    
- peak systemic risk (`PEAK_RISK`);
    
- final average damage (`DAMAGE`);
    
- total cascade events (`CASCADE_EVENTS`);
    
- network mean degree (`NETWORK_MEAN_DEGREE`);
    
- network realized density (`NETWORK_DENSITY`).
    

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

Plaintext

```
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