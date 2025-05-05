---

## Model Architecture

- *Base Model*: ResNet50 (pretrained on ImageNet, include_top=False)
- *Custom Top Layers*:
  - GlobalAveragePooling2D
  - Dense(128, activation='relu')
  - Dense(3, activation='softmax')
- *Training Enhancements*:
  - *Data Augmentation*: rotation, flipping, zoom, brightness
  - *Callbacks*: EarlyStopping, ModelCheckpoint

---

## Evaluation Metrics

| Metric     | CNN (Original) | ResNet50 (Modified) |
|------------|----------------|---------------------|
| Accuracy   | 91.8%          | *96.2%*           |
| Precision  | 0.92           | *0.96*            |
| Recall     | 0.91           | *0.97*            |

Evaluation includes:
- Confusion Matrix
- Classification Report
- Training and Validation Curve Visualization

---

## How to Run (via Google Colab)

1. Clone or open directly in Colab:
   [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/irell05/Kidney_Tumor_Detection_And_Classification/blob/main/Tumor_type_classification.ipynb)

2. Mount your Google Drive or upload dataset folders.

3. Run all cells sequentially to train and evaluate the model.

---

## Related Paper

A short research paper is available, containing:
- Literature review on kidney tumor classification
- Methodology using ResNet50 and augmentation
- Results analysis and confusion matrix
- Suggestions for future work

---

## Dependencies

Install required packages:

```bash
pip install tensorflow numpy matplotlib scikit-learn seaborn
