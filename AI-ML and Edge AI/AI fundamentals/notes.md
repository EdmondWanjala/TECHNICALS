                AI FUNDAMENTALS
Artificial Intelligence (AI) is the field of computer science concerned with creating systems capable of performing tasks that normally require human intelligence, such as reasoning, learning, perception, language understanding, decision-making and problem-solving.
Objectives of AI;
- Automate repetitive and complex tasks.
- Learn patterns from data and improve performance.
- Make predictions and support decision-making.
- Interpret images, speech, text and sensor data.
- Enable autonomous systems such as robots and intelligent vehicles.
Types of AI by capability;
1. Narrow AI (ANI): Designed for specific tasks, e.g., face recognition, translation and recommendation systems. Most existing AI belongs to this category.
2. General AI (AGI): A hypothetical system capable of performing a broad range of intellectual tasks at human-like flexibility.
3. Superintelligent AI (ASI): A hypothetical intelligence exceeding human capabilities across most domains.
Major AI subfields;
- Machine Learning (ML): Learns patterns from data.
- Deep Learning (DL): Uses multilayer neural networks.
- Computer Vision: Interprets images and videos.
- Natural Language Processing (NLP): Processes and generates human language.
- Robotics: Combines perception, planning and physical action.
- Knowledge Representation and Reasoning: Represents facts and derives conclusions.
- Expert Systems: Apply encoded rules and domain knowledge.

 MACHINE LEARNING (ML):
Machine Learning is a branch of AI in which algorithms learn patterns from data to make predictions or decisions without requiring every rule to be explicitly programmed.
Basic ML workflow;
1. Define the problem and performance objective.
2. Collect relevant, representative data.
3. Clean data and handle missing values, noise and duplicates.
4. Select useful features and prepare the dataset.
5. Split data into training, validation and test sets.
6. Select and train a model.
7. Evaluate performance using appropriate metrics.
8. Tune hyperparameters and compare models.
9. Deploy the model.
10. Monitor accuracy, latency, drift and reliability; retrain when necessary.
Supervised Learning;
Learns a mapping from labelled examples (input X and known target y).
- Classification: Predicts categories, e.g., defective/non-defective products or spam/not spam.
- Regression: Predicts continuous numerical values, e.g., temperature, energy consumption or house prices.
Examples of algorithms:
- Linear and logistic regression.
- Decision trees and random forests.
- Support Vector Machines (SVM).
- k-Nearest Neighbours (k-NN).
- Neural networks.
Unsupervised Learning;
Discovers structures in unlabelled data.
- Clustering: Groups similar observations, e.g., customer segmentation.
- Dimensionality reduction: Reduces the number of features while preserving useful information.
- Anomaly detection: Identifies unusual observations.
Examples: k-means clustering, Principal Component Analysis (PCA) and selected anomaly-detection algorithms.
Semi-supervised Learning;
Uses a small labelled dataset together with a larger unlabelled dataset. Useful when labelling data is expensive.
Self-supervised Learning;
Creates training targets from the data itself. Commonly used to pretrain language, image and audio models.
Reinforcement Learning (RL);
An agent interacts with an environment, receives rewards or penalties and learns a policy that maximizes cumulative reward.
Key terms:
- Agent: The learner or decision-maker.
- Environment: The system with which the agent interacts.
- State (s): Current situation.
- Action (a): Decision made by the agent.
- Reward (r): Feedback from an action.
- Policy (π): Strategy for selecting actions.
Applications: Robotics, game-playing, resource allocation and control systems.

 DEEP LEARNING AND NEURAL NETWORKS:
Deep Learning is a subset of ML that uses neural networks with multiple processing layers to learn complex representations from data.
Artificial neuron;
A neuron computes a weighted sum of inputs, adds a bias and applies an activation function.
    z = Σ(wᵢxᵢ) + b
    a = f(z)
