# Capstone-2-E_Commerce

## Description
This capstone project is another simple RNN project to classify text category based on data from (https://www.kaggle.com/datasets/saurabhshahane/ecommerce-text-classification) using Tensorflow.Keras. (its also my second time posting here)
The architure is a simple LTSM based RNN where it have one layers of Bi-directional LTSM with nodes of 32, and one output layer of 4 nodes.

## The process of how this model training been done

1. Import Packages
   - Import libraries that might be useful for this model (dunno la)
     
3. Data Loading
   - Load the given dataset
     
4. Create a pandas dataframe using the CSV file
   - Since there is no column name for this file, we created new column names with "Category" and "Product Detail"
     
5. Preprocess the dataset
   - Check & remove Null values
   - Check duplicated values
   - set the feauture and label
   - use label encoder to make model understand the classification
     
6. Train Test Split
   - Setting the random seed = 42
   - Divide the data set to 70% / 15% / 15%, training, validation, testing
  
6. Tokenization
   - Here we use tokenizer
   - This is the process to convert individual text (word) into integers, the converted integers are called tokens.
   - We set the maximum token to 5000, and its output sequence length = 200
     
7. Embedding
    - This is the process to convert tokens into a long vector known as embedding, this long vector is a special representation that can help your machine learning model to understand the context of words

8. Model Architecture
    - Model Sequential Layer
    - Tokenizer Layer
    - Embedding Layer
    - Bi-directional LTSM Layer (32, return_sequence = False)
    - Dense Layer (4 nodes, softmax activation)
      
![Model Summary](https://github.com/user-attachments/assets/2c51e3d0-c72c-4ca9-b2ee-d020c24820db)
![Model Architecture](https://github.com/user-attachments/assets/c201d864-5287-40c2-9d47-ca9a4efe1a2d)

9. Model Compiler
    - Optimizer = Adam (Default)
    - loss function = sparse_categorical_crossentropy
    - metric = accuracy
      
10. Model Training
    - epoch = 10
    - early stop (patience=2, verbose=3)
    - batch size = 32
      
11. Evaluation & Classification Report
    - Here we can see the loss and accuracy of model
    - Using classification report, we can see it's precision, recall, f1-score, and support
      
![Model Accuracy](https://github.com/user-attachments/assets/cd9f80f9-e005-4435-8e74-b6c794d49ae8)
![Model Loss](https://github.com/user-attachments/assets/7d5aee34-c3b1-4cd8-8767-1823a608b683)
![Model Performance](https://github.com/user-attachments/assets/bd7b98e3-aa04-46df-987d-e2bd15c1f254)


12. Prediction of the Model
    - We test the model with first 20 testing dataset and compared it with real values
    - As you can see, the model managed to predict accurately
         
![Model Predicted Output](https://github.com/user-attachments/assets/d0ce7684-cd95-451a-bc7c-43affc6be268)

13. Last Step
    - for my last step, I saved necessary function such as Model, Tokenizer, Label Encoder
      
![Model Save](https://github.com/user-attachments/assets/f359a3b6-b8e0-4740-9a23-7019716277da)

## Acknowledgements

- Also thanks to my SHRDC Trainers for giving me the opportunity and knowledges about coding, machine learning and deep learning
