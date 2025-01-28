# **Cycle-Somatic Box: Design Document**

## **Overview**

The Cycle-Somatic Box is a dual-purpose system designed to address two critical challenges:

1. **Continuous energy generation** for the Seigr Hub during periods when solar power is insufficient.
2. **Efficient waste management**, transforming organic material into nutrient-rich soil.

This document outlines the design of the Cycle-Somatic Box, focusing on its physical structure, core components, operational principles, and system integration.

---

## **1. Objectives**

### Primary Objectives

- **Sustainable Power Generation**: Utilize microbial fuel cell (MFC) technology to harvest electricity from organic waste.
- **Regenerative Composting**: Convert organic waste into high-quality soil for forest regeneration.

### Secondary Objectives

- Operate year-round, including in low-temperature and low-sunlight conditions.
- Provide modular scalability for increased energy output.
- Minimize maintenance requirements while ensuring ease of operation.

---

## **2. Physical Design**

### Dimensions

- **Outer Dimensions**: 1m x 1m x 1m.
- **Internal Compartments**:
  - Composting Zone: Occupies the bulk of the internal volume.
  - Soil Collection Tray: Accessible at the base for easy removal of finished compost.

### Materials

- **Wood**:
  - Locally sourced, treated with the **Shou Sugi Ban** method (charred wood) for durability and pest resistance.
  - Sealed with linseed oil and non-toxic sealants for moisture protection.
- **3D-Printed Components**:
  - Made from **PETG filament** for durability, moisture resistance, and flexibility.
- **Metal Reinforcements**:
  - Stainless steel hinges, screws, and optional corner braces for structural stability.

### Key Features

- **Ventilated Lid**:
  - Hinged with hydraulic or spring-assisted supports for stability during operation.
  - Includes slatted vents for airflow control.
- **Drainage System**:
  - Perforated bottom or dedicated drainage outlet to manage leachate (excess liquid) effectively.
- **Sliding Soil Tray**:
  - A bottom-mounted tray with guide rails, allowing for easy extraction of finished compost.

---

## **3. Core Components**

### 3.1 **Electrodes**

#### Design

- **Material**: 3D-printed panels coated with **graphene spray** for high conductivity and durability.
- **Dimensions**:
  - Bottom (anode) panels: Four 50cm x 50cm segments.
  - Side (cathode) panels: Eight 50cm x 25cm segments (two per wall).
- **Structure**:
  - Perforated or grooved surface to increase microbial interaction and maximize electricity generation.

#### Placement

- **Anode**:
  - Positioned at the bottom of the compost pile in the anaerobic zone.
  - Designed for interaction with microbes that thrive in low-oxygen environments.
- **Cathode**:
  - Mounted near the top of the compost pile or along the inner walls.
  - Optimized for oxygen exposure to complete the electrochemical reaction.

---

### 3.2 **Power Regulation System**

#### DC-DC Step-Up Converter

- Converts MFC output (~0.7-1.0V per electrode pair) to a usable range (11-48V) for the EcoFlow Power Kit.

#### Capacitor Bank

- Smooths out voltage fluctuations caused by microbial activity and ensures consistent power output.

#### Wiring

- **Moisture-Resistant Wires**: Routed through 3D-printed grooves for protection.
- **Connection Hub**: Integrates all electrode outputs into the power regulation system.

---

### 3.3 **Moisture and Aeration Control**

- **Adjustable Vents**:
  - Slatted vents on the lid and upper walls allow airflow to maintain proper oxygen levels.
- **Drainage**:
  - Leachate collection via perforations at the base, preventing waterlogging and optimizing microbial activity.
- **Insulation**:
  - Thermal insulation in the walls to retain heat and support microbial activity during colder months.

---

### 3.4 **Compost and Soil Management**

- **Layering System**:
  - Organic waste is layered to ensure proper aeration and microbial distribution.
- **Separator Grids**:
  - Prevents unfinished compost from reaching the soil tray while allowing fine soil to filter through.
- **Soil Tray**:
  - Sliding or tilting tray design for easy collection of finished compost.

---

## **4. Operational Workflow**

1. **Input**:
   - Organic material, including kitchen scraps, forest biomass, and human waste, is added via the top lid.
   - Moisture levels are adjusted as needed to support microbial activity.

2. **Decomposition**:
   - Microbial activity breaks down organic material into compost, releasing electrons as a byproduct.

3. **Electricity Generation**:
   - Electrons travel from the anode (anaerobic zone) to the cathode (aerobic zone), generating a current captured by the electrodes.

4. **Energy Storage**:
   - Captured electricity is regulated via a DC-DC converter and stored in the EcoFlow Power Kit.

5. **Soil Extraction**:
   - Finished compost is collected from the bottom tray, leaving space for new organic waste.

---

## **5. Scalability and Modularity**

- **Series Connection**:
  - Multiple Cycle-Somatic Boxes can be connected in series to increase voltage output.
- **Parallel Connection**:
  - Configurations for higher current output to meet greater energy demands.
- **Shared Power Hub**:
  - A centralized voltage regulation unit can handle multiple boxes for streamlined energy storage.

---

## **6. Environmental Considerations**

- **Winter Operation**:
  - Insulated walls and microbial heat generation ensure consistent operation during colder months.
- **Sustainable Materials**:
  - Locally sourced wood and recyclable 3D-printed components minimize environmental impact.
- **Leachate Management**:
  - Excess liquid is collected and recycled to maintain compost moisture levels.

---

## **7. Challenges and Future Improvements**

### Current Challenges

- **Optimizing Electrode Efficiency**:
  - Ensuring the graphite coating remains durable and conductive over time.
- **Scaling the System**:
  - Managing wiring complexity in multi-box setups.
- **Cold Weather Performance**:
  - Maintaining microbial activity during prolonged freezing conditions.

### Future Improvements

- **Integrated Sensors**:
  - Add temperature, moisture, and voltage sensors for real-time monitoring.
- **Automated Systems**:
  - Implement a microcontroller to optimize airflow and energy storage dynamically.

---

## **8. Conclusion**

The Cycle-Somatic Box represents a seamless integration of biological and technological innovation. By leveraging microbial processes to generate electricity and soil, this design aligns with Seigr's ethos of sustainability, modularity, and environmental stewardship. This document serves as a foundation for further experimentation and refinement, inspiring a future of resilient and sustainable systems.

---
