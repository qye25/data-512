# Personality and Movie Preference Analysis

Data 512 Final Project
Qinglang Ye
The full report with implementation is in [`final project.ipynb`](final project.ipynb)

## Abstract

Movie recommendation systems are widely used by apps and websites, but it is challenging to predict the recommendation list for new users. This analysis aims to find out the correlation between a person’s personality traits and individual movie preference so that it can help engineers improve current recommendation algorithms. By analyzing the distributions of five critical personality traits - openness, agreeableness, emotional stability, conscientiousness, and extraversion, and the relationships between these individual personalities and movie preferences, we conclude that personality traits are highly correlated with movie ratings. And most importantly, people with different personalities have different tastes in movie categories. Thus, this analysis shows the existence of a correlation between personality and movie preference so that future machine learning based recommendation models can include personality traits as a valuable predictor. 

## Data 

### Raw Data

[Top Personality Dataset](https://www.kaggle.com/arslanali4343/top-personality-dataset)

The dataset contains two files `2018-personality-data.csv` and `2018_ratings.csv`. The personality data assessed over 1800 users’ personality traits using the Ten-item Personality Inventory (TIPI). And the rating data records user ratings of levels of diversity, popularity, and serendipity of a given list of movies. This data was originally collected for training recommendation systems based on user personality traits so it is very suitable for addressing my research goal. There is no specific license or terms of use for this dataset.

#### data/2018-personality-data.csv

| Column | Description |
|--------|-------------|
| `userid` | The hashed user_id |
| `openness` | Assessment score (from 1 to 7) assessing user tendency to prefer new experience. |
| `agreeableness` | Assessment score (from 1 to 7) assessing user tendency to be compassionate and cooperative rather than suspicious and antagonistic towards others. |
| `emotional_stability` | Assessment score (from 1 to 7) assessing user tendency to have psychological stress. |
| `conscientiousness` | Assessment score (from 1 to 7) assessing user tendency to be organized and dependable, and show self-discipline. |
| `extraversion` | Assessment score (from 1 to 7) assessing user tendency to be outgoing. |
| `assigned metric` | One of "serendipity", "popularity", "diversity", "default". |
| `assigned condition` | One of "high", "medium", "low". |
| `movie_x (x is from 1 to 12)` | The list consists of 12 movies. These fields contain the ids of the twelve movies in the list. |
| `predicted_rating_x (x is from 1 to 12)` | The predicted rating of the corresponding movie_x for the user. |
| `is_personalized` | The response of the user to the question "This list is personalized for me" (1: Strongly Disagree, 5: Strongly Agree). |
| `enjoy_watching` | The response of the user to the question "This list contains movies I think I enjoyed watching" (1: Strongly Disagree, 5: Strongly Agree). |

#### data/2018_ratings.csv

| Column | Description |
|--------|-------------|
| `userid` | The hashed user_id. |
| `movie_id` | The id of the movie that the user (corresponding to userId) rated. |
| `rating` | The user rating (from 0.5 to 5 stars). |
| `tstamp` | The time when the user rated the movie. |

### Processed Data

#### processed_data/personality per person.csv

This data is derived from the joined table of `2018-personality-data.csv` and `2018_ratings.csv`.

| Column | Description |
|--------|-------------|
| `userid`   | The hashed user_id. |
| `rating` | The average user rating (from 0.5 to 5 stars) of all movies provided to this user. |
| `openness`   | Assessment score (from 1 to 7) assessing user tendency to prefer new experience. |
| `agreeableness`  | Assessment score (from 1 to 7) assessing user tendency to be compassionate and cooperative rather than suspicious and antagonistic towards others. |
| `emotional_stability` | Assessment score (from 1 to 7) assessing user tendency to have psychological stress. |
| `conscientiousness` | Assessment score (from 1 to 7) assessing user tendency to be organized and dependable, and show self-discipline. |
| `extraversion` | Assessment score (from 1 to 7) assessing user tendency to be outgoing. |

## References

1. [Bottom-Up and Top-Down: Predicting Personality with Psycholinguistic and Language Model Features](https://github.com/yashsmehta/personality-prediction)
2. [User Personality and User Satisfaction with Recommender Systems](https://link.springer.com/article/10.1007/s10796-017-9782-y)

## License

This report is available under the [MIT License](LICENSE)