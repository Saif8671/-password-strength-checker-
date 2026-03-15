<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:10b981&height=200&section=header&text=Password%20Security%20Toolkit&fontSize=52&fontColor=ffffff&fontAlignY=38&desc=Real-Time%20Analysis%20%7C%20Breach%20Detection%20%7C%20ML%20Guessability&descSize=16&descAlignY=60" width="100%"/>

<div align="center">

[![Live Demo](https://img.shields.io/badge/🔗%20Live%20Demo-password--scanner--tool.netlify.app-10b981?style=for-the-badge&logo=netlify&logoColor=white)](https://password-scanner-tool.netlify.app)

![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-API-000000?style=flat-square&logo=flask&logoColor=white)
![React](https://img.shields.io/badge/React-Frontend-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-10b981?style=flat-square)

</div>

---

## Overview

**Password Security Toolkit** is a multi-interface security tool that gives you a complete picture of how strong — or breakable — any password really is. It combines real-time strength scoring, Have I Been Pwned breach lookups, hardware-calibrated crack-time estimation, and ML-based pattern detection into a single deployable toolkit available as a web app, REST API, and CLI.

---

## Features

### Analysis Engine
- **Real-time scoring** — instant feedback on every keystroke, no submit needed
- **HIBP breach detection** — checks against hundreds of millions of known compromised passwords via k-anonymity hashing (your password never leaves in plaintext)
- **Crack time estimation** — calculates time-to-crack on modern consumer and enterprise hardware
- **ML guessability** — scikit-learn model trained to detect dictionary substitutions, keyboard walks, and structural patterns attackers exploit
- **Multi-language dictionary** — common word detection across major languages, not just English
- **Policy enforcement** — configurable org-level rules for length, character classes, and expiry requirements
- **Visual strength meter** — block-based progress indicator with per-criterion breakdown

### Interfaces

| Interface | Best For |
|---|---|
| **Web Dashboard** | Interactive use — React frontend with live feedback |
| **Flask REST API** | Integrating analysis into external apps or CI pipelines |
| **CLI Tool** | Batch processing password lists, automation, scripting |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Flask 3.x (Python 3.7+) |
| ML Model | scikit-learn |
| Breach Lookup | Have I Been Pwned API (k-anonymity) |
| Frontend | React + Vite |
| Deployment | Netlify (frontend) / any WSGI host (backend) |

---

## Project Structure

```
password-security-toolkit/
├── backend/
│   ├── app.py                # Flask REST API entry point
│   ├── analyzer.py           # Core password analysis engine
│   ├── breach_check.py       # HIBP API integration
│   ├── crack_time.py         # Crack time estimation logic
│   ├── ml_model.py           # ML guessability predictor
│   ├── policy.py             # Org policy enforcement
│   └── dictionary/           # Multi-language word lists
├── cli/
│   └── toolkit.py            # CLI batch processing tool
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── StrengthMeter.jsx
│   │   │   ├── BreachBadge.jsx
│   │   │   └── MetricsDash.jsx
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
├── requirements.txt
├── .env.example
└── README.md
```

---

## Getting Started

**Prerequisites:** Python 3.7+, Node.js 16+ (frontend only), pip

### 1. Clone

```bash
git clone https://github.com/Saif8671/password-security-toolkit.git
cd password-security-toolkit
```

### 2. Install backend dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the API

```bash
python backend/app.py
```

API available at `http://localhost:5000`.

### 4. Run the frontend *(optional)*

```bash
cd frontend
npm install
npm run dev
```

### 5. Use the CLI

```bash
# Single password
python cli/toolkit.py --password "MyP@ssw0rd"

# Batch from file
python cli/toolkit.py --file passwords.txt
```

---

## API Reference

### `POST /analyze`

Full password security analysis.

**Request**
```json
{ "password": "MyP@ssw0rd123" }
```

**Response**
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

---

### `POST /breach`

HIBP breach check only. Uses k-anonymity — only the first 5 characters of the SHA-1 hash are transmitted.

**Request**
```json
{ "password": "password123" }
```

**Response**
```json
{ "breached": true, "count": 2478921 }
```

---

## Roadmap

| Status | Feature |
|---|---|
| 📋 Planned | Browser extension for real-time password field analysis |
| 📋 Planned | Policy-aware password generator |
| 📋 Planned | Export audit reports (PDF / CSV) |
| 📋 Planned | Organization-wide policy monitoring dashboard |
| 📋 Planned | Passphrase entropy analysis |
| 💡 Idea | Dark web monitoring integration |

---

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit with conventional messages: `git commit -m "feat: describe your change"`
4. Push and open a pull request

---

## License

MIT © [Saif ur Rahman](https://github.com/Saif8671)
Free to use, modify, and distribute with attribution.

---

<div align="center">

**Built by [Saif ur Rahman](https://github.com/Saif8671)**

[![GitHub](https://img.shields.io/badge/GitHub-Saif8671-100000?style=flat-square&logo=github)](https://github.com/Saif8671)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://linkedin.com/in/saif-ur-rahman-0211002b9)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-00C7B7?style=flat-square&logo=netlify)](https://saif-portfolio8671.netlify.app)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=flat-square&logo=gmail)](mailto:saifurrahman887@gmail.com)

<br/>

*Strong passwords aren't optional. Neither is knowing why.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:10b981,100:0d1117&height=120&section=footer" width="100%"/>

</div>
