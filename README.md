# AI-BASED-EARLY-LANDSLIDE-WARNING-IN-NER-
AI-based landslide early warning and risk assessment platform for Northeast India using rainfall, slope, soil moisture, historical landslides and vegetation data.
# 🌧️ AI-Based Landslide Early Warning System for Northeast India

### Smart India Hackathon (SIH) Project

An interactive, AI-assisted landslide risk assessment and early warning platform designed to identify potentially vulnerable areas across **Northeast India (NER)** using multiple environmental and historical risk factors.

The system combines **rainfall, slope, soil moisture, previous landslide history and vegetation conditions** to calculate a location-specific landslide risk score and display the result through an interactive map-based dashboard.

---

## 🚨 Problem Statement

Northeast India is characterized by mountainous terrain, steep slopes, intense monsoon rainfall and environmentally sensitive landscapes, making several areas susceptible to landslides.

Landslides can cause:

* Loss of human lives
* Road and transportation disruption
* Damage to houses and infrastructure
* Communication and power failures
* Isolation of remote communities
* Economic losses
* Difficulties for disaster-response teams

Existing landslide information can be difficult for ordinary users and local decision-makers to interpret quickly.

Our project aims to provide a **simple, visual and location-based early-warning interface** that converts multiple environmental risk factors into an understandable risk level.

---

# 🎯 Project Objective

The main objective is to develop a web-based platform that can:

1. Monitor important landslide risk factors.
2. Calculate a location-specific landslide risk score.
3. Display risk levels on an interactive map.
4. Identify low, moderate and high-risk areas.
5. Provide a breakdown of individual risk factors.
6. Allow users to search for a location.
7. Generate appropriate warning messages.
8. Support faster awareness and decision-making.
9. Provide a foundation that can later integrate real-time government and sensor data.

---

# 🧠 Proposed Solution

The system uses a **rule-based AI risk scoring model**.

Instead of relying on a single parameter such as rainfall, multiple factors are combined to estimate the overall landslide risk.

### Risk Factors

| Risk Factor                   |   Weight |
| ----------------------------- | -------: |
| 🌧️ Rainfall                  |      30% |
| ⛰️ Slope                      |      25% |
| 💧 Soil Moisture              |      20% |
| 📍 Previous Landslide History |      15% |
| 🌳 Vegetation                 |      10% |
| **Total**                     | **100%** |

The final risk score is calculated using weighted contributions from these factors.

### Risk Score Formula

```text
Risk Score =
(Rainfall × 0.30)
+ (Slope × 0.25)
+ (Soil Moisture × 0.20)
+ (Historical Landslides × 0.15)
+ (Vegetation × 0.10)
```

Each factor is normalized to a common scale before calculating the final score.

---

# ⚠️ Risk Classification

The calculated risk score is converted into an easy-to-understand warning level.

| Risk Score | Risk Level  | Warning             |
| ---------: | ----------- | ------------------- |
|       0–39 | 🟢 LOW      | Normal monitoring   |
|      40–69 | 🟡 MODERATE | Increased caution   |
|     70–100 | 🔴 HIGH     | Immediate attention |

> **Note:** These thresholds are prototype decision rules and should be calibrated and validated against official datasets before operational disaster-management use.

---

# 🗺️ Interactive Risk Map

The platform provides an interactive map for visualizing landslide risk.

Different colours represent different risk levels:

* 🟢 **Green — Low Risk**
* 🟡 **Yellow — Moderate Risk**
* 🔴 **Red — High Risk**

Users can interact with the map to understand the spatial distribution of potential landslide risk.

The interface is designed to make complex environmental information easier to understand for:

* Citizens
* Students and researchers
* Disaster-management teams
* Local authorities
* Emergency responders
* Infrastructure planners

---

# 🔎 Location Search

Users can search for a specific location in Northeast India.

After selecting a location, the system can display:

### Location Information

* Location name
* Latitude and longitude
* Risk level
* Overall risk score
* Individual risk factors
* Warning message
* Risk-factor contribution

Example:

```text
Location: Gangtok, Sikkim

Overall Risk: HIGH
Risk Score: 78/100

Rainfall:        High
Slope:           High
Soil Moisture:   Moderate
History:         High
Vegetation:      Moderate

Warning:
HIGH LANDSLIDE RISK — Avoid unnecessary travel
through vulnerable slopes and monitor local alerts.
```

---

# 📊 Risk Factor Breakdown

The dashboard does not only provide a final risk score.

It also explains **why** an area has been classified as risky.

For example:

