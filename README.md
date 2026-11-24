#  Smart Vegetable Detection & Checkout (Faster R-CNN)

[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-EE4C2C.svg)](https://pytorch.org/)
[![Gradio](https://img.shields.io/badge/UI-Gradio-orange.svg)](https://www.gradio.app/)
[![Roboflow](https://img.shields.io/badge/Dataset-Roboflow%20COCO-purple.svg)](https://roboflow.com/)

An AI-powered smart supermarket checkout system that detects produce using **Faster R-CNN (ResNet-50 FPN)**, counts items, and automatically calculates total prices with a live **Gradio** web app.

---

##  Highlights
- **Model:** Faster R-CNN with ResNet-50-FPN backbone fine-tuned on custom COCO dataset (35+ vegetable & fruit classes).
- **Smart Checkout System:** Detects items, draws bounding boxes, and generates an itemized receipt with pricing in RM.
- **Interactive Web UI:** Live image upload and webcam testing powered by Gradio.

---

##  Model Comparison

| Model | Accuracy | Precision | Recall |
| :--- | :---: | :---: | :---: |
| **Faster R-CNN (Ours)** | **0.77** | **0.74** | **0.73** |
| YOLOv8 | 0.62 | 0.46 | 0.48 |
| RetinaNet | 0.02 | 0.02 | 0.02 |

---

##  Quickstart

### 1. Install Dependencies
```bash
pip install torch torchvision pycocotools roboflow gradio matplotlib seaborn torchmetrics
```

### 2. Run the Notebook
Open `RCNNASSIGNMENT.ipynb` in **Google Colab (GPU)** or Jupyter and run all cells:
1. Downloads dataset from Roboflow in COCO format.
2. Trains Faster R-CNN using SGD optimizer (`lr=0.005`, `epochs=5`).
3. Evaluates with Confusion Matrix & PR Curves.
4. Launches the Gradio checkout web interface.

---

##  Sample Checkout Output

```text
========================================
         SMART CHECKOUT RECEIPT         
========================================
  Broccoli             x 2  = RM  9.00
  Tomato               x 3  = RM  2.40
  Carrot               x 1  = RM  1.10
----------------------------------------
  Grand Total: RM 12.50
========================================
```

---

##  Author
* **Justin Yong Wei Li** ([@justinyw105](https://github.com/justinyw105))