Where:
- xᵢ = input features.
- wᵢ = learned weights.
- b = bias.
- f(z) = activation function.
- a = neuron output.
Common activation functions;
1. ReLU: f(z) = max(0, z). Common in hidden layers.
2. Sigmoid: σ(z) = 1 / (1 + e⁻ᶻ). Outputs values between 0 and 1; useful for binary classification outputs.
3. Softmax: Converts a vector of logits into class probabilities that sum to 1.
4. Tanh: Outputs values between -1 and 1.
Main neural network components;
- Input layer: Receives features.
- Hidden layers: Learn intermediate representations.
- Output layer: Produces predictions.
- Weights and biases: Trainable parameters.
- Loss function: Measures prediction error.
- Optimizer: Updates parameters to reduce the loss.
Training process;
1. Forward propagation: Computes predictions.
2. Loss calculation: Measures prediction error.
3. Backpropagation: Computes gradients of the loss with respect to parameters.
4. Parameter update: An optimizer adjusts weights and biases.
5. Repeat over batches and epochs until the stopping criterion is met.
Gradient descent update:
    θₜ₊₁ = θₜ − η∇θL(θₜ)
Where θ represents model parameters, η is the learning rate, L is the loss function and ∇θL is its gradient.
Common architectures;
- Feedforward Neural Network (FNN): General prediction tasks.
- Convolutional Neural Network (CNN): Image and spatial-pattern recognition.
- Recurrent Neural Network (RNN): Sequential data; includes LSTM and GRU variants.
- Transformer: Uses attention mechanisms; widely used in language, vision and multimodal AI.
- Autoencoder: Learns compressed representations; used in feature learning and anomaly detection.
- Generative models: Produce new text, images, audio or other content.
AI, ML and DL relationship
AI is the broad field; ML is a subset of AI; DL is a subset of ML.

 IMPORTANT ML EQUATIONS AND METRICS:
Linear regression
    ŷ = wx + b
For multiple features:
    ŷ = wᵀx + b
Mean Squared Error (MSE):
    MSE = (1/n) Σ(yᵢ − ŷᵢ)²
MSE penalizes large prediction errors more heavily.
Logistic regression
    p(y = 1 | x) = 1 / (1 + e⁻ᶻ), where z = wᵀx + b.
Binary cross-entropy loss:
    L = −(1/n) Σ[yᵢlog(pᵢ) + (1 − yᵢ)log(1 − pᵢ)]
Classification metrics;
- Accuracy = (TP + TN)/(TP + TN + FP + FN)
- Precision = TP/(TP + FP)
- Recall = TP/(TP + FN)
- F1-score = 2 × (Precision × Recall)/(Precision + Recall)
TP = true positive; TN = true negative; FP = false positive; FN = false negative.
Accuracy can be misleading on imbalanced datasets. Precision matters when false positives are costly; recall matters when false negatives are costly.
Dataset splitting;
- Training set: Learns model parameters.
- Validation set: Supports model selection and hyperparameter tuning.
- Test set: Estimates final generalization performance.
Avoid data leakage: Test information must not influence training, feature selection or model tuning.
Overfitting and underfitting;
- Overfitting: Learns training-specific patterns or noise; performs poorly on unseen data.
- Underfitting: Model is too simple or insufficiently trained to capture the underlying patterns.
- Generalization: Ability to perform well on new, unseen data.
Ways to reduce overfitting:
- More representative training data.
- Regularization, e.g., L1 or L2.
- Dropout and data augmentation where appropriate.
- Early stopping.
- Cross-validation and simpler models.
Bias-variance trade-off: High bias is associated with underfitting; high variance is associated with sensitivity to the training data and overfitting.

 EDGE AI:
Edge AI is the execution of AI inference on or near the device where data is generated, rather than relying entirely on a remote cloud server.
Examples of edge devices:
- Microcontrollers (MCUs).
- Smartphones and tablets.
- Smart cameras.
- Industrial gateways.
- Embedded Linux computers.
- Robots, drones and IoT sensors.
Cloud AI vs Edge AI;
 Cloud AI:
- Processing occurs on remote servers.
- Supports large models and substantial computing resources.
- Often requires network connectivity.
- May incur network latency, bandwidth usage and cloud costs.
 Edge AI:;
- Processing occurs locally or near the data source.
- Can reduce response time and network traffic.
- Can continue operating during internet outages if the complete workflow is local.
- Can improve privacy by keeping raw data on the device.
- Is constrained by memory, processing power, energy and thermal limits.
Hybrid AI combines edge and cloud processing. For example, a camera detects events locally and uploads selected clips or summaries for further analysis.
 Edge AI pipeline;
