            COMPUTER VISION (CV)
Computer Vision is a field of AI concerned with enabling machines to understand and interpret visual information from the physical world using cameras, images and video-processing systems.
  Main objectives;
- Detect and recognize objects.
- Classify images into categories.
- Identify and track moving objects.
- Estimate distance, position and movement.
- Understand scenes and environments.
- Extract useful information from visual data.
- Support autonomous decision-making.
  Computer Vision vs Image Processing;
Image Processing: Focuses on manipulating or improving images, such as filtering, resizing, sharpening and noise removal.
Computer Vision: Focuses on interpreting images to extract meaningful information, such as identifying objects, recognizing faces and estimating motion.
Image processing is often a component of a computer vision system.
  Applications;
- Autonomous vehicles.
- Facial recognition.
- Medical image analysis.
- Industrial inspection.
- Robotics and navigation.
- Surveillance and security.
- Agricultural monitoring.
- Augmented and virtual reality.
- Optical character recognition (OCR).

 COMPUTER VISION SYSTEM ARCHITECTURE
A typical computer vision system follows these stages:
1. Image acquisition: Capturing visual data using a camera or imaging sensor.
2. Preprocessing: Improving image quality and preparing data.
3. Segmentation: Separating objects or regions of interest.
4. Feature extraction: Identifying useful visual characteristics.
5. Feature representation: Converting visual information into numerical representations.
6. Recognition and classification: Identifying objects or image categories.
7. Interpretation: Understanding spatial relationships and scene information.
8. Decision and action: Producing an output, alert or control instruction.
Example: An industrial inspection camera captures a product, processes the image, detects defects and sends a rejection signal to an automated sorting mechanism.

 IMAGE FUNDAMENTALS
An image is a two-dimensional representation of visual information.
  Pixels;
A pixel (picture element) is the smallest addressable element of a digital image.
A digital image consists of a grid of pixels, each containing intensity or colour information.
  Image resolution;
Resolution describes the number of pixels in an image.
For example:
1920 × 1080 = 2,073,600 pixels.
Higher resolution can preserve more visual detail but generally requires more storage, memory and processing.
  Types of digital images;
1. Binary image
- Contains two pixel values, typically 0 and 1.
- Commonly used in thresholding and object segmentation.
2. Grayscale image
- Contains intensity values.
- Commonly represented using 8 bits per pixel, giving 256 intensity levels (0–255).
3. RGB image
- Contains Red, Green and Blue colour channels.
- Each channel commonly uses 8 bits.
- Standard 8-bit RGB images use 24 bits per pixel.
4. HSV image
- Represents colour using Hue, Saturation and Value.
- Useful for colour-based object detection and segmentation.
  Image formats;
- JPEG/JPG: Compressed image format, commonly used for photographs.
- PNG: Supports lossless compression and transparency.
- BMP: Typically stores pixel data with relatively little compression.
- TIFF: Common in professional imaging and scientific applications.
- RAW: Stores minimally processed camera sensor data.
  Colour spaces;
A colour space is a mathematical representation of colours.
Common colour spaces:
- RGB: Red, Green and Blue.
- HSV: Hue, Saturation and Value.
- Grayscale: Intensity only.
- YCbCr: Luminance and colour-difference components.

 IMAGE PREPROCESSING
Preprocessing prepares images for analysis and improves the performance of subsequent vision algorithms.
  Resizing;
Changes image dimensions to meet model input requirements or reduce computation.
  Normalization;
Scales pixel values into a suitable numerical range.
For 8-bit grayscale or RGB channel values:
    x' = x/255
This maps pixel values from [0,255] to [0,1].
  Image filtering;
Used to remove noise or enhance image features.
Mean filter: Replaces each pixel with the average of neighbouring pixels.
Gaussian filter: Smooths images using a Gaussian-weighted kernel.
Median filter: Replaces a pixel with the median of neighbouring values; useful for salt-and-pepper noise.
Sobel filter: Estimates image intensity gradients to detect edges.
  Image enhancement;
Improves visual quality or makes features easier to detect.
Techniques:
- Contrast enhancement.
- Histogram equalization.
- Brightness adjustment.
- Sharpening.
- Noise reduction.
  Thresholding;
Converts grayscale images into binary images based on a selected intensity threshold.
    I'(x,y) = 1, if I(x,y) ≥ T
    I'(x,y) = 0, otherwise.
