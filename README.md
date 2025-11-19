AD-MoE

This repository contains the official implementation of the AD-MoE model.

This project is built upon the Time-Series-Library (TSLib) framework developed by Tsinghua University. We have migrated the original command-line based execution (.sh scripts) to an interactive Jupyter Notebook (.ipynb) environment to facilitate results visualization, code debugging, and analysis.

📚 Directory Structure

The project consists of the following core directories:

AD-MoE/
├── data_provider/      # Data loading and processing logic
├── exp/                # Experiment execution scripts (Train/Vali/Test functions, adapted from TSLib)
├── layers/             # Basic neural network layers (from TSLib)
├── models/             # Model definitions
│   ├── AD_MoE.py             # [Core Code] Main file for the AD-MoE model
│   ├── ablation_variants.py  # [Core Code] Model variants for ablation studies
│   └── ...                   # Other built-in TSLib models (Transformer, DLinear, etc.)
├── tutorial/           # Running scripts and tutorials (Jupyter Notebooks)
│   ├── process_Data.ipynb    # Data preprocessing script
│   ├── forecasting.ipynb     # Main experiment script (AD-MoE model)
│   ├── baseline.ipynb        # Script for running baseline models
│   ├── ABLATION.ipynb        # Script for running ablation studies
│   ├── checkpoints/          # (Auto-generated) Path for saving model weights
│   └── test_results/         # (Auto-generated) Prediction results and visualization outputs
└── utils/              # General utility functions


🧬 Model Introduction

The following core code is implemented in the models directory:

AD_MoE.py: The architecture of the AD-MoE model proposed in this paper.

ablation_variants.py: Model variants used to verify the effectiveness of different components in ablation studies.

Additionally, we have retained the mainstream time series forecasting models organized in TSLib as baselines for comparison.

💾 Datasets

Note: The original dataset used in the paper involves confidential information and cannot be made public.

In this repository, we use the ETTh1 (Electricity Transformer Temperature) dataset as a demonstration example to ensure that the code runs smoothly and the experimental process can be reproduced.

Data processing logic is located in the data_provider folder.

If you need to use custom data, please refer to tutorial/process_Data.ipynb for preprocessing.

🚀 Usage

Unlike the traditional TSLib which uses terminal .sh files, this project uses the more user-friendly Jupyter Notebook format. Please run the code in the tutorial folder in the following order:

1. Environment Preparation

Please ensure that the necessary Python dependencies are installed (Python 3.8+ is recommended).

2. Run Main Experiment (Forecasting)

Open and run tutorial/forecasting.ipynb.

This file contains the complete process for model training, validation, and testing.

The core model AD_MoE is called here.

After execution, model weights will be saved to tutorial/checkpoints/, and prediction results will be saved to tutorial/test_results/.

3. Run Comparison Experiments (Baselines)

Open and run tutorial/baseline.ipynb.

This file is configured with the environment for running baseline models to generate comparison data.

4. Run Ablation Studies

Open and run tutorial/ABLATION.ipynb.

This file calls the model variants in models/ablation_variants.py to verify the contribution of each module.

📊 Results

All experimental output results (including logs, visualization charts, and prediction values) will be automatically saved in the following two folders under the tutorial directory:

checkpoints/: Stores trained model parameters.

test_results/: Stores prediction result files for the test set (usually numpy arrays or visualization images).

🔗 Acknowledgement

The code framework of this project is primarily based on the Time-Series-Library open-sourced by the Machine Learning Group of the School of Software, Tsinghua University (THUML). We are very grateful for their outstanding contributions and organization in the field of time series analysis.

Time-Series-Library (TSLib): https://github.com/thuml/Time-Series-Library
