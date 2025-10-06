# Glass Classification Project

## Overview
This project uses the **Glass Identification Dataset** to classify types of glass based on their chemical composition. The dataset is analyzed and preprocessed, and a K-Nearest Neighbors (KNN) classifier is applied to predict the glass type.

## Dataset
The dataset (`glass.csv`) contains 214 samples with 10 attributes:
- **Features** (9): 
  - RI: Refractive Index
  - Na: Sodium
  - Mg: Magnesium
  - Al: Aluminum
  - Si: Silicon
  - K: Potassium
  - Ca: Calcium
  - Ba: Barium
  - Fe: Iron
- **Target**: Type (glass type, categorical with values 1 to 7)

The dataset is used to predict the type of glass based on its chemical properties.

## Project Structure
- **Glass Classification.ipynb**: Jupyter notebook containing the code for data loading, preprocessing, model training, and evaluation.
- **glass.csv**: The dataset file (included in this repository).

## Prerequisites
To run the notebook, install the required Python libraries:
```bash
pip install pandas scikit-learn
```

## Steps in the Notebook
1. **Data Loading**:
   - The dataset is loaded into a pandas DataFrame from `glass.csv`.
   - The dataset has 214 rows and 10 columns.

2. **Preprocessing**:
   - The features (RI, Na, Mg, Al, Si, K, Ca, Ba, Fe) are standardized using `StandardScaler` to ensure all features are on the same scale.
   - The target variable (`Type`) is separated from the features.

3. **Data Splitting**:
   - The dataset is split into training (70%) and testing (30%) sets using `train_test_split`.

4. **Model Training**:
   - A K-Nearest Neighbors (KNN) classifier is used with `n_neighbors=3`.
   - The model is trained on the training set.

5. **Model Evaluation**:
   - Training accuracy: ~81.88%
   - Testing accuracy: ~64.62%

## Results
- The KNN model with 3 neighbors achieves a training accuracy of approximately 81.88% and a testing accuracy of approximately 64.62%.
- The model shows signs of overfitting, as the training accuracy is significantly higher than the testing accuracy. Further tuning (e.g., adjusting `n_neighbors` or using cross-validation) could improve performance.

## How to Run
1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Place the `glass.csv` dataset in the same directory as the notebook.
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook Ex_08_Glass.ipynb
   ```
4. Run all cells to reproduce the analysis and results.

## License
This project is licensed under the MIT License.
