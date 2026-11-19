<div align="center">

# 🌌 PROJECT ZENITH — *The Celestial Eye*

**A real-time interactive sky map and orbital mission console for exploring the night sky from any coordinate on Earth while tracking live movements of the International Space Station (ISS) and the seven other planets of our solar system.**

[![Frontend](https://img.shields.io/badge/Frontend-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://github.com/nIyAtTI/Project-Zenith)
[![Backend](https://img.shields.io/badge/Backend-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://github.com/nIyAtTI/Project-Zenith)
[![Astronomy Engine](https://img.shields.io/badge/Ephemeris-PyEphem%20%26%20SGP4-0B0F19?style=for-the-badge)](https://github.com/nIyAtTI/Project-Zenith)
[![License: MIT](https://img.shields.io/badge/License-MIT-00E5FF?style=for-the-badge)](LICENSE)

### 🔗 [Launch Live Mission Console](https://cosmic-explorer-207.preview.emergentagent.com/)

</div>

---

## 🖥️ Mission Console Preview

### 1. Sky Explorer & Live Orbital Telemetry
> *Interactive 3D Earth location selector paired with real-time local sky state, planetary visibility (`VISIBLE` vs. `BELOW HORIZON`), and live ISS telemetry.*

![Project Zenith Sky Explorer Dashboard](dashboard.png)

### 2. Object Profile & AI Cosmic Dossier
> *Detailed celestial inspection combining scientific orbital parameters, discovery history, and ancient mythology.*

![Project Zenith Object Profile and Dossier](dossier.png)

---

## ✨ Core Capabilities

- **🌍 Coordinate-Based Sky Navigation:** Select any point on the interactive 3D globe, search by city, or use browser geolocation to immediately recompute the celestial sphere overhead[cite: 2].
- **🛰️ Live ISS Telemetry & Propagation:** Streams real-time **Latitude**, **Longitude**, **Altitude (~433 km)**, and **Orbital Velocity (~27,500 km/h)** using `SGP4` / `Skyfield` orbital mechanics[cite: 2, 3].
- **🪐 Planetary & Constellation Tracking:** Calculates live **Altitude**, **Azimuth**, **Apparent Magnitude**, and **Constellation position** for the Sun, Moon, Mercury, Venus, Mars, Jupiter, Saturn, Uranus, and Neptune[cite: 2, 3].
- **🌗 Local Sky State & Viewing Conditions:** Displays local solar phase (*Day / Night*), exact next **Sunrise & Sunset** timestamps, and **Bortle scale** light-pollution heuristics for dark-sky visibility[cite: 2, 3].
- **📖 Cosmic Dossier (AI Story Mode):** Generates a structured three-act narrative covering cold scientific facts, human discovery history, and cultural mythology for selected celestial bodies[cite: 1].

---

## 🛠️ Tech Stack & System Architecture

| Layer | Technologies & Libraries | Purpose |
| :--- | :--- | :--- |
| **Frontend UI** | React, JavaScript (ES6+), Tailwind CSS | Responsive sci-fi mission console, state management, and 3D Earth globe rendering |
| **Celestial Engine** | Python, `PyEphem` | Computes equatorial coordinates (RA/Dec) and local horizontal projections (Alt/Az)[cite: 3] |
| **Orbital Mechanics** | `SGP4` / `Skyfield` | Propagates real-time ISS trajectory and ground-track telemetry[cite: 3] |
| **External APIs** | Live ISS Telemetry API, OpenStreetMap Nominatim, Claude LLM | Real-time satellite coordinates, city geocoding, and AI-generated celestial dossiers[cite: 1] |

---

## 📐 How the Astronomy Engine Works (`celestial.py`)

Project Zenith translates raw astronomical data into observer-specific sky views through a three-stage pipeline[cite: 3]:

1. **Observer Horizon Frame:** Captures the user's geographic coordinates ($\text{Latitude}, \text{Longitude}$) and current UTC timestamp to establish the local meridian and horizon plane[cite: 2, 3].
2. **Coordinate Transformation:** Uses `PyEphem` astronomical algorithms to compute each planet's Right Ascension ($\alpha$) and Declination ($\delta$), converting them into local **Altitude** (degrees above the horizon) and **Azimuth** (compass bearing)[cite: 2, 3].
3. **Visibility & Bortle Filtering:** Evaluates object altitude ($\text{Alt} > 0^\circ$) and apparent magnitude against local Bortle light-pollution heuristics to flag whether a planet is currently `VISIBLE` or `BELOW` the horizon[cite: 2, 3].

---

## 🗺️ Future Enhancements

- [ ] **Time-Travel Sky Scrubber:** Interactive timeline slider to simulate planetary alignments and ISS passes on past or future dates.
- [ ] **Overhead Pass Alerts:** Countdown timer predicting the next visible ISS flyover for the user's chosen city.
- [ ] **Deep-Sky Catalog Overlay:** Toggleable Messier objects and constellation line overlays directly on the sky canvas.

---

<div align="center">
  <sub>Built with curiosity for space, orbital mechanics, and interactive web engineering by <a href="https://github.com/nIyAtTI">Niyatti</a>.</sub>
</div>
<img width="896" height="1991" alt="image" src="https://github.com/user-attachments/assets/f51e12ef-ab04-4c24-92b2-b7db90e713a8" />
<img width="896" height="930" alt="image" src="https://github.com/user-attachments/assets/2005ad4e-e05d-4206-ab4f-a8339d10231b" />
<img width="896" height="725" alt="image" src="https://github.com/user-attachments/assets/3fcfe421-a189-4951-8119-8e2cbba7a5a8" />
<img width="896" height="1217" alt="image" src="https://github.com/user-attachments/assets/d1518c0c-f5b9-4606-a277-c95f9b864d8b" />


