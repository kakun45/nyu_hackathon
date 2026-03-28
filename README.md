# 🕵️‍♂️ Conversational Data Investigator

A high-fidelity hackathon prototype for interrogating NYC mortgage data (HMDA) using **Gemini 2.5 Flash Lite**.

## 🌟 Features
- **Live Analyst**: Real-time typing animations for AI insights.
- **Deep Data Integration**: Cross-references borough-level summaries with a 446k record statewide dataset.
- **Dynamic Visualization**: Real-time Chart.js dashboards that update based on the borough.
- **Glassmorphism UI**: A premium, modern interface designed for high-impact demos.

## 🚀 Setup

1. **Clone the repo**
2. **Install dependencies**:
   ```bash
   pip install fastapi uvicorn requests python-dotenv
   ```
3. **Set up API Key**:
   Create a `.env` file and add:
   ```env
   GEMINI_API_KEY=your_key_here
   ```
4. **Run the server**:
   ```bash
   python -m uvicorn backend:app --reload
   ```
5. **Open the UI**:
   Open `index.html` in any modern browser.

## 📊 Data Sources
- **`data.json`**: Pre-aggregated borough summaries for Manhattan, Brooklyn, and Queens.
- **`hmda_sample.csv`**: A 5,000-row slice of the 2017 NY HMDA dataset for row-level AI context.
- **Full Dataset**: The original 446k record dataset (`hmda_2017_ny_all-records_labels.csv`) is excluded from this repo due to size (356MB). To use the full dataset, download it from HMDA and place it in the root directory.
