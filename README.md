# Movie Rating Prediction with Python

This project is part of my **Data Science Internship at CodSoft**. The goal is to build a machine learning model that predicts the rating of a movie based on features like genre, director, and actors using regression techniques.

---

## Project Overview

The `IMDb Movies India.csv` dataset provides a historical look at the Indian film industry. By analyzing this data, I developed a model that estimates the ratings users or critics might give to a movie.

This project explores the entire **data science pipeline**:

- **Data Cleaning**: Handling missing values and formatting inconsistencies
- **EDA (Exploratory Data Analysis)**: Visualizing trends in ratings and movie durations
- **Feature Engineering**: Converting categorical variables (Directors, Actors) into numerical insights via Target Encoding
- **Machine Learning**: Implementing and comparing Linear Regression and Random Forest models

---

## Technologies Used

| Tool/Library | Purpose |
|--------------|---------|
| **Python** | Core programming language |
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical operations |
| **Matplotlib & Seaborn** | Data visualization |
| **Scikit-Learn** | Machine learning modeling |

---

## Dataset

The project utilizes the **`IMDb Movies India.csv`** file.

### Features:
- `Name` - Movie title
- `Year` - Release year
- `Duration` - Movie length in minutes
- `Genre` - Movie category (Drama, Comedy, Action, etc.)
- `Rating` - IMDb rating (target variable)
- `Votes` - Number of user votes
- `Director` - Director's name
- `Actor 1`, `Actor 2`, `Actor 3` - Lead actors

### Target Variable:
- **`Rating`** (Continuous numerical value from ~1.0 to 10.0)

---

## Key Steps in the Workflow

### Preprocessing
- Removed string characters from `Year` and `Duration` columns
- Converted columns to proper numeric formats
- Handled missing values in `Votes` and `Rating` columns

### Encoding
- Used **Target Encoding** for high-cardinality features (`Director`, `Actor 1`, `Actor 2`, `Actor 3`)
- This replaces each name with the average rating associated with that individual, providing the model with historical performance data

### Exploratory Data Analysis (EDA)
- Distribution analysis of movie ratings
- Trends in ratings over the years
- Genre popularity and rating correlations
- Duration vs. rating relationships

### Model Building
- **Linear Regression**: Served as the baseline model
- **Random Forest Regressor**: Provided better accuracy by capturing non-linear relationships

---

## Results

| Model | Performance |
|-------|-------------|
| Linear Regression | Baseline model |
| Random Forest Regressor | ✅ Better accuracy |

### Key Insight
The Random Forest model identified **Votes** (and/or Director_encoded) as the most significant factor in predicting a movie's rating. Movies with more votes tend to have more stable and reliable ratings.
