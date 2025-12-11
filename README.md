🚀 **Overview**

This project implements a Question Answering (QA) System using a Recurrent Neural Network (RNN) in PyTorch.
The model is trained on a custom dataset containing 100 unique question-answer pairs, and learns to predict the most likely answer token for a given question.

This project demonstrates end-to-end NLP steps:
- Text Tokenization
- Vocabulary Construction
- Converting Text → Numerical Indices
- Custom PyTorch Dataset + DataLoader
- RNN-based sequence modelling
- Model training
- Making predictions using Softmax probabilities

This repository is a great foundational example for beginners working with Deep Learning, NLP, PyTorch, and RNN architectures.

🧠 **Model Architecture**

The architecture is intentionally simple to demonstrate the fundamentals:

- **Embedding Layer**
Converts token IDs into 50-dimensional dense vectors.
**- RNN Layer**
Processes embedded question tokens to learn sequential dependencies.

Input size: 50
Hidden size: 64
batch_first=True

**- Fully Connected Layer**
Maps the final hidden state to a probability distribution over the vocabulary.

**Output:**
The model predicts one word as the most likely answer.

**📊 Dataset**

The project uses a small custom CSV dataset:
100 Question-Answer pairs
Two columns: question, answer

| question                       | answer      |
| ------------------------------ | ----------- |
| What is the capital of France? | Paris       |
| Who wrote Romeo and Juliet?    | Shakespeare |


**🛠️ How It Works**
**1️⃣ Tokenization**
Simple lowercasing + punctuation removal + word splitting.

**2️⃣ Vocabulary Building**
A vocabulary dictionary is created containing:
- All unique tokens from the dataset
- <UNK> token for unknown words

**3️⃣ Text → Indices Conversion**
Words are mapped to numeric token IDs.

**4️⃣ PyTorch Dataset + DataLoader**
Custom dataset returns:
  (question_tensor, answer_tensor)

**5️⃣ Training**
Loss: CrossEntropyLoss
Optimizer: Adam
Epochs: 20
Model learns to map a question sequence to a single answer token.


**▶️ Running the Project**
1. Install Dependencies
   - pip install torch pandas matplotlib
2. Load the Dataset
Place your 100_Unique_QA_Dataset.csv in the same folder.
3. Run the Notebook
Open in Google Colab or Jupyter Notebook.
4. Train the Model
Simply run all cells — model trains in seconds due to small dataset.


**📈 Improvements You Can Add Later**
- This project is intentionally simple. You can extend it by:
- Using LSTM or GRU instead of RNN
- Predicting full sentences instead of single tokens
- Adding attention mechanism
- Using pretrained embeddings (GloVe, FastText)
- Training on larger datasets (SQuAD, NaturalQuestions)

**🤝 Contributing**
Pull requests and suggestions are welcome!
Feel free to fork and improve the architecture or dataset.
