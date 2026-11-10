                EMBEDDED AI
Embedded AI (Edge AI) is the integration of Artificial Intelligence and Machine Learning algorithms into embedded systems so that devices can process data, make predictions and perform intelligent actions locally, without necessarily depending on cloud computing.
  It combines:
- Embedded hardware: Microcontrollers (MCUs), microprocessors and sensors.
- Software: Firmware, operating systems and AI frameworks.
- Machine Learning: Algorithms that learn patterns from data.
- Communication: Interfaces for exchanging data with other devices.
  Examples:
- Smart cameras that detect objects.
- Wearable devices that recognize activities.
- Predictive maintenance systems that detect machine faults.
- Autonomous robots that navigate their environment.
- Smart agriculture systems that identify plant diseases.

 Embedded AI Architecture
  A typical embedded AI system follows this process:
1. Data acquisition: Sensors collect environmental or physical data.
2. Preprocessing: Raw data is filtered, normalized and prepared.
3. AI inference: A trained model analyzes the input and produces a prediction.
4. Decision-making: The system determines the appropriate response.
5. Actuation: Motors, relays or other actuators execute the response.
6. Communication: Results may be transmitted to other devices or cloud platforms.
  Basic architecture:
Sensors → Data acquisition → Preprocessing → AI model → Decision-making → Actuators

 Artificial Intelligence, Machine Learning and Deep Learning
  Artificial Intelligence (AI):
A broad field of computer science concerned with creating systems capable of performing tasks that normally require human intelligence.
  Machine Learning (ML):
A branch of AI in which systems learn patterns from data to make predictions or decisions without explicitly programming every rule.
  Deep Learning (DL):
A branch of machine learning that uses multilayer artificial neural networks to learn complex patterns.
  TinyML:
The implementation of machine learning models on resource-constrained devices, particularly microcontrollers, with limited memory, processing power and energy.

 Types of Machine Learning
  Supervised Learning;
The model learns from labelled training data, where inputs have known outputs.
Applications:
- Image classification.
- Fault detection.
- Temperature prediction.
- Speech recognition.
Common algorithms:
- Linear regression.
- Logistic regression.
- Decision trees.
- Support Vector Machines (SVM).
- Neural networks.
  Unsupervised Learning;
The model learns patterns from unlabelled data.
Applications:
- Anomaly detection.
- Sensor data clustering.
- Identifying unusual machine behaviour.
Common algorithms:
- K-means clustering.
- Principal Component Analysis (PCA).
- Autoencoders.
  Reinforcement Learning;
An agent learns by interacting with an environment and receiving rewards or penalties.
Applications:
- Robot navigation.
- Autonomous control.
- Adaptive decision-making.

 Neural Networks
An Artificial Neural Network (ANN) is a computational model inspired by biological neural systems.
  It consists of:
- Input layer: Receives input features.
- Hidden layers: Process and learn patterns.
- Output layer: Produces predictions or classifications.
A neuron calculates a weighted sum of inputs and applies an activation function.
Neuron equation:
    z = Σ(wᵢxᵢ) + b
    y = f(z)
Where:
- xᵢ = Input features.
- wᵢ = Corresponding weights.
- b = Bias.
- f(z) = Activation function.
- y = Neuron output.
  Common activation functions:
ReLU:
    f(x) = max(0, x)
Sigmoid:
    f(x) = 1 / (1 + e⁻ˣ)
Softmax:
    Pᵢ = eᶻⁱ / Σⱼeᶻʲ
Applications:
- ReLU: Hidden neural network layers.
- Sigmoid: Binary classification outputs.
- Softmax: Multi-class classification.

 AI Model Training and Inference
Model training is the process of teaching a machine learning model using data so that it learns relationships and patterns.
Training normally occurs on a computer with greater processing power.
  Main stages:
1. Collect and label datasets.
2. Clean and preprocess data.
3. Divide data into training, validation and testing sets.
4. Select an appropriate algorithm.
5. Train the model.
6. Evaluate accuracy and performance.
7. Optimize and export the model.
Model inference is the process of using a trained model to make predictions from new input data.
In embedded AI, inference is commonly performed directly on the microcontroller or edge processor.
  Important distinction:
