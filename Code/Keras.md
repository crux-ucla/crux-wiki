A high level API that allows for quick development of neural networks. 
[Keras API Reference](https://colab.research.google.com/corgiredirector?site=https%3A%2F%2Fkeras.io%2Fapi%2F) 
## Example Model

```Python
from keras.models import Sequential
from keras.layers import Input, Dense, Dropout, Activation
from keras.layers import Embedding
from keras.layers import LSTM

hidden_size = 64

# Initialize the model
model = Sequential()

# Specify the input to the model 
model.add(Input(shape=(X_train.shape[1], 1)))

# Add a Long Short-Term Memory Layer (form of RNN) with 64 neurons
model.add(LSTM(hidden_size))

# Add a Dropout Layer, which randomly sets inputs to 0 35% of the time
# This is a regularization technique commonly used to prevent overfitting
model.add(Dropout(0.35))

# Add a Dense Layer, which is a layer of neurons in a neural network that 
# receive inputs from all neurons from the previous layer. 
# In this case, this is our output layer.
model.add(Dense(1))

# Adds an Activation Layer, which simply provides an activation function
model.add(Activation('sigmoid'))

# Compile the model, specifying the loss function and optimizer to use
model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['mae', 'acc'])

print(model.summary())
```

<iframe
  src="https://jupyterlite.github.io/demo/repl/index.html?kernel=python&code=import%20matplotlib.pyplot%20as%20plt%20%20%0Aimport%20numpy%20as%20np
&theme=JupyterLab Dark"
  width="100%"
  height="100%"
></iframe>
