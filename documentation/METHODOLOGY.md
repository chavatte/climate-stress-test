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

## 3. Agents and Network Structure

The model contains a baseline of 100 synthetic municipal agents.

Each agent receives synthetic values for exposure, vulnerability, resilience, and sectoral sensitivities.

The principal sensitivities are:

- water;
- agriculture;
- urban systems;
- heat.

Dynamic variables include hazard, water stress, agricultural impact, energy stress, economic impact, cascade load, local risk, damage, recovery capacity, and status.

### Network Structural Metrics
Municipal agents are connected via an undirected dependency network (`dependencies`). While user input controls the target connection parameter (`network-density`), actual structural metrics are measured post-generation:

- `network-edge-count`: Total number of undirected links $E$.
- `network-mean-degree`: Average degree across $N$ agents ($2E / N$).
- `network-realized-density`: Observed graph density ($E / [N(N-1)/2]$).

## 4. Hazard formulation

The model combines four normalized pressure components:

- warming pressure;
- El Niño intensity;
- deforestation pressure;
- urban pressure.

The Version 2.4.0 formulation uses the following conceptual weights:

```text
Warming pressure       0.45
El Niño intensity      0.20
Deforestation pressure 0.20
Urban pressure         0.15
```

Seasonality is applied with an approximate ±10% amplitude, together with a small monthly temporal drift term (~1.2% annual rate, or 0.012/month) used as an experimental trend.

Version 2.4.0 deliberately reduces hazard saturation and moderates temporal amplification relative to earlier internal formulations.

## 5. Local risk

The raw local-risk construct is:

Plaintext

```
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
    

The cascade load has persistent memory: previous cascade load decays exponentially by 8% per month (`cascade-load * 0.92`) before new spillover is incorporated.

This mechanism allows the model to represent persistence and propagation rather than treating every tick as an independent event.

## 7. Damage and recovery

Damage combines local risk, economic impact, and cascade load.

Recovery depends on the combined capacity represented by resilience, infrastructure, and adaptation, operating at a gradual recovery rate coefficient of 0.020 per tick.

Version 2.4.0 uses gradual recovery to reduce artificial oscillations and make the recovery process less abrupt.

## 8. Scenario controls and comparison

### Fail-open

Adaptation and infrastructure efficiency are reduced to approximately 55%.

### Balanced

Nominal efficiency is used (100%).

### Resilient by design

Efficiency may reach up to approximately 130%.

### Automated Scenario Comparison

The `compare-scenarios` procedure executes all three scenarios sequentially under identical initial conditions (same seed `20260916`, same municipal count, and same network topology) over the 60-month horizon to provide direct comparative diagnostic outputs.

These scenarios are experimental parameterizations, not forecasts of real policy outcomes.

## 9. Reproducibility

`setup` uses:

Plaintext

```
random-seed 20260916
```

The same model version, parameters, and compatible NetLogo version should reproduce the same stochastic sequence.

For statistical analysis, `replication-test N` executes $N$ independent runs with sequential seeds, printing final systemic risk, peak systemic risk, average damage, cascade event counts, mean degree, and realized density.

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