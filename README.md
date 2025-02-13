```markdown
# potential-waffle

## Overview
This project builds a recommendation system using real data from the IBM Watson Studio platform. The notebook includes various methods for making recommendations that can be used for different situations.

## Setup Instructions

### 1. Install Dependencies
Ensure the following Python packages are installed:
```sh
pip install pandas numpy matplotlib scikit-learn flask plotly
```

### 2. Prepare the Data
Load the data files:
- user-item-interactions.csv
- articles_community.csv

### 3. Run the Notebook
Execute the Jupyter notebook Recommendations_with_IBM.ipynb to build and evaluate the recommendation system.

## Repository Structure
```
project-root/
├── data/
│   ├── articles_community.csv       # Dataset - articles content
│   ├── user-item-interactions.csv   # Dataset - user interactions
├── Recommendations_with_IBM.ipynb   # Jupyter notebook with the recommendation system
├── project_tests.py                 # Test functions for the project
├── README.md                        # Project documentation
```

## Project Workflow

### I. Exploratory Data Analysis

1. **Distribution of User-Article Interactions**
   - Explore the distribution of how many articles a user interacts with in the dataset.
   - Provide visual and descriptive statistics.

2. **Removing Duplicate Articles**
   - Explore and remove duplicate articles from the `df_content` dataframe to ensure data integrity.

3. **Descriptive Statistics**
   - Find the number of unique articles that have an interaction with a user.
   - Find the number of unique articles in the dataset (whether they have any interactions or not).
   - Find the number of unique users in the dataset (excluding null values).
   - Find the number of user-article interactions in the dataset.

4. **Most Viewed Article**
   - Identify the most viewed article and how often it was viewed.

5. **Mapping User Emails to User IDs**
   - Map user emails to user IDs using the `email_mapper` function.

### II. Rank-Based Recommendations

- Create functions to return the top `n` articles ordered by the number of interactions.
- Test these functions to ensure they return the expected results.

### III. User-User Based Collaborative Filtering

1. **Creating User-Item Matrix**
   - Reformat the `df` dataframe to be shaped with users as rows and articles as columns.
   - Each entry in the matrix indicates whether a user has interacted with an article.

2. **Finding Similar Users**
   - Create a function to find the most similar users to a given user based on the dot product of their interactions.

3. **Recommending Articles**
   - Create functions to recommend articles to users based on the interactions of similar users.

### IV. Content-Based Recommendations (EXTRA - NOT REQUIRED)

- Create a content-based recommender using TF-IDF vectorization and cosine similarity to recommend articles based on their content.

### V. Matrix Factorization

1. **Performing SVD**
   - Perform Singular Value Decomposition (SVD) on the user-item matrix.
   - Evaluate the accuracy of the predictions with different numbers of latent features.

2. **Evaluating Accuracy**
   - Evaluate the accuracy of the predictions using mean squared error.
   - Determine the optimal number of latent features.

### VI. Extras & Concluding

- Discuss the results and potential improvements to the recommendation system.

## Required Imports

To run the notebook end to end, the following imports are required:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import project_tests as t
import pickle
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.metrics import mean_squared_error
from sklearn.metrics.pairwise import cosine_similarity

%matplotlib inline
```

## Contribution
If you'd like to contribute, feel free to submit pull requests or raise issues on GitHub!

You can find the project on GitHub at: [GitHub Repository](https://github.com/your-repo-link)

---

Developed as part of the Recommendations with IBM project.
```

This `README.md` file provides a detailed explanation of the project workflow, setup instructions, repository structure, and required imports. It also includes a section for contributions and a link to the GitHub repository.
This `README.md` file provides a detailed explanation of the project workflow, setup instructions, repository structure, and required imports. It also includes a section for contributions and a link to the GitHub repository.