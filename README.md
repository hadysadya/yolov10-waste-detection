# YOLOv10 Waste Detection System 

An object detection system for classifying waste into plastic, paper, metal, glass, and organic categories using YOLOv10.

## Problem Statement 

Waste classification is a challenging computer vision problem due to object variety, lighting conditions, and background noise.
This project aims to build an object detection model capable of detecting and classifying waste objects in real-world environments.

## Dataset 

- Custom waste dataset (1400 images)
- Classes: plastic, paper, metal, glass, organic
- Split: train / validation / test
- Preprocessing: resize 640x640, auto-orient

## Model & Training 

- Model: YOLOv10s
- Training approach:
  - v1: trained on 500 images
  - v2: fine-tuned on 1400 images
- Framework: Ultralytics YOLOv10
- Hardware: NVIDIA Tesla T4 (Google Colab)

## Results

### Training Results (v2)
- Precision 0.545
- Recall: 0.421
- mAP50: 0.469
- mAP50-95: 0.344

![Training Results](assets/training_v2_results.png)

## Inference Example

The model was tested on real-world images and successfully detected small waste objects with high confidence. 

![Inference Result](assets/inference_sample_v2.jpg)

## My Role (Machine Learning Engineer)

- Dataset preprocessing and validation
- YOLOv10 model training and fine-tuning
- Model evaluation and analysis
- Preparing the model for backend deployment

## Future Work 

- Improve organic waste detection with targeted data collection
- Deploy model as a REST API for mobile integration
