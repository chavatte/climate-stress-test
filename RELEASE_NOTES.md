# Version 2.4.0 Release Notes

## Overview

Version 2.4.0 introduces enhancements to simulation determinism, numerical dynamics, intersectoral cascade modeling, and diagnostic metrics. This release formally frames the model as an **exploratory stress-testing artifact** for scenario analysis, rather than a predictive climate forecasting tool.

## Reproducibility & Testing

- **Deterministic Initialization:** Added explicit `random-seed` initialization to guarantee fully reproducible simulation runs under identical initial parameter configurations.
    
- **Multi-Run Replication Support:** Introduced the `replication-test N` execution procedure to automate repeated Monte Carlo runs across sequential seeds for stochastic sensitivity analysis.
    

## Numerical Behavior & Dynamic Calibration

- **Hazard Tuning:** Reduced hazard saturation, dampened seasonality amplitude, and lowered artificial temporal growth rates to prevent premature clipping.
    
- **Initial Distribution Control:** Narrowed synthetic baseline distributions across municipal attributes to eliminate initialization outliers.
    
- **Adaptation & Infrastructure Adjustment:** Moderated monthly adaptation and infrastructure gain rates to reflect realistic long-term capacity building.
    
- **Gradual Recovery Mechanics:** Recalibrated municipal damage recovery coefficients to enforce a more gradual, realistic restoration curve.
    
- **Cascade Memory & Thresholds:** Integrated exponential decay into cascade load calculations to simulate memory attenuation over time, paired with elevated intersectoral trigger thresholds to reduce false-positive propagation.
    

## Metrics & Diagnostics

- **Peak Systemic Risk Tracking:** Added real-time tracking and interface monitors for maximum systemic risk (`peak-system-risk`).
    
- **Peak Damage Tracking:** Added tracking for peak average municipal damage (`peak-average-damage`) across the execution timeline.
    
- **Replication Summaries:** Implemented aggregated output reporting and summary statistics for multi-run replication suites.
    

## Scientific Positioning

- **Exploratory Scope:** Formally designated as a scenario-based stress-testing framework to evaluate relative systemic vulnerabilities, rather than a predictive or deterministic climate forecast model.