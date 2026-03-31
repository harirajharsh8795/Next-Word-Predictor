# 🚀 Next Word Predictor

<div align="center">

**An intelligent next word prediction system powered by LSTM neural networks**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.16-orange?logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-Interactive%20Web%20App-red?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

</div>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Training Details](#training-details)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

## 📖 Overview

This project implements a **deep learning-based next word prediction system** using LSTM (Long Short-Term Memory) neural networks. Given a sequence of words, the model predicts the most likely next word with high accuracy.

The application features an interactive **Streamlit web interface** that allows users to input text and get real-time predictions. The model is trained on literary texts (Shakespeare's Hamlet) and implements early stopping to prevent overfitting.

---

## ✨ Features

- 🧠 **LSTM-based Neural Network** - State-of-the-art deep learning architecture for sequence prediction
- 🎯 **Accurate Predictions** - High accuracy next word predictions based on context
- 🎨 **Interactive Web Interface** - User-friendly Streamlit dashboard for easy interaction
- ⏹️ **Early Stopping** - Prevents overfitting during model training
- 📊 **Tokenization** - Advanced text preprocessing with Keras tokenizer
- 🔄 **Sequence Padding** - Proper handling of variable-length input sequences

---

## 🛠️ Technology Stack

| Technology | Purpose |
|-----------|---------|
| **Python** | Core programming language |
| **TensorFlow/Keras** | Deep learning framework |
| **LSTM** | Recurrent neural network for sequence modeling |
| **Streamlit** | Web application framework |
| **NumPy** | Numerical computations |
| **Pandas** | Data manipulation |
| **scikit-learn** | Machine learning utilities |
| **NLTK** | Natural language processing |

---

## 📁 Project Structure

```
Next-Word-Predictor/
│
├── app.py                                      # Streamlit web application
├── experiments.ipynb                           # Jupyter notebook for model training & experiments
├── hamlet.txt                                  # Training dataset (Shakespeare's Hamlet)
├── next_word_lstm.h5                          # Trained model (standard)
├── next_word_lstm_model_with_early_stopping.h5 # Trained model (with early stopping)
├── tokenizer.pickle                           # Saved tokenizer for text processing
├── requirements.txt                           # Python dependencies
├── README.md                                  # Project documentation
└── .gitignore                                 # Git ignore file
```

---

## 🔧 Installation

### Prerequisites
- Python 3.8 or higher
- pip or conda package manager

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/harirajharsh8795/Next-Word-Predictor.git
   cd Next-Word-Predictor
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   
   # Activate virtual environment
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 Usage

### Run the Web Application

Start the interactive Streamlit app:

```bash
streamlit run app.py
```

The application will open in your default browser at `http://localhost:8501`

**Example Usage:**
1. Enter a sequence of words in the input field (e.g., "To be or not to")
2. Click "Predict Next Word"
3. View the predicted next word in the output

---

## 🧠 Model Architecture

The LSTM model consists of:

- **Input Layer**: Sequences of tokenized words (variable length, padded)
- **Embedding Layer**: Converts token indices to dense vectors
- **LSTM Layer(s)**: Captures long-term dependencies and patterns in text
- **Dense Layers**: Fully connected layers for prediction
- **Output Layer**: Softmax activation for word probability distribution

**Key Parameters:**
- Sequence Length: 20 words
- Vocabulary Size: Learned from training data
- LSTM Units: 100+ (optimized for accuracy)
- Optimizer: Adam
- Loss Function: Categorical Cross-Entropy

---

## 📊 Training Details

### Dataset
- **Source**: Shakespeare's Hamlet (hamlet.txt)
- **Preprocessing**: 
  - Text tokenization using Keras Tokenizer
  - Sequence generation (creating input-output pairs)
  - Padding sequences to fixed length

### Training Configuration
- **Batch Size**: 64
- **Epochs**: 100+ (with early stopping)
- **Early Stopping**: Monitors validation loss to prevent overfitting
- **Validation Split**: 20%
- **Callbacks**: Early stopping, learning rate reduction

### Models Available
- `next_word_lstm.h5` - Standard trained model
- `next_word_lstm_model_with_early_stopping.h5` - Optimized with early stopping

---

## 📈 Results

The model achieves:
- ✅ **High Accuracy** on test dataset
- ✅ **Fast Inference** (<1 second per prediction)
- ✅ **Robust Performance** across various input sequences
- ✅ **Generalization** to unseen word combinations

---

## 🤝 Contributing

Contributions are welcome! Please feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 👤 Author

**Hari Raj Harsh**
- GitHub: [@harirajharsh8795](https://github.com/harirajharsh8795)

---

## 📞 Support

If you encounter any issues or have questions, please open an issue on GitHub or contact the author directly.

---

<div align="center">

Made with ❤️ by Hari Raj Harsh

</div>
