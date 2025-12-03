🖋️ Signature Verification Project (Python + OpenCV)

This project implements a signature verification system using Python and OpenCV.
It compares an original signature with a user-submitted signature by preprocessing both images, extracting key features, and evaluating their similarity.

The system performs:

🔹 Image Preprocessing
Convert images to grayscale
Apply adaptive thresholding (binarization)
Remove noise using morphological operations
Resize signatures to the same dimensions

🔹 Visualization
The project displays all stages for both signatures:
Original (color)
Grayscale
Binary
Cleaned (noise-removed)

🔹 Feature Extraction
From each cleaned signature, the system extracts:
Largest contour
Contour area
Contour perimeter
Hu Moments (shape descriptors)

🔹 Verification
Two types of comparison are used:
SSIM (Structural Similarity Index)
Feature vector distance (based on contour features)

A final decision (match / no match) is made based on these metrics.
