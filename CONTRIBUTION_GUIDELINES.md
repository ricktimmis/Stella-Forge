# ⭐ Stella Forge: Contribution Guidelines

## 💡 Our Philosophy
Stella Forge is a high-stakes, technically rigorous project focused on bridging theoretical space engineering with industrial application. Contributions are welcomed, but must maintain technical precision and adhere strictly to the defined scope.

## ⚙️ Development Workflow (Current Phase: Concept Validation)

1.  **Understand the Mandate:** Before any code review or design proposal, thoroughly read `VISION.md` and `REQUIREMENTS.md`. If a proposed change violates existing requirements, it must be justified as a necessary enhancement to meet a higher-priority goal.
2.  **Simulation & Validation:** All changes to `modeling_spec.md` must be paired with corresponding adjustments to `artifacts.sim/simulation_results.py` and documented in a separate validation report that satisfies **REQ-SCI-002**.
3.  **Code Review:** Focus on modularity, computational efficiency (especially in finite element/CFD solvers), and strict adherence to established data flow (per `AGENT_PROTOCOLS.md`).
4.  **Proposals:** For major feature additions (new phases, new technologies), open a formal proposal that articulates the specific gaps in current requirements and the expected impact on commercial viability (REQ-CMR-004).

## 📝 Suggested Contribution Types
*   **Simulation Refinement:** Improving solver performance, refining boundary condition parameters, or replicating new scenarios.
*   **Documentation Expansion:** Elaborating on technical assumptions or filling gaps in risk registers.
*   **Literature Review:** Proposing new ISRU pathways or citing competitive manufacturing solutions.

**NOTE:** This project is heavily gatechecked. All major architectural shifts must be approved by the Technical Lead and Advisory Agent before implementation.
