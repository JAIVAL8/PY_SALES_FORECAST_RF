# PY_SALES_FORECAST_RF

This project forecasts daily sales for specific food items using historical sales data, holiday information, and weather data. It leverages machine learning (XGBoost) and external APIs for feature enrichment.

## Features

- **Sales Forecasting:** Predicts daily sales for a selected dish.
- **Holiday Integration:** Fetches national holidays using the Calendarific API.
- **Weather Integration:** Retrieves historical weather data from the Open-Meteo API.
- **Feature Engineering:** Includes lag features, rolling averages, holiday flags, and weather encoding.
- **Modeling:** Uses XGBoost regression for forecasting.

## Project Structure

```
.
├── app.ipynb                 # Main Jupyter notebook for data processing and modeling
├── .env                      # Environment variables (not included in version control)
├── Sales Dataset OG.xlsx     # Sales data (Excel)
├── calendarific.json         # (Optional) Cached holiday data
├── open_meteo_weather.json   # (Optional) Cached weather data
└── readme.md                 # Project documentation
```

## Setup

1. **Clone the repository** and navigate to the project folder.

2. **Install dependencies:**

   ```bash
   pip install pandas numpy scikit-learn xgboost matplotlib python-dotenv requests openpyxl
   ```

3. **Configure environment variables:**

   - Create a `.env` file in the project root.
   - Add your API keys, location, and other configuration values as environment variables.
   - **Do not share or commit your `.env` file.**

4. **Prepare your sales data:**
   - Place your sales Excel file (e.g., `Sales Dataset OG.xlsx`) in the project folder.
   - Ensure it has columns like `Food Name`, `System Date`, and `Quantity`.

## Usage

- Open `app.ipynb` in Jupyter or VS Code.
- Run the notebook cells step by step.
- The notebook will:
  - Load environment variables.
  - Fetch and process holiday and weather data.
  - Engineer features and train the model.
  - Output model performance and sales forecast plots.

## Notes

- **API Keys:** You need a valid Calendarific API key. Register at [calendarific.com](https://calendarific.com/) if you don't have one.
- **Weather API:** Uses Open-Meteo, which does not require an API key.
- **.env Security:** Keep your `.env` file private and never commit it to public repositories.

## Example Output

- Model performance metrics (MAE, R²)
- Forecast vs. actual sales plot for the selected dish

---
