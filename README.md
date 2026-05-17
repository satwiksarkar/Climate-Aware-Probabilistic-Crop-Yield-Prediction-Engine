# 🌾 Climate-Aware Probabilistic Crop Yield Prediction Engine

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.0.3-black?logo=flask&logoColor=white)
![Google Gemini](https://img.shields.io/badge/AI-Google_Gemini-orange?logo=google&logoColor=white)

A comprehensive, climate-aware web application designed to empower farmers and agricultural researchers with highly accurate, probabilistic crop yield predictions, weather forecasts, and AI-driven agronomic strategies.

## ✨ Key Features

- **Probabilistic Crop Yield Prediction**: Leverages an integrated Machine Learning model (NGBoost/Scikit-Learn) to provide not just the expected crop yield, but also the confidence interval (risk assessment).
- **Climate & Weather Forecasting**: Utilizes Facebook's **Prophet** to analyze historical weather data and generate daily and monthly forecasts for temperature, rainfall, humidity, and wind speed.
- **AI Agronomist Roadmap**: Integrates **Google Gemini GenAI** to automatically generate a tailored, phase-by-phase agronomic strategy complete with cost estimates and risk assessments based on location and crop predictions.
- **Location-Aware Context**: Uses **Geopy** for reverse geocoding to automatically resolve geographical coordinates into state and district levels for precise regional predictions.
- **Visual Analytics & Reporting**: Generates dynamic probability distribution graphs for crop yields and exports comprehensive PDF reports for offline use.
- **Secure Authentication**: Integrated Google OAuth login via Flask-Dance.

## 🛠️ Technology Stack

- **Backend**: Python, Flask
- **Machine Learning**: Prophet (Time-series forecasting), Joblib (Model loading), Pandas, NumPy, SciPy
- **AI Integration**: Google Generative AI (Gemini 2.5)
- **Data Visualization**: Matplotlib
- **Geospatial & Mapping**: Geopy, Nominatim
- **PDF Generation**: fpdf2, reportlab
- **Authentication**: Flask-Dance (Google OAuth)

## 📁 Project Structure

```
├── app.py                  # Main Flask application entry point
├── auth/                   # Authentication blueprint (Google OAuth)
├── dashboard/              # User dashboard UI and logic
├── showYield/              # ML yield prediction & AI roadmap generation
├── services/
│   └── weatherpredict/     # Prophet-based weather forecasting engine
├── static/                 # CSS, JS, Images, and generated graphs
├── templates/              # Global HTML templates
├── createpdf.py            # PDF report generation utility
└── requirements.txt        # Python dependencies
```

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- A Google Gemini API Key
- Google OAuth 2.0 Client Credentials (for authentication)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/satwiksarkar/Climate-Aware-Probabilistic-Crop-Yield-Prediction-Engine.git
   cd Climate-Aware-Probabilistic-Crop-Yield-Prediction-Engine
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Configuration:**
   Create a `.env` file in the root directory and add your API keys:
   ```env
   GEMINI_API_KEY=your_gemini_api_key_here
   GOOGLE_OAUTH_CLIENT_ID=your_oauth_client_id_here
   GOOGLE_OAUTH_CLIENT_SECRET=your_oauth_client_secret_here
   ```

### Running the Application

Start the Flask development server:
```bash
python app.py
```
The application will be available at `http://localhost:5000` or `http://0.0.0.0:5000`.

## 📈 ML Models Setup
The crop prediction engine relies on an integrated model (`wheat_integrated_v2.pkl`). Ensure this file is present in the `showYield/` directory for the prediction service to function correctly.

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/satwiksarkar/Climate-Aware-Probabilistic-Crop-Yield-Prediction-Engine/issues).

## 📄 License
This project is licensed under the MIT License.