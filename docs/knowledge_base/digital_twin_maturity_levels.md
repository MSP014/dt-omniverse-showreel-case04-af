# Digital Twin Maturity Levels — Classification Framework

**Source:** Academic research (Tao et al.) and industry frameworks
**Date:** 2026-02-01
**Context:** Reference documentation for Case 04 (Air Field) Digital Twin classification

---

## Overview

Digital Twin maturity levels classify the sophistication and capabilities of a digital twin, progressing from basic descriptive models to highly autonomous and predictive systems. The classification extends from **L0 (static replica)** to **L5 (autonomous co-existence)**, with the core operational levels being L1-L3.

---

## Level Definitions

### L0: No Twin / Static Model

**Descriptor:** Descriptive / Static Replica

**Characteristics:**

- No active digital twin or only a static 3D model
- Describes and depicts the physical entity without real-time data connection
- Measurements are disparate or non-existent
- Sensors are not interconnected

**Use Cases:**

- Visualisation
- Planning and communication
- CAD/BIM models for documentation
- Geometry and material representation

**Key Limitation:** No dynamic behaviour or connection to the physical world.

---

### L1: Status / Reflecting the Real with the Virtual

**Descriptor:** Informative (Real-Time Data) / Connected - Manual

**Characteristics:**

- Real-time data capture from sensors
- Replicates the real-time state and changes in the physical entity
- Continuous monitoring of asset condition and performance
- Manual data entry or limited automated connection
- Primary function: **"What is happening right now?"**

**Use Cases:**

- Real-time status dashboards
- Condition monitoring
- Performance tracking
- Asset visibility

**Data Flow:** Physical Asset → Sensors → Digital Twin (Visualisation)

**Key Capability:** Reflects current conditions dynamically.

---

### L2: Controlling the Real with the Virtual

**Descriptor:** Informative (Real-Time + Historical Data) / Connected - Supervisory / Decision Support

**Characteristics:**

- Real-time data + historical data or benchmarks
- Can indirectly control the physical entity's operations
- Enables informed decision-making and analysis
- Captures and estimates effects of real-world events using historical data
- Rudimentary situational awareness
- Primary function: **"What should I do about it?"**

**Use Cases:**

- Predictive maintenance (early stage)
- Asset optimisation
- Decision support systems
- Supervisory control (operator-in-the-loop)
- Logistics optimisation (e.g. Vehicle Routing Problem)

**Data Flow:** Physical Asset ↔ Digital Twin ↔ Operator (Decision Support)

**Key Capability:** Supports operational decisions through analysis and recommendations.

---

### L3: Anticipating the Real with the Virtual

**Descriptor:** Predictive / Forecasting

**Characteristics:**

- Forecasts future state and operational processes
- Couples real-time + historical data with Machine Learning or physical process-based models
- Predicts future behaviour and performance
- Identifies patterns and assesses risks
- Enables "what-if" scenario analysis
- Primary function: **"What will happen next?"**

**Use Cases:**

- Risk mitigation
- Capacity planning
- Supply chain optimisation
- Failure prediction
- Performance forecasting

**Data Flow:** Physical Asset → Digital Twin → ML/Simulation Models → Predictions → Operator

**Key Capability:** Predictive analytics and future state forecasting.

---

## Extended Levels (L4-L5)

Some frameworks extend beyond L3:

- **L4: Optimisation** — Autonomous optimisation of processes based on predictions
- **L5: Autonomous Co-existence** — Fully autonomous operation with minimal human intervention

---

## Case 04 (Air Field) — Classification Justification

**Classified Level:** **L2 (Decision Support / Supervisory)**

### Scenario

Visualising the optimal refuelling order and tanker routes calculated based on flight priorities (departure times).

### L2 Characteristics Present

- ✅ **Real-time data:** Aircraft status (fuel levels, departure times)
- ✅ **Historical/Context data:** Flight schedules, priorities
- ✅ **Decision Support:** VRP (Vehicle Routing Problem) logic calculates optimal refuelling order
- ✅ **Supervisory control:** HUD/FUI displays recommended actions to the operator
- ✅ **Situational awareness:** System provides actionable intelligence

### Why Not L1?

L1 would only display: "Here are the aircraft and their current fuel levels."
**L2 provides:** "Here is the optimal action plan based on data analysis."

### Why Not L3?

L3 would predict: "In 2 hours, there will be a refuelling bottleneck due to peak traffic."
**Case 04 solves:** Current optimisation task, not future forecasting.

---

## References

1. Tao et al. — Digital Twin Maturity Framework
2. [ResearchGate: Digital Twin Classification Research](https://www.researchgate.net/)
3. [Digital Twin Atlas](https://digital-twin-atlas.com/)
4. Industry frameworks: Royal HaskoningDHV, BIM Community

---

**Document Status:** Knowledge Base Reference
**Last Updated:** 2026-02-01
**Maintained by:** Arthur (Case 04 Assistant)