```text
TOTAL RISK SCORE: 76

Rainfall             ████████████████  86%
Slope                ██████████████    72%
Soil Moisture        ███████████       58%
Historical Activity  ███████████████   78%
Vegetation           ███████           35%
```

This improves transparency and makes the system easier to understand.

---

# 🤖 AI / Decision Logic

The current prototype uses a **rule-based AI approach**.

The system receives environmental parameters, normalizes them and calculates a weighted score.

### Processing Pipeline

```text
Environmental Data
        ↓
Data Normalization
        ↓
Risk Factor Calculation
        ↓
Weighted Risk Model
        ↓
Overall Risk Score
        ↓
Risk Classification
        ↓
Warning Generation
        ↓
Interactive Map + Dashboard
```

---

# 🌧️ Rainfall Risk

Rainfall is given the highest weight because intense or prolonged rainfall can increase water infiltration and pore-water pressure, reducing slope stability.

```text
Rainfall Weight = 30%
```

Higher rainfall conditions increase the rainfall component of the risk score.

---

# ⛰️ Slope Risk

Steeper terrain generally presents greater susceptibility to slope failure.

```text
Slope Weight = 25%
```

The system therefore gives significant importance to terrain steepness.

---

# 💧 Soil Moisture Risk

High soil moisture can contribute to reduced soil strength and increased instability.

```text
Soil Moisture Weight = 20%
```

---

# 📍 Historical Landslide Risk

Previous landslide occurrence provides important information about the vulnerability of an area.

```text
Historical Landslide Weight = 15%
```

Areas with known historical landslide activity receive a higher risk contribution.

---

# 🌳 Vegetation Risk

Vegetation can influence slope stability through root reinforcement, interception and water-related processes.

```text
Vegetation Weight = 10%
```

Lower vegetation coverage can therefore contribute to increased risk in the prototype model.

---

# 🖥️ Website Features

### Current / Prototype Features

* 🌍 Interactive map
* 📍 Location search
* 🎨 Colour-coded risk visualization
* ⚠️ Automatic warning messages
* 📊 Risk-factor breakdown
* 🧮 Weighted risk calculation
* 🌧️ Rainfall risk
* ⛰️ Slope risk
* 💧 Soil-moisture risk
* 📍 Historical landslide risk
* 🌳 Vegetation risk
* 📱 Responsive dashboard
* 🚨 Low / Moderate / High warning system

---

# 🛰️ Future Real-Time Architecture

The prototype can later be expanded into a real-time early-warning platform.

```text
        WEATHER DATA
             │
             ▼
      Rainfall Sensors
             │
             ▼
       ┌─────────────┐
       │ Data Layer  │
       └─────────────┘
             │
   ┌─────────┼──────────┐
   ▼         ▼          ▼
Rainfall   Soil       Satellite
           Moisture     Data
   │         │          │
   └─────────┼──────────┘
             ▼
       Risk Engine
             │
             ▼
     Landslide Risk Score
             │
       ┌─────┼─────┐
       ▼     ▼     ▼
      LOW  MEDIUM HIGH
       │     │     │
       └─────┼─────┘
             ▼
       Warning System
             │
     ┌───────┼────────┐
     ▼       ▼        ▼
   Website   SMS    Dashboard
```

---

# 📡 Possible Data Sources

The project can eventually integrate official and sensor-based data sources.

Potential sources include:

* Geological Survey of India (GSI)
* India Meteorological Department (IMD)
* Satellite remote-sensing datasets
* Digital Elevation Models (DEM)
* Soil-moisture datasets
* Historical landslide inventories
* IoT soil-moisture sensors
* Automatic weather stations

GSI's National Landslide Forecasting Centre provides landslide-related information, susceptibility maps, inventories and forecasting resources.

GSI also reports that baseline landslide susceptibility mapping and landslide inventory data are available through its platforms.

---

# 🗺️ Target Region

The initial focus is **Northeast India (NER)**.

The system can be extended to cover:

* Arunachal Pradesh
* Assam
* Manipur
* Meghalaya
* Mizoram
* Nagaland
* Sikkim
* Tripura

The architecture can later be expanded to other landslide-prone regions of India.

---

# 🧑‍💻 Technology Stack

Depending on the implementation, the project can use:

### Frontend

* HTML5
* CSS3
* JavaScript
* Leaflet.js / Map-based visualization
* Responsive UI

### Backend

* Python / Flask or Node.js
* REST APIs
* Risk calculation engine

### Data / AI

