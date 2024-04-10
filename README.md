# YOLOv8n Object Detection using Ultralytics

## Overview

This repository contains code for performing object detection using YOLOv8n (YOLO version 8n) implemented in PyTorch with the Ultralytics library. YOLO (You Only Look Once) is a popular real-time object detection system known for its speed and accuracy.

## Requirements

- Python 3.x
- PyTorch
- Ultralytics library
- Pre-trained YOLOv8n weights (`yolov8n.pt`)

## Installation

1. Install Python (if not already installed) from [python.org](https://www.python.org/).
2. Install PyTorch by following instructions on [pytorch.org](https://pytorch.org/).
3. Install Ultralytics library using pip:
    ```
    pip install ultralytics
    ```

## Usage

1. Clone this repository or download the `yolov8n.pt` file.
2. Import the YOLO class from Ultralytics and load the pre-trained model:

    ```python
    from ultralytics import YOLO

    modelo = YOLO('yolov8n.pt')
    ```

3. Make predictions using the `predict()` method. You can specify the source (image or video path) and whether to display the predictions:

    ```python
    modelo.predict(source='0', show=True)
    ```

    - `source`: Path to the image or video file to perform detection on. You can also use camera input by specifying `'0'`.
    - `show`: Set to `True` to display the annotated image or video with bounding boxes.

4. Run your Python script containing the above code.

## Notes

- The `yolov8n.pt` file contains the pre-trained weights for YOLOv8n. Ensure it is present in the same directory as your Python script or specify the correct path when loading the model.
- YOLOv8n is a specific version of YOLO, and the model performance may vary based on the dataset it was trained on and any fine-tuning done.
- You can customize various parameters such as confidence threshold, iou threshold, etc., according to your requirements by modifying the YOLO object after initialization.

## References

- Ultralytics GitHub repository: [https://github.com/ultralytics/yolov5](https://github.com/ultralytics/yolov5)
- YOLOv8n paper (if available)
- PyTorch documentation: [https://pytorch.org/docs/stable/index.html](https://pytorch.org/docs/stable/index.html)
