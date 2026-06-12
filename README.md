# 🌌 ExoAIP (Exoplanet Aeronautical Information Publication)

**ExoAIP** is a high-fidelity, interactive interstellar mission simulator and aeronautical information generator. It transforms real-world astronomical data from the **NASA Exoplanet Archive** into immersive, mission-critical documentation and real-time tactical displays for exoplanet exploration.

Designed as a professional **Sci-Fi / Aerospace Dashboard**, ExoAIP bridges the gap between pure astronomy and applied aerospace engineering, incorporating ICAO-standard protocols, procedural physics, and interactive 3D visualizations.

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![Flask](https://img.shields.io/badge/flask-3.0-green.svg)
![Three.js](https://img.shields.io/badge/Three.js-r128-cyan.svg)
![NASA](https://img.shields.io/badge/Data-NASA_Exoplanet_Archive-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

---

## 🚀 Key Mission Modules

### 1. 🦾 Advanced Physics & Aerodynamics
*   **Gravity & Escape Velocity:** Precise calculation of surface gravity ($g$) and escape velocity ($v_e$) in m/s, km/h, and knots (KT).
*   **Atmospheric Modeling:** Estimation of gas composition, specific gas constants, and local speed of sound ($c$).
*   **Drone Flight Dynamics:** Dynamic calculation of **Stall Speed ($V_s$)** for the *Exo-Drone MK-I* reference aircraft based on local air density ($\rho$).
*   **Re-entry Profile:** Calculation of the safe **Entry Angle Corridor** and **Thermal Load** factors to prevent atmospheric bounce or structural incineration.
*   **Plasma Blackout:** Prediction of ionization blackout duration during high-velocity atmospheric entry.

### 2. 🗺️ Holographic 3D Tactical Display
*   **3D Wireframe Terrain:** Interactive 3D landscape rendered via **Three.js** using procedural heightmap data.
*   **ExoATC Radar Simulator:** Active 360° radar sweep tracking flight targets (Probes, Drones, Scouts) with live Track Labels.
*   **Visual Interference:** Real-time simulation of signal degradation (glitches) caused by high bio-hazards or intense stellar activity.

### 3. 📡 Communications & Meteorology
*   **Exo-VOLMET:** Continuous meteorological radio broadcast in strict ICAO phraseology.
*   **Encoded METAR/TAF:** Procedural generation of raw coded weather reports, including exotic phenomena like **Methane Snow (SN CH4)** or **Volcanic Ash (VA)**.
*   **Interstellar Radio Transcript:** Dynamic dialogue simulation between *Orbital Control* and planet-side assets, featuring **Light-Speed Delay** calculations based on parsec distance.

### 4. 🧭 Navigation & Operations
*   **PulseWay RNAV:** Pulsar-based navigation system replacing GPS, utilizing galactic pulsar triangulation (e.g., PSR J0437-4715).
*   **Exo-FPL (Flight Plan):** Interactive mission filing system. Validates vessel **Delta-V** and mass against planetary gravity.
*   **Load & Balance Manifest:** Real-time structural integrity check. Prevents landing if local weight ($N$) exceeds landing gear limits ($kN$).
*   **SAR-26 Protocol:** Automated Search & Rescue planning, calculating **Time of Useful Consciousness (TUC)** based on atmospheric toxicity and pressure.

### 5. ☣️ Astrobiology & Planetary Protection
*   **Bio-Hazard Leveling:** Classification of planetary biomes (Level 1 to 5) based on habitability and corrosive factors.
*   **Biosphere Analysis Report:** Scientific generation of hypothetical ecosystems (e.g., Aeroplankton, Silicate-based life).
*   **Sterilization Checklist:** Mandatory multi-step decontamination protocol (UV-C, Thermal Bake-out) for high-risk biological environments.

---

## 🛠️ Architecture & Tech Stack

### Backend (Python/Flask)
- **Engine:** Modular architecture with specialized engines for Physics, Bio-hazard, Weather, and Navigation.
- **Data Integration:** `astroquery` for real-time NASA database synchronization.
- **Cache System:** Persistent JSON-based planet registry for instant autocomplete search.
- **Scientific Ops:** `numpy` and `scipy` for terrain filtering and complex aerodynamic formulas.

### Frontend (Modern Sci-Fi UI)
- **Visuals:** `Three.js` (WebGL) for 3D terrain and `HTML5 Canvas` for radar overlays.
- **Styling:** Custom "Aero-Terminal" design system using CSS variables, grid layouts, and monochromatic cyan/orange accents.
- **Interactivity:** Vanilla JS with Fetch API for real-time FPL validation and typewriter-style radio transcripts.
- **Print System:** Specialized `@media print` CSS that transforms the neon dashboard into a professional, black-and-white ICAO-standard paper document.

---

## 📦 Installation & Deployment

### Prerequisites
- Python 3.10 or higher
- Modern Web Browser (Chrome/Edge/Firefox) with WebGL support

### Setup
1. **Clone the repository:**
   ```bash
   git clone https://github.com/vás-profil/ExoAIP.git
   cd ExoAIP
   ```

2. **Initialize Virtual Environment:**
   ```bash
   python -m venv .venv
   .\.venv\Scripts\activate  # Windows
   source .venv/bin/activate  # Linux/macOS
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

## 🖥️ Running the Simulator

1. **Start the Flask Server:**
   ```bash
   python app.py
   ```
2. **Access the Dashboard:**
   Open **[http://localhost:8080](http://localhost:8080)** in your browser.

*Note: On the first run, the system will download the latest verified planet list from NASA (approx. 5-10MB). This list is cached locally in `planets_cache.json` for subsequent lightning-fast searches.*

---

## 📐 Scientific Models & Formulas

The simulator utilizes simplified but physically grounded models:
- **Atmospheric Density:** $\rho = \frac{P}{R_{spec} \cdot T}$
- **Stall Speed:** $V_s = \sqrt{\frac{2 \cdot m \cdot g}{\rho \cdot S \cdot C_{Lmax}}}$
- **Signal Delay:** $t = \frac{d_{ly}}{c}$ (where $c$ is the speed of light)
- **Local Weight:** $F_g = m \cdot (g \cdot 9.80665)$

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 🤝 Acknowledgments
- **NASA Exoplanet Archive** for providing open interstellar data.
- **ICAO/FAA** for the aeronautical phraseology and documentation standards.
- Inspired by classic aerospace terminal aesthetics and deep-space exploration concepts.

---
**SIGNAL STATUS: STABLE // AUTHORIZATION: INTERSTELLAR FEDERATION [NAV-DPT]**
