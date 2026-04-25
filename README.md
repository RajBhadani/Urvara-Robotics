<div align="center">

# 🌾 Urvara-Robotics

### *हर खेत का AI साथी · An AI Companion for Every Farm*

<br/>

[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active%20Development-orange.svg)]()
[![Made in Bihar](https://img.shields.io/badge/Made%20in-Bihar%20🇮🇳-blue.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Languages](https://img.shields.io/badge/Lang-Hindi%20%7C%20Bhojpuri%20%7C%20Maithili-yellow.svg)]()

<br/>

**AI + Robotics for 7.5 million small farmers across Bihar, UP & Jharkhand**

[🌐 Live Demo](#) · [📱 Features](#-features) · [🚀 Get Started](#-getting-started) · [🤝 Contribute](#-contributing)

</div>

---

## 📖 Table of Contents

- [About](#-about)
- [The Problem](#-the-problem)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [Contact](#-contact)

---

## 🚀 About

**Urvara-Robotics** is an open AgriTech platform combining a **vernacular AI assistant app** with an **affordable solar-powered agricultural robot** — built specifically for small and marginal farmers across Bihar, Uttar Pradesh, and Jharkhand.

> *"Only 3% of Bihar's 1.2 crore farmers have access to expert agricultural advice. We are fixing that."*

---

## 🌧️ The Problem

| # | Challenge | Reality |
|---|---|---|
| 1 | 🧑‍🌾 No agronomist access | Nearest expert is 50–100 km away |
| 2 | 🗣️ Language barrier | Most apps don't support Bhojpuri or Maithili |
| 3 | 💸 Wrong pesticide use | Massive annual crop losses across India |
| 4 | 🌊 Late weather response | Floods & droughts damage crops before farmers react |
| 5 | 👷 Labour shortage | Youth migration leaves farms critically understaffed |

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 📱 AI Companion App
- 📸 **Crop Disease Detection** — WhatsApp photo → AI diagnosis in seconds
- 🗣️ **Voice-First** — speak in Hindi, Bhojpuri, or Maithili
- 🌤️ **Weather Advisory** — 7-day farm-specific forecasts
- 📊 **Live Mandi Prices** — real-time rates across UP, Bihar & Jharkhand
- 🏛️ **Govt. Schemes** — PM-KISAN, KCC, PMFBY in one place
- 🤖 **AI Chat Assistant** — 24/7 farming advice in your language

</td>
<td width="50%">

### 🤖 Agricultural Robot *(Phase 2)*
- ☀️ Solar-powered, field-ready design
- 📷 Autonomous crop scanning with onboard camera
- 💧 Targeted pesticide spraying (infected areas only)
- 🌱 Real-time soil health sensors (NPK, moisture, pH)
- 🔋 Built in India at a fraction of import cost
- 📦 Daily rental model for FPOs & Panchayats

</td>
</tr>
</table>

---

## 🛠️ Tech Stack

### Frontend / App
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)

### AI / Backend
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)

### APIs & Services

| Service | Purpose |
|---|---|
| Claude Sonnet (Anthropic) | AI chat assistant & crop advisory |
| Google Gemini API | Hindi / Bhojpuri language responses |
| Google Speech-to-Text | Voice input processing |
| Whisper (OpenAI OSS) | Offline voice recognition |
| OpenWeatherMap | Farm-specific weather forecasts |
| Twilio / Meta Cloud API | WhatsApp bot integration |
| Supabase | Database & auth |

### Robot Hardware

| Component | Role |
|---|---|
| Raspberry Pi 4 | Main processing unit |
| Arduino Mega | Motor & actuator control |
| Pi Camera Module | Crop scanning |
| NPK Soil Sensors | Real-time soil health |
| 20W Solar Panel + LiPo | Power system |

---

## 🏁 Getting Started

### Prerequisites

```bash
node >= 18.0.0
python >= 3.10
git
```

### Installation

```bash
# 1. Clone the repo
git clone https://github.com/your-username/urvara-robotics.git
cd urvara-robotics

# 2. Install frontend dependencies
npm install

# 3. Install backend dependencies
pip install -r requirements.txt

# 4. Set up environment variables
cp .env.example .env
# Fill in your API keys in .env
```

### Environment Variables

```env
ANTHROPIC_API_KEY=your_key_here
GEMINI_API_KEY=your_key_here
GOOGLE_SPEECH_API_KEY=your_key_here
OPENWEATHER_API_KEY=your_key_here
TWILIO_ACCOUNT_SID=your_sid_here
TWILIO_AUTH_TOKEN=your_token_here
SUPABASE_URL=your_url_here
SUPABASE_KEY=your_key_here
```

### Run Locally

```bash
# Open the app directly in browser
open index.html

# OR start the backend API
uvicorn main:app --reload --port 8000
```

---

## 📁 Project Structure

```
urvara-robotics/
│
├── 📱 app/
│   ├── index.html              # Main PWA app
│   ├── css/                    # Stylesheets
│   └── js/                     # App logic & API calls
│
├── 🤖 backend/
│   ├── main.py                 # FastAPI entry point
│   ├── routes/
│   │   ├── advisory.py         # Crop advisory endpoints
│   │   ├── disease.py          # Disease detection endpoints
│   │   └── weather.py          # Weather & mandi endpoints
│   └── models/                 # ML model files
│
├── 🦾 robot/
│   ├── firmware/               # Arduino & Raspberry Pi code
│   ├── sensors/                # Soil & camera modules
│   └── vision/                 # YOLOv8 crop detection
│
├── 📊 data/
│   └── mandi_prices/           # District-wise crop price data
│
├── .env.example
├── requirements.txt
├── package.json
└── README.md
```

---

## 🗺️ Roadmap

```
✅  Phase 1 — AI App MVP
    ├── WhatsApp crop disease detection
    ├── Live mandi prices  (UP · Bihar · Jharkhand)
    ├── AI chat in Hindi / Bhojpuri / Maithili / Magahi / Awadhi
    ├── Government schemes directory
    └── 7-day weather advisory

🔄  Phase 2 — Agricultural Robot  (In Progress)
    ├── Solar robot prototype build
    ├── Soil sensor integration
    ├── Targeted spray system
    └── FPO rental model launch

🔜  Phase 3 — Platform & Data Layer
    ├── Anonymised agri-data marketplace
    ├── AI-powered input supply chain
    ├── Crop insurance risk data API
    └── Pan-India expansion  (MP · Odisha · WB)
```

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

```bash
# Fork the repo and create your branch
git checkout -b feature/your-feature-name

# Commit your changes
git commit -m "feat: describe your change"

# Push and open a Pull Request
git push origin feature/your-feature-name
```

**Ways to contribute:**
- 🌐 Add support for more regional languages (Odia, Maithili improvements)
- 🌾 Add more crop disease training data & images
- 📊 Improve mandi price accuracy for more districts
- 🤖 Robot firmware & sensor improvements
- 🐛 Bug fixes and performance optimisations

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a PR.

---

## 📬 Contact

| | |
|---|---|
| 📍 Location | Patna, Bihar → Pan India |
| 🐙 GitHub | [@urvara-robotics](https://github.com/urvara-robotics) |
| 📧 Email | hello@urvara-robotics.in |
| 💬 WhatsApp Community | [Join Here](#) |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**🌾 Built with ❤️ for the farmers of Bihar**

*"India's next agricultural revolution will begin in the fields."*

<br/>

⭐ **Star this repo** if you believe in technology for Bharat's farmers!

</div>
