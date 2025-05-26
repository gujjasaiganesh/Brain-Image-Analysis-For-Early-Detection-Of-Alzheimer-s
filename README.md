
# 🧠 Alzheimer's Disease Detection with EfficientNetB3 + Grad-CAM

Welcome to a deep learning project built to **detect and visualize stages of cognitive impairment** using MRI image classification powered by **EfficientNetB3** and **Grad-CAM heatmaps**.

> 💡 This model not only predicts **"Mild", "Moderate", "Very Mild", or "No Impairment"**, but also visually **highlights the key regions** of the brain MRI contributing to the prediction—giving insights you can trust.

---

## 🚀 Key Features

- 🧠 **Multiclass Classification** of Alzheimer's disease stages.
- ⚙️ Built using **TensorFlow Keras Functional API** for flexibility and Grad-CAM compatibility.
- 🧰 Utilizes **EfficientNetB3**, pretrained on ImageNet, for transfer learning.
- 🔍 **Grad-CAM Visualizations** with special blue-yellow heatmaps for “No Impairment” cases.
- 📊 Accuracy, Loss, Time-per-Epoch graphs and Confusion Matrix for evaluation.
- 📁 Supports image datasets structured by class folders (e.g., Mild Impairment, Moderate Impairment, etc.).
- 🧪 Automatically generates prediction reports with **confidence scores**.
- 💾 Saves trained model and CSV outputs for further analysis.

---

## 📂 Dataset Format

Expected dataset folder structure:

```
train/
├── Mild Impairment/
├── Moderate Impairment/
├── No Impairment/
└── Very Mild Impairment/
```

Make sure your images are organized in this way before running the model.

---

## 🧪 How to Run This Project in Google Colab

1. **Open Google Colab**  
   Go to [Google Colab](https://colab.research.google.com) in your browser.

2. **Upload the Python Script**  
   - Click on the folder icon (left sidebar).  
   - Click the upload icon and upload the `project.py` file.

3. **Mount Google Drive**  
   If you are using files from Google Drive, run:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

4. **Install Dependencies**

   Run the following in a code cell to install required packages:

   ```bash
   !pip install tensorflow keras numpy pandas matplotlib seaborn opencv-python
   ```

5. **Run the Python Script**

   Either copy and run code cells manually or run the whole script:

   ```bash
   !python project.py
   ```

6. **Modify and Experiment**

   You can also split code into cells for step-by-step editing and visualization.

7. **Save Results Back to Google Drive**

   Example:

   ```bash
   !cp /content/test_predictions.csv /content/drive/MyDrive/
   ```

---

## 📈 Training Curves

Automatically plots:

- 📉 Training vs Validation Accuracy  
- 🔥 Training vs Validation Loss  
- ⏱️ Time per Epoch (performance trend)

---

## 🖼️ Grad-CAM Example

Special Grad-CAM visualization uses:

- 🔵🟡 Blue-yellow heatmap for **"No Impairment"**
- 🔴 Red-based heatmaps for other stages
- Overlays heatmaps on original MRI scans

---

## 📬 Future Work

- Add GUI/Flask web interface for user upload & diagnosis
- Integrate with medical imaging databases
- Support DICOM format

---

## 🙌 Acknowledgements

- [TensorFlow](https://www.tensorflow.org/)
- [EfficientNet](https://arxiv.org/abs/1905.11946)
- [Grad-CAM Paper](https://arxiv.org/abs/1610.02391)
- Dataset Source: [ADNI / Kaggle Dataset (assumed)]

---

## 📜 License

This project is for educational and research use only. Medical diagnostics should always be confirmed by professionals.
