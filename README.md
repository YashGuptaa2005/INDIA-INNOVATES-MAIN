# AI Flood Prediction Dashboard

A full-stack ML application that predicts flood risk across Indian districts using rainfall, elevation, and historical data, combined with a Streamlit dashboard for visualization and decision support.

---

## What It Does

Get flood predictions and insights:

* *"Will this district face flood risk?"*
* *"What is the predicted flood severity?"*
* *"What factors contributed to this prediction?"*
* *"What actions can be taken to prevent damage?"*

The system combines:

1. **Machine Learning model** trained on historical flood and environmental data
2. **Geographical features** (elevation, rainfall patterns)
3. **District-level datasets** across India
4. **Interactive dashboard** for visualization and suggestions

Returns flood predictions along with insights and control suggestions.

---

## Architecture Overview

```
User interacts with dashboard
              ↓
    ┌─────────────────────┐
    │   Input Data (CSV)  │  ← Rainfall + Elevation datasets
    └────────┬────────────┘
             ↓
    ┌─────────────────────┐
    │ Feature Processing  │  ← Cleaning + transformation
    └────────┬────────────┘
             ↓
    ┌─────────────────────┐
    │  ML Model (Pickle)  │  ← Predict flood risk
    └────────┬────────────┘
             ↓
    ┌─────────────────────┐
    │ Predictions Output  │  ← Risk level + probability
    └────────┬────────────┘
             ↓
    ┌─────────────────────┐
    │ Streamlit Dashboard │  ← Visualization + suggestions
    └─────────────────────┘
```

---

## Tech Stack

| Layer                          | Technology                  |
| ------------------------------ | --------------------------- |
| **Frontend**                   | Streamlit                   |
| **Backend**                    | Python                      |
| **ML Model**                   | Scikit-learn (Pickle Model) |
| **Data Processing**            | pandas, numpy               |
| **Visualization**              | matplotlib                  |
| **Computer Vision (optional)** | OpenCV                      |
| **Deployment**                 | Streamlit Cloud             |

---

## Features Used

The model uses environmental and geographical features:

| Category             | Features                        |
| -------------------- | ------------------------------- |
| **Rainfall Data**    | District-wise rainfall patterns |
| **Elevation Data**   | Terrain height and slope        |
| **Historical Data**  | Flood occurrence records        |
| **Derived Features** | Combined rain-elevation metrics |

---

## Project Structure

```
INDIA-INNOVATES-MAIN/
├── India-Innovates-main/
│   ├── app.py                    # Streamlit dashboard
│   ├── main.py                  # Core logic
│   ├── predict_new_data.py      # Prediction script
│   ├── requirements.txt         # Dependencies
│   │
│   ├── elevation_folder/        # Elevation datasets
│   ├── rainfall_folder/         # Rainfall datasets
│   │
│   ├── flood_model.pkl          # Trained ML model
│   ├── scaler.pkl               # Data scaler
│   │
│   ├── static/
│   │   └── styles.css           # UI styling
│   │
│   └── CSV/XLSX datasets
```

---

## Setup & Installation

### Prerequisites

* Python 3.10+
* pip installed

---

### Local Setup

#### 1. Clone the repository

```bash
git clone https://github.com/YashGuptaa2005/INDIA-INNOVATES-MAIN.git
cd INDIA-INNOVATES-MAIN/India-Innovates-main
```

---

#### 2. Create and activate virtual environment

```bash
python -m venv venv
venv\Scripts\activate
```

---

#### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

#### 4. Run the application

```bash
streamlit run app.py
```

App runs at: `http://localhost:8501`

---

## Model Details

* **Type**: Classification Model
* **Input**: Rainfall + Elevation features
* **Output**: Flood Risk Prediction
* **Storage**: `.pkl` files (model + scaler)

---

## UI Overview

The dashboard provides:

* 📊 Flood prediction results
* 📍 District-wise analysis
* 📈 Data visualization
* 💡 Preventive suggestions

---

## Notes

* Dataset-driven predictions (no real-time API yet)
* Model accuracy depends on training data quality
* Designed for research and educational use

---

## Future Improvements

* Integration with real-time weather APIs
* GIS-based map visualization
* Deep learning model for improved accuracy
* Mobile-friendly UI

---

## Disclaimer

This project is for educational and research purposes only. Flood prediction depends on multiple real-world factors and may not always be accurate. Use results as guidance, not as a definitive decision-making tool.

---
