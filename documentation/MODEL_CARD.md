# Model Card

## Model identification

**Name:** Climate Stress Test — Brazil 2026–2030  
**Version:** 2.4.0  
**Model class:** Exploratory Agent-Based Model  
**Implementation:** NetLogo  
**Author:** João Carlos Chavatte

## Intended purpose

The model explores systemic vulnerability and cascading interactions among synthetic municipalities exposed to interacting environmental and socioeconomic stressors.

It is designed for research exploration, teaching, methodological experimentation, and reproducibility work.

## Out-of-scope uses

The model should not be used as:

- an official climate forecast;
- a municipal risk score;
- an infrastructure investment decision engine;
- a probability estimator for specific disasters;
- a calibrated socioeconomic forecast;
- a substitute for observed climate, hydrological, economic, or infrastructure data.

## Agents

Each municipality is represented as a synthetic agent with attributes including:

- exposure;
- vulnerability;
- resilience;
- water sensitivity;
- agricultural sensitivity;
- urban sensitivity;
- heat sensitivity.

Dynamic state variables include:

- hazard;
- water stress;
- agricultural impact;
- energy stress;
- economic impact;
- cascade load;
- local risk;
- damage;
- recovery capacity;
- status.

## Network representation

The `dependencies` relationship represents abstract inter-municipal dependencies.

It does **not** represent the actual Brazilian electricity grid, water network, supply chain, trade network, transportation network, or financial system.

Version 2.4.0 explicitly measures and reports realized network structural metrics post-generation:
- `network-edge-count`: Total graph edges ($E$).
- `network-mean-degree`: Average degree across agents ($2E / N$).
- `network-realized-density`: Realized graph density ($E / [N(N-1)/2]$).

## Output interpretation

The model's risk and damage values are internal model constructs. They should be interpreted comparatively within the experimental design, not as directly measurable real-world quantities.

## Reproducibility and Scenario Comparison

Version 2.4.0 includes a fixed setup seed (`20260916`), an automated multi-scenario comparison routine (`compare-scenarios`), and a stochastic replication procedure (`replication-test`). The fixed seed supports reproducibility of a particular trajectory; repeated runs with independent seeds are required for statistical analysis.

## Known limitations

The model is synthetic and not empirically calibrated. Spatial, network, hazard, sensitivity, adaptation, and recovery mechanisms are simplified.

## Ethical and scientific note

The model is deliberately transparent about its abstraction level. The use of the word “Brazil” identifies the conceptual scenario and research context; it does not imply that the synthetic municipalities correspond to real Brazilian municipalities.

## Version 2.4.0 changes

Version 2.4.0 includes:

1. reproducible random-seed initialization (`20260916`);
2. automated multi-scenario comparison procedure (`compare-scenarios`);
3. real-time calculation and reporting of realized network structural metrics (edge count, mean degree, realized density);
4. reduced hazard saturation and controlled temporal drift (~1.2%/year);
5. reduced seasonality amplitude (±10%);
6. narrower synthetic initial distributions;
7. reduced monthly adaptation/infrastructure gains;
8. more gradual recovery (rate 0.020/month);
9. cascade memory with exponential decay (8%/month);
10. higher cascade thresholds to reduce false positives;
11. peak systemic-risk and peak-damage tracking;
12. an automated multi-run replication procedure (`replication-test`).