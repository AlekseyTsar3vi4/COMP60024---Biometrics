# 🔐 Biometric Evaluation Suite

This repository provides a unified notebook to evaluate three biometric systems - **Face**, **Fingerprint**, and **Voice** -based on industry-standard metrics such as **FMR**, **FNMR**, **EER**, **ATV**, **FTER**, and **ATSR**.

> 📘 Built by Alexei Gaicovschi; Pratik Gami and Ade Adeyemi using PyTorch, OpenCV, Librosa, and scikit-learn. All metrics were derived from experiments and visualised in Google Colab using real biometric datasets.

---

## 🚀 Run the Notebook in Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qXaYSXdy7-p7yqsTMPRbr97quCwPrC1H?usp=sharing)

---

## 🧠 Supported Biometric Modalities

| Modality    | Description |
|-------------|-------------|
| **Face**    | CNN-based classifier trained on LFW with adversarial and morphing attack detection |
| **Voice**   | MFCC and Wav2Vec2 triplet embedding with spoof tests (noise, pitch, speed, reverse) |
| **Fingerprint** | CNN classifier and spoof detector with morph, blur, rotate, and low-res attacks |

---

## 📊 Evaluation Metrics Summary

| Metric   | Face | Fingerprint | Voice |
|----------|------|-------------|-------|
| **EER**  | 0.000 | 0.000       | 0.00 → 0.67 |
| **FMR**  | 0.000 | 1.000 (spoof accepted) | 0.00 → 0.75 |
| **FNMR** | 0.000 | 0.000       | 0.00 → 0.67 |
| **FTER** | 0.000 | 0.000       | 0.000       |
| **ATV**  | 1.000 | 1.000       | 1.00 → 0.33 |
| **ATSR** | 0.000 | 1.000       | 0.83 → 0.98 |

---

## 🧪 Attack Examples

| Adversarial Types Tested |
|--------------------------|
| Face: FGSM, Morphing, Brightness, Occlusion, Flip, Rotation |
| Fingerprint: Morph, Blur, Rotate, Low-res |
| Voice: Pitch shift, Speed change, Noise addition, Reverse |

📸 See attack samples in the `assets/` folder or within the Colab notebook.

---

## 📁 Project Directory (Google Drive Structure)

| Path | Description |
|------|-------------|
| `OS&BIOMETRICS/content/Finger samples/` | Fingerprint dataset |
| `OS&BIOMETRICS/content/lfw-deepfunneled/` | Face dataset |
| `OS&BIOMETRICS/content/cv-corpus-19.0/` | Voice samples (Common Voice) |
| `OS&BIOMETRICS/models/` | Trained model checkpoints |

---

## 🔐 Security Recommendations Summary

✅ Use multi-modal biometrics  
✅ Apply anti-spoof measures (e.g. liveness, challenge-response)  
✅ Encrypt stored biometric templates (GDPR-compliant)  
✅ Regular adversarial testing/audits

See the full **[Cost vs Impact Matrix](#)** and [Appendix Summary Table](#) for deployment guidance.


## 📬 Contact

For academic collaboration or project reuse, please contact:

**Alexei Gaicovschi - g028335l@student.staffs.ac.uk**; **Pratik Gami**; **Ade Adeyemi**
