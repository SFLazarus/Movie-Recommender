# Movie-Recommender
Built Clustering model to design a movie recommender based on rating and tags by other users.

# Problem Statement
## Blockbuster or art film?
1. Set up a data science project structure in a new git repository in your GitHub account
2. Download the one of the MovieLens datasets from https://grouplens.org/datasets/movielens/
3. Load the data set into panda data frames
4. Formulate one or two ideas on how the combination of ratings and tags by users helps the data set to establish additional value using exploratory data analysis
5. Build one or more clustering models to determine similar movies to recommend using the other ratings and tags of movies by other users as features
6. Document your process and results
7. Commit your notebook, source code, visualizations and other supporting files to the git repository in GitHub

---
## Data Description
This dataset (ml-latest-small) describes 5-star rating and free-text tagging activity from http://movielens.org, a movie recommendation service. It contains 100836 ratings and 3683 tag applications across 9742 movies. These data were created by 610 users between March 29, 1996 and September 24, 2018. Users were selected at random for inclusion. All selected users had rated at least 20 movies.Each user is represented by an id and had rated at least 20 movies.
The data are contained in the files `links.csv`, `movies.csv`, `ratings.csv` and `tags.csv`.

---
## What we want to do?
- use few Clustering models to recommend movies based on ratings and tags by other users.

## Analysis of Data

![](https://github.com/SFLazarus/Movie-Recommender/blob/master/reports/popularityofgenres_plot.png)

### Using Feature Engineering and exploratory analysis we could use features to the best for training Clustering models and generate Recommendations

- First, we used KMeans Clustering Model, after finding optimal k value which was 20 we could form these clusters:

![](https://github.com/SFLazarus/Movie-Recommender/blob/master/reports/kmeanclusters_plot.png)

- Then we used Agglomerative Clustering Model with 20 clusters again and formed these clusters:

![](https://github.com/SFLazarus/Movie-Recommender/blob/master/reports/AgglomerativClusters_plot.png)

- We then built two recommenders each based on above mentioned clustering models.
---
## Results
### When tried to find 5 recommendations for Titanic (1997)
#### KMeans based Recommender suggested:
- American Beauty (1999)
- Good Will Hunting (1997)
- Titanic (1997)
- Eternal Sunshine of the Spotless Mind (2004)
- Beautiful Mind, A (2001)
#### Agglomerative Clustering based Recommender suggested:
- Beautiful Mind, A (2001)
- Rob Roy (1995)
- Pearl Harbor (2001)
- Bodyguard, The (1992)
- About Time (2013)

---

# Project Structure:
### Readme.md
- Project description
### Data
- Contains raw data files in csv format
### Notebooks
- Jupyter Notebook for Exploratory data analysis, Visualization, Feature Engineering and Clustering.
### Reports
- plot- popularity of genres
- Plot- Kmeans Clusters
- Plot- Agglomerative Clusters
### Requirements.txt
- Info about Tools, frameworks and libraries required to reproduce the work flow
