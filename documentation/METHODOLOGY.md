# Methodology

## 1. Conceptual design

Climate Stress Test — Brazil 2026–2030 is an exploratory Agent-Based Model in which synthetic municipalities interact through an abstract dependency network.

The central modeling idea is that systemic stress may emerge from the interaction of:

1. external hazard pressure;
2. heterogeneous exposure;
3. heterogeneous vulnerability;
4. local resilience;
5. sector-specific sensitivities;
6. adaptation and infrastructure capacity;
7. network-mediated cascading effects;
8. damage accumulation and recovery.

The model does not claim that these mechanisms reproduce Brazil's real climate or infrastructure systems.

## 2. Temporal and spatial scales

One NetLogo tick represents one month.

The experimental horizon is 60 ticks, representing a five-year period from 2026 to 2030.

The spatial environment is a two-dimensional abstract grid containing five stylized regional bands. The spatial arrangement is a modeling device and should not be interpreted as geographic cartography.

## 3. Agents

The model contains a baseline of 100 synthetic municipal agents.

Each agent receives synthetic values for exposure, vulnerability, resilience, and sectoral sensitivities.

The principal sensitivities are:

- water;
- agriculture;
- urban systems;
- heat.

Dynamic variables include hazard, water stress, agricultural impact, energy stress, economic impact, cascade load, local risk, damage, recovery capacity, and status.

## 4. Hazard formulation

The model combines four normalized pressure components:

- warming pressure;
- El Niño intensity;
- deforestation pressure;
- urban pressure.

The Version 2 formulation uses the following conceptual weights:

```text
Warming pressure       0.45
El Niño intensity      0.20
Deforestation pressure 0.20
Urban pressure         0.15
```

Seasonality is applied with an approximate ±10% amplitude, together with a small imposed temporal growth term used as an experimental trend.

Version 2.0 deliberately reduces hazard saturation and moderates temporal amplification relative to the earlier internal formulation.

## 5. Local risk

The raw local-risk construct is:

```text
RawRisk = Hazard × Exposure × Vulnerability / 10000
```

Net local risk is then reduced by resilience, effective infrastructure, and effective adaptation.

These terms are normalized model constructs and are not direct estimates of observed risk.

## 6. Cascading mechanism

Municipalities are connected through `dependencies`.

Cascade pressure is influenced by:

- average neighboring risk;
- network density;
- cascade sensitivity.

The cascade load has memory: previous cascade load contributes to current load and then decays over time.

This mechanism allows the model to represent persistence and propagation rather than treating every tick as an independent event.

## 7. Damage and recovery

Damage combines local risk, economic impact, and cascade load.

Recovery depends on the combined capacity represented by resilience, infrastructure, and adaptation.

Version 2.0 uses more gradual recovery to reduce artificial oscillations and make the recovery process less abrupt.

## 8. Scenario controls

### Fail-open

Adaptation and infrastructure efficiency are reduced to approximately 55%.

### Balanced

Nominal efficiency is used.

### Resilient

Efficiency may reach up to approximately 130%.

These scenarios are experimental parameterizations, not forecasts of real policy outcomes.

## 9. Reproducibility

`setup` uses:

```text
random-seed 20260916
```

The same model version, parameters, and compatible NetLogo version should reproduce the same stochastic sequence.

For statistical analysis, `replication-test N` uses multiple seeds.

## 10. Recommended experimental protocol

For a formal experiment:

1. document the exact NetLogo version;
2. record the model version;
3. record all parameter values;
4. run at least 30 independent replications per scenario;
5. preserve the random seeds;
6. export raw outputs;
7. calculate mean, median, standard deviation, minimum, maximum, and uncertainty intervals;
8. compare scenarios using pre-specified metrics;
9. inspect distributions rather than relying only on averages;
10. report limitations and sensitivity analyses.

## 11. Interpretation

The model is most appropriately interpreted as a computational laboratory.

A change in output means that the modeled assumptions produced a different trajectory under the specified experimental conditions. It does not, by itself, establish that the corresponding real-world relationship has the same magnitude or direction.

## 12. ODD-oriented documentation

The model documentation follows the spirit of the Overview, Design concepts, and Details (ODD) framework:

- purpose and patterns;
- entities, state variables, and scales;
- process overview;
- scheduling;
- initialization;
- submodels;
- design concepts;
- input data and parameterization;
- experimental analysis.

The current implementation is an exploratory artifact rather than a fully empirically validated ODD model.
