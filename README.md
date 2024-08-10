Poem Text Generator using LSTM
Description
This project develops a Poem Text Generator using Long Short-Term Memory (LSTM) networks in Python. The system is trained on a dataset of 2400 lines of poetry and generates new poetic text based on the learned patterns. The model is built using TensorFlow and Keras, leveraging the power of LSTMs to capture the sequential nature of text.

Dataset
The dataset used in this project consists of 2400 lines of poetry, which can be downloaded directly from the following link:

Download the Poem Dataset
Dataset Summary:
Total lines: 2400
Model
The model is built using an LSTM architecture, which is well-suited for handling sequential data like text. The architecture includes an embedding layer, LSTM layers, and dense layers for the final output.

Architecture
Input Layer: Embedding layer with a vocabulary size of vocab_size, embedding dimensions of 50, and input length of seq_length.
LSTM Layers:
First LSTM layer with 100 units and return_sequences=True.
Second LSTM layer with 100 units.
Dense Layers:
First dense layer with 100 neurons and ReLU activation.
Output dense layer with vocab_size neurons and softmax activation for multi-class classification.
Model Summary
python
Copy code
model = Sequential()
model.add(Embedding(vocab_size, 50, input_length=seq_length))
model.add(LSTM(100, return_sequences=True))
model.add(LSTM(100))
model.add(Dense(100, activation="relu"))
model.add(Dense(vocab_size, activation="softmax"))
Performance
Training Accuracy: 85%
Dependencies
The following libraries and frameworks are required to run this project:

tensorflow
keras
numpy
pandas
Installation
To install the necessary dependencies, run the following command:

bash
Copy code
pip install tensorflow keras numpy pandas
Usage
To train the model or generate text using a pre-trained model, you can use the following commands:

Train the Model
python
Copy code
python train.py --data_path path/to/dataset.txt --epochs 50 --batch_size 64
Generate Text
python
Copy code
python generate.py --model_path path/to/pretrained/model.h5 --seed "Your starting text"
Results
The trained model is capable of generating poetic text that reflects the style and structure of the input dataset. The generated text has an accuracy of 85%, showing its ability to capture the essence of the training data.

Contributing
Contributions are welcome! If you'd like to improve the model, fix bugs, or add new features, feel free to submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.

