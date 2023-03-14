# Deep_Learning models

# CNN

The core idea behind CNNs is that they are designed to recognize patterns and features in images by applying a series of filters or "convolutions" to the input image. These filters are small matrices of numbers that are slid over the image one pixel at a time, and at each position, they perform a dot product operation between the filter values and the corresponding pixel values in the image. This process creates a new matrix, called a feature map, that highlights certain patterns and features in the input image.

CNNs typically consist of multiple layers, including convolutional layers, pooling layers, and fully connected layers. In convolutional layers, the filters are applied to the input image to extract features, and in pooling layers, the feature maps are downsampled to reduce the size of the data and extract more robust features. Finally, fully connected layers use the extracted features to classify the input image into one of several categories.

During training, the network is presented with a large number of images with known labels, and the weights of the filters and layers are adjusted to minimize the difference between the predicted output and the true label. This process is called backpropagation, and it allows the network to learn to recognize and classify images with increasing accuracy over time.

Overall, CNNs are a powerful tool for image recognition and classification, and they have been used in a wide range of applications, from self-driving cars to medical image analysis.

# LSTM  

Long Short-Term Memory (LSTM) is a type of Recurrent Neural Network (RNN) that is designed to handle the vanishing gradient problem and better capture long-term dependencies in sequential data. The LSTM architecture is composed of a series of memory cells that are connected to each other through a set of gating mechanisms.

Each memory cell is responsible for maintaining a hidden state vector, which represents the cell's memory of the past inputs it has seen. The LSTM architecture includes three gating mechanisms that control the flow of information into and out of the memory cells: the input gate, the forget gate, and the output gate.

The input gate determines which components of the current input should be added to the memory cell state. It takes as input the current input and the previous hidden state and applies a sigmoid activation function to the concatenated input. This produces a vector of gate values that determine which components of the input should be added to the memory cell state.

The forget gate determines which components of the current memory cell state should be retained or discarded. It takes as input the current input and the previous hidden state and applies a sigmoid activation function to the concatenated input. This produces a vector of gate values that determine which components of the memory cell state should be kept and which should be discarded.

The output gate determines which components of the memory cell state should be used to compute the output. It takes as input the current input and the previous hidden state and applies a sigmoid activation function to the concatenated input. This produces a vector of gate values that determine which components of the memory cell state should be used to compute the output.

The memory cell state is updated by combining the input gate and the current input, and then adding or subtracting components based on the forget gate. Finally, the output gate is used to determine which components of the updated memory cell state should be used to compute the output.

LSTMs have been shown to be effective in a wide range of applications, including language modeling, speech recognition, and image captioning. They are particularly useful in tasks that require the model to capture long-term dependencies in the data, as they are able to maintain a memory of past inputs and selectively retain or discard components of that memory based on the current input.

# RNN
      
Recurrent Neural Networks (RNNs) are a type of neural network architecture that is designed to handle sequential data. They are particularly useful for processing data that has a temporal or sequential relationship, such as time series data, text, and speech.

The key idea behind RNNs is that they are able to maintain an internal state or "memory" that allows them to process inputs one at a time, while also taking into account the context of previous inputs. This makes them well-suited for tasks like language modeling, where the probability of a given word depends on the preceding words in the sentence.

In an RNN, each neuron has a recurrent connection to itself, which allows it to use its previous state as an input to the current state. This means that the output of the network at each time step depends not only on the current input but also on the previous state.

During training, the network learns to update its internal state based on the current input and the previous state, and to produce an output that is appropriate for the current input and the context provided by the previous inputs. This is achieved through a process called backpropagation through time, where the error is propagated backwards through the network, updating the weights at each time step.

RNNs have been successfully used in a wide range of applications, including speech recognition, natural language processing, and image captioning. However, they can be challenging to train, as the gradients can sometimes vanish or explode over time, leading to difficulties in learning long-term dependencies. To address this issue, a number of variants of RNNs have been developed, including Long Short-Term Memory (LSTM) networks and Gated Recurrent Units (GRUs), which are designed to better capture long-term dependencie    
    

# Transformers

Transformers are a type of neural network architecture that is designed to process sequential data, such as text or time series data. Unlike Recurrent Neural Networks (RNNs), which process data sequentially, Transformers can process the entire input sequence in parallel, making them more computationally efficient.

The key innovation in the Transformer architecture is the self-attention mechanism, which allows the model to weigh the importance of different parts of the input sequence when making predictions. This is achieved by computing a set of attention weights for each position in the input sequence, based on the relationships between all pairs of positions.

The Transformer architecture is composed of an encoder and a decoder. The encoder takes the input sequence and processes it using a series of self-attention layers and feedforward layers. The self-attention layers compute a set of attention weights for each position in the input sequence, based on the relationships between all pairs of positions. The feedforward layers then use these attention weights to compute a new set of representations for each position in the input sequence.

The decoder takes as input the encoded representation of the input sequence and a set of previously generated tokens (if any), and processes them using a similar set of self-attention and feedforward layers. In addition, the decoder includes an additional set of attention weights that compute the relationships between the encoder representations and the decoder representations.

During training, the Transformer model is trained to predict the correct output sequence given the input sequence. This is achieved using a combination of teacher forcing, where the correct output sequence is provided as input during training, and beam search, which is used to generate the output sequence during inference.

Transformers have been shown to be effective in a wide range of natural language processing tasks, including machine translation, language modeling, and text classification. They have also been used in
