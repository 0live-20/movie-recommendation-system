# Movie Recommendation System (DSA 1080A Project)

### The Goal
Is to build a simple recommendation system based on the **user ratings** and **genre**

### Project Summary (Duration:5 Weeks)

#### **Week 1-2: Data collection , Exploration and Cleaning**
* **Dataset:**Downloading MovieLens 100k ( which uses `u.data` for movie ratings and `u.item` for movie titles).
* **Initial Findings:** After merging the ratings and titles, we observed **high data sparsity**. Which means users only rated a small fraction of all available movies.

#### **Week 3: Feature Engineering and Selection**
* The raw data was transformed into a **User-Item Interaction Matrix**.
    * **Rows:** Unique Users (`user_id`)
    * **Columns:** Movie Titles (`title`)
    * **Values:** The User's Rating (1.0 to 5.0)
* This matrix is an important structure used for the collaborative filtering algorithm.

#### **Week 4: Model Building (Train a Machine Learning Model)**
* **Algorithm:** We implemented **Item-Item Collaborative Filtering**. This method finds similarity between movies, not users.
* **Core Logic:** The model calculates the **Cosine Similarity** between every pair of movies based on the shared user rating patterns. Movies with a high similarity score are recommended together.

#### **Week 5: Model Evaluation & Reporting**
* The model's performance is evaluated by its ability to generate high-quality **Top-N** recommendations.

### Final Recommendation Output

The system successfully generates relevant recommendations. When asked for movies similar to **'Star Wars (1977)'** (one of the most popular movies in the dataset), the model outputs similar highly-rated sci-fi/adventure classics:

| Movie Title | Similarity Score |
| :--- | :--- |
| Empire Strikes Back, The (1980) | 0.82 |
| Return of the Jedi (1983) | 0.77 |
| Raiders of the Lost Ark (1981) | 0.65 |
| Godfather, The (1972) | 0.61 |
| Silence of the Lambs, The (1991) | 0.58 |


### These are the files submitted:

* `01_eda_and_data_exploration.ipynb`: The complete Jupyter Notebook with all the code, cleaning, matrix creation, model building, and final output.
* `README.md`: This project summary file.
* `data/ml-100k/`: Contains the necessary `u.data` and `u.item` files used to run the project.sss
* `report.md`: contains summanry of the results
