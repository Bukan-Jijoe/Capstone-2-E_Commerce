# Capstone-2-E_Commerce

## Description
This capstone project is another simple RNN project to classify based on data from (https://www.kaggle.com/datasets/saurabhshahane/ecommerce-text-classification) using Tensorflow.Keras. (its also my second time posting here)
The architure is a simple LTSM based RNN where it have one layers of Bi-directional LTSM with nodes of 32, and one output layer of 4 nodes.

## The process of how this model training been done

1. Import Packages
2. Data Loading
   - Load the given dataset
     
4. Create a pandas dataframe using the CSV file
   - Since there is no column name for this file, we created new column names with "Category" and "Product Detail"
   - 
6. Preprocess the dataset
   - Check & remove Null values
   - Check duplicated values
   - set the feauture and label
   - use label encoder to make model understand the classification
     
7. Train Test Split
   - Setting the random seed = 42
   - Divide the data set to 70% / 15% / 15%, training, validation, testing
  
8. Tokenization
   - Here we use tokenizer
   - This is the process to convert individual text (word) into integers, the converted integers are called tokens.
   - We set the maximum token to 5000, and its output sequence length = 200
     
9. Embedding
    - This is the process to convert tokens into a long vector known as embedding, this long vector is a special representation that can help your machine learning model to understand the context of words

14. Model Architecture
    - LSTM Layer x2
    - Dropout Layer x1
    - Dense Layer x1
      
16. Model Training
    - epoch = 200
    - batch size = 32
18. Prediction & Evaluation




## Acknowledgements

- Also thanks to my SHRDC Trainers for giving me the opportunity and knowledges about coding, machine learning and deep learning