Where T is the threshold value.
Applications:
- Object separation.
- Document processing.
- Industrial defect inspection.

 IMAGE TRANSFORMATIONS
Image transformations modify the spatial arrangement or appearance of image pixels.
  Geometric transformations;
Translation: Moves an image horizontally or vertically.
Rotation: Rotates an image about a reference point.
Scaling: Increases or decreases image dimensions.
Reflection: Flips an image horizontally or vertically.
Affine transformation: Combines linear transformations and translation while preserving straight lines and parallelism.
Perspective transformation: Models changes in viewpoint and can represent perspective distortion.
 Applications:
- Image alignment.
- Camera calibration.
- Image registration.
- Augmented reality.
  Convolution;
Convolution is an operation that applies a filter (kernel) across an image to extract or modify local features.
It is fundamental to image filtering and Convolutional Neural Networks (CNNs).
A two-dimensional convolution can be expressed as:
    S(i,j) = ΣₘΣₙ I(i−m,j−n)K(m,n)
Where:
- I = Input image.
- K = Filter/kernel.
- S = Output feature map.
Common kernels:
- Blur kernel.
- Sharpening kernel.
- Edge detection kernel.
- Gaussian kernel.
- Sobel kernels.

 EDGE DETECTION AND FEATURE EXTRACTION
  Edge detection;
Identifies boundaries where image intensity changes significantly.
Common algorithms:
1. Sobel operator
Uses horizontal and vertical gradient filters.
2. Prewitt operator
Uses directional gradient masks to identify edges.
3. Canny edge detector
A multi-stage edge detection algorithm:
1. Gaussian smoothing.
2. Gradient calculation.
3. Non-maximum suppression.
4. Double thresholding.
5. Edge tracking by hysteresis.
Canny generally produces thin and well-connected edges.
  Feature extraction;
Identifies important visual characteristics that help distinguish objects.
Common features:
- Edges.
- Corners.
- Textures.
- Shapes.
- Colour distributions.
- Local patterns.
  Corner detection;
Identifies points where image intensity changes significantly in two directions.
Examples:
- Harris Corner Detector.
- Shi-Tomasi Corner Detector.
Applications:
- Image matching.
- Object tracking.
- Visual navigation.
  Local feature descriptors;
Represent distinctive image regions for matching and recognition.
Examples:
- SIFT.
- ORB.
- SURF.
Applications:
- Image stitching.
- Object recognition.
- Visual localization.

 IMAGE SEGMENTATION
Image segmentation divides an image into meaningful regions or objects.
  Types of segmentation;
1. Threshold-based segmentation
Separates objects according to pixel intensity.
2. Edge-based segmentation
Uses detected boundaries to separate regions.
3. Region-based segmentation
Groups neighbouring pixels with similar characteristics.
4. Semantic segmentation
Assigns a class label to every pixel.
Example: Every pixel belonging to a road is labelled as road.
5. Instance segmentation
Identifies individual object instances and separates them, even when they belong to the same class.
Example: Separately identifying three people in an image.
6. Panoptic segmentation
Combines semantic and instance segmentation to provide a complete scene representation.
Applications:
- Medical image analysis.
- Autonomous driving.
- Agricultural monitoring.
- Industrial inspection.

 OBJECT DETECTION AND RECOGNITION
  Image classification;
Assigns an image to a predefined category.
Example: Identifying whether an image contains a cat, dog or vehicle.
  Object detection;
Identifies objects and determines their locations within an image.
Outputs commonly include:
- Object class.
- Confidence score.
- Bounding box coordinates.
Bounding boxes are generally represented by four coordinates, such as (x_min, y_min, x_max, y_max).
  Popular algorithms:
YOLO (You Only Look Once)
- Single-stage object detector.
- Designed for efficient object detection.
- Commonly used in real-time applications.
SSD (Single Shot MultiBox Detector)
- Single-stage detection architecture.
- Predicts object classes and bounding boxes at multiple feature scales.
Faster R-CNN
- Two-stage detector.
- Uses region proposals followed by object classification and bounding-box refinement.
  Object recognition;
Identifies what an object is using its visual characteristics and learned representations.
Applications:
- Face recognition.
- Product identification.
- Vehicle recognition.
- Industrial component recognition.
  Object tracking;
