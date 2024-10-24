# Wine Quality Prediction using Random Forest Classifier

This project predicts the quality of red wine based on its physicochemical properties using a machine learning model. The dataset used for this project is from the [UCI Machine Learning Repository](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009), specifically the Portuguese "Vinho Verde" red wine dataset. A Random Forest Classifier is trained to classify wines as either of good quality (quality >= 7) or bad quality (quality < 7).

## Table of Contents
- [Dataset](#dataset)
- [Project Overview](#project-overview)
- [Setup Instructions](#setup-instructions)
- [Project Workflow](#project-workflow)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Dataset

The dataset used in this project contains various physicochemical properties of red wine, such as pH, alcohol content, and acidity levels, which are used as input features. The target variable is wine quality, which is scored on a scale of 0 to 10. The dataset can be downloaded from [here](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009).

**Columns:**
- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol
- Quality (target)

## Project Overview

This project involves:
1. Loading and exploring the dataset to understand the data distribution.
2. Visualizing relationships between physicochemical features and wine quality using Seaborn.
3. Preprocessing the data, including handling missing values and label binarization.
4. Splitting the dataset into training and testing sets.
5. Training a Random Forest Classifier on the training set.
6. Evaluating the accuracy of the model using the test set.
7. Building a predictive system that classifies a new instance of wine as either "Good Quality" or "Bad Quality".

## Setup Instructions

To run this project, you need to set up a Python environment with the required dependencies. Follow the instructions below to install the necessary packages and run the code:

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/wine-quality-prediction.git
cd wine-quality-prediction
```

### 2. Create a Virtual Environment (Optional)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

The required libraries are listed in the `requirements.txt` file. You can install them using:

```bash
pip install -r requirements.txt
```

If you want to generate `requirements.txt` yourself, run:

```bash
pip freeze > requirements.txt
```

### 4. Run the Project

Execute the Jupyter notebook or Python script to run the model and test the predictions:

```bash
python wine_quality_prediction.py
```

## Project Workflow

1. **Data Collection**: Load the dataset and inspect its dimensions, data types, and summary statistics.
2. **Exploratory Data Analysis**:
   - Check for missing values and outliers.
   - Visualize distributions of features like volatile acidity and citric acid in relation to wine quality.
3. **Data Preprocessing**:
   - Drop the target column (`quality`) to create the feature matrix `X`.
   - Convert the quality scores into a binary classification label using Label Binarization (`1` for good quality, `0` for bad quality).
4. **Train-Test Split**: Split the dataset into training and test sets using an 80/20 ratio.
5. **Model Training**: Train a Random Forest Classifier on the training set.
6. **Model Evaluation**: Evaluate the model on the test set and display the accuracy score.
7. **Predictive System**: Build a simple predictive system that takes wine properties as input and predicts whether the wine is of good or bad quality.

## Results

The Random Forest Classifier achieves an accuracy of around **X%** on the test dataset. The accuracy may vary depending on the train-test split or hyperparameter tuning.

Example of a prediction using the input features:
```python
input_data = (7.5, 0.5, 0.36, 6.1, 0.071, 17.0, 102.0, 0.9978, 3.35, 0.8, 10.5)
```

The model predicts whether the wine is of **Good Quality** or **Bad Quality** based on these features.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for improvements, bug fixes, or additional features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```

Make sure to adjust the paths and project-specific details such as the accuracy once you have run the project fully!