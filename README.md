# 🖋️ Signature Verification Project

A robust **Signature Verification System** built with **Python** and **OpenCV**! This project compares an original (reference) signature with a user-submitted signature using advanced image processing and feature extraction techniques. It’s ideal for educational purposes, research, or as a foundation for production verification workflows.

---

## 🚀 Features Overview

- **Image Preprocessing**  
  Prepare both reference and submitted signature images using:
  - Grayscale conversion
  - Adaptive thresholding (binarization)
  - Noise removal with morphological operations
  - Uniform resizing for comparison

- **Stage-by-Stage Visualization**
  - See each transformation step side-by-side:
    - Original (color)
    - Grayscale
    - Binary
    - Noise-cleaned

- **Feature Extraction**
  - For each cleaned signature image:
    - Largest contour detection
    - Contour area and perimeter calculation
    - Extraction of Hu Moments (shape descriptors)

- **Signature Matching**
  - Two core similarity metrics:
    - **SSIM** (Structural Similarity Index): pixel-wise comparison
    - **Feature Vector Distance**: compares geometric shape descriptors
  - Combines these scores for a final verdict: **MATCH** or **NO MATCH**

---

## 📂 Project Structure

```
Signature-Verification/
│
├── main.py                 # Entry point – run signature verification
├── signature_utils.py      # Image preprocessing & feature extraction functions
├── verification.py         # Comparison and decision logic
├── assets/                 # Example signature images
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

---

## 🛠️ Getting Started

1. **Clone the repository**
    ```bash
    git clone https://github.com/Honda-2005/Signature-Verification.git
    cd Signature-Verification
    ```

2. **Install required packages**
    ```bash
    pip install -r requirements.txt
    ```

3. **Place signature images**
    - Put your original and submitted signature images in the `assets/` directory.

4. **Run the verification**
    ```bash
    python main.py --reference assets/original.png --test assets/test.png
    ```

---

## 📊 How It Works

1. **Preprocessing**  
   Both images are converted to grayscale, binarized, denoised, and resized.

2. **Visualization**  
   Each stage is saved/displayed so you can inspect the transformation process.

3. **Feature Extraction**  
   The largest contour is detected, and features like contour area, perimeter, and Hu Moments are computed.

4. **Verification Metrics**
   - **SSIM:** Measures structural similarity for the overall pixel layout.
   - **Feature Distance:** Compares extracted shape descriptors for geometric similarity.

5. **Final Decision**  
   The system combines the similarity scores to declare a **MATCH** or **NO MATCH**.

---

## 🧩 Dependencies

- Python 3.7+
- OpenCV (`opencv-python`)
- NumPy
- scikit-image (`scikit-image`)

All dependencies are listed in `requirements.txt`.

---

## 🎓 Applications

- Bank/financial document authentication
- Automated form verification
- Research & experimentation in image recognition
- Educational projects

---

## 📝 Notes

- The system works best with clean, scanned signatures on white background.
- For noisy or low-resolution images, adjust the preprocessing parameters for optimal results.
- Not intended for high-security production without further testing & adaptation.

---

## 📄 License

This project is MIT Licensed.  
Feel free to modify, extend, and use as you wish!

---

## 🙏 Acknowledgements

- Inspired by OpenCV’s image processing capabilities
- See [Wikipedia: Hu Moments](https://en.wikipedia.org/wiki/Image_moment) for details on shape descriptors

---

Happy verifying! ✍️
