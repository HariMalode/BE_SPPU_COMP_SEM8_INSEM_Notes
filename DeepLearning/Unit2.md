# Deep Neural Networks(DNNs) 

### Q1. Explain biological neurons.

A biological neuron is the fundamental building block of the nervous system in animals, including humans. It is a specialized cell that processes and transmits information in the form of electrical and chemical signals. Here's a detailed explanation of a biological neuron:

### Structure of a Biological Neuron

<img src ="./images/4.png">

1. **Cell Body (Soma)**: 
   - This is the central part of the neuron where the nucleus is located. The nucleus contains the cell’s genetic material (DNA) and controls cell activities. 

2. **Dendrites**: 
   - These are tree-like branches that extend from the cell body and receive signals from other neurons. The dendrites increase the surface area of the neuron to receive more inputs.

3. **Axon**: 
   - A long, thin extension that transmits electrical signals (action potentials) away from the cell body to other neurons, muscles, or glands. 

4. **Axon Terminals**:
   - These are the small branches at the end of the axon. They release  (chemical messengers) to communicate with other neurons.

### Connection to Artificial Neurons in Deep Learning
In artificial neural networks, the biological neuron serves as a metaphor for the **artificial neuron**:
- The **inputs** to an artificial neuron correspond to the **dendrites** of a biological neuron.
- The **weights** of the inputs in an artificial neuron are similar to the strength or magnitude of the signal received at the synapses.
- The **activation function** in an artificial neuron mirrors the way a biological neuron integrates signals and decides whether or not to fire (i.e., generate an action potential).
---

### Q2. What is a Perceptron? What are the steps involved for training a Perceptron in Deep Learning? [5]
<img src ="./images/5.png">

### **What is a Perceptron?**  
A **Perceptron** is the simplest type of artificial neural network model used for binary classification problems. It is a type of artificial neuron that mimics the working of a biological neuron by taking multiple inputs, applying weights, summing them, and passing the result through an activation function to produce an output.  

The Perceptron consists of the following components:  
- **Input Layer:** Accepts multiple features (input values).  
- **Weights (W):** Each input is assigned a weight that determines its importance.  
- **Summation Function:** Computes the weighted sum of inputs.  
- **Activation Function:** Applies a function (usually step function) to decide whether the neuron should be activated (output = 1) or not (output = 0).  

### **Mathematical Representation of Perceptron**  
The Perceptron computes the weighted sum:  
**Z = W₁X₁ + W₂X₂ + ... + WₙXₙ + b**  

where:  
- **X₁, X₂, ..., Xₙ** are input features.  
- **W₁, W₂, ..., Wₙ** are corresponding weights.  
- **b** is the bias term.  
- **Z** is the weighted sum.  

The activation function (Step Function) determines the final output:  

If **Z ≥ 0**, then **Y = 1**  
If **Z < 0**, then **Y = 0**  

### **Steps to Train a Perceptron**  
Training a Perceptron involves updating the weights to minimize classification errors. The process follows these steps:

1️⃣ **Initialize Weights and Bias**  
   - Set small random values for weights (**W**) and bias (**b**).  

2️⃣ **Feed Forward (Compute Output)**  
   - Calculate the weighted sum:  
     **Z = W₁X₁ + W₂X₂ + ... + WₙXₙ + b**  
   - Apply the **step activation function** to get output **Y**.  

3️⃣ **Compute Error**  
   - Compare **predicted output (Y)** with the **actual output (Y_true)**.  
   - Compute **error (E)**:  
     **E = Y_true - Y**  

4️⃣ **Update Weights using Perceptron Learning Rule**  
   - Adjust weights and bias using the formula:  
     **Wᵢ = Wᵢ + η × (Y_true - Y) × Xᵢ**  
     **b = b + η × (Y_true - Y)**  
   where **η** (learning rate) controls how much weights change.  

5️⃣ **Repeat for All Training Examples**  
   - Repeat steps **2-4** for each training data point.  

6️⃣ **Iterate Until Convergence**  
   - Continue training for multiple iterations (**epochs**) until weights stabilize or classification accuracy is maximized.  
---

### Q3. What is Perceptron? Write short note on Multilayer Feed-Forward network with figure [5]

### **Multilayer Feed-Forward Network**  

A **Multilayer Feed-Forward Network (MLFFN)** is an artificial neural network that consists of multiple layers of neurons, where information flows in one direction—from the **input layer** to the **output layer** through one or more **hidden layers**. It is also known as a **Multi-Layer Perceptron (MLP)** when fully connected.  

