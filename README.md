# Kuaishou Recommender System

This project focuses on building and evaluating a recommendation system using the KuaiRec dataset, derived from the Kuaishou App, a popular short-video platform. The dataset includes comprehensive user-video interactions, enabling detailed analysis and predictive modeling.

## Project Overview

Recommender Systems (RS) are intelligent systems that help users navigate large online repositories by providing personalized recommendations. This project leverages a fully observed dataset to enhance recommendation accuracy and evaluates various neural network-based models to predict user preferences.

## Objectives

1. **Predict Watch Ratio**: Estimate how much of a video a user will watch based on various features.
2. **Predict User Preference**: Classify whether a user will like or dislike a video.
3. **Video Duration Analysis**: Determine if shorter videos are more favored than longer ones.

## Dataset Description

The dataset used in this project is fully observed, containing millions of user-video interactions with minimal missing values. It is organized into the following files:

- `big_matrix.csv`: Training data with over 12 million interactions.
- `small_matrix.csv`: Evaluation data with over 4 million interactions.
- `social_network.csv`: Social connections between users.
- `item_feat.csv`: Video metadata including tags.

### Data Quality

- **Missing Values**: Minimal missing data, only in `small_matrix.csv`.
- **Duplicated Values**: Consistent duplicates in `big_matrix.csv`.
- **Outliers**: Present in numerical features but considered informative.

## Methodology

1. **Data Preprocessing**:
   - Handle missing values and duplicates.
   - Normalize numerical features.
   - Feature engineering to create new attributes like `liked` and `friend_list_len`.

2. **Model Building**:
   - Built neural network models for both regression (predicting watch ratio) and classification (predicting likes).
   - Evaluated models using metrics like mean squared error, mean absolute error, accuracy, precision, and recall.

3. **Hypothesis Testing**:
   - Conducted statistical tests to determine user preferences for video durations.

## Key Results

1. **Regression Model**:
   - Predicting watch ratio with a mean squared error of 0.2110 and mean absolute error of 0.1274 on training data.

2. **Classification Model**:
   - Achieved an accuracy of 0.612, with high precision but lower recall, indicating a challenge with unbalanced data.

3. **Hypothesis Testing**:
   - No significant preference for shorter videos over longer ones, based on statistical tests.

## Challenges and Limitations

- **Large Dataset**: Processing millions of records posed computational challenges.
- **Cold Start Problem**: Difficulty in recommending new videos or for new users without historical data.
- **Scalability**: Real-world deployment requires advanced techniques to handle dynamic data efficiently.

## Future Work

- Enhance feature set with additional user behavior data.
- Experiment with alternative models and big data techniques for scalability.

## Repository Structure

- `notebooks/`: Contains Jupyter notebooks for data analysis and model building.
- `data/`: Raw and processed datasets used in the project.
- `reports/`: Final project report and additional documentation.

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Libraries: `numpy`, `pandas`, `matplotlib`, `tensorflow`, etc.

### Running the Project

1. Clone the repository:
2. Navigate to the project directory and install dependencies:
3. Run the Jupyter notebooks in the `notebooks/` directory to replicate the analysis.


## References

- [Microsoft Recommenders: Best Practices for Production-Ready Recommendation Systems](https://dl.acm.org/doi/abs/10.1145/3366424.3382692)
- [KuaiRec: A Fully-observed Dataset for Recommender Systems](https://arxiv.org/abs/2202.10842)
- [Recommender Systems: An Overview, Research Trends, and Future Directions](https://www.researchgate.net/publication/339172772_Recommender_Systems_An_Overview_Research_Trends_and_Future_Directions)
