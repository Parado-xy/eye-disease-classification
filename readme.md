# Eye Disease Classification

Minimal Flask + TensorFlow service to classify retinal images into eye-disease categories.

Quick links

- Server: [model_server.py](model_server.py) (uses [`IMG_WIDTH`](model_server.py), [`IMG_HEIGHT`](model_server.py), and [`checkpoint_path`](model_server.py))
- Trained Model: https://drive.google.com/file/d/1ycHYUXr9XUFsmI0bexlUs7wgkZa0h270/view?usp=sharing
- Example result: [test](test)

Requirements

- Python 3.8+
- Install: pip install tensorflow flask pillow numpy

Run (local)

1. (optional) python -m venv .venv && source .venv/bin/activate
2. pip install tensorflow flask pillow numpy
3. python model_server.py
4. POST an image to the server (example):
   curl -X POST -F "file=@/path/to/eye.jpg" http://127.0.0.1:5000/predict

Expected output (JSON)
{
"predicted_class": "<one of: cataract, diabetic_retinopathy, glaucoma, normal>",
"confidence": 0.0-1.0
}


```// filepath: /home/ojalla/dev/eye-disease-classification/README.md
# Eye Disease Classification

Minimal Flask + TensorFlow service to classify retinal images into eye-disease categories.

Quick links
- Server: [model_server.py](model_server.py) (uses [`IMG_WIDTH`](model_server.py), [`IMG_HEIGHT`](model_server.py), and [`checkpoint_path`](model_server.py))
- Trained weights: https://drive.google.com/file/d/1ycHYUXr9XUFsmI0bexlUs7wgkZa0h270/view?usp=sharing
- Example result: [test](test)

Requirements
- Python 3.8+
- Install: pip install tensorflow flask pillow numpy

Run (local)
1. (optional) python -m venv .venv && source .venv/bin/activate
2. pip install tensorflow flask pillow 
3. python model_server.py
4. POST an image to the server (example):
   curl -X POST -F "file=@/path/to/eye.jpg" http://127.0.0.1:5000/predict

Expected output (JSON)
{
  "predicted_class": "<one of: cataract, diabetic_retinopathy, glaucoma, normal>",
  "confidence": 0.0-1.0
}


```
