# Big Data Movie Recommendation System Using PySpark

This project presents a scalable and efficient **Movie Recommendation System** built using **Apache Spark (PySpark)** and the **MovieLens 20M** dataset. Unlike traditional approaches, this system leverages **Big Data technologies** for distributed processing and machine learning, making it suitable for real-world, large-scale deployments.

---

## Project Highlights

- **Big Data Pipeline**: Built entirely on **PySpark**, ensuring fast, distributed data processing.
- **Data Analysis at Scale**: Over **20 million ratings** across **27,000 movies**.
- **ALS-based Recommendation Engine**: Implements Spark MLlib's **Alternating Least Squares (ALS)** algorithm with hyperparameter tuning.
- **Insightful Visualizations**: Genre trends, time-based activity plots, rating distributions, and more.
- **Personalized Predictions**: Model adapts to user-specific ratings for tailored movie recommendations.

---

## Dataset: MovieLens 20M

> Provided by GroupLens Research, this dataset includes:
- `ratings.csv`: 20M user-movie ratings with timestamps.
- `movies.csv`: Movie titles and genres for ~27,000 films.

📎 [Dataset Source](https://grouplens.org/datasets/movielens/20m/)

---

## Core Workflow

### 1. **Data Loading & Exploration**
- Schema inference and validation via `SparkSession`
- Initial profiling: movie counts, ratings distribution, genre breakdown

### 2. **Exploratory Data Analysis (EDA)**
- Top-rated and most-rated movies
- Genre-wise trends
- Monthly user activity trends
- Correlation between number of ratings and average rating

### 3. **Modeling: ALS in PySpark**
- Dataset split into **train**, **validation**, and **test**
- Tuning ALS `rank` and `regParam`
- Evaluation using:
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Error (MAE)
  - Accuracy based on normalized MAE

### 4. **Personalized Recommendations**
- Accepts custom user ratings
- Predicts top movie recommendations for unrated items

---

## Model Performance

| Metric      | Value     |
|-------------|-----------|
| **Best RMSE**   | 0.8149    |
| **Best MAE**    | 0.6324    |
| **Accuracy**    | ~87.35%   |

Rank = 8 yielded the best performance.

---

## Visual Insights

- Ratings distribution and popularity
- Time-series trend of rating activity
- Average rating by genre
- Rating frequency vs average score (Hexbin)
- Boxplots of ratings vs rating counts

All visualizations are rendered using `matplotlib` and `seaborn`.

---

## Future Enhancements

- Integrate **real-time streaming** with Apache Kafka and Spark Streaming
- Extend to **hybrid filtering** combining content + collaborative models
- Build an interactive **web interface** using Streamlit or Flask
- Deploy as **cloud-native Spark application** on AWS EMR or GCP Dataproc


