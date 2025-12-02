# TrackAI – Project Roadmap

This document outlines the **planned development roadmap for the TrackAI project**, from the initial MVP to the advanced AI-driven research platform.

TrackAI is developed in **incremental, versioned phases** to ensure:
- Stable architectural growth
- Clear research milestones
- Progressive learning & feature expansion

---

## ✅ Version 1 – MVP (Foundation Stage)

**Status:** Completed / In Development  
**Goal:** Establish core system architecture and basic race visualization.

### Objectives
- Prove technical feasibility
- Validate frontend–backend communication
- Implement basic race replay & prediction

### Features
- Single-race replay from historical data
- Timing tower with live-style position updates
- Driver gaps and intervals
- Simple animated track map
- Basic race win probability calculation
- Manual data loading (local files)
- REST API-based frontend–backend communication

### Technical Milestones
- Next.js frontend setup
- FastAPI backend setup
- Local SQLite/JSON data access
- Base project structure
- Version-specific documentation (`Version_1_MVP/README.md`)

### Out of Scope (V1)
- No chatbot
- No season analytics
- No what-if simulation
- No machine learning models

---

## 🔄 Version 2 – Strategy & Season Intelligence

**Status:** Planned  
**Goal:** Introduce strategic analysis and season-level intelligence.

### Key Enhancements
- Multi-race and season support
- Driver & constructor standings
- Points progression and performance charts
- Detailed pit stop & tyre stint timelines
- Improved rules-based probability engine
- Basic AI chatbot for race & season queries

### New System Capabilities
- Strategy analysis layer
- Season analytics APIs
- Natural language query support via LLM
- Data ingestion & caching pipeline

### Technical Focus
- pandas-based data processing
- Multi-race database support
- Chatbot API integration (Gemini/OpenAI)
- Modular backend services

### Risks & Research Challenges
- Strategy modeling accuracy
- Safe and correct use of external LLM APIs
- Efficient handling of multi-race datasets

---

## 🚀 Version 3 – AI & What-If Simulation Platform

**Status:** Planned (Advanced Research Phase)  
**Goal:** Transform TrackAI into a full-featured **AI-driven prediction & simulation system**.

### Major Features
- Multi-season analytics
- Machine learning-based race & championship predictions
- Monte Carlo simulation engine
- Interactive **what-if strategy simulation**
- Advanced AI chatbot with model interpretation
- Track- and tyre-specific performance modeling

### New Capabilities
- Feature engineering for ML models
- Offline model training pipeline
- Model persistence & reuse
- Strategy scenario re-simulation
- Model explainability via chatbot

### Technical Focus
- scikit-learn / XGBoost models
- Simulation-based probability estimation
- Background model training scripts
- Advanced visualization dashboards

### Research Value
- Probabilistic modeling of race outcomes
- Strategy optimization under uncertainty
- Human-AI interaction for motorsport analysis

---

## 🧭 Long-Term Vision (Post V3)

These are **future research/extensions** beyond the current academic scope:

- Real-time live race integration (only with licensed data)
- Cloud-based deployment
- Collaborative multi-user simulations
- Driver behavior modeling
- Reinforcement learning for pit stop optimization
- Mobile application

---

## 📌 Documentation & Governance

- **Root README:** High-level overview & legal notice
- **Version READMEs:** Detailed setup & usage per version
- **SRS.md:** Formal system specification
- **ROADMAP.md:** This file (development planning)
- **LICENSE.txt:** MIT License

---

## ⚠️ Legal & Compliance Note

TrackAI is:
- Unofficial
- Non-commercial
- Academic & research-oriented
- Not affiliated with Formula 1 or FIA
- Free of proprietary branding and licensed data

All roadmap milestones are subject to:
- Data availability
- API policy changes
- Research feasibility

---

> TrackAI is developed as a **progressive engineering and AI research platform**, with each version designed as a standalone, well-documented academic milestone.