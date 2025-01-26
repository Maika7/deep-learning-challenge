# deep-learning-challenge

## Project Overview
The goal of this project is to build a binary classification model that predicts whether applicants funded by the nonprofit foundation Alphabet Soup will be successful in their ventures. 

## Dataset Information
The dataset contains over 34,000 records of organizations that received funding from Alphabet Soup. Key columns include:
- Target: `IS_SUCCESSFUL` (1 if successful, 0 otherwise)
- Features: Application type, affiliation, classification, use case, organization type, income classification, special considerations, and requested funding amount.

Columns such as `EIN` and `NAME` were dropped as they do not contribute to the prediction.

## Analysis Workflow
1. **Data Preprocessing:**
   - Dropped unnecessary columns (`EIN`, `NAME`).
   - Grouped rare categories in `APPLICATION_TYPE` and `CLASSIFICATION` as `"Other"`.
   - Split the data into training and testing datasets.
   - Scaled the features using Standard Scaler.

2. **Model Creation:**
   - Defined a Sequential neural network model with:
     - Input layer with neurons.
     - Two hidden layers with 80 and 30 neurons, respectively.
     - Output layer with a sigmoid activation function.
   - Compiled and trained the model using binary cross-entropy loss and the Adam optimizer.

3. **Optimization:**
   - Applied various techniques to improve accuracy, including:
     - Adjusting the number of neurons.
     - Adding/removing layers.
     - Trying different activation functions and epochs.

4. **Evaluation:**
   - Evaluated the model’s performance using test data.

## Requirements
To run this project, install the following:
- Python 3.7+
- TensorFlow
- Pandas
- scikit-learn
- Google Colab
