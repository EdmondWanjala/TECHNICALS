            MACHINE LEARNING (ML
Machine Learning (ML) is a branch of Artificial Intelligence that enables computer systems to learn patterns and relationships from data and use the learned information to make predictions, classifications or decisions without explicitly programming every rule.
  Objectives of Machine Learning;
- Identify patterns and relationships in datasets.
- Predict unknown or future outcomes.
- Automate decision-making.
- Detect abnormalities and unusual behaviour.
- Improve system performance through experience.
- Extract useful information from large datasets.
  Basic ML terminology;
1. Dataset: A collection of data used to develop and evaluate a model.
2. Sample/Instance: A single observation or record in a dataset.
3. Feature: An input variable used by a model.
4. Label/Target: The output value a model is expected to predict.
5. Model: A mathematical or computational representation of learned relationships.
6. Algorithm: The procedure used to train or construct a model.
7. Parameters: Internal values learned during training, such as weights and biases.
8. Hyperparameters: Settings chosen before or during training, such as learning rate and tree depth.
9. Training: The process of learning model parameters from data.
10. Inference: Using a trained model to make predictions on new data.
11. Epoch: One complete pass through the training dataset.
12. Batch: A subset of training data processed in one training step.

 TYPES OF MACHINE LEARNING
  SUPERVISED LEARNING;
Supervised learning trains a model using labelled data, where each input has a known correct output.
The objective is to learn a mapping:
    y = f(X)
Where X represents input features and y represents the target output.
 Two main tasks:
1.Classification
Predicts discrete categories or classes.
Examples:
- Email: spam or not spam.
- Medical image: normal or abnormal.
- Machine condition: faulty or operational.
- Object recognition: car, person or bicycle.
Common algorithms:
- Logistic Regression.
- Decision Trees.
- Random Forest.
- Support Vector Machines.
- k-Nearest Neighbours.
- Naive Bayes.
- Neural Networks.
2.Regression
Predicts continuous numerical values.
Examples:
- Predicting electricity consumption.
- Estimating equipment temperature.
- Forecasting product demand.
- Predicting house prices.
- Estimating battery remaining life.
Common algorithms:
- Linear Regression.
- Polynomial Regression.
- Decision Tree Regression.
- Random Forest Regression.
- Support Vector Regression.
  UNSUPERVISED LEARNING;
Unsupervised learning discovers patterns, structures and relationships in unlabelled datasets.
There are no predefined target outputs.
 Main tasks:
1.Clustering
Groups similar data points based on their characteristics.
Examples:
- Grouping customers by purchasing behaviour.
- Grouping machines by operating patterns.
- Identifying similar sensor readings.
Algorithms:
- K-means.
- Hierarchical Clustering.
- DBSCAN.
2.Dimensionality Reduction
Reduces the number of input features while retaining as much useful information as possible.
Applications:
- Data visualization.
- Noise reduction.
- Feature compression.
- Simplifying complex datasets.
Algorithm: Principal Component Analysis (PCA).
3.Anomaly Detection
Identifies observations that differ significantly from normal patterns.
Applications:
- Fraud detection.
- Network intrusion detection.
- Fault detection in industrial machines.
- Abnormal sensor readings.
  SEMI-SUPERVISED LEARNING;
Combines a small amount of labelled data with a larger amount of unlabelled data.
Useful when collecting data is easy but manually labelling it is expensive.
Applications:
- Medical image classification.
- Speech recognition.
- Industrial defect detection.
  SELF-SUPERVISED LEARNING;
Learns representations by generating supervisory signals from the data itself.
For example, a language model learns to predict missing or next words using text data.
Applications:
- Language models.
- Image representation learning.
- Speech processing.
  REINFORCEMENT LEARNING;
An agent learns by interacting with an environment and receiving rewards or penalties for its actions.
Important components:
- Agent: Decision-making system.
- Environment: The world in which the agent operates.
- State: Current condition of the environment.
- Action: An operation performed by the agent.
- Reward: Feedback received after an action.
- Policy: Strategy used to choose actions.
Applications:
- Robot navigation.
- Autonomous systems.
- Industrial process control.
- Resource optimization.

 MACHINE LEARNING WORKFLOW
A typical ML development process follows these stages:
  Problem definition;
- Identify the problem.
- Determine the desired output.
- Select appropriate evaluation metrics.
  Data collection;
- Sensors and IoT devices.
- Databases.
- APIs.
- Images and videos.
- Files and external datasets.
  Data preprocessing;
Preparing raw data for model training.
Common operations:
- Handling missing values.
- Removing duplicates.
- Correcting inconsistent data.
- Detecting and handling outliers.
- Encoding categorical variables.
- Normalizing or standardizing numerical features.
  Exploratory Data Analysis (EDA);
Examining data to understand its characteristics.
Methods:
- Statistical summaries.
- Histograms.
- Scatter plots.
- Correlation matrices.
- Box plots.
  Feature engineering;
Selecting, transforming or creating useful input variables to improve model performance.
Examples:
- Extracting temperature averages from sensor readings.
- Converting dates into day, month and hour features.
- Extracting frequency-domain features from vibration signals.
  Dataset splitting;
- Training set: Used to learn model parameters.
- Validation set: Used for model selection and hyperparameter tuning.
- Test set: Used for final evaluation on unseen data.
  Model selection;
Choose an algorithm appropriate for the problem, data size, complexity and available resources.
  Model training;
The algorithm learns parameters from the training dataset.
  Model evaluation;
Assess how well the model performs using appropriate metrics.
  Hyperparameter tuning;
Adjust settings to improve performance.
  Deployment;
Integrate the trained model into an application, cloud service or edge device.
 Monitoring and maintenance;
Monitor accuracy, latency, data drift and reliability. Retrain or update the model when necessary.

 IMPORTANT MACHINE LEARNING ALGORITHMS
  LINEAR REGRESSION;
A supervised learning algorithm used to predict continuous numerical values by modelling a linear relationship between input variables and an output.
Simple linear regression:
    y = mx + c
Where:
- y = predicted output.
- x = input variable.
- m = slope.
- c = intercept.
Multiple linear regression:
    ŷ = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ
Applications:
- Temperature prediction.
- Energy consumption forecasting.
- Equipment performance estimation.
  LOGISTIC REGRESSION;
A supervised classification algorithm that estimates the probability of an observation belonging to a particular class.
Uses the sigmoid function:
    P(y=1|x) = 1/(1 + e⁻ᶻ)
Where z = wᵀx + b.
Applications:
- Fault classification.
- Disease prediction.
- Spam detection.
  DECISION TREES;
A supervised learning algorithm that makes predictions through a sequence of decision rules.
Structure:
- Root node: First decision.
- Internal nodes: Decision conditions.
- Branches: Outcomes of decisions.
- Leaf nodes: Final predictions.
Applications:
- Fault diagnosis.
- Risk classification.
- Predictive maintenance.
Advantages:
- Easy to interpret.
- Handles numerical and categorical features.
- Requires relatively little preprocessing.
Limitation: Deep trees can overfit training data.
  RANDOM FOREST;
An ensemble learning algorithm that combines multiple decision trees to improve prediction performance.
- Classification: Uses voting among trees.
- Regression: Commonly averages predictions.
Advantages:
- Reduces the variance of individual decision trees.
- Handles complex relationships.
- Often performs well with limited feature engineering.
Applications:
- Fault detection.
- Classification of sensor data.
- Predictive maintenance.
  SUPPORT VECTOR MACHINE (SVM);
A supervised algorithm that finds a decision boundary (hyperplane) separating different classes while maximizing the margin between them.
A kernel function can enable nonlinear classification.
Applications:
- Image classification.
- Fault diagnosis.
- Pattern recognition.
  K-NEAREST NEIGHBOURS (K-NN);
A supervised algorithm that predicts an observation using the labels or values of its K closest training examples.
Working principle:
1. Select K.
2. Calculate distances between the new sample and training samples.
3. Identify the K nearest neighbours.
4. Classification: Use majority voting.
5. Regression: Use an average or weighted average.
Common distance metric — Euclidean distance:
    d(x,y) = √Σ(xᵢ − yᵢ)²
Applications:
- Pattern recognition.
- Classification.
- Similarity-based recommendation.
  K-MEANS CLUSTERING;
An unsupervised algorithm that divides data into K clusters based on similarity.
Working principle:
1. Choose the number of clusters K.
2. Initialize K centroids.
3. Assign each data point to its nearest centroid.
4. Recalculate centroids.
5. Repeat until assignments or centroids stabilize.
Objective function:
    J = Σₖ₌₁ᴷ Σₓᵢ∈Cₖ ||xᵢ − μₖ||²
Where μₖ is the centroid of cluster k.
Applications:
- Customer segmentation.
- Sensor behaviour grouping.
- Industrial operating-state identification.
  NAIVE BAYES;
A probabilistic classification algorithm based on Bayes' theorem and the assumption that features are conditionally independent given the class.
Bayes' theorem:
    P(A|B) = [P(B|A)P(A)]/P(B)
Applications:
- Text classification.
- Spam filtering.
- Basic document categorization.
  PRINCIPAL COMPONENT ANALYSIS (PCA);
An unsupervised dimensionality-reduction technique that transforms correlated variables into a smaller set of uncorrelated variables called principal components.
The first principal component captures the greatest possible variance; subsequent components capture the greatest remaining variance subject to orthogonality.
Applications:
- Data compression.
- Visualization.
- Noise reduction.
- Feature extraction.

 MODEL TRAINING AND OPTIMIZATION
Training involves adjusting model parameters to minimize a loss function.
  Loss function;
Measures the difference between model predictions and actual values.
Common loss functions:
Mean Squared Error (MSE)
    MSE = (1/n)Σ(yᵢ − ŷᵢ)²
Used mainly for regression.
Mean Absolute Error (MAE)
    MAE = (1/n)Σ|yᵢ − ŷᵢ|
Measures the average absolute prediction error.
Binary Cross-Entropy
    L = −(1/n)Σ[yᵢlog(pᵢ) + (1−yᵢ)log(1−pᵢ)]
Used for binary classification.
  Gradient Descent;
An optimization algorithm that updates model parameters in the direction that reduces the loss.
    θₙ₊₁ = θₙ − η∇L(θₙ)
Where:
- θ = model parameters.
- η = learning rate.
- ∇L = gradient of the loss function.
Types:
1. Batch Gradient Descent: Uses the entire training dataset for each update.
2. Stochastic Gradient Descent (SGD): Uses one training example per update.
3. Mini-batch Gradient Descent: Uses a small batch of examples per update.
  Learning rate;
Controls the size of parameter updates.
- Too high: Training may become unstable or fail to converge.
- Too low: Training may be extremely slow.
  Regularization;
Techniques that discourage unnecessarily complex models and reduce overfitting.
- L1 regularization (Lasso): Encourages some parameters to become exactly zero.
- L2 regularization (Ridge): Penalizes large squared parameter values.
- Dropout: Randomly disables selected neural-network units during training.

 MODEL EVALUATION
Evaluation determines whether a trained model performs adequately on unseen data.
  Classification metrics;
Let:
- TP = True Positive.
- TN = True Negative.
- FP = False Positive.
- FN = False Negative.
Accuracy:
    Accuracy = (TP + TN)/(TP + TN + FP + FN)
Precision:
    Precision = TP/(TP + FP)
Recall (Sensitivity):
    Recall = TP/(TP + FN)
Specificity:
    Specificity = TN/(TN + FP)
F1-score:
    F1 = 2 × (Precision × Recall)/(Precision + Recall)
Confusion matrix: A table comparing actual classes with predicted classes.
ROC curve: Plots true positive rate against false positive rate at different classification thresholds.
AUC: Area under the ROC curve; measures the model's ability to rank positive examples above negative examples.
  Regression metrics;
Mean Squared Error:
    MSE = (1/n)Σ(yᵢ − ŷᵢ)²
Root Mean Squared Error:
    RMSE = √MSE
Mean Absolute Error:
    MAE = (1/n)Σ|yᵢ − ŷᵢ|
Coefficient of determination:
    R² = 1 − [Σ(yᵢ − ŷᵢ)² / Σ(yᵢ − ȳ)²]
R² measures the proportion of target variance explained relative to a mean-prediction baseline. It can be negative on test data.

 OVERFITTING, UNDERFITTING AND GENERALIZATION
  Overfitting;
Occurs when a model learns training data too closely, including noise and irrelevant patterns.
Symptoms:
- Very high training accuracy.
- Poor validation or test accuracy.
Solutions:
- Increase representative training data.
- Apply regularization.
- Reduce model complexity.
- Use early stopping.
- Apply data augmentation where appropriate.
  Underfitting;
Occurs when a model is too simple or insufficiently trained to learn important patterns.
Symptoms:
- Poor training performance.
- Poor test performance.
Solutions:
- Increase model complexity.
- Improve feature representation.
- Train for longer when appropriate.
- Reduce excessive regularization.
  Generalization;
The ability of a model to perform accurately on previously unseen data.
Cross-validation: 
A method of evaluating model performance using multiple training and validation splits. 
K-fold cross-validation divides the dataset into K parts and rotates the validation fold.
Important: 
Data leakage occurs when information unavailable at prediction time influences model training or evaluation. 
Fit preprocessing transformations only on training data, then apply them to validation and test data.

 FEATURE ENGINEERING AND DATA PREPROCESSING
  Feature scaling;
Normalization (Min-Max scaling)
    x' = (x − x_min)/(x_max − x_min)
Typically maps values into the range [0,1].
Standardization (Z-score)
    z = (x − μ)/σ
Produces features with mean approximately zero and standard deviation approximately one.
  Categorical encoding;
- Label encoding: Assigns integer codes to categories.
- One-hot encoding: Creates binary columns representing categories.
  Missing data handling;
- Remove observations when justified.
- Replace missing values using mean, median or mode.
- Use more advanced imputation methods where necessary.
  Outlier detection;
Methods include:
- Interquartile Range (IQR).
- Z-score.
- Isolation Forest.
- Local Outlier Factor.
Preprocessing must be appropriate to the data and algorithm. 
For example, scaling is especially important for distance-based algorithms such as K-NN and SVM.

 ENSEMBLE LEARNING
Ensemble learning combines predictions from multiple models to improve performance.
  Bagging;
Trains multiple models on bootstrap samples and combines their predictions.
Example: Random Forest.
  Boosting;
Trains models sequentially, with later models focusing on errors made by earlier ones.
Examples:
- AdaBoost.
- Gradient Boosting.
- XGBoost.
  Stacking;
Combines predictions from multiple base models using another model called a meta-learner.
Main benefits:
- Improved predictive performance.
- Reduced variance in some methods.
- Better handling of complex patterns.

 TIME-SERIES MACHINE LEARNING
Time-series data consists of observations recorded sequentially over time.
Examples:
- Temperature readings.
- Electricity consumption.
- Stock prices.
- Motor vibration.
- Network traffic.
  Important characteristics:;
- Trend: Long-term upward or downward movement.
- Seasonality: Repeating patterns at fixed intervals.
- Cyclic behaviour: Longer-term fluctuations without necessarily fixed periods.
- Noise: Random variation.
  Methods:
- Linear regression with time features.
- Decision-tree-based forecasting.
- ARIMA and related statistical models.
- RNN, LSTM and GRU networks.
- Transformer-based forecasting models.
Important: Preserve chronological order when splitting time-series datasets. 
Random splitting can cause future information to leak into training.

 MACHINE LEARNING IN ENGINEERING APPLICATIONS
  Predictive maintenance;
Uses machine sensor data to estimate equipment condition and identify possible failures before they occur.
Inputs: Vibration, temperature, pressure and current.
Outputs: Fault classification, anomaly score or remaining useful life estimate.
  Electronics and embedded systems;
- Component fault classification.
- Battery health estimation.
- Intelligent power management.
- Sensor calibration.
  Robotics;
- Object recognition.
- Obstacle detection.
- Navigation.
- Motion prediction.
- Intelligent manipulation.
  Industrial automation;
- Automated quality inspection.
- Production optimization.
- Process monitoring.
- Defect detection.
  IoT systems;
- Smart environmental monitoring.
- Energy consumption prediction.
- Intelligent sensor networks.
- Anomaly detection.
  Computer vision;
- Object detection.
- Image classification.
- Face recognition.
- Visual inspection.
  Communication and networking;
- Network traffic prediction.
- Intrusion detection.
- Resource allocation.
- Signal classification.

 MACHINE LEARNING AND EDGE AI
Machine Learning models can be deployed on edge devices to perform inference locally.
  Deployment process;
1. Collect and prepare training data.
2. Train the model on a suitable development computer or server.
3. Evaluate its accuracy and reliability.
4. Optimize the model for the target device.
5. Convert it to a compatible model format.
6. Deploy it to an edge processor.
7. Run inference using live sensor or application data.
8. Monitor performance and update the model when necessary.
  Model optimization techniques;
Quantization: Reduces the numerical precision of model parameters and/or activations, for example FP32 to INT8.
Pruning: Removes less important model weights or structures.
Knowledge distillation: Trains a smaller student model to reproduce a larger teacher model's behaviour.
Model compression: Reduces storage requirements through techniques such as quantization and pruning.
  Deployment tools and frameworks
- Scikit-learn: Traditional ML algorithms.
- TensorFlow: ML and deep-learning development.
- PyTorch: Deep-learning model development.
- TensorFlow Lite / LiteRT: Lightweight inference on supported edge platforms.
- ONNX: Interoperable model representation.
- ONNX Runtime: Model inference across supported platforms.
- OpenCV: Computer vision and image processing.
- Edge Impulse: Embedded ML development and deployment workflows.

 LIMITATIONS AND CHALLENGES OF MACHINE LEARNING
1. Data dependency: Poor-quality or insufficient data produces unreliable models.
2. Bias: Biased training data can produce unfair predictions.
3. Overfitting: Models may fail on unseen data.
4. Computational cost: Complex models require substantial computing resources.
5. Interpretability: Some models are difficult to explain.
6. Data privacy: Sensitive information requires protection.
7. Model drift: Changing environments can reduce predictive accuracy.
8. Security: Models may be vulnerable to adversarial inputs and attacks.
9. Deployment constraints: Memory, power, latency and hardware compatibility can limit practical use.

 IMPORTANT EXAM AND PRACTICAL TIPS
1. Understand the difference between AI, ML and Deep Learning.
2. Know the five learning approaches: supervised, unsupervised, semi-supervised, self-supervised and reinforcement learning.
3. Classification predicts categories; regression predicts numerical values.
4. Know the principles, advantages and limitations of major ML algorithms.
5. Understand the difference between model parameters and hyperparameters.
6. Understand training, validation and testing.
7. Know the purpose of loss functions and gradient descent.
8. Distinguish overfitting from underfitting.
9. Understand accuracy, precision, recall, F1-score, MAE, MSE and RMSE.
10. Know why data preprocessing and feature engineering are important.
11. Understand ensemble learning, clustering and dimensionality reduction.
12. For Edge AI, consider accuracy, memory, latency, energy consumption and hardware compatibility.
13. Always evaluate models on data that was not used to train or tune them.