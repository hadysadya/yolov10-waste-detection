# YOLOv10-Based Waste Detection System (Baseline & Fine-Tuned)

An object detection system for classifying waste into plastic, paper, metal,
glass, and organic categories using YOLOv10. This project demonstrates an
iterative training approach, starting from a baseline model and improving
performance through fine-tuning.

## Problem Statement

Waste classification is a challenging computer vision problem due to object
variety, lighting conditions, occlusion, and background noise. This project
aims to build an object detection model capable of detecting and classifying
waste objects in real-world environments.

## Dataset

- Derived from the **TACO Dataset (Trash Annotations in Context)**  
  https://github.com/pedropro/TACO
- Curated and filtered subset for waste classification
- Total images: 1,400
- Classes: plastic, paper, metal, glass, organic
- Split: train / validation / test
- Format: YOLO
- Preprocessing: resize to 640×640, auto-orient

## Model & Training

- Model architecture: YOLOv10s
- Training strategy:
  - **v1 (Baseline):** trained on 500 images
  - **v2 (Fine-Tuning):** continued training on an expanded dataset of 1,400 images
- Framework: Ultralytics YOLOv10
- Hardware: NVIDIA Tesla T4 (Google Colab)

## Results

### Training Results (v2)

- Precision: 0.545
- Recall: 0.421
- mAP@50: 0.469
- mAP@50–95: 0.344

These results represent realistic performance on a limited, real-world dataset
and serve as a strong baseline for further improvements.

![Training Results](assets/training_v2_results.png)

## Inference Example

The fine-tuned model was evaluated on unseen real-world images and demonstrated
the ability to detect small waste objects under varying conditions.

![Inference Result](assets/inference_sample_v2.jpg)

## My Role

- Dataset curation and preprocessing from the TACO dataset
- Baseline training and fine-tuning of the YOLOv10 model
- Model evaluation and result analysis
- Preparing the model for backend and API-based deployment

## Future Work

- Improve organic waste detection with targeted data collection
- Apply additional data augmentation and hyperparameter tuning
- Deploy the model as a REST API for mobile or web integration