Maintains the identity and position of objects across successive video frames.
Popular methods:
- Kalman Filter.
- Optical Flow.
- SORT.
- Deep SORT.
Applications:
- People counting.
- Vehicle tracking.
- Robot navigation.
- Motion analysis.

 DEEP LEARNING IN COMPUTER VISION
Deep Learning enables computer vision systems to automatically learn complex visual features from large datasets.
  Convolutional Neural Networks (CNNs);
CNNs are neural networks designed to process grid-like data such as images.
Main components:
1. Convolutional layer
Applies learnable filters to extract visual features.
2. Activation function
Introduces nonlinearity. ReLU is commonly used:
    f(x) = max(0,x)
3. Pooling layer
Reduces spatial dimensions and computational requirements.
Types:
- Max pooling.
- Average pooling.
4. Fully connected layer
Combines extracted features to produce predictions.
5. Output layer
Produces class scores or other predictions.
 CNN working process
1. Input image enters the network.
2. Convolutional filters extract features.
3. Activation functions introduce nonlinear relationships.
4. Pooling reduces feature-map dimensions.
5. Deeper layers learn more complex features.
6. Fully connected or task-specific layers produce outputs.
Early CNN layers often learn edges and textures, while deeper layers learn more complex visual patterns.
 Common CNN architectures
- LeNet: Early CNN architecture for handwritten digit recognition.
- AlexNet: Demonstrated the effectiveness of deep CNNs for large-scale image classification.
- VGG: Uses repeated small convolutional filters.
- ResNet: Uses residual connections to enable deeper networks.
- MobileNet: Designed for computationally constrained devices.
- EfficientNet: Balances model depth, width and resolution.
  Vision Transformers (ViT);
Use transformer attention mechanisms to process image patches and learn relationships between different image regions.
Applications:
- Image classification.
- Object detection.
- Image segmentation.
  Transfer learning;
Uses a model pretrained on a large dataset as the starting point for a new task.
Benefits:
- Reduces training time.
- Requires less labelled data.
- Often improves performance on smaller datasets.

 VIDEO PROCESSING AND MOTION ANALYSIS
Video is a sequence of images called frames displayed over time.
  Important concepts;
Frame rate (FPS): Number of frames displayed or processed per second.
Temporal information: Information describing how a scene changes over time.
Optical flow: Estimates apparent motion of image points between consecutive frames.
Motion detection: Identifies moving regions in video.
Background subtraction: Separates moving foreground objects from a relatively stationary background.
Object tracking: Follows identified objects across frames.
Applications:
- Traffic monitoring.
- Surveillance.
- Sports analysis.
- Robotics.
- Gesture recognition.

 CAMERA CALIBRATION AND 3D COMPUTER VISION
Camera calibration estimates camera parameters required for accurate geometric measurements.
  Camera parameters;
Intrinsic parameters
Describe the internal characteristics of the camera:
- Focal length.
- Principal point.
- Pixel scaling.
- Lens distortion.
Extrinsic parameters
Describe the camera's position and orientation relative to a world coordinate system:
- Rotation matrix (R).
- Translation vector (t).
Pinhole camera model
A simplified perspective projection model is:
    x = fX/Z
    y = fY/Z
Where:
- X, Y = 3D coordinates relative to the camera.
- Z = Depth.
- f = Focal length.
- x, y = Projected image coordinates, in compatible units.
In practical pixel coordinates, camera intrinsic parameters are also applied.
Stereo vision
Uses two cameras at different positions to estimate depth from the difference in corresponding image positions.
Disparity:
    d = x_left − x_right
Depth:
    Z = fB/d
Where:
- Z = Object depth.
- f = Focal length in compatible units.
- B = Distance between camera centres (baseline).
- d = Disparity.
Applications:
- 3D reconstruction.
- Robot navigation.
- Autonomous vehicles.
- Depth estimation.

 COMPUTER VISION PERFORMANCE EVALUATION
  Intersection over Union (IoU);
Measures the overlap between a predicted bounding box and the ground-truth bounding box.
    IoU = Area of Intersection / Area of Union
Ranges from 0 to 1.
A higher IoU indicates better localization.
  Mean Average Precision (mAP);
Measures object detection performance by combining precision-recall information across object classes.
  Pixel accuracy;
Measures the proportion of correctly classified pixels in image segmentation.
    Pixel Accuracy = Correctly Classified Pixels / Total Pixels
  Dice coefficient;
Measures overlap between predicted and ground-truth segmentation regions.
    Dice = 2|A ∩ B| / (|A| + |B|)
  Inference latency;