1. Sensors acquire data.
2. A processor collects and preprocesses data.
3. A trained model performs local inference.
4. Post-processing converts predictions into decisions.
5. An application triggers an alert, control action or data transmission.
6. Logs or selected data may be sent to the cloud for monitoring and improvement.
Important distinction: Training learns model parameters; inference uses a trained model to make predictions. Edge devices commonly perform inference, although capable devices can also perform limited or full training.

 EDGE AI OPTIMIZATION:
Models must fit device resource limits while meeting acceptable accuracy, latency and energy requirements.
Quantization;
Represents weights and/or activations with lower numerical precision, e.g., FP32 to INT8.
Benefits
- Smaller model storage.
- Reduced memory bandwidth.
- Potentially faster inference and lower energy consumption on supported hardware.
Trade-off: Quantization may reduce accuracy. Post-training quantization and quantization-aware training are common approaches.
Pruning;
Removes less important weights, connections or structures to reduce computation or model size. Actual speed gains depend on whether the hardware and runtime exploit the resulting sparsity.
Knowledge distillation;
Trains a smaller student model to reproduce useful behaviour from a larger teacher model.
Efficient architectures;
Use compact models, fewer operations and hardware-friendly layers. Examples include MobileNet-style CNNs and compact transformer variants.
Hardware acceleration;
- CPU: General-purpose processing.
- GPU: Parallel computation.
- NPU: Neural-network acceleration.
- DSP: Signal processing and selected ML workloads.
- MCU: Low-power embedded control and tiny inference workloads.
Hardware compatibility, memory capacity and software support are as important as theoretical compute performance.
Key deployment metrics;
- Accuracy: Correctness of predictions.
- Latency: Time to produce a result.
- Throughput: Number of inferences completed per unit time.
- RAM: Memory needed during execution.
- Model size: Storage required for model parameters.
- Energy per inference: Energy consumed for each prediction.
- Power: Rate of energy consumption.

 PRACTICAL APPLICATIONS OF AI/ML AND EDGE AI:
1. Predictive maintenance: Sensors monitor vibration and temperature to identify likely machine failures.
2. Smart agriculture: Edge devices detect crop disease, monitor soil conditions and automate irrigation.
3. Industrial automation: Vision systems inspect products and identify defects on production lines.
4. Smart homes: Devices recognize events and control lighting, security and energy use.
5. Healthcare: AI assists medical-image analysis and monitoring; clinical decisions require appropriate validation and oversight.
6. Transport: Embedded models support driver assistance, object detection and traffic monitoring.
7. Environmental monitoring: Local processing identifies abnormal air quality, water quality or sound patterns.
8. Robotics: Models support perception, navigation and object manipulation.
Example: An industrial motor uses vibration and temperature sensors. An edge model estimates the probability of a fault. If a validated threshold is exceeded, the device triggers an alert and sends a summary to a monitoring server.

 RESPONSIBLE AI AND SECURITY:
- Data privacy: Collect only necessary data and protect sensitive information.
- Security: Secure model files, communications, firmware and device access.
- Fairness: Evaluate performance across relevant populations and operating conditions.
- Explainability: Provide interpretable outputs when needed for safety or accountability.
- Robustness: Test under noise, changing conditions and unexpected inputs.
- Human oversight: Preserve appropriate intervention for high-impact decisions.
- Model drift: Monitor changes in input data or the relationship between inputs and targets.
- Safety: Validate model decisions and retain independent safety controls in critical systems.
An AI model's prediction is not automatically a reliable fact. Confidence scores may be miscalibrated, and performance can degrade after deployment.

 IMPORTANT TIPS AND EXAM NOTES:
1. AI is the broad field; ML learns from data; DL uses multilayer neural networks.
2. Classification predicts categories; regression predicts numerical values.
3. Supervised learning uses labelled examples; unsupervised learning discovers structure in unlabelled data.
4. Reinforcement learning learns through actions and rewards.
5. Training updates model parameters; inference uses learned parameters.
6. Loss measures model error; an optimizer updates parameters to reduce it.
7. Overfitting harms generalization; underfitting indicates inadequate learning or model capacity.
8. Edge AI reduces dependence on cloud connectivity but does not automatically guarantee privacy, security or low latency.
9. Quantization reduces numerical precision; pruning removes model components; distillation transfers behaviour from a teacher to a student.
10. Choose an edge model based on accuracy, latency, RAM, storage, energy, hardware compatibility and safety requirements—not accuracy alone.

END OF NOTES