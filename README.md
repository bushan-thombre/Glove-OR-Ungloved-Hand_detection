# Glove-OR-Ungloved-Hand_detection

Dataset A) Dataset Name : glove.v1i.yolov8.zip B) Source - Custom collected images Manually labeled using Roboflow Dataset structured in YOLO format

Model Used Model: YOLOv8s Framework: Ultralytics YOLO Base weights: yolov8s.pt (pretrained on COCO) Fine-tuned on custom dataset

Preprocessing & Training A) Image Preprocessing Automatic resizing to 640x640 Normalization (handled by YOLO) Label verification

B) Data Augmentation (Enabled) YOLOv8 default augmentation: Mosaic Random horizontal flip HSV color augmentation Scaling & translation Rotation

This improves robustness to:Lighting variation,Motion blur,Industrial environment noise

Production Detection Pipeline Features implemented: CLI-based execution Batch inference GPU support JSON logging Annotated image output Error handling Structured logging

What Worked

YOLOv8 fine-tuning improved detection accuracy significantly. Data augmentation improved generalization. Batch inference improved processing speed. Confidence threshold tuning reduced false positives. JSON output makes the system production-ready.

6 How to run script python detect.py
--model runs/detect/train/weights/best.pt
--input test/images
--output output
--confidence 0.5
--batch 8
