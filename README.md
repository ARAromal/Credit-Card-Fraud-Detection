# Credit Card Fraud Detection 💳

This project uses machine learning to detect fraudulent credit card transactions from a highly imbalanced dataset.

-----

### About The Project

This repository contains the code and analysis for a machine learning project aimed at identifying fraudulent credit card transactions. The primary challenge is the severe class imbalance in the dataset, where fraudulent transactions are extremely rare compared to legitimate ones.

The project explores two different classification models to tackle this issue:

  * **Logistic Regression** (as a baseline)
  * **Random Forest Classifier**

The goal is to build a model that can effectively flag fraudulent activity, thereby helping financial institutions prevent losses while minimizing the impact on legitimate customers.

The dataset used is the "Credit Card Fraud Detection" dataset from Kaggle, which contains transactions made by European cardholders. Due to confidentiality, the original features have been transformed using Principal Component Analysis (PCA). The only features that have not been transformed are 'Time', 'Amount', and 'Class'.

-----

### Getting Started

To get a local copy up and running, follow these simple steps.

#### Prerequisites

Make sure you have Python and pip installed on your system. You will also need to have Jupyter Notebook or JupyterLab to run the notebook.

  * **Python**
  * **pip**

#### Installation

1.  **Clone the repo**
    ```sh
    git clone https://github.com/your_username/your_repository.git
    ```
2.  **Navigate to the project directory**
    ```sh
    cd your_repository
    ```
3.  **Install the required packages**
    Create a `requirements.txt` file with the following content:
    ```txt
    pandas
    scikit-learn
    kaggle
    jupyter
    ```
    Then run:
    ```sh
    pip install -r requirements.txt
    ```

-----

### Usage

To see the analysis and model training process, launch the Jupyter Notebook:

```sh
jupyter notebook ML.ipynb
```

You can run the cells sequentially to see the data loading, exploratory data analysis, model training, and final evaluation.

-----

### Methodology and Results

The project follows a standard machine learning workflow:

1.  **Data Loading & Exploration**: The `creditcard.csv` dataset is loaded into a pandas DataFrame. A key finding from the initial analysis is the dataset's severe imbalance, with only 492 fraudulent transactions (0.17%) out of 284,807 total transactions.

2.  **Data Splitting**: The data is split into an 80% training set and a 20% testing set. Stratification is used to ensure that the proportion of fraudulent to normal transactions is maintained in both sets.

3.  **Model Training & Evaluation**:

      * A **Logistic Regression** model was trained as a baseline. It achieved a **recall of 69%** for fraudulent transactions, meaning it correctly identified 69% of all frauds in the test set. Its precision was 84%.
      * An improved **Random Forest Classifier** was then trained. This model showed significantly better performance, achieving a **recall of 82%** and a **precision of 94%** for the fraud class.

    | Model | Precision (Fraud) | Recall (Fraud) | F1-Score (Fraud) |
    | :--- | :---: | :---: | :---: |
    | Logistic Regression | 0.84 | 0.69 | 0.76 |
    | **Random Forest** | **0.94** | **0.82** | **0.87** |

-----

### Conclusion

The final Random Forest model significantly outperformed the baseline Logistic Regression model. With a fraud **recall of 82%**, it successfully identifies a higher percentage of fraudulent transactions, which is crucial for loss prevention. The high **precision of 94%** ensures that the model does not excessively flag legitimate transactions as fraudulent.

This model is recommended as an effective solution for detecting credit card fraud in this dataset.

-----

### Acknowledgments

  * This project uses the "Credit Card Fraud Detection" dataset, which can be found on [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).
  * The dataset was collected and analyzed during a research collaboration of Worldline and the Machine Learning Group (MLG) of ULB (Université Libre de Bruxelles) on big data mining and fraud detection.

-----

### Contact

Your Name - araromal2002@gmail.com

Project Link: [https://github.com/ARAromal/Card-Fraud-Detection](https://www.google.com/search?q=https://github.com/ARAromal/Card-Fraud-Detection)
