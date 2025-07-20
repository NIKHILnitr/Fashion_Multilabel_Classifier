# 👗 Fashion Product Multi-label Classification

This project is part of the **Codemonk Machine Learning Intern Assignment**.  
It predicts 4 labels from a fashion product image:

- 🧍‍♂️ Gender (Men / Women / Unisex)  
- 🎨 Color  
- ☀️ Season (Summer / Winter / etc.)  
- 👕 Type (T-shirt / Shoes / Dress / etc.)

---

## 📁 Dataset

- Source: [Kaggle - Fashion Product Images Dataset](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset)
- Includes:
  - Product Images
  - CSV file (`styles.csv`) with metadata (gender, color, season, type)

---

## ✅ Tasks Done

- [x] EDA: Explored and cleaned data  
- [x] Preprocessing: Encoded labels (one-hot), resized images  
- [x] Model: Used MobileNetV2 with 4 output heads  
- [x] Training: Trained for 10 epochs with decent performance  
- [x] Evaluation: Accuracy and loss plotted per label  
- [x] Prediction: Model tested on Amazon product screenshots  
- [x] Notebook: Code well-commented and organized  

---

## 🧠 Model Architecture

- **Base Model**: MobileNetV2 (ImageNet weights, frozen layers)
- **Input**: 128x128 RGB images
- **Outputs**:  
  - Dense softmax layer for each label  
- **Loss**: Categorical Crossentropy (multi-output)
- **Optimizer**: Adam

---

## 📊 Accuracy Summary

| Label   | Train Accuracy | Validation Accuracy |
|---------|----------------|---------------------|
| Gender  | 93.81%         | 85.87%              |
| Color   | 72.86%         | 55.75%              |
| Season  | 80.27%         | 71.03%              |
| Type    | 90.48%         | 80.16%              |

---

## 🧪 Sample Predictions

The model can predict on any custom image (including screenshots from Amazon).

---

## 📁 Project Structure

```
fashion_multilabel_classifier/
├── data/
│   └── styles.csv, images/
├── fashion_classifier_notebook.ipynb
├── model/
│   └── saved_model.h5
├── streamlit_app/
│   └── app.py (optional UI)
├── README.md
```

---

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone <your-repo-url>
   cd fashion_multilabel_classifier
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch notebook:
   ```bash
   jupyter notebook fashion_classifier_notebook.ipynb
   ```

4. To test prediction on a new image, use:
   ```python
   model.predict(processed_image)
   ```

---

## 📝 Submission Info

- ✅ Jupyter Notebook
- ✅ Trained Model (`.h5`)
- ✅ Cleaned Dataset
- ✅ Sample Images Tested
- ✅ Streamlit App (Optional, can be added later)

---

## 🔗 Credits

- Kaggle Dataset: Param Aggarwal
- MobileNetV2: TensorFlow Keras

---

> Feel free to fork, reuse, or build on top of this repo!
