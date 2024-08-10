# Text Generator using LSTM

## Description
This project develops a Poem Text Generator using Long Short-Term Memory (LSTM) networks in Python. The system is trained on a dataset of 2400 lines of poetry and generates new poetic text based on the learned patterns. The model is built using TensorFlow and Keras, leveraging the power of LSTMs to capture the sequential nature of text.

## Dataset
The dataset used in this project consists of 2400 lines of poetry, which can be downloaded directly from the following link:

- [Download the Poem Dataset](https://raw.githubusercontent.com/laxmimerit/poetry-data/master/adele.txt)

### Dataset Summary:
- Total lines: 2400

## Model
The model is built using an LSTM architecture, which is well-suited for handling sequential data like text. The architecture includes an embedding layer, LSTM layers, and dense layers for the final output.

### Architecture
- **Input Layer**: Embedding layer with a vocabulary size of `vocab_size`, embedding dimensions of 50, and input length of `seq_length`.
- **LSTM Layers**: 
  - First LSTM layer with 100 units and `return_sequences=True`.
  - Second LSTM layer with 100 units.
- **Dense Layers**:
  - First dense layer with 100 neurons and ReLU activation.
  - Output dense layer with `vocab_size` neurons and softmax activation for multi-class classification.
  
### Performance
Training Accuracy: 85%

## Dependencies
The following libraries and frameworks are required to run this project:
- `numpy`
- `tensorflow`
- `keras`
- `matplotlib`
- `pandas`

## Installation
To install the necessary dependencies, run the following command:
```bash
pip install tensorflow keras numpy pandas






