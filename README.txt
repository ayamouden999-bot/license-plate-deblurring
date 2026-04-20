License Plate Deblurring — Dataset
====================================

Source: Kaggle — "Large License Plate Dataset" by Fares El Menshawi
URL: https://www.kaggle.com/datasets/fareselmenshawii/large-license-plate-dataset

Contents
--------
11 real license plate images (plate_001.jpg to plate_011.jpg)
cropped from full vehicle photos using YOLO bounding box annotations.

Countries represented: USA, Germany, Spain, Georgia (US state)
Image size: 320x100 pixels (resized from original crops)
Format: JPEG, grayscale

Quality filtering
-----------------
Images were filtered using Laplacian variance (threshold=50) to remove
blurry source images. All 11 plates passed the quality filter.

Usage in the project
--------------------
These images serve as SHARP GROUND TRUTH.
The notebook applies synthetic motion blur on top to create
paired sharp/blurred training and validation data, following
standard practice in image restoration research.

Split
-----
Training set  : 7 images (plates 001-007)
Validation set: 4 images (plates 008-011)

Blur configurations applied
---------------------------
Length 15px, Angle 0°
Length 20px, Angle 0°
Length 25px, Angle 15°
Length 30px, Angle 30°
Length 35px, Angle 45°
Noise sigma: 5.0
