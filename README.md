# Speech Recognition CNN

## Overview
This project builds a convolutional neural network (CNN) to classify spoken digits (0–9) from audio recordings using spectrogram-based feature extraction.

Raw audio signals are transformed into spectrograms, allowing the model to interpret audio data as image-like inputs for classification.

---

## Dataset
- Free Spoken Digit Dataset (FSDD)
- Contains `.wav` audio recordings of spoken digits (0–9)
- Multiple speakers and recordings per digit

> Note: The dataset is included in compressed form in the `project-data/Recordings.zip` file.

---

## Methodology

### Data Preparation
- Loaded raw `.wav` audio files from the recordings dataset
- Converted audio signals into structured format (DataFrame)
- Extracted digit labels from filenames

### Feature Engineering
- Generated spectrograms from audio signals using signal processing techniques
- Converted spectrograms to log scale (dB)
- Standardized spectrogram dimensions using padding

### Modeling
- Built a Convolutional Neural Network (CNN)
- Used spectrograms as image-like inputs
- Applied convolutional and pooling layers followed by dense layers

### Training
- Train/test split (80/20)
- Optimized using Adam optimizer
- Loss function: sparse categorical cross-entropy

---

## Results
- Test accuracy: ~95%
- Model successfully classifies spoken digits across multiple speakers
- Spectrogram-based features provide strong performance for audio classification

---

## Key Insights
- Spectrograms enable audio data to be processed effectively using CNNs
- Even relatively simple CNN architectures can achieve high accuracy
- Feature representation plays a critical role in model performance

---

## Repository Structure

```
speech-recognition-cnn/
│
├── notebooks/
│   ├── CNN_Spoken_Digit_Recognition_Clean_Code.ipynb
│   └── Spoken_Digit_Recognition_CNN_Original_Code.ipynb
│
├── project-data/
│   └── Recordings.zip
│
├── report/
│   ├── Spectrogram-based CNN Final Report.pdf
│   └── Spectrogram-based CNN Final Report.docx
│
└── README.md
```

---

## How to Run

### Option 1: Google Colab (Recommended)
1. Upload or mount your Google Drive  
2. Extract `Recordings.zip`  
3. Update the `folder_path` in the notebook to point to the extracted `recordings` folder  
4. Run all cells  

---

### Option 2: Local Environment
1. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib scipy scikit-learn tensorflow
   ```
2. Extract `Recordings.zip`  
3. Update the `folder_path` variable to the recordings directory  
4. Run the notebook  

---

## Tools & Technologies
- Python  
- NumPy / pandas  
- SciPy (signal processing)  
- TensorFlow / Keras  
- matplotlib  

---

## Limitations
- Small dataset size  
- Limited to digit classification (0–9)  
- Performance may vary on unseen speakers  

---

## Future Work
- Expand to larger speech datasets  
- Explore more advanced architectures (RNNs, transformers)  
- Improve generalization across speakers  

---

## Author
Waleed Jamil  
Syracuse University – Applied Data Science