### **Structure of MLFFN**  
1️⃣ **Input Layer**: Receives input features (X₁, X₂, ..., Xₙ).  
2️⃣ **Hidden Layers**: Intermediate layers that process the input using weights and activation functions. These layers help in feature extraction and learning complex patterns.  
3️⃣ **Output Layer**: Produces the final output (classification or regression result).  

Each neuron in one layer is **fully connected** to neurons in the next layer, and activation functions like **ReLU, Sigmoid, or Tanh** introduce non-linearity, enabling the network to solve complex problems.  

### **Working of MLFFN**  
✅ **Forward Propagation**: Inputs are passed through weighted connections, summed, and activated to produce outputs.  
✅ **Backpropagation**: The network adjusts weights using the **gradient descent algorithm** to minimize error.  
✅ **Training**: The process repeats for multiple iterations (epochs) until the network learns the correct mapping of inputs to outputs.  

### **Advantages of MLFFN**  
✔️ Can learn **non-linear relationships**  
✔️ Extracts **high-level features** using hidden layers  
✔️ Used in **deep learning applications** like image recognition, NLP, and medical diagnosis  

---

### Q4. Explain how a Neural Networks can be trained with Back propagation and Forward propagation methods. [5]  


### **Training a Neural Network Using Forward Propagation and Backpropagation**  

Training a **Neural Network (NN)** involves adjusting the network's **weights and biases** to minimize the error in predictions. The training process consists of two main steps:  

## **1. Forward Propagation**  
Forward propagation is the process of **passing inputs through the network layers** to generate an output. It follows these steps:  

### **Steps of Forward Propagation**  
🔹 **Step 1: Input Layer**  
- The input features **(X₁, X₂, ..., Xₙ)** are fed into the neural network.  

🔹 **Step 2: Weighted Sum Calculation**  
- Each neuron calculates a weighted sum of its inputs:  
  
  Z = W₁X₁ + W₂X₂ + ... + WₙXₙ + b
   
  where **W** are the weights, and **b** is the bias.  

🔹 **Step 3: Activation Function**  
- The weighted sum is passed through an activation function (e.g., **ReLU, Sigmoid, or Tanh**) to introduce non-linearity.  

🔹 **Step 4: Output Generation**  
- The final layer produces an output, either **a probability (classification) or a numerical value (regression).**  

---

## **2. Backpropagation (Backward Propagation of Errors)**  
Backpropagation is a method used to **minimize error** by adjusting the network’s weights using the **gradient descent** algorithm.  

### **Steps of Backpropagation**  
🔹 **Step 1: Compute Error (Loss Function)**  
- The difference between the predicted output and actual output is calculated using a **loss function** (e.g., Mean Squared Error for regression, Cross-Entropy for classification).  

🔹 **Step 2: Compute Gradients**  
- The derivative of the loss function with respect to each weight is computed using **partial derivatives** (Gradient Descent).  

🔹 **Step 3: Weight Updates (Gradient Descent)**  
- The weights are updated using the formula:  
 W(new) = W(old) - n * (dL/dW)

  where **η (learning rate)** controls the step size.  

🔹 **Step 4: Repeat Until Convergence**  
- The process continues iteratively for multiple epochs until the loss is minimized.  

---
### Q5. AND  Compare Back Propagation and Forward Propagation. [5]

| Feature            | Forward Propagation        | Backpropagation            |
|--------------------|--------------------------|----------------------------|
| **Definition**     | Process of passing input through the network to generate an output. | Process of adjusting weights by propagating error backward. |
| **Direction**      | Moves from input layer to output layer. | Moves from output layer to input layer. |
| **Purpose**        | Computes the predicted output. | Updates weights to minimize error. |
| **Computation**    | Uses weighted sum and activation functions. | Uses gradient descent and derivatives of the loss function. |
| **Error Calculation** | No error calculation, only forward pass. | Computes error using loss function and propagates it backward. |
| **Weight Update**  | No weight updates. | Adjusts weights and biases using gradient descent. |
| **Learning Process** | Only calculates outputs; does not modify the network. | Modifies network parameters to improve accuracy. |
| **Dependency**     | Requires initialized weights and biases. | Requires output from forward propagation. |
| **Execution Step** | First step in training a neural network. | Second step, which optimizes the network. |

In summary, **forward propagation** computes predictions, while **backpropagation** minimizes error by adjusting weights. 🚀

