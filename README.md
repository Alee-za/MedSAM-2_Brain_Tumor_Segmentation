```markdown
# 🧠 MedSAM-2 Brain Tumor Segmentation on Synthetic BRATS Data

This repository contains a complete pipeline for brain tumor segmentation using a simulated version of **MedSAM-2** (Medical Segment Anything Model v2).
 The project uses synthetic BRATS-format MRI data for validation, educational experimentation, and proof-of-concept purposes.

## 🚀 Project Overview
- **Objective**: Demonstrate MedSAM-2 pipeline on synthetic multi-modal MRI data.
- **Data**: Simulated BRATS-style datasets with T1, T1ce, T2, FLAIR modalities.
- **Output**: Tumor segmentation results, visualizations, and evaluation metrics.

## 🧩 Pipeline Components
- `data_generator.py`: Generates synthetic  BRATS-style MRI scans.
- `medsam2_simulator.py`: Simulates the MedSAM 2 segmentation model.
- `evaluator.py`: Evaluates segmentation results using Dice, IoU, Sensitivity, Specificity, Hausdorff.
- `visualizer.py`: Visualizes segmentation masks, difference maps, and metrics.
- `main.py`: Full orchestration script for data creation, segmentation, evaluation, and visualization.

## 🛠️ Installation
```bash
# Optional: create a virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install required dependencies
pip install -r requirements.txt
```

## 📦 File Structure
```
MedSAM2-Brain-Tumor/
├── data_generator.py
├── medsam2_simulator.py
├── evaluator.py
├── visualizer.py
├── main.py
├── requirements.txt
├── results/
│   ├── evaluation_results.csv
│   ├── performance_summary.png
│   └── [BraTS19_xxx_slice_x_comparison.png]
└── README.md
```

## 📊 Evaluation Metrics
| Metric             | Mean ± Std         |
|--------------------|--------------------|
| Dice Score         | 0.017 ± 0.007      |
| Sensitivity        | 0.477 ± 0.064      |
| Specificity        | 0.927 ± 0.000      |
| Hausdorff Distance | 10.01 ± 1.66 mm    |

## 🔍 Results Highlights
- Visual slice-by-slice comparisons
- Performance heatmaps and bar charts
- CSV summary of per-patient metrics

## ❗ Limitations
- Simplified model logic for demonstration
- Synthetic data lacks real tumor variability
- Operates on 2D slices rather than full 3D volumes

## 📈 Future Enhancements
- Integrate real BRATS 2019 dataset
- Use real MedSAM-2 checkpoint for inference
- Extend to 3D volumetric segmentation
- Incorporate advanced training/evaluation frameworks

---

**Author**: Hafiza Aliza Mustafa
```
