# deep-learning-challenge
deep-learning-challenge, Week 21 Data analytics bootcamp challenge

## Key differences between the original 'AlphabetSoupCharity' code and the 'AlphabetSoupCharity_Optimization' code:
# Dropped Columns:
- Code 1 retains the 'STATUS' and 'SPECIAL_CONSIDERATIONS' columns.
- Code 2 drops additional columns 'STATUS' and 'SPECIAL_CONSIDERATIONS' beyond 'EIN' and 'NAME'.

# Binning of Application Types:
- Code 1 uses a cutoff value of 500 to bin 'APPLICATION_TYPE'.
- Code 2 uses a lower cutoff value of 100 for binning 'APPLICATION_TYPE'.

# Binning of Classifications:
- Code 1 sets a cutoff value of 1000 for binning 'CLASSIFICATION'.
- Code 2 uses a more aggressive cutoff value of 100.

# Custom Binning of ASK_AMT:
- Code 1 does not perform custom binning on 'ASK_AMT'.
- Code 2 introduces custom bins for 'ASK_AMT' and creates a new 'ASK_AMT_Bucket' column based on these bins, then drops the original 'ASK_AMT' column.

# Neural Network Architecture:
- Code 1 defines the first hidden layer with 80 neurons and the second with 30 neurons.
- Code 2 increases complexity with the first hidden layer having 100 neurons and the second with 50 neurons.

# Number of Training Epochs:
- Both Codes train the model for 100 epochs.

# Model Output:
- Code 1 reports a loss of 0.5534 and an accuracy of 0.7297.
- Code 2 reports an accuracy of 0.7293 with a loss of 0.5685.

## Report
1. Overview of the Analysis:
The objective of the challenge was to develop a machine learning model to predict applications that would be funded. The model could assist Alphabet Soup in identifying which projects could use their funding effectively.

2. Results:

Data Preprocessing:

Target Variables: 'IS_SUCCESSFUL' was used as the target/dependent variable.
Feature Variables: The features included 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT', and newly engineered 'ASK_AMT_Bucket'.
Removed Variables: 'EIN', 'NAME', 'STATUS', and 'SPECIAL_CONSIDERATIONS' were removed as they do not contribute to significant changes to the model.

Compiling, Training, and Evaluating the Model:

The model included two hidden layers with 100 and 50 neurons.
The model did not achieve the target performance, with an accuracy of approximately 72.93%.
To increase model performance, we adjusted variables, binning of variables, the number of training epochs, and the number of neurons in the hidden layers.

3. Summary:
The deep learning model, despite optimization efforts, fell short of the 75% accuracy target. For future attempts, it is recommended to explore running the model with more data, and avoid using variables that don't contribute to improving it (start with the optimized model).



