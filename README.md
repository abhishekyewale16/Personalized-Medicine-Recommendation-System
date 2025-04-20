# Health Care Advisory System

The **Health Care Advisory System** is a Flask-based web application designed to provide health-related insights and recommendations based on user-input symptoms. It leverages machine learning models and datasets to predict potential diseases and offers suggestions for precautions, medications, diets, and workouts.

---

## Features

- **Symptom-Based Disease Prediction**: Enter symptoms to get a predicted disease.
- **Health Recommendations**:
  - Precautions to take.
  - Suggested medications.
  - Recommended diets.
  - Workout plans.
- **Interactive UI**: User-friendly interface with modals for detailed information.
- **Additional Pages**:
  - About Us
  - Contact Us


---

## Project Structure

```
ML-Project/
├── datasets/                # CSV files for symptoms, precautions, medications, etc.
├── models/                  # Pre-trained machine learning models (e.g., svc.pkl)
├── static/                  # Static assets (e.g., images, CSS, JS)
├── templates/               # HTML templates for the web pages
│   ├── index.html           # Main page
│   ├── about.html           # About Us page
│   ├── contact.html         # Contact Us page
├── main.py                  # Main Flask application
└── README.md                # Project documentation
```

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/ML-Project.git
   cd ML-Project
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure the datasets and pre-trained models are in their respective directories:
   - `datasets/` contains CSV files like `symptoms_df.csv`, `precautions_df.csv`, etc.
   - `models/` contains the `svc.pkl` file.

---

## Usage

1. Run the Flask application:
   ```bash
   python main.py
   ```

2. Open your browser and navigate to:
   ```
   http://127.0.0.1:5000/
   ```

3. Use the following routes:
   - `/` - Home page for symptom input and predictions.
   - `/about` - About Us page.
   - `/contact` - Contact Us page.
   - `/developer` - Developer Info page.
   - `/blog` - Blog page.

---

## Key Files

### `main.py`
- Implements the Flask application.
- Routes:
  - `/predict`: Handles symptom input and prediction logic.
  - `/about`, `/contact`, `/developer`, `/blog`: Render respective HTML templates.
- Functions:
  - `helper(dis)`: Fetches disease details, precautions, medications, diets, and workouts.
  - `match_user_symptoms_to_known`: Matches user symptoms to known symptoms using fuzzy matching.

### Templates
- **`index.html`**: Main page for symptom input and displaying results.
- **`about.html`**: About Us page.
- **`contact.html`**: Contact Us page.


---

## Datasets

The application uses the following datasets:
- **`symptoms_df.csv`**: Contains symptoms and their descriptions.
- **`precautions_df.csv`**: Lists precautions for diseases.
- **`medications.csv`**: Contains medications for diseases.
- **`diets.csv`**: Recommended diets for diseases.
- **`workout_df.csv`**: Suggested workouts for diseases.

---

## Technologies Used

- **Backend**: Flask
- **Frontend**: HTML
- **Machine Learning**: Pre-trained SVC model (`svc.pkl`)
- **Libraries**:
  - `numpy`
  - `pandas`
  - `rapidfuzz`
  - `pickle`

---
