 Capsule-Endoscopy-Circle-Detection
MATLAB codes for detection and analysis of circular patterns in capsule endoscopy frames using Fast Circlet Transform

 🩺 Circular Pattern Detection in Capsule Endoscopy Bubble Frames using Fast Circlet Transform (FCT)

This repository contains the MATLAB implementation of the methods proposed in the paper:

📄 Identification of Circular Patterns in Capsule Endoscopy Bubble Frames,  
Hossein Mir, Vahid Sadeghi, Alireza Vard, Alireza Mehri Dehnavi  
*Journal of Medical Signals & Sensors, 2024*  
🔗 [Read the paper](https://journals.lww.com/jmss/fulltext/2024/07020/identification_of_circular_patterns_in_capsule.3.aspx)  
📬 DOI: [10.4103/jmss.jmss_50_23](https://doi.org/10.4103/jmss.jmss_50_23)

---

🧠 Overview

This project presents an object-oriented method for detecting and quantifying circular patterns in two wireless capsule endoscopy (WCE) image datasets with different radius sizes using:

- Wavelet Transform (WT) for enhancing circular borders
- Fast Circlet Transform (FCT) for robust circle detection
- Postprocessing to remove false detections (O-type and C-type circles)
- Quantitative metrics: Area Ratio (AR), Dice Similarity (DSC), Circularity Percentage (CPP), and Overall Discrimination Factor (ODF)

The results reveal the potential of FCT in analyzing rheological properties of intraintestinal fluids by measuring bubble abundance and coverage.

---

🧪 Method Pipeline

1. Preprocessing  
   Enhance circular features in capsule endoscopy frames using Wavelet Transform (sym10 or db10).

2. Circle Detection with FCT  
   Apply the Fast Circlet Transform (FCT) across multiple radii (5–30 pixels). Accumulate responses and extract prominent circular patterns.

3. Postprocessing 
   Filter out false detections (e.g. overlapping or partial circles) via spatial constraints and statistical thresholds.

4. Machine Learning-Based Classification  
   Extract features from each image:
   - Number of detected circles
   - Mean and standard deviation of radii
   - Area ratio (AR)
   - Dice Similarity Coefficient (DSC)
   - Circularity Percentage (CPP)
   - Overall Discrimination Factor (ODF)

   Then classify images using:
   - Support Vector Machine (SVM)
   - K-Nearest Neighbors (KNN)
   - Decision Tree (Tree)
   - Logistic Regression
   - Naive Bayes (NB)
   - Linear Discriminant Analysis (LDA)
   - Multilayer Perceptron (MLP)
---


## 📊 Evaluation Metrics (Summary)

| Metric | Meaning |
|--------|---------|
| AR  | Area Ratio: overlap between FCT mask and ground truth |
| DSC | Dice Similarity Coefficient |
| CPP | Percentage of visually confirmed circular bubbles |
| ODF | Overall Discrimination Factor (bubble count × area) |

These metrics were used both for validation and feature extraction in the classification step.


