🌀 AD-MoE: Adaptive Dilation Mixture-of-Experts for Time Series Forecasting
<p align="center"> <img src="https://raw.githubusercontent.com/github/explore/main/topics/time-series/time-series.png" width="120"> </p> <p align="center"><b>Multi-scale · Adaptive · Efficient · Accurate</b></p> <p align="center"> <a href="https://github.com/thuml/Time-Series-Library"><img src="https://img.shields.io/badge/Base-TSLib-blue?logo=tensorflow&logoColor=white"></a> <img src="https://img.shields.io/badge/Python-3.8+-blue.svg?logo=python"> <img src="https://img.shields.io/badge/PyTorch-1.12+-red.svg?logo=pytorch"> <img src="https://img.shields.io/badge/License-MIT-green.svg"> <img src="https://img.shields.io/badge/Status-Active-brightgreen"> </p>
⭐ Overview

AD-MoE (Adaptive Dilation Mixture-of-Experts) is a time-series forecasting framework built on top of Tsinghua University’s Time Series Library (TSLib).

To ensure data confidentiality for industrial projects, this repository demonstrates the workflow using the public ETTh1 dataset.
All experiments are designed to run inside Jupyter Notebooks, allowing easy visualization and reproducibility without requiring terminal .sh scripts.

📁 Repository Structure
AD-MoE/
│
├── data_provider/             # Data loading & preprocessing
├── exp/                       # Training/validation/testing logic (adapted from TSLib)
├── layers/                    # Neural network layers used by models
├── models/
│     ├── AD_MoE.py            # Main AD-MoE model
│     ├── ablation_variants.py # Ablation experiment variants
│     └── ...                  # Baseline models from TSLib
│
├── tutorial/
│     ├── forecasting.ipynb        # Main experiment notebook
│     ├── ABLATION.ipynb           # Ablation studies
│     ├── baseline.ipynb           # Baseline model comparison
│     └── process_Data.ipynb       # ETTh1 preprocessing example
│
├── utils/                    # Helper tools
├── checkpoints/             # Auto-saved model weights
└── test_results/            # Auto-saved predictions & metrics

🛠 Installation
Clone the repository and install dependencies:
git clone https://github.com/YourName/AD-MoE.git
cd AD-MoE
pip install -r requirements.txt

Installation Flow (Diagram)
+------------------------------------------------------+
| Step 1: Clone the repository                         |
| git clone https://github.com/YourName/AD-MoE.git     |
+------------------------------------------------------+
                         |
                         v
+------------------------------------------------------+
| Step 2: Install required dependencies                |
| pip install -r requirements.txt                      |
+------------------------------------------------------+
                         |
                         v
+------------------------------------------------------+
| Step 3: Launch Jupyter Notebook                      |
| jupyter notebook                                     |
+------------------------------------------------------+

🚀 Quick Start
1. Run the forecasting experiment

Open:

tutorial/forecasting.ipynb


This notebook includes:

ETTh1 data loading

AD-MoE training and validation

Evaluation and visualization

Automatic saving to /checkpoints and /test_results

2. Run ablation studies

Open:

tutorial/ABLATION.ipynb


Ablation variants are implemented in:

models/ablation_variants.py


Available variants:

Variant	Description
A1: RandomFusion	Replace learnable gating with random weights
A2: No-TCN	Disable temporal encoder
A3: FixedGating	Use constant fusion weights
3. Run baseline models

Open:

tutorial/baseline.ipynb


This notebook reproduces multiple TSLib baseline models and compares them with AD-MoE.

🎯 Model Architecture (Placeholder)

Replace the image below with your actual AD-MoE architecture diagram (PNG/SVG).

<p align="center"> <img src="https://raw.githubusercontent.com/github/explore/main/topics/machine-learning/machine-learning.png" width="480"> </p> <p align="center"><i>▲ Placeholder for AD-MoE Architecture</i></p>
📈 Example Results (Placeholder)

You may insert forecasting curves, loss plots, or ablation charts here.

<p align="center"> <img src="https://raw.githubusercontent.com/github/explore/main/topics/matplotlib/matplotlib.png" width="520"> </p> <p align="center"><i>▲ Placeholder for experimental results</i></p>
📚 Acknowledgements

This repository builds upon:

Tsinghua University — Time Series Library (TSLib)

https://github.com/thuml/Time-Series-Library

We greatly appreciate their contributions to the time-series research community.

📜 License

This project is released under the MIT License.

📩 Contact

For questions, collaboration, or industrial applications of time-series modeling, feel free to reach out:

Email: danniew@yeah.net
