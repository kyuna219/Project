# Yuna Kim | Data Science & Engineering Portfolio

Data Science graduate from Chapman University (May 2024), interested in data analytics, data engineering, and applied machine learning. This portfolio highlights projects spanning data collection, transformation, storage, modeling, automation, and visualization.

## Featured Projects

### Wi-Fi Certified Product Data Pipeline
**Data Engineering · ETL · Workflow Automation · PostgreSQL · Dashboarding**

An automated pipeline that collects Wi-Fi Certified™ product information from the [Wi-Fi Alliance](https://www.wi-fi.org/), transforms records with Python and Pandas, stores them in PostgreSQL (Neon), and presents the data in a Streamlit dashboard.

- Retrieves product certification records with pagination.
- Normalizes product attributes and extracts supported Wi-Fi standards.
- Deduplicates by certification ID (`cid`) and uses PostgreSQL UPSERTs.
- Runs weekly ingestion and monthly exports through GitHub Actions.
- Archives monthly CSV/XLSX exports in GitHub and uploads Excel backups to Google Drive.
- Provides Plotly charts, brand filtering, and XLSX downloads in Streamlit.

**Data flow:** `Wi-Fi Alliance → Python / Pandas ETL → PostgreSQL (Neon) → Streamlit / Plotly`

**Technologies:** Python, Requests, Pandas, PostgreSQL, psycopg2, Neon, GitHub Actions, Streamlit, Plotly, SQLAlchemy, Google Drive.

- [Source repository](https://github.com/kyuna219/wifi-product-pipeline)
- [Live dashboard](https://wifi-certified.streamlit.app/)

### Airline Sentiment Analysis
**Data Analytics · NLP · Machine Learning · Power BI**

Analyzed 14,640 airline-related tweets and developed classifiers to predict positive, neutral, and negative sentiment.

- Cleaned data, handled missing features, and encoded airline categories.
- Used TextBlob to derive polarity and subjectivity features.
- Explored sentiment distributions, airline feedback, and common complaints.
- Trained Logistic Regression, Decision Tree, and Random Forest models.
- Tuned Decision Tree and Random Forest with GridSearchCV.
- Evaluated accuracy, confusion matrices, and classification metrics.
- Presented findings in Power BI.

**Best model:** Tuned Random Forest — **67.4% test accuracy**.

| Model | Before tuning | After tuning |
|---|---:|---:|
| Logistic Regression | 63.8% | 63.8% |
| Decision Tree | 57.7% | 66.7% |
| Random Forest | 63.2% | **67.4%** |

**Technologies:** Python, Pandas, scikit-learn, TextBlob, GridSearchCV, Power BI.

- [Project folder](https://github.com/kyuna219/Project/tree/main/airline-sentiment-analysis)
- [Power BI dashboard](https://app.powerbi.com/view?r=eyJrIjoiYmVlOWI4NjgtNjM4Zi00ZDkwLWE3ZmEtNDRiYThiZTA3OTUwIiwidCI6IjgwOTkyOWFmLTJkMjUtNDViZi05ODM3LTA4OWViOWNmYmQwMSIsImMiOjZ9)

## Technical Skills

| Area | Technologies |
|---|---|
| Programming | Python, SQL |
| Data processing | Pandas, Requests |
| Databases | PostgreSQL, MySQL, MongoDB, SQLite |
| Machine learning | scikit-learn, model evaluation, hyperparameter tuning |
| NLP | TextBlob, sentiment analysis |
| Visualization | Power BI, Streamlit, Plotly |
| Automation & cloud | GitHub Actions, Neon, Google Drive API |
| Development | Git, GitHub, Jupyter Notebook |

## Repository Structure

```text
Project/
├── airline-sentiment-analysis/
├── wifi-product-pipeline/        # Git submodule
├── .gitmodules
└── README.md
```

Clone with the Wi-Fi pipeline submodule:

```bash
git clone --recurse-submodules https://github.com/kyuna219/Project.git
```

Or initialize submodules after cloning:

```bash
git submodule update --init --recursive
```

## About Me

**Yuna Kim** · B.S. in Data Science, Chapman University (May 2024)

- [GitHub](https://github.com/kyuna219)
- [LinkedIn](https://www.linkedin.com/in/yuna-kim-/)

Thanks for visiting!
 
