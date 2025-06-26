# 🏆 PL-Predictor

This project leverages historical English Premier League match data to predict whether a team will win a match using a machine learning model.

## 📂 Project Overview

Using a dataset of football matches, the project performs the following steps:

- Preprocesses match data (including encoding categorical features).
- Extracts time-based and performance-based features.
- Trains a **Random Forest Classifier** on pre-2022 data to predict match outcomes.
- Tests and evaluates the model on 2022 and later matches.

## 🔍 Dataset

The dataset used (`matches.csv`) includes:

- Team-based match metadata (venue, opponent, time, result).
- Statistical features engineered from historical match performance.

## 🎯 Feature Descriptions

| Feature Variable Name | Description |
|------------------------|-------------|
| `venue_code`           | Encoded venue (Home/Away/Neutral) |
| `opp_code`             | Encoded opponent team |
| `hour`                 | Match start hour |
| `day_code`             | Day of the week (0=Monday, 6=Sunday) |
| `gf_rolling`           | Rolling average of goals for (last 3 matches) |
| `ga_rolling`           | Rolling average of goals against (last 3 matches) |
| `sh_rolling`           | Rolling average of shots (last 3 matches) |
| `sot_rolling`          | Rolling average of shots on target (last 3 matches) |
| `dist_rolling`         | Rolling average of distance covered (last 3 matches) |
| `fk_rolling`           | Rolling average of free kicks (last 3 matches) |
| `pk_rolling`           | Rolling average of penalties scored (last 3 matches) |
| `pkatt_rolling`        | Rolling average of penalties attempted (last 3 matches) |
| `recent_points`        | Points earned in last 5 matches |
| `home_win_rate`        | Home win rate in last 10 home games |
| `away_win_rate`        | Away win rate in last 10 away games |
| `h2h_win_rate`         | Win rate vs opponent in last 5 meetings |
| `gd_rolling`           | Rolling average of goal difference (last 3 matches) |

## ⚙️ Model

- **Model**: `RandomForestClassifier`
- **Features Used**: All of the above

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
numpy
requests
beautifulsoup4

```

You can install them with:

```bash
pip install pandas requests beautifulsoup4 scikit-learn
```

## 🚀 How to Run

1. Place `matches.csv` in the same directory as the notebook.
2. Open and run `prediction.ipynb` using Jupyter Notebook or VS Code.
3. Modify the model or features as needed for improved performance.