---

### Q6. What is Activation Function? Enlist and Explain different Activation functions used in Neural Network. [5]


### **Activation Function in Neural Networks**  

- An **activation function** is a mathematical function used in a neural network to introduce non-linearity in the model.
- It determines whether a neuron should be activated based on the weighted sum of inputs and bias. 
- Without activation functions, the neural network would behave like a simple linear regression model
- With activation function model learn complex patterns.  

---

### **Types of Activation Functions**  
**Some of the activation functions include Sigmoid, Relu, Leaky ReLU, Tạnh, Softmax, ELU, etc.**

### **Sigmoid and ReLU Activation Functions in Detail**  

#### **1. Sigmoid Activation Function**  
• The sigmoid function maps input values between 0 and 1, making it useful for binary/classification problems.  

##### **Formula**  
f(x) = {1}/{1 + e^{-x}}

if x =2 then f(x) = 1/{1 + e^{-2}} = 0.88
This means neuron is activated.

- Sigmoid function helps in probability-based predictions (eg, classifying emails as spam (1) or not spam (0).)

##### **Characteristics**  
- Output range: (0,1)  
- Non-linear, allowing complex patterns to be learned.  
- Converts large negative values close to 0 and large positive values close to 1.  


#### **2. ReLU (Rectified Linear Unit) Activation Function**  
The **ReLU function** introduces non-linearity by returning **zero for negative inputs** and the input itself for positive inputs.  

##### **Formula**  

f(x) = \max(0, x)

if x = 2 then f(x) = \max(0, 2) = 2
This means neuron is activated.
if  x = -2 then f(x) = \max(0, -2) = 0
This means neuron is not activated.


##### **Characteristics**  
- Output range: [0, ∞)  
- Non-linear, allowing deep networks to model complex functions.  
- Does not saturate for large positive values, unlike sigmoid.  


#### **3. Leaky ReLU Activation Function**  
Leaky ReLU is a variation of ReLU that allows a small negative slope for negative inputs.

#### **4. Softmax Activation Function**  
Softmax is used for multi-class classification problems. It converts raw scores into probabilities.

---

### Q7. Define Loss functions used in Deep Neural Network. Enlist and Explain any two of them in detail. [5]


### **Loss Functions in Deep Neural Networks**  

- A **loss function** measures the difference between the predicted output and the actual target value in a neural network.
- The goal of training is to minimize this loss to improve the model’s accuracy. 
- loss functions help neural networks learn patterns and make accurate predictions.
- Common loss functions include Mean Squared Exrox (MSE), Mean Absolute Error (MAE), Binary cross-entropy, Huber loss, etc.

---

### **Types of Loss Functions**  

1 **Mean Squared Error (MSE)**  
- Formula:  

 MSE = 1/n * Σ(y[actual] - ŷ[predicted])^2

 if actuual = 10 and predicted = 8 then MSE = 1/1 * (10 - 8)^2 = 4

- Penalizes large errors more than small errors.  
- Used in **regression problems**.  
- Sensitive to **outliers**.
- It helps to minimize the difference between predicted and actual values.

2 **Mean Absolute Error (MAE)**  
- Formula:  

MAE = 1/n * Σ|y[actual] - ŷ[predicted]|

if actual = 10 and predicted = 8 then MAE = 1/1 * |10 - 8| = 2

- Less sensitive to **outliers** than MSE.  
- Computes absolute differences, making it more **robust**.
- It helps to minimize the absolute difference between predicted and actual values.

3 **Huber Loss**  
- **Combination of MSE and MAE**, handling outliers better.  
- Used in **robust regression tasks**.  

---

### Q8. Write Short Note on: Hyper parameters used in Neural Network. [5]
### **Hyperparameters Used in Neural Networks**  

- Hyperparameters are *parameter* that are set before training a neural network. 
- These parameters affect the learning process and model performance.  
- Hyperparameters are not learned during training but are set before training.
- It is kind of setting that can be tuned to improve model performance.
- Examples of hyperparameters include learning rate, number of hidden layers, number of neurons per layer, etc.
---

### **Types of Hyperparameters**  

#### **1. Learning Rate (α)**  
- Controls how much the weights are updated during training.  
- A **high learning rate** may cause the model to converge too quickly or diverge.  
- A **low learning rate** may result in slow convergence or getting stuck in local minima.  

#### **2. Number of Hidden Layers**  
- Determines the depth of the neural network.  
- More layers allow learning complex patterns but increase computational cost.  

