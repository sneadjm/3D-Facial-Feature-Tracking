# 3D Facial Feature Tracking with Multimodal Depth Fusion

As models based in artificial intelligence increase in sophistication, there is a higher demand for the integration of hardware components to heighten real-world implementations. Both facial feature tracking and shape-from-focus are known techniques in computer vision. However, the combination of these two elements, particularly in a cost-effective configuration, has not been extensively explored. In this study, a 64 megapixel (MP) autofocus Arducam camera module collected images of participants at various focal lengths, such that the subject would come in and out of focus across each second of the experiment. The image data was then processed by two convolutional neural networks (CNNs) from Google MediaPipe that identified the bounding box for the face and the coordinates of facial features. These coordinates, in conjunction with a shape-from-focus calculations, were fused to measure facial feature depths relative to the camera system. The depths, aggregated across a working period represented a proxy for total participant effort in a Human Robot Collaboration (HRC) experiment.  Precise tracking of facial features was achieved with a relative consistency in 2D, as well as 3D motion trends from a singular, static imaging system. </br>

**Keywords:** Convolutional neural networks (CNNs), shape-from-focus, facial feature tracking, Human Robot Collaboration (HRC).

The notebook **Facial_Data_Processing.ipynb** contains the code used for processing the raw data in the methodology outlined above. </br>

The process of loading and applying the Face Detector and Facial Landmarker models from Google MediaPipe is largely based on their Python tutorial featured </br>
at this site: https://ai.google.dev/edge/mediapipe/solutions/vision/face_detector. 

The model card for the specific FaceMesh model used can be found at the following Model Card: https://storage.googleapis.com/mediapipe-assets/Model\%20Card\%20MediaPipe\%20Face\%20Mesh\%20V2.pdf.

### Data
The data used for this experimentation has not been made publicly available, but can be replicated by imaging a human participant
involved in a HRC task approximately 30 cm away using an Arducam Hawkeye 64MP camera (Arducam documentation: https://blog.arducam.com/64mp-ultra-high-res-camera-raspberry-pi/)
at iterating focus step levels. 

The paths in the notebook currently assume that the data is located in the same directory as the code itself. Paths should be changed as needed if stored elsewhere. 