Time required for a model to process an input and produce an output.
  FPS;
Frames per second processed by a vision system.
    FPS = Number of processed frames / Processing time (seconds)
A good computer vision system must balance accuracy, speed, memory use and reliability.

 COMPUTER VISION IN EDGE AI AND EMBEDDED SYSTEMS
Edge computer vision performs image and video analysis directly on local devices rather than relying entirely on remote cloud processing.
  Hardware platforms;
- Raspberry Pi: Embedded Linux computer for image processing and lightweight AI.
- NVIDIA Jetson: Embedded computing platform with GPU acceleration.
- ESP32-CAM: Microcontroller-based camera platform for lightweight vision tasks.
- Google Coral: Edge AI acceleration using supported hardware.
- Smartphones: Integrated cameras and AI accelerators.
- Industrial smart cameras: Dedicated machine-vision systems.
  Edge vision pipeline;
1. Camera captures an image or video.
2. Processor acquires image data.
3. Image preprocessing is performed.
4. An optimized model performs inference.
5. Results are interpreted.
6. The device triggers an action or sends an alert.
7. Selected information may be transmitted to a cloud server.
  Edge optimization techniques;
Quantization: Reduces model numerical precision, e.g., FP32 to INT8.
Pruning: Removes less important model weights or structures.
Knowledge distillation: Transfers learned behaviour from a large model to a smaller model.
Image resizing: Reduces input resolution and computational requirements.
Efficient architectures: Uses compact networks such as MobileNet.
  Common software tools;
- OpenCV: Image and video processing.
- Python: Computer vision development and experimentation.
- PyTorch: Deep-learning model development.
- TensorFlow: Machine-learning and computer-vision development.
- Ultralytics YOLO: Object detection and related vision tasks.
- ONNX Runtime: Model inference on supported platforms.
- MediaPipe: Real-time perception pipelines for tasks such as hand, face and pose tracking.

 PRACTICAL ENGINEERING APPLICATIONS
1. Industrial inspection: Detecting cracks, surface defects and incorrect component placement.
2. Robotics: Identifying objects, obstacles and navigation landmarks.
3. Autonomous vehicles: Detecting pedestrians, traffic signs, vehicles and road boundaries.
4. Smart agriculture: Detecting plant diseases, weeds and crop maturity.
5. Medical engineering: Analysing X-rays, CT scans and MRI images.
6. Security systems: Detecting and tracking objects in monitored environments.
7. Embedded systems: Building low-power intelligent cameras.
8. Quality control: Checking dimensions, alignment and product consistency.
9. Smart traffic: Vehicle counting and congestion monitoring.
10. Human-machine interaction: Gesture and pose recognition.
Example: Automated industrial defect detection
An inspection camera captures images of manufactured components. A trained CNN or object detector analyses each image and identifies defective components.
  Process:
1. Capture component image.
2. Resize and preprocess image.
3. Run the trained model.
4. Detect and classify defects.
5. Compare the result with an acceptance threshold.
6. Send a signal to a sorting mechanism.
7. Store inspection results for quality monitoring.

 LIMITATIONS AND CHALLENGES
- Lighting variations can affect image quality and detection accuracy.
- Occlusion occurs when objects partially block one another.
- Motion blur reduces visual clarity.
- Low-resolution cameras limit available detail.
- Large models require substantial computational resources.
- Biased training datasets can cause unreliable predictions.
- Camera calibration errors affect geometric measurements.
- Real-time processing introduces latency constraints.
- Adversarial inputs can mislead vision models.
- Privacy and security must be considered when collecting and processing images.

 IMPORTANT EXAM AND PRACTICAL TIPS
1. Differentiate image processing from computer vision.
2. Understand pixels, resolution, colour channels and colour spaces.
3. Know the purpose of image preprocessing and filtering.
4. Understand convolution, kernels and edge detection.
5. Distinguish feature extraction from image segmentation.
6. Differentiate classification, object detection and object tracking.
7. Understand CNN architecture and the function of its layers.
8. Know the differences between YOLO, SSD and Faster R-CNN.
9. Understand camera calibration and stereo vision.
10. Know IoU, mAP, Dice coefficient, FPS and inference latency.
11. Understand how computer vision is deployed on edge devices.
12. Consider accuracy, speed, memory, power and environmental conditions when designing practical systems.