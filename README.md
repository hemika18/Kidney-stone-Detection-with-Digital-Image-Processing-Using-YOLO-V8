# Kidney Stone Detection using YOLOv8

This project presents a deep learning-based solution for **automatic kidney stone detection** using CT scan images.
The YOLOv8 object detection model is used to identify and localize stones within uploaded medical images.
A Flask-based web app provides a simple user interface to interact with the model.

## Motivation

Kidney stones are a common and painful medical condition.
Manual detection from CT scans is time-consuming and error-prone. 
Automating this process with YOLOv8 helps in early diagnosis and reduces the workload on radiologists.

##  Objectives
- Train a YOLOv8 model for detecting kidney stones in CT scan images.
- Build a Flask web interface for image upload and prediction.
- Provide bounding box visualization if stones are detected.
- Enable binary output: “Stone Present” or “No Stone”.
- Use performance metrics like Precision, Recall, and mAP for evaluation.
- 
##  Folder Structure

kidneystoneapp/
│
├── app.py                  # Flask application (main backend logic)
├── best.pt                 # Trained YOLOv8 model weights
├── code.ipynb              # Training notebook (YOLOv8 training and evaluation)
├── data.yaml               # YOLO dataset configuration file
├── requirements.txt        # List of Python dependencies
├── run.bat                 # Optional script to run the app (Windows)
│
├── templates/              # HTML templates (Flask frontend)
│   └── index.html
│
├── static/                 # Static files (e.g., CSS, images)
│
├── train/                  # Training dataset images
├── valid/                  # Validation dataset images
├── test/                   # Test dataset images
├── runs/                   # YOLOv8 training logs and results

##  How to Run

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Run the Flask App

#### ▶️ On **Windows**
```bat
run.bat
```

#### ▶️ On **Linux/macOS**
```bash
chmod +x run.sh
./run.sh
```

### 3. Open your browser
- Visit: `http://localhost:5000`
- Upload a CT scan image to get detection results.



##  Tools & Libraries Used

| Tool/Library     | Purpose                         |
|------------------|----------------------------------|
| YOLOv8 (Ultralytics) | Object Detection & Training     |
| Flask            | Web Application Backend         |
| OpenCV           | Image Processing & Annotation   |
| Python           | Core Programming Language       |
| Google Colab     | Model Training Environment      |

---

##  Dataset

- **Source**: Curated CT scan dataset from [Roboflow](https://roboflow.com)
- Split into `train`, `valid`, and `test` folders as per YOLO format.


##  Model Performance

- Evaluated using metrics: **Precision**, **Recall**, **mAP**
- Achieved high detection accuracy for binary classification of kidney stones.



##  References

- [Ultralytics YOLOv8 Docs](https://docs.ultralytics.com)
- [Roboflow Dataset Hosting](https://roboflow.com)
- [Flask Official Docs](https://flask.palletsprojects.com)
- Research papers on CNN-based medical image analysis.



##  Output

 Bounding box predictions with confidence score.
 Message: “No Stone Detected” if no bounding boxes are returned.



## Authors

Developed by: Dinesh P  
Project: Kidney Stone Detection using YOLOv8  
Date: July 2025