#### **3. Number of Neurons per Layer**  
- More neurons increase the model's capacity but may lead to overfitting.  
- Fewer neurons may underfit the data.  

#### **4. Batch Size**  
- • It defines how many training samples are them processed at once
• A small batch size leads to faster updates but is noisy, while a large batch size is more stable but requires more memory  

#### **5. Number of Epochs**  
- One epoch is a full pass of the entire dataset through the model.  
- **Too few epochs** may cause underfitting.  
- **Too many epochs** may cause overfitting.  

#### **6. Activation Functions**  
- Defines how neurons activate based on input.  
- Common choices: **ReLU, Sigmoid, Tanh, Softmax**.  

#### **7. Regularization**  
- **L1 and L2 Regularization** help prevent overfitting.  
- **L2 (Ridge Regression)**: Penalizes large weights.  
- **L1 (Lasso Regression)**: Shrinks some weights to zero.  

---

### Q9. Explain Sentimental Analysis and Its types. [5]

### **Sentiment Analysis and Its Types**  

#### **What is Sentiment Analysis?**  
Sentiment Analysis (also called **opinion mining**) is a **Natural Language Processing (NLP) technique** used to determine the sentiment or emotion expressed in text data. It is commonly applied to customer reviews, social media comments, survey responses, and more to understand people's opinions and feelings.  

---

### **Types of Sentiment Analysis**  

#### **1. Based on Polarity and Emotion**  
✅ **Positive Sentiment:** Indicates a favorable or happy opinion.  
✅ **Negative Sentiment:** Indicates an unfavorable or unhappy opinion.  
✅ **Neutral Sentiment:** No strong opinion, balanced response.  

Example:  
- "The product is amazing!" → **Positive**  
- "I hated the service." → **Negative**  
- "The event was okay." → **Neutral**  


#### **2. Aspect-Based Sentiment Analysis (ABSA)**  
- Analyzes **sentiment for specific aspects** of a product or service.  
- Example:  
  - "The camera quality is great, but the battery life is poor."  
  - Sentiment for **camera** → **Positive**  
  - Sentiment for **battery** → **Negative**  

---

#### **3. Fine-Grained Sentiment Analysis**  
- More detailed than basic polarity classification.  
- Uses a **rating scale** (e.g., 1 to 5 stars).  
  - ⭐⭐⭐⭐⭐ → **Very Positive**  
  - ⭐⭐⭐ → **Neutral**  
  - ⭐ → **Very Negative**  

---

### Working
- **Data Collection:** Gather text data from various sources.
- **Data Preprocessing:** Clean and preprocess the text data.
- **Feature Extraction:** Convert text into numerical features.
- **Classification:** Apply machine learning algorithms to classify sentiment.
- **Evaluation:** Assess the model's performance.


### **Applications of Sentiment Analysis**  
✅ Customer feedback analysis  
✅ Brand reputation monitoring  
✅ Market research and product improvement  
✅ Political and social trend analysis  

---

### Q10. Write short note on PyTorch and Colab. [5]


### **PyTorch and Google Colab**  

#### **1. PyTorch**  
✅ **What is PyTorch?**  
- PyTorch is an **open-source deep learning framework** developed by **Facebook AI Research (FAIR)**. - It is widely used for building and training neural networks due to its ease of use, flexibility and strong GPU support.  
- It supports both **CPU and GPU** computations, making it suitable for various applications.
- It is widely used in research and industry for tasks such as image recognition, natural language processing, and more.
- It provides a **flexible and intuitive** interface for building and training neural networks.
- Common pytorch modules include torch, torch.nn, torch.optim, and torch.utils.data.


#### **2. Google Colab**  
✅ **What is Google Colab?**  
Google Colab (Colaboratory) is a **free cloud-based Jupyter Notebook** environment that allows users to write and execute Python code, especially for **machine learning and deep learning** without needing to set up a local environment.
- It is based on Jupyter Notebook, a web-based interactive computing environment.

✅ **Key Features of Google Colab:**  
- **Free GPU & TPU Access:** Train deep learning models without needing expensive hardware.  
- **Pre-installed Libraries:** Comes with TensorFlow, PyTorch, OpenCV, etc.  
- **Cloud Storage Integration:** Supports Google Drive for saving/loading files.  
- **Easy Collaboration:** Share notebooks like Google Docs.  
- **No Installation Required:** Runs in a web browser.  

---

