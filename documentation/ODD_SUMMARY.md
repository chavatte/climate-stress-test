# ODD-Oriented Summary

## Overview

### Purpose

To explore how interacting environmental pressure, exposure, vulnerability, resilience, adaptation, infrastructure capacity, and network dependencies can produce systemic risk and cascading effects in a synthetic municipal system.

### Entities, state variables, and scales

**Municipal agents:** Synthetic municipalities with exposure, vulnerability, resilience, and sectoral sensitivities (water, agriculture, urban, heat).

**Dependencies:** Abstract undirected dependencies (`undirected-link-breed`) used to propagate cascade effects; they do not represent empirical Brazilian infrastructure networks. Realized network metrics are monitored post-generation (`network-edge-count`, `network-mean-degree`, `network-realized-density`).

**Patches:** Abstract spatial cells organized into five stylized regional bands.

**Time:** One tick equals one month; 60 ticks represent five years (2026–2030 experimental horizon).

## Design concepts

### Emergence

Systemic risk and cascading damage emerge from interactions among local states and network dependencies.

### Adaptation

Adaptation investment modifies effective protective capacity (acting at 55% in `FAIL OPEN`, 100% in `BALANCED`, and up to 130% in `RESILIENT BY DESIGN`).

### Resilience

Resilience reduces effective local risk and contributes to gradual recovery (0.020/month rate).

### Interaction

Neighbor risk contributes to cascade pressure. Cascade load incorporates persistent memory with an 8%/month exponential decay (`cascade-load * 0.92`) before absorbing new spillover.

### Stochasticity

Synthetic initialization and network structure contain stochastic components. Version 2.4.0 provides fixed-seed reproducibility (`20260916`), automated scenario comparisons (`compare-scenarios`), and multi-run stochastic replications (`replication-test`).

### Observation

The model tracks local and systemic risk, peak systemic risk (`peak-system-risk`), average damage, peak damage (`peak-average-damage`), sector stress indices, total cascade events, graph density metrics, and scenario-level summary measures.

## Details

### Initialization

`setup` initializes the world, agents, attributes, network, dynamic variables, and the default reproducibility seed (`20260916`).

### Process overview

The conceptual process order per tick (month) is:

1. configure scenario;
2. update local hazard (~1.2%/year drift, ±10% seasonality);
3. calculate local risk;
4. update sector impacts;
5. propagate cascades (memory decay + spillover + intersectoral triggers);
6. apply adaptation;
7. apply recovery;
8. calculate aggregate metrics (including network structural diagnostics);
9. update visual state.

### Submodels

The model contains simplified submodels for hazard, local risk, sector impacts, cascading propagation, adaptation, damage, and recovery.

### Input data

No empirical municipal dataset is required by the current synthetic model. Baseline inputs are normalized experimental parameters (0–100 scales).

## Purpose-fit statement

The model is suitable for hypothesis exploration and computational stress testing. It is an exploratory research artifact rather than an empirical prediction or policy-grade forecasting model.