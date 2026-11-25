# 🌍 5-Satellite 7-Day Latitude & Longitude Ground-Track Calculator

An interactive ground-track calculation tool I built in Google Colab using `Skyfield`, `Pandas`, and `Gradio` to track **Intelsat**, **Eutelsat**, **Starlink**, **Qianfan**, and **Kuiper** across the next 7 days (168 hours) and output their subpoint latitude, longitude, and altitude schedule in UTC.

## ✨ Key Features
- **5-Slot Communications Satellite Setup:** Dedicated input slots for **Intelsat**, **Eutelsat**, **Starlink**, **Qianfan**, and **Kuiper** with live readiness status (`0/5` up to `5/5`).
- **Complete-Set Gate:** Waits until all 5 satellite TLE slots have valid Line 1 and Line 2 entries before computing the 7-day schedule.
- **7-Day Subpoint Ground-Track Schedule:** Propagates each satellite forward for 7 days in configurable time steps (15, 30, 60, or 120 minutes) using `Skyfield` and exports a `Pandas` table of UTC timestamps, latitudes, longitudes, and altitudes.
- **Summary Cards:** Displays latitude span, longitude span, sampling step, and total computed rows in a dark-mode dashboard.

## 🛠️ Tech Stack
- **Environment:** Google Colab
- **Orbital Propagation, Data & UI:** Python, `Skyfield`, `Pandas`, `Gradio`

## ⚙️ How to Run the Project
1. **Open in Google Colab:**
   - Upload the notebook or script to Google Colab (`colab.research.google.com`).
2. **Run & Launch:**
   - Run the cell to install `skyfield`, `gradio`, and `pandas` and launch the Gradio interface.
3. **Paste 5 TLEs & Compute:**
   - Paste valid TLE blocks for **Intelsat**, **Eutelsat**, **Starlink**, **Qianfan**, and **Kuiper**, choose the sampling step, and click **Compute 7-Day Lat/Lon Track (All 5)**.

## 📌 Scope & Assumptions
- Intended for exploratory 7-day ground-track visualization and comparative analysis from user-supplied TLE data, not operational mission planning or collision avoidance.
- Uses SGP4/Skyfield propagation from the pasted TLE epochs over a 7-day UTC window starting at execution time.
