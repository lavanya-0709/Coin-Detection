# Coin-Detection

## Aim
To detect and count coins in an image using morphological image processing techniques such as thresholding, dilation, erosion, and blob detection.

## Theory

## 1. Morphological Operations
Morphological operations are image processing methods that focus on the structure or shape of an image. They use a structuring element (kernel) to modify the geometric structure of the image.

## 2. Thresholding
Thresholding converts a grayscale image into a binary image.
Pixels with intensity values above or below a certain threshold are turned into white or black.
In this task, binary inverse thresholding is used so that coins appear white on a dark background, making them easier to detect.

## 3. Blob Detection
A blob is a group of connected pixels that share similar properties.
The SimpleBlobDetector in OpenCV identifies circular or blob-like regions in an image.
It uses different filters such as:
Circularity – Detects round objects
Convexity – Detects solid objects
Inertia – Ensures objects are not elongated
Using these filters, we can detect and count circular coins in the image.

## Algorithm
Read the input image (CoinsA.png).
Convert the image to grayscale.
Split the image into Red, Green, and Blue channels.
Use the Green channel for thresholding to get a binary image.
Apply dilation to fill small gaps in the coins.
Apply erosion to smooth the coin boundaries.
Use SimpleBlobDetector to identify circular coins.
Count and display the number of coins detected.
Draw circles around detected coins and show the final output.
