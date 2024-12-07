# Video Game Sales Prediction and Recommendation System

This project combines two functionalities: predicting video game sales based on various features and recommending similar games based on user-selected titles. It leverages machine learning and natural language processing techniques.

---

## Features

### 1. **Video Game Sales Prediction**
   - **Objective**: Predict global sales (`Global_Sales`) of video games using features like platform, genre, publisher, critic score, and user score.
   - **Techniques Used**:
     - Data preprocessing (handling missing values, standardization, one-hot encoding)
     - Linear regression model
   - **Key Libraries**: `pandas`, `scikit-learn`

### 2. **Game Recommendation System**
   - **Objective**: Suggest similar video games based on genre, platform, and publisher.
   - **Techniques Used**:
     - TF-IDF (Term Frequency-Inverse Document Frequency) vectorization
     - Cosine similarity for recommendation
   - **Key Libraries**: `pandas`, `scikit-learn`

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/bukkybyte/video_games_machine_learning.git
   ```
2. Navigate to the project directory:
   ```bash
   cd video_games_machine_learning
   ```
3. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

### 1. **Sales Prediction**
   - The prediction pipeline includes preprocessing of numeric and categorical data using a `Pipeline` and `ColumnTransformer`.
   - To train and evaluate the model:
     - Run the provided script, which splits the data into training and testing sets, trains the model, and evaluates it using metrics such as Mean Squared Error (MSE) and Root Mean Squared Error (RMSE).
     - Output: 
       - MSE and RMSE values for the test set.

### 2. **Game Recommendation**
   - Preprocess the data to create a `combined_features` column using `Genre`, `Platform`, and `Publisher`.
   - Use TF-IDF and cosine similarity to compute similarity between games.
   - Run the recommendation system:
     - Pass a game title to the `get_recommendations` function to receive a list of 10 similar games.
     - Example:
       ```python
       get_recommendations("Game Title")
       ```

---

## Example Outputs

### Sales Prediction
- Sample output after training:
  ```
  Mean Squared Error (MSE): 0.12345
  Root Mean Squared Error (RMSE): 0.35123
  ```

### Game Recommendation
- Sample recommendations for `Super Mario`:
  ```
  Recommendations for Super Mario:
  1. Mario Kart
  2. Super Mario Bros
  3. Mario Party
  4. Super Smash Bros
  5. Yoshi's Island
  ...
  ```

---

## Files in the Repository

- `Video_Games.csv`: Dataset used for prediction and recommendation.
- `video_games.ipynb`: Main script to run both functionalities.
- `requirements.txt`: List of required Python packages.

---

## Contributing

Contributions are welcome! If you'd like to improve this project, follow these steps:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature-name"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a Pull Request.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments

- The dataset is sourced from [Video Game Sales Dataset](https://example-dataset-link.com).
- Special thanks to contributors and the open-source community.
