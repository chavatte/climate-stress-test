<pre style="font-size: 0.5rem;">

                              \\\\\\
                           \\\\\\\\\\\\
                          \\\\\\\\\\\\\\\
-------------,-|           |C>   // )\\\\|    .o88b. db   db  .d8b.  db    db  .d8b.  d888888b d888888b d88888b
           ,','|          /    || ,'/////|   d8P  Y8 88   88 d8' '8b 88    88 d8' '8b '~~88~~' '~~88~~' 88'  
---------,','  |         (,    ||   /////    8P      88ooo88 88ooo88 Y8    8P 88ooo88    88       88    88ooooo 
         ||    |          \\  ||||//''''|    8b      88~~~88 88~~~88 '8b  d8' 88~~~88    88       88    88~~~~~ 
         ||    |           |||||||     _|    Y8b  d8 88   88 88   88  '8bd8'  88   88    88       88    88.   
         ||    |______      ''''\____/ \      'Y88P' YP   YP YP   YP    YP    YP   YP    YP       YP    Y88888P
         ||    |     ,|         _/_____/ \
         ||  ,'    ,' |        /          |                 ___________________________________________
         ||,'    ,'   |       |         \  |              / \                                           \ 
_________|/    ,'     |      /           | |             |  |                                            | 
_____________,'      ,',_____|      |    | |              \ |      chavatte@duck.com                     | 
             |     ,','      |      |    | |                |                       chavatte.vercel.app  | 
             |   ,','    ____|_____/    /  |                |    ________________________________________|___
             | ,','  __/ |             /   |                |  /                                            /
_____________|','   ///_/-------------/   |                 \_/____________________________________________/ 
              |===========,'                                                                                  
			  

</pre>

# CLIMATE STRESS TEST

**Languages:** 🇺🇸 **English** · 🇧🇷 [Português](README.pt-BR.md) 

## Brazil 2026–2030

### Agent-Based Model for Exploratory Climate Risk Stress Testing

> **Version 2.4.0 — Reproducibility and Numerical Verification**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22836683.svg)](https://doi.org/10.5281/zenodo.22836683)  
[![NetLogo](https://img.shields.io/badge/NetLogo-7.x-4E9F3D.svg)](https://ccl.northwestern.edu/netlogo/)  
![Model](https://img.shields.io/badge/Model-Agent--Based%20Model-2563EB.svg)  
![Version](https://img.shields.io/badge/version-2.4.0-0f172a.svg)  
[![Research](https://img.shields.io/badge/Research-Exploratory-7C3AED.svg)](https://chavatte.vercel.app/projects/climate-stress-test)  
![Reproducibility](https://img.shields.io/badge/Reproducibility-Seed%20%2B%20Replications-059669.svg)

---

## DOI

**Zenodo DOI:** 10.5281/zenodo.22836683

---

## MODEL

**Platform:** NetLogo 7.x  
**Model Type:** Exploratory Agent-Based Model (ABM)  
**Domain:** Climate Risk · Systemic Risk · Complex Networks · Resilience  
**Version:** 2.4.0

---

## TYPE

**Agent-Based Model**

Climate Stress Test represents a synthetic system of municipalities as interacting agents exposed to multiple external stressors and connected through an abstract dependency network.

The model investigates how local vulnerability, resilience, adaptation capacity, infrastructure conditions, and network-mediated cascades can interact to generate systemic risk.

The model is explicitly designed as a **computational stress-testing framework**, not as an official climate or socioeconomic forecasting system.

---

## HORIZON

**2026–2030**

The simulation covers a five-year experimental horizon.

```text
1 tick   = 1 month
60 ticks = 5 years
```

The 2026–2030 period represents the experimental scenario horizon and should not be interpreted as a prediction of actual Brazilian conditions during those years.

## AGENTS

**Baseline:** 100 synthetic municipalities

Each municipality is represented as an autonomous agent with heterogeneous characteristics.

### Static attributes

- Exposure
    
- Vulnerability
    
- Resilience
    
- Water sensitivity
    
- Agricultural sensitivity
    
- Urban sensitivity
    
- Heat sensitivity
    
- Regional classification
    

### Dynamic variables

- Hazard
    
- Water stress
    
- Agricultural impact
    
- Energy stress
    
- Economic impact
    
- Cascade load
    
- Local risk
    
- Damage
    
- Recovery capacity
    
- System status
    

The municipalities are **synthetic entities** and do not correspond to specific real-world Brazilian municipalities.

## TIME STEP

**1 tick = 1 month**

The model advances through monthly simulation steps.

Each tick represents the interaction between environmental pressure, local vulnerability, protective capacity, sectoral impacts, network dependencies, cascading effects, damage accumulation, and recovery.

The conceptual process order is:

Plaintext

```
Configure Scenario
       ↓
Update Local Hazard
       ↓
Calculate Local Risk
       ↓
Update Sector Impacts
       ↓
Propagate Cascades
       ↓
Apply Adaptation
       ↓
Apply Recovery
       ↓
Calculate Aggregate Metrics
       ↓
Update Visual State
```

# Quick Start

## 1. Install NetLogo

Download and install **NetLogo 7.x** from the official NetLogo website.

The model was designed for the NetLogo 7.x environment.

## 2. Download the model

Clone this repository or download the repository as a ZIP archive.

Bash

```
git clone https://github.com/chavatte/climate-stress-test.git
cd climate-stress-test
```

Then open the model file located in `model/`:

Plaintext

```
model/[Version_2_4-EN]_Climate_stress_Test_(Brasil-2026-2030).nlogox
model/[Version_2_4-PT-BR]_Climate_stress_Test_(Brasil-2026-2030).nlogox
```

## 3. Open the model in NetLogo

Launch NetLogo and open the Climate Stress Test `.nlogox` model.

The main interface provides scenario controls, simulation controls, monitors, plots, and console outputs.

## 4. Run the baseline experiment

Start with the baseline parameters:

|**Variable**|**Value**|
|---|---|
|Municipalities|100|
|Warming pressure|60|
|El Niño intensity|55|
|Deforestation pressure|35|
|Urban pressure|55|
|Adaptation investment|35|
|Infrastructure resilience|45|
|Network density|6|
|Cascade sensitivity|40|

Then execute:

Plaintext

```
setup
```

followed by:

Plaintext

```
go
```

Each tick represents one simulated month.

To run the complete experimental horizon automatically, use:

Plaintext

```
run-to-2030
```

This advances the model through the 60-month experimental horizon.

## 5. Compare scenarios

The model provides three principal experimental configurations (`FAIL OPEN`, `BALANCED`, and `RESILIENT BY DESIGN`).

To compare all three scenarios automatically under identical initial conditions (same seed and network structure), click **COMPARE SCENARIOS** or run:

Plaintext

```
compare-scenarios
```

Alternatively, run individual scenarios manually:

Plaintext

```
setup
↓
scenario-balanced
↓
run-to-2030
↓
print-summary
```

> Scenario names describe model configurations. They do not represent forecasts of actual Brazilian policy or future conditions.

## 6. Reproduce the baseline run

Version 2.4.0 uses:

Plaintext

```
random-seed 20260916
```

The same:

- model version;
    
- NetLogo version;
    
- parameter configuration; and
    
- random seed
    

should reproduce the same stochastic sequence.

This makes an individual simulation trajectory reproducible.

## 7. Run multiple replications

For exploratory statistical analysis, use:

Plaintext

```
replication-test 30
```

The procedure executes 30 stochastic replications with independent seeds and reports:

Plaintext

```
Seed
Final Systemic Risk
Peak Systemic Risk
Final Average Damage
Total Cascade Events
Network Mean Degree
Network Realized Density
```

A fixed seed is useful for reproducibility, while multiple seeds are required to investigate stochastic variability.

## Minimal Workflow

The shortest path to running the model is:

Plaintext

```
1. Open the .nlogox file
2. Run setup
3. Select a scenario (or run compare-scenarios)
4. Run go or run-to-2030
5. Run print-summary
```

For reproducibility testing:

Plaintext

```
setup
run-to-2030
print-summary
```

For replication testing:

Plaintext

```
replication-test 30
```

## Interactive Browser Simulation

A browser-based version of the model is also available:

**Web Simulation:** [Climate Stress Test ![Português](https://flagcdn.com/24x18/br.png)](https://chavatte.vercel.app/html-projects/climate_stress_test/index.html)

**Web Simulation:** [Climate Stress Test ![English](https://flagcdn.com/24x18/us.png)](https://chavatte.vercel.app/html-projects/climate_stress_test/index-EN.html)

The browser version provides an accessible way to interact with the simulation without opening the NetLogo desktop application. For research-grade work, the released NetLogo model and its documented parameters should be treated as the primary research artifact.

# 1. Abstract

Climate Stress Test — Brazil 2026–2030 is an exploratory Agent-Based Model implemented in NetLogo to investigate systemic vulnerability and cascading interactions among synthetic municipalities exposed to interacting climate, environmental, infrastructural, socioeconomic, and network-related stressors.

The model combines heterogeneous municipal exposure, vulnerability, resilience, sectoral sensitivities, adaptation investment, infrastructure resilience, and abstract inter-municipal dependencies.

The objective is not to forecast the future state of Brazil. Instead, the model functions as a **computational laboratory for stress testing**: controlled scenarios can be used to examine how changes in resilience, adaptation, network structure, and cascade sensitivity influence simulated systemic risk and damage.

Version 2.4.0 introduces explicit reproducibility mechanisms (fixed seed), automated multi-scenario comparison (`compare-scenarios`), graph density diagnostics, and repeated stochastic replication testing (`replication-test`).

> **Scientific scope:** The model is synthetic and exploratory. Its outputs should be interpreted as stress-test trajectories and hypothesis-exploration results rather than empirical forecasts.

# 2. Research Question

The central research question is:

> **How can interacting climate-related stressors, heterogeneous municipal vulnerability, resilience capacity, and network dependencies contribute to systemic risk and cascading effects within a synthetic municipal system?**

The model supports investigation of related questions:

### RQ1 — Adaptation

How does increased adaptation capacity affect local and systemic risk?

### RQ2 — Infrastructure

How does infrastructure resilience influence damage accumulation and recovery?

### RQ3 — Network Effects

How does network density affect the propagation of risk between municipalities?

### RQ4 — Cascading Risk

Under what modeled conditions can local stress propagate through dependencies and become systemic?

### RQ5 — Recovery

How does combined resilience, infrastructure capacity, and adaptation affect recovery dynamics?

# 3. Model Objectives

### 3.1 Explore systemic vulnerability

Represent how multiple interacting stressors can produce risk beyond isolated local impacts.

### 3.2 Explore cascading effects

Represent how risk in one municipality can influence neighboring or dependent municipalities through an abstract network.

### 3.3 Examine resilience

Explore the relationship between resilience, infrastructure, adaptation, damage, and recovery.

### 3.4 Support reproducible experimentation

Provide deterministic seed control, automated scenario comparisons, and repeated stochastic simulations.

### 3.5 Provide an extensible research framework

Create a computational foundation that can eventually incorporate empirical climate, geographic, infrastructure, and socioeconomic datasets.

# 4. Conceptual Framework

Plaintext

```
                 CLIMATE / ENVIRONMENTAL PRESSURE
                              │
                              ▼
                         ┌─────────┐
                         │ HAZARD  │
                         └────┬────┘
                              │
                              ▼
                 ┌─────────────────────────┐
                 │ Exposure × Vulnerability│
                 └───────────┬─────────────┘
                             │
                             ▼
                       ┌───────────┐
                       │ Local Risk│
                       └─────┬─────┘
                             │
                ┌────────────┴────────────┐
                │                         │
                ▼                         ▼
       Resilience / Adaptation       Sector Impacts
                │                         │
                └────────────┬────────────┘
                             │
                             ▼
                     ┌──────────────┐
                     │ Dependencies │
                     └──────┬───────┘
                            │
                            ▼
                     ┌──────────────┐
                     │   Cascades   │
                     └──────┬───────┘
                            │
                            ▼
                    ┌────────────────┐
                    │ Systemic Risk  │
                    └───────┬────────┘
                            │
                            ▼
                    Damage / Recovery
```

The framework combines concepts from Agent-Based Modeling, Complex Networks, Climate Risk Stress Testing, Cascading Failures, Infrastructure Resilience, Adaptation Dynamics, and Water–Energy–Food Nexus reasoning.

# 5. Agent Architecture

Each synthetic municipality contains a set of fixed characteristics and dynamic states.

## 5.1 Exposure

Represents the modeled degree to which an agent is exposed to the simulated hazard environment.

## 5.2 Vulnerability

Represents the modeled susceptibility of the agent to hazard impacts.

## 5.3 Resilience

Represents the modeled ability to absorb stress and contribute to recovery.

## 5.4 Sectoral sensitivities

Each municipality contains synthetic sensitivity parameters for:

- Water
    
- Agriculture
    
- Urban systems
    
- Heat
    

## 5.5 Dynamic state

The agent evolves through the simulation as hazard, sector impacts, cascade load, risk, damage, and recovery change over time.

## 5.6 Visual status

Municipalities transition between four qualitative visual states:

Plaintext

```
GREEN   → STABLE
YELLOW  → WARNING
ORANGE  → HIGH
RED     → CRITICAL
```

# 6. Risk Formulation

## 6.1 Hazard components

The model combines four principal pressure components:

|**Component**|**Weight**|
|---|---|
|Warming pressure|0.45|
|El Niño intensity|0.20|
|Deforestation pressure|0.20|
|Urban pressure|0.15|

Seasonality is modeled with an approximate amplitude of ±10%. A temporal drift of ~1.2%/year is applied.

Version 2.4.0 reduces hazard saturation and moderates temporal amplification relative to earlier internal formulations.

## 6.2 Raw Local Risk

Plaintext

```
RawRisk = Hazard × Exposure × Vulnerability / 10000
```

## 6.3 Net Risk

Net local risk is reduced by resilience, effective infrastructure, and effective adaptation:

Plaintext

```
Net Risk = Raw Risk − Resilience Effect − Infrastructure Effect − Adaptation Effect
```

## 6.4 Damage & Recovery

Damage incorporates local risk, economic impact, and cascade load.

Recovery depends on the combined capacity of resilience, infrastructure, and adaptation. Version 2.4.0 uses a gradual recovery rate (0.020/month).

# 7. Cascade Mechanism

Municipalities are connected through an abstract dependency network (`dependencies`).

Cascade pressure depends on neighboring risk, network connectivity, and cascade sensitivity.

### Cascade memory

Version 2.4.0 maintains persistent cascade load memory that decays exponentially by 8% per month (`cascade-load * 0.92`) before incorporating new spillover.

# 8. Scenarios

## 8.1 Fail-Open

Adaptation and infrastructure efficiency: **55%** (low protection).

## 8.2 Balanced

Nominal efficiency: **100%** (baseline protection).

## 8.3 Resilient

Efficiency: **up to 130%** (high protection).

# 9. Reproducibility & Multi-Run Analysis

`setup` uses:

Plaintext

```
random-seed 20260916
```

For statistical evaluation, `replication-test N` runs $N$ independent iterations across sequential seeds and reports key indicators to the console.

# 10. Limitations

- **Synthetic Municipalities:** Agents do not correspond to real Brazilian municipalities.
    
- **Abstract Topology:** Grid placement and dependencies are stylized.
    
- **Uncalibrated Parameters:** Inputs represent normalized scales (0–100), not absolute physical units.
    

> **Scientific interpretation:** The model should be interpreted as a stress-testing and hypothesis-exploration framework, not as an official climate forecast for Brazil.

# 11. Citation

If you use, modify, analyze, or build upon this model, please cite the corresponding software release:

**Chavatte, João Carlos. (2026). _Climate Stress Test — Brazil 2026–2030: An Exploratory Agent-Based Model for Systemic Climate Risk Stress Testing_. Version 2.4.0. Zenodo.**

**DOI:** 10.5281/zenodo.22836683

A machine-readable citation record is provided in `CITATION.cff`.

# 12. License

- **Code:** MIT License (`LICENSE`)
    
- **Documentation:** Creative Commons Attribution 4.0 International (`LICENSE-DOCS`)
    

# Status

Plaintext

```
╔══════════════════════════════════════════════════════╗
║  CLIMATE STRESS TEST                                 ║
║  BRAZIL 2026–2030                                    ║
║                                                      ║
║  VERSION        : 2.4.0                              ║
║  MODEL          : AGENT-BASED                        ║
║  PLATFORM       : NETLOGO                            ║
║  HORIZON        : 60 MONTHS                          ║
║  AGENTS         : 100 SYNTHETIC MUNICIPALITIES       ║
║  REPRODUCIBLE   : YES                                ║
║  REPLICATION    : AVAILABLE                          ║
║                                                      ║
║  STATUS         : EXPLORATORY RESEARCH ARTIFACT      ║
╚══════════════════════════════════════════════════════╝
```

> **This model is a computational stress test — not an official forecast.**