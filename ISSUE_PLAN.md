# Project Issue Plan: Stella Forge (v0.2)

This plan formalizes the development pipeline by breaking down the thermal and mechanical modeling into actionable, open-source issues. These issues are candidates for community contribution.

## 🎯 Goal
Transition from concept to verifiable, simulated baseline for Stella Forge.

## 🛠 Issue Breakdown: Technical Modeling (High Priority)

### #1: FEA Model Setup - Steady-State Printing Phase
*   **Description:** Create the baseline geometry and BCs for continuous operation. Focus on establishing the thermal equilibrium of a steady $100\text{mm}$ weld bead.
*   **Requirements:** Input alloy properties ($\rho, \text{C}_\text{p}, k, T_m$); define the heat flux ($\text{W/mm}^2$); implement the $h_{coupling}$ boundary condition reflecting the heat-transferring copper clamps.
*   **Expected Output:** Simulation results showing stable $\text{T}(x)$ profiles and maximum sustained print velocity.

### #2: FEA Model Setup - Transient Transition Phase
*   **Description:** Model the dynamic cycle—the transition from the active deposition phase to the un-clamped travel phase.
*   **Requirements:** Must integrate an instantaneous removal of heat flux upon un-clamping; accurately model the thermal inertia and time lag of the clamping system.
*   **Expected Output:** Data showing thermal shock profiles and proving the required thermal buffer time between successive prints.

### #3: Thermal Validation - Integrated Heat Loop
*   **Description:** Focus solely on the closed-loop heat management system. Validate the thermal efficiency of heat moving from the Cooler to the Pre-heater using a simplified system model.
*   **Requirements:** Must define the efficiency of the simulated heat pipe/conduction link; compare net power demand against ideal thermodynamic limits.
*   **Expected Output:** Efficiency metrics ($\eta$) for the heat recovery system under various load scenarios.

## 🏗 Issue Breakdown: Infrastructure & Standards (Medium Priority)

### #4: Open-Source Data Schema & API
*   **Description:** Define the standardized format for sharing simulation data. This allows external contributors to interface with the models without needing to replicate data structures.
*   **Requirements:** Define JSON/YAML schemas for material input parameters, BC definitions, and final result outputs.
*   **Expected Output:** A formal `data_schema.yaml` file and starter scripts for data ingestion.

### #5: Code Repository Initialization
*   **Description:** Set up the core Git structure, establish CI/CD for simulation code, and create templates for new contributors.
*   **Requirements:** Initialize basic Python project structure; implement environment management ($\text{venv}$); integrate tools for static code analysis.
*   **Expected Output:** A functional, templated repository ready for contribution.