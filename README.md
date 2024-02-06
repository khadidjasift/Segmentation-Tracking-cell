# Segmentation-Tracking-cell





# Object Detection and Tracking Project

This project demonstrates how to set up an object detection and tracking cell system using the Ultralytics YOLO model and the Supervision library. 


1. **Install Required Packages**: Install the Ultralytics package and the Supervision library for object detection and tracking.
    ```bash
    !pip install ultralytics
    !pip install supervision
    ```
2. **Clone Supervision Repository**: Clone the Supervision repository to access its tracking and annotation features.
    ```bash
    !git clone https://github.com/roboflow/supervision.git
    !cd supervision
    ``
## Object Detection and Tracking

This project uses the Ultralytics YOLO model for object detection and the Supervision library for bounding box annotations and tracking.

1. **Initialize the Model**: Load the YOLO model with pre-trained weights.

    ```python
    from ultralytics import YOLO
    model = YOLO('/path/to/weights/last.pt')
    ```
2. **Video Processing for Object Detection**: Process a video to detect objects and annotate them with bounding boxes.

    ```python
    import numpy as np
    import supervision as sv
    from ultralytics import YOLO
    # Define callback for processing frames
    ```
3. **Object Tracking in Video**: Enhance object detection with tracking, allowing objects to be followed across frames.

    ```python
    tracker = sv.ByteTrack()
    box_annotator = sv.BoundingBoxAnnotator()
    label_annotator = sv.LabelAnnotator()
    # Define callback for tracking and labeling
    ```
4. **Process Video**: Apply detection and tracking to a video file, saving the annotated result.

    ```python
    sv.process_video(source_path="/content/video_result.mp4", target_path="result-cell2.mp4", callback=callback)
    ```
