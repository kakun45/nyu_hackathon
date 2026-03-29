# 🕵️‍♂️ Conversational Data Investigator

A high-fidelity hackathon prototype for interrogating NYC mortgage data (HMDA) using **Gemini 2.5 Flash Lite**.

Make your interrogation happened, sample questions:
"Are mortgage approvals fair in this borough?" or "Why is there disparity?" "I'm Black; what can I do to increase my chances for a mortgage approval in this borough?" `select from a dropdown`

<img width="1105" height="802" alt="Screenshot 2026-03-28 at 11 16 48 PM" src="https://github.com/user-attachments/assets/e34d2c46-2292-4b5c-a821-4434a6b96e72" />
<img width="1088" height="789" alt="Screenshot 2026-03-28 at 11 19 31 PM" src="https://github.com/user-attachments/assets/462eccee-3783-4df3-ba7d-ddf3d8bf8c5a" />

## 🌟 Features
- **Live Analyst**: Real-time typing animations for AI insights.
- **Deep Data Integration**: Cross-references borough-level summaries with a 446k record statewide dataset.
- **Dynamic Visualization**: Real-time Chart.js dashboards that update based on the borough.
- **Glassmorphism UI**: A premium, modern interface designed for high-impact demos.
- **30-row cut out**: Statistically focused state. Using the first 30 rows of 2017 NY HMDA dataset to provide concrete examples during demo. Reason: the project is now lightweight, portable, and respects GitHub's file size limits, and saves on tokens. The limit that is easy to remove.

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
   pyenv shell <nyu_hackathon>
   python -m uvicorn backend:app --reload
   ```
5. **Open the UI**:
   Open `index.html` in any modern browser.

## 📊 Data Sources
- **`data.json`**: Pre-aggregated borough summaries for Manhattan, Brooklyn, and Queens.
- **`hmda_sample.csv`**: A 5,000-row slice of the 2017 NY HMDA dataset for row-level AI context.
- **Full Dataset**: The original 446k record dataset (`hmda_2017_ny_all-records_labels.csv`) is excluded from this repo due to size (356MB). To use the full dataset, [download](https://www.consumerfinance.gov/data-research/hmda/historic-data/?geo=ny&records=all-records&field_descriptions=labels) it from HMDA and place it in the root directory.
