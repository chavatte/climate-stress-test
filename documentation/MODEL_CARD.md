# Model Card

## Model identification

**Name:** Climate Stress Test — Brazil 2026–2030  
**Version:** 2.0  
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

## Output interpretation

The model's risk and damage values are internal model constructs. They should be interpreted comparatively within the experimental design, not as directly measurable real-world quantities.

## Reproducibility

Version 2.0 includes a fixed setup seed and a replication procedure. The fixed seed supports reproducibility of a particular trajectory; repeated runs with different seeds are required for statistical analysis.

## Known limitations

The model is synthetic and not empirically calibrated. Spatial, network, hazard, sensitivity, adaptation, and recovery mechanisms are simplified.

## Ethical and scientific note

The model is deliberately transparent about its abstraction level. The use of the word “Brazil” identifies the conceptual scenario and research context; it does not imply that the synthetic municipalities correspond to real Brazilian municipalities.

## Version 2.0 changes

Version 2.0 includes:

1. reproducible random-seed initialization;
2. reduced hazard saturation;
3. reduced seasonality amplitude;
4. reduced artificial temporal growth;
5. narrower synthetic initial distributions;
6. reduced monthly adaptation/infrastructure gains;
7. more gradual recovery;
8. cascade memory with decay;
9. slightly higher cascade thresholds;
10. peak systemic-risk and peak-damage tracking;
11. a `replication-test` procedure.
