<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:10b981&height=200&section=header&text=Password%20Security%20Toolkit&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=Real-Time%20Analysis%20%7C%20Breach%20Detection%20%7C%20ML%20Guessability&descSize=15&descAlignY=58" width="100%"/>

[![Live Demo](https://img.shields.io/badge/Live_Demo-password--scanner--tool.netlify.app-10b981?style=for-the-badge&logo=netlify&logoColor=white)](https://password-scanner-tool.netlify.app)
[![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask_API-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

> Know exactly how breakable your password is —  
> real-time strength scoring, HIBP breach lookups, crack-time estimation,  
> and ML-powered guessability detection in one toolkit.

</div>

---

## 🌟 Features
https://password-strength-checker-indol-seven.vercel.app/
### 🔍 Core Analysis
| Feature | Details |
|---|---|
| ⚡ Real-time Analysis | Instant feedback on every keystroke |
| 🚨 HIBP Breach Detection | Cross-checks against known compromised password databases |
| ⏱️ Crack Time Estimation | Calculates time-to-crack on modern hardware |
| 🌍 Multi-language Dictionary | Detects common words across multiple languages |
| 🏢 Policy Enforcement | Customizable org-level security requirement rules |
| 🤖 ML Guessability | AI-powered weakness and pattern detection |
| 📊 Visual Strength Meter | Block-based intuitive strength visualization |

### 🛠️ Technical Interfaces
| Interface | Use Case |
|---|---|
| 🖥️ CLI Tool | Batch processing and automation |
| 🔌 Flask REST API | Integration with external apps and services |
| 🌐 Web Frontend | Interactive React/HTML dashboard with live feedback |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![HIBP](https://img.shields.io/badge/HaveIBeenPwned-API-10b981?style=flat&logo=security&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat&logo=netlify&logoColor=white)

---

## 📂 Project Structure
```
password-security-toolkit/
├── backend/
│   ├── app.py                    # Flask REST API entry point
│   ├── analyzer.py               # Core password analysis engine
│   ├── breach_check.py           # HIBP API integration
│   ├── crack_time.py             # Crack time estimation logic
│   ├── ml_model.py               # ML guessability predictor
│   ├── policy.py                 # Org policy enforcement rules
│   └── dictionary/               # Multi-language word lists
├── cli/
│   └── toolkit.py                # CLI batch processing tool
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── StrengthMeter.jsx # Block-based visual meter
│   │   │   ├── BreachBadge.jsx   # HIBP result display
│   │   │   └── MetricsDash.jsx   # Full security dashboard
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
├── requirements.txt
├── .env.example
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Python **3.7+**
- Node.js **16+** *(for frontend development)*
- pip package manager

### 1. Clone the Repository
```bash
git clone https://github.com/Saif8671/password-security-toolkit.git
cd password-security-toolkit
```

### 2. Backend Setup
```bash
pip install -r requirements.txt
```

### 3. Frontend Setup *(optional — for local development)*
```bash
npm install
npm run dev
```

### 4. Run the Flask API
```bash
python backend/app.py
```

API runs at **http://localhost:5000**

### 5. Run the CLI Tool
```bash
# Analyze a single password
python cli/toolkit.py --password "MyP@ssw0rd"

# Batch process from a file
python cli/toolkit.py --file passwords.txt
```

---

## 🔌 API Reference

### `POST /analyze`
Full password security analysis.

**Request:**
```json
{ "password": "MyP@ssw0rd123" }
```

**Response:**
```json
{
  "score": 82,
  "strength": "Strong",
  "crack_time": "3 centuries",
  "breached": false,
  "guessability": "Low",
  "suggestions": ["Add special characters", "Avoid keyboard patterns"]
}
```

### `POST /breach`
HIBP breach check only.
```json
{ "password": "password123" }
→ { "breached": true, "count": 2478921 }
```

---

## 🗺️ Roadmap

- [ ] Browser extension for real-time password field analysis
- [ ] Password generator with policy-aware output
- [ ] Export audit reports (PDF / CSV)
- [ ] Team dashboard for organization-wide policy monitoring
- [ ] Passphrase strength analysis
- [ ] Dark web monitoring integration

---

## 🤝 Contributing

1. Fork the repo
2. Create a branch: `git checkout -b feat/your-feature`
3. Commit: `git commit -m "feat: describe your change"`
4. Push and open a PR

---

## 📄 License

MIT © [Saif ur Rahman](https://github.com/Saif8671)

---

<div align="center">

Strong passwords aren't optional. Neither is knowing why. 🔐

[![GitHub](https://img.shields.io/badge/GitHub-Saif8671-100000?style=flat&logo=github)](https://github.com/Saif8671)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-00C7B7?style=flat&logo=netlify)](https://saif-portfolio8671.netlify.app)
[![Live Tool](https://img.shields.io/badge/Try_It_Live-password--scanner--tool.netlify.app-10b981?style=flat&logo=netlify)](https://password-scanner-tool.netlify.app)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:10b981,100:0d1117&height=100&section=footer" width="100%"/>

</div>