* Rule-based AI
* Geospatial datasets
* Historical landslide data
* Weather data
* Soil-moisture data
* Terrain/slope data

### Deployment

* GitHub
* GitHub Pages / Vercel / Netlify
* Cloud backend if required

---

# 📂 Suggested Repository Structure

```text
AI-Landslide-Early-Warning-NER/
│
├── index.html
├── style.css
├── script.js
│
├── assets/
│   ├── images/
│   ├── icons/
│   └── logos/
│
├── data/
│   ├── locations.json
│   ├── rainfall.json
│   └── landslide-history.json
│
├── docs/
│   ├── architecture.md
│   ├── methodology.md
│   └── references.md
│
├── screenshots/
│   ├── dashboard.png
│   ├── risk-map.png
│   └── location-analysis.png
│
├── README.md
└── LICENSE
```

---

# 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/AI-Landslide-Early-Warning-NER.git
```

### 2. Open the project

```bash
cd AI-Landslide-Early-Warning-NER
```

### 3. Run the website

If it is a static website, simply open:

```text
index.html
```

For development, you can use VS Code with Live Server.

---

# 🌐 Live Website

## 🔗 Live Demo

**[ADD YOUR LIVE WEBSITE LINK HERE]**

Example:

```text
https://your-project.vercel.app
```

or

```text
https://YOUR-USERNAME.github.io/AI-Landslide-Early-Warning-NER/
```

---

# 📱 Demo

Add screenshots/GIFs of your working project here.

```text
Dashboard
↓
Interactive Map
↓
Location Search
↓
Risk Analysis
↓
Warning System
```

Example Markdown:

```markdown
![Dashboard](screenshots/dashboard.png)

![Risk Map](screenshots/risk-map.png)
```

---

# 🏆 Smart India Hackathon

This project is developed as a **Smart India Hackathon (SIH)** solution focused on disaster-risk reduction and technology-assisted landslide early warning.

### Core Innovation

The proposed system focuses on combining multiple risk factors into a simple, interpretable and location-specific risk score.

Instead of presenting raw environmental data, the platform converts the information into:

```text
DATA
 ↓
ANALYSIS
 ↓
RISK SCORE
 ↓
WARNING
 ↓
ACTION
```

This allows users to understand the potential severity of a location quickly.

---

# 🔮 Future Improvements

Future versions can include:

* Real-time IMD rainfall integration
* Live IoT soil-moisture sensors
* Satellite-based vegetation monitoring
* DEM-based automated slope calculation
* Historical landslide database integration
* Machine-learning prediction models
* SMS alerts
* WhatsApp alerts
* Mobile application
* Offline mode for remote regions
* Multi-language support
* Community reporting
* Emergency response integration
* Automatic rainfall-threshold detection
* Advanced GIS layers
* AI-based landslide probability forecasting

---

# ⚠️ Important Disclaimer

This project is a **prototype developed for research, educational and hackathon purposes**.

The risk score generated by the system should **not be treated as an official disaster warning or a replacement for government-issued alerts**.

For operational deployment, the model must be validated using reliable field observations, historical landslide records, meteorological data, terrain data and appropriate expert-reviewed thresholds.

Official information from agencies such as GSI and other relevant government authorities should be considered for actual disaster-management decisions.

---

# 📚 References

### Geological Survey of India

* National Landslide Forecasting Centre / BhuSanket
  https://bhusanket.gsi.gov.in/

* GSI Landslide Hazard & Forecasting Information
  https://bhusanket.gsi.gov.in/

### GitHub Documentation

* GitHub Repository Documentation
  https://docs.github.com/en/repositories

* GitHub README Documentation
  https://docs.github.com/en/get-started/learning-to-code/finding-and-understanding-example-code

---

# 👥 Team

### Smart India Hackathon Team

**Project:** AI-Based Landslide Early Warning System in Northeast India

**Domain:** Disaster Management / Artificial Intelligence / GIS / Web Technology

**Institution:** YOUR COLLEGE NAME

**Team Members:**

* Member 1 — Name
* Member 2 — Name
* Member 3 — Name
* Member 4 — Name
* Member 5 — Name
* Member 6 — Name

---

# ⭐ Project Vision

> **"From environmental data to early action — helping communities understand landslide risk before it becomes a disaster."**

The long-term vision is to build an accessible, scalable and data-driven landslide early-warning platform that can support communities and authorities in vulnerable mountainous regions.

---

## ⭐ If you find this project useful

Give the repository a ⭐ Star and feel free to contribute ideas, improvements and feedback.

**Built for Smart India Hackathon 🇮🇳**
