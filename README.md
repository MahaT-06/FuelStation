# ⛽ FuelStation: AI-Optimized Kitchen Command

A distributed, AI-driven logistics platform designed to eliminate the **"Sync Gap"** in food delivery. By utilizing a **Random Forest Regressor**, the system synchronizes kitchen preparation with real-time rider arrival times to ensure peak food freshness and zero driver idle time.

---

### 🚀 Key Features

* **Predictive AI**: Uses a Random Forest model to calculate preparation times based on item complexity and current kitchen load.
* **Real-Time Synchronization**: Monitors rider ETAs to trigger "Start Cooking" alerts only when the prep window aligns with arrival.
* **Distributed Architecture**: Features a dedicated Customer App, a Python-based AI Engine, and a live Kitchen Dashboard.

---

### 📂 Project Structure

* **/fuel-station-dash-main**: The Customer App (React/Vite) used for placing orders.
* **/FuelStationKitchenCommand**:
    * **/ai_engine**: The FastAPI backend containing the `.pkl` machine learning models and prediction logic.
    * **/src**: The Kitchen Dashboard frontend for real-time order tracking and AI alerts.

---

### 🛠️ Tech Stack

* **Frontend**: React, Vite, Tailwind CSS.
* **Backend**: Python, FastAPI, Uvicorn.
* **Machine Learning**: Scikit-Learn (Random Forest Regressor), NumPy, Pickle.

---

### 🚦 Getting Started

**1. Start the AI Engine (Backend)**
```bash
cd FuelStationKitchenCommand/ai_engine
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000
```
**2. Start the Kitchen Dashboard**
```
cd FuelStationKitchenCommand
npm install
npm run dev
```
**3. Start the Customer App**
```
cd fuel-station-dash-main
npm install
npm run dev
```
