
# Automatic Car Detection and License Plate Recognition System

## Overview

This project aims to develop an intelligent system for detecting vehicles and recognizing their license plates along with reading the number and logging the data using advanced computer vision techniques and machine learning models.

## Features

- Vehicle Detection
- License Plate Detection
- License Plate Recognition
- License Plate Reading
- Vehicle Tracking
- Data Logging

## Technologies

- YOLOV8
- EasyOCR
- SORT

## Demo

[![Video Preview](path_to_thumbnail_or_gif)](https://drive.google.com/file/d/1JbwLyqpFCXmftaJY1oap8Sa6KfjoWJta/view?usp=sharing)

## Project Description

The project is a Smart Car Detection and License Plate Recognition System built using computer vision and machine learning techniques. The main goal is to develop an intelligent system that can detect vehicles, track them, and recognize their license plates in real-time.

Here's how the project works:

    Detection and Tracking:
        The system uses a pre-trained YOLOv8 model (yolov8n.pt) to detect vehicles in a given video stream (sample.mp4).
        After detecting vehicles, it employs the SORT (Simple Online and Realtime Tracking) algorithm for vehicle tracking across frames.

    License Plate Recognition:
        For each detected vehicle, the system uses a custom-trained YOLO model (license_plate_detector.pt) to detect the license plate within the vehicle's bounding box.
        Once the license plate is detected, it extracts the region of interest (ROI) containing the license plate image for further processing.

    Optical Character Recognition (OCR):
        The extracted license plate image is then processed using EasyOCR, an optical character recognition library.
        EasyOCR reads the text from the license plate image and provides the recognized text along with confidence scores.

    Data Logging:
        The system logs the detection and recognition results into a CSV file (test.csv).
        Each entry in the CSV file includes the frame number, vehicle ID, vehicle bounding box, license plate bounding box, recognized license plate text, and confidence scores.

    Utility Functions:
        The util.py file contains utility functions for OCR, license plate formatting, and writing results to the CSV file.
        These utility functions handle tasks such as formatting the license plate text, checking compliance with the required format, and writing results to a CSV file in an organized manner.

    Dependencies:
        The project requires several Python packages such as ultralytics, opencv-python, easyocr, numpy, and matplotlib.
        These dependencies are listed in the requirements.txt file for easy installation.

Overall, the project integrates various technologies to create a robust and efficient solution for real-time vehicle tracking and license plate recognition, making it suitable for applications in traffic management, security surveillance, and smart city initiatives.
