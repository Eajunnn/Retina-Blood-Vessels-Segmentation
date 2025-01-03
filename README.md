
# 🧠 Retina Blood Vessels Segmentation

This project implements a robust image processing pipeline for **automatic segmentation of retinal blood vessels**, which is essential in diagnosing and monitoring retinal diseases such as diabetic retinopathy, hypertension, and glaucoma. 🚑👁️

---

## 📜 Overview

- **Purpose**: To accurately segment retinal blood vessels for medical diagnostics.
- **Key Features**:
  - Contrast enhancement using CLAHE.
  - Morphological filtering and advanced techniques like Frangi filtering.
  - Automatic thresholding with OTSU and Hysteresis Threshold.
  - Noise reduction and vessel enhancement for improved segmentation results.

---

## 🚀 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Eajunnn/Retina-Blood-Vessels-Segmentation.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd Retina-Blood-Vessels-Segmentation
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🛠️ How to Use

1. Place all the **retina images**, **mask images**, and **label images** in the same folder as the code.
2. Update the file paths in the script for:
   - Images: `imgpath1`, `imgpath2`
   - Masks: `maskimages`, `labelimages`
3. Adjust the iteration count based on the number of images.
4. Run the code:
   ```bash
   python main.py
   ```
5. Processed outputs will include:
   - Segmented blood vessels 🩸
   - Performance metrics 📊

---

## 📖 Methodology

### 1️⃣ Preprocessing
- **Green Channel Extraction** 🌿: 
  - Extracts the green channel from RGB images for better contrast.
- **CLAHE** ✨:
  - Enhances local contrast to highlight blood vessels.

### 2️⃣ Filtering
- **Morphological Operations** 🔲:
  - Uses a rectangular kernel for noise reduction.
- **Top-Hat Transformation** 🖤:
  - Enhances dark structures against a bright background.
- **OTSU Thresholding** 🎚️:
  - Automatically finds the optimal threshold for binarization.
- **Frangi Filtering** 🔬:
  - Enhances tubular structures like blood vessels.
- **Hysteresis Thresholding** 🔗:
  - Ensures edge continuity and robustness.

### 3️⃣ Mask Operations
- Combines results from multiple filters using logical operations for optimal segmentation.

---

## 📊 Results

- Achieved high accuracy in segmenting both thick and thin blood vessels.
- Comparison with other algorithms showed improved sensitivity and vessel clarity.

---

## ⚖️ Advantages and Disadvantages

### ✅ Advantages
- Multi-scale analysis using Frangi filter for capturing both thin and thick vessels.
- Effective enhancement of vascular structures with minimal parameter tuning.

### ❌ Disadvantages
- Residual noise in closely packed vessel regions due to limitations of OTSU thresholding.
- Higher sensitivity to noise compared to advanced filters like Homomorphic filtering.

---

## 🖥️ Performance

| Metric            | Value          |
|--------------------|----------------|
| **Accuracy (Acc)** | 94.19%         |
| **Specificity (Sp)** | 98.55%        |
| **Sensitivity (Sn)** | 64.59%        |
| **Processing Time** | ~17 seconds/image |

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository, submit pull requests, and enhance the project.

---

## 📜 License

This project is licensed under the MIT License.

---

## 📚 References

1. Khan et al. (2018): Robust technique for retinal vessel extraction.
2. Mahapatra et al. (2022): Retinal vessel segmentation using Frangi filter.
3. Ozkava et al. (2018): Efficient retinal blood vessel segmentation.
4. Zugair et al. (2023): Segmentation using Gabor filter and optimized Top-Hat morphology.

---

## ⚠️ Disclaimer

This tool is for research and educational purposes only. Always consult with medical professionals for diagnostic decisions.
