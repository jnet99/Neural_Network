# Neural_Network
##Objective:
Implement a Python function, nn_keras, to train and evaluate a neural network model using TensorFlow/Keras. The model is trained on a dataset and tested on a separate test set, with configurable hyperparameters.


## Code Structure

### `nn_keras_main.py`:
- Sets the dataset directory, dataset name, and hyperparameters (`layers`, `units_per_layer`, `epochs`).
- Calls the `nn_keras` function with the specified inputs.

### `nn_keras.py`:
- **Data Loading**: Reads training and test data from UCI-format files.
- **Data Normalization**: Normalizes input features by dividing by the maximum absolute value across all training data.
- **Model Architecture**:
  - Input layer size matches the dataset's feature dimensions.
  - Hidden layers use the sigmoid activation function and are fully connected (dense).
  - Output layer size matches the number of classes in the dataset.
- **Training**: Uses the Adam optimizer and Sparse Categorical Crossentropy loss.
- **Evaluation**:
  - Predicts classes for test data.
  - Computes accuracy for each test object, handling ties appropriately.
  - Prints object ID, predicted class, true class, and accuracy for each test example.
  - Computes and prints the overall classification accuracy.
## Key Features
- Supports configurable neural network architectures (number of layers, units per hidden layer).
- Handles multi-class classification tasks.
- Normalizes input data to improve training stability.
- Uses TensorFlow/Keras for model implementation and training.

## Testing and Results
- Tested on the `pendigits` dataset with the following configurations:
  1. **2 layers, 10 epochs**:
     - Output: Classification accuracy for each test object and overall accuracy.
  2. **4 layers, 40 units per hidden layer, 20 epochs**:
     - Output: Classification accuracy for each test object and overall accuracy.
- Results were consistent with expected performance ranges (e.g., 87.34%–89.14% accuracy for `pendigits` with 4 layers and 50 units per hidden layer).


  ## Example Output
![nn_keras_pendigits_4_50_20](https://github.com/user-attachments/assets/c7fae9e5-7003-49c1-bf17-39a7864feb34)
  
