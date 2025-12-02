Perfect time to formalize everything. Below is a **complete, professional Software Requirements Specification (SRS)** for **TrackAI**.
This is written in a format you can directly use for:

* College submission
* GitHub documentation
* Funding / research proposals
* MS applications / portfolio

You can also convert this into a PDF later if you want.

---

# **Software Requirements Specification (SRS)**

## **Project Title:** TrackAI

### **Unofficial Formula 1 Strategy & Prediction Research Platform**

---

## 1. **Introduction**

### 1.1 Purpose

The purpose of this document is to specify the functional and non-functional requirements of **TrackAI**, an unofficial research-based web platform designed to analyze Formula 1 race data, visualize race dynamics, simulate strategy scenarios, and predict race and championship outcomes using probabilistic and AI-based models.

This SRS is intended for:

* Developers
* Academic evaluators
* Project reviewers
* Open-source contributors

---

### 1.2 Scope

TrackAI is a **browser-based analytics and simulation platform** that allows users to:

* Replay and visualize Formula 1 races
* View live-style race states from historical data
* Analyze race strategies (tyres, stints, pit stops)
* Predict race and championship outcomes
* Perform “what-if” strategy simulations
* Interact with the system using a natural-language chatbot

TrackAI is an **unofficial, non-commercial, research-focused** platform and is not affiliated with Formula 1, the FIA, or any Formula 1 teams.

---

### 1.3 Definitions, Acronyms & Abbreviations

| Term | Meaning                             |
| ---- | ----------------------------------- |
| F1   | Formula 1                           |
| API  | Application Programming Interface   |
| UI   | User Interface                      |
| DB   | Database                            |
| JSON | JavaScript Object Notation          |
| MVP  | Minimum Viable Product              |
| LLM  | Large Language Model                |
| ML   | Machine Learning                    |
| SRS  | Software Requirements Specification |

---

### 1.4 References

* OpenF1 API Documentation
* FastF1 Python Library
* FastAPI Documentation
* Next.js Documentation
* Tailwind CSS Documentation

---

## 2. **Overall Description**

---

### 2.1 Product Perspective

TrackAI follows a **client-server architecture**:

* **Frontend:** Web UI built using Next.js
* **Backend:** API server built with FastAPI
* **Data Layer:** Local database and processed race datasets
* **ML Layer:** Offline-trained prediction models
* **LLM Layer:** External AI API for chatbot responses

The frontend and backend communicate using **REST APIs** over HTTP.

---

### 2.2 Product Functions (High Level)

* Load and replay historical races
* Display live-style race visualization
* Display driver standings and season trends
* Analyze pit stop strategies and tyre stints
* Predict race and championship outcomes
* Run "what-if" simulations
* Answer user questions through a chatbot

---

### 2.3 User Characteristics

| User Type            | Skills                            |
| -------------------- | --------------------------------- |
| Student / Researcher | Basic programming & data analysis |
| F1 Enthusiast        | No technical background required  |
| Developer            | Comfortable with web technologies |

TrackAI is designed for **single-user local execution**.

---

### 2.4 Operating Environment

* **OS:** Windows / Linux / macOS
* **Frontend:** Runs in any modern web browser
* **Backend:** Python 3.10+
* **Database:** SQLite / PostgreSQL (optional upgrade)

---

### 2.5 Design & Implementation Constraints

* No official F1 logos or proprietary branding may be used
* No proprietary F1 data may be redistributed
* All API keys must be stored in environment variables
* All prediction models must run locally
* The system must function without internet for historical analysis

---

### 2.6 Assumptions & Dependencies

* Users will fetch their own race data using legal data sources
* Users will provide their own LLM API key for chatbot usage
* Predictions are probabilistic and not guaranteed to be accurate

---

## 3. **System Architecture Overview**

### 3.1 High-Level Architecture

```
User → Browser (Next.js UI)
        ↓
   FastAPI Backend
        ↓
  Local Database / Files
        ↓
   ML Prediction Models
        ↓
   External LLM API (Chatbot)
```

---

### 3.2 Logical Components

1. Frontend Visualization Layer
2. Backend API Layer
3. Strategy & Prediction Engine
4. Data Ingestion Layer
5. Machine Learning Layer
6. Chatbot & LLM Integration Layer

---

## 4. **Functional Requirements**

---

### 4.1 Race Visualization

| ID   | Requirement                                             |
| ---- | ------------------------------------------------------- |
| FR-1 | The system shall display race positions lap-by-lap      |
| FR-2 | The system shall show driver gaps to the leader         |
| FR-3 | The system shall visualize car positions on a track map |
| FR-4 | The system shall allow replay of any loaded race        |
| FR-5 | The system shall support multiple races per season      |

---

### 4.2 Season Analysis

