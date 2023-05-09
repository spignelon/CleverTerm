# CleverTerm

CleverTerm is a prototype project that utilizes a LSTM model trained on bash history to suggest the next word in a command line interface. The project is unreleased and is currently in its alpha version.

## Model

The model used for CleverTerm is a sequential model with the following layers:
```
Layer (type)                Output Shape              Param #   
=================================================================
embedding (Embedding)       (None, None, 14)          347858    
                                                                 
lstm (LSTM)                 (None, None, 100)         46000     
                                                                 
lstm_1 (LSTM)               (None, 100)               80400     
                                                                 
dense (Dense)               (None, 100)               10100     
                                                                 
dense_1 (Dense)             (None, 24847)             2509547   
                                                                 
```
The model was trained using TensorFlow and has a total of 2,993,905 parameters, all of which are trainable.

## Usage
The trained model can be found at https://github.com/spignelon/CleverTerm/releases/download/v0.0.1-alpha/cleverterm_model.h5. More information about the project, including the code used to train the model, can be found in the following Jupyter notebook: https://github.com/spignelon/CleverTerm/blob/main/CleverTerm%20LSTM.ipynb.

## Data Source
The bash history data used to train the model was taken from [this Kaggle dataset](https://www.kaggle.com/datasets/thuyngandao/bashlogs), as well as various .bash_history files uploaded to GitHub and GitHub gists.

## Future Development
At the moment, CleverTerm is an experimental project and its future development is uncertain. However, we may continue working on it in the future to improve its accuracy and functionality.

## License
This project is licensed under the GNU General Public License v3.0
