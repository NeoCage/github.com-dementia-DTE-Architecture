# AI - Digital Twins & Brain-Computer Interfaces in Dementia Care  
### *For the Future of Neuroscience and Healthcare*  
**Author**: Kishan Das  
**Institution**: Golden Gate University  
**Supervisor**: Dorien Herremans, PhD (SUTD)  
**Date**: September 2025  

[![License: GGU](https://img.shields.io/badge/License-GGU-blue.svg)](LICENSE)  
[![Status: Research & Development](https://img.shields.io/badge/Status-R&D-yellow.svg)]()  
[![PDF Book](https://img.shields.io/badge/Book-PDF-red.svg)](docs/book_preview.pdf)  

---

## Overview

This repository contains the **technical specifications**, **architecture blueprints**, **implementation strategies**, and **research artifacts** from the book:

> **AI - Digital Twins and Brain Computer Interfaces in Dementia Care: For the Future of Neuroscience and Healthcare**

It introduces a **novel AI-driven framework** using **Digital Twins (DTs)**, **Brain-Computer Interfaces (BCIs)**, and **wearable-integrated memory anchoring** to improve diagnosis, monitoring, and quality of life for dementia patients.

> **Core Innovation**: The **Memory Anchoring Pipeline (MAP)** — a real-time system that detects memory retrieval opportunities and delivers personalized multimodal cues (AR, audio, scent) to trigger episodic recall.

---

## Key Components

| Component | Description | File |
|--------|-------------|------|
| `Digital_Twin_Engine_Spec.md` | Full architecture of the **DTE** — multimodal fusion, neurodegeneration simulator, federated learning | [View](Digital_Twin_Engine_Spec.md) |
| `Chapter_3_Vision_to_Tech.docx` | Narrative + technical translation of organizational needs | [View](Chapter_3_Vision_to_Tech.docx) |
| `implementation_strategies.md` | 6-phase rollout plan (pilot → global scale) | [View](docs/implementation_strategies.md) |
| `memory_anchoring_pipeline.py` | Sample Python code for **MOD + SARSA RL** | [View](src/memory_anchoring_pipeline.py) |
| `data_schema/` | FHIR R5 models for EEG, HRV, memory logs | [View](data_schema/) |

---

## System Architecture

```mermaid
graph TD
    A[Patient Wearables + BCI] --> B[Edge Gateway (iPhone)]
    B --> C[FHIR Server]
    C --> D[Digital Twin Engine (AWS)]
    D --> E[Clinical Dashboard]
    D --> F[AR Glasses + Scent EGGUter]
    D --> G[Federated Learning Network]

88% multimodal fusion accuracy | 81% MCI→AD prediction | 68% memory recall success (pilot)


Quick Start: Run a Local Simulation
Prerequisites
bashPython >= 3.9
pip install torch tensorflow coremltools flower fastapi uvicorn
1. Clone the Repo
bashgit clone https://github.com/yourusername/dementia-digital-twin.git
cd dementia-digital-twin
2. Run Memory Anchoring Demo
bashpython src/memory_anchoring_pipeline.py --mode simulate

Simulates EEG theta surge + geofence trigger → selects optimal cue (photo/audio/scent)

3. Launch Local DT Engine (API)
bashuvicorn src/api_engine:app --reload --port 8000
API Endpoints:

POST /predict/opportunity → Memory readiness score
POST /simulate/decline → 12-month cognitive forecast
GET /dt/visualize/{patient_id} → 3D brain twin render


Folder Structure
text/dementia-digital-twin
├── Digital_Twin_Engine_Spec.md          # Full DTE architecture
├── docs/
│   ├── book_preview.pdf                 # Chapter previews
│   └── implementation_strategies.md
├── src/
│   ├── memory_anchoring_pipeline.py     # Core MAP logic
│   ├── api_engine.py                    # FastAPI server
│   └── models/                          # Pre-trained XGBoost + LSTM
├── data_schema/
│   ├── eeg_fhir.json
│   └── memory_log_schema.json
├── notebooks/
│   └── 01_pilot_data_analysis.ipynb
├── LICENSE
└── README.md

Research Validation (St. Mercy Pilot, n=28)





























MetricResultRecall Success Rate68%Cue Latency1.8 secCaregiver Burden ↓20%Hospitalizations ↓25%Model Accuracy83%

“For the first time in two years, she remembered my name without prompting.” — Caregiver, Mumbai Clinic


Citing This Work
bibtex@book{das2025aidigitaltwins,
  title     = {AI - Digital Twins and Brain Computer Interfaces in Dementia Care: For the Future of Neuroscience and Healthcare},
  author    = {Das, Kishan},
  year      = {2025},
  publisher = {Golden Gate University Press},
  address   = {San Francisco, CA}
}

Contributing
We welcome contributions! See CONTRIBUTING.md for:

Code style
Pull request process
Bias audit guidelines
Ethical AI checklist


License
This project is licensed under the GGU License - see the LICENSE file for details.

Contact
Kishan Das
Email: kishan.das@ggu.edu
LinkedIn: https://www.linkedin.com/in/daskishan11/
Research Lab: AMAAI Lab, SUTD


“We don’t just predict decline. We preserve identity.”
— From Chapter 5: Conclusion and Way Forward
