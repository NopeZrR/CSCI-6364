# ViT vs. Baseline Algorithms for EEG-based Gaze Prediction

## Overview
This project explores the performance of a convolutional neural network(CNN) model on the EEG-based gaze prediction task from the EEGEyeNet dataset. I compare this with two baseline algorithms: **Lasso Regression** and **Random Forest**. The specific task used from the EEGEyeNet dataset is `Position_task_with_dots_synchronised_min`. Due to limited experience with hyperparameter tuning, the performance of all three models has been suboptimal, and further adjustments are planned.

## Dataset Download
To download the dataset, use the following command:
```bash
wget -O "./dataset/Position_task_with_dots_synchronised_min.npz" "https://osf.io/download/ge87t/"
```

## Installation

### General Requirements
We recommend using Conda to install general requirements:
```bash
conda install --file general_requirements.txt
```

### PyTorch Requirements
For PyTorch and related dependencies, use Conda with the following command:
```bash
conda install -c pytorch torch torchvision torchaudio
```

## Usage

### Data Loading
Upload the dataset file in your Google Drive, and load it with the following code:
```python
from google.colab import drive
drive.mount('/content/drive')

import sys
sys.path.append('/content/drive/MyDrive/Colab Notebooks/CNN_Test')

from EEGEyeNet import EEGEyeNetDataset

data_file_path = '/content/drive/MyDrive/Colab Notebooks/Position_task_with_dots_synchronised_min.npz'
```

## Hyperparameter Tuning
To further optimize the model, consider adjusting the following hyperparameters:
- **Learning Rate**: Try a lower or higher learning rate to improve model stability.
- **Batch Size**: Depending on hardware, experiment with smaller or larger batch sizes to observe the impact on training.
- **Network Depth**: Adjust the number of CNN layers to modify model complexity.

## Future Work
Future plans include exploring alternative baseline algorithms and model architectures to improve performance on the EEG-based gaze prediction task.

## License
This project is licensed under the MIT License. Contributions and suggestions are welcome.

