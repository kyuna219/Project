# Airline Sentiment Analysis

A machine learning and data analytics project exploring airline customer feedback from Twitter. The project uses text-derived features and classification models to predict positive, neutral, or negative sentiment.

## Project Overview

- **Dataset:** 14,640 tweets
- **Target:** `airline_sentiment` (positive, neutral, negative)
- **Project period:** March–April 2024
- **Course:** MGSC 410, Chapman University
- **Best model:** Tuned Random Forest
- **Best test accuracy:** **67.4%**

## Workflow

1. Prepare and clean the tweet dataset.
2. Explore sentiment patterns across airlines and complaint themes.
3. Engineer text-derived and time-based features.
4. Train baseline classification models.
5. Tune selected models with GridSearchCV.
6. Evaluate model performance and feature importance.
7. Present findings through charts and a Power BI dashboard.

## Data Preparation & Feature Engineering

The documented preparation steps include:

- Removing features with more than 30% missing values.
- One-hot encoding the `airline` variable.
- Converting `tweet_created` into numeric date and time features.
- Applying TextBlob to calculate:
  - **Polarity:** direction and strength of sentiment.
  - **Subjectivity:** how subjective or opinion-based the text is.

The documented predictors are `date`, `time`, `airline`, `polarity`, and `subjectivity`; the target is `airline_sentiment`.

## Exploratory Data Analysis

Findings documented in the project:

- Negative sentiment is the largest sentiment group.
- United Airlines has the highest volume of negative tweets in this dataset.
- Poor customer service is a frequent complaint theme.

![Sentiment distribution](results/exploratory-analysis-1.png)

![Negative tweets by airline](results/exploratory-analysis-2.png)

![Common complaint themes](results/exploratory-analysis-3.png)

## Modeling

Models compared:

- Logistic Regression
- Decision Tree
- Random Forest

GridSearchCV was used to tune the Decision Tree and Random Forest models.

| Model | Test accuracy before tuning | Test accuracy after tuning |
|---|---:|---:|
| Logistic Regression | 63.8% | 63.8% |
| Decision Tree | 57.7% | 66.7% |
| Random Forest | 63.2% | **67.4%** |

The tuned Random Forest achieved the highest test accuracy. Its training accuracy was 72.0%, compared with 67.4% on the test set.

## Evaluation

The selected Random Forest model was evaluated using accuracy, a confusion matrix, and classification metrics.

- Negative tweets were classified most successfully.
- Neutral tweets were the most difficult category, with lower precision/recall than the other classes.

![Confusion matrix](results/confusion-metrics.png)

![Classification metrics](results/classification-metrics.png)

## Feature Importance

The three most important features in the Random Forest model were:

1. Polarity
2. Time of tweet
3. Subjectivity

![Feature importance](results/feature-importance.png)

## Key Takeaways

- Tuned Random Forest performed best, with 67.4% test accuracy.
- TextBlob polarity and subjectivity, together with tweet timing, were useful predictive features.
- Neutral sentiment was comparatively difficult to classify, leaving room to improve feature representation and class-level performance.

Accuracy is a summary metric; class-level evaluation matters because performance differs across sentiment categories.

## Future Improvements

- Compare TextBlob features with TF-IDF, n-grams, or transformer embeddings.
- Investigate class imbalance and evaluate resampling or class-weighting.
- Add cross-validation and further error analysis by airline and sentiment.
- Explore deployment through a lightweight API or interactive application.

## Project Structure

```text
airline-sentiment-analysis/
├── data/         # Dataset (Tweets.csv)
├── notebooks/    # Jupyter notebooks for EDA and modeling
├── results/      # Charts and evaluation visuals
├── docs/         # Presentation and appendix files
├── misc/         # Supporting files
└── README.md
```

## Dashboard

[Open the Power BI dashboard](https://app.powerbi.com/view?r=eyJrIjoiYmVlOWI4NjgtNjM4Zi00ZDkwLWE3ZmEtNDRiYThiZTA3OTUwIiwidCI6IjgwOTkyOWFmLTJkMjUtNDViZi05ODM3LTA4OWViOWNmYmQwMSIsImMiOjZ9).

## Tools

Python, Pandas, TextBlob, scikit-learn, GridSearchCV, Power BI.

## Author

**Yuna Kim**

- [GitHub](https://github.com/kyuna219)
- [LinkedIn](https://www.linkedin.com/in/yuna-kim-/)

*This project was originally completed as a course project. Findings reflect the supplied course dataset and should be interpreted within that context.*
