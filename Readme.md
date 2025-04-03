# Underwater Object Detection using YOLO

## Overview
This project focuses on object detection in underwater environments using YOLO (You Only Look Once). It utilizes a pre-trained model on the COCO dataset and fine-tunes it for underwater object detection.

## Installation
To set up the environment, follow these steps:

1. Clone this repository:
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Verify GPU availability (if applicable):
   ```bash
   !nvidia-smi
   ```
4. Install YOLO via Ultralytics:
   ```bash
   pip install ultralytics
   ```

## Dataset
This project uses an underwater dataset. If not already provided, download it from the specified source and place it in the appropriate directory.

## Model Training & Inference
1. **Training the model:**
   ```python
   from ultralytics import YOLO
   model = YOLO("yolov8n.pt")  # Load pre-trained YOLO model
   model.train(data="underwater.yaml", epochs=50, imgsz=640)
   ```

2. **Inference on test images:**
   ```python
   results = model.predict(source="test_images/", save=True)
   ```

## Usage
- Modify `HOME` in the notebook to set the working directory.
- Ensure the dataset and model weights are correctly placed.
- Run the provided cells to train or perform inference.

## Dependencies
- Python 3.x
- Ultralytics YOLO
- OpenCV
- NumPy
- Matplotlib

## Results
The trained model detects underwater objects with improved accuracy. The results are saved in the `runs/detect/` directory.

## Contributors
- **Your Name** - Initial work
- **Others** - Contributions

## License
This project is licensed under the MIT License - see the LICENSE file for details.

