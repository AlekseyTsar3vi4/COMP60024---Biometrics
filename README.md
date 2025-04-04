# 🔐 Biometric Evaluation Suite

This repository provides a unified notebook to evaluate three biometric systems - **Face**, **Fingerprint**, and **Voice** -based on industry-standard metrics such as **FMR**, **FNMR**, **EER**, **ATV**, **FTER**, and **ATSR**.

> 📘 Built by Alexei Gaicovschi; Pratik Gami and Ade Adeyemi using PyTorch, OpenCV, Librosa, and scikit-learn. All metrics were derived from experiments and visualised in Google Colab using real biometric datasets.

---

## 🚀 Run the Notebook in Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qXaYSXdy7-p7yqsTMPRbr97quCwPrC1H?usp=sharing)

---

## 📁 Project Structure

```bash
biometric-evaluation-suite/
├── biometric_evaluation_notebook.ipynb       # 📘 Main practical notebook (Colab-ready)
├── models/                                   # 🧠 Pretrained Models
│   ├── fingerprint_cnn.pt
│   ├── fingerprint_resnet18.pt
│   ├── wav2vec2_triplet_5_speakers.pth
│   └── wav2vec2_triplet_8_speakers.pth
└── data/                                     # 📂 Datasets
    ├── Finger samples/                       # Fingerprint images (.tif)
    ├── lfw-deepfunneled/                     # Face dataset (LFW + match CSVs)
    └── cv-corpus-19.0-delta-2024-09-13-en/   # Voice dataset (Common Voice v19 EN)
```

## 🧠 Supported Biometric Modalities

| Modality    | Description |
|-------------|-------------|
| **Face**    | CNN-based classifier trained on LFW with adversarial and morphing attack detection |
| **Voice**   | MFCC and Wav2Vec2 triplet embedding with spoof tests (noise, pitch, speed, reverse) |
| **Fingerprint** | CNN classifier and spoof detector with morph, blur, rotate, and low-res attacks |

---

## 🔗 Required Downloads (Google Drive Only)

Due to size limitations on GitHub, **all datasets and models must be downloaded manually** from the following Drive links:

| 📂 Resource | 🔗 Google Drive Link |
|------------|----------------------|
| 🧠 Pretrained Models (CNN, ResNet18, Wav2Vec2) | [Models Drive Folder](https://drive.google.com/drive/folders/1faXs5e6hUYbE5wOodiztZjFaSqwAXfgX?usp=sharing) |
| 🔊 Voice Dataset (Common Voice v19) | [Voice Corpus Folder](https://drive.google.com/drive/folders/1egpCptKTutadubFm_o1NrKpHHaxw_-IQ?usp=sharing) |
| 🧷 Fingerprint Dataset (TIF images) | [Fingerprint Folder](https://drive.google.com/drive/folders/1tiXDyNK4uRjc6Jm6t7s9FiwJPwkzOjak?usp=sharing) |
| 🧑‍🤝‍🧑 Face Dataset (LFW Deepfunneled) | [LFW Folder](https://drive.google.com/drive/folders/1GmLJSTt09nH4QO0iEC2baGmN-na8y6t5?usp=sharing) |

Once downloaded, place the files in your mounted `/content/drive/MyDrive/OS&BIOMETRICS/content/` directory.

---

## ✅ Evaluation Metrics Used

- **FMR** – False Match Rate  
- **FNMR** – False Non-Match Rate  
- **EER** – Equal Error Rate  
- **FTER** – Failure to Enrol Rate  
- **ATV** – Ability to Verify  
- **ATSR** – Ability to Spoof Rate

---

## 📊 Highlights

- 🔍 Real-world spoofing attacks: adversarial faces, morphed fingerprints, pitch/voice manipulations.
- 📈 Metric visualisation: ROC curves, spoof confusion matrices, training loss and accuracy.
- 🧠 Models: CNN, ResNet18, Wav2Vec2 Triplet networks.
- 🧪 Dataset coverage across all modalities with reproducible pipelines.

---

## 🚀 How to Run

1. **Open** the `biometric_evaluation_notebook.ipynb` in Google Colab.
2. **Mount Google Drive** in Colab.
3. **Download required assets** from the links above and place them in `/content/drive/MyDrive/OS&BIOMETRICS/content/`.
4. **Run each section** and examine inline results.

---

## 🧪 Attack Examples

| Adversarial Types Tested |
|--------------------------|
| **Face:** FGSM, Morphing, Brightness, Occlusion, Flip, Rotation |
| **Fingerprint:** Morph, Blur, Rotate, Low-res |
| **Voice:** Pitch shift, Speed change, Noise addition, Reverse |

📸 See attack samples within the Colab notebook.

---

## 📬 Contact

For academic collaboration or project reuse, please contact:

**Alexei Gaicovschi - g028335l@student.staffs.ac.uk** 
**Pratik Gami - g013176l@student.staffs.ac.uk**; 
**Ade Adeyemi - a016719l@student.staffs.ac.uk**

---

## 📎 License

This project is for educational purposes only. All external datasets must be used under their respective licenses. No biometric data used here is linked to real identities.
