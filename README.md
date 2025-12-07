# 📘 Pose86K-CSLR-Isharah  
### Continuous Sign Language Recognition using Pose Keypoints  
### ICS471 – Final Project

This repository provides:

1. A **Google Colab notebook**: `ICS471_ishara.ipynb`  
2. A **zipped project folder**: `Pose86K-CSLR-Isharah.zip` (code + data structure): https://drive.google.com/file/d/1iF-x0Iiv_iDAM1pLQxXaywQ3rViQdqbF/view?usp=sharing

The user is expected to:

- **Download the zipped project from GitHub**
- **Extract it locally**
- **Upload the extracted folder to Google Drive** (inside a folder called `My_Drive`)
- **Open the notebook in Colab and run everything from there**

All training, evaluation, and analysis are done inside **Colab**, using the project folder stored in the user’s own Google Drive.

---

## 🚀 Project Goal

We build a **pose-based Continuous Sign Language Recognition (CSLR)** system on the **Pose86K-CSLR-Isharah** dataset and compare three models:

1. **Simple BiLSTM** (our basic baseline)  
2. **Improved BiLSTM** (stronger recurrent model)  
3. **Improved Encoder-only Transformer** (best model)

All models operate on **pose keypoints** (86 per frame):

- Upper body skeleton  
- 2D hand keypoints (left & right hands)  
- Face keypoints  
- Lips contour  

The task is **signer-independent**:  
Training and evaluation are done on disjoint signer sets.

---

## 📁 What’s Inside This Repository?

You will find at least:

- a link to `Pose86K-CSLR-Isharah.zip` – https://drive.google.com/file/d/1iF-x0Iiv_iDAM1pLQxXaywQ3rViQdqbF/view?usp=sharing 
- `ICS471_ishara.ipynb` – the main Colab notebook  

After extracting `Pose86K-CSLR-Isharah.zip`, the folder structure looks like:

```text
Pose86K-CSLR-Isharah/
│── annotations_v2/         # Train/dev/test annotation txt files
│── data/                   # Pose data files (e.g. pickle / npz per sequence)
│── models/
│     ├── lstm.py           # Simple + improved LSTM implementations
│     ├── transformer.py    # Basic + improved encoder-only Transformer
│── utils/                  # Decoding, metrics, dataset utilities, etc.
│── main.py                 # Training + validation loop
│── test_script.py          # Test-set inference script
│── data_loader_test.py     # Data loader for test inference
