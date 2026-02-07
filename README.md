# 🔮 Next-Word Predictor: LSTM Language Model
An LSTM-based neural network designed to predict and generate sequential text. This project bridges the gap between raw text data and creative AI-driven text generation using Deep Learning.

## 🚀 Key Features:
🧹 Smart Preprocessing: Automated text cleaning, lowercasing, and special character removal.

🔢 Advanced Tokenization: Robust sequence creation with fixed-length input windows.

🧠 Deep LSTM Architecture: Multi-layered Long Short-Term Memory network with Dropout regularization.

🛡️ Robust Training: Integrated EarlyStopping and ModelCheckpoint to ensure the best model is saved without overfitting.

🎲 Creative Generation: Implements Temperature-based sampling to balance between predictable and creative text outputs.

💻 Interactive UI: User-friendly interface for real-time dynamic text prediction.

## 🏗️ Model Architecture
The model processes text through a sophisticated pipeline to understand linguistic patterns:

-Layer	Function
-Embedding	Transforms integers into dense vectors of fixed size.
-LSTM	Captures long-term dependencies and sequence patterns.
-Dropout	Randomly deactivates neurons to prevent overfitting.
-Dense	Fully connected layer to map outputs to vocabulary size.
-Softmax	Outputs probability distribution for the next token.

## 📊 Dataset
We use the Next-Word Predictor Text Generator Dataset from Kaggle.

File: next_word_predictor.txt

Content: Rich text corpus suitable for training sequence-to-word models.

## 🛠️ Installation & Setup
1. Clone the Vault
```
git clone https://github.com/yourusername/next-word-predictor.git
cd next-word-predictor
```
2. Install Dependencies
```
pip install -r requirements.txt
Note: Key requirements include tensorflow, numpy, and kagglehub.
```

## 🖥️ Usage
Training:
Simply run the notebook or the main training script. The model will automatically download the dataset via KaggleHub if it's missing.

### Inference (Generating Text)
Use the following snippet to generate text from a seed phrase:
<img width="1583" height="618" alt="image" src="https://github.com/user-attachments/assets/4710adaa-8a86-4d2f-8518-b85ebccbef20" />

### Python
from predict import predict_next_words

# Define your starting point
seed_text = "The sun was shining brightly"

# Generate 25 creative words
generated_text = predict_next_words(
    model=model,
    tokenizer=tokenizer,
    seed_text=seed_text,
    num_words=25,
    sequence_length=30,
    temperature=0.8 # Higher = more creative/random
)

print(f" Prediction: {generated_text}")

## 📈 Training Progress
Batch Size: 64

Epochs: 70 (with Early Stopping)

Optimization: Adam Optimizer with Categorical Cross-Entropy loss.

## 🤝 Contributing
Got an idea to make the model smarter?

1-Fork the Project.

2-Create your Feature Branch (git checkout -b feature/AmazingFeature).

3-Commit your Changes (git commit -m 'Add some AmazingFeature').

4-Push to the Branch (git push origin feature/AmazingFeature).

5-Open a Pull Request.

## Current Goals:

[ ] Add GRU-based architecture for faster training.

[ ] Implement Beam Search for better sentence structure.

[ ] Deploy as a Flask/FastAPI web app.

## 📜 License
Distributed under the MIT License. See LICENSE for more information.

Made by Syed Sarim Abbas
