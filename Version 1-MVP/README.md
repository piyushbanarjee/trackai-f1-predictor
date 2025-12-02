# TrackAI – Version 1 (MVP)
### Unofficial Formula 1 Race Visualization & Prediction Prototype

TrackAI V1 is the **Minimum Viable Product (MVP)** of the TrackAI project.  
It focuses on **core race visualization and basic prediction**, built as a **local, browser-based research prototype**.

> ⚠️ **IMPORTANT:** This is an **unofficial, non-commercial, fan-made research project**.  
> It is **NOT affiliated with, endorsed by, or connected to Formula 1, the FIA, or any Formula 1 teams.**

---

## 🎯 Goal of Version 1

The goal of Version 1 is to:
- Prove the **core technical feasibility**
- Establish a clean **frontend–backend architecture**
- Enable basic **race replay + prediction**
- Serve as the **foundation for Version 2 & Version 3**

---

## ✅ Features in Version 1 (MVP)

- Single race replay from historical data  
- Lap-by-lap driver positions  
- Timing tower (positions + gaps)  
- Basic track map visualization  
- Simple win probability prediction  
- Manual local data loading (no live feed)  
- REST API-based frontend–backend communication  

❌ No chatbot  
❌ No what-if simulation  
❌ No full season analytics  

---

## 🛠 Tech Stack (V1)

### Frontend
- Next.js (React + JavaScript)
- Tailwind CSS
- Basic SVG/Canvas animations

### Backend
- Python 3.10+
- FastAPI
- SQLite (local file database)
- pandas, numpy

### Data
- OpenF1 API / FastF1 (user-fetched data only)

---

## 🏗 Architecture (V1)

Browser (Next.js UI)
↓
FastAPI Backend
↓
Local SQLite / JSON Data


- The frontend **never directly accesses the database**
- All data flows through **FastAPI REST endpoints**
- Race data is **loaded locally from files**

---

## 📁 Project Structure (V1)

trackai-v1/
├── backend/
│ ├── app/
│ │ ├── api/ # Race endpoints
│ │ ├── services/ # Race state + prediction logic
│ │ └── main.py # FastAPI entry point
│ ├── data/ # Local race data
│ ├── scripts/ # Data fetch scripts
│ ├── requirements.txt
│ └── .env.example
│
├── frontend/
│ ├── public/
│ ├── src/
│ │ ├── pages/
│ │ ├── components/
│ │ ├── lib/api/
│ │ └── styles/
│ ├── package.json
│ └── .env.local.example
│
├── .gitignore
├── README.md
└── LICENSE

---

## ⚙️ Installation & Setup (V1)

### 1️⃣ Clone Repository
```bash
git clone https://github.com/piyushbanarjee/TrackAI-F1-Predictor.git
cd trackai

### 2️⃣ Backend Setup
cd backend
python -m venv venv
source venv\Scripts\activate
pip install -r requirements.txt

### 3️⃣Create .env File (Backend)
cp .env.example .env


### Edit .env:
DEBUG=True
4️⃣ Run Backend
uvicorn app.main:app --reload


Backend runs at:

http://localhost:8000

5️⃣ Frontend Setup
cd ../frontend
npm install
cp .env.local.example .env.local


Edit .env.local:

NEXT_PUBLIC_API_BASE_URL=http://localhost:8000


Run frontend:

npm run dev


Frontend runs at:

http://localhost:3000

📊 Data Usage (V1)

This repository does NOT include real F1 data

Users must fetch their own race data

Supported tools:

OpenF1 API

FastF1 Python library

Data is stored locally in:

backend/data/

🔐 Security (V1)

No API keys are used in Version 1

No authentication is implemented

All data is local

Safe for public GitHub hosting

⚖️ Legal Disclaimer

TrackAI V1 is an unofficial academic and research project.

Not affiliated with Formula 1, FIA, or any racing team

All trademarks belong to their respective owners

No official logos or branding assets are used

No proprietary or paid data is distributed

Built strictly for educational and research purposes

📜 License

This project is released under the MIT License.

You may:

Use

Modify

Fork

Distribute

With proper attribution.

🧭 Roadmap Beyond V1

Version 2: Strategy engine, season analytics, basic chatbot

Version 3: Machine learning predictions, what-if simulation, advanced AI chatbot

📬 Contact

Project Author: Piyush Banarjee
Email: dev.piyush195@gmail.com

GitHub: https://github.com/piyushbanarjee

TrackAI V1 is the foundational prototype for a larger research-grade Formula 1 analytics platform.