- Training: Learning model parameters.
- Inference: Using learned parameters to make predictions.

 Embedded AI Hardware
Embedded AI requires hardware capable of executing machine learning operations within limited resources.
  Microcontrollers (MCUs);
Examples:
- ESP32.
- STM32.
- Arduino-compatible microcontrollers.
- Raspberry Pi Pico.
Characteristics:
- Low power consumption.
- Limited RAM and flash memory.
- Integrated peripherals.
- Suitable for small AI models.
  Microprocessors (MPUs);
Examples:
- ARM Cortex-A processors.
- Raspberry Pi application processors.
They generally offer greater processing capability and can run full operating systems such as Linux.
  AI Accelerators;
Specialized hardware designed to accelerate AI computations.
Examples:
- Neural Processing Units (NPUs).
- Digital Signal Processors (DSPs).
- GPUs.
- Dedicated AI accelerator chips.
Hardware selection factors:
- Processing speed.
- RAM and flash capacity.
- Power consumption.
- AI model size.
- Sensor and communication interfaces.
- Cost and operating environment.

 TinyML and Model Optimization
TinyML enables machine learning on small embedded devices with limited computational resources.
Because microcontrollers have limited memory and processing power, AI models must be optimized.
Important optimization techniques:
  Quantization;
Reduces the numerical precision used to represent model parameters.
For example:
- 32-bit floating point (FP32).
- 16-bit floating point (FP16).
- 8-bit integer (INT8).
Benefits:
- Reduces model size.
- Reduces memory usage.
- Can improve inference speed.
- May reduce energy consumption.
  Pruning;
Removes unnecessary or less important neural network connections and parameters.
Benefits:
- Reduces computational complexity.
- Reduces model storage requirements.
  Knowledge Distillation;
Transfers knowledge from a large, complex teacher model to a smaller student model.
  Model Compression;
Reduces the storage and computational requirements of a model through techniques such as quantization and pruning.
  Efficient Architecture Design;
Uses lightweight models designed for resource-constrained hardware.
Examples include MobileNet and compact neural networks.

 Embedded AI Software and Frameworks
  Important development tools include:
- TensorFlow: Machine learning framework used to develop and train models.
- TensorFlow Lite for Microcontrollers: Framework for running optimized models on microcontrollers.
- Edge Impulse: Platform for collecting sensor data, training models and deploying embedded AI applications.
- PyTorch: Machine learning framework for model development and training.
- ONNX: Open Neural Network Exchange format for model interoperability.
- CMSIS-NN: Optimized neural network kernels for Arm Cortex-M processors.
  Typical development workflow:
1. Collect sensor data.
2. Train a model using Python and an ML framework.
3. Optimize and convert the model.
4. Deploy the model to the embedded device.
5. Integrate it with firmware.
6. Test inference performance on the actual hardware.

 Important Equations and Performance Metrics
  Accuracy;
Accuracy = Correct predictions / Total predictions
Percentage accuracy:
Accuracy (%) = (Correct predictions / Total predictions) × 100
  Precision;
Precision = TP / (TP + FP)
Measures how many positive predictions are actually positive.
  Recall;
Recall = TP / (TP + FN)
Measures how many actual positive cases the model correctly identifies.
  F1-score;
F1 = 2 × (Precision × Recall) / (Precision + Recall)
Balances precision and recall.
Where:
- TP = True Positives.
- TN = True Negatives.
- FP = False Positives.
- FN = False Negatives.
  Inference Latency;
Latency = Output time − Input processing start time
Measures the time required to produce an AI prediction.
  Throughput;
Throughput = Number of inferences / Total processing time
Measures how many predictions can be performed per unit time.
  Memory Requirement
Total memory ≈ Model memory + Runtime memory + Input/output buffers + Application memory.
The actual memory requirement depends on the framework and execution method.
  Power Consumption;
P = V × I
Where:
- P = Power (W).
- V = Voltage (V).
- I = Current (A).
  Energy consumption:
E = P × t
Where t is operating time.

 Real-Time Embedded AI
