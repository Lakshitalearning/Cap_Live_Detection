# Cap_Live_Detection
A Python application (using tkinter) that detects and highlights a man wearing a cap from a live video feed using OpenCV and MobileNet SSD model (for person detection) . It is done using basic heuristics which  checks for changes in colour, edges, or patterns in the head region.
# Dataset

- Cap images: Kaggle dataset ([(https://www.kaggle.com/datasets/shivanandverma/cap-dataset)])
- Pre-trained MobileNet SSD model: OpenCV

# Heuristic Approach:

1. Load pre-trained MobileNet SSD model for person detection.
2. Load cap images from Kaggle dataset.
3. Resize cap images to 100x100 pixels.
4. Define a video stream function to capture frames from webcam.
5. For each frame:
    - Detect persons using MobileNet SSD model.
    - Extract head region from detected persons.
    - Resize head region to match cap image size.
    - Use template matching (TM_CCOEFF_NORMED) to detect cap.
    - Draw bounding box and label "Cap Detected" if cap is detected.
6. Display video stream using Tkinter.
   
# Requirements
- OpenCV 4.x
- TensorFlow 2.x
- Tkinter
- Python 3.x
  
# Future Work
- Improve cap detection accuracy.
- Expand dataset for diverse cap styles.
- Integrate with other computer vision applications.