| ID   | Requirement                                       |
| ---- | ------------------------------------------------- |
| FR-6 | The system shall display driver standings         |
| FR-7 | The system shall display constructor standings    |
| FR-8 | The system shall show points progression charts   |
| FR-9 | The system shall compare performance across races |

---

### 4.3 Strategy Analysis

| ID    | Requirement                                        |
| ----- | -------------------------------------------------- |
| FR-10 | The system shall display pit stop laps             |
| FR-11 | The system shall display tyre compound usage       |
| FR-12 | The system shall show stint timelines              |
| FR-13 | The system shall estimate undercut/overcut effects |

---

### 4.4 Prediction System

| ID    | Requirement                                     |
| ----- | ----------------------------------------------- |
| FR-14 | The system shall calculate win probabilities    |
| FR-15 | The system shall calculate podium probabilities |
| FR-16 | The system shall calculate points probabilities |
| FR-17 | The system shall predict championship outcomes  |
| FR-18 | The system shall allow predictions at any lap   |

---

### 4.5 What-If Simulation

| ID    | Requirement                                   |
| ----- | --------------------------------------------- |
| FR-19 | The system shall allow changing pit stop lap  |
| FR-20 | The system shall allow changing tyre compound |
| FR-21 | The system shall re-simulate race outcome     |
| FR-22 | The system shall show updated probabilities   |

---

### 4.6 Chatbot System

| ID    | Requirement                                         |
| ----- | --------------------------------------------------- |
| FR-23 | The system shall accept user questions              |
| FR-24 | The system shall use race data as chatbot context   |
| FR-25 | The system shall explain prediction results         |
| FR-26 | The system shall answer strategy comparison queries |
| FR-27 | The system shall return natural-language responses  |

---

### 4.7 Data Management

| ID    | Requirement                                        |
| ----- | -------------------------------------------------- |
| FR-28 | The system shall allow importing external data     |
| FR-29 | The system shall store processed race data locally |
| FR-30 | The system shall cache season statistics           |
| FR-31 | The system shall support multi-season storage      |

---

## 5. **Non-Functional Requirements**

---

### 5.1 Performance

* NFR-1: Race state retrieval time ≤ 300 ms (local)
* NFR-2: Prediction computation ≤ 2 seconds
* NFR-3: What-if simulation ≤ 3 seconds

---

### 5.2 Scalability

* NFR-4: Support at least 10 seasons of data
* NFR-5: Support simultaneous analysis of 20+ drivers

---

### 5.3 Security

* NFR-6: No API keys shall be hardcoded
* NFR-7: Sensitive configuration must be stored in `.env`
* NFR-8: No third-party data will be redistributed

---

### 5.4 Usability

* NFR-9: The UI shall be usable without technical knowledge
* NFR-10: All charts must be clearly labeled
* NFR-11: The chatbot must respond in under 5 seconds

---

### 5.5 Reliability

* NFR-12: System must not crash if external APIs are unavailable
* NFR-13: System must gracefully handle missing race data

---

### 5.6 Maintainability

* NFR-14: Codebase must follow modular architecture
* NFR-15: Services must be independently testable

---

### 5.7 Portability

* NFR-16: Application must run on Windows and Linux
* NFR-17: Application must run independent of cloud services

---

## 6. **External Interface Requirements**

---

### 6.1 User Interface (UI)

* Web-based dashboard
* Timing tower
* Track map visualization
* Strategy timeline
* Probability panel
* Chat panel

---

### 6.2 API Interfaces

| Endpoint                     | Purpose                   |
| ---------------------------- | ------------------------- |
| `/api/race/{id}/state`       | Get race state at lap     |
| `/api/race/{id}/strategy`    | Get strategy data         |
| `/api/race/{id}/predictions` | Get probabilities         |
| `/api/season/standings`      | Get standings             |
| `/api/whatif/simulate`       | Simulate what-if scenario |
| `/api/chat`                  | Chatbot interaction       |

---

### 6.3 Software Interfaces

* OpenF1 API (optional)
* FastF1 Python library
* LLM APIs (Gemini/OpenAI)

---

## 7. **Data Requirements**

### 7.1 Input Data

* Lap times
* Driver positions
* Tyre compounds
* Pit stop laps
* Championship points

### 7.2 Output Data

* Race state JSON
* Prediction probabilities
* Strategy timelines
* Chatbot responses

---

## 8. **System Models**

* Client–Server Model
* Modular Service-Oriented Architecture
* ML Pipeline Architecture:

  * Data → Features → Model → Predictions

---

## 9. **Future Enhancements (Beyond Version 3)**

* Live race support (if licensed data becomes available)
* Multiplayer race simulations
* Driver behavior modeling
* Cloud-based deployment
* Mobile application version

---

## 10. **Legal & Compliance Notice**

TrackAI is an unofficial fan-made research project.
It does not claim affiliation with Formula 1, the FIA, or any Formula 1 teams.
All trademarks belong to their respective owners.

---