Embedded AI systems frequently operate under real-time constraints.
A real-time AI system must generate and act on predictions within an acceptable time limit.
Important considerations:
- Inference latency.
- Processing deadlines.
- Sensor sampling frequency.
- Scheduling.
- Memory availability.
- Interrupt handling.
- Predictable execution time.
For example, an obstacle-detection robot must identify an obstacle and respond quickly enough to avoid a collision.
Important: High AI accuracy alone does not guarantee a reliable real-time system. Prediction speed and timing guarantees also matter.

 Edge AI vs Cloud AI
  Edge AI:
AI processing occurs locally on the embedded device or nearby edge hardware.
Advantages:
- Low communication latency.
- Reduced dependence on internet connectivity.
- Improved privacy because data can remain local.
- Reduced cloud bandwidth requirements.
- Faster local decision-making.
Limitations:
- Limited computational resources.
- Restricted memory.
- Difficult model updates.
- Limited ability to run large models.
  Cloud AI:
AI processing occurs on remote cloud servers.
Advantages:
- Large computational resources.
- Supports complex AI models.
- Centralized storage and model management.
- Easier access to large datasets.
Limitations:
- Requires network connectivity.
- Communication delays.
- Higher bandwidth requirements.
- Potential privacy and security concerns.

 Applications of Embedded AI
  Robotics;
- Object detection.
- Obstacle avoidance.
- Gesture recognition.
- Intelligent navigation.
  Industrial Automation;
- Predictive maintenance.
- Equipment fault detection.
- Quality inspection.
- Intelligent process monitoring.
  Smart Agriculture;
- Plant disease detection.
- Soil condition monitoring.
- Automated irrigation.
- Crop monitoring.
  Healthcare and Wearables;
- Activity recognition.
- Abnormal movement detection.
- Wearable monitoring.
- Intelligent health-device processing.
  Smart Homes;
- Voice recognition.
- Occupancy detection.
- Intelligent security systems.
- Energy management.
  Automotive Systems;
- Driver monitoring.
- Lane detection.
- Object recognition.
- Intelligent sensor processing.

 Challenges in Embedded AI
1. Limited memory: Models must fit available RAM and flash.
2. Limited processing power: Complex neural networks may be too demanding.
3. Power constraints: Battery-operated devices require energy-efficient inference.
4. Model accuracy: Compression may reduce prediction accuracy.
5. Real-time requirements: Predictions must meet deadlines.
6. Data quality: Poor sensor data reduces model reliability.
7. Security: Models and device data must be protected.
8. Environmental conditions: Temperature, vibration and electrical noise can affect hardware and sensor measurements.
9. Model updates: Deployed devices need safe and reliable model maintenance.

 Practical Embedded AI Development Example
Project: Intelligent Temperature-Based Fault Detection
Objective: Detect abnormal machine temperature using an embedded AI device.
Required components:
- ESP32 or STM32 microcontroller.
- Temperature sensor.
- LED or buzzer.
- Computer for model training.
- Embedded AI framework.
Working principle:
1. The temperature sensor measures machine temperature.
2. The microcontroller reads and preprocesses the sensor data.
3. The trained AI model analyzes the readings.
4. The model classifies the machine condition as normal or abnormal.
5. If an abnormal condition is detected, the controller activates an alarm.
6. The system may transmit the fault information to an IoT platform.
Example output:
- Normal: Machine operates normally.
- Abnormal: Warning alarm activated.
This demonstrates how sensing, machine learning, embedded processing and actuation work together.

 Important Examination and Practical Tips
- Understand the difference between AI, ML, deep learning and TinyML.
- Distinguish model training from model inference.
- Understand the complete embedded AI architecture.
- Know the functions of sensors, MCUs, processors and AI accelerators.
- Understand quantization, pruning and knowledge distillation.
- Know the difference between edge AI and cloud AI.
- Be able to calculate accuracy, precision, recall, F1-score, power and energy.
- Consider memory, processing speed, power consumption and latency when selecting hardware.
- Remember that a model must be tested on its actual target hardware.
- For real-time applications, evaluate both prediction accuracy and execution time.

KEY TAKEAWAY:
Embedded AI combines embedded hardware, sensors, firmware and machine learning to create intelligent devices capable of processing information and making decisions locally. 
TinyML makes this possible even on resource-constrained microcontrollers through lightweight models and optimization techniques.