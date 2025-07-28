# drdo-noise-cancellation-dl
Implementation of adaptive voice noise cancellation using deep learning models as part of my summer internship at DRDO-DEAL. Includes custom dataset creation, audio preprocessing, and model evaluation (UNet, LSTM, CNN) for speech denoising.
# 🎧 Adaptive Noise Cancellation using Deep Learning

**Summer Internship Project | DRDO-DEAL, Dehradun (June–July 2025)**  
By Nandini Singh

---

## 📌 Overview

This project focuses on **adaptive noise cancellation** using **deep learning models**. The objective is to remove environmental and electronic noise (static and dynamic) from speech signals while preserving voice clarity. This was carried out as part of my internship at **Defence Electronics Application Laboratory (DEAL), DRDO, Dehradun**.

---

## 📁 Dataset

A **custom dataset** was created using clean voice audio mixed with various types of noise:

- **Clean Voice:** Publicly available clean speech recordings
- **Static Noise:** Radio hums
- **Dynamic Noise:** Wind, Helicopter, Explosion, Gunfire  
- **Sources:** Noise samples were obtained from **Kaggle** and **YouTube**, and processed using **Python**, **Librosa**, and **Soundfile**.

The final dataset includes:
- Clean audio
- Mixed audio (clean + static + dynamic)
- Spectrogram representations (STFT, Log-Mel)

---

## 🧠 Models Explored

| Model             | Status        | Notes                                |
|------------------|---------------|--------------------------------------|
| LMS / RLS        | ✅ Explored    | Traditional adaptive filtering       |
| CNN              | ❌ Failed      | Poor denoising, overfitting          |
| LSTM             | ❌ Failed      | Blurred speech output                |
| CNN Autoencoder  | ❌ Failed      | Ineffective in removing noise        |
| **UNet**         | ✅ Successful  | Best results with PSNR: **49.32 dB** |

UNet was applied on **Log-Mel spectrograms** and gave the best performance in terms of speech clarity and noise reduction.

---

## 🧪 Evaluation

- **Quantitative Metrics:**
  - PSNR (Peak Signal-to-Noise Ratio): *49.32 dB with UNet*
- **Qualitative Analysis:**
  - Waveform and spectrogram comparison
  - Audio playback listening tests

---

## 🔧 Tools & Libraries

- **Languages:** Python  
- **Libraries:**  
  - Librosa, NumPy, Soundfile, Matplotlib  
  - TensorFlow / PyTorch  
- **Platforms:** Google Colab, Jupyter Notebook

---

## 📂 Folder Structure (Suggested)

