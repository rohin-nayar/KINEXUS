# Attitude Determination System for Kinexus Spacecraft

## Overview

This repository contains the MATLAB code implementation for the Attitude Determination System designed for the Kinexus spacecraft, an asteroid kinetic impactor vehicle. The system aims to achieve highly accurate state estimation to meet stringent fine-pointing accuracy requirements during different mission modes.

## Contents

- **`src/`**: Contains the MATLAB source code for the attitude determination system.
- **`simulations/`**: Includes simulation scripts and scenarios for testing the attitude determination algorithms.
- **`docs/`**: Documentation and additional resources related to the system design.

## System Design

The attitude determination system design involves the following key components:

- Quantification of disturbance environment.
- Selection of appropriate sensor hardware.
- Implementation of redundancy architecture.
- Evaluation of various attitude determination algorithms.

The chosen approach combines the Quaternion Estimator (QUEST) algorithm with the Unscented Kalman Filter (UKF) to provide a robust dual attitude determination solution.

## Simulation Results

Simulation results, including Root Mean Square Error (RMSE) comparisons, indicate that the UKF outperformed other algorithms in the spacecraft scenario. Monte Carlo simulations were subsequently conducted to optimize characteristic parameters, leading to the development of a precise dual attitude determination algorithm.

## Mission Modes

The spacecraft operates in different modes during the mission:

- **Nominal Mode**: Enables telemetry tracking with the transponder activated.
- **Safe Mode**: Used for spacecraft stabilization, utilizing the Reaction Control System (RCS).
- **Attitude Acquisition Mode**: Ensures minimal pointing error after orbit injection or trajectory correction maneuvers.
- **Stand-by Mode**: The standby state of the spacecraft.

## Performance Requirements

The spacecraft's performance requirements are classified into two modes:

- **Fine-Pointing Attitude Mode**: Requires pointing accuracy of less than $0.1^\circ$ for trajectory orbit insertion and on-station communication.
- **Coarse Attitude Pointing Mode**: Requires pointing accuracy of $1^\circ$ for instrument initialization, calibration, and unloading of saturated reaction wheels.

## Getting Started

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/attitude-determination.git
    cd attitude-determination
    ```

2. Open MATLAB and navigate to the `src/` or `simulations/` directory to run specific scripts.

3. Explore the provided documentation in the `docs/` directory for more details on system design and simulation scenarios.

## References

- Space Mission Engineering, The New SMAD.