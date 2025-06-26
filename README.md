# 🏆 PL-Predictor

This project leverages historical English Premier League match data to predict whether a team will win a match using a machine learning model.

## 📂 Project Overview

Using a dataset of football matches, the project performs the following steps:

- Preprocesses match data (including encoding categorical features).
- Extracts time-based features such as match hour and day of the week.
- Trains a **Random Forest Classifier** on pre-2022 data to predict match outcomes.
- Tests and evaluates the model on 2022 and later matches.

## 🔍 Dataset

The dataset used (`matches.csv`) includes fields such as:
- `team`, `opponent`
- `date`, `venue`, `result`, `time`
- Feature-engineered columns like:
  - `venue_code`, `opp_code`, `hour`, `day_code`
  - Target column: `target` (1 = Win, 0 = Not Win)

## ⚙️ Model

- **Model**: `RandomForestClassifier`
- **Features Used**:
  - `venue_code`: Encoded venue (Home/Away)
  - `opp_code`: Encoded opponent team
  - `hour`: Match start hour
  - `day_code`: Day of the week

## 🧪 Training & Testing

- **Training Data**: Matches before 2022
- **Testing Data**: Matches in 2022 and beyond

## 📈 Evaluation

The notebook outputs:
- Prediction results
- Probability estimates for match outcomes
- Model accuracy (if included in future updates)

## 📦 Dependencies

```bash
pandas
scikit-learn
requests
beautifulsoup4
numpy
```

You can install them with:

```bash
pip install pandas requests beautifulsoup4 scikit-learn numpy
```

## 🚀 How to Run

1. Place `matches.csv` in the same directory as the notebook.
2. Open and run `prediction.ipynb` using Jupyter Notebook or VS Code.
3. Modify the model or features as needed for improved performance.

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
