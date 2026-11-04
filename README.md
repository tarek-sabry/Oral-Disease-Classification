# 🦷 Oral Disease Classification Using Deep Learning

## 📌 Project Overview

This project focuses on classifying oral diseases from dental and oral images using Deep Learning and Transfer Learning techniques.

The main objective is to develop and compare multiple Convolutional Neural Network (CNN) models, optimize model performance through Hyperparameter Tuning, and deploy the best-performing model using Streamlit.

## 🎯 Project Objectives
 LINK Project Kaggle / https://www.kaggle.com/code/tareksabry/notebook4b233f9618
- Build a Custom CNN model for image classification.
- Apply Transfer Learning using pretrained models.
- Compare different Deep Learning architectures.
- Perform Hyperparameter Tuning to improve model performance.
- Evaluate models using multiple classification metrics.
- Deploy the final model through a Streamlit web application.

## 📂 Dataset Description

The dataset contains **5,563 images** distributed across six oral disease categories.

| Class | Number of Images |
|---|---:|
| Caries | 219 |
| Mouth Ulcer | 265 |
| Tooth Discoloration | 183 |
| Hypodontia | 1,251 |
| Gingivitis | 2,349 |
| Calculus | 1,296 |
| **Total** | **5,563** |

### Dataset Split

| Dataset | Images |
|---|---:|
| Training | 3,894 |
| Validation | 834 |
| Testing | 835 |
| **Total** | **5,563** |

**Preprocessing:**
- Image resizing: 128 × 128 pixels.
- Color format: RGB.
- Image normalization according to model requirements.
- Training, validation, and testing datasets.

## 🧠 Models Implemented

Four Deep Learning models were developed and evaluated:

1. **Custom CNN:** A convolutional neural network trained from scratch.
2. **MobileNetV2:** A pretrained model using ImageNet weights.
3. **EfficientNetB0:** A pretrained architecture designed for efficient image classification.
4. **MobileNetV2 Tuned:** An optimized MobileNetV2 model using selected hyperparameters.

## ⚙️ Hyperparameter Tuning

Hyperparameter experiments were conducted using different combinations of Learning Rate and Dropout.

Six experiments were performed.

**Selected Hyperparameters:**

| Parameter | Selected Value |
|---|---:|
| Learning Rate | 0.001 |
| Dropout | 0.3 |
| Optimizer | Adam |

The final tuned model was selected based on validation performance, including Validation Accuracy, Validation Loss, and Macro F1-score.

## 📊 Model Evaluation and Comparison

All four models were evaluated using the test dataset.

| Model | Accuracy | Macro F1 | Weighted F1 |
|---|---:|---:|---:|
| Custom CNN | 42.75% | 26.57% | 41.76% |
| MobileNetV2 | 76.41% | 66.74% | 74.56% |
| EfficientNetB0 | 77.60% | 69.11% | 76.56% |
| **MobileNetV2 Tuned** | **77.84%** | **74.73%** | **77.47%** |

### Results Discussion

- Custom CNN achieved the lowest performance among the evaluated models.
- Transfer Learning significantly improved classification performance.
- EfficientNetB0 achieved strong accuracy and weighted F1-score.
- MobileNetV2 Tuned achieved the best overall results across the three evaluation metrics.
- Hyperparameter optimization improved the balance of classification performance across the six classes.

**Final Selected Model: MobileNetV2 Tuned**

## 🚀 Deployment

The final model was integrated into a Streamlit web application.

### Application Features

- Upload oral images.
- Select a Deep Learning model.
- Predict the oral disease category.
- Display prediction confidence.
- Display probability scores for all six classes.

### Run the Application

Install the required libraries:

```bash
pip install tensorflow streamlit numpy pillow
```

Run the application:

```bash
streamlit run app.py
```

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Streamlit
- Kaggle

## 📁 Project Structure

```text
Oral-Disease-Classification/
│
├── app.py
├── README.md
│
├── models/
│   ├── best_custom_cnn.keras
│   ├── best_mobilenetv2.keras
│   ├── best_tuned_mobilenetv2.keras
│   └── best_efficientnetb0.keras
│
├── results/
│   ├── Model_Comparison.csv
│   ├── Hyperparameter_Tuning_Results.csv
│   ├── Model_Comparison.png
│   └── Classification_Reports/
│
└── notebooks/
    └── Oral_Disease_Classification.ipynb
```

## ⚠️ Limitations

- The dataset has an imbalanced class distribution.
- Some disease categories may have visually similar features.
- Model performance depends on image quality and dataset diversity.
- Predictions are experimental and are not a substitute for professional medical diagnosis.

## 🏁 Conclusion

This project demonstrates the effectiveness of Transfer Learning and Hyperparameter Tuning in oral disease image classification.

Among the evaluated models, **MobileNetV2 Tuned** achieved the best overall performance, with 77.84% test accuracy and a 74.73% Macro F1-score.

The final model was selected for the Streamlit deployment application.

## 👨‍💻 Author

**Tarek Sabry**

Data Science & Deep Learning Enthusiast

---

*Educational and research project only. Not intended for clinical diagnosis or medical decision-making.*
