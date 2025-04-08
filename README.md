# 🇷🇺 Russian Sign Language Alphabet Recognition (Bukva Dataset)

This project trains an action recognition model to classify Russian Sign Language (RSL) fingerspelling letters using the [Bukva dataset](https://github.com/ai-forever/bukva).  
It is based on the [MMAction2](https://github.com/open-mmlab/mmaction2) framework and uses the TSM architecture with a MobileNetV2 backbone.

---

## 📁 Project Structure

generate_split_files.py # Generates train/val file lists 
tsm_mobilenetv2_bukva.py # Training configuration
plot_training_log.py # Training visualization (loss/accuracy) 
train.txt / val.txt # Paths and labels for training
annotations.tsv # Annotation file 
videos_cropped/ # Video clips (excluded from Git)

# 🚀 Quickstart

### 1. Install dependencies

pip install -r requirements.txt
If not available: install manually torch, mmengine, mmaction2, mmcv, matplotlib, pandas, etc.

**Prepare the dataset**

Download the following from Bukva Dataset:

    annotations.tsv

    videos_cropped/ (trimmed video clips)

Place them in:
gluh/bukva/

**Generate training splits**
python generate_split_files.py
This creates train.txt and val.txt with paths and labels.

**Train the model**
cd mmaction2
python tools/train.py ../gluh/tsm_mobilenetv2_bukva.py

**Visualize training progress**
python ../gluh/plot_training_log.py

**Tech Stack**

    Python 3.10+

    PyTorch 2.1 (CPU or CUDA)

    MMEngine, MMAction2, MMCV 2.x

    TSM (Temporal Shift Module) + MobileNetV2

    Bukva Dataset

**Dataset**

    Source: Bukva Dataset

    Authors: Sber AI, 2024

    Paper: Bukva: Russian Sign Language Alphabet

    Author

Developed by @PavelAndreyev
Feel free to open issues or contribute with pull requests!

MIT License. 
