# ODD-Oriented Summary

## Overview

### Purpose

To explore how interacting environmental pressure, exposure, vulnerability, resilience, adaptation, infrastructure capacity, and network dependencies can produce systemic risk and cascading effects in a synthetic municipal system.

### Entities, state variables, and scales

**Municipal agents:** synthetic municipalities with exposure, vulnerability, resilience, and sectoral sensitivities.

**Dependencies:** abstract directed/undirected-style relationships used to propagate cascade effects; they are not empirical Brazilian infrastructure networks.

**Patches:** abstract spatial cells organized into five stylized regional bands.

**Time:** one tick equals one month; 60 ticks represent five years.

## Design concepts

### Emergence

Systemic risk and cascading damage emerge from interactions among local states and network dependencies.

### Adaptation

Adaptation investment modifies effective protective capacity.

### Resilience

Resilience reduces effective local risk and contributes to recovery.

### Interaction

Neighbor risk contributes to cascade pressure.

### Stochasticity

Synthetic initialization and network structure contain stochastic components. Version 2.0 provides fixed-seed reproducibility and repeated replication.

### Observation

The model tracks local and systemic risk, damage, recovery-related variables, and scenario-level summary measures.

## Details

### Initialization

`setup` initializes the world, agents, attributes, network, dynamic variables, and the reproducibility seed.

### Process overview

The conceptual process order is:

1. configure scenario;
2. update local hazard;
3. calculate local risk;
4. update sector impacts;
5. propagate cascades;
6. apply adaptation;
7. apply recovery;
8. calculate aggregate metrics;
9. update visual state.

### Submodels

The model contains simplified submodels for hazard, local risk, sector impacts, cascading propagation, adaptation, damage, and recovery.

### Input data

No empirical municipal dataset is required by the current synthetic model. Baseline inputs are normalized experimental parameters.

## Purpose-fit statement

The model is suitable for hypothesis exploration and computational stress testing. It is not currently fit for empirical prediction or policy-grade forecasting.
