Here's a professionally formatted `README.md` file for your **Cheetah Detection and Tracking System** project, based on all the content you've shared, including models, results, and discussion.

---

### ✅ `README.md`

```markdown
# 🐆 Cheetah Detection and Tracking System

This project presents a **real-time system** to detect and track cheetahs in video streams using **YOLO** object detection models and **DeepSORT** tracking. The system supports **wildlife conservation** and helps enhance **public safety** in human-animal conflict zones.

---

## 🔍 Features

- Real-time cheetah detection using custom-trained **YOLOv5, YOLOv8x, YOLOv10m, YOLO11s, YOLO11m, YOLO11x**
- Multi-object tracking using **DeepSORT**
- Custom dataset of **1,400+ images** with varied terrains and lighting
- Robust against occlusion and background clutter
- Comparison of **DeepSORT** and **BoT-SORT** tracking algorithms
- Visual and quantitative evaluation of models

---

## 📁 Folder Structure

```

cheetah-detection-tracking/
├── data/                       # Custom dataset (via Git LFS or external link)
│   └── cheetah\_dataset.zip
├── notebooks/                 # Training and evaluation notebooks
│   ├── yolov5.ipynb
│   ├── yolo8x.ipynb
│   ├── yolo11s.ipynb
│   ├── yolo11m.ipynb
│   ├── yolo11x.ipynb
│   └── deepsort.ipynb
├── weights/                   # Best model checkpoints
│   ├── yolo8x\_best.pt
│   ├── yolo11s\_best.pt
│   ├── yolo11x\_best.pt
├── outputs/                   # Visual results
│   ├── final\_video.mp4
│   └── sample\_frames/
├── requirements.txt           # Python dependencies
└── README.md

````

---

## 🧠 Model Evaluation Summary

### 🔸 Detection Performance (mAP50:95)

| Model     | mAP50 | mAP50:95 | F1-score | Loss  |
|-----------|--------|-----------|-----------|--------|
| YOLOv5    | 89.80  | 49.00     | 88.81     | 0.022  |
| YOLOv8x   | 92.30  | **55.20** | 86.03     | 1.418  |
| YOLOv10m  | 88.10  | 53.10     | 85.08     | 2.749  |
| YOLO11s   | 91.10  | 55.00     | 86.38     | 1.402  |
| YOLO11m   | 91.00  | 54.20     | 84.53     | 1.378  |
| YOLO11x   | 91.10  | 54.90     | **86.96** | 1.358  |

> 🔍 **YOLOv8x** gave the best detection accuracy, while **YOLO11s** balanced performance and speed.

---

### ⚙️ Computational Comparison

| Model    | CoP (M) | Size (MB) | mDT Frame (CPU) | mDT 30s Video (GPU) |
|----------|---------|------------|------------------|----------------------|
| YOLOv8x  | 68.2    | 136.7 MB   | 3586 ms          | 36.5 sec             |
| YOLO11s  | 9.4     | 19.2 MB    | **431 ms**       | **13.6 sec**         |
| YOLO11x  | 56.9    | 109.1 MB   | 1377 ms          | 21.8 sec             |

---

## 🧪 Occlusion Testing Results

| Model    | mAP   | mAP50:95 | F1-Score |
|----------|--------|-----------|-----------|
| YOLOv8x  | 81.1   | **50.8**  | 77.69     |
| YOLO11s  | **82.5** | 49.5   | 78.25     |
| YOLO11x  | 80.8   | 49.7     | **78.77** |

> 🧩 **YOLOv8x** excels at high-precision detection, while **YOLO11s** and **YOLO11x** are more stable under occlusion.

---

## 🎯 Object Tracking Comparison

| Metric       | DeepSORT | BoT-SORT |
|--------------|----------|----------|
| MOTA         | **85.06**| 66.12    |
| MOTP         | **92.11**| 27.65    |
| IDF1         | **92.06**| 76.87    |
| ID Switches  | 2        | 4        |
| False Positives | 39.33  | **27.67**|
| Misses       | **30.33**| 35.67    |

> 🎯 **DeepSORT** outperforms BoT-SORT in tracking consistency and precision.

---

## 📷 Visualization

The outputs/ folder contains results from detection and tracking experiments:

🎥 detection_video.mp4: Raw cheetah detection output using YOLO

🎥 tracking_deepsort_video.mp4: YOLO + DeepSORT-based real-time cheetah tracking

🖼️ detected_images/: Object detection results on static images with confidence scores

📊 results.xlsx: Excel sheet comparing detection metrics, model complexity, and tracking statistics

---

## 🧩 Requirements

Install all dependencies:

```bash
pip install -r requirements.txt
````

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/cheetah-detection-tracking.git
   cd cheetah-detection-tracking
   ```

2. If needed, install Git LFS and pull models:

   ```bash
   git lfs install
   git lfs pull
   ```

3. Launch Jupyter or open `.ipynb` files in Google Colab.

4. Run training/evaluation or inference scripts from:

   * `notebooks/yolo*.ipynb`
   * `notebooks/deepsort.ipynb`

---

## 📦 Dataset

The dataset (1,400+ labeled cheetah images) can be downloaded from:

🔗 [Google Drive Dataset Link](https://drive.google.com/file/d/1uDm1OUrcxW6O3ks_u5uHeQCLlXlS2KK1/view?usp=sharing)

---

