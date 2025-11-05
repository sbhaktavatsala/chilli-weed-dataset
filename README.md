# chilli-weed-dataset
Annotated chilli crop–weed dataset for precision agriculture research
# 🌿 Chilli Crop–Weed Detection Dataset  
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)  
[![Made with Python](https://img.shields.io/badge/Made%20with-Python-blue.svg)](https://www.python.org/)  
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](https://github.com/username/chilli-weed-dataset/issues)  
[![IEEE Paper](https://img.shields.io/badge/IEEE-ICONEECT%202025-red)](#citation)  

---

## 📘 Overview
This repository hosts the **Chilli Crop–Weed Detection Dataset**, developed as part of the research work:

> **“Deep Learning–Based Crop–Weed Detection Framework for Precision Agriculture in Chilli (Capsicum annuum L.) Cultivation”**,  
> *submitted to the IEEE International Conference on Electronics, Electrical, and Communication Technologies (ICONEECT 2025), MITS Gwalior, India.*

This dataset is designed for developing and evaluating **deep learning models** such as YOLOv5, YOLOv11, MobileViT, and EfficientNet for **automated crop–weed detection and classification** under real-field agricultural conditions.

---

## 📂 Dataset Description
| **Attribute** | **Description** |
|----------------|----------------|
| **Total Images** | 2,200 RGB images |
| **Resolution** | 1280 × 720 px |
| **Format** | JPEG + Pascal VOC (.xml) + YOLO (.txt) |
| **Classes** | `0 - Crop`, `1 - Weed` |
| **Capture Device** | Handheld and UAV RGB cameras |
| **Locations** | Agricultural fields, Southern India |
| **Growth Stages** | Early vegetative → flowering |
| **Variations** | Soil texture, illumination, weed density, occlusion |

---

## 🧠 Annotation Details
Annotations were created using **LabelImg** and **Roboflow**.  
Both YOLO and Pascal VOC formats are included.

Example YOLO annotation:
0 0.521 0.447 0.125 0.182
1 0.317 0.526 0.146 0.207

yaml
Copy code
where `0 = Crop` and `1 = Weed`.

---

## 🧩 Repository Structure
chilli-weed-dataset/
│
├── Images/
│ ├── Train/
│ ├── Validation/
│ └── Test/
│
├── Annotations_XML/ # Pascal VOC (.xml)
├── Annotations_YOLO/ # YOLO (.txt)
├── data/chilli.yaml # Dataset config file for YOLO training
└── README.md

yaml
Copy code

---

## ⚙️ Quick Start

### 🔸 Clone and Setup
```bash
git clone https://github.com/username/chilli-weed-dataset.git
cd chilli-weed-dataset
🔸 Train with YOLOv5 (Example)
bash
Copy code
python train.py --data data/chilli.yaml --img 640 --batch 16 --epochs 100 --weights yolov5s.pt
📊 Benchmark Summary
Model	mAP@0.5	mAP@0.5:0.95	FPS
YOLOv11	0.92	0.90	58
YOLOv5	0.91	0.78	45
ResNet-101	0.88	0.68	5
MobileViT	0.80	0.80	15
HSV + Edges	0.25	0.20	25

📸 Sample Images
Field Conditions	Detection Outputs
<img src="samples/chilli_field.jpg" width="400"/>	<img src="samples/detection_output.jpg" width="400"/>

📜 License
This dataset is released under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.
You may use and modify the data for academic and non-commercial research, provided proper attribution is given.

java
Copy code
© 2025 Bhaktavatsala Shivaram et al.,

🧾 Citation
If you use this dataset or results in your research, please cite:

bibtex
Copy code
@inproceedings{shivaram2025chilliweed,
  author    = {Bhaktavatsala Shivaram and T. K. Ramesh and J. Kumar},
  title     = {Deep Learning–Based Crop–Weed Detection Framework for Precision Agriculture in Chilli Cultivation},
  booktitle = {Proc. IEEE Int. Conf. on Electronics, Electrical, and Communication Technologies (ICONEECT)},
  year      = {2025},
  address   = {MITS Gwalior, India}
}

@misc{shivaram2025dataset,
  author    = {Bhaktavatsala Shivaram},
  title     = {Chilli Crop–Weed Detection Dataset},
  year      = {2025},
  howpublished = {\url{https://github.com/username/chilli-weed-dataset}},
  note      = {Accessed November 2025}
}
🤝 Acknowledgments
This dataset was developed with support from:

Department of Electronics & Communication Engineering, Amrita

Special thanks to the field teams (Puttaswamy M, Pavan Gowda M P, Prajwal Narayan, Varun Gowda, and Rangaswamy for their help in sowing chilli saplings and collecting images from the agricultural field.)  and annotation volunteers (Hemanth) who contributed to dataset curation.

🔗 Related Resources
YOLOv11 – Ultralytics (2024)

MobileViT – Lightweight Vision Transformer

EfficientNet – Scalable CNN Architectures

⭐ If you find this dataset useful, please star the repository!
Your citation and feedback will support further open-source research in AI-driven precision agriculture.

---






You said:

