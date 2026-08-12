# Axiom CNC: Precision Open-Source Desktop Mill 🛠️

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Design Phase](https://img.shields.io/badge/Status-Design%20Phase-blue)](#roadmap)

**Axiom CNC** is a high-rigidity, open-source desktop milling platform designed to bridge the gap between low-cost hobbyist routers and industrial milling machines. 

The primary objective of Axiom is to provide a professional-grade, reproducible blueprint for a machine capable of **precise PCB fabrication** and **light metal machining (Aluminum/Brass)**, making high-precision manufacturing accessible to students, makers, and educators worldwide.

## 🎯 Project Vision
Most DIY CNCs rely on belts or V-wheels, which lack the rigidity needed for precision work. Axiom solves this by utilizing a professional-grade mechanical stack consisting of Ball Screws and Linear Rails while maintaining a "home-buildable" philosophy using easily sourced parts.

This project is intended as an educational resource for the **Prince William County / MCPS VA school district**, providing a scalable "lab-in-a-box" model for STEM students to learn mechatronics, embedded systems, and precision engineering.

---

## ⚙️ Technical Specifications

### Mechanical Architecture
- **Work Envelope:** $600\text{mm} \times 600\text{mm} \times 150\text{mm}$ ($\approx$ 2ft x 2ft).
- **Frame:** T-Slot/V-Slot Aluminum Extrusions (2040/2080 profiles).
- **Motion System:** SFU1204/SFU1605 Ball Screws on X/Y axes to eliminate backlash.
- **Guidance:** MGN12H Linear Rails for high repeatability and load capacity.
- **Spindle:** 500W High-RPM Brushless DC Spindle.
- **Target Tolerance:** $\pm 0.01\text{mm}$.

### Control Stack
Axiom CNC utilizes a decoupled compute/control architecture to ensure maximum stability:
- **Compute Layer:** Raspberry Pi 4B/5B running a Linux environment.
- **Interface:** Powered by **CNCjs**. This provides a professional web-based UI for G-code management, real-time monitoring, and remote operation via any browser on the local network.
- **Control Layer:** RATTMMOTOR GRBL Controller Board for high-precision stepper pulse generation.
- **UI/UX:** 
    - **Remote:** Web-access via CNCjs.
    - **Local:** Direct HDMI output to monitor with USB Keyboard/Mouse for standalone workstation operation.

---

## 🏗️ System Architecture Diagram
`[User Interface (CNCjs)]` $\rightarrow$ `[Raspberry Pi (Host)]` $\rightarrow$ `[GRBL Board (Controller)]` $\rightarrow$ `[Stepper Motors]`

---

## 🗺️ Project Roadmap

- [x] **Phase 1: Technical Specification**
    - Define mechanical requirements for metal/PCB milling.
    - Select control electronics and CNCjs compute stack.
    - Draft initial Bill of Materials (BOM).
- [ ] **Phase 2: CAD & Design**
    - Create full assembly in Fusion 360 / FreeCAD.
    - Design custom brackets for aluminum extrusion joints.
    - Export STL files for 3D printed components.
- [ ] **Phase 3: Prototyping & Assembly**
    - Source industrial components (Rails, Ball Screws).
    - Assemble frame and calibrate axis movement.
    - Deploy CNCjs on Raspberry Pi and calibrate GRBL firmware.
- [ ] **Phase 4: Testing & Validation**
    - Perform precision tests (milling test PCBs).
    - Document "Build Guide" for public replication.
- [ ] **Phase 5: Public Release**
    - Publish all CAD files, BOMs, and Config scripts to this repo.

---

## 📦 Bill of Materials (BOM)
The full BOM is currently being finalized based on the CAD design. Once complete, it will be available as a `.csv` file in the `/docs` folder with direct links to sourced components from Amazon, McMaster-Carr, and OpenBuilds.

---

## 🤝 Contributing & Sponsorship
Axiom CNC is 100% open source. Contributions in the form of CAD reviews, electronics optimization, or funding are welcome.

**Sponsorship:** If you are a corporate entity interested in supporting local STEM innovation and workforce development in Manassas, VA, please reach out via my [LinkedIn](https://www.linkedin.com/in/andrew-richardson-2ba138351/)
.

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
