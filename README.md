


# 🐆 Cheetah Detection and Tracking System

### Real-time cheetah **detection** and **tracking** using **YOLO** and **DeepSORT**, built for **wildlife conservation** and **public safety** in human-animal conflict zones.


---

## 🔍 Key Features

- 📦 Custom-trained models: **YOLOv5, YOLOv8x, YOLOv10m, YOLO11s, YOLO11m, YOLO11x**
- 🧠 Object tracking with **DeepSORT** and comparison with **BoT-SORT**
- 🖼️ Dataset of **1,400+ cheetah images** in diverse terrains and lighting
- 📊 Evaluation: Precision, recall, speed, occlusion handling, and model size
- 📁 Outputs include videos, images, and an Excel comparison report

---

## 📈 Detection Model Performance

| Model     | mAP50 | mAP50:95 | F1-score | Loss   |
|-----------|-------|-----------|----------|--------|
| YOLOv5    | 89.80 | 49.00     | 88.81    | 0.022  |
| YOLOv8x   | 92.30 | **55.20** | 86.03    | 1.418  |
| YOLOv10m  | 88.10 | 53.10     | 85.08    | 2.749  |
| YOLO11s   | 91.10 | 55.00     | 86.38    | 1.402  |
| YOLO11m   | 91.00 | 54.20     | 84.53    | 1.378  |
| YOLO11x   | 91.10 | 54.90     | **86.96**| 1.358  |

> 🏆 **YOLOv8x** achieved the highest detection accuracy.  
> ⚖️ **YOLO11s** offered a good balance between accuracy and speed.

---

## ⚙️ Speed & Model Complexity

| Model    | CoP (M) | Size (MB) | CPU (ms/frame) | GPU (30s video) |
|----------|---------|-----------|----------------|------------------|
| YOLOv8x  | 68.2    | 136.7     | 3586 ms        | 36.5 sec         |
| YOLO11s  | 9.4     | 19.2      | **431 ms**     | **13.6 sec**     |
| YOLO11x  | 56.9    | 109.1     | 1377 ms        | 21.8 sec         |

---

## 🧪 Occlusion Testing Results

| Model    | mAP   | mAP50:95 | F1-score |
|----------|-------|-----------|----------|
| YOLOv8x  | 81.1  | **50.8**  | 77.69    |
| YOLO11s  | **82.5** | 49.5   | 78.25    |
| YOLO11x  | 80.8  | 49.7     | **78.77**|

> 🧩 **YOLO11s** is most stable under occlusion.  
> 🎯 **YOLOv8x** shines in precision.

---

## 🎯 Object Tracking Comparison

| Metric           | DeepSORT   | BoT-SORT  |
|------------------|------------|-----------|
| MOTA             | **85.06**  | 66.12     |
| MOTP             | **92.11**  | 27.65     |
| IDF1             | **92.06**  | 76.87     |
| ID Switches      | 2          | 4         |
| False Positives  | 39.33      | **27.67** |
| Misses           | **30.33**  | 35.67     |

> ✅ **DeepSORT** offers better tracking accuracy and fewer identity switches.

---

## 📂 Output Files

Available in the `outputs/` folder:

- 🎥 `detection_video.mp4`: Cheetah detection using YOLO
- 🎥 `tracking_deepsort_video.mp4`: YOLO + DeepSORT tracking
- 🖼️ `detected_images/`: Detection results on sample images
- 📊 `results.xlsx`: Detailed comparison of models and trackers

---

## 🧩 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
````

> ✅ Python 3.8+ recommended.

---

## 🚀 How to Run

1. **Clone the repository**

   ```bash
   git clone https://github.com/ShivaSai06/cheetahDetectionAndTracking.git
   cd cheetahDetectionAndTracking
   ```

2. **Install Git LFS and pull model files**

   ```bash
   git lfs install
   git lfs pull
   ```

3. **Run Jupyter Notebooks**
   Open `.ipynb` files in Jupyter or Google Colab:

   * `notebooks/yolo*.ipynb`: Model training/evaluation
   * `notebooks/deepsort.ipynb`: Tracker evaluation

---

## 📦 Dataset

Custom dataset with 1,400+ annotated cheetah images.
Download from Google Drive:

🔗 [Cheetah Dataset (Drive)](https://drive.google.com/file/d/1uDm1OUrcxW6O3ks_u5uHeQCLlXlS2KK1/view?usp=sharing)





